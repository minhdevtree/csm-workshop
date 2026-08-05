# Bảy đoạn demo cần quay

Slide 11, 13, 15, 18, 19, 22, 23 đang để khung nét đứt. Bỏ file vào `assets/` đúng tên dưới đây là
slide tự hiện ảnh, không cần sửa gì trong HTML.

Sau khi có đủ file, chạy lệnh ở cuối trang này để thay khung nét đứt bằng ảnh.

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

## Bảy đoạn cần quay

| File | Slide | Quay cái gì |
|---|---|---|
| `demo-01-session-alive.gif` | 11 | Đóng tab một session đang chạy. Nó vẫn nằm trong sidebar, chấm vẫn nhảy. Mở lại thấy nguyên. |
| `demo-02-attention.gif` | 13 | **Quan trọng nhất.** 3 session chạy, một con chuyển sang chờ, chấm đổi vàng, badge nhảy số, bấm badge nhảy tới đúng con đó. |
| `demo-03-split-layout.gif` | 15 | Chia màn thành 3 ô, kéo một tab sang ô khác, lưu thành template, đóng hết rồi mở template ra lại. |
| `demo-04-worktree.gif` | 18 | Chuột phải lên project, tạo worktree, nó hiện lồng bên dưới, mở một session trong đó. |
| `demo-05-diff.gif` | 19 | Bấm ⇧⌘D, diff mở thành tab, chia đôi màn đặt cạnh file gốc. |
| `demo-06-mobile.gif` | 22 | Điện thoại mở địa chỉ máy bàn, thấy một con đang chờ, gõ trả lời, máy bàn nhận được. |
| `demo-07-help.gif` | 23 | Bấm dấu hỏi ở header, hỏi "làm sao lưu cách chia màn hình", nhận câu trả lời kèm đúng phím tắt. |

Nếu chỉ kịp quay một cái thì quay `demo-02-attention.gif`.

### Mẹo dựng cảnh cho demo-02

Cho một session chạy lệnh cần duyệt quyền, ví dụ nhờ nó chạy một lệnh shell. Nó sẽ
dừng lại hỏi, và đó là lúc chấm chuyển sang vàng.

### Mẹo cho demo-06

Quay được cả màn hình điện thoại lẫn màn hình máy bàn trong cùng một khung hình thì
tốt hơn nhiều so với cắt cảnh, vì người xem thấy ngay là **cùng một lúc**.

---

## Chèn vào slide

Sau khi đủ bảy file, chạy trong thư mục gốc của repo này:

```bash
python3 - <<'PY'
import re, pathlib
p = pathlib.Path('slides/index.html')
s = p.read_text()
# Thay mỗi khung nét đứt bằng thẻ ảnh, giữ nguyên phần chú thích bên dưới.
s = re.sub(
    r'<div class="demo-frame"><span class="lbl">[^<]*</span><span class="file">([^<]+)</span></div>',
    lambda m: '<img src="../%s" alt="">' % m.group(1),
    s)
p.write_text(s)
print('đã chèn')
PY
```

Kiểm tra lại bằng cách mở `slides/index.html` và bấm tới slide 13. Nếu ảnh không
hiện, kiểm tra đường dẫn: slide nằm trong `slides/` nên đường dẫn tới `assets/`
phải bắt đầu bằng `../`.
