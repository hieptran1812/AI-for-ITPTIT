# Feature Engineering 

## Nhắc lại kiến thức các bước xử lý một bài toán học máy (machine learning pipeline)

Bất kì hệ thống thông minh nào về cơ bản đều bao gồm các bước bắt đầu từ việc nhập dữ liệu thô, sử dụng các kỹ thuật để sắp xếp, xử lý, thiết kế các đặc trưng (feature) và thuộc tính có ý nghĩa từ dữ liệu này. Sau đó, chúng ta thường sử dụng các kỹ thuật như mô hình thống kê hoặc các mô hình học máy để xây dựng các mô hình với mục đích giải quyết yêu cầu đặt ra. Một quy trình tiêu chuẩn điển hình dựa trên mô hình tiêu chuẩn công nghiệp CRISP-DM được mô tả như hình dưới đây.

<p align = "center"><img src = "https://images.viblo.asia/7e86ba93-2bf0-4bc4-bcdd-c5d9b7464e91.png"></p>

Hãy tưởng tượng các bước trên giống như quá trình nấu ăn vậy. Từ những nguyên liệu đã mua, thu hoạch -> sơ chế -> nấu -> ăn thử. Thì ở đây, bạn tưởng tượng nguyên liệu chính là dữ liệu, sơ chế là feature engineering, nấu là thực hiện các thuật toán, ăn thử là đánh giá chất lượng của output :D. Trong phần sơ chế mà không làm sạch thức ăn, không chọn được những nguyên liệu phù hợp, không băm thái phù hợp thì các đoạn sau coi như vứt hết :)) và đó ta thấy vai trò rất rất quan trọng của Feature engineering. Tóm lại, hiểu đơn giản Feature engineering là sơ chế dữ liệu ha :DD

## Sự cần thiết của Feature engineering

Feature engineering là một giai đoạn không thể thiếu trong quá trình phát triển bất kỳ một hệ thống thông minh nào. Mặc dù hiện nay chúng ta có rất nhiều các phương pháp mới như học sâu, siêu mô hình hỗ trợ học máy tự động (automated machine learning), tuy nhiên với mỗi vấn đề cụ thể cần giải quyết luôn có những đặc trưng quan trọng hơn, có giá trị hơn để quyết định hiệu suất hệ thống của bạn. Ví dụ, bạn có thông tin về tình trạng sức khỏe của hàng trăm người và có nhiệm vụ dự đoán xem người đó có nguy cơ bị ung thư ABC gì đó không. Rõ ràng ta cần loại bỏ thông tin tên của những người đó vì tên của họ chẳng liên quan gì đến việc người đó có nguy cơ bị ung thư hay không cả. Hãy xem những nhà khoa học dữ liệu nổi tiếng nói gì về Feature engineering.

“Coming up with features is difficult, time-consuming, requires expert knowledge. ‘Applied machine learning’ is basically feature engineering.” — Prof. Andrew Ng.

Các nhà khoa học dữ liệu dành 70% thời gian của họ cho giai đoạn feature engineering. Đây là một quá trình khó khăn đòi hỏi cả kiến thức chuyên ngành và tính toán toán học.

“Feature engineering is the process of transforming raw data into features that better represent the underlying problem to the predictive models, resulting in improved model accuracy on unseen data.” — Dr. Jason Brownlee

“At the end of the day, some machine learning projects succeed and some fail. What makes the difference? Easily the most important factor is the features used.” — Prof. Pedro Domingos

Vậy mới thấy tầm quan trọng của Feature engineering trong việc cải thiện hiệu suất học máy và việc vọc vạch phần này tốn thời gian đến mức nào.


