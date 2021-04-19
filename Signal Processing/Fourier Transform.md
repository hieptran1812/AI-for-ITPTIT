# Fourier Transform

## Time Series

Time series chỉ đơn giản là một tập hợp các giá trị được sắp xếp theo thời gian. Ví dụ, giá chỉ số chứng khoán, thường được mô tả dưới dạng biểu đồ giá so với thời gian. Một ví dụ khác là dự báo 7 ngày sẽ cho thấy nhiệt độ cao trong vài ngày. Chuỗi thời gian là một cách tự nhiên để biểu diễn dữ liệu.

<p align="center"><img src="https://miro.medium.com/max/875/1*tExj_F1VumxNq2Q8pxay8A.png"></p>

## Signals

Tín hiệu là một loại time series. Cụ thể hơn, tín hiệu là các đại lượng thay đổi theo thời gian biểu thị các sự kiện vật lý. Hai tính chất cơ bản của tín hiệu là: biên độ và tần số.  Biên độ của một tín hiệu là độ lớn của nó, ví dụ: Độ lớn của tín hiệu âm thanh. Tần số của tín hiệu đặc trưng cho dao động của nó trong thời gian, ví dụ: Cao độ do guitar phát ra.

<p align="center"><img src="https://miro.medium.com/max/875/1*QaUWu-_TmyO7yTZ1W3ylmA.png"></p>

Dễ thấy, khi đi từ tín hiệu liên tục (tập hợp đại lượng vô hạn) sang tín hiệu rời rạc (tập đại lượng hữu hạn) thì thông tin bị mất. Do đó, tín hiệu rời rạc thường là tín hiệu gần đúng của tín hiệu liên tục.  Ví dụ, hãy xem xét việc thu thập các biến động nhiệt độ trong văn phòng để chạy hệ thống HVAC.  Tại bất kỳ thời điểm nào, văn phòng sẽ có nhiệt độ môi trường trung bình.  Giả sử một bộ nhiệt kế được sử dụng để đo nhiệt độ mỗi giờ.  Phép đo này sẽ tạo ra một tín hiệu rời rạc xấp xỉ với sự dao động nhiệt độ thực trong văn phòng.  Có lý khi nghi ngờ rằng những bản ghi nhiệt độ hàng giờ này sẽ dẫn đến điều hòa không khí kém, vì nhiệt độ có thể sẽ thay đổi theo thời gian với quy mô nhỏ hơn nhiều giờ.  Nếu vậy, nhiệt độ phải được đo thường xuyên như thế nào? Câu hỏi này được trả lời bằng cách sử dụng Định lý Nyquist. Trạng thái nào để thu được tín hiệu liên tục một cách đáng tin cậy, tốc độ ghi thông tin, được gọi là tốc độ lấy mẫu, phải gấp đôi tần số của tín hiệu quan tâm.  Đây là lý do tại sao âm thanh thường được lấy mẫu ở 44.100 Hz, vì giới hạn trên đối với thính giác của con người là khoảng 20.000 Hz.

Trong thực tế, việc nắm bắt thông tin có ý nghĩa từ một môi trường có thể không đơn giản như vậy. Các tín hiệu trong thế giới thực thường không theo chu kỳ, nhiễu và bị ảnh hưởng bởi nhiều nguồn. Trích xuất thông tin hữu ích từ các tín hiệu này là mục tiêu cơ bản của quá trình xử lý tín hiệu.

## The Fourier Transform

<p align="center"><img src="https://miro.medium.com/max/640/1*PTm2p-z-PPV9sb1-WGl9vw.png"></p>

Cốt lõi của quá trình xử lý tín hiệu là Fourier Transform (FT). FT phân hủy một hàm thành sin và cosin, tức là sóng. Về lý thuyết, bất kỳ hàm nào cũng có thể được biểu diễn theo cách này, nghĩa là, dưới dạng tổng (có thể là vô hạn) hàm sin và cosin của các biên độ và tần số khác nhau.

<p align="center"><img src="https://miro.medium.com/max/875/1*ByM5OCU2NL8alWCdmpPIVQ.png"></p>


