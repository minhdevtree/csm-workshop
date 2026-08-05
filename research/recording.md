# Cách quay GIF demo bằng harness tự động

7 trong 11 GIF được quay tự động, không thao tác tay. Ghi lại đây để lần sau khỏi
dò lại từ đầu.

## Cách chạy

Harness nằm trong scratchpad của phiên làm việc, gồm:

- `package.json` với `main: wrapper.mjs`
- `wrapper.mjs` đặt `app.setPath('userData', …)` rồi `import` bản build của app
- symlink `app -> <repo>/app`
- `userdata/state.json` seed sẵn folder, project, session

Playwright điều khiển bằng `_electron.launch({ recordVideo })`, rồi ffmpeg đổi
webm sang GIF (`palettegen` + `paletteuse`, nếu không thì chữ trên nền tối vỡ hạt).

## Ba chỗ mất thời gian nhất

1. **Playwright chỉ bắt tay được với bản build PRODUCTION.** Bản `app/` do
   `nextron dev` sinh ra có `NODE_ENV` bị inline thành `"development"`, nên main
   luôn trỏ vào Next dev server và `electron.launch` treo ở handshake không báo
   lỗi gì. Dựng bằng `npx nextron build --no-pack` là chạy.
2. **Dùng `setContentSize`, đừng dùng `setBounds`.** `setBounds` tính cả khung
   cửa sổ nên video thừa một dải đen dưới đáy.
3. **Claude thật cần folder đã được trust.** Prompt trust là TUI, gõ phím qua
   Playwright rất khó trúng. Cách chắc ăn là thêm sẵn đường dẫn vào `projects`
   trong `~/.claude.json` với `hasTrustDialogAccepted: true`.

## Dựng cảnh cho trạng thái waiting

Chấm vàng chỉ lên khi Claude thật sự xin phép. Lệnh chỉ đọc như `git status` bị
tự duyệt nên không ra. Việc chắc chắn xin phép là **ghi file**: prompt kiểu
"tạo giúp mình file src/lib/robots.js" thì Claude dừng lại hỏi, hook
`PermissionRequest` bắn về, chấm chuyển vàng và badge nhảy số.

Một lượt như vậy mất khoảng 20 giây, phần lớn là màn hình đứng yên. Cắt bỏ đoạn
giữa bằng `trim` + `concat` của ffmpeg, giữ lại lúc gửi prompt và lúc chấm đổi màu.

## Bốn cái còn lại chưa quay

| File | Vì sao chưa xong |
|---|---|
| `demo-06-remote.gif` | Bật host mode xong thì nút QR và switch LAN vẫn `disabled` một lúc, script bấm quá sớm nên timeout. Cần chờ theo điều kiện thay vì chờ theo thời gian. |
| `demo-07-help.gif` | Cần một lượt Claude thật trong hộp chat trợ giúp. Làm được, chỉ là chưa chạy. |
| `demo-08-inbox.gif` | Cần hai session cùng ở trạng thái chờ, tức hai lượt Claude. Làm được, tốn thời gian gấp đôi demo-02. |
| `demo-10-conversation.gif` | Transcript phải còn sống, nên phải chạy một lượt Claude rồi chuyển sang chế độ hội thoại **trong cùng một lần mở app**. |

Bốn cái này quay tay trong app thật nhanh hơn nhiều, vì ở đó Claude đã đăng nhập
và thư mục đã trust sẵn.
