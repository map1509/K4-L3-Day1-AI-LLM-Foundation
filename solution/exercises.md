# K4 — Ngày 1: Bài Tập & Phản Ánh
## Khám Phá LLM API | Phiếu Thực Hành

**Thời lượng:** 4 tiếng
**Cách làm:** Trả lời từng câu ngay sau khi hoàn thành block tương ứng —
đừng để dồn hết về cuối buổi. Thay dòng `*Câu trả lời của bạn*` bằng câu
trả lời thật (chấm tự động sẽ đếm số câu đã trả lời).

---

## Block 1 — API Cơ Bản (trả lời sau Checkpoint 1)

### Câu 1.1 — Độ nhạy của temperature
Gọi `call_openai` với temperature 0.0, 0.5, 1.0 và 1.5 dùng prompt
 0.0: "Một sự thật thú vị nữa về Việt Nam là đất nước này có một nền ẩm thực đường phố phong phú và đa dạng, được biết đến rộng rãi trên toàn thế giới. Một trong những món ăn nổi tiếng nhất là phở - một món súp gồm bánh phở, nước dùng thơm ngon, thịt bò hoặc gà, và các loại rau thơm tươi sống. Phở đã trở thành biểu tượng ẩm thực của Việt Nam và được yêu thích không chỉ trong nước mà còn trên toàn cầu.

 Ngoài phở, ẩm thực đường phố Việt Nam còn rất nhiều món khác như bánh mì, bún chả, gỏi cuốn, và bánh xèo, mỗi món đều mang trong mình sự kết hợp độc đáo của các hương vị và nguyên liệu. Văn hóa ăn uống ở các quán vỉa hè và chợ đêm cũng góp phần tạo nên sức hấp dẫn độc đáo, khiến cho ẩm thực Việt trở thành một phần quan trọng trong trải nghiệm của du khách khi đến thăm đất nước này."

 0.5:"Một sự thật thú vị khác về Việt Nam là đất nước này có một hệ thống ngầm của vô số các di sản thiên nhiên và văn hóa được UNESCO công nhận. Tính đến nay, Việt Nam có 8 di sản thế giới được UNESCO công nhận, bao gồm 5 di sản văn hóa (như Hoàng thành Thăng Long, Quần thể di tích cố đô Huế) và 2 di sản tự nhiên (như Vịnh Hạ Long, Vườn quốc gia Phong Nha-Kẻ Bàng) cùng 1 di sản hỗn hợp (Tràng An).

 Những di sản này thể hiện sự đa dạng và phong phú của văn hóa, lịch sử và cảnh quan thiên nhiên của Việt Nam, đồng thời thu hút hàng triệu du khách mỗi năm. Du khách đến Việt Nam thường tìm kiếm cơ hội khám phá những di sản này để hiểu rõ hơn về văn hóa và lịch sử đặc sắc của đất nước. Ví dụ, Vịnh Hạ Long nổi tiếng với hàng ngàn đảo đá vôi kỳ vĩ, trong khi Quần thể di tích cố đô Huế là minh chứng cho thời kỳ hoàng kim của triều đại nhà Nguyễn."

 1.0:"Một sự thật thú vị về Việt Nam là đất nước này sở hữu một trong những mạng lưới sông ngòi phong phú nhất thế giới, với hai con sông lớn là sông Hồng và sông Mekong. Đặc biệt, Đồng bằng sông Cửu Long ở miền Nam Việt Nam là vùng đất phù sa màu mỡ bậc nhất, được ví như "vựa lúa" của cả nước vì sản xuất ra một lượng lớn gạo để tiêu thụ trong nước và xuất khẩu.

 Ngoài ra, hệ thống sông ngòi này còn là nơi sinh sống của rất nhiều loài động thực vật đa dạng và là nguồn cung cấp thủy sản quan trọng. Cuộc sống của người dân vùng sông nước cũng gắn liền với sông ngòi qua các hoạt động như đánh bắt cá, vận chuyển hàng hóa và du lịch đường thủy. Những chợ nổi trên sông như Cái Răng hay Phong Điền là điểm đến hấp dẫn, nơi du khách có thể trải nghiệm nét văn hóa độc đáo và sinh động của đời sống miền Tây Nam Bộ."

 1.5:"Một sự thật thú vị về Việt Nam là đất nước này có một hệ thống hang động rộng lớn và kỳ vĩ, trong đó nổi bật nhất là Hang Sơn Đoòng - hang động lớn nhất thế giới. Được phát hiện vào năm 1991 và chính thức thám hiểm vào năm 2009, Hang Sơn Đoòng nằm trong quần thể hang động Phong Nha-Kẻ Bàng thuộc tỉnh Quảng Bình.

 Hang Sơn Đoòng có kích thước ấn tượng với chiều dài hơn 9 km, chiều cao của trần hang lên đến 200 m, và rộng khoảng 150 m. Bên trong hang là một hệ sinh thái độc đáo với rừng nguyên sinh, sông ngầm và cả những đám mây riêng biệt. Những khối thạch nhũ và măng đá khổng lồ bên trong hang tạo ra cảnh quan ngoạn mục, làm say lòng những người yêu thích thám hiểm và thiên nhiên.

 Khám phá Hang Sơn Đoòng là một trải nghiệm đặc biệt và chỉ có một số lượng giới hạn du khách được phép tham gia mỗi năm để bảo vệ môi trường tự nhiên. Hang động này đã thu hút sự quan tâm của các nhà khoa học, nhà khám phá và du khách từ khắp nơi trên thế giới."
