# Day 16 Submission

## Members
- Trần Vọng Triển - 2A202600320
---

## 1. Idea reframed

Original idea:
> Agent chăm sóc sức khỏe và chế độ ăn cho người cao tuổi mắc bệnh tiểu đường.

Reframed as a product opportunity:
> Người cao tuổi mắc tiểu đường phải tự đưa ra quyết định ăn uống mỗi ngày trong trạng thái thiếu thông tin và lo âu, trong khi người thân của họ không có cách theo dõi để hỗ trợ từ xa. Điều này dẫn đến rủi ro sức khỏe tích tụ và stress kéo dài cho cả hai phía. Tôi tin rằng nếu có một lớp *decision support* đơn giản theo thời gian thực và một lớp *monitoring + alert* cho caregiver, thì việc quản lý bệnh tại nhà có thể chuyển từ reactive sang proactive.

---

## 2. Customer / Segment Card

- **Segment name:** Caregiver (25–50 tuổi) có bố mẹ/ ông bà mắc tiểu đường tuýp, có điều kiện kinh tế trung bình khá và có thói quen sử dụng smartphone để liên lạc và tìm kiếm thông tin.
- **Operational context:** Người con bận rộn công việc, không sống cùng hoặc không thể theo dõi bố mẹ liên tục, nhưng vẫn chịu trách nhiệm chính trong việc đảm bảo sức khỏe cho họ.
- **Recurring workflow:** Gọi điện hỏi bố mẹ ăn gì → nhắc nhở kiêng khem → cuối tuần về kiểm tra tình trạng → đưa đi khám định kỳ → lặp lại
- **Pain moment:** Không biết bố mẹ ăn gì mỗi ngày và chỉ phát hiện vấn đề khi đã có triệu chứng (mệt, choáng, nhập viện)
- **Why now:** Công nghệ AI đã đủ mạnh để nhận diện món ăn qua hình ảnh và dự đoán phản ứng đường huyết cá nhân hóa, trong khi người tiêu dùng đã quen với việc sử dụng smartphone cho các nhu cầu hàng ngày.
- **Access path:** Qua các nhóm cộng đồng online về chăm sóc người già, hợp tác với các hiệu thuốc bán máy đo đường huyết, hoặc thông qua con cái của họ trên các mạng xã hội.

One-sentence description:
> Người con 35–50 tuổi làm việc tại đô thị, mỗi ngày vẫn phải gọi điện 2–3 lần để hỏi “hôm nay bố/mẹ ăn gì” vì không yên tâm về tình trạng sức khỏe của họ.

---

## 3. Need Map 

### Need #1 (Priority: Hỗ trợ ra quyết định ăn uống tức thời)
- **Statement (JTBD):** Khi tôi chuẩn bị ăn một món ăn không tự nấu (đi tiệc, đi ăn ngoài), tôi muốn biết ngay lập tức món này có an toàn cho mức đường huyết hiện tại không, để có thể tự tin ăn uống mà không lo sợ bị tăng đường huyết đột ngột gây choáng váng hoặc phải nhập viện.
- **Current workaround:** Tra cứu Google thủ công (thông tin thường quá chung chung), gọi điện hỏi con cái, hoặc "ăn liều" một ít rồi chờ đo máy sau 2 tiếng.
- **Pain signal:** **Stress vận hành và rủi ro sức khỏe.** Người già luôn sống trong sự lo âu mỗi bữa ăn, dẫn đến việc ăn uống không ngon miệng hoặc kiêng khem quá mức gây suy nhược.
- **Evidence / proxy evidence:** Tỉ lệ bệnh nhân tiểu đường nhập viện do biến chứng tăng/hạ đường huyết đột ngột; các câu hỏi lặp đi lặp lại trong các hội nhóm "Tôi bị tiểu đường có ăn được món X không?".
- **Why underserved:** Các app dinh dưỡng hiện nay quá phức tạp (bắt nhập khối lượng gram, calo), không hỗ trợ nhận diện món ăn Việt Nam qua hình ảnh một cách đơn giản cho người cao tuổi.

---

### Need #2 (Giảm tải áp lực cho người thân chăm sóc)
- **Statement (JTBD):** Khi tôi đang ở nơi làm việc và không ở cạnh bố mẹ, tôi muốn nhận được báo cáo tự động về việc bố mẹ đã ăn gì và chỉ số có ổn định không, để có thể yên tâm làm việc mà không phải gọi điện kiểm tra/nhắc nhở liên tục gây áp lực cho cả hai bên.
- **Current workaround:** Gọi điện video mỗi bữa ăn để kiểm tra mâm cơm, thuê người giúp việc (tốn kém nhưng họ thường không có kiến thức y khoa), hoặc cuối tuần mới về kiểm tra sổ ghi chép một lần.
- **Pain signal:** Mất thời gian và stress tâm lý. Người con bị xao nhãng công việc vì lo lắng; mối quan hệ gia đình căng thẳng do việc nhắc nhở ăn uống giống như "kiểm soát".
- **Evidence / proxy evidence:** Chi phí thuê điều dưỡng/người giúp việc chuyên biệt cho người bệnh rất cao; khảo sát về "áp lực chăm sóc" ở các gia đình thành thị có người già mắc bệnh nền.
- **Why underserved:** Thị trường chỉ có máy đo chỉ số hoặc camera giám sát rời rạc, chưa có giải pháp nào kết nối dữ liệu ăn uống thực tế với chỉ số sức khỏe để gửi cảnh báo thông minh cho người thân.

