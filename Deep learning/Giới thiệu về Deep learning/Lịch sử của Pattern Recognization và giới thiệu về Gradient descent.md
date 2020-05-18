## Lịch sử của Pattern Recognization và Gradient descent

Tiêu chuẩn một mô hình theo Pattern Recognization là trích chọn đặc trưng (feature extractor) và phân loại đào tạo (trainable classifier). 
Input đi vào trình feature extractor, trích xuất các đặc điểm hữu ích có liên quan từ các đầu vào như phát hiện mắt khi mục tiêu là nhận diện khuôn mặt. Sau đó, vectơ của các feature được đưa đến bộ phân loại có thể huấn luyện để tính tổng trọng số và so sánh nó với ngưỡng. Ở đây, một trainable classifier có thể là một mạng lưới tri giác hoặc mạng thần kinh đơn lẻ. Vấn đề là feature extractor nên được thiết kế bằng tay. 
Điều đó có nghĩa là, Pattern Recognization/thị giác máy tính tập trung vào trình feature extractor xem xét cách thiết kế nó cho một vấn đề cụ thể, không dành nhiều cho trainable classifier.
