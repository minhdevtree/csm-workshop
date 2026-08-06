# GIF demo cần quay

Bỏ file vào `assets/` đúng tên là **slide tự nhận**, không cần chạy lệnh gì. Chưa có
file thì khung nét đứt ở nguyên và ghi rõ tên file cần bỏ vào, nên deck vẫn trình
chiếu được bình thường.

## Quy cách chung

- **Định dạng**: GIF hoặc MP4 im lặng. GIF an toàn hơn vì chạy được cả khi mở
  bằng `file://`.
- **Tỉ lệ**: khoảng 16:10, khung hiển thị trên slide rộng chừng 520 x 400 điểm ảnh
  logic. Quay ở 2x rồi thu nhỏ cho nét.
- **Độ dài**: 6 tới 12 giây. Phải xem hết được trong lúc bạn nói một câu.
- **Lặp**: có. Người xem sẽ thấy nó chạy vòng thứ hai trong lúc bạn nói.
- **Không có chuột bay lung tung.** Di chuột thẳng tới chỗ cần bấm rồi dừng.
- **Phóng to giao diện trước khi quay.** Chữ trên slide chiếu phải đọc được từ
  cuối phòng. Trong app: Settings, phần Fonts, tăng cỡ chữ giao diện.
- **Che thứ không nên chiếu**: tên khách hàng, đường dẫn nội bộ, token, tên repo
  của công ty nếu buổi này có người ngoài team.

---

## Mười một đoạn, xếp theo ưu tiên

**Cả 11 đã quay xong** bằng harness tự động, xem `../research/recording.md`.
Muốn quay lại cái nào thì theo mô tả trong bảng; bỏ file mới vào `assets/` đè lên
là slide tự nhận.

| Ưu tiên | File | Slide | Quay cái gì |
|---|---|---|---|
| ✅ đã có Bắt buộc | `demo-01-session-alive.gif` | 11 | Đóng tab một session đang chạy. Nó vẫn nằm trong sidebar, chấm vẫn nhảy. Mở lại thấy nguyên. |
| ✅ đã có Bắt buộc | `demo-02-attention.gif` | 13 | 3 session chạy, một con chuyển sang chờ, chấm đổi vàng, badge nhảy số, bấm badge nhảy tới đúng con đó. |
| ✅ đã có Bắt buộc | `demo-06-remote.gif` | 24 | Ba đoạn ghép lại: bật host mode ở máy chủ; một app CSM khác thêm host vào Remote hosts (tên, URL, token, ô tunnel command); cửa sổ remote mở ra với đúng cây session của máy chủ. |
| ✅ đã có Nên có | `demo-03-split-layout.gif` | 16 | Chia màn thành 3 ô, kéo một tab sang ô khác, lưu thành template, đóng hết rồi mở template ra lại. |
| ✅ đã có Nên có | `demo-04-worktree.gif` | 20 | Chuột phải lên project, tạo worktree, nó hiện lồng bên dưới, mở một session trong đó. |
| ✅ đã có Nên có | `demo-05-diff.gif` | 21 | Bấm ⇧⌘D, diff mở thành tab, chia đôi màn đặt cạnh file gốc. |
| ✅ đã có Nên có | `demo-07-help.gif` | 25 | Bấm dấu hỏi ở header, hỏi "làm sao lưu cách chia màn hình", nhận câu trả lời kèm đúng phím tắt. |
| ✅ đã có Có thì tốt | `demo-08-inbox.gif` | 15 | Bấm ⇧⌘A, danh sách hiện mọi session đang chờ từ nhiều dự án, chọn một cái là nhảy tới đó. |
| ✅ đã có Có thì tốt | `demo-09-prompt.gif` | 17 | **Bật chế độ hội thoại trước**, rồi gõ prompt vào ô nhập và gửi. Ở chế độ terminal thì chữ hiện trong dòng nhập của Claude, nhìn không ra là có ô riêng. |
| ✅ đã có Có thì tốt | `demo-10-conversation.gif` | 19 | Đổi từ terminal sang chế độ hội thoại, cuộn lại và tìm một câu Claude nói lúc nãy. |
| ✅ đã có Có thì tốt | `demo-11-history.gif` | 22 | Bấm ⇧⌘H, gõ chữ vào ô tìm để lọc commit, chọn một commit rồi chọn file để xem thay đổi. |

### Mẹo dựng cảnh cho demo-02

Cho một session chạy lệnh cần duyệt quyền, ví dụ nhờ nó chạy một lệnh shell. Nó sẽ
dừng lại hỏi, và đó là lúc chấm chuyển sang vàng.

### Mẹo cho demo-06

Quay được cả màn hình điện thoại lẫn màn hình máy bàn trong cùng một khung hình thì
tốt hơn nhiều so với cắt cảnh, vì người xem thấy ngay là **cùng một lúc**.

---

## Chèn vào slide

**Không cần làm gì cả.** Bỏ file vào `assets/` đúng tên là xong. Slide tự thử tải
ảnh khi mở: có file thì nó thay khung nét đứt bằng ảnh, chưa có thì khung ở nguyên
và vẫn ghi tên file cần bỏ vào.

Ảnh không hiện thì kiểm tra hai thứ:

1. Tên file có đúng từng ký tự không, kể cả phần `.gif`.
2. File có nằm thẳng trong `assets/` không, đừng để trong thư mục con.
