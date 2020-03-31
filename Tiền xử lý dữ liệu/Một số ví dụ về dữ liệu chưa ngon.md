# Một số ví dụ về dữ liệu chưa ngon

## Mở đầu

Thiết kế ra một model ngon và đáp ứng được những nhiệm vụ Business giống như việc bạn nấu một món ăn vậy. Món ăn ngon cấu thành từ hai phần: Công thức nấu chuẩn chỉ + Nguyên liệu tươi ngon. Nguyên liệu của các thuật toán trí tuệ nhân tạo chính là Data. Phần này sẽ nêu một số ví dụ về Data chưa được ngon mà ta cần sàng lọc và xử lý.

## Ví dụ

### Số lượng dữ liệu chưa đủ

Giáo viên giao cho bạn một bài toán và bạn có dám chắc là chỉ cần học một bài toán đó là có thể làm được những bài tương tự ? Chưa chắc đúng không. Machine Learning cũng vậy, phải mất rất nhiều dữ liệu để máy có thể làm việc đúng. Ngay cả với vấn đề đơn giản bạn cũng phải cần hàng ngàn ví dụ, còn với vấn đề phức tạp như nhận dạng hình ảnh hoặc giọng nói bạn có thể cần đến hàng triệu ví dụ (trừ khi bạn có thể tái sử dụng một mô hình đã tồn tại trước đó).

<p align="center"><img src = "https://github.com/hieptran1812/AI-for-ITPTIT/blob/master/Ti%E1%BB%81n%20x%E1%BB%AD%20l%C3%BD%20d%E1%BB%AF%20li%E1%BB%87u/images/du%20lieu%20chua%20du.PNG"></p>

rong một bài báo nổi tiếng xuất bản năm 2001, các nhà nghiên cứu của Microsoft Michele Banko và Eric Brill đã chỉ ra rằng các thuật toán Machine Learning rất khác nhau, bao gồm các thuật toán khá đơn giản, đã thực hiện gần như hoàn toàn chính xác đối với một vấn đề phức tạp về xử lý ngôn ngữ tự nhiên một khi chúng được cung cấp đủ dữ liệu (như bạn có thể thấy trên hình). Rõ ràng chúng ta không nên chỉ tập trung công sức và tiền bạc cho phát triển thuật toán đúng không.

### Dữ liệu không có tính đại diện

Dữ liệu của bạn không mang tính đại diện hay nói một cách khác là không mang tính tổng quát khi dữ liệu của bạn không bao hết toàn bộ trường hợp có thể có của dữ liệu. Ví dụ:

<p align="center"><img src = "https://github.com/hieptran1812/AI-for-ITPTIT/blob/master/Ti%E1%BB%81n%20x%E1%BB%AD%20l%C3%BD%20d%E1%BB%AF%20li%E1%BB%87u/images/nonrepresent.PNG"></p>

Ở biểu đồ trên, ta sử dụng Linear regression (Hồi quy tuyến tính) để dự đoán chỉ số hạnh phúc của người dân dựa trên chỉ số GDP đầu người trong mỗi quốc gia. Đường nét đứt là biểu thị cho model cũ và nét liền là model mới. Như bạn có thể thấy, không chỉ việc thêm một vài quốc gia bị thiếu làm thay đổi đáng kể mô hình, mà còn cho thấy rõ rằng một mô hình tuyến tính đơn giản như vậy có lẽ sẽ không bao giờ hoạt động tốt. Có vẻ như các nước rất giàu không hạnh phúc hơn các nước giàu vừa phải (thực tế họ có vẻ không hạnh phúc hơn), và ngược lại, một số nước nghèo có vẻ hạnh phúc hơn nhiều nước giàu. Do vậy, với một tập dữ liệu đào tạo không có tính đại diện, ta không thể đào tạo một mô hình có khả năng dự đoán chính xác. Đặc biệt là đối với các nước rất giàu hoặc rất nghèo. 

### Dữ liệu kém chất lượng

Rõ ràng, nếu dữ liệu đào tạo của bạn chứa đầy lỗi (error), ngoại lệ (outlier) và nhiễu (noise) (ví dụ: do các phép đo kém), hệ thống sẽ khó phát hiện các mẫu cơ bản hơn, do đó mô hình của bạn sẽ đưa ra dự đoán kém chính xác hơn. Do vậy rất cần thiết để làm sạch dữ liệu. Sự thật là, hầu hết các nhà khoa học dữ liệu dành một phần đáng kể thời gian của họ để làm việc đó. Ví dụ:
* Nếu một số trường hợp rõ ràng là ngoại lệ (outlier), có thể chỉ cần loại bỏ chúng hoặc cố gắng sửa lỗi bằng tay.
* Nếu một số trường hợp thiếu một vài tính năng (ví dụ: 5% khách hàng của bạn đã không khai báo tuổi của họ), bạn phải quyết định xem bạn có muốn bỏ qua thuộc tính này hoàn toàn không, bỏ qua các trường hợp này, điền vào các giá trị còn thiếu (ví dụ: với tuổi trung bình) hoặc đào tạo một mô hình với tính năng (tuổi) và một mô hình không có nó,... vân vân.

### Chọn các tính năng (feature) không liên quan

Hệ thống của bạn sẽ chỉ có khả năng học nếu dữ liệu đào tạo chứa đủ các feature có liên quan và không có quá nhiều feature không liên quan. Quá trình này, được gọi là _feature engineering_, bao gồm:
* Lựa chọn feature: chọn các tính năng hữu ích nhất để đào tạo trong số các tính năng hiện có.
* Trích xuất feature: kết hợp các feature hiện có để tạo ra một feature hữu ích hơn (như chúng ta đã thấy trước đó, các thuật toán giảm chiều có thể giúp ích).
* Tạo các feature mới bằng cách thu thập dữ liệu mới.

Ví dụ để dự đoán giá của một chiếc xe hơi thì bạn có thể bỏ qua tên của chiếc xe vì nó không liên quan gì nhiều đến giá của xe hơi đó cả.
