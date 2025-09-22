# Swift-MyKnowledge
Đây sẽ là nơi mình chia sẻ lại kiến thức về IOS đã vào đầu mình thì nó sẽ như thế nào.

## Phần 1 : OOP
Đây là điểm bắt đầu của mọi lập trình viên sau khi học về con trỏ.
**Hướng đối tượng là gì ?** - Câu hỏi dễ để hiểu nhưng khó để trình bày.
Theo ý hiểu của mình : Thì lập trình hướng đối tượng là việc lập trình viên sẽ trìu tượng hoá các đối tượng và biến nó thành code
Ví dụ : Bạn không thể thể hiện Con người, con vật hay đồ vật trong code mà không có OOP, OOP sẽ trìu tượng nó và biến nó thành code

**Một đối tượng sẽ có 4 Tính chất : Kế thừa, Đóng gói, Đa hình, Trìu tượng**
Ban đầu mình thấy khá lú giữa cái đa hình và trìu tượng khi mới học mà chưa được va vấp nhiều
**Đầu tiên: Tính kế thừa**
Khi lớp con kế thừa từ lớp cha thì sẽ được kế thừa toàn bộ các thuộc tính và phương thức của lớp cha đó.
Có 2 kiểu kế thừa là đa kế thừa và đơn kế thừa, tuy nhiên **Swift chỉ hỗ trợ đơn kế thừa giữa các class**
Có thể mô phỏng đa kế thừa nhưng chỉ có thể kế thừa từ protocol 
**Protocol là gì ?**
Theo mình hiểu thì protocol là một bản hợp đồng, giống như interface của các ngôn ngữ như Java hoặc C#,
nó như một khuôn mẫu sẵn và bắt buộc những class kế thừa nó phải tuân theo và thực hiện
-> Cái này mình mới search chat thì nó bảo nó sẽ phục vụ cho tính đa hình và trìu tượng cùng tìm hiểu ở dưới nhé!

**Thứ hai: Tính đóng gói**
Hiểu sơ sơ là bạn sẽ quyết định xem một số thứ của bạn ( biến , hàm) ai được dùng nó, Ví dụ như bạn đóng gói số dư tài khoản và chỉ mở hàm chuyển tiền -> muốn thay đổi số dư bắt buộc phải thông qua hàm chuyển tiền
Sẽ được thể hiện bằng các từ khoá các bạn rất hay gặp là public hay private
Nó sẽ là access control sẽ có 5 loại : private, fileprivate, internal, public, open
Giờ sẽ đi tìm hiểu từng cái 1 nhé : 
-Private : Chỉ có phạm vi truy cập trong class đó ( Bạn kế thừa class có thuộc tính private thì class con cũng sẽ không truy cập được private của cha nhé )
-Fileprivate : Là cho phép truy cập bên trong cùng một file Swift chứa định nghĩa ( Khá lú, chả hiểu lắm )
-internal ( mặc định) : Là sẽ cho phép truy cập bên trọng cùng một module - là ứng dụng của mình hoặc framework
-public : cho phép truy cập từ bất kỳ đâu hen, thường sẽ dùng cho thư viện hoặc framework (Giờ mới biết nè)
-open : giống như public nhưng cho phép ghi đè hoặc kế thừa từ bên ngoài nghĩa là ( = public + overiding) ( lú vch)
**À quên phân biệt giữa Library và Framework nhé, Nhiều bạn vẫn nhầm lẫn giữa 2 cái này**
Dễ hình dung nhất ta sẽ có ví dụ là UIKit là framework còn Alamofire, Rxswift là Library
Thì sẽ hiểu là thư viện sẽ là các hàm, lớp dùng để thực hiện 1 số chức năng nào đó như Alamofire để call API, Networking , còn framework là tổng hợp của các thư viện nó như một bộ khung được dựng sẵn, có cấu tạo hoàn chỉnh để có thể phát triển ứng dụng.

**Thứ ba: Tính đa hình**
Thực chất đa hình để giải quyết bài toán cùng là một hành động gì đó nhưng cách thực hiện sẽ khác nhau -> Giúp tăng tính linh hoạt và mở rộng khi code.
Ví dụ như đều là con người -> chúng ta đều biết nói chuyện nhưng người Việt Nam sẽ nói Tiếng Việt còn người Trung Quốc thì họ nói tiếng Hán thì đa hình sẽ giải quyết cái này trong việc code.
--Có 2 loại đa hình là tĩnh và động--

**Cuối cùng: Tính trìu tượng( lú nhất)**
Chỉ tập trung vào cái gì chứ không tập trung vào làm như thế nào.
Cái này mình hiểu là nó sẽ giúp phát triển và bảo trì, ví dụ BE đưa đầu api cho biết data đầu vào đầu ra FE không cần biết nó thực hiện như thế nào chỉ cần cầm nó và chạy
Cách sử dùng thường sẽ dùng protocol hoặc extension

**Giờ sẽ thực hành chút cho dễ hình dung nhé**
<img width="656" height="585" alt="image" src="https://github.com/user-attachments/assets/07d42194-df8b-4a15-9c22-47044f50ad9a" />
--Để sau đi--

***Kết thúc phần 1 nhé !***

## Phần 2 : Phần này chúng ta sẽ đi làm rõ về Protocol, Closure, và Callback nhé!

