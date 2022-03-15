# Tại sao lại là Containerize?

Sự cách ly được cung cấp bởi các container cho phép các giai đoạn học máy có thể di động và có thể tái tạo. Các ứng dụng được containerized được tách biệt khỏi phần còn lại của máy và bao gồm tất cả các requirements (từ hệ điều hành trở lên).

Các container được xây dựng trong các layer có thể ghép lại, cho phép bạn sử dụng một container khác làm cơ sở. 
Ví dụ: nếu bạn muốn sử dụng thư viện xử lý ngôn ngữ tự nhiên (NLP) mới, 
bạn có thể thêm nó vào đầu container hiện có — bạn không phải bắt đầu lại từ đầu mỗi lần. 
Khả năng kết hợp cho phép bạn tái sử dụng một cơ sở chung; 
Ví dụ: các container R và Python mà chúng tôi sử dụng đều dùng chung một container Debian cơ sở.

Một lo lắng phổ biến khi sử dụng container là chi phí cao. 
Tổng chi phí của các container phụ thuộc vào việc triển khai của bạn, 
nhưng một bài báo từ IBM cho thấy chi phí này khá thấp và nói chung là nhanh hơn so với ảo hóa. 
Với Kubeflow, có một số chi phí lớn là cài đặt thứ mà bạn có thể không sử dụng. 
Chi phí này là không đáng kể trên một cụm sản xuất nhưng có thể đáng chú ý trên máy tính xách tay.
