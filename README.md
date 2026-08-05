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
slides/index.html          Deck 36 slide, tự chứa, có ghi chú diễn giả
script/script-vi.md        Kịch bản nói chi tiết, có mốc thời gian và chỉ dẫn sân khấu
script/demo-checklist.md   Sáu đoạn demo cần quay, và cách chèn vào slide
context/                   Bối cảnh về app được lấy làm case study
research/sources.md        Mọi con số dẫn trong bài, kèm link gốc
assets/                    Chỗ bỏ GIF demo vào
```

## Còn thiếu

Mười một khung demo đang để trống có chủ đích, chờ GIF quay màn hình. Xem `script/demo-checklist.md` để biết cần quay gì và đặt tên file
thế nào. **Bỏ file vào `assets/` là slide tự nhận**, không phải chạy lệnh gì. Chưa
có file thì khung ở nguyên và ghi rõ tên file cần bỏ vào, nên deck vẫn trình chiếu
được bình thường.

## Ghi chú về tính trung thực

Mọi con số nói trên sân khấu đều có nguồn trong `research/sources.md`. Hai chỗ cần
đặc biệt cẩn thận khi trình bày:

1. **Không còn số liệu nghiên cứu nào trên slide.** METR và DORA đều đã bỏ ra khỏi
   deck vì chúng kéo buổi chia sẻ thành bài giảng về năng suất. Nguồn vẫn giữ trong
   `research/sources.md` để trả lời khi được hỏi.
2. **Ghi công.** Repo `csm-next` có nhiều hơn một người đóng góp. Slide đầu và kịch
   bản đều nói rõ chuyện đó. Nhớ thay handle GitHub bằng tên thật của đồng nghiệp
   trước khi trình chiếu.
3. **Subagent.** Slide 8 nói rõ Claude Code tự nó đã chạy song song được, và cây bốn
   tầng không phải để thay subagent. Đừng trình bày nó như một thứ Claude không làm
   được, vì không đúng.
4. **Số liệu dự án** trong `context/04-numbers.md` đo ngày 05/08/2026. Đo lại bằng
   lệnh trong đó nếu định nhắc tới.
