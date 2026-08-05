# CSM là gì

**Claude Session Manager (CSM)** là một ứng dụng desktop giữ nhiều phiên Claude Code
sống cùng lúc trong một cửa sổ, và cho bạn biết phiên nào đang cần bạn.

Repo mã nguồn: `minhdevtree/csm-next` (private). Repo này chỉ chứa tài liệu workshop,
không chứa mã nguồn.

## Vấn đề nó sinh ra để giải

Khi một agent code chạy mất 3 tới 10 phút cho mỗi lượt, bạn có ba lựa chọn:

1. Ngồi nhìn nó chạy. An toàn, nhưng đó là thời gian chết.
2. Chuyển sang việc khác. Nhanh hơn, nhưng bạn không biết lúc nào agent gọi mình.
3. Chạy nhiều agent cùng lúc. Nhanh nhất, nhưng sinh ra ba vấn đề mới:
   - Không biết cái nào đang chờ mình.
   - Đóng terminal là mất phiên.
   - Nhiều nhánh cùng lúc thì đụng nhau trong cùng một thư mục làm việc.

CSM tồn tại vì lựa chọn thứ ba, và ba vấn đề của nó.

## Nguyên tắc thiết kế (trích PRODUCT.md của dự án)

1. **Điều hướng sự chú ý là ưu tiên số một.** Phiên nào đang chờ phải tìm thấy được
   trong một cái liếc mắt, từ mọi bề mặt: cây dự án, thanh rail, header, dock.
2. **Không bao giờ cắt ngang terminal.** Không cướp focus, không modal mặc định,
   phím tắt không được đụng phím của shell.
3. **Dùng thứ người ta đã quen.** Từ vựng shadcn/Radix, tương tác cây kiểu VS Code.
   Không phát minh control mới.
4. **Dày nhưng vẫn đọc được.** Dòng trong sidebar nén, cắt chữ chứ không xuống dòng.
5. **Ngang bằng trên Windows.** Mọi tương tác chạy y hệt trên Windows (ConPTY,
   quy ước phím Ctrl, toast).

## Bối cảnh người dùng

Một lập trình viên chạy nhiều phiên Claude Code song song trên nhiều dự án, macOS khi
phát triển và Windows ở bản đóng gói. Họ sống trong cửa sổ này hàng giờ: terminal là
nội dung, phần vỏ chỉ tồn tại để điều hướng sự chú ý giữa các phiên.
