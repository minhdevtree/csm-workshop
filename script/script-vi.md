# Kịch bản nói

50 phút nói + 10 phút hỏi đáp. 34 slide.

Cách dùng: cột thời gian là mốc tính từ lúc bắt đầu. Tới slide 11 mà đồng hồ đã quá
17 phút thì lướt nhanh phần tính năng, bỏ slide 13, 16, 19.

Chữ **in đậm** là chỗ nhấn giọng. Chữ trong ngoặc vuông là chỉ dẫn cho mình, không
đọc ra.

Giọng: kể chuyện cho đồng nghiệp nghe, không phải thuyết trình. Nói "mình" chứ đừng
"tôi". Từ kỹ thuật cứ để tiếng Anh, đừng dịch: session, worktree, diff, tab, badge.

---

## Chuẩn bị trước khi vào phòng

- [ ] Mở `slides/index.html`, bấm `F` cho toàn màn hình.
- [ ] Bấm `T` xem thử nền sáng. Phòng sáng thì dùng nền sáng. **Chốt trước, đừng đổi
      lúc đang đứng trên bục.**
- [ ] Bấm `S` xem ghi chú có nằm ở màn hình của mình không. Chỉ có một màn hình thì
      đừng bấm, cầm bản in file này.
- [ ] Kiểm tra 7 GIF đã nằm trong `assets/`, slide 10, 12, 14, 17, 18, 21, 22 hiện
      ảnh chứ không phải khung nét đứt.
- [ ] Mở sẵn một terminal ở tab khác, đã `cd` vào một repo thật, để chạy
      `claude --help` ở slide 30.
- [ ] Tắt thông báo trên máy. Buổi này nói về việc bị ngắt quãng, đừng để bị ngắt.

---

## Mở đầu (0:00 → 0:04)

**Slide 1.** [Đừng đọc slide. Hỏi trước.]

> Trước khi vào, mình hỏi hai câu, mọi người giơ tay giúp.
>
> Ai đang chạy **từ 2 con Claude Code trở lên** cùng lúc?
>
> [Đếm to.]
>
> Ai từng **đóng nhầm terminal rồi mất luôn cả cuộc chat**?
>
> [Đếm. Thường có tiếng cười.]
>
> Được rồi. Hôm nay mình kể về một cái app tụi mình làm để xử mấy chuyện đó.
>
> [**Ghi công cho đúng ngay từ đầu, đừng để cuối buổi.**]
>
> Nói trước cho rõ: app này không phải một mình mình làm. Có **[tên đồng nghiệp]**
> đóng góp một phần, và phần lớn code là Claude Code viết dưới sự dẫn dắt của tụi
> mình. Nói xong câu này thì cả buổi sau đó mình xưng "mình" cho gọn, không ai hiểu
> nhầm.

