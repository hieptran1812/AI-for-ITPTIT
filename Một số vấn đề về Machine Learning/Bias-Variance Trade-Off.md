# The Bias-Variance Trade-Off

Thuật toán học giám sát có thể giải thích dễ hiểu thông qua lăng kính Bias-Variance Trade-Off. Ở phần này, chúng ta sẽ tìm hiểu về Bias-Variance Trade-Off
, cách sử dụng nó để hiểu hơn về các thuật toán học máy và có hiệu suất tốt hơn trên dữ liệu.

## Tổng quan

Trong các thuật toán học có giám sát, mục tiêu của ta là tìm một hàm ánh xạ f giữa input data (X) và đầu ra (Y). Hàm này có chức năng dự đoán đầu ra khi nhận vào một điểm dữ liệu mới.
Lỗi dự đoán (Prediction error) của bất kì thuật toán học máy nào đều có thể chia làm ba phần:
* Bias Error
* Variance Error
* Lỗi không thể khắc phục :DD

Lỗi không thể khắc phục có thể hiểu là dù bạn xây dựng một mô hình ngon đến đâu, bạn vẫn phải dính phải cái lỗi đó. Lỗi này đa phần là do các nhiễu (noise) trong dữ liệu của bạn.
Lượng nhiễu này thường khó tránh khỏi trong tập dữ liệu. 

<p align = "center"><img src = "https://i1.wp.com/nttuan8.com/wp-content/uploads/2019/04/bias_variance.png?w=468&ssl=1"></p>

## Bias Error

Bias: nghĩa là độ lệch, biểu thị sự chênh lệch giữa giá trị trung bình mà mô hình dự đoán và giá trị thực tế của dữ liệu.

Một mô hình với Bias cao thường không khớp với tập dữ liệu huấn luyện (Training data) hay nói một cách khác là mô hình này quá đơn giản. Điều này dẫn đến giá trị dự đoán sai lệch rất lớn so với training data và test data.

Một số ví dụ về các thuật toán low-bias gồm: KNN, SVM, Decision Trees. High-bias: Linear regression, Logistic Regression.

## Variance Error

Variance: nghĩa là phương sai, biểu thị độ phân tán của các giá trị mà mô hình dự đoán so với giá trị thực tế.

Một mô hình với Bias cao thường quá khớp với tập dữ liệu huấn luyện (Training data) hay nói một cách khác là mô hình này quá phức tạp, không mang tính tổng quát. Điều này dẫn đến giá trị dự đoán biểu diễn tốt trên training data nhưng lại high error trên test data.

Một số ví dụ về các thuật toán low-variance: Linear regression, Logistic Regression. High-variance: SVM, Decision Trees, KNN.

<p align = "center"><img src = "https://i2.wp.com/nttuan8.com/wp-content/uploads/2019/04/bias_variance_1-1.png?w=1042&ssl=1"></p>

## Dưới góc nhìn toán học

Ta có công thức sau: 

<p align = "center"><img src ="https://miro.medium.com/max/1158/1*e7VaoBh5apjaM2p4afkFyg.png"></p>

## Bias-Variance Trade-Off

<p align = "center"><img src = "https://miro.medium.com/max/1400/1*9hPX9pAO3jqLrzt0IE3JzA.png"></p>

Nếu model quá đơn giản và ít tham số sẽ dẫn đến bias cao và variance thấp. Ngược lại nếu model quá phức tạp và nhiều tham số sẽ dẫn đến bias thấp và variance cao. Do đó ta cần điểm cân bằng để hạn chế vấn đề này.

<p align = "center"><img src ="https://miro.medium.com/max/1124/1*RQ6ICt_FBSx6mkAsGVwx8g.png"></p>

Nói một cách khác ta sẽ minimize total error.

<p align = "center"><img src ="https://miro.medium.com/max/882/1*SKHGhoGKnBh_GPGHI2Ktvw.png"></p>

Hiểu vấn đề về Bias Variance Trade-Off sẽ giúp bạn xây dựng model ngon nghẻ hơn :DDD

## Tham khảo

* [Toward Data Science](https://towardsdatascience.com/)
* [nttuan8](https://nttuan8.com/bai-10-cac-ky-thuat-co-ban-trong-deep-learning/)
