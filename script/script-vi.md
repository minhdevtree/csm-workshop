# Kịch bản nói chi tiết

Workshop 50 phút nói + 10 phút hỏi đáp. Dev team. Tiếng Việt.

Cách dùng file này: cột thời gian là mốc tích luỹ tính từ lúc bắt đầu. Nếu tới
slide 19 mà đồng hồ đã quá 26 phút, cắt phần 3 xuống còn slide 16 và 17, bỏ slide
18. Đừng cắt phần 4.

Chữ **in đậm** là chỗ cần nhấn giọng. Chữ trong ngoặc vuông là chỉ dẫn sân khấu,
không đọc ra.

---

## Trước khi vào phòng

- [ ] Mở `slides/index.html` bằng trình duyệt, bấm `F` cho toàn màn hình.
- [ ] Bấm `T` một lần để xem chế độ sáng. Phòng sáng thì dùng chế độ sáng.
- [ ] Bấm `S` để bật ghi chú, kiểm tra nó nằm ở màn hình của bạn chứ không phải
      màn chiếu (nếu chỉ có một màn hình thì tắt đi, cầm bản in file này).
- [ ] Kiểm tra sáu GIF demo đã nằm trong `assets/` và slide 21 tới 26 hiện ảnh
      chứ không phải khung nét đứt.
- [ ] Mở sẵn một terminal ở tab khác, đã `cd` vào một repo thật, để chạy
      `claude --help` ở slide 16.
- [ ] Tắt thông báo trên máy. Trớ trêu thay, đây là buổi nói về việc bị ngắt quãng.

---

## Mở đầu (0:00 tới 0:03)

**Slide 1.**

[Không đọc slide. Đứng ra giữa, hỏi trước.]

> Trước khi bắt đầu tôi hỏi hai câu, mọi người giơ tay giúp tôi.
>
> Câu một: ai ở đây đang chạy **từ hai phiên Claude Code trở lên** cùng lúc?
>
> [Đếm to. Ghi nhận.]
>
> Câu hai: ai từng **mất một phiên** vì lỡ đóng terminal?
>
> [Đếm. Thường sẽ có tiếng cười.]

> Được rồi. Buổi hôm nay nói về đúng khoảng giữa hai câu hỏi đó.

