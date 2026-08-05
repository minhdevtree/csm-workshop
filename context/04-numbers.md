# Số liệu dự án

Tất cả đo từ chính repo `csm-next` ngày **05/08/2026**. Không có con số nào ở đây là
ước lượng hay làm tròn cho đẹp. Nếu dùng lại trong slide, đo lại trước khi nói.

| Chỉ số | Giá trị | Lệnh đã dùng |
|---|---|---|
| Commit đầu tiên | 17/06/2026 | `git log --reverse --format=%aI \| head -1` |
| Commit gần nhất | 04/08/2026 | `git log -1 --format=%aI` |
| Số ngày | 48 | tính từ hai mốc trên |
| Tổng commit | 727 | `git rev-list --count HEAD` |
| Dòng TypeScript/TSX | 72.212 | `find main renderer -name '*.ts' -o -name '*.tsx' \| xargs wc -l` |
| File nguồn | 376 | cùng lệnh trên, đếm file |
| Test tự động | 2.708 | `npx vitest run` |
| File test | 129 | `npx vitest run` |
| Phiên bản đã phát hành | 51 | số mục trong `CHANGELOG.md` |
| Phiên bản hiện tại | 1.30.0 | `package.json` |

## Cách đọc mấy con số này

**727 commit trong 48 ngày** là khoảng 15 commit mỗi ngày, kể cả cuối tuần. Đây không
phải chỉ số năng suất của một người gõ code, mà là chỉ số của một người **điều hướng
agent**: phần lớn commit do Claude Code viết, dưới sự dẫn dắt và kiểm tra.

**2.708 test** là phần đáng nói hơn số dòng. Chúng tồn tại vì một lý do cụ thể: khi
agent viết phần lớn code, cái bạn cần không phải là đọc từng dòng, mà là một cái lưới
bắt được lúc nó sai. Test là hợp đồng bạn viết, code là thứ agent điền vào.

**51 phiên bản trong 48 ngày** nghĩa là mỗi thay đổi hành vi đều được đóng gói và phát
hành. Vòng lặp ngắn là điều kiện để phát hiện sai sớm, không phải là thành tích.

## Cảnh báo khi dùng trong slide

Đừng trình bày mấy con số này như bằng chứng "AI làm bạn nhanh hơn 15 lần". Chúng là
bằng chứng cho một điều hẹp hơn nhiều: **với đúng một người, đúng một loại việc, có
quy trình kiểm tra tự động, thì khối lượng đầu ra đã khác hẳn.** Xem
`../research/sources.md` cho phần dữ liệu nói ngược lại.
