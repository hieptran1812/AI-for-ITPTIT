# Numpy

## Giới thiệu

### Numpy là gì ?

Numpy là một package cơ bản cho tính toán khoa học trong Python. Đó là một thư viện Python cung cấp một đối tượng mảng nhiều chiều (multidimensional array) và các thao tác nhanh trên mảng, bao gồm: toán học, logic, shape manipulation, sắp xếp, lựa chọn, I/O, biến đổi Fourier rời rạc, đại số tuyến tính cơ bản, thống kê cơ bản, mô phỏng ngẫu nhiên (random simulation) và hơn thế nữa.

Có một số sự khác biệt giữa array Numpy và các collection Python (list, tuple, set, dictionary) tiêu chuẩn đó là:
* Array Numpy có kích thước cố định khi tạo, không giống như List trong Python (có thể phát triển linh hoạt). Thay đổi kích thước của một ndarray sẽ tạo ra một array mới và xóa array gốc.
* Các phần tử trong mảng Numpy đều được yêu cầu phải cùng loại dữ liệu. Ngoại lệ: người ta có thể có các mảng của các đối tượng (Python, bao gồm Numpy), do đó cho phép các mảng của các yếu tố kích thước khác nhau.
* Mảng Numpy tạo điều kiện cho tính toán toán học và các hoạt động khác trên số lượng lớn dữ liệu. Thông thường, các hoạt động như vậy được thực thi hiệu quả hơn và với ít phải code dài hơn (mình sẽ giải thích trong phần code).

### Tại sao Numpy lại nhanh như vậy ?

Ưu điểm của Vectorization (Vector hóa):

* Code vector hóa ngắn gọn hơn và dễ đọc hơn.
* Vì ngắn gọn hơn nên việc debug không bị rối mắt :D
* Việc code các công thức toán học sẽ rất tường mình, dễ hiểu.
* Giảm tối đa việc for-loop từng phần tử, công thức. Do đó tận dụng được ưu thế của phần cứng giúp cho việc tính toán nhanh hơn.

### Một số thao tác trên Numpy

* Khởi động nhanh: [Quickstart](https://github.com/hieptran1812/AI-for-ITPTIT/blob/master/Python%20for%20Data%20Science/Numpy/Quickstart%20Numpy.ipynb)

## Tham khảo

1. [Khóa học CS231](https://cs231n.github.io/python-numpy-tutorial/#numpy)
2. [nttuan8](https://nttuan8.com/)
