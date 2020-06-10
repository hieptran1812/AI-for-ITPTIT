# Feature Selection

## Lợi ích của Feature Selection

Lợi ích chính của **Feature selection** là nó làm giảm Overfitting. Bằng cách xóa dữ liệu không liên quan, nó cho phép mô hình chỉ tập trung vào các feature quan trọng của dữ liệu và không phải học từ những dữ liệu không liên quan. Một lợi ích khác của việc loại bỏ thông tin không liên quan là nó **cải thiện độ chính xác** của các dự đoán mô hình. Nó cũng làm **giảm thời gian tính toán** liên quan để có được mô hình. Cuối cùng, có số lượng tính năng nhỏ hơn làm cho **mô hình của bạn tường mình và dễ hiểu hơn**. Nhìn chung, lựa chọn tính năng là chìa khóa để có thể dự đoán các giá trị với bất kỳ mức độ chính xác nào.

<p align = "center"><img src = "https://miro.medium.com/max/2000/1*tcS-bJJ1B4IOHD60158SDw.png"></p>

Tóm lại, có thể hiểu lợi ích của Feature selection qua ví dụ sau: Bạn có tập ngân hàng đề cho ba môn Toán, Anh, Văn. Sắp tới bạn thi cuối kì môn Toán và tất nhiên là bạn muốn điểm số cao nhất có thể :D Việc giải bài như nào để được điểm cao (giống như phần thuật toán của Machine Learning) ta sẽ tìm hiểu sau. Vấn đề là trong đống ngân hàng đề (Data) kia, ta chọn ra môn và bài tập phù hợp. Sắp tới thi toán mà ôn cả văn và anh (dữ liệu không liên quan) chắc chắn lủng rồi :)) Ta sẽ chọn ngân hàng đề toán để ôn thôi vì sao ?

* Cải thiện điểm số (giống như cải thiện độ chính xác mô hình) làm bài thi toán không bị phân tâm sang các môn văn, anh.
* Đỡ mất thời gian học các môn khác (giống như giảm thời gian tính toán).

<p align = "center"><img src = "https://miro.medium.com/max/2000/1*hoeZ8_6QaN3rc0TN1yAdwA.png"></p>

## Tổng quan

Có ba loại Feature Selection (mình xin phép không dịch sang tiếng Việt vì không sát nghĩa): Wrapper methods (forward, backward, and stepwise selection), Filter methods (ANOVA, Pearson correlation, variance thresholding), và Embedded methods (Lasso, Ridge, Decision Tree). Ta sẽ cùng nhau làm rõ hơn trong phần sau.

### Wrapper methods

**Wrapper methods** là phương pháp tính toán hiệu suất mô hình với một tập hợp con các feature nhất định và đánh giá tầm quan trọng của từng feature. Sau đó, ta lặp lại và thử một tập hợp con các features khác nhau cho đến khi đạt được tập hợp con tối ưu. Hai nhược điểm của phương pháp này là thời gian tính toán lớn cho dữ liệu có nhiều features và nó có xu hướng phù hợp với mô hình khi không có nhiều điểm dữ liệu. Các Wrapper methods đáng chú ý nhất của Feature selection là **forward selection**, **backward selection**, và **stepwise**. selection.
