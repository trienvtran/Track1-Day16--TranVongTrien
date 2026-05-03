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

### Need #3 (Priority: Phát hiện rủi ro tích tụ & kích hoạt hành động)

* **Statement (JTBD):** **When** hành vi ăn uống và chỉ số đường huyết của bố mẹ bắt đầu có xu hướng xấu đi theo thời gian, **I want** được cảnh báo sớm kèm mức độ nghiêm trọng và gợi ý hành động cụ thể, **so I can** can thiệp kịp thời trước khi xảy ra biến chứng nguy hiểm.
* **Current workaround:** Chỉ phát hiện khi có triệu chứng rõ ràng (mệt, choáng), hoặc đợi đến lần khám định kỳ để bác sĩ phát hiện vấn đề.
* **Pain signal:** **Rủi ro “silent failure”.** Mọi thứ có thể xấu dần mà không ai nhận ra cho đến khi quá muộn.
* **Evidence / proxy evidence:** Biến chứng tiểu đường thường đến từ việc kiểm soát kém kéo dài (không phải một bữa ăn sai duy nhất).
* **Why underserved:** Không có hệ thống nào:

  * Tổng hợp **dữ liệu theo thời gian (trend)**
  * Và chuyển nó thành **cảnh báo dễ hiểu + hành động cụ thể cho người không chuyên**

---

## Strategy Statement

- **For** người cao tuổi mắc tiểu đường và người thân bận rộn của họ.
- **who struggle with** nỗi lo âu về việc ăn sai thực đơn gây tăng đường huyết đột ngột và áp lực ghi chép chỉ số thủ công hàng ngày.
- **our product helps them** duy trì chỉ số đường huyết ổn định và tận hưởng bữa ăn ngon miệng mà không lo sợ biến chứng.
- **through** một Agent AI nhận diện món ăn qua hình ảnh và phản hồi tức thì về mức độ an toàn dựa trên bệnh lý cá nhân.
- **unlike** việc tự tra cứu Google chung chung hoặc sử dụng các ứng dụng đếm Calo phức tạp của phương Tây.
- **because we can leverage** thuật toán nhận diện sâu các món ăn đặc thù của Việt Nam kết hợp với dữ liệu y tế cá nhân hóa của người dùng.

---

## Moat Hypothesis

* **Our moat mechanism is:** **Care loop data flywheel** kết hợp với **personalization lock-in**.

* **If we deploy 50 times in the same vertical, the following things get systematically better:**

1. **Độ chính xác của Vision AI:** Khả năng nhận diện món ăn Việt Nam ngoài đời thực (mâm cơm gia đình, quán ăn, tiệc) cải thiện mạnh nhờ dữ liệu hình ảnh thực tế từ user.
2. **Mô hình hiểu “response cá nhân”:** Hệ thống học được mối quan hệ giữa *món ăn → phản ứng đường huyết* của từng người → chuyển từ generic advice sang **predictive & personalized**.
3. **Caregiver dependency (switching cost):** Người con dần phụ thuộc vào dashboard/cảnh báo → mất dữ liệu lịch sử = mất khả năng theo dõi → khó chuyển sang sản phẩm khác.

**Why competitors cannot easily replicate this:**

* Dữ liệu cần là **multi-layer + dài hạn**:

  * Ảnh món ăn thực tế (không phải dataset internet)
  * Hành vi ăn uống hàng ngày
  * Chỉ số đường huyết theo thời gian
* Các model lớn (GPT, Gemini) có thể nhận diện tốt ảnh, nhưng **không có longitudinal health data + context Việt Nam** để build insight có ý nghĩa.
* Lợi thế không nằm ở model, mà nằm ở **data flywheel trong một vertical rất cụ thể (Vietnamese diabetic diet)**.

---
## TAM–SAM–SOM estimation

### TAM – Total Addressable Market

* ~3.5 triệu người Việt mắc tiểu đường 
* Tỷ lệ tiểu đường ~3.4% – 6.1% dân số trưởng thành 
* Tỷ lệ cao hơn nhiều ở nhóm >45 tuổi (~11.4% trong nghiên cứu đô thị) 
* Xu hướng: tăng nhanh ở đô thị & người lớn tuổi
* 90% là type 2 diabetes
---

- Assumptions:

  - Define TAM = **“care units” (bệnh nhân + người thân có thể dùng app)**

  * Tổng người mắc: **2.5M – 7M**
  * % type 2: ~90% → **2.2M – 6.3M**
  * % có caregiver (con cái hỗ trợ): ~60%
    → **1.3M – 3.8M care units**
  * % có smartphone (caregiver): ~80–90%

 >Effective TAM users: **~1M – 3.4M**

---

- Pricing assumption: Subscription: $3 – $8 / tháng (caregiver trả)

- TAM Revenue

  * Low: 1M × $3 × 12 = **$36M/year**
  * High: 3.4M × $8 × 12 = **$326M/year**

 > **TAM = ~$35M – $300M / year (Vietnam)**

---

### SAM – Serviceable Available Market

- Scope cụ thể:

> Người cao tuổi mắc tiểu đường type 2, sống ở đô thị, có caregiver

---

- Assumptions

  * % >60 tuổi: ~40–50%
  * % sống ở đô thị: ~35–40%
  * % có caregiver active: ~60%

>SAM ratio: ≈ 0.45 × 0.4 × 0.6 ≈ **11% TAM**

---

- SAM users

  * 1M – 3.4M × 11%
    → **~110K – 375K users**

---

- SAM revenue

  * Low: 110K × $3 × 12 = **~$4M**
  * High: 375K × $8 × 12 = **~$36M**

 >**SAM = ~$4M – $36M / year** -->

---

### SOM – Serviceable Obtainable Market (2–3 năm)

- Assumptions thực tế

* Go-to-market:

  * caregiver-first
  * pharmacy / clinic distribution
* Adoption trong healthcare thường chậm
* Trust cần thời gian build

 realistic capture:
**3% – 8% SAM**

---

-  SOM users

* Low: 110K × 3% ≈ **3.3K users**
* High: 375K × 8% ≈ **30K users**

---

- SOM revenue

* Low: 3K × $3 × 12 ≈ **$100K/year**
* High: 30K × $6 × 12 ≈ **$2.1M/year**

 **SOM = ~$100K – $2M / year (realistic early stage)**

---

### 4. Top 3 Unknowns cần research

1.  Willingness to pay (critical)

* % caregiver sẵn sàng trả $5–10/tháng?
* Trigger trả tiền là:

  * alert?
  * peace of mind?
  * hay doctor recommendation?

---

2.  Adoption friction (2-user system)

* Người già có chịu chụp ảnh mỗi bữa không?
* Onboarding:

  * ai setup app?
  * ai dạy ai?

---

3.  Trust threshold (make-or-break)

* Accuracy bao nhiêu % thì user tin?
* 1 lần sai → churn?

> Health product = **trust-sensitive market**
