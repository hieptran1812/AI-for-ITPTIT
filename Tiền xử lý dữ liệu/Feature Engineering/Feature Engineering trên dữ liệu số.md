## Features là gì ?

Một đặc trưng (feature) thường là một đại diện cụ thể trên dòng đầu tiên của dữ liệu thô, là một thuộc tính riêng lẻ, có thể đo lường và mô tả bởi một cột trong tập dữ liệu. Lấy ví dụ với một tập dữ liệu hai chiều, mỗi observation (quan sát) được mô tả bởi một hàng và mỗi đặc trưng được mô tả bởi một cột, sẽ có giá trị cụ thể cho mỗi đặc trưng của từng quan sát.

<p align = "center"><img src = "https://images.viblo.asia/560bb949-3c2e-41b1-b9b8-2d64dc82c3ca.png"></p>

Như ví dụ ở hình trên, mỗi hàng thường biểu thị một vectơ đặc trưng và tập hợp tất cả các đặc trưng trên tất cả các quan sát tạo thành một ma trận hai chiều còn được gọi là feature-set. Thông thường, các thuật toán học máy hoạt động với các ma trận số hóa hoặc tensor bởi vậy hầu hết các kỹ thuật feature engineering sẽ xử lý việc chuyển đổi dữ liệu thô thành các dạng biểu diễn số học giúp các thuật toán có thể dễ dàng hiểu được.

Các đặc trưng có thể chia thành hai loại chính:

* **Đặc trưng thô (Raw features)**: là các đặc trưng vốn có được lấy trực tiếp từ tập dữ liệu mà không cần sử dụng thêm thao tác kỹ thuật nào.
* **Đặc trưng phát sinh (Derived features)**: là các đặc trưng được thu được sau quá trình feature engineering, là kết quả của quá trình trích xuất và xử lý các đặc trưng có sẵn. Ví dụ, chúng ta có một đặc trưng thô là "sinh nhật" của nhân viên và chúng ta có thể dễ dàng có được một đặc trưng mới là "tuổi" của các nhân viên đó bằng cách trừ năm hiện tại cho năm sinh của họ.

Có rất nhiều loại và nhiều định dạng dữ liệu khác nhau bao gồm cả dữ liệu có cấu trúc và dữ liệu phi cấu trúc. Trong phần tiếp theo, chúng ta sẽ thảo luận về các cách tiếp cận khác nhau để xử lý dữ liệu có cấu trúc dạng số liên tục (continuous numeric data). 

## Feature Engineering trên dữ liệu số

* Dữ liệu số (numeric data) thường biểu thị dữ liệu dưới dạng giá trị vô hướng mô tả các quan sát, bản ghi hoặc thang đo. Ở đây, với từ **numeric data** chúng ta cần hiểu là dữ liệu liên tục mà không phải dạng dữ liệu rời rạc thường được coi như dạng dữ liệu phân loại (categorical data).
* Dữ liệu số cũng có thể được biểu diễn dưới dạng vectơ của các giá trị, trong đó mỗi giá trị trong vectơ có thể biển diễn cho một đặc trưng cụ thể. Intergers và Floats là các loại dữ liệu số phổ biến nhất và thường được sử dụng cho dạng dữ liệu số liên tục.
* Mặc dù dữ liệu số là dạng dữ liệu có thể đưa trực tiếp vào các mô hình học máy. Tuy nhiên, việc thiết kế các tính năng có liên quan đến kịch bản, vấn đề cần giải quyết và domain của bài toán vẫn là rất cần thiết.

Sau đây, chúng ta sẽ sử dụng python để xây dựng một số phương pháp feature engineering với dữ liệu dạng số liên tục.

## Xử lý thô (Raw Measures)

Như đã đề cập ở trên, dữ liệu thô có thể được đưa trực tiếp vào các mô hình học máy tùy thuộc vào hoàn cảnh và dạng của dữ liệu. Xử lý thô thường là cách sử dụng biến số trực tiếp của các đặc trưng mà không có bất kỳ hình thức, kỹ thuật biến đổi nào. Thông thường, các biến số này sẽ cho biết giá trị hoặc số lượng của đặc trưng. 

<p align = "center"><img src = "https://miro.medium.com/max/1400/1*UEVbo3a2WWK2sY1CH5RI9g.png"></p>

## Xử lý giá trị (Values)

Hãy quan sát hình trên, bạn có thể thấy rằng một số đặc trưng có thể sử dụng trực tiếp bằng giá trị thô. Đoạn code dưới đây sẽ thể hiện rõ hơn những đặc trưng này.

poke_df[['HP', 'Attack', 'Defense']].head()

<p align = "center"><img src = "https://images.viblo.asia/bdb088fe-a9ee-4cab-9d1a-4c263fcd81d6.png"></p>

Bảng trên thể hiện đặc trưng với các giá trị số liên tục của nó. Do đó, bạn có thể trực tiếp đưa các đặc trưng này vào thuật toán học máy. Chúng bao gồm từng chỉ số của Pokémon: lượng máu (HP), sức tấn công (Attack), sức phòng thủ (Defense). Trên thực tế, chúng ta hoàn toán có thể sử dụng một số phương pháp thống kê cơ bản cho các đặc trưng này.

poke_df[['HP', 'Attack', 'Defense']].describe()

<p align = "center"><img src = "https://images.viblo.asia/2f9b0ea1-f658-49f9-8556-58b593c2afd9.png"></p>

