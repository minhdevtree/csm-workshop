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

Không cần quay đủ. **Ba cái "Bắt buộc" là đủ để buổi nói chạy tốt**, phần còn lại
thiếu thì slide vẫn trình chiếu được, khung sẽ hiện tên file cần bỏ vào.

| Ưu tiên | File | Slide | Quay cái gì |
|---|---|---|---|
| Bắt buộc | `demo-01-session-alive.gif` | 11 | Đóng tab một session đang chạy. Nó vẫn nằm trong sidebar, chấm vẫn nhảy. Mở lại thấy nguyên. |
| Bắt buộc | `demo-02-attention.gif` | 13 | 3 session chạy, một con chuyển sang chờ, chấm đổi vàng, badge nhảy số, bấm badge nhảy tới đúng con đó. |
| Bắt buộc | `demo-06-share.gif` | 23 | Tạo link chỉ đọc giới hạn một session, quét QR bằng điện thoại, bên kia thấy đúng session đó và không gõ được. |
| Nên có | `demo-03-split-layout.gif` | 15 | Chia màn thành 3 ô, kéo một tab sang ô khác, lưu thành template, đóng hết rồi mở template ra lại. |
| Nên có | `demo-04-worktree.gif` | 19 | Chuột phải lên project, tạo worktree, nó hiện lồng bên dưới, mở một session trong đó. |
| Nên có | `demo-05-diff.gif` | 20 | Bấm ⇧⌘D, diff mở thành tab, chia đôi màn đặt cạnh file gốc. |
| Nên có | `demo-07-help.gif` | 24 | Bấm dấu hỏi ở header, hỏi "làm sao lưu cách chia màn hình", nhận câu trả lời kèm đúng phím tắt. |
| Có thì tốt | `demo-08-inbox.gif` | 14 | Bấm ⇧⌘A, danh sách hiện mọi session đang chờ từ nhiều dự án, chọn một cái là nhảy tới đó. |
| Có thì tốt | `demo-09-prompt.gif` | 16 | Gõ prompt vào ô nhập, đính một ảnh, gõ / để hiện slash command. |
| Có thì tốt | `demo-10-conversation.gif` | 18 | Đổi từ terminal sang chế độ hội thoại, cuộn lại và tìm một câu Claude nói lúc nãy. |
| Có thì tốt | `demo-11-history.gif` | 21 | Bấm ⇧⌘H, gõ chữ vào ô tìm để lọc commit, chọn một commit rồi chọn file để xem thay đổi. |

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
