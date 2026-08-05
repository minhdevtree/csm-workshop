# Cách quay GIF demo bằng harness tự động

7 trong 11 GIF được quay tự động, không thao tác tay. Ghi lại đây để lần sau khỏi
dò lại từ đầu.

## Cách chạy

Harness nằm trong scratchpad của phiên làm việc, gồm:

- `package.json` với `main: wrapper.mjs`
- `wrapper.mjs` đặt `app.setPath('userData', …)` rồi `import` bản build của app
- symlink `app -> <repo>/app`
- `userdata/state.json` seed sẵn folder, project, session

Playwright điều khiển bằng `_electron.launch({ recordVideo })`, rồi ffmpeg đổi
webm sang GIF (`palettegen` + `paletteuse`, nếu không thì chữ trên nền tối vỡ hạt).

## Ba chỗ mất thời gian nhất

1. **Playwright chỉ bắt tay được với bản build PRODUCTION.** Bản `app/` do
   `nextron dev` sinh ra có `NODE_ENV` bị inline thành `"development"`, nên main
   luôn trỏ vào Next dev server và `electron.launch` treo ở handshake không báo
   lỗi gì. Dựng bằng `npx nextron build --no-pack` là chạy.
2. **Dùng `setContentSize`, đừng dùng `setBounds`.** `setBounds` tính cả khung
   cửa sổ nên video thừa một dải đen dưới đáy.
3. **Claude thật cần folder đã được trust.** Prompt trust là TUI, gõ phím qua
   Playwright rất khó trúng. Cách chắc ăn là thêm sẵn đường dẫn vào `projects`
   trong `~/.claude.json` với `hasTrustDialogAccepted: true`.

## Dựng cảnh cho trạng thái waiting

Chấm vàng chỉ lên khi Claude thật sự xin phép. Lệnh chỉ đọc như `git status` bị
tự duyệt nên không ra. Việc chắc chắn xin phép là **ghi file**: prompt kiểu
"tạo giúp mình file src/lib/robots.js" thì Claude dừng lại hỏi, hook
`PermissionRequest` bắn về, chấm chuyển vàng và badge nhảy số.

Một lượt như vậy mất khoảng 20 giây, phần lớn là màn hình đứng yên. Cắt bỏ đoạn
giữa bằng `trim` + `concat` của ffmpeg, giữ lại lúc gửi prompt và lúc chấm đổi màu.

## Ba cái suýt hỏng, và vì sao

**State của lần quay trước dính sang lần sau.** Chế độ hội thoại, layout chia đôi
và transcript chết đều được nhớ lại, nên demo quay ra sai màn hình. Phải reset
`state.json` về baseline trước mỗi lần quay, và ép về chế độ terminal bằng nút
"Show the terminal" vì cờ đó KHÔNG nằm trong `state.json`.

**Transcript không được ghi.** Harness chạy bên trong một phiên Claude Code, nên
môi trường có sẵn `CLAUDECODE` và `CLAUDE_CODE_CHILD_SESSION`. Session do app đẻ
ra thừa hưởng và tắt luôn việc ghi transcript, terminal in ra dòng "Transcript
saving is off". Lọc mọi biến `CLAUDE_CODE_*` và `CLAUDECODE` trước khi truyền
xuống là hết.

**Chờ theo đồng hồ thì trượt.** Nút QR trong phần Remote còn `disabled` một lúc
sau khi bật host mode. Phải chờ tới khi panel hiện URL rồi mới bấm, đừng
`waitForTimeout` một con số đoán mò.

## Cắt video

Một lượt Claude thật mất 20 tới 100 giây, phần lớn là màn hình đứng yên. Hai cách
đang dùng:

- Cắt lấy N giây cuối bằng `ffmpeg -ss <dur - N>`, hợp với demo mà phần đáng xem
  nằm ở cuối.
- Cắt hai đoạn rồi nối bằng `trim` + `concat`, hợp với demo-02: giữ lúc gửi prompt
  và lúc chấm đổi màu, bỏ đoạn giữa Claude đang nghĩ.

## Quay phía client của chế độ remote

Cần hai tiến trình: app làm host, và một trình duyệt làm client. Ba cái bẫy:

1. **Cổng đụng nhau.** App thật đang chạy đã chiếm 4870. Harness phải đổi sang
   cổng khác, nếu không nó không bind được và trình duyệt sẽ nói chuyện với app
   THẬT bằng token của harness rồi bị từ chối. Bản thân app báo rất rõ chuyện này
   trong panel Remote.
2. **Token phải đọc SAU khi host chạy.** Đọc từ `state.json` của lần chạy trước
   thì nhận "this link's token is invalid or was regenerated".
3. **Ghép nhiều clip.** Chuẩn hoá cùng độ phân giải và fps rồi mới `concat`.

## Quay phần nối app sang app

Cần hai instance với hai `userData` khác nhau. Instance client để `state.json`
rỗng project, như vậy nhìn là biết ngay nó đang xem máy khác chứ không phải máy
mình.

Bấm Connect thì app mở một **cửa sổ mới**. Playwright quay mỗi page một file, nên
sau khi chạy xong có hai `.webm`. Phân biệt bằng ĐỘ DÀI: cửa sổ chính chạy suốt
nên dài hơn, cửa sổ remote mở sau nên ngắn hơn. Đừng dựa vào thứ tự file, `ls -tr`
cho kết quả ngược.

Cắt đoạn giữa phải theo mốc thật: phần điền form nằm ở GIỮA clip của cửa sổ
chính, lấy "N giây cuối" là trượt mất.
