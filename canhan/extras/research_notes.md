# Research Notes — AI Transaction Classification

## Cách thức hoạt động của Moni AI (Giả định)
Moni AI có khả năng sử dụng các mô hình phân loại (Classification) dựa trên:
- **Merchant Category Code (MCC):** Mã ngành nghề của đơn vị chấp nhận thẻ/thanh toán.
- **Keywords:** Phân tích chuỗi ký tự trong nội dung giao dịch hoặc tên cửa hàng.
- **User History:** Dựa trên các thói quen tag thủ công trước đó của người dùng.

## Thách thức kỹ thuật
Sự không chắc chắn (Uncertainty) phát sinh khi:
1. **Dữ liệu nhiễu:** Các cửa hàng tạp hóa nhỏ dùng chung QR của cá nhân, không có MCC rõ ràng.
2. **Giao dịch đa mục đích:** Một lần chi tiêu tại Shopee có thể là "Sách", "Quần áo" hoặc "Đồ gia dụng".

## Framework cải tiến (4 Paths Applied)
Để tăng độ tin tưởng, hệ thống nên áp dụng:
- **Confidence Threshold:** Chỉ tự động tag khi confidence > 90%.
- **Active Learning:** Khi user sửa category, trigger một tiến trình fine-tuning nhẹ cho profile của user đó hoặc cập nhật trọng số cho keyword liên quan.
