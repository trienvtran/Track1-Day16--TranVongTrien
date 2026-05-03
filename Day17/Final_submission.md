# Day 17 Submission

**Student:** Trần Vọng Triển

**Date:** 03/05/2026

**Product idea:** Hệ thống hỗ trợ ra quyết định và giám sát ăn uống từ xa giúp người con kiểm soát rủi ro đường huyết cho bố mẹ mắc tiểu đường.

---

## 1. MVP Boundary Sheet

**Riskiest Assumption:**
> Người cao tuổi có thể duy trì việc ghi dữ liệu hằng ngày nếu giao diện cực kỳ đơn giản (chụp ảnh thay vì nhập liệu).

**In-Scope** (tối đa 3):
- **Giao diện "One-Tap Photo" cho người cao tuổi**: Chụp ảnh bữa ăn để AI tự phân loại món.
- **Dashboard theo dõi thời gian thực cho Caregiver**: Xem lịch sử ăn uống và chỉ số đường huyết được đồng bộ ngay lập tức.
- **Hệ thống nhắc nhở thông minh (Smart Reminders)**: Tự động nhắc người cao tuổi nhập liệu dựa trên thói quen giờ ăn hằng ngày.

**Out-of-Scope:**
- Caregiver phản hồi trực tiếp/chat trong app (dùng Zalo/gọi điện để tối ưu giai đoạn đầu).
- Chatbot tư vấn tâm lý nâng cao (không phải giá trị cốt lõi lúc này).
- Phân tích xu hướng và dự đoán phản ứng đường huyết cá nhân hóa (để lại cho Phase 2 khi đủ dữ liệu).

**Non-Goals:**
- Không thay thế bác sĩ hoặc đưa ra quyết định điều trị y tế.
- Không phải là thiết bị đo đường huyết vật lý.

---

## 2. PRD Skeleton

### Problem Statement
> Người con 35–50 tuổi tại đô thị phải gọi điện kiểm tra bố mẹ 2–3 lần/ngày gây gián đoạn công việc và áp lực tâm lý cho cả hai phía.

### Target User
> Caregiver (25–50 tuổi) bận rộn và bố mẹ mắc tiểu đường tuýp 2 sống xa con cái hoặc cần giám sát hỗ trợ.

### User Stories
**Story 1:**
> Với tư cách là **Người chăm sóc (Caregiver)**, tôi muốn **xem nhật ký hình ảnh các bữa ăn của bố mẹ**, để **tôi có thể ngừng việc gọi điện hỏi "hôm nay bố mẹ ăn gì" mỗi ngày**.

**Story 2:**
> Với tư cách là **Người dùng cao tuổi**, tôi muốn **ghi lại bữa ăn của mình chỉ bằng cách chụp một bức ảnh**, để **tôi không phải vất vả với việc nhập liệu hay các thao tác điều hướng phức tạp trên ứng dụng**.

### AI-Specific

**Model Selection:**
- Model: **GPT-4o (Vision) hoặc Gemini 1.5 Flash**.
- Lý do chọn: Cần khả năng multimodal mạnh để nhận diện món ăn Việt Nam từ ảnh thực tế (low quality/low light).
- Trade-offs chấp nhận: Chi phí API cao hơn model CNN tự build nhưng rút ngắn thời gian launch MVP.
- Trade-offs không chấp nhận: Không chấp nhận việc model tự bịa ra thông tin y khoa nếu ảnh không rõ.

**Data Requirements:**
- Nguồn: User-uploaded images và chỉ số đường huyết nhập tay.
- Owner: Người dùng (Người cao tuổi/ Caregiver).
- Update frequency: Theo thời gian thực.

**Fallback UX:**
- Chiến lược: **Human-in-the-loop**.
- Trigger: Khi Confidence Score của model nhận diện ảnh < 80%.
- Hành động: Hiển thị 3 lựa chọn món ăn có Confidence Score cao nhất và cho người dùng xác nhận.
- User options: Người cao tuổi chọn từ gợi ý hoặc Caregiver có thể vào gắn tag (tagging) lại món ăn sau đó trên dashboard.

### Success Metrics
- Primary metric: **% Giảm số cuộc gọi kiểm tra hằng ngày (self-reported bởi Caregiver)**.
- Ngưỡng thành công: Giảm > 30% sau 7 ngày sử dụng.
- Timeframe đo lường: 2 tuần sau khi onboard.

### Dependencies & Constraints
- Độ ổn định của Internet tại nhà người cao tuổi.
- Tích hợp camera smartphone dễ dàng.

---

## 3. Hypothesis Table

### Hypothesis 1 (cho tính năng In-Scope #1)
> "Chúng tôi tin rằng **tính năng chụp ảnh món ăn** sẽ giúp **người cao tuổi** **duy trì thói quen ghi lại bữa ăn đều đặn**. Chúng tôi sẽ biết mình đúng khi thấy **tỷ lệ người dùng ghi dữ liệu ít nhất 1 lần/ngày đạt > 40% trong tuần đầu**".

Riskiest assumption: Người cao tuổi biết cách cầm điện thoại chụp ảnh đủ rõ nét để AI nhận diện.
Cách test cheapest: Làm một buổi workshop nhỏ (5-10 người cao tuổi) quan sát họ dùng camera chụp mâm cơm thật.

---

## 4. PMF Scorecard

**Aha Moment:**
> Lần đầu tiên Caregiver mở app vào lúc 12h30 trưa, thấy ảnh mâm cơm bố mẹ đã chụp và quyết định **không bấm nút gọi điện** nữa.

**Actionable Metric:**
> **DAU/MAU Ratio (Stickiness)** - Đo lường tần suất Caregiver quay lại kiểm tra app hằng ngày.

**PMF Method:**
> **Sean Ellis Test**.
> Ngưỡng thành công: > 40% "Very disappointed" nếu app không còn tồn tại.

**Vanity Metrics tôi sẽ không dùng:**
- Tổng số lượt tải app.
- Tổng số món ăn AI đã nhận diện thành công.

---

## 5. AI Critique Log

**Điểm AI chỉ ra:**
1. **Mâu thuẫn Scope** - Action: **Accept** - Đưa tính năng nhận diện ảnh vào In-Scope vì đây là cách duy nhất để người cao tuổi chịu dùng app (Simple UI).
2. **Fallback UX quá cứng nhắc** - Action: **Accept** - Chuyển từ "bắt người cao tuổi chọn lại" sang "Caregiver hỗ trợ sửa tag sau" (Human-in-the-loop) để giảm stress cho người cao tuổi.
3. **Metric đo PMF quá chung chung** - Action: **Accept** - Chuyển sang đo lường sự thay đổi hành vi (quyết định không gọi điện) của Caregiver.

**Thay đổi lớn nhất giữa Version A và Version B:**
> Chuyển trọng tâm từ việc AI phải "thông minh/dự đoán" sang việc AI phải "làm thay việc nhập liệu" để tạo thói quen sử dụng bền vững cho người cao tuổi.

---

## 6. Self-assessment

Mắt xích nào trong [MVP Boundary → PRD → Hypothesis → PMF] bạn đang yếu nhất?
> **Hypothesis & Measurement.** Tôi vẫn lo ngại về việc thiết kế cách đo lường "số cuộc gọi giảm đi" một cách chính xác mà không quá phụ thuộc vào self-report của user.

Open questions:
1. Làm sao để thiết kế onboarding cho người cao tuổi một cách "zero-friction" nhất?.
2. Nếu Caregiver không vào sửa tag ảnh sai, dữ liệu AI sẽ bị bẩn (garbage in), xử lý việc này thế nào về lâu dài?.