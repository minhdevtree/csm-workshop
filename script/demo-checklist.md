# Sáu đoạn demo cần quay

Slide 21 tới 26 đang để khung nét đứt. Bỏ file vào `assets/` đúng tên dưới đây là
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

## 1. `assets/demo-01-attention.gif`

**Slide 21. Đây là demo quan trọng nhất. Nếu chỉ kịp quay một cái thì quay cái này.**

Cảnh cần có, theo thứ tự:

1. Ba phiên đang chạy, thấy rõ ba chấm trạng thái trong sidebar.
2. Một phiên chuyển sang **chờ**: chấm đổi màu sang hổ phách.
3. Badge ở header nhảy số.
4. Bấm vào badge, giao diện nhảy thẳng tới đúng phiên đang chờ.

Mẹo dựng cảnh: cho một phiên chạy lệnh cần duyệt quyền, ví dụ nhờ nó chạy một lệnh
shell. Nó sẽ dừng lại hỏi, và đó là lúc trạng thái chuyển sang chờ.

---

## 2. `assets/demo-02-session-alive.gif`

**Slide 22.**

1. Một phiên đang chạy, có chữ đang trôi trong terminal.
2. Đóng tab của chính phiên đó.
3. Phiên **vẫn nằm trong sidebar**, chấm vẫn báo đang chạy.
4. Bấm mở lại, nội dung còn nguyên.

Điểm cần thấy rõ: giữa bước 2 và 3, chấm không hề đổi trạng thái.

---

## 3. `assets/demo-03-worktree.gif`

**Slide 23.**

1. Chuột phải lên một dự án trong cây.
2. Chọn tạo worktree, đặt tên nhánh.
3. Worktree hiện ra **lồng bên dưới** dự án cha.
4. Mở một phiên bên trong worktree đó.

Nếu bước 2 có dialog, để dialog hiện đủ lâu để người xem đọc được tên nhánh.

---

## 4. `assets/demo-04-diff-history.gif`

**Slide 24.**

1. Bấm phím tắt mở diff (`⇧⌘D`).
2. Diff mở ra như một tab editor.
3. Chia đôi màn hình, đặt diff cạnh chính file nó nói về.
4. Mở lịch sử (`⇧⌘H`), gõ một chữ vào ô tìm, danh sách commit lọc lại.

Đây là đoạn dài nhất trong sáu đoạn. Nếu quá 12 giây thì tách làm hai file và
chèn hai khung cạnh nhau trên slide.

---

## 5. `assets/demo-05-mobile.gif`

**Slide 25. Có thể quay màn hình điện thoại thay vì GIF.**

1. Điện thoại mở trình duyệt, vào địa chỉ máy bàn.
2. Thấy danh sách phiên, một phiên đang chờ.
3. Gõ câu trả lời từ điện thoại.
4. Cắt sang màn hình máy bàn, thấy nó nhận được.

Nếu quay được cả hai màn hình trong một khung hình thì tốt hơn nhiều so với cắt
cảnh, vì người xem thấy ngay là **cùng một lúc**.

---

## 6. `assets/demo-06-help.gif`

**Slide 26.**

1. Bấm dấu hỏi ở header.
2. Gõ một câu hỏi thật, ví dụ "làm sao lưu cách chia màn hình".
3. Câu trả lời hiện ra, **có kèm đúng phím tắt**.

Chọn câu hỏi mà câu trả lời có phím tắt cụ thể, để người xem thấy nó trả lời từ
tài liệu chứ không phải nói chung chung.

---

## Chèn vào slide

Sau khi đủ sáu file, chạy trong thư mục gốc của repo này:

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

Kiểm tra lại bằng cách mở `slides/index.html` và bấm tới slide 21. Nếu ảnh không
hiện, kiểm tra đường dẫn: slide nằm trong `slides/` nên đường dẫn tới `assets/`
phải bắt đầu bằng `../`.
