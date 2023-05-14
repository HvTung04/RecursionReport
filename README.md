# :man_teacher: SELF_STUDY REPORT ON RECURSION 

![Thinking Recursive](https://realpython.com/cdn-cgi/image/width=640,format=auto/https://files.realpython.com/media/Thinking-Recursively-in-Python_Watermarked.db67ac63aeb5.jpg) 

## **1, Khái niệm đệ quy**

Đệ quy là một phương pháp giải quyết bài toán bằng cách phân chia bài toán lớn thành các bài toán con nhỏ hơn có cách giải quyết tương tự. Vì thế ta hoàn toàn có thể áp dụng lại cách giải quyết của bài toán lớn để giải quyết bài toán con, trong lập trình, việc này được thực hiện khi một hàm gọi lại chính nó.

Trong đệ quy, thay vì giải quyết bài toán lớn trực tiếp, ta sẽ chia nhỏ nó thành các bài toán con có cùng cấu trúc và giải quyết từng bài toán con đó. Trong quá trình giải quyết bài toán con, nếu bài toán con vẫn còn phức tạp, ta sẽ tiếp tục chia nhỏ và giải quyết bài toán con đó bằng cách sử dụng lại chính phương pháp giải quyết bài toán ban đầu, tương tự như bước đầu tiên. Phương pháp đệ quy thường được sử dụng trong lập trình để giải quyết các bài toán liên quan đến cây, đồ thị, hoặc các bài toán có cấu trúc lặp đi lặp lại. 

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


## **5, Ý tưởng thuật toán**

Đệ quy có bản chất tương tự như một vòng lặp, khi mà ở mỗi bước đệ quy, ta lại lặp đi lặp lại một công việc nhất định. Để có được ý tưởng khi triển khai giải một bài toán, ta phải nhận ra rằng bài toán có thể được chia thành các bài toán con nhỏ hơn, và các bài toán con này lại có thể được chia thành các bài toán con nhỏ hơn nữa. Quá trình này được lặp đi lặp lại cho đến khi chúng ta có thể giải quyết các bài toán con đơn giản một cách trực tiếp (base case). Việc này đòi hỏi một khả năng tư duy trừu tượng và phân tích, và có thể giúp giải quyết các bài toán phức tạp một cách hiệu quả và dễ dàng hơn.

#### **a, Mã giả**
Bài toán: Tìm chiều cao của một cây nhị phân.
Cây nhị phân có các nút:

```
struct Node {
  int val;
  Node *left; // left child
  Node *righ; // right child
}
```
  Ta có thể áp dụng đệ quy để tìm chiều cao của một cây nhị phân như sau:
  
  ```
  int getHeight(node root: Chiều cao tính từ node này) {
    if (Cây không chứa node nào) return 0; // base case: Cây không có nút nào thì có chiều cao là 0
    
    Khởi tạo chiều cao của cây con trái: 
      leftHeight = getHeight(node root->left: Chiều cao bắt đầu tính từ node con bên trái)  // Recursive part
    Khởi tạo chiều cao của cây con phải: 
      rightHeight = getHeight(node root->right: Chiều cao bắt đầu tính từ node con bên phải)  // Recursive part
      
    Trả về chiều cao của cây
    return 1 + max (leftHeight, rightHeight); // Hàm đệ quy được gọi
  }
  ```


#### **b, Cài đặt**

Cài đặt thuật toán trên bằng ngôn ngữ C++:

```
int getHeight(Node* root) {
  if (!root) return 0;
  
  int leftHeight = getHeight(root->left);
  int rightHeight = getHeight(root->right);
  
  return 1 + max(leftHeight, rightHeight);
}
```

#### **c, Đánh giá**

- Bất biến của thuật toán này là chiều cao của cây con trái và cây con phải được tính toán độc lập với nhau, ta lấy chiều cao lớn nhất trong hai cây con và cộng thêm 1 để tính chiều cao của cây hiện tại.
- Time Complexity: Thuật toán này có độ phức tạp thời gian là O(n), trong đó n là số lượng nút trong cây. Trường hợp tốt nhất, khi cây có một node duy nhất hoặc không có node nào, thuật toán sẽ có độ phức tạp O(1). Trong trường hợp xấu nhất, độ phức tạp sẽ là O(n) khi cây có dạng như một danh sách liên kết. Độ phức tạp trung bình của thuật toán phụ thuộc vào cấu trúc của cây, nên không thể đưa ra một giá trị chính xác.
- Độ phức tạp không gian của thuật toán này là O(h), với h là chiều cao của cây. Vì khi thực hiện đệ quy, mỗi lần gọi đệ quy sẽ tạo ra một khung stack mới để lưu trữ các biến cục bộ và chỉ trả về kết quả khi đệ quy được giải quyết. Do đó, chiều cao của cây sẽ là h, số lượng khung stack cần tạo ra để giải quyết đệ quy sẽ là h và do đó độ phức tạp không gian sẽ là O(h).

#### **d, Cải tiến**

- Ý tưởng cải tiến: Sử dụng kỹ thuật [Memoization](https://www.freecodecamp.org/news/memoization-in-javascript-and-react/#:~:text=In%20programming%2C%20memoization%20is%20an,instead%20of%20computing%20it%20again.) (lưu trữ kết quả tính toán để tránh tính toán lại). Cụ thể, chúng ta có thể tạo ra một bảng băm (hash table) để lưu trữ chiều cao của các nút đã được tính toán. Khi đệ quy đến một nút, trước khi tính chiều cao của nó, ta kiểm tra xem chiều cao của nút đó đã được tính toán trước đó chưa, nếu có thì trả về kết quả lưu trữ trong bảng băm, ngược lại tính toán bình thường và lưu trữ kết quả vào bảng băm.


- Mã giả:
```
int getHeight(Node root: bắt đầu tính từ node này, unordered_map<Node*, int>& memo: bảng băm lưu trữ chiều cao các nút đã được tính toán) {
  if (root là null) return 0;
  
  if (tìm thấy root trong bảng) return chiều cao tương ứng với root được lưu trong bảng;
  
  Khởi tạo chiều cao cây con trái, phải
  int leftHeight = getHeight(root->left, memo);
  int rightHeight = getHeight(root->right, memo);
  
  Khởi tạo chiều cao tương ứng với node hiện tại
  int height = 1 + max(leftHeight, rightHeight);
  
  Lưu trữ chiều cao vào bảng băm
  
  return chiều cao;
}
```
- Cài đặt:

```

int getHeight(Node* root, unordered_map<Node*, int>& memo) {
    if (!root) return 0;
    
    if (memo.find(root) != memo.end()) {
        return memo[root];
    }
    
    int leftHeight = getHeight(root->left, memo);
    int rightHeight = getHeight(root->right, memo);
    
    int height = 1 + max(leftHeight, rightHeight);
    memo[root] = height;
    
    return height;
}
```

- Đánh giá:
  - Cải tiến này giúp giảm thiểu số lần tính toán chiều cao của các nút trên cây bằng cách lưu trữ chiều cao của mỗi nút trong cây. Việc lưu trữ này cho phép chúng ta truy cập và sử dụng chiều cao của một nút đã được tính toán trước đó mà không cần tính toán lại.

  - Với cải tiến này, khi tính chiều cao của một nút, ta chỉ cần truy cập vào giá trị chiều cao đã được tính toán trước đó của nút con, thay vì phải tính toán lại chiều cao của nút con đó. Do đó, số lần tính toán chiều cao trên các nút trong cây sẽ giảm, làm tăng tốc độ tính toán và giảm độ phức tạp của thuật toán.

  - Cụ thể, với cải tiến này, ta chỉ cần thực hiện một lần duyệt cây để tính toán và lưu trữ chiều cao của mỗi nút, sau đó ta có thể truy cập và sử dụng giá trị chiều cao này mỗi khi cần thiết mà không cần tính toán lại.

Tổng quan, cải tiến này giúp tối ưu hóa thời gian tính toán và độ phức tạp của thuật toán, đồng thời giảm thiểu việc tính toán lại các giá trị đã tính toán trước đó, giúp tăng tốc độ tính toán.

- Time complexity: O(n), trong đó n là số nút trên cây. Vì mỗi nút được truy cập đúng một lần và mỗi lần truy cập mất O(1) thời gian, nên tổng thời gian là O(n).

- Space complexity: O(h), trong đó h là chiều cao của cây. Do sử dụng đệ quy, với mỗi lời gọi đệ quy, một khung stack mới được tạo ra, và nó sẽ được giải phóng khi hàm đệ quy trả về. Vì vậy, tối đa có thể có h khung stack trên đỉnh nhau, do đó không gian bổ sung tối đa mà thuật toán này sử dụng là O(h). Trong trường hợp xấu nhất, khi cây là cây màu đen (nghĩa là có chiều cao là log n), không gian bổ sung sẽ là O(log n).


## **6, Bài tập** ##
Sau đây là một vài ví dụ về bài tập đệ quy:
- Tính giai thừa: Giai thừa của một số n là tích của dãy số dương từ 1 đến n, hay có thể gọi là tích của n với giai thừa của (n-1). Do đó ta có thể thiết kế hàm đệ quy cho (n-1) cho đến khi n bằng 1.

- Tìm số Fibonacci: Số fibonacci thứ n là tổng của số fibonacci thứ (n - 1) và số fibonacci thứ (n - 2) với f(0) = 0 và f(1) = 1. Để tính số fibonacci thứ n ta có thể gọi đệ quy cho (n - 1) và (n - 2) cho đến khi n = 0 hoặc n = 1 thì trả về chính nó.

- Sắp xếp mảng: Chọn một phần tử bất kỳ trong mảng làm chốt, rồi phân tách mảng thành hai phần: một phần chứa các phần tử nhỏ hơn hoặc bằng chốt và một phần chứa các phần tử lớn hơn chốt. Ta sử dụng đệ quy để sắp xếp hai phần này và ghép lại với nhau.

- Duyệt và tìm kiếm trong cây nhị phân: Đệ quy thường được ứng dụng trong các cấu trúc dữ liệu như cây nhị phân, danh sách liên kết, ... Ta có thể giải đa số các bài tập liên quan đến các cấu trúc dữ liệu trên bằng đệ quy.


