# IDEA:
Agent chăm sóc sức khỏe và chế độ ăn của người cao tuổi
## Customer/ Segment Card

- **Segment name**         : Người cao tuổi mắc tiểu đường tuýp 2 đang tự điều trị tại nhà ở đô thị

- **Operational context**   : Bệnh nhân phải tự quản lý chế độ ăn nghiêm ngặt theo chỉ định của bác sĩ, thường xuyên phải đo chỉ số đường huyết và đối chiếu với thực đơn hàng ngày để tránh biến chứng.

- **Recurring workflow**    : Kiểm tra thực phẩm trước khi mua/ăn -> Ước lượng hàm lượng tinh bột/đường -> Ăn uống -> Đo đường huyết sau ăn (2h) -> Ghi chép sổ tay -> Đối chiếu chỉ số với ngưỡng an toàn.

- **Pain moment**          : Sự lúng túng và lo âu khi đứng trước một món ăn mới/lạ mà không biết có gây tăng vọt đường huyết hay không, và sự mệt mỏi khi phải ghi chép thủ công các con số khô khan mỗi ngày.

- **Why now**              : Công nghệ Vision AI hiện nay đã đủ mạnh để nhận diện thực phẩm qua hình ảnh và tính toán chỉ số dinh dưỡng tức thời, giúp thay thế việc tra cứu thủ công vốn quá khó khăn với người già.

- **Access path**           : Hợp tác với các hiệu thuốc bán máy đo đường huyết, tham gia vào các nhóm Zalo/Facebook cộng đồng "Sống khỏe cùng tiểu đường", hoặc thông qua con cái của họ trên các mạng xã hội.
---

## Need Map

### Need #1 (Priority: Hỗ trợ ra quyết định ăn uống tức thời)
- **Statement (JTBD):** **When** tôi chuẩn bị ăn một món ăn không tự nấu (đi tiệc, đi ăn ngoài), **I want** biết ngay lập tức món này có an toàn cho mức đường huyết hiện tại không, **so I can** tự tin ăn uống mà không lo sợ bị tăng đường huyết đột ngột gây choáng váng hoặc phải nhập viện.
- **Current workaround:** Tra cứu Google thủ công (thông tin thường quá chung chung), gọi điện hỏi con cái, hoặc "ăn liều" một ít rồi chờ đo máy sau 2 tiếng.
- **Pain signal:** **Stress vận hành và rủi ro sức khỏe.** Người già luôn sống trong sự lo âu mỗi bữa ăn, dẫn đến việc ăn uống không ngon miệng hoặc kiêng khem quá mức gây suy nhược.
- **Evidence / proxy evidence:** Tỉ lệ bệnh nhân tiểu đường nhập viện do biến chứng tăng/hạ đường huyết đột ngột; các câu hỏi lặp đi lặp lại trong các hội nhóm "Tôi bị tiểu đường có ăn được món X không?".
- **Why underserved:** Các app dinh dưỡng hiện nay quá phức tạp (bắt nhập khối lượng gram, calo), không hỗ trợ nhận diện món ăn Việt Nam qua hình ảnh một cách đơn giản cho người cao tuổi.

---

### Need #2 (Giảm tải áp lực cho người thân chăm sóc)
- **Statement (JTBD):** **When** tôi đang ở nơi làm việc và không ở cạnh bố mẹ, **I want** nhận được báo cáo tự động về việc bố mẹ đã ăn gì và chỉ số có ổn định không, **so I can** yên tâm làm việc mà không phải gọi điện kiểm tra/nhắc nhở liên tục gây áp lực cho cả hai bên.
- **Current workaround:** Gọi điện video mỗi bữa ăn để kiểm tra mâm cơm, thuê người giúp việc (tốn kém nhưng họ thường không có kiến thức y khoa), hoặc cuối tuần mới về kiểm tra sổ ghi chép một lần.
- **Pain signal:** **Mất thời gian và stress tâm lý.** Người con bị xao nhãng công việc vì lo lắng; mối quan hệ gia đình căng thẳng do việc nhắc nhở ăn uống giống như "kiểm soát".
- **Evidence / proxy evidence:** Chi phí thuê điều dưỡng/người giúp việc chuyên biệt cho người bệnh rất cao; khảo sát về "áp lực chăm sóc" ở các gia đình thành thị có người già mắc bệnh nền.
- **Why underserved:** Thị trường chỉ có máy đo chỉ số hoặc camera giám sát rời rạc, chưa có giải pháp nào kết nối dữ liệu ăn uống thực tế với chỉ số sức khỏe để gửi cảnh báo thông minh cho người thân.

---

## Strategy Statement

- **For** người cao tuổi mắc tiểu đường tại đô thị và người thân bận rộn của họ.
- **who struggle with** nỗi lo âu về việc ăn sai thực đơn gây tăng đường huyết đột ngột và áp lực ghi chép chỉ số thủ công hàng ngày.
- **our product helps them** duy trì chỉ số đường huyết ổn định và tận hưởng bữa ăn ngon miệng mà không lo sợ biến chứng.
- **through** một Agent AI nhận diện món ăn qua hình ảnh và phản hồi tức thì về mức độ an toàn dựa trên bệnh lý cá nhân.
- **unlike** việc tự tra cứu Google chung chung hoặc sử dụng các ứng dụng đếm Calo phức tạp của phương Tây.
- **because we can leverage** thuật toán nhận diện sâu các món ăn đặc thù của Việt Nam kết hợp với dữ liệu y tế cá nhân hóa của người dùng.

---

## Moat Hypothesis

- **Our moat mechanism is:** **Domain-learning flywheel** kết hợp với **Data compounding**.

- **If we deploy 50 times in the same vertical, the following things get systematically better:**
1.  **Độ chính xác của Vision AI:** Khả năng nhận diện các món ăn Việt Nam phức tạp (ví dụ: các loại bún, phở, món ăn gia đình) trở nên cực kỳ chính xác nhờ dữ liệu hình ảnh thực tế từ người dùng.
2.  **Mô hình dự báo cá nhân hóa:** AI hiểu được phản ứng đường huyết của từng cá nhân với từng loại thực phẩm cụ thể để đưa ra lời khuyên ngày càng chuẩn.
3.  **Lòng tin của người dùng (Brand Moat):** Khi dữ liệu sức khỏe của họ đã nằm trong hệ thống và được chứng minh là giúp ổn định bệnh, chi phí chuyển đổi (switching cost) sang app khác sẽ rất cao.

**Why competitors cannot easily replicate this:**
Các mô hình AI lớn của thế giới (như GPT, Gemini) có thể giỏi tiếng Anh nhưng không hiểu sâu về văn hóa ẩm thực và cách chế biến món ăn Việt Nam ảnh hưởng thế nào đến đường huyết bệnh nhân nội địa như chúng ta làm.

---

## TAM–SAM–SOM estimation
---

### Facts 

* ~3.5 triệu người Việt mắc tiểu đường ([MDPI][1])
* Tỷ lệ tiểu đường ~3.4% – 6.1% dân số trưởng thành ([Trading Economics][2])
* Tỷ lệ cao hơn nhiều ở nhóm >45 tuổi (~11.4% trong nghiên cứu đô thị) ([PubMed][3])
* Xu hướng: tăng nhanh ở đô thị & người lớn tuổi ([SpringerLink][4])

---

### Assumptions (explicit)

Define TAM = **toàn bộ người tiểu đường type 2 có thể dùng giải pháp AI hỗ trợ ăn uống**

* Dân số VN ~100M
* Người trưởng thành (20–79): ~70% → ~70M
* Tỷ lệ tiểu đường: 3–6% → **~2.1M – 4.2M người**
* % type 2: ~90% → **~1.9M – 3.8M**
* % có smartphone (già + trung niên): 50–70%

 TAM user base:
**~1M – 2.5M người**

---

### Pricing assumption

* Freemium + subscription:

  * 50k – 150k VND / tháng (~$2–6)

 TAM revenue:

* Low: 1M × $2 × 12 = **$24M/year**
* High: 2.5M × $6 × 12 = **$180M/year**

 **TAM = $25M – $180M / year (Vietnam only)**

---

## SAM – Serviceable Available Market

### Narrow scope:

> “Người cao tuổi mắc tiểu đường type 2, sống ở đô thị, tự quản lý tại nhà”

---

### Assumptions

* % người tiểu đường là >60 tuổi: ~40–50%
* % sống ở đô thị: ~35–40%
* % đủ tech literacy / có con hỗ trợ: ~50%

 SAM user base:

= TAM × 0.45 × 0.4 × 0.5
≈ **9% TAM**

→ **~90K – 225K người**

---

### SAM revenue

* 90K × $2 × 12 = **~$2.1M**
* 225K × $6 × 12 = **~$16M**

 **SAM = ~$2M – $16M / year**

---

## SOM – Serviceable Obtainable Market (realistic 2–3 năm)

### Assumptions thực tế startup:

* Distribution khó (healthcare + elderly)
* Adoption chậm
* Phải build trust

 realistic capture:

* 1% – 5% SAM trong 2–3 năm

---

### SOM user

* 1% → ~900 – 2,200 users
* 5% → ~4,500 – 11,000 users

---

### SOM revenue

* Low: ~1K users × $3 × 12 ≈ **$36K/year**
* High: ~10K users × $5 × 12 ≈ **$600K/year**

 **SOM = ~$30K – $600K / year (early stage realistic)**