**Bạn nhận thấy quy luật gì qua bốn phản hồi?** (2–3 câu)
> Khi điều chỉnh temperature, có sự thay đổi về cân bằng giữa tính quyết đoán và tính sáng tạo của mô hình trong việc tạo ra các câu trả lời.Giá trị temperature thấp ưu tiên cho sự chính xác và ổn định, trong khi giá trị temperature cao dần lên thì câu trả lời càng có tính đa dạng và bất ngờ.Ở temperature 1.5,phản hồi có thể cực kỳ sáng tạo, nhưng đôi khi dẫn tới việc mô hình đưa ra thông tin bất thường hoặc không chính xác. Ở mức này, mô hình có nhiều kiểu câu trả lời hơn, có thể gây ra tính ngẫu nhiên cao.

### Câu 1.2 — Chọn temperature cho sản phẩm
**Bạn sẽ đặt temperature bao nhiêu cho chatbot hỗ trợ khách hàng, và tại sao?**
> Temperature thấp (khoảng 0.2–0.4), vì chatbot hỗ trợ khách hàng cần trả lời chính xác, nhất quán và đúng chính sách hơn là sáng tạo. Temperature thấp giúp giảm hallucination (bịa thông tin) và giữ giọng điệu chuyên nghiệp, ổn định qua nhiều lần hỏi.

### Câu 1.3 — Đánh đổi chi phí
Kịch bản: 10.000 người dùng hoạt động mỗi ngày, mỗi người gọi API 3 lần,
mỗi lần trung bình ~350 token đầu ra.

**Ước tính GPT-4o đắt hơn GPT-4o-mini bao nhiêu lần cho workload này? Nêu một
trường hợp GPT-4o xứng đáng với chi phí và một trường hợp nên dùng mini:**
> Chi phí/ngày (10.000 × 3 × 350 = 10,5 triệu token output):
- GPT-4o ($10/1M): ~$105
- GPT-4o-mini ($0,60/1M): ~$6,3
- →GPT-4o đắt hơn ~16,7 lần

Dùng GPT-4o: câu hỏi phức tạp, cần suy luận nhiều bước (tranh chấp hoàn tiền, khách hàng giận dữ cần xử lý khéo) — sai sót ở đây gây thiệt hại lớn hơn nhiều so với chênh lệch chi phí.

Dùng GPT-4o-mini: câu hỏi lặp lại, đơn giản (giờ làm việc, theo dõi đơn hàng, chính sách cơ bản) — chiếm phần lớn traffic, chất lượng không chênh lệch nhiều nhưng tiết kiệm đáng kể ở volume lớn.

---

## Block 2 — System Prompt & Token (trả lời sau Checkpoint 2)

### Câu 2.1 — Sức mạnh của persona
Gọi `chat_with_system_prompt` hai lần với cùng câu hỏi
**"Giải thích blockchain là gì?"** nhưng hai system prompt khác nhau:
- "Bạn là giáo viên tiểu học, giải thích thật đơn giản cho trẻ 8 tuổi."
- "Bạn là chuyên gia tài chính, trả lời chuyên sâu bằng thuật ngữ kỹ thuật."

**Hai phản hồi khác nhau như thế nào (độ dài, từ vựng, ví dụ)? System prompt
ảnh hưởng đến hành vi model ra sao?** (3–4 câu)
> Hai phản hồi khác nhau chủ yếu ở độ dài, từ vựng, và mức độ phức tạp của giải thích. Phản hồi đầu tiên ngắn gọn, sử dụng từ ngữ dễ hiểu và đưa ra ví dụ đồ chơi đơn giản, phù hợp với trẻ em. Trong khi đó, phản hồi thứ hai dài hơn, sử dụng nhiều thuật ngữ kỹ thuật như "cryptographic hash function", "Proof of Work", và cung cấp nhiều chi tiết hơn về chức năng của blockchain trong các ngành khác nhau. System prompt hướng dẫn mô hình điều chỉnh phong cách và mức độ chi tiết của phản hồi để phù hợp với đối tượng cụ thể.

