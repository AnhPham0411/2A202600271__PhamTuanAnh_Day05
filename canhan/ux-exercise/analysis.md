# UX Exercise — MoMo Moni AI Assistant

## Sản phẩm: MoMo — Trợ thủ tài chính Moni AI

## 4 paths phân tích

### 1. Khi AI Đúng (Path 1)
- **Kịch bản:** User thực hiện một giao dịch mua đồ ăn tại cửa hàng tiện lợi. Moni AI tự động nhận diện và gán tag "Ăn uống".
- **Trải nghiệm:** Hệ thống hiện icon category ngay tại màn hình lịch sử giao dịch. User không cần thao tác gì thêm, cảm thấy sự tiện lợi của tự động hóa.
- **UI:** Nhãn dán category rõ ràng, màu sắc dễ nhận diện.

### 2. Khi AI Không Chắc (Path 2)
- **Kịch bản:** User chuyển tiền cho một số điện thoại lạ nhưng không ghi nội dung rõ ràng.
- **Trải nghiệm:** Moni AI thường bỏ trống phân loại hoặc để vào mục "Khác". 
- **Xử lý:** Hệ thống không chủ động hỏi user "Giao dịch này thuộc loại nào?". User phải tự vào chi tiết giao dịch để chỉnh sửa nếu muốn báo cáo chi tiêu chính xác.
- **Vấn đề:** Thiếu sự gợi ý chủ động khi độ tin tưởng (confidence level) thấp.

### 3. Khi AI Sai (Path 3)
- **Kịch bản:** User thanh toán phí bảo hiểm nhưng Moni AI lại tag vào "Mua sắm" (do nhầm lẫn tên đối tác).
- **Trải nghiệm:** User phát hiện ra khi xem biểu đồ tổng quan cuối tuần/tháng.
- **Cách sửa:** User phải nhấn vào giao dịch -> Chọn "Sửa phân loại" -> Tìm kiếm category đúng trong danh mục dài. Quá trình này mất khoảng 3-4 bước chạm.
- **Thiếu sót:** Chưa có cơ chế "Quick fix" ngay từ thông báo hoặc màn hình danh sách chính.

### 4. Khi User Mất Niềm Tin (Path 4)
- **Kịch bản:** Sau 3-4 lần liên tiếp AI tag sai các khoản chi lớn, user không còn tin vào báo cáo "Thông kê chi tiêu" tự động nữa.
- **Hệ quả:** User quay lại thói quen kiểm tra thủ công từng dòng hoặc ngừng sử dụng tính năng Moni.
- **Exit path:** Hiện tại MoMo cho phép tắt tính năng Moni nhưng nút ẩn sâu trong cài đặt. Không có tùy chọn "Reset AI" hoặc "Chế độ tag thủ công 100%".

---

## Đánh giá Path yếu nhất
**Path 3 & Path 4 là yếu nhất.**
Sản phẩm chưa tập trung vào việc **Learning từ lỗi sai**. Khi user sửa lỗi, hệ thống không xác nhận rõ ràng là "Tôi đã học được từ lỗi này, lần sau sẽ đúng hơn". Điều này khiến user cảm thấy việc sửa lỗi là vô ích và tốn công sức.

## Gap giữa Marketing và Thực tế
- **Marketing:** Hứa hẹn "Quản lý tài chính thông minh", "Tự động hoàn toàn".
- **Thực tế:** "Thông minh" chỉ ở mức 70-80% cho các giao dịch phổ thông. Đối với các giao dịch phức tạp, hệ thống vẫn "ngây ngô", tạo ra khoảng cách lớn giữa kỳ vọng (100% đúng) và thực tế (phải kiểm tra lại).

---

## Đề xuất Sketch
*Lưu ý: Bạn cần vẽ tay nội dung này vào giấy theo hướng dẫn dưới đây:*

- **As-is (Hiện tại):** Giao dịch -> AI tag tự động (có thể sai) -> User phát hiện -> Vào sâu 3 lớp menu để sửa -> Không biết AI có học không.
- **To-be (Đề xuất):** Giao dịch -> AI tag -> Nếu độ tin tưởng thấp, hiện nhãn **"Hỏi Moni?"** mờ mờ -> User chạm nhẹ để xác nhận/đổi nhanh -> Moni hiện thông báo nhỏ: **"Đã ghi nhớ cho lần sau!"**.
