
# V.2
## MVP Boundary Scope
- **In-scope**:
  - Giao diện **đơn giản để người cao tuổi ghi lại bữa ăn và chỉ số đường huyết hằng ngày** (ưu tiên chọn nhanh thay vì chat tự do).
  - Lưu trữ lịch sử dữ liệu để **caregiver có thể xem lại (view-only)**.
  - Nhắc nhở (notification đơn giản) để duy trì thói quen nhập dữ liệu.
- **Out-of-scope**:
  - Caregiver phản hồi trực tiếp trong app.
  - Chatbot tư vấn tâm lý/phản hồi nâng cao .
  - Nhận diện món ăn bằng hình ảnh và dự đoán phản ứng đường huyết cá nhân hóa.
  - Phân tích xu hướng dựa trên dữ liệu lịch sử, cảnh báo thông minh, khuyến nghị hành động phức tạp.
- **None-goals**:
  - Không phải app dinh dưỡng tổng quát.
  - Không thay thế bác sĩ hoặc đưa ra quyết định điều trị.
  - Không phải thiết bị đo đường huyết.
---
## PRD Skeleton
- **Problem**: Người con 35–50 tuổi làm việc tại đô thị phải gọi điện 2–3 lần/ngày để hỏi tình trạng ăn uống và chỉ số của bố mẹ, gây gián đoạn công việc và không bền vững.
- **Target User**:
  - Primary: Người cao tuổi (bệnh nền như tiểu đường) cần ghi lại thông tin hằng ngày.
  - Secondary: Con cái (caregiver) cần theo dõi từ xa.
- **User Story #1**: Khi tôi không ở cạnh bố mẹ, tôi muốn xem nhanh dữ liệu ăn uống và chỉ số đã được ghi lại mỗi ngày, để giảm nhu cầu phải gọi điện kiểm tra liên tục.
- **User Story #2**: Tôi muốn một công cụ cực kỳ đơn giản (ít thao tác, ít chữ), để bố mẹ tôi có thể ghi lại thông tin mà không cần học nhiều hoặc cảm thấy áp lực.
---
### AI-Specific:

- **Model Selection**:
    - **Phase 1 (Data Collection / MVP)**: Không phụ thuộc vào AI phức tạp. Ưu tiên structured input (preset món ăn, input đơn giản).
    - **Phase 2**:
        - CNN nhận diện món ăn Việt Nam từ ảnh (có confidence threshold rõ ràng).
        - Mô hình dự đoán phản ứng đường huyết cá nhân hóa (chỉ kích hoạt khi đủ dữ liệu lịch sử).
    - Không đưa ra kết luận causal (“món X làm tăng đường huyết”) nếu không có đủ bằng chứng và luôn hiển thị mức độ chắc chắn (confidence / uncertainty).
- **Data Source**:
  - Dữ liệu lịch sử ăn uống + đường huyết (user input).
  - Dữ liệu hình ảnh (chỉ dùng khi đã đủ volume và chất lượng).
  - Có cơ chế lọc dữ liệu bẩn (ảnh mờ, input không rõ ràng).
- **Fallback UX**:
  - Khi model không chắc chắn → không đoán → yêu cầu chọn lại từ danh sách (structured).
  - Khi thiếu dữ liệu → hiển thị “chưa đủ dữ liệu để đưa ra nhận định”.
  - Cold start (7 ngày đầu):
   - Không có insight cá nhân hóa, chỉ hiển thị dữ liệu thô.
   - Không lặp lại nhiều lần yêu cầu sửa lỗi (tránh làm user khó chịu).
---
## Hypothesis & PMF scorecard
- **Riskiest assumption:**
  Người cao tuổi có thể duy trì việc ghi dữ liệu hằng ngày nếu giao diện đủ đơn giản và không gây áp lực.
- **Hypothesis:**
  Nếu người cao tuổi có thể ghi dữ liệu dễ dàng và đều đặn, caregiver sẽ giảm tần suất gọi điện kiểm tra và tiếp tục sử dụng sản phẩm lâu dài.
- **Aha moment:**
  Khi caregiver nhận ra rằng họ **không cần gọi điện mỗi ngày nhưng vẫn nắm được tình trạng**, họ sẽ bắt đầu tin tưởng và phụ thuộc vào công cụ.
- **PMF signal:**
  - % người dùng cao tuổi ghi ít nhất 1 lần/ngày trong 5 ngày đầu ≥ 40%
  - % caregiver xem dữ liệu ít nhất 1 lần/ngày trong 5 ngày đầu ≥ 30%
  - % giảm số cuộc gọi kiểm tra/ngày (self-reported) ≥ 30% sau 7 ngày
  - Retention Day 7 ≥ 25%