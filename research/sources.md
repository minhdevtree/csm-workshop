# Nguồn dẫn trong bài

Mọi con số nói trên sân khấu đều phải có một dòng ở đây. Nếu một slide dẫn số mà
không tìm được nguồn trong file này thì bỏ slide đó đi.

## Dữ liệu về năng suất

**DORA 2025, State of AI-assisted Software Development.** Khảo sát gần 5.000 người làm
công nghệ. Hai kết luận dùng trong bài:

- Áp dụng AI tương quan **thuận** với throughput giao hàng phần mềm.
- Áp dụng AI cũng tương quan với **bất ổn định cao hơn**: nhiều thay đổi hỏng hơn,
  nhiều việc làm lại hơn.
- Luận điểm trung tâm: *"AI is not a solution in a box; it's an amplifier."* AI khuếch
  đại cái sẵn có. Nền tốt thì tăng tốc, nền lộn xộn thì lộn xộn nhanh hơn.
- Nút thắt bị đẩy xuống hạ nguồn: kiểm thử, review, QA.

Nguồn:
- https://cloud.google.com/blog/products/ai-machine-learning/announcing-the-2025-dora-report
- https://dora.dev/insights/balancing-ai-tensions/

**METR, tháng 7/2025.** Thử nghiệm ngẫu nhiên có đối chứng trên 16 lập trình viên mã
nguồn mở giàu kinh nghiệm, 246 tác vụ, trên chính repo của họ.

- Trước khi làm, họ dự đoán AI giúp nhanh hơn khoảng 24%.
- Thực tế: **chậm hơn 19%** khi được dùng AI.
- Sau khi làm, họ vẫn tin AI đã giúp họ **nhanh hơn 20%**.

Lưu ý bắt buộc phải nói trên sân khấu: METR hiện đã gắn nhãn kết quả này là **lịch
sử**, không nhất thiết phản ánh công cụ hay quy trình hiện tại. Công cụ trong nghiên
cứu là Cursor Pro với Claude 3.5/3.7 Sonnet, tức là trước thời agent chạy dài.

Bài học lấy ra không phải "AI vô dụng", mà là: **cảm giác nhanh và nhanh thật là hai
đại lượng khác nhau, và con người rất tệ trong việc phân biệt chúng.**

Nguồn:
- https://metr.org/blog/2025-07-10-early-2025-ai-experienced-os-dev-study/
- https://arxiv.org/abs/2507.09089

**Gloria Mark, UC Irvine.** Nghiên cứu quan sát tại chỗ về công việc bị ngắt quãng.

- Trung bình **23 phút 15 giây** để quay lại tác vụ ban đầu sau một lần bị ngắt.
- Người bị ngắt thường làm nhanh hơn để bù, nhưng kèm căng thẳng và lỗi nhiều hơn.
- Trung bình có 2 tác vụ xen vào trước khi quay lại việc cũ.

Nguồn:
- https://ics.uci.edu/~gmark/chi08-mark.pdf
- https://www.fastcompany.com/944128/worker-interrupted-cost-task-switching

## Bối cảnh công cụ

**Bản thân Claude Code đã có sẵn** (kiểm tra tại tài liệu chính thức, 08/2026):

- `--worktree` / `-w`: khởi động trong một git worktree cô lập tại
  `<repo>/.claude/worktrees/<name>`.
- `--tmux`: tạo phiên tmux cho worktree đó.
- `--resume` / `-r`, `--continue` / `-c`, `--fork-session`.
- `--settings`: trỏ tới file settings JSON riêng cho phiên, đè lên settings gốc.
- Hooks: hơn 30 sự kiện trong vòng đời một lượt, cấu hình bằng JSON, handler có thể
  là lệnh, HTTP endpoint, MCP tool, prompt hoặc agent.
- `--permission-mode`: `default`, `acceptEdits`, `plan`, `auto`, `dontAsk`,
  `bypassPermissions`, `manual`.

Nguồn:
- https://code.claude.com/docs/en/cli-reference
- https://code.claude.com/docs/en/hooks

**Các hình dạng công cụ khác trên thị trường.** Dùng để vẽ bản đồ, không dùng để chấm
điểm. Ghi nhận tháng 8/2026:

| Công cụ | Hình dạng |
|---|---|
| tmux, zellij | terminal multiplexer tự dựng |
| Claude Squad | quản lý phiên trong terminal, mã nguồn mở |
| Conductor | app macOS, mỗi agent một worktree, mạnh về diff và luồng PR |
| Crystal (Stravu) | app Electron, MIT. **Đã ngừng phát triển tháng 2/2026**, trỏ sang bản kế nhiệm đóng nguồn có phí |
| Vibe Kanban (Bloop) | bảng kanban cho agent, kéo thẻ thì agent nhận việc trên nhánh riêng |
| ccmanager, dmux, agentree | các bộ quản lý phiên khác |

Nguồn tổng hợp:
- https://www.augmentcode.com/tools/open-source-agent-orchestrators
- https://nimbalyst.com/blog/best-tools-for-running-parallel-ai-coding-agents/
- https://parallelcode.app/blog/multi-agent-coding-tools-2026/

Cảnh báo: phần lớn bài viết dạng "best tools 2026" là nội dung tiếp thị của chính một
công cụ trong danh sách. Đọc để lấy tên, đừng lấy thứ hạng.

## Số liệu của chính dự án

Xem `../context/04-numbers.md`. Đo lại bằng lệnh ghi trong đó trước ngày thuyết trình.