### Câu 2.2 — tiktoken vs đếm từ
Chọn một đoạn văn tiếng Việt ~100 từ. So sánh số token theo `count_tokens`
(tiktoken) với ước lượng `số từ / 0.75` mà Part 1 đã dùng.

**Hai con số chênh nhau bao nhiêu phần trăm? Vì sao tiếng Việt thường tốn
nhiều token hơn tiếng Anh cùng độ dài?**
> 2 con số chênh lệch nhau khoảng 7%,do Tiếng Việt có dấu còn Tiếng Anh thì không.

---

## Block 3 — Streaming & Độ Bền (trả lời sau Checkpoint 3)

### Câu 3.1 — Trải nghiệm người dùng với streaming
**Streaming quan trọng nhất trong trường hợp nào, và khi nào thì
non-streaming lại phù hợp hơn?** (1 đoạn văn)
> Streaming quan trọng nhất khi có người dùng chờ trực tiếp và output dài (chatbot, trợ lý viết), vì nó giảm độ trễ cảm nhận và cho phép phản hồi/ngắt sớm. Non-streaming phù hợp hơn khi output cần xử lý trọn vẹn trước khi dùng,như JSON có cấu trúc để parse, cần kiểm duyệt trước khi hiển thị, hoặc chạy batch không có người chờ.

### Câu 3.2 — Vì sao backoff theo cấp số nhân?
**So với delay cố định (ví dụ luôn chờ 1 giây), exponential backoff có lợi
thế gì khi API bị quá tải? Điều gì xảy ra nếu hàng nghìn client cùng retry
với delay cố định giống nhau?**
> Exponential backoff: mỗi lần fail thì đợi lâu hơn (1s→2s→4s...), cho server thời gian hồi phục thay vì bị dội liên tục. Thường thêm jitter (random nhẹ) để các client không retry trùng giờ nhau.

Delay cố định = vấn đề "thundering herd": hàng nghìn client cùng fail → cùng đợi đúng 1 giây → cùng retry lại cùng một lúc. Server vừa thở được 1 giây thì lại ăn nguyên một đợt sóng request y hệt lần trước, cộng thêm request mới đang tới. Cứ thế lặp lại, server không kịp hồi phục, outage kéo dài dù ban đầu chỉ là quá tải tạm thời.

---

## Block 4 — Mini-Project (trả lời sau Checkpoint 4)

### Câu 4.1 — Thiết kế persona
**Bạn chọn persona gì cho trợ lý của mình? Viết lại system prompt đó và giải
thích 1–2 lựa chọn từ ngữ quan trọng trong prompt (ví dụ: vì sao yêu cầu
"trả lời ngắn gọn", vì sao chỉ định ngôn ngữ...):**
> Tôi chọn persona cho trợ lý của mình là một người đồng hành thông minh và hỗ trợ đa dạng, với phong cách giao tiếp thân thiện
System Prompt:
"Hãy cung cấp câu trả lời rõ ràng, ngắn gọn và dễ hiểu.Sử dụng ngôn ngữ tiếng Việt."

"Rõ ràng, ngắn gọn và dễ hiểu": Việc yêu cầu câu trả lời rõ ràng và ngắn gọn giúp tôi nhanh chóng nắm bắt được thông tin cần thiết mà không bị lạc trong các chi tiết không quan trọng.

"Ngôn ngữ tiếng Việt": Việc chỉ định ngôn ngữ Tiếng Việt vì nó là ngôn ngữ tôi hay dùng nhất.

### Câu 4.2 — Hạn chế & cải thiện
**Trợ lý của bạn hiện có hạn chế lớn nhất là gì (ví dụ: history chỉ 3 lượt,
không có bộ nhớ dài hạn, không kiểm duyệt nội dung...)? Đề xuất một cải
thiện cụ thể và mô tả ngắn cách triển khai:**
> Hạn chế lớn nhất hiện tại của trợ lý là không có bộ nhớ dài hạn.
Cải thiện: Tích Hợp Bộ Nhớ Dài Hạn
Tích hợp một hệ thống bộ nhớ dài hạn cho phép trợ lý lưu trữ và truy xuất thông tin cá nhân hóa về người dùng qua nhiều phiên trò chuyện. Điều này giúp nâng cao khả năng cá nhân hóa và cải thiện trải nghiệm người dùng.
---

## Danh Sách Kiểm Tra Nộp Bài

- [ ] `python grade.py` — xem điểm tự động, mục tiêu ≥ 75/100
- [ ] Cả 4 checkpoint pytest đều pass
- [ ] Tất cả 9 câu trong file này đã được trả lời
- [ ] Đã copy bài làm vào folder `solution/`, push lên fork và dán link trên trang bài Lab ở VLearn trước 23:59 ngày 11/09/2026
