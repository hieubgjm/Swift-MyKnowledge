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

## Phần 2 : Phần này chúng ta sẽ đi làm rõ về Protocol, Closure, và Callback, Delegate nhé!
**Đầu tiên : Là sẽ tìm hiểu rõ về Protocol và Delegate.**
Bản chất Delegate nó là 1 protocol ( bản hợp đồng, interface) - Đã tìm hiểu ở trên
Delegate là 1 loại Design Pattern cho phép 1 đối tượng uỷ quyền một số tác vụ cho một số đối tượng khác thông qua protocol, ví dụ Sếp bạn nhận nhiệm vụ hoàn thành 1 task , sếp bạn không thể một mình làm hết dự án -> uỷ quyền cho bạn làm phần A -> Khi bạn làm xong, bàn giao lại cho sếp

**Closure là gì**
Bản chất closure là một function nhưng vô danh, nó được capture lại vào một biến, hằng trong để hoàn thành một nhiệm vụ trong ngữ cảnh nào đó.
--Chắc chả hiểu gì--

**Call back là gì**
Là một cơ chế trong đó một hàm ( hoặc closure) được truyền vào như một tham số và sẽ được gọi lại khi một tác vụ hoàn thành hoặc một sự kiện được xảy ra. Thường sẽ được sử dụng để xử lý các tác vụ bất đồng bộ ( gọi API, xử lý sự kiện, hoặc animation)
***Thông thường sẽ có 2 cách chính là Delegate và Closure :***
Theo mình tìm hiểu thì trước đây đa số sẽ xử dụng Delegate nhưng về sau khi Closure ra mắt nó được sử dụng rộng rãi.
Nhưng tuỳ hoàn cảnh cũng sẽ có những ưu nhược điểm. 
Về Delegate sẽ có ưu điểm là dễ bảo trì và mở rộng nhưng triển khai khó hơn và khi xử lý one to many relationships thì sẽ rất rối.( Bạn có thể hình dung giống việc bạn có 2 table view trong cùng 1 viewcontroller và bạn vẫn dùng .delegate = self) . Lúc này thì ....

Còn về closure thì sẽ rất dễ triển khai, code sẽ đơn lập dễ nhìn nhưng khó mở rộng, hoặc tái sử dụng lại.

**Phần này bạn cứ làm nhiều sẽ tự ngộ ra**

## Phần 3 : ARC (Automatic Reference Counting) 
Nó giúp tự động quản lý bộ nhớ cho các thể hiện(instance) của lớp(class) - Không phải làm thủ công như trước đây ( phải gọi retain - hoặc release )

**Sẽ chia làm 2 loại là Tham chiếu mạnh(Strong References) và Tham chiếu yếu(Weak References)**
Tham chiếu mạnh sẽ làm tăng thể hiện tham chiếu của đối tượng lên 1, có ít nhất 1 tham chiếu mạnh lên đối tượng thì đối tượng sẽ không được giải phóng.
Tham chiếu yếu không làm tăng số lượng tham chiếu nên đối tượng, khi đối tượng được giải phóng tham chiếu yếu sẽ tự động thành nil, do đó tham chiếu yếu luông là kiểu Optional.

## Phần 4 : Bất đồng bộ GCD - Async/Await
**Bản chất của 2 thằng hoàn toàn khác nhau nhé : về thằng GCD sẽ sâu về quản lý các Thread, có thể cấu hình từng thread 1 còn thằng async/await thì sẽ chủ yếu hỗ trợ về phần bất đồng bộ**
Trước hết ta phải hiểu là đồng bộ là gì và bất đồng bộ là gì :
Đồng bộ thì là ta sẽ làm từng việc một, làm xong việc này mới làm việc tiếp theo. Còn bất đồng bộ là ta sẽ thực hiện các việc khác rồi khi nào việc kia hoàn thành mới xử lý tiếp. Ví dụ như việc trò chuyện bằng thư, khi ta đi gửi thư xong phải mất thời gian người ta mới phản hồi thì trong lúc đó ta không thể chỉ chờ mà sẽ đi hoàn thành các việc khác trước rồi khi nào nhận được phản hồi mới xử lý tiếp. 
**Bản chất thằng Async/Await là nó sẽ tối ưu để làm sao làm được nhiều task nhất nhưng dùng ít thread nhất có thể**


