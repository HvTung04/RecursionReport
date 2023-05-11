# :man_teacher: SELF_STUDY REPORT ON RECURSION 

![Thinking Recursive](https://realpython.com/cdn-cgi/image/width=640,format=auto/https://files.realpython.com/media/Thinking-Recursively-in-Python_Watermarked.db67ac63aeb5.jpg) 

## **1, Khái niệm đệ quy**

Đệ quy là một phương pháp giải quyết bài toán bằng cách phân chia bài toán lớn thành các bài toán con nhỏ hơn, và giải quyết từng bài toán con đó bằng cách sử dụng lại chính phương pháp giải quyết bài toán ban đầu trên bài toán con đó.

Trong đệ quy, thay vì giải quyết bài toán lớn trực tiếp, ta sẽ chia nhỏ nó thành các bài toán con có cùng cấu trúc và giải quyết từng bài toán con đó. Trong quá trình giải quyết bài toán con, nếu bài toán con vẫn còn phức tạp, ta sẽ tiếp tục chia nhỏ và giải quyết bài toán con đó bằng cách sử dụng lại chính phương pháp giải quyết bài toán ban đầu.

Phương pháp đệ quy thường được sử dụng trong lập trình để giải quyết các bài toán liên quan đến cây, đồ thị, hoặc các bài toán có cấu trúc lặp đi lặp lại. Trong lập trình, đệ quy thường được triển khai thông qua việc sử dụng hàm đệ quy, trong đó hàm sẽ gọi lại chính nó để giải quyết các bài toán con.

## **2, Ví dụ cơ bản**

Đệ quy có thể được sử dụng để giải quyết đa dạng các bài toán như:

- Tính giai thừa của một số nguyên dương n.
- Tìm kiếm tuyến tính trong một mảng.
- Tìm kiếm nhị phân trong một mảng đã được sắp xếp.
- Duyệt cây nhị phân và in ra các node.
- Sắp xếp một mảng bằng phương pháp quicksort.

## **3, Ứng dụng của đệ quy**

Đệ quy là một khái niệm quan trọng trong khoa học máy tính và được sử dụng rộng rãi trong nhiều ứng dụng thực tế. Dưới đây là một số ví dụ về ứng dụng của đệ quy trong thực tế:

- Thuật toán sắp xếp đệ quy: Các thuật toán sắp xếp đệ quy như quicksort và mergesort được sử dụng để sắp xếp một mảng các phần tử. Những thuật toán này được sử dụng rộng rãi trong lĩnh vực khoa học máy tính và là một phần quan trọng của các thư viện sắp xếp tiêu chuẩn trong nhiều ngôn ngữ lập trình.

- Cấu trúc dữ liệu đệ quy: Cấu trúc dữ liệu đệ quy như danh sách liên kết đơn và cây nhị phân là các cấu trúc dữ liệu được sử dụng rộng rãi trong nhiều ứng dụng thực tế, bao gồm các trình duyệt web, các hệ thống tìm kiếm và các hệ thống quản lý cơ sở dữ liệu.

- Giải thuật tìm kiếm đệ quy: Giải thuật tìm kiếm đệ quy được sử dụng để tìm kiếm các giá trị trong một mảng hoặc trong một cấu trúc dữ liệu như danh sách liên kết đơn hoặc cây nhị phân.

- Lập trình phân tán: Đệ quy được sử dụng trong lập trình phân tán để giải quyết các bài toán về tìm kiếm và xử lý dữ liệu trên các hệ thống phân tán.

- Xử lý ngôn ngữ tự nhiên: Trong xử lý ngôn ngữ tự nhiên, đệ quy được sử dụng để phân tích câu, phân tích cú pháp và sinh từ vựng.

Với sự phát triển của khoa học máy tính và công nghệ thông tin, đệ quy đã được sử dụng rộng rãi trong nhiều lĩnh vực và được xem là một công cụ mạnh mẽ trong việc giải quyết các bài toán phức tạp.

## **4, Các tính chất của đệ quy**

Đệ quy được xây dựng lên bởi các tính chất cơ bản nhưng vô cùng quan trọng: 
- Trường hợp cơ sở: Đây là điều kiện dừng của đệ quy. Nói cách khác, đệ quy phải dừng lại ở một điểm nào đó và trả về một kết quả.
- Thành phần tự hồi: Đệ quy là quá trình giải quyết một bài toán bằng cách giải quyết các bài toán con của nó. Các bài toán con này thường giống hệt bài toán ban đầu, chỉ khác về quy mô nhỏ hơn.
- Đệ quy trực tiếp và gián tiếp: Trong đệ quy trực tiếp, một hàm gọi chính nó làm đầu vào. Trong đệ quy gián tiếp, một hàm gọi một hàm khác, và sau đó hàm được gọi lại gọi lại hàm ban đầu.
- Thứ tự giải quyết: Khi giải quyết bài toán đệ quy, thứ tự của các bài toán con được giải quyết có thể ảnh hưởng đến hiệu suất của thuật toán. Đệ quy có thể được giải quyết theo thứ tự trên xuống hoặc từ dưới lên.
- Thời gian và không gian: Thời gian và không gian là hai yếu tố quan trọng cần được xem xét khi sử dụng đệ quy. Đệ quy có thể tốn nhiều thời gian và bộ nhớ hơn so với các phương pháp khác.

Ngoaì ra cần lưu ý một số định lý liên quan đến đệ quy như sau:
- Định lý về đệ quy: Định lý này chỉ ra rằng một thuật toán đệ quy có thể được chuyển đổi thành một thuật toán không đệ quy, và ngược lại.

- Định lý đệ quy đơn giản: Định lý này chỉ ra rằng một bài toán đệ quy có thể được giải quyết bằng một thuật toán đệ quy đơn giản nếu các bài toán con của nó được giải quyết bằng các bài toán con đơn giản hơn.