[Nếu phần lớn phòng chỉ chạy một phiên: nói thêm một câu, "Nếu bạn đang chạy một
phiên và thấy ổn, phần đầu vẫn đáng nghe, còn phần sau bạn cứ coi như một ca bệnh
để tham khảo." Rồi rút ngắn phần 4 xuống ba slide đau thay vì sáu.]

**Slide 2.** [Chuyển slide]

> Trước khi bắt đầu tôi muốn nói rõ buổi này **không phải** cái gì, vì tôi có làm
> một cái app và tôi sẽ nói về nó ở phần bốn.
>
> Không có bảng so sánh công cụ nào nhiều tính năng hơn. Không có lời khuyên
> "hãy dùng cái tôi đang dùng". Đây không phải quảng cáo.
>
> Cái có ở đây là một cách tự hỏi để biết **bạn** cần gì, một bản đồ các hình
> dạng công cụ, và một case study thật, **kể cả phần dở của nó**.
>
> Nếu cuối buổi các bạn về mà không cài gì cả, nhưng biết rõ hơn mình cần gì,
> thì với tôi buổi này thành công.

**Slide 3.** [Lướt nhanh, không đọc từng dòng]

> Sáu phần, năm mươi phút, mười phút hỏi đáp. Phần bốn dài nhất và có demo.
> Nếu bị trễ tôi sẽ cắt phần ba chứ không cắt phần bốn.

---

## Phần 1: Nút thắt đã đổi chỗ (0:03 tới 0:11)

**Slide 4.** [Slide phân đoạn, chỉ một câu]

> Bắt đầu bằng câu hỏi: tại sao chúng ta lại phải bàn chuyện này vào **năm 2026**,
> chứ không phải năm 2023.

**Slide 5.**

> Trước đây, bạn nghĩ ra cách làm rồi bỏ phần lớn thời gian để **gõ nó ra**. Tốc
> độ gõ, độ thuộc API, độ quen codebase quyết định bạn xong nhanh hay chậm.
>
> Bây giờ agent gõ hộ. Cái còn lại của bạn là **ra đề bài**, **chờ**, và **kiểm
> tra lại**.
>
> Nghĩ về cái editor của các bạn một giây. Autocomplete, snippet, đa con trỏ,
> refactor tự động. Toàn bộ những thứ đó phục vụ **một việc mà bây giờ bạn làm ít
> đi rất nhiều**.
>
> Tôi không nói editor vô dụng. Tôi nói nó **không còn là nơi thời gian của bạn
> trôi đi**. Và khi phần việc thay đổi mà công cụ không đổi, bạn sẽ tối ưu nhầm chỗ.

**Slide 6.**

> Thời gian của bạn giờ nằm ở ba chỗ.
>
> **Ra đề bài.** Đây là việc duy nhất trong ba việc bạn không ủy thác được.
>
> **Chờ.** Ba tới mười phút mỗi lượt.
>
> **Kiểm tra lại.** Đọc diff, chạy test, quyết định nhận hay bỏ.
>
> [Hỏi phòng] Trong lúc chờ, các bạn làm gì?
>
> [Chờ vài câu trả lời. Câu thật thường là: xem điện thoại, đọc Slack, hoặc ngồi
> nhìn con trỏ nhấp nháy.]
>
> Cả buổi hôm nay xoay quanh **khoảng ở giữa**. Nhưng tôi sẽ nói trước cái bẫy,
> vì nó là thứ làm nhiều người thất bại: **chạy song song làm khoảng thứ hai ngắn
> lại, nhưng làm khoảng thứ ba dài ra.** Slide sau là bằng chứng.

**Slide 7.**

> DORA, báo cáo 2025 về phát triển phần mềm có AI hỗ trợ. Khảo sát gần năm nghìn
> người làm công nghệ.
>
> Kết luận một: áp dụng AI làm **throughput tăng**. Cái này ai cũng đoán được.
>
> Kết luận hai, ít người nói tới: áp dụng AI cũng làm **bất ổn định tăng**. Nhiều
> thay đổi hỏng hơn, nhiều việc phải làm lại hơn, thời gian khắc phục dài hơn.
>
> Câu tôi thích nhất trong báo cáo đó là câu bên trái: **AI không phải giải pháp
> đóng hộp, nó là một cái khuếch đại.**
>
> Nói cho gọn: **nền tốt thì AI tăng tốc, nền lộn xộn thì AI làm bạn lộn xộn
> nhanh hơn.**
>
> Áp vào chủ đề hôm nay: chạy mười agent song song trên một repo không có test là
> cách nhanh nhất để tạo ra mười thứ phải sửa. **Song song là bộ khuếch đại,
> không phải cái loa.**

**Slide 8.**

> Và đây là con số làm mọi người khó chịu.
>
> METR, tháng bảy 2025. Thử nghiệm ngẫu nhiên có đối chứng. Mười sáu lập trình
> viên mã nguồn mở giàu kinh nghiệm, hai trăm bốn mươi sáu tác vụ, trên **chính
> repo của họ**.
>
> Trước khi làm, họ dự đoán AI giúp họ nhanh hơn khoảng hai mươi tư phần trăm.
>
> Thực tế đo được: họ **chậm hơn mười chín phần trăm**.
>
> Và sau khi xong, họ **vẫn tin** mình đã nhanh hơn hai mươi phần trăm.
>
> [Dừng một nhịp, rồi nói ngay phần cảnh báo. Không được bỏ.]
>
> Tôi phải nói kèm một điều, nếu không là tôi trích dẫn không trung thực: **METR
> hiện đã gắn nhãn kết quả này là lịch sử.** Công cụ trong nghiên cứu là Cursor
> với Claude 3.5 và 3.7, tức là trước thời agent chạy dài. Đừng ai về nói "có
> nghiên cứu chứng minh AI làm chậm".
>
> Bài học thật **không nằm ở cột giữa**. Nó nằm ở khoảng cách giữa cột hai và cột
> ba: **cảm giác nhanh và nhanh thật là hai đại lượng khác nhau, và con người rất
> tệ trong việc phân biệt chúng.**
>
> Nên nếu tối nay các bạn về, cài một công cụ mới, và thấy sướng, thì **cái cảm
> giác sướng đó không phải bằng chứng**. Cuối bài tôi sẽ nói cách đo thay cho
> cách cảm.

**Slide 9.**

> Con số cuối của phần này. Gloria Mark, UC Irvine, nghiên cứu quan sát tại chỗ,
> được trích dẫn nhiều nhất về công việc bị ngắt quãng.
>
> **Hai mươi ba phút** để quay lại đúng mạch việc ban đầu, sau **một** lần bị ngắt.
> Và trung bình có hai việc khác xen vào trước khi người ta quay lại việc cũ.
>
> [Kể chuyện thật, ngắn.]
>
> Tôi từng có một buổi chiều mở ba terminal, cứ vài phút lại alt-tab qua từng cái
> xem xong chưa. Cuối buổi nhìn lại, tôi không làm được việc gì tử tế ở giữa cả.
> Ba agent đều xong việc, còn tôi thì không.
>
> Điểm cần đọng lại: **chạy song song mà không có cách điều hướng chú ý thì không
> phải là làm nhiều việc. Đó là tự ngắt quãng mình liên tục.**

**Slide 10.**

> Nên câu hỏi đúng **không phải** là "công cụ nào mạnh nhất".
>
> Mà là: **trong ba khoảng thời gian của tôi, khoảng nào đang đau nhất, và công
> cụ nào chạm được vào đúng khoảng đó.**
>
> [Dừng. Đây là bản lề của cả bài. Để câu này đứng vài giây.]

---

## Phần 2: Sáu câu hỏi (0:11 tới 0:19)

**Slide 11.** [Phân đoạn]

> Giờ tới phần thực tế. Sáu câu hỏi. Trả lời thật lòng, không cần nói ra.

**Slide 12.** [Đọc lướt cả sáu, không giải thích từng câu]

> Câu một: bạn chạy mấy agent một lúc? **Nếu câu trả lời là một, dừng lại. Bạn
> không cần công cụ nào cả**, và đó là một kết luận hợp lệ.
>
> Câu hai: trong lúc chờ, bạn làm gì.
> Câu ba: bạn cần biết agent gọi sau bao lâu.
> Câu bốn: bạn đọc thay đổi kiểu gì.
> Câu năm: việc của bạn có chia nhánh không.
> Câu sáu: bạn có rời khỏi máy không.
>
> Ba câu quan trọng nhất tôi sẽ đào sâu ở hai slide sau.

**Slide 13.** [Slide đáng dừng lâu nhất phần này. Đọc theo hàng.]

> Câu số hai là câu phân loại mạnh nhất. Đọc theo hàng.
>
> Nếu trong lúc chờ bạn **ngồi nhìn**, thì bạn không thiếu gì cả. Đừng đổi gì. Thật.
>
> Nếu bạn **chuyển sang việc khác**, cái bạn thiếu là một tín hiệu gọi bạn về.
> Thông báo, badge, một hộp thư liệt kê cái đang chờ.
>
> Nếu bạn **chạy agent thứ hai**, bạn thiếu hai thứ: cô lập, và cách biết cái nào
> đang chờ.
>
> Nếu bạn **chạy năm agent**, bạn thiếu cả hai thứ trên, cộng thêm khả năng review
> nhanh.
>
> Để ý cột giữa. **Không có dòng nào cần "nhiều tính năng hơn".** Mỗi dòng thiếu
> đúng một thứ.
>
> [Nếu có người nhận mình ở dòng bốn, hỏi lại: "bạn review kiểu gì?" Câu trả lời
> gần như luôn là "đọc PR trên GitLab", và đó chính là chỗ đau tiếp theo của họ.]

**Slide 14.**

> Câu ba, độ trễ bạn chịu được. **Đây là chỉ số duy nhất trong cả bài mà tôi
> khuyên các bạn đo thật.**
>
> Cách đo rẻ tới mức không có lý do gì để không làm: mở đồng hồ, chạy một agent,
> làm việc khác, và ghi lại **khoảng cách giữa lúc nó thật sự cần bạn và lúc bạn
> phát hiện ra**. Làm ba lần trong một buổi chiều là bạn có một con số.
>
> Con số đó chọn công cụ giúp bạn, chứ không phải bảng tính năng của ai.
>
> Câu năm, cô lập. Hai agent sửa cùng một thư mục sẽ giẫm lên nhau, và bạn mất
> nhiều thời gian gỡ hơn số thời gian tiết kiệm được.
>
> **Cô lập không phải là một tính năng để so sánh. Nó là điều kiện để song song
> có nghĩa.** Công cụ nào không có nó thì thực chất chỉ phục vụ một agent.
>
> Câu trả lời chuẩn cho câu năm là git worktree. Và Claude Code đã có sẵn nó.
>
> [Nếu phòng chưa quen worktree, giải thích một câu: nhiều thư mục làm việc trên
> cùng một repo, mỗi thư mục một nhánh, dùng chung lịch sử git. Không phải clone
> lại.]

---

## Phần 3: Bản đồ công cụ (0:19 tới 0:27)

**Slide 15.** [Phân đoạn]

> Có sáu câu trả lời rồi, giờ xem chúng dẫn tới đâu. Tôi sẽ không xếp hạng cái
> nào, chỉ nói mỗi hình dạng đánh đổi cái gì.

**Slide 16.** [Slide gây ngạc nhiên nhất trong bài]

> Trước khi thêm bất cứ thứ gì, kiểm tra thứ các bạn **đã có**.
>
> `--worktree` khởi động Claude ngay trong một worktree cô lập. Thêm `--tmux` thì
> có luôn phiên tmux cho nó.
>
> `--resume` lấy lại đúng cuộc hội thoại cũ. Đóng terminal không còn là mất trắng.
>
> `--permission-mode` cho bạn chọn từ hỏi từng bước tới tự nhận sửa file. Chọn
> đúng mức là **giảm hẳn số lần bị gọi**, mà không cần công cụ nào cả.
>
> Và **hooks**: hơn ba mươi sự kiện trong vòng đời một lượt. Handler có thể là
> một lệnh, một HTTP endpoint, một MCP tool, hoặc một agent khác.
>
> [Chuyển sang terminal đã mở sẵn, chạy `claude --help` ngay tại chỗ. Sống động
> hơn slide rất nhiều.]
>
> Nói thêm về hooks vì nó quan trọng: **đây là cái mà mọi công cụ quản lý phiên
> đều dựa vào** để biết agent đang làm gì. Không có hooks thì chỉ còn cách đoán
> qua đầu ra terminal. Mà đoán thì không bao giờ biết chắc lúc nào agent **đang
> chờ** và lúc nào nó **đang nghĩ**.

**Slide 17.** [Đi từ trên xuống, mỗi dòng một câu. Dừng lâu nhất ở cột cuối.]

> Năm hình dạng.
>
> **Không gì cả**, nhiều tab terminal. Hợp với một tới hai agent và luôn ngồi máy.
> Đổi lại: không có tín hiệu gọi.
>
> **Multiplexer**, tmux hoặc zellij, hoặc Claude Squad. Hợp với người sống trong
> terminal và muốn tự script layout. Đổi lại: phải tự dựng, và không có diff.
>
> **Trong IDE**, Claude Code cho VS Code hoặc JetBrains. Hợp khi muốn review ngay
> chỗ đang code. Đổi lại: nhiều agent thì chật.
>
> **App quản lý**, ví dụ Conductor, và cái tôi tự làm. Hợp với nhiều agent, nhiều
> repo. Đổi lại: thêm một app phải học.
>
> **Bảng việc**, Vibe Kanban hoặc agent chạy trên cloud. Hợp khi giao việc rồi đi,
> review qua PR. Đổi lại: vòng phản hồi dài.
>
> [Ghi chú trung thực, nên nói.]
>
> Một chuyện đáng nói về rủi ro: Crystal, một app mã nguồn mở khá được ưa chuộng
> trong nhóm này, **đã ngừng phát triển tháng 2 năm 2026** và trỏ người dùng sang
> một sản phẩm đóng nguồn có phí. Đó là rủi ro thật của thị trường mới: **cái bạn
> chọn hôm nay có thể biến mất.**
>
> [Nếu ai hỏi "vậy cái nào tốt nhất": "Câu đó không có đáp án, và đó chính là lý
> do phần hai có sáu câu hỏi."]

**Slide 18.**

> Ba quy tắc đọc bản đồ này.
>
> Một: chọn hình dạng **nhỏ nhất** giải được vấn đề bạn **đang** có, không phải
> vấn đề bạn nghĩ mình sẽ có sau này.
>
> Hai: nếu bạn chưa từng bị đau vì một vấn đề, đừng chọn công cụ vì nó giải vấn
> đề đó. Bạn trả giá bằng độ phức tạp mà không nhận lại gì.
>
> [Thú nhận một cái để câu này thật: kể một tính năng bạn làm vì "sau này sẽ cần"
> mà tới giờ chưa dùng lần nào.]
>
> Ba: **đổi một thứ một lần.** Đổi hai thứ cùng lúc thì bạn không bao giờ biết
> cái nào có tác dụng.

---

## Phần 4: Case study (0:27 tới 0:43)

**Slide 19.** [Phân đoạn]

> Giờ tới phần tôi kể chuyện của mình. Nghe với tâm thế **một ca bệnh**, không
> phải một lời khuyên.

**Slide 20.**

> Sáu câu hỏi đó, trả lời cho trường hợp của tôi.
>
> Ba tới sáu agent, trên nhiều repo khác nhau cùng lúc. Lúc chờ thì tôi chạy agent
> khác hoặc review cái vừa xong. Độ trễ chịu được là vài giây, chờ lâu hơn là tôi
> mất mạch. Tôi cần diff tử tế, và cần nó nằm cạnh file đang mở. Tôi chia nhánh
> thường xuyên. Và tôi **hay rời khỏi máy**, muốn theo dõi từ điện thoại.
>
> [Nhấn dòng cuối.]
>
> Cái dòng cuối là dòng quan trọng nhất. Nhu cầu "rời máy và trả lời từ điện
> thoại" là nhu cầu **hiếm**, và nó là lý do lớn nhất khiến các lựa chọn có sẵn
> không vừa với tôi. Đây là ví dụ sống của thông điệp cả buổi: **nhu cầu riêng
> quyết định lựa chọn, không phải bảng tính năng.**

**Slide 21 tới 26.** [Sáu cặp đau và cách giải, mỗi slide khoảng 90 giây, có GIF]

Với mỗi slide, nhịp giống nhau: đọc cái đau bằng giọng kể chuyện thật, để GIF
chạy một vòng trong im lặng, rồi nói một câu về **bài học chuyển giao được**.

**Slide 21, không biết cái nào đang chờ.**

> Ba phiên đang chạy. Một cái đã hỏi tôi "có cho phép chạy lệnh này không" từ bốn
> phút trước. Tôi không biết, vì nó nằm ở tab tôi không nhìn.
>
> [Để GIF chạy một vòng.]
>
> Trạng thái này lấy từ **hook của Claude Code**, không phải đoán qua đầu ra
> terminal.
>
> Đây là bài học chuyển giao được, và là bài học quan trọng nhất trong sáu cái:
> **"đang chờ" là một sự kiện, không phải một suy đoán.** Nhìn đầu ra terminal
> thì chỉ biết có chữ chạy hay im lặng. Mà im lặng có thể là đang nghĩ, cũng có
> thể là đang chờ. Hook nói thẳng cái nào là cái nào. Ai định tự dựng công cụ thì
> bắt đầu từ hook.

**Slide 22, mất phiên.**

> Đóng nhầm tab là mất cả cuộc hội thoại. Cả buổi sáng bối cảnh đi theo.
>
> [GIF]
>
> Cách giải: tiến trình terminal sống ở tiến trình chính của app, **không sống
> trong tab**. Chuyển tab chỉ gắn hoặc gỡ phần hiển thị.
>
> Bài học: **vòng đời của tiến trình không nên gắn với vòng đời của cái khung
> nhìn.** Đây là lỗi mà rất nhiều công cụ tự dựng mắc phải, kể cả script tmux tự
> viết.

**Slide 23, nhánh giẫm nhau.**

> Hai agent trên cùng một repo, cùng một thư mục. Cái này sửa file cái kia đang
> đọc.
>
> [GIF]
>
> Nhắc lại câu ở phần hai: **cô lập là điều kiện, không phải tính năng.** Đây là
> chỗ nó thành hình.

**Slide 24, review.**

> Agent xong. Giờ tôi phải nhảy ra ngoài, mở một app khác, để trả lời một câu duy
> nhất: nó vừa đổi cái gì.
>
> [GIF]
>
> Nối lại với DORA lúc nãy: **kiểm tra lại là nút thắt mới.** Đây là tính năng
> phục vụ đúng cái nút thắt đó, và cũng là tính năng tôi làm **sau cùng**, sau khi
> đã đau đủ lâu. Đó cũng là ví dụ cho quy tắc hai: tôi không làm nó vì app quản lý
> nào cũng có diff, mà vì tôi đã alt-tab ra ngoài đủ nhiều lần.

**Slide 25, rời máy.**

> Rời bàn mười lăm phút là mù hoàn toàn.
>
> [GIF hoặc video điện thoại]
>
> [Nói phần bảo mật ngay, đừng chờ bị hỏi.]
>
> Trước khi có người hỏi: cái này **mặc định tắt**, chỉ chạy trong mạng nội bộ, có
> token, và có mức token **chỉ đọc** cho trường hợp muốn cho người khác xem mà
> không cho gõ.

**Slide 26, không nhớ app làm được gì.**

> App có quá nhiều thứ. Tôi tự làm mà còn quên phím tắt và quên cả tính năng mình
> đã viết.
>
> [GIF]
>
> Con trợ lý này chạy với **mọi công cụ bị tắt**: không đọc file của bạn, không
> thấy phiên của bạn, không chạy được gì. Nó chỉ biết cách dùng app.
>
> Và đây là bài học tôi thích nhất: **tài liệu không phải thứ viết sau cho có. Nó
> là thứ duy nhất con bot biết.** Trong repo có một luật: PR nào đổi giao diện thì
> phải cập nhật user guide trong **cùng PR đó**. Vì nếu không, con bot sẽ rất tự
> tin nói với người dùng rằng tính năng đó không tồn tại.
>
> Đó là cách buộc tài liệu không bị mục mà không cần ai đi nhắc.

**Slide 27.** [Nói con số rồi đóng khung lại ngay]

> Dự án này bằng số. Bốn mươi tám ngày. Bảy trăm hai mươi bảy commit. Bảy mươi
> hai nghìn dòng TypeScript. Hai nghìn bảy trăm lẻ tám test. Năm mươi mốt phiên
> bản đã phát hành. Ba nền tảng chạy trong CI.
>
> [Đừng khoe. Chuyển ngay sang cách đọc.]
>
> Con số đáng nói nhất **không phải** bảy mươi hai nghìn dòng. Là **hai nghìn bảy
> trăm test**.
>
> Vì khi agent viết phần lớn code, cái bạn cần không phải là đọc từng dòng. Cái
> bạn cần là **một cái lưới bắt được lúc nó sai**. Test là hợp đồng bạn viết, code
> là thứ agent điền vào.
>
> Và đây chính là "nền tốt thì AI tăng tốc" của DORA. **Không có cái lưới đó thì
> bảy trăm hai mươi bảy commit trong bốn mươi tám ngày là một thảm hoạ, chứ không
> phải một thành tích.**

**Slide 28.** [Slide quan trọng ngang slide 2]

> Và đây là phần tôi không muốn kể.
>
> Cái giá một: tự làm công cụ là **một dự án thứ hai**. Nó có bug, có CI hỏng, có
> việc bảo trì. Thời gian tôi tiết kiệm ở việc chính, một phần không nhỏ chảy
> ngược vào đây.
>
> Cái giá hai: tôi là **người dùng duy nhất**. Mọi lựa chọn thiết kế đều vừa vặn
> với tôi. Đó vừa là điểm mạnh, vừa là lý do nó có thể không hợp với bạn.
>
> Cái giá ba, và là cái thật nhất: con số bốn mươi tám ngày nghe ấn tượng, nhưng
> nó **không nói gì về việc công việc chính của tôi có nhanh hơn không**. Đó là
> hai đại lượng khác nhau, và tôi **chưa đo được cái thứ hai một cách tử tế**.
>
> Tức là tôi đang có đúng cái cảm giác mà METR cảnh báo ở phần một. Tôi biết vậy,
> và tôi vẫn chưa đo. Nói ra để các bạn đừng lặp lại.
>
> Nên khuyến nghị thật lòng của tôi cho phòng này là: **đừng tự làm.** Dùng cái có
> sẵn, trừ khi nhu cầu của bạn thật sự không có cái nào vừa, và bạn thấy việc làm
> công cụ tự nó đã vui.

---

## Phần 5: Rút ra (0:43 tới 0:50)

**Slide 29.** [Phân đoạn]

> Bỏ app của tôi sang một bên. Năm điều sau đúng với mọi lựa chọn.

**Slide 30.** [Slide để chụp màn hình. Nói chậm, mỗi ý một câu, không thêm ví dụ mới.]

> Một: **đo bằng độ trễ, không bằng số tính năng.** Chỉ số đáng theo dõi là bao
> lâu kể từ lúc agent cần bạn tới lúc bạn biết.
>
> Hai: **song song chỉ có lãi khi có cách điều hướng chú ý.**
>
> Ba: **cô lập là điều kiện, không phải tính năng.**
>
> Bốn: **kiểm tra lại là nút thắt mới.** DORA đã đo. Công cụ nào rút ngắn được
> vòng review sẽ thắng công cụ nào chỉ chạy được nhiều agent hơn.
>
> Năm: **công cụ tốt nhất là cái bạn còn dùng sau hai tuần.** Mọi thứ khác là cảm
> giác mới lạ, và cảm giác thì METR đã nói rồi.

**Slide 31.**

> Nếu muốn thử, làm theo thứ tự này.
>
> Tuần một: **không cài gì cả.** Chỉ dùng Claude Code với `--worktree`. Mỗi ngày
> ghi ba lần: agent cần bạn lúc mấy giờ, bạn biết lúc mấy giờ. Cuối tuần bạn có
> một con số thật.
>
> Tuần hai: thêm **đúng một** lớp, chọn theo con số tuần một. Đo lại đúng cách đó.
> Nếu con số không giảm, **bỏ nó đi mà không tiếc**.
>
> Đừng đổi hai thứ cùng lúc, và đừng đánh giá bằng cảm giác của ngày đầu tiên.
>
> Cách đo này rẻ tới mức không có lý do gì để không làm, và nó biến một cuộc tranh
> luận về sở thích thành một con số.

**Slide 32.**

> **Không có công cụ tốt nhất. Chỉ có công cụ vừa tay.**
>
> Sáu câu hỏi ở phần hai quan trọng hơn toàn bộ phần còn lại của buổi này.
>
> Slide, kịch bản và toàn bộ nguồn dẫn nằm ở link dưới.
>
> [Dừng. Để câu này đứng một mình vài giây trước khi mở hỏi đáp.]

---

## Hỏi đáp (0:50 tới 1:00)

**Slide 33.**

Đừng hỏi "có ai hỏi gì không", thường sẽ im lặng. Mở bằng một câu mồi cụ thể:

> Ai đang ở **dòng thứ tư** của cái bảng lúc nãy, chạy từ năm agent trở lên?

hoặc

> Có ai vừa nhận ra mình đang ở **dòng một** mà lâu nay tưởng mình ở dòng ba không?

Nếu phòng vẫn im, quay lại slide 13 và đi từng dòng, hỏi ai ở dòng nào.

### Câu chuẩn bị sẵn

**Chạy nhiều agent có tốn nhiều token hơn không?**
Có. Song song không làm mỗi lượt rẻ đi, nó chỉ làm nhiều lượt xảy ra cùng lúc. Nếu
bạn đang chạm trần gói, song song sẽ chạm nhanh hơn.

**Bao nhiêu agent là quá nhiều?**
Khi hàng đợi review của bạn dài hơn thời gian bạn có để review. Con số đó khác nhau
ở mỗi người, và nó thấp hơn nhiều so với số agent bạn chạy được về mặt kỹ thuật.

**Sao không dùng tmux cho xong?**
Hoàn toàn được, và nếu bạn đã sống trong tmux thì đó là lựa chọn rẻ nhất. Cái tmux
không cho bạn là tín hiệu "agent đang chờ" (nó không đọc hook) và diff. Nếu hai thứ
đó không phải chỗ đau của bạn thì tmux là đủ.

**Có định mở mã nguồn không?**
[Trả lời theo ý bạn. Nếu chưa quyết thì nói thẳng là chưa quyết, đừng hứa.]

**Team dùng chung được không?**
Tôi mới chỉ chạy một người. Mọi câu trả lời của tôi về quy mô team đều là suy đoán,
nên tôi sẽ không đoán.

**Nó có làm anh làm việc nhanh hơn không?**
Tôi chưa đo được một cách tử tế. Xem lại slide 28. Tôi biết mình đang có đúng cái
cảm giác mà METR cảnh báo.

---

## Nếu bị trễ giờ

| Đang ở | Đồng hồ | Làm gì |
|---|---|---|
| Slide 10 | quá 13 phút | Bỏ slide 14, gộp câu 3 và 5 vào lời nói ở slide 13 |
| Slide 19 | quá 28 phút | Bỏ slide 18. Ở phần 4 chỉ demo slide 21, 24, 25 |
| Slide 27 | quá 45 phút | Bỏ slide 31, nói kế hoạch hai tuần bằng lời trong 30 giây |

Không bao giờ cắt: slide 2, slide 10, slide 13, slide 28, slide 30.
