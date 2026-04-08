# Cá nhân Reflection — Ngày 5: AI Product Design

## Suy ngẫm về sự không chắc chắn (Uncertainty)
Bài học hôm nay đã thay đổi tư duy của tôi về việc xây dựng sản phẩm AI. Trước đây, tôi thường nghĩ AI là một "hộp đen" chỉ cần độ chính xác cao là đủ. Tuy nhiên, sau khi tìm hiểu về framework **4 paths**, tôi nhận ra rằng:
- Thiết kế cho trường hợp **AI sai** (Path 3) quan trọng không kém gì thiết kế cho trường hợp đúng.
- Niềm tin của người dùng (Trust) được xây dựng dựa trên cách sản phẩm xử lý những lúc nó "không chắc chắn".

## Ứng dụng vào thực tế
Khi phân tích MoMo Moni AI, tôi thấy rằng việc thiếu một feedback loop rõ ràng (user sửa nhưng không biết AI có học không) là một điểm yếu phổ biến. Trong các dự án tới, tôi sẽ ưu tiên:
1. Luôn cung cấp cơ chế phản hồi (Feedback logic).
2. Thiết kế UI tinh tế để gợi ý khi AI có độ tự tin thấp, thay vì im lặng hoặc đoán bừa.

## Kết luận
Thiết kế sản phẩm AI không chỉ là làm cho model tốt hơn, mà là làm cho **trải nghiệm người dùng an toàn và đáng tin cậy hơn** ngay cả khi công nghệ có sai sót.
