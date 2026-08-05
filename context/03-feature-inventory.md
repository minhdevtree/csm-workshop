# Những gì CSM làm được

Nhóm theo nhu cầu, không theo module. Mỗi mục là một câu hỏi người dùng thật sự hỏi.

## Giữ phiên sống

- Mỗi dự án có PTY riêng chạy `claude`, sống qua việc chuyển tab.
- Đóng tab không giết phiên. Kết thúc phiên là một hành động riêng.
- Khởi động lại app thì lấy lại hội thoại cũ qua `--resume`.
- Cờ Claude lưu theo từng dự án (`--model`, `--permission-mode`, ...).
- Bộ cờ hay dùng lưu lại thành profile.

## Biết phiên nào đang chờ

- Chấm trạng thái năm màu, lấy từ hook.
- Hộp thư chú ý: mọi phiên đang chờ, một danh sách, một phím tắt.
- Badge trong app, thông báo hệ điều hành, badge dock, chuông. Bật tắt riêng.
- Bấm badge ở header là nhảy tới phiên chờ kế tiếp.

## Nhìn nhiều phiên cùng lúc

- Chia màn hình nhiều chiều, kéo tab giữa các ô.
- Lưu cách sắp xếp thành template, mở lại bất cứ lúc nào.
- Ô có thể ghim sẵn phiên cố định, hoặc hỏi lại mỗi lần dùng.
- Cách sắp xếp sống qua khởi động lại.

## Trả lời Claude mà không cần gõ vào terminal

- Ô nhập prompt riêng, có đính ảnh, có slash command.
- Chạy một chuỗi prompt nối nhau.
- Hẹn giờ chạy prompt.
- Thư viện prompt dùng lại.
- Gửi một prompt tới nhiều phiên cùng lúc.
- Xem phiên dưới dạng hội thoại thay vì terminal thô.

## Nhiều nhánh cùng lúc

- Tạo git worktree ngay trong cây dự án.
- Worktree nằm lồng dưới dự án cha, có nhánh riêng, phiên riêng.
- Nhận diện worktree đã có sẵn trong repo.

## Đọc thay đổi và lịch sử

- Diff của cây làm việc mở ra như một tab editor, ngồi cạnh file nó nói về.
- Lịch sử commit mở như một tab: message, tác giả, thời gian, nhánh và tag.
- Chọn commit để xem file nó đổi, chọn file để xem đổi chỗ nào.
- Tìm commit theo nội dung message, đọc bất kỳ nhánh nào mà không cần checkout.

## Editor tích hợp

- Cây file, mở file, sửa, lưu.
- Nhảy tới file (`⌘P`), tìm trong toàn bộ file (`⇧⌘F`).
- Cả hai cây (dự án và file) tự cuộn theo tab đang mở.

## Rời khỏi máy

- Bật chế độ host: máy phục vụ giao diện qua HTTP cho thiết bị khác.
- Mở bằng điện thoại, điều khiển phiên đang chạy trên máy bàn.
- Token chỉ đọc, và token giới hạn trong đúng một phiên.

## Những thứ nhỏ

- Ba bảng màu, sáng và tối.
- Chọn font và cỡ chữ riêng cho terminal, editor, và giao diện.
- Đồng hồ usage và token.
- Trợ lý trong app trả lời "làm thế nào để..." bằng chính user guide.
- Một con pet pixel trong sidebar, và một phòng nghỉ.
