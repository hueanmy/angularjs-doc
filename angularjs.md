#### Introduction:

* What is angularjs?
  * What? : is a structural framework for dynamic web apps.
  * A library: a collection of functions which are useful when writing web apps.
  * Frameworks: a particular implementation of web application, where your code fills in the details.
  * Client-side:
* A complete client-side solution:
  * Angularjs ko phải là một thành phần duy nhất trong tổng thể việc xây dựng ứng dụng web phía client-side. 
  * Nó xử lý tất cả các mã DOM và AJAX mà chúng ta từng viết bằng tay và đặt chúng vào trong một cấu trúc được xđ rõ ràng.
  * Angular đi kèm với out-of-the-box:
    * Bất cứ thứ gì chúng ta cần để xây dựng một ứng dụng CRUD đều nằm trong một bộ cố định: Data-binding, basic templating directives, form validation, routing, deep-linking, reusable components and dependency injection.
    * Testability story: Unit-testing, end-to-end testing, mocks and test harnesses.
    * Seed application with directory layout and test scripts as a starting point.
* Angular's sweet spot:
  * Angular simplifies application development by presenting a higher level of abstraction to the developer
* The Zen of Angular:
  * DOM : 
    * DOM  là một giao diện lập trình độc lập nền tảng và độc lập ngôn ngữ. Nó cho phép các chương trình, các mã lập trình truy xuất động và cập nhật nội dung, cấu trúc cũng như định dạng của tài liệu.
    * là một chuẩn được định nghĩa bởi W3C dùng để truy xuất và thao tác trên các tài liệu có cấu trúc dạng HTML hay XML bằng các ngôn ngữ lập trình thông dịch (scripting language) như Javascript, PHP, Python
    * DOM giúp thao tác dữ liệu theo mô hình hướng đối tượng
  * Imperative Programming & Declarative Programming:
    * Imperative Programming: telling the “machine” how to do something, and as a result what you want to happen will happen. (Quan tam den viec lam the nao de giai quyet bai toan)
    * Declarative Programming:  telling the “machine” what you would like to happen, and let the computer figure out how to do it. (Quan tam toi dau vao dau ra cua bai toan khong quan tam den cach lam)
  * Angular sử dụng declarative code. Imperative code phù hợp cho việc thể hiện logic nghiệp vụ.
  * Angularjs giúp bạn thoát khỏi:
    * Registering callbacks: 
    * Manipulating HTML DOM programmatically.
    * Marshaling data to and from the UI
    * Writing tons of initialization code just to get started
* Các thành phần quan trọng của AngularJs:
  * Data binding
  * Scope
  * Dependency injection
  * Filters
  * Services
  * Factories
  * Expressions
  * Providers
  * Validators
  * Derectives
  * Controllers
  * Modules


### Data binding

* What? : Trong ứng dụng angularjs thì data binding là việc đồng bộ dữ liệu giữa model và các view components một cách tự động.

* Cách mà angularjs triển khai data binding cho phép chúng ta coi model là single-source-of-truth trong ứng dụng.

* View là sự thể hiện của model tại tất cả các thời điểm, khi model thay đổi view sẽ phản ánh lại sự thay đổi đó và ngược lại.

* Data binding is Classical template system: 

  ![](https://docs.angularjs.org/img/One_Way_Data_Binding.png)

* In angularJs template

  ![Two way data binding](https://docs.angularjs.org/img/Two_Way_Data_Binding.png)

* Đầu tiên, template sẽ được biên dịch trên browser. Bước biên dịch này ta xem trực tiếp trên view, mọi thay đổi của View sẽ được update vào Model, và bất cứ thay đổi nào của model sẽ được truyền ra view. 

### Controllers

* In angularjs, a controller is defined by a Js constructor function 
* A Controller gắn với phần tử DOM thông qua lệnh ng-controller. AngularJs sẽ tạo ra một new Controller object, sử dụng constructor function của controller được chỉ định. Một new child scope sẽ được tạo và có thể dùng như một tham số đính kèm tới controller's constructor function  như scope.
* Sử dụng controller để:
  * Setup trạng thái ban đầu (initial state) của $scope object: đính kèm các thuộc tính vào trong scope object.
  * Thêm hành vi (behavior) tới $scope object: thêm method tới scope object

### Services

* Is substitutable objects được nối với nhau bằng cách sử dụng dependency injection.
* Use to: organize and share code across to app
* Angularjs service are: 
  * Lazily instantiated: chỉ khởi tạo một service khi một app component phụ thuộc vào nó.
  * Singletons: Môĩ component phụ thuộc vào một service tham chiếu đến một single instance được tạo bởi service factory.
  * ​