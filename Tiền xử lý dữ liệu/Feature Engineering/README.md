# Feature Engineering 

## Nhắc lại kiến thức các bước xử lý một bài toán học máy (machine learning pipeline)

Bất kì hệ thống thông minh nào về cơ bản đều bao gồm các bước bắt đầu từ việc nhập dữ liệu thô, sử dụng các kỹ thuật để sắp xếp, xử lý, thiết kế các đặc trưng (feature) và thuộc tính có ý nghĩa từ dữ liệu này. Sau đó, chúng ta thường sử dụng các kỹ thuật như mô hình thống kê hoặc các mô hình học máy để xây dựng các mô hình với mục đích giải quyết yêu cầu đặt ra. Một quy trình tiêu chuẩn điển hình dựa trên mô hình tiêu chuẩn công nghiệp CRISP-DM được mô tả như hình dưới đây.

<p align = "center"><img src = "https://images.viblo.asia/7e86ba93-2bf0-4bc4-bcdd-c5d9b7464e91.png"></p>

Hãy tưởng tượng các bước trên giống như quá trình nấu ăn vậy. Từ những nguyên liệu đã mua, thu hoạch -> sơ chế -> nấu -> ăn thử. Thì ở đây, bạn tưởng tượng nguyên liệu chính là dữ liệu, sơ chế là feature engineering, nấu là thực hiện các thuật toán, ăn thử là đánh giá chất lượng của output :D. Trong phần sơ chế mà không làm sạch thức ăn, không chọn được những nguyên liệu phù hợp, không băm thái phù hợp thì các đoạn sau coi như vứt hết :)) và đó ta thấy vai trò rất rất quan trọng của Feature engineering. Tóm lại, hiểu đơn giản Feature engineering là sơ chế dữ liệu ha :DD

## Sự cần thiết của Feature engineering

Feature engineering là một giai đoạn không thể thiếu trong quá trình phát triển bất kỳ một hệ thống thông minh nào. Mặc dù hiện nay chúng ta có rất nhiều các phương pháp mới như học sâu, siêu mô hình hỗ trợ học máy tự động (automated machine learning), tuy nhiên với mỗi vấn đề cụ thể cần giải quyết luôn có những đặc trưng quan trọng hơn, có giá trị hơn để quyết định hiệu suất hệ thống của bạn. Ví dụ, bạn có thông tin về tình trạng sức khỏe của hàng trăm người và có nhiệm vụ dự đoán xem người đó có nguy cơ bị ung thư ABC gì đó không. Rõ ràng ta cần loại bỏ thông tin tên của những người đó vì tên của họ chẳng liên quan gì đến việc người đó có nguy cơ bị ung thư hay không cả. Hãy xem những nhà khoa học dữ liệu nổi tiếng nói gì về Feature engineering.

“Coming up with features is difficult, time-consuming, requires expert knowledge. ‘Applied machine learning’ is basically feature engineering.” — Prof. Andrew Ng.

Các nhà khoa học dữ liệu dành 70% thời gian của họ cho giai đoạn feature engineering. Đây là một quá trình khó khăn đòi hỏi cả kiến thức chuyên ngành và tính toán toán học.

<p align = "center"><img src = "https://miro.medium.com/max/1400/0*-dn9U8gMVWjDahQV.jpg"></p>

“Feature engineering is the process of transforming raw data into features that better represent the underlying problem to the predictive models, resulting in improved model accuracy on unseen data.” — Dr. Jason Brownlee

“At the end of the day, some machine learning projects succeed and some fail. What makes the difference? Easily the most important factor is the features used.” — Prof. Pedro Domingos

Vậy mới thấy tầm quan trọng của Feature engineering trong việc cải thiện hiệu suất học máy và việc vọc vạch phần này tốn thời gian đến mức nào.

## Phương pháp Feature engineering

### Trích lọc feature
Không phải toàn bộ thông tin được cung cấp từ một biến dự báo hoàn toàn mang lại giá trị trong việc phân loại. Do đó chúng ta cần phải trích lọc những thông tin chính từ biến đó. Chẳng hạn như trong các mô hình chuỗi thời gian chúng ta thường sử dụng kĩ thuật phân rã thời gian để trích lọc ra các đặc trưng như Ngày thành Năm, Tháng, Quí,.... Các đặc trưng mới sẽ giúp phát hiện các đặc tính chu kì và mùa vụ, những đặc tính mà thường xuất hiện trong các chuỗi thời gian. Kĩ thuật trích lọc đặc trưng thông thường được áp dụng trên một số dạng biến như:
1. Trích lọc đặc trưng trong xử lý ảnh và xử lý ngôn ngữ tự nhiên: Các mạng nơ ron sẽ trích lọc ra những đặc trưng chính và học từ những đặc trưng này để thực hiện tác vụ phân loại.
2. Dữ liệu về vị trí địa lý: Từ vị trí địa lý có thể suy ra vùng miền, thành thị, nông thôn, mức thu nhập trung bình, các yếu tố về nhân khẩu,....
3. Dữ liệu thời gian: Phân rã thời gian thành các thành phần thời gian.

### Biến đổi feature 
Biến đổi dữ liệu gốc thành những dữ liệu phù hợp với mô hình nghiên cứu. Những biến này thường có tương quan cao hơn đối với biến mục tiêu và do đó giúp cải thiện độ chính xác của mô hình. Các phương pháp này bao gồm:
1. Chuẩn hóa và thay đổi phân phối của dữ liệu thông qua các kĩ thuật feature scaling như Minmax scaling, Mean normalization, Unit length scaling, Standardization (các kĩ thuật này mình sẽ đề cập sau).
2. Tạo biến tương tác: Trong thống kê các bạn hẳn còn nhớ kiểm định ramsey reset test về mô hình có bỏ sót biến quan trọng? Thông qua việc thêm vào mô hình các biến bậc cao và biến tương tác để tạo ra một mô hình mới và kiểm tra hệ số các biến mới có ý nghĩa thống kê hay không. Ý tưởng của tạo biến tương tác cũng gần như thế. Tức là chúng ta sẽ tạo ra những biến mới là các biến bậc cao và biến tương tác.
3. Xử lý dữ liệu missing: Có nhiều lý do khiến ta phải xử lý missing data. Một trong những lý do đó là dữ liệu missing cũng mang những thông tin giá trị, do đó nếu thay thế được các missing bằng những giá trị gần đúng sẽ mang lại nhiều thông tin hơn cho mô hình. Bên cạnh đó nhiều mô hình không làm việc được với dữ liệu missing dẫn tới lỗi training. Do đó ta cần giải quyết các biến missing. Đối với biến số, các phương pháp đơn giản nhất là thay thế bằng mean, median,.... Một số kĩ thuật cao cấp hơn sử dụng phân phối ngẫu nhiên để *lấp đầy* các giá trị missing dựa trên phân phối của các giá trị đã biết hoặc sử dụng phương pháp simulate missing value dựa trên trung bình của các quan sát láng giềng. Đối với dữ liệu category, missing value có thể được giữ nguyên như một class độc lập hoặc gom vào các nhóm khác có đặc tính phân phối trên biến mục tiêu gần giống.

### Lựa chọn feature
Phương pháp này được áp dụng trong những trường hợp có rất nhiều dữ liệu mà chúng ta cần lựa chọn ra dữ liệu có ảnh hưởng lớn nhất đến sức mạnh phân loại của mô hình. Các phương pháp có thể áp dụng đó là ranking các biến theo mức độ quan trọng bằng các mô hình như Random Forest, Linear Regression, Neural Network, SVD,...; Sử dụng chỉ số IV trong scorecard; Sử dụng các chỉ số khác như AIC hoặc Pearson Correlation, phương sai. Chúng ta có thể phân chia các phương pháp trên thành 3 nhóm:
1. Cách tiếp cận theo phương pháp thống kê: Sử dụng tương quan Pearson Correlation, AIC, phương sai, IV.
2. Lựa chọn đặc trưng bằng sử dụng mô hình: Random Forest, Linear Regression, Neural Network, SVD.
3. Lựa chọn thông qua lưới (grid search): Coi số lượng biến như một thông số của mô hình. Thử nghiệm các kịch bản với những số lượng biến khác nhau. Các bạn có thể xem cách thực hiện grid search.

Vì mỗi vấn đề và dữ liệu mà có các cách xử lý khác nhau. Hãy thử google các kĩ thuật trên, đừng ngại khó, sắp tới mình sẽ giải thích và sử dụng trong các bài toán cụ thể.

## Quá trình thực hiện Feature engineering

Quá trình Feature engineering gồm các bước cơ bản sau:

1. Liệt kê các features nhiều nhất có thể.
2. Quyết định xem nên lấy các features nào.
3. Tạo features từ attributes.
4. Kiểm tra các features này ảnh hưởng như nào đến model của bạn.
5. Cải thiện các features nếu cần thiết.
6. Quay lại bước 1 cho đến khi model đạt hiệu suất mong muốn.