### Need #3 (Priority: Phát hiện rủi ro tích tụ & kích hoạt hành động)

* **Statement (JTBD):** Khi hành vi ăn uống và chỉ số đường huyết của bố mẹ bắt đầu có xu hướng xấu đi theo thời gian, tôi muốn được cảnh báo sớm kèm mức độ nghiêm trọng và gợi ý hành động cụ thể, để có thể can thiệp kịp thời trước khi xảy ra biến chứng nguy hiểm.
* **Current workaround:** Chỉ phát hiện khi có triệu chứng rõ ràng (mệt, choáng), hoặc đợi đến lần khám định kỳ để bác sĩ phát hiện vấn đề.
* **Pain signal:** **Rủi ro “silent failure”.** Mọi thứ có thể xấu dần mà không ai nhận ra cho đến khi quá muộn.
* **Evidence / proxy evidence:** Biến chứng tiểu đường thường đến từ việc kiểm soát kém kéo dài (không phải một bữa ăn sai duy nhất).
* **Why underserved:** Không có hệ thống nào:

  * Tổng hợp **dữ liệu theo thời gian (trend)**
  * Và chuyển nó thành **cảnh báo dễ hiểu + hành động cụ thể cho người không chuyên**

---
## 4. Strategy Statement

- **For** người cao tuổi mắc tiểu đường và người thân bận rộn của họ.
- **who struggle with** nỗi lo âu về việc ăn sai thực đơn gây tăng đường huyết đột ngột và áp lực ghi chép chỉ số thủ công hàng ngày.
- **our product helps them** duy trì chỉ số đường huyết ổn định và tận hưởng bữa ăn ngon miệng mà không lo sợ biến chứng.
- **through** một Agent AI nhận diện món ăn qua hình ảnh và phản hồi tức thì về mức độ an toàn dựa trên bệnh lý cá nhân.
- **unlike** việc tự tra cứu Google chung chung hoặc sử dụng các ứng dụng đếm Calo phức tạp của phương Tây.
- **because we can leverage** thuật toán nhận diện sâu các món ăn đặc thù của Việt Nam kết hợp với dữ liệu y tế cá nhân hóa của người dùng.
---
## 5. Moat Hypothesis

**Moat mechanism:** Vòng lặp dữ liệu chăm sóc (care loop data flywheel) kết hợp với khóa chặt cá nhân hóa (personalization lock-in)

Nếu triển khai 50 lần, các yếu tố sau sẽ được cải thiện dần theo thời gian:
1. Độ chính xác trong việc nhận diện món ăn thực tế (ảnh chụp đời thường, mâm cơm gia đình, quán ăn)
2. Khả năng hiểu và dự đoán phản ứng đường huyết của từng cá nhân với từng loại thực phẩm
3. Mức độ phụ thuộc của người con (caregiver) vào dashboard và lịch sử dữ liệu để theo dõi và ra quyết định

**Why competitors cannot easily replicate this:**
> Dữ liệu cần thiết là dữ liệu theo thời gian (longitudinal) và gắn với ngữ cảnh cụ thể (context-specific), bao gồm món ăn Việt Nam, hành vi ăn uống hàng ngày và phản ứng đường huyết của từng cá nhân. Loại dữ liệu này chỉ có thể thu thập khi người dùng sử dụng sản phẩm liên tục trong workflow thực tế, và không tồn tại sẵn trên internet hoặc các dataset chung.

---

## 6. Initial TAM / SAM / SOM view

| Layer | Estimate | Key assumptions | Confidence |
|---|---|---|---|
| TAM | $35M–$300M/năm | 1M–3.4M care units, $3–8/tháng | medium |
| SAM | $4M–$36M/năm | ~11% TAM (người cao tuổi đô thị + caregiver) | medium |
| SOM | $100K–$2M/năm | chiếm 3–8% SAM trong 2–3 năm | low |

**Top 3 unknowns cần nghiên cứu thêm:**
1. Tỷ lệ caregiver sẵn sàng trả $5–10/tháng và yếu tố kích hoạt hành vi trả tiền là gì
2. Ma sát trong quá trình sử dụng giữa người già và người con (ai là người cài đặt, ai là người dùng chính, ai là người thanh toán)
3. Mức độ chính xác tối thiểu cần đạt để tạo được niềm tin và tránh người dùng rời bỏ (churn)

**Judgment:**
- [x] Worth pursuing now
- [ ] Worth pursuing but not now (cần validate thêm [...])
- [ ] Not worth pursuing as currently framed

---

## 7. Positioning Note (2 sentences)

**What we are:**
> Một lớp hỗ trợ ra quyết định (decision) và theo dõi (monitoring) giúp người con kiểm soát rủi ro ăn uống của bố mẹ mắc tiểu đường từ xa.

**What we are not / not yet:**
> Không phải là ứng dụng thay thế bác sĩ điều trị và cũng không phải là hệ thống theo dõi sức khỏe toàn diện.

---

## 8. Self-assessment before Day 17

Trong 6 mắt xích, đang yếu nhất ở:
> Moat — cần kiểm chứng xem data flywheel này có thực sự hình thành nhanh và đủ mạnh để tạo lợi thế cạnh tranh không.

Open questions muốn khám phá thêm ở Day 17:
1. Feature nào là đủ cho MVP để tạo thói quen sử dụng (scan vs alert vs dashboard)
2. Kênh phân phối (distribution) nào hiệu quả nhất (pharmacy vs cộng đồng caregiver online?)
3. Mô hình giá nào phù hợp (subscription vs bundle với thiết bị đo đường huyết)