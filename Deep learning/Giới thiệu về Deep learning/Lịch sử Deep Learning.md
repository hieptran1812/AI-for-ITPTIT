## Lời nói đầu

Trước khi tìm hiểu một vấn đề gì, chúng ta nên tìm hiểu lịch sử ra đời, cách chúng được tạo ra và phát triển như nào. Điều này rất tốt cho
việc tìm nguồn cảm hứng học tập, không những thế ta có thể bắt được mạch suy nghĩ của thời đại về vấn đề đó, từ đấy bản thân có thể suy rộng và phát triển thêm. Hãy dành chút thời gian đọc bài viết này mặc dù nó không liên quan nhiều đến kiến thức cần học nhé.

## Nguồn cảm hứng và lịch sử của Deep Learning

Ở cấp độ khái niệm, ta có thể thấy trong nhiều bài báo nói rằng Deep learning lấy cảm hứng từ bộ não con người nhưng phải hiểu rằng không
phải chi tiết nào của bộ não cũng đều liên quan. So sánh một chút, ta biết rằng máy bay được ra đời được truyền cảm hứng từ những chú chim. Nguyên lý bay có thể như nhau, nhưng cách vận hành của hai vật thể lại rất khác nhau.

Lịch sử của Deep learning bắt đầu từ những năm 1940 bởi hai nhà khoa học McCulloch và Pitts. Họ đã đưa ra ý tưởng rằng các nơ-ron là đơn vị ngưỡng có trạng thái bật và tắt. Bạn có thể xây dựng một mạch Boolean bằng cách kết nối các nơ-ron với nhau và tiến hành suy luận logic với các nơ-ron. Bộ não về cơ bản là một cỗ máy suy luận logic vì tế bào thần kinh là nhị phân. Neuron tính tổng đầu vào có trọng số và so sánh tổng đó với ngưỡng của nó. Nó bật nếu nó vượt quá ngưỡng và tắt nếu nó dưới ngưỡng, đây là một cái nhìn đơn giản về cách thức hoạt động của các mạng thần kinh.

Năm 1947, Donald Hebb đã có ý tưởng rằng các tế bào thần kinh trong não học bằng cách sửa đổi sức mạnh của các kết nối giữa các tế bào thần kinh. Điều này được gọi là Hyper learning, trong đó nếu hai nơ ron fired cùng nhau, thì kết nối liên kết giữa chúng tăng lên; nếu không, thì kết nối sẽ giảm. 

Sau năm 1948, điều khiển học được Norbert Wiener đề xuất, ý tưởng là có các hệ thống cảm biến và bộ truyền động, bạn có một vòng phản hồi và hệ thống tự điều chỉnh. Các quy tắc của cơ chế phản hồi của một chiếc xe đều xuất phát từ công việc này. 

Năm 1957, Frank Rosenblatt đã đề xuất Perceptron, đây là một thuật toán học tập điều chỉnh trọng số của các mạng lưới thần kinh rất đơn giản.

Nhìn chung, ý tưởng cố gắng chế tạo máy móc trí tuệ bằng cách mô phỏng rất nhiều tế bào thần kinh đã ra đời vào những năm 1940, cất cánh vào những năm 1950 và hoàn toàn ngỏm vào cuối những năm 1960. Những lý do chính cho lĩnh vực này hấp hối vào năm 1960 là:

* Các nhà nghiên cứu đã sử dụng tế bào thần kinh là nhị phân. Tuy nhiên, cách để backpropagation hoạt động là sử dụng các chức năng kích hoạt liên tục. Vào thời điểm đó, các nhà nghiên cứu đã không có ý tưởng sử dụng các nơ-ron liên tục và họ đã không nghĩ rằng họ có thể train với gradient vì các nơ-ron nhị phân không khác biệt. 
* Với các nơ-ron liên tục, người ta sẽ phải nhân hàm kích hoạt của một nơ-ron với trọng số để có được sự đóng góp cho tổng trọng số. Tuy nhiên, trước năm 1980, phép nhân của hai số, đặc biệt là số có dấu phẩy động, cực kỳ chậm. Điều này dẫn đến một lý do khác để tránh sử dụng tế bào thần kinh liên tục.

Deep Learning quay trở lại vào năm 1985 với sự xuất hiện của Backpropagation. Năm 1995, lĩnh vực này đã chết một lần nữa và cộng đồng máy học đã từ bỏ ý tưởng về mạng lưới thần kinh. Đầu năm 2010, mọi người bắt đầu sử dụng mạng nơ ron trong nhận dạng giọng nói với sự cải thiện hiệu suất lớn và sau đó nó đã được triển khai rộng rãi trong lĩnh vực thương mại. Năm 2013, thị giác máy tính bắt đầu chuyển sang neural network. Năm 2016, quá trình chuyển đổi tương tự đã xảy ra trong xử lý ngôn ngữ tự nhiên. Không lâu nữa, các cuộc cách mạng tương tự sẽ xảy ra trong chế tạo robot, điều khiển và nhiều lĩnh vực khác.

