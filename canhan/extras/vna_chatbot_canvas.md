# AI Product Canvas: Vietnam Airlines Chatbot (NEO)

Tiếp nối phần phân tích MoMo, dưới đây là Canvas cho Chatbot NEO của Vietnam Airlines để đối chiếu sự khác biệt giữa hai lĩnh vực.

---

## 1. Cột VALUE (Giá trị mang lại)

- **User nào? Pain nào?**: Hành khách có nhu cầu tra cứu chuyến bay, check-in online hoặc hỏi về quy định hành lý nhưng ngại gọi tổng đài (thời gian chờ lâu) hoặc khó tìm thông tin trên website phức tạp.
- **Auto hay Aug?**: 
    - **Auto**: Tự động trả lời các câu hỏi thường gặp (FAQs), tra cứu tình trạng chuyến bay dựa trên mã đặt chỗ.
    - **Aug**: Chuyển đổi sang nhân viên hỗ trợ (Human agent) khi gặp các yêu cầu phức tạp hoặc khi AI không hiểu intent.
- **Value khi AI đúng?**: Giải quyết yêu cầu của khách hàng 24/7 tức thì, giảm tải cho trung tâm cuộc gọi, tăng trải nghiệm số cho hãng hàng không quốc gia.

## 2. Cột TRUST (Niềm tin & Quản trị rủi ro)

- **Precision hay Recall?**: Cần sự cân bằng, nhưng **Recall** (khả năng hiểu được nhiều cách hỏi khác nhau) cực kỳ quan trọng để khách hàng không cảm thấy chatbot "ngu". Tuy nhiên, thông tin về giờ bay/cổng ra máy bay phải đạt **Precision 100%**.
- **Khi sai → user biết/sửa thế nào?**: User biết ngay khi nhận được câu trả lời không liên quan. Chatbot cần có nút "Chưa đúng ý tôi" hoặc "Gặp nhân viên hỗ trợ" ngay trong khung chat.
- **Trust recovery**: Cần thông cảm và chuyển hướng nhanh: "Xin lỗi, tôi chưa hiểu ý bạn. Bạn muốn nói chuyện với nhân viên tư vấn không?".

## 3. Cột FEASIBILITY (Tính khả thi)

- **Cost / Latency**: 
    - **Latency**: Cần phản hồi dưới 1s để tạo cảm giác hội thoại tự nhiên.
    - **Cost**: Chi phí duy trì hệ thống NLP và kết nối API vào hệ thống quản lý bay (Sabre/Amadeus) vốn rất tốn kém và phức tạp.
- **Risk chính**: 
    - **Hallucination (Ảo giác)**: AI tự chế ra quy định hành lý hoặc giờ bay (rất nguy hiểm).
    - **Language**: Tiếng Việt chuyên ngành hàng không và tên địa danh dễ bị nhầm lẫn.

## 4. Learning Signal

- **User corrections**: Khi user chọn "Không hữu ích" hoặc thoát chat để gọi tổng đài, đó là tín hiệu AI đã thất bại. Các đoạn hội thoại này cần được gắn nhãn để tái huấn luyện model Intent.
- **Tình trạng**: Đang tốt lên nếu tỷ lệ **Hand-over** (chuyển sang người) giảm dần và tỷ lệ khách hàng hoàn thành **Check-in qua bot** tăng lên.

---

### SO SÁNH NHANH (Finance vs Aviation)

| Đặc điểm | MoMo (Tài chính) | VNA NEO (Hàng không) |
|----------|-----------------|---------------------|
| **Ưu tiên** | Precision (Chính xác tuyệt đối) | Recall (Hiểu đa dạng ý định) |
| **Rủi ro lớn** | Sai lệch con số tài chính | Cung cấp sai quy định bay |
| **Learning** | Dựa trên hành động sửa tag | Dựa trên đánh giá mức độ hài lòng cuối chat |
