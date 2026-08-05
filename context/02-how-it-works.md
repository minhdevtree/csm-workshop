# CSM hoạt động thế nào

Chỉ mô tả kiến trúc ở mức đủ để nói chuyện trong workshop. Không có mã nguồn ở đây.

## Ba lớp

| Lớp | Công nghệ | Việc nó làm |
|---|---|---|
| Electron main | Node trong tiến trình main | Đẻ và giữ PTY, đọc git, phục vụ IPC |
| Renderer | Next.js (Pages Router), Tailwind v4, shadcn/Radix | Toàn bộ giao diện |
| Terminal | xterm.js 6 + node-pty | Hiển thị và nhận phím của phiên |

Điểm mấu chốt: **PTY sống ở tiến trình main, không sống trong tab.** Chuyển tab chỉ
gắn hoặc gỡ phần hiển thị xterm. Tiến trình `claude` chạy tiếp không hề biết.
Đó là lý do đóng tab không giết phiên.

## Trạng thái tới từ đâu

Đây là phần đáng nói nhất trong workshop, vì nó là thứ phân biệt "biết agent đang
chờ" với "đoán agent đang chờ".

Claude Code có cơ chế **hooks**: nó gọi ra ngoài tại các thời điểm trong vòng đời một
lượt. CSM tận dụng bằng cách:

1. Khi mở một phiên, CSM sinh một file settings tạm cho **riêng phiên đó**, có nhúng
   sẵn id phiên và số cổng loopback.
2. Truyền file đó qua cờ `--settings` của Claude CLI. File settings thật của người
   dùng (`~/.claude/settings.json`) không bị đụng tới.
3. Claude Code bắn hook, hook POST về `http://127.0.0.1:<port>` trong tiến trình main.
4. Main quy đổi sự kiện thành trạng thái và đẩy sang renderer.

Các sự kiện hook CSM lắng nghe: `SessionStart`, `UserPromptSubmit`, `PreToolUse`,
`PostToolUse`, `PermissionRequest`, `Notification`, `Stop`, `SessionEnd`.

Năm trạng thái hiển thị bằng một chấm động trong sidebar:

| Trạng thái | Ý nghĩa |
|---|---|
| `idle` | `claude` đang chạy nhưng im |
| `working` | đang xử lý prompt |
| `waiting` | **đang chờ bạn duyệt hoặc trả lời** |
| `done` | vừa trả lời xong, nháy rồi về idle |
| `ended` | tiến trình đã thoát |

Khi chưa có hook nào tới, hoạt động đầu ra của PTY sẽ tạm đóng vai trò tín hiệu.
Nhưng chấm **không bao giờ** hiện `waiting` chỉ từ đầu ra: chờ là một sự kiện, không
phải một suy đoán.

## Chú ý được đẩy ra bốn nơi

Khi một phiên chuyển sang `waiting`: badge trong app, thông báo hệ điều hành, badge
trên dock, và một tiếng chuông ngắn. Bật tắt riêng từng cái trong Settings.

## Chế độ remote

Máy chạy CSM có thể tự phục vụ chính giao diện của nó qua HTTP cho máy khác trong
mạng. Điện thoại mở bằng trình duyệt là điều khiển được phiên đang chạy trên máy bàn.
Kênh IPC nào được phép đi qua remote là một danh sách trắng khai báo tường minh, và
có một danh sách hẹp hơn nữa cho token chỉ đọc.