[Nếu đa số chỉ chạy 1 con: nói thêm "phần cấu trúc ở giữa vẫn đáng nghe kể cả khi
bạn không định dùng app", rồi lát nữa lướt nhanh phần tính năng nâng cao.]

**Slide 2.**

> Chuyện là thế này. Mình hay chạy 3 tới 6 con một lúc, trên mấy repo khác nhau.
> Nhanh hơn thật, nhưng đẻ ra ba cái phiền.
>
> Một, **không biết con nào đang chờ mình**. Nó hỏi "cho chạy lệnh này không" từ 5
> phút trước, mà mình đang nhìn tab khác.
>
> Hai, **đóng tab là mất**. Lỡ tay một cái, cả buổi sáng context đi theo.
>
> Ba, **hai con giẫm chân nhau**. Cùng một thư mục, con này sửa file con kia đang đọc.
>
> [Nhấn câu cuối.]
>
> App sinh ra để xử đúng ba cái đó. Lát nữa mình sẽ kể một đống tính năng khác,
> nhưng **chỉ ba cái này là lý do nó tồn tại**. Phần còn lại là tiện thì thêm.

**Slide 3.** [Lướt nhanh]

> Đi theo thứ tự này. Phần 2 là phần mình nghĩ đáng nghe nhất, kể cả với người không
> định cài gì, vì cái cấu trúc ở đó áp dụng được cho mọi cách quản lý session.

---

## Phần 1: được gì mất gì (0:04 → 0:07)

**Slide 4.** [Một slide, 60 giây. Đừng giảng.]

> Chạy nhiều con thì được gì, mất gì.
>
> **Được**: mỗi lượt Claude chạy 3 tới 10 phút, chạy nhiều con thì không phải ngồi
> chờ khoảng đó nữa.
>
> **Mất** hai thứ. Một là **phải review nhiều hơn**: chờ ngắn lại thì phần đọc và
> kiểm tra dài ra. Hai là **dễ bị ngắt liên tục**: không biết con nào đang gọi mình
> thì cứ vài phút lại tự đi kiểm tra.
>
> [Kể chuyện thật cho gần.]
>
> Mình từng có buổi chiều mở 3 terminal, cứ vài phút alt-tab qua từng cái xem xong
> chưa. Cuối buổi cả 3 con đều xong việc, còn mình thì chả làm được gì ra hồn.
>
> [Câu chốt, dẫn thẳng sang phần cấu trúc.]
>
> **Nên thứ quyết định không phải là chạy được mấy con, mà là bạn có biết con nào
> đang cần mình hay không.**

[Nếu có người hỏi số liệu: có nghiên cứu của Gloria Mark, sau một lần bị ngắt thì
trung bình mất 23 phút mới quay lại đúng mạch cũ. **Chỉ nói khi được hỏi.** Bản
trước để nó lên slide và bị phản hồi là khó hiểu, vì nó kéo buổi thành bài giảng
về năng suất.]

---

## Phần 2: cấu trúc (0:07 → 0:18)

**Slide 5.** [Phân đoạn]

> Giờ mình chỉ cho mọi người app được xếp thế nào. Hiểu cái này rồi thì phần tính
> năng ở sau chỉ là chi tiết.

**Slide 6.** [30 giây, chỉ để định vị]

> Cửa sổ chia ba phần. **Sidebar** bên trái, cái này đáng nói nhất, slide sau nói
> riêng. **Thanh tab** giống trình duyệt, mỗi tab là một session hoặc một file hoặc
> một cái diff. **Phần nội dung** chia được nhiều ô, kéo tab qua lại giữa các ô.
>
> Bấm `⌘B` là giấu sidebar cho terminal rộng ra.

**Slide 7.** [**Slide quan trọng nhất phần này. Đứng lại lâu.** Chỉ vào cây bên trái.]

> Cây trong sidebar có bốn tầng. Mình đi từ trên xuống.
>
> **Folder.** Đây là thư mục ảo, chỉ để gom dự án cho gọn. **Không liên quan gì tới
> thư mục trên ổ cứng.** Chỗ này hay nhầm. Kéo thả tuỳ ý, muốn xếp sao thì xếp.
>
> **Project.** Cái này mới là thư mục thật trên máy. Nó nhớ riêng bộ cờ chạy `claude`
> của nó, ví dụ repo này luôn chạy với `--permission-mode auto`.
>
> **Worktree.** Nằm lồng ngay dưới project cha. Cùng repo, khác nhánh, khác thư mục
> làm việc.
>
> **Session.** Là một tiến trình `claude` đang chạy. Nhiều session trong cùng một
> project là chuyện bình thường.
>
> [Chỉ vào mấy cái chấm.]
>
> Mấy cái chấm này đang chạy thật trên slide luôn. Con vàng là đang chờ mình, con
> xanh là đang làm. Trong app nó cũng nhảy y hệt vậy.

**Slide 8.** [**Chỗ dễ bị bắt bẻ nhất cả buổi. Nói cẩn thận.**]

> Vì sao lại cần tới bốn tầng.
>
> [**Nói phần này TRƯỚC, đừng để ai phải giơ tay hỏi.**]
>
> Nói rõ một chuyện trước đã: **Claude Code tự nó đã chạy song song được rồi.** Nó
> đẻ subagent trong cùng một session, và giờ còn có cả agent team. Nên đây **không
> phải** chuyện làm được hay không làm được. Ai nghĩ mình đang nói "Claude không làm
> được nên phải có app" thì hiểu sai.
>
> Cái khác nhau là **ranh giới**.
>
> Subagent nằm trong **cùng một cuộc hội thoại**: dùng chung context, chung luồng
> duyệt quyền, và xong việc là tan.
>
> Còn session riêng thì có context riêng, lịch sử riêng, sống qua nhiều ngày. Duyệt
> quyền riêng nên mình biết đúng **con nào** đang hỏi. Và bỏ một con đi không ảnh
> hưởng con kia.
>
> [Ví dụ cụ thể, đây là chỗ làm người nghe hiểu.]
>
> Ví dụ mình đang sửa bug ở nhánh mr-2103. Việc "đọc log production để tìm nguyên
> nhân" là **một mạch riêng**, hôm sau vẫn còn dùng tới. Nếu đưa vào subagent thì
> xong lượt là mất, mà nó còn ăn chung context với việc sửa code.
>
> Nói gọn: **subagent hợp khi một việc chia được thành mấy việc con rồi gộp kết quả
> lại. Session riêng hợp khi đó là mấy việc không liên quan tới nhau, mỗi việc một
> mạch, kéo dài nhiều ngày.**
>
> Bốn tầng là để **quản lý mấy session riêng đó**, không phải để thay subagent. Hai
> thứ dùng cùng lúc được, và mình dùng cả hai.
>
> Còn folder thì đơn giản: hai chục repo vẫn xếp gọn, việc công ty một hộp, việc cá
> nhân một hộp.

**Slide 9.**

> Cái chấm bên trái mỗi session có 5 trạng thái. Xám là đang chạy nhưng im. Xanh dương
> là đang làm việc. **Vàng là đang chờ mình trả lời**, đây là cái quan trọng nhất.
> Xanh lá là vừa xong. Vòng tròn rỗng là đã tắt.
>
> Nó biết bằng cách nào? Claude Code có cái gọi là **hook**: nó bắn ra ngoài ở từng
> mốc trong một lượt. App mở một cổng ở địa chỉ loopback, dựng một file settings riêng
> cho từng session, rồi nghe.
>
> [Nhấn chỗ này, đây là phần mang về được.]
>
> Chỗ quan trọng: **"đang chờ" là một sự kiện, không phải đoán mò.**
>
> Nhìn chữ chạy trong terminal thì chỉ biết có chữ hay im. Mà im thì có thể là đang
> nghĩ, cũng có thể là đang chờ. Hook nói thẳng cái nào ra cái nấy.
>
> Nên ai định tự dựng công cụ: **bắt đầu từ hook, đừng parse output terminal.** Parse
> output là ngõ cụt.

**Slide 10.** [Có GIF]

> Còn một chuyện về cấu trúc: **session không sống trong tab.**
>
> Tiến trình `claude` chạy ở tiến trình chính của app. Cái tab chỉ là chỗ để nhìn vào
> nó thôi.
>
> [Để GIF chạy một vòng.]
>
> Nên đóng tab thì session vẫn chạy, vẫn nằm trong sidebar, chấm vẫn nhảy. Mở lại là
> thấy nguyên.
>
> Muốn kết thúc hẳn thì có hành động riêng trong menu chuột phải, không ai đóng nhầm
> được.
>
> Bài học mang về: **đừng gắn vòng đời tiến trình vào vòng đời cái khung nhìn.** Rất
> nhiều script tmux tự viết dính đúng lỗi này.

---

## Phần 3: tính năng (0:18 → 0:41)

Nhịp chung: mỗi slide 60 tới 90 giây. Nói cái đau trước, rồi cách giải, rồi để GIF
chạy. Đừng đọc hết gạch đầu dòng, chỉ nhấn 2 ý mỗi slide.

**Slide 11.** [Phân đoạn]

> Hiểu cấu trúc rồi thì phần này đi nhanh. Mình gom theo nhóm nhu cầu chứ không theo
> menu.

**Slide 12. Biết con nào đang chờ.** [Có GIF. **Nếu chỉ kịp chiếu một GIF thì chiếu cái này.**]

> Nhóm một, và cũng là lý do app tồn tại. Có bốn đường báo.
>
> Chấm trong cây đổi màu tại chỗ. Badge ở header đếm số con đang chờ, **bấm vào là
> nhảy tới con tiếp theo**. Thông báo hệ điều hành, bấm vào là mở đúng session đó.
> Và tiếng chuông, cộng badge trên dock.
>
> [Để GIF chạy.]
>
> Bật tắt riêng từng cái được. Có người ghét chuông, có người ghét thông báo. Cái đó
> là chuyện phải có chứ không phải tính năng để khoe.

**Slide 13. Hộp thư chú ý.** [Bỏ được nếu trễ giờ]

> `⇧⌘A` mở một danh sách gom mọi session đang chờ, từ tất cả dự án.
>
> Khác badge ở chỗ badge chỉ nói **có bao nhiêu**, còn hộp thư nói **là những con
> nào**, kèm nó đang hỏi gì.
>
> Nói thật là chạy dưới 3 con thì cái này hơi thừa. Từ khoảng 4 con trở lên mới có
> nghĩa.

**Slide 14. Chia màn hình.** [Có GIF]

> Chia dọc chia ngang tuỳ ý, lồng nhau được, kéo tab từ ô này sang ô kia.
>
> Cái hay hơn: **lưu cách sắp xếp thành template**, `⇧⌘L`. Mở lại lúc nào cũng được.
>
> Mỗi ô chọn được hai kiểu: luôn mở đúng session đó, hoặc hỏi lại mỗi lần dùng. Ô ghim
> cố định hợp với mấy cái mình luôn mở, ô hỏi lại hợp với việc lặt vặt. Một template
> trộn cả hai kiểu được.
>
> [Nói câu này để không ai sợ thử.]
>
> Áp template **không bao giờ đóng hay xoá session nào**. Nó chỉ xếp lại thôi.

**Slide 15. Ô nhập prompt.**

> Gõ thẳng vào terminal thì hay mất chữ lúc Claude đang in ra, và không dán ảnh được.
> Nên có ô nhập riêng. Dán ảnh được, chạy cả trên điện thoại, gõ `/` là hiện slash
> command.
>
> [Cột phải, chỗ hay gây "ồ" nhất.]
>
> Và mấy thứ chỉ có ở ô này. **Xếp hàng nhiều prompt**: viết sẵn 3 việc, xong cái này
> nó tự chạy cái kia. **Hẹn giờ**: đặt sáng mai 8h tự chạy. Thư viện prompt hay dùng.
> Và gửi một lượt cho nhiều session, kiểu "cả 4 con cùng chạy test đi".
>
> Ví dụ thật: tối trước khi về xếp 3 việc, sáng ra đọc kết quả.

**Slide 16. Xem dạng hội thoại.** [Bỏ được nếu trễ giờ]

> Terminal thô thì quen mắt với dân dev, nhưng cuộn ngược lại tìm một câu Claude nói
> lúc nãy thì khổ. Bật chế độ hội thoại là nó hiện ra như một cuộc chat, tìm kiếm được.
>
> Chat cũ vẫn đọc lại được kể cả khi session đã tắt, vì nó nằm trong file trên máy.

**Slide 17. Worktree.** [Có GIF]

> Nhóm git. Worktree là nhiều thư mục làm việc trên cùng một repo, mỗi thư mục một
> nhánh, **dùng chung lịch sử git**. Không phải clone lại, nên rẻ hơn nhiều.
>
> Chuột phải lên project, tạo worktree, đặt tên nhánh. Nó hiện lồng ngay dưới project
> cha.
>
> [Nói cho công bằng.]
>
> Cái này `claude --worktree` cũng làm được mà không cần app nào. Thứ app thêm vào là
> nó **nằm trong cây, nhìn thấy được**, và có session riêng.

**Slide 18. Diff.** [Có GIF]

> `⇧⌘D`. Diff mở ra như một tab, ngồi cạnh chính file nó nói về, chia đôi màn được,
> và ở nguyên đó trong lúc mình làm việc tiếp.
>
> [Nối về slide 5.]
>
> Nhớ cái DORA lúc nãy không: **review là chỗ nghẽn mới**. Cái này sinh ra đúng vì
> chỗ đó.
>
> Nói thật là mình làm nó gần như sau cùng, sau khi alt-tab ra ngoài đủ nhiều lần.
> Không phải làm vì "app nào cũng có diff".

**Slide 19. Lịch sử commit.** [Bỏ được nếu trễ giờ]

> `⇧⌘H`. Danh sách commit, chọn một cái để xem nó đổi file nào, chọn file để xem đổi
> chỗ nào.
>
> Hai cái đáng nói: **tìm commit theo message**, tìm cả lịch sử chứ không phải chỉ
> 100 dòng đang hiện. Và **đọc nhánh khác mà không cần checkout**, kể cả nhánh remote.
> Kiểu "trên origin/main có gì mà máy mình chưa có".
>
> Không có đồ thị nhánh, và đó là cố ý. Vẽ đồ thị là một đống việc để trả lời câu hỏi
> mà mình gần như không bao giờ hỏi.

**Slide 20. Editor.**

> Có editor bên trong, nhưng **không phải để thay VS Code**. Mục đích hẹp thôi: sửa
> nhanh một dòng, đọc file Claude vừa nhắc tới, sửa `CLAUDE.md`.
>
> `⌘P` nhảy tới file, `⇧⌘F` tìm trong toàn bộ dự án. Bôi đen một từ rồi bấm `⇧⌘F` là
> nó tìm luôn từ đó, khỏi copy paste.
>
> Cây file cũng tự mở tới file đang xem, y như cây session tự cuộn tới session đang
> mở. Hai cây hành xử giống nhau, đó là chủ ý.

**Slide 21. Điện thoại.** [Có GIF. **Nói phần bảo mật ngay, đừng chờ bị hỏi.**]

> Máy chạy app tự phục vụ luôn giao diện của nó qua HTTP cho thiết bị khác trong mạng.
> Điện thoại mở trình duyệt là thấy đủ trạng thái và trả lời được.
>
> [Nói ngay, trước khi có người giơ tay.]
>
> Trước khi ai hỏi: cái này **mặc định tắt**, chỉ trong mạng nội bộ, có token, và có
> mức token **chỉ đọc** cho trường hợp muốn cho người khác xem mà không cho gõ.
>
> Đây cũng là nhu cầu khiến mình không dùng được mấy app có sẵn. Lát nữa nói lại.

**Slide 22. Hỏi thẳng app.** [Có GIF]

> App nhiều thứ quá, mình tự làm mà còn quên phím tắt. Nên có một chỗ chat để hỏi
> "làm sao để...".
>
> Nó chạy với **mọi công cụ bị tắt**: không đọc file của bạn, không thấy session của
> bạn, không chạy được gì. Nó chỉ biết đúng một thứ là cách dùng app.
>
> [Bài học hay, nên kể.]
>
> Chỗ này có một bài học mình thích: **con bot chỉ biết đúng cái user guide**. Nên
> trong repo có một luật: PR nào đổi giao diện thì phải sửa user guide trong **cùng
> PR đó**. Vì nếu không, con bot sẽ rất tự tin bảo người dùng là tính năng đó không
> tồn tại.
>
> Đó là cách bắt tài liệu không bị mục mà không cần ai đi nhắc.

**Slide 23. Còn lại.** [Lướt nhanh, chỉ dừng 2 chỗ]

> Mấy thứ còn lại gom một slide. Ba bảng màu sáng tối. Tag và lọc. Xem usage token.
> `⌘K` tìm mọi thứ.
>
> Hai cái đáng dừng. Một, **chọn font và cỡ chữ riêng cho terminal, editor và giao
> diện** vì ba chỗ đó đọc ở khoảng cách khác nhau. Ai mắt kém sẽ thích.
>
> Hai, **danger shield**: đánh dấu dự án nào là nguy hiểm để không lỡ tay chạy
> `--dangerously-skip-permissions` ở đó.
>
> [Cuối slide, cho vui.]
>
> Và có một con pet pixel trong sidebar. Nó chả có tác dụng gì cả. Đó là lý do nó ở
> lại: app dùng cả ngày thì cần một chỗ không nghiêm túc.

**Slide 24. Phím tắt.** [Để mọi người chụp màn hình]

> Slide này để mọi người chụp lại. Mình chỉ nhấn ba cái hay nhất: `⌘K` bảng lệnh,
> `⇧⌘A` hộp thư, `⇧⌘L` template.
>
> Có một nguyên tắc đáng nói: **phím nào shell đang dùng thì app không lấy**. Ví dụ
> Ctrl+W trên Windows vẫn là xoá từ trong terminal, app không đụng vào.

---

## Phần 4: một ngày (0:41 → 0:46)

**Slide 25.** [Phân đoạn]

> Liệt kê tính năng thì khô. Kể một ngày thật cho dễ hình dung hơn.

**Slide 26.** [Kể như kể chuyện, đừng đọc bảng]

> Mở máy: bấm `⇧⌘L`, mở template quen. Bên trái session chính của repo đang làm, bên
> phải một con để hỏi vặt.
>
> Ra đề cho con chính. Trong lúc nó chạy, mở worktree mới cho một task khác rồi giao
> tiếp.
>
> Rồi đi pha cà phê. [Nhấn dòng này.] **Không canh.** Con nào cần thì nó tự gọi.
>
> Chuông kêu, bấm badge, nhảy tới đúng con đang chờ, duyệt rồi quay lại việc cũ.
>
> Xong một việc thì `⇧⌘D` xem nó sửa gì, đặt diff cạnh file gốc, đọc, rồi bảo nó
> commit.
>
> Rời bàn thì mở điện thoại xem có con nào đứng chờ không.
>
> [Chốt.]
>
> Cái dòng "đi pha cà phê" là cả điểm của app. Mọi thứ khác chỉ phục vụ để dòng đó
> thành sự thật.

**Slide 27.** [Slide mua tín nhiệm. Nói thẳng.]

> Nói thật cái nào mình dùng cái nào không.
>
> Ngày nào cũng dùng: chấm trạng thái và thông báo, chia màn hình, worktree, diff,
> `⌘K`. **Năm cái này là app.** Bỏ hết phần còn lại thì nó vẫn dùng được.
>
> Còn hẹn giờ, gửi nhiều session một lượt, thư viện prompt, xem dạng hội thoại: mình
> làm xong rồi ít đụng.
>
> **Mình làm mấy cái đó vì nghĩ sẽ cần, chứ không phải vì đã đau.** Đó là một lỗi, và
> lát nữa có một quy tắc rút ra từ nó.

---

## Phần 5: ai thì hợp (0:46 → 0:54)

**Slide 28.** [Phân đoạn]

> Phần cuối, và là phần mình nghĩ đáng nghe nhất kể cả khi bạn không định cài gì.

**Slide 29.**

> Bốn câu tự hỏi trước khi cài bất cứ thứ gì.
>
> Một: **bạn chạy mấy con một lúc?** Nếu là một thì thôi, không cần gì cả.
>
> [Nói câu này bằng giọng thật, nó mua được nhiều tín nhiệm.]
>
> Thật đấy. Nếu bạn chạy một con và thấy ổn thì buổi nay không có gì cho bạn cả, và
> mình thấy vậy là tốt.
>
> Hai: **trong lúc chờ bạn làm gì?** Ngồi canh thì không cần gì. Làm việc khác thì cần
> cái gọi mình về. Chạy con thứ hai thì cần thêm cô lập.
>
> Ba: **bạn chịu được bao lâu mới biết nó gọi?** Vài giây, hay vài phút, hay không
> quan trọng.
>
> Bốn: **bạn có hay rời khỏi máy không?** Câu này ít người hỏi, mà nó lại là câu quyết
> định với mình. Chính vì nó mà mấy app có sẵn không vừa.

**Slide 30.** [**Chạy `claude --help` ngay tại chỗ.** Slide này gây "ồ" to nhất buổi.]

> Trước khi cài thêm gì, kiểm tra thứ mình đã có. Claude Code tự nó đã kha khá.
>
> `claude --worktree` khởi động ngay trong worktree cô lập. Thêm `--tmux` có luôn
> phiên tmux. `--resume` lấy lại đúng cuộc chat cũ. `--permission-mode` chỉnh mức hỏi,
> chọn đúng là bớt hẳn số lần bị gọi.
>
> [Mở terminal, chạy `claude --help`.]
>
> Đây, mọi người xem. Rất nhiều người dùng hàng ngày mà chưa mở cái này bao giờ.
>
> Và ngoài app của mình còn mấy hình dạng khác: tmux hay zellij tự dựng, Claude Squad
> quản lý session trong terminal, Conductor là app Mac mỗi agent một worktree, Vibe
> Kanban là bảng việc kéo thẻ.
>
> [Nói một chuyện cho công bằng.]
>
> Có một rủi ro thật: Crystal, một app khá được ưa chuộng trong nhóm này, đã ngừng
> phát triển hồi tháng 2. Chọn công cụ trong thị trường mới thì cái mình chọn hôm nay
> có thể biến mất.

**Slide 31.** [Giữ cho cả buổi không thành quảng cáo. Nói thẳng, đừng làm nhẹ.]

> Và cái giá của việc tự làm.
>
> Một: **nó là một dự án thứ hai.** Có bug, có CI hỏng, có việc bảo trì. Thời gian
> tiết kiệm ở việc chính chảy ngược một phần vào đây.
>
> Hai: **mình là người dùng duy nhất.** Mọi lựa chọn đều vừa vặn với mình. Vừa là điểm
> mạnh, vừa là lý do nó có thể không hợp với bạn.
>
> Ba, và là cái thật nhất: **mình chưa đo được** công việc chính có nhanh hơn không.
> Cảm giác thì có, số liệu thì chưa. Mình biết vậy mà vẫn chưa đo, nói ra để mọi người
> đừng lặp lại.
>
> Nên khuyên thật lòng: **đừng tự làm.** Dùng cái có sẵn, trừ khi nhu cầu của bạn
> không có cái nào vừa, và bạn thấy việc làm công cụ tự nó đã vui.

**Slide 32.**

> Muốn thử thì làm theo thứ tự này.
>
> Tuần 1: **không cài gì cả.** Chỉ dùng Claude Code với `--worktree`. Mỗi ngày ghi 3
> lần: nó cần mình lúc mấy giờ, mình biết lúc mấy giờ. Cuối tuần có một con số thật.
>
> Tuần 2: thêm **đúng một** thứ, chọn theo con số tuần 1. Đo lại y hệt. Con số không
> giảm thì bỏ, đừng tiếc.
>
> Đừng đổi hai thứ cùng lúc, và đừng đánh giá bằng cảm giác ngày đầu tiên.

**Slide 33.**

> **Không có công cụ tốt nhất. Chỉ có công cụ vừa tay.**
>
> Bốn câu hỏi lúc nãy quan trọng hơn cả buổi nói này.
>
> Slide và ghi chú ở link dưới, mọi người mở bằng điện thoại là lấy được luôn.
>
> [Dừng vài giây rồi mới mở hỏi đáp.]

---

## Hỏi đáp (0:54 → 1:04)

**Slide 34.**

Đừng hỏi "có ai hỏi gì không", thường sẽ im. Mở bằng câu cụ thể:

> Ai đang chạy từ 4 con trở lên?

hoặc

> Có ai vừa nhận ra mình chỉ cần một con thôi không?

Phòng vẫn im thì quay lại slide 29, hỏi từng câu.

### Câu chuẩn bị sẵn

**Chạy nhiều con có tốn token hơn không?**
Có. Song song không làm mỗi lượt rẻ đi, chỉ làm nhiều lượt xảy ra cùng lúc. Đang chạm
trần gói thì song song chạm nhanh hơn.

**Bao nhiêu con là quá nhiều?**
Khi hàng chờ review dài hơn thời gian mình có để review. Con số đó thấp hơn số con
chạy được về mặt kỹ thuật nhiều.

**Claude tự đẻ subagent được mà, sao còn cần nhiều session?**
Hai thứ khác nhau chứ không thay nhau. Subagent chia một việc thành mấy việc con rồi
gộp kết quả, chung context, xong là tan. Session riêng là mấy việc không liên quan
nhau, mỗi cái một mạch hội thoại, sống qua nhiều ngày. Mình dùng cả hai cùng lúc.

**Sao không xài tmux cho xong?**
Được chứ, và nếu đã sống trong tmux thì đó là lựa chọn rẻ nhất. Cái tmux không cho là
tín hiệu "đang chờ", vì nó không đọc hook, và cái diff. Không đau hai chỗ đó thì tmux
là đủ.

**Có mở mã nguồn không?**
[Trả lời theo ý mình. Chưa quyết thì nói chưa quyết, đừng hứa.]

**Team dùng chung được không?**
Mới chạy một người. Nói gì về quy mô team cũng là đoán, nên mình không đoán.

**Nó làm anh nhanh hơn bao nhiêu?**
Chưa đo được tử tế. Xem lại slide 31. Mình biết mình đang có đúng cái cảm giác mà
nghiên cứu người ta cảnh báo.

**Sao không dùng Conductor cho rồi?**
Có thử. Nó tốt. Cái nó không có là mở được bằng điện thoại, và cái cây bốn tầng. Với
người không cần hai thứ đó thì Conductor là lựa chọn hợp lý hơn tự làm nhiều.

---

## Nếu trễ giờ

| Đang ở | Đồng hồ | Làm gì |
|---|---|---|
| Slide 11 | quá 20 phút | Bỏ slide 13, 16, 19 |
| Slide 25 | quá 43 phút | Bỏ slide 27, kể luôn vào phần 5 |
| Slide 29 | quá 50 phút | Bỏ slide 32, nói kế hoạch 2 tuần bằng lời trong 20 giây |

Không bao giờ cắt: slide 2, 7, 8, 9, 12, 27, 29, 31.
