# Workshop: Chạy nhiều Claude Code cùng lúc mà không loạn

Slide, kịch bản và nguồn dẫn cho một buổi chia sẻ nội bộ 60 phút.

Luận điểm của buổi này không phải "công cụ nào tốt hơn", mà là **cách tự biết mình
cần gì** trước khi chọn bất cứ công cụ nào. Case study là một app tôi tự viết, kể
cả phần dở của nó.

**Xem thẳng trên web**: <https://minhdevtree.github.io/csm-workshop/slides/>

## Mở slide

```bash
open slides/index.html      # macOS
```

Không cần server, không cần cài gì. Mở thẳng bằng `file://` cũng chạy đủ: không có
font ngoài, script ngoài hay ảnh ngoài nào.

| Phím | Việc |
|---|---|
| `←` `→` `Space` | Chuyển slide |
| `S` | Bật tắt ghi chú diễn giả |
| `O` | Xem toàn bộ slide dạng lưới |
| `T` | Đổi giữa nền tối và nền sáng |
| `F` | Toàn màn hình |
| `#12` trên URL | Nhảy thẳng tới slide 12 |

**Xuất PDF**: mở slide rồi in ra PDF. Đã có sẵn quy tắc in, mỗi slide một trang
ngang 1280 x 720. Nhớ bật "In nền và hình ảnh" trong hộp thoại in.

**Chọn nền sáng hay tối**: phòng tối và máy chiếu tốt thì để mặc định là nền tối.
Phòng nhiều ánh sáng tự nhiên thì bấm `T`. Quyết định việc này **trước** buổi nói,
không phải lúc đang đứng trên bục.

## Trong repo có gì

```
slides/index.html          Deck 33 slide, tự chứa, có ghi chú diễn giả
script/script-vi.md        Kịch bản nói chi tiết, có mốc thời gian và chỉ dẫn sân khấu
script/demo-checklist.md   Sáu đoạn demo cần quay, và cách chèn vào slide
context/                   Bối cảnh về app được lấy làm case study
research/sources.md        Mọi con số dẫn trong bài, kèm link gốc
assets/                    Chỗ bỏ GIF demo vào
```

## Còn thiếu

Sáu khung demo ở slide 21 tới 26 đang để trống có chủ đích, chờ GIF quay màn hình.
Xem `script/demo-checklist.md` để biết cần quay gì và đặt tên file thế nào. Slide
vẫn trình chiếu được khi chưa có, khung sẽ hiện tên file cần bỏ vào.

## Ghi chú về tính trung thực

Mọi con số nói trên sân khấu đều có nguồn trong `research/sources.md`. Hai chỗ cần
đặc biệt cẩn thận khi trình bày:

1. **Nghiên cứu METR** (slide 8) đã được chính METR gắn nhãn là lịch sử. Kịch bản
   bắt buộc phải nói kèm điều đó. Trích một nửa con số là trích sai.
2. **Số liệu dự án** (slide 27) đo ngày 05/08/2026. Đo lại bằng lệnh trong
   `context/04-numbers.md` trước ngày nói.
