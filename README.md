### 1. Spring MVC (Spring Web MVC)

  Spring MVC là một Framework / 1 Project mã nguồn mở của Spring.

  Spring MVC Framework cung cấp kiến trúc MVC (Model-View-Controller) và các component được sử dụng để phát triển các ứng dụng web một cách linh hoạt
  
### 2. Flow trong Spring MVC
  ![spring-mvc-flow](https://user-images.githubusercontent.com/21329726/53214532-8284d280-367f-11e9-8da4-f758e6d74486.png)
  
  - Bất kỳ request nào tới ứng dụng web đều sẽ được gửi tới Front Controller (Dispatcher Servlet)
  - Front Controller sẽ sử dụng Handler Mapping để biết được controller nào sẽ xử lý request đó
  - Controller nhận request, gọi tới các class service thích hợp để xử lý yêu cầu.
  - Sau khi xử lý xong, Controller sẽ nhận được model từ tầng Service hoặc tầng DAO.
  - Controller gửi model vừa nhận được tới Front Controller (Dispatcher Servlet)
  - Dispatcher Servlet sẽ tìm các mẫu view, sử dụng view resolver và truyền model vào nó.
  - View template, model, view page được build và gửi trả lại Front Controller
  - Front Controller gửi một page view tới trình duyệt để hiển thị nó cho người dùng.
  
  ![spring-mvc-flow-768x471](https://user-images.githubusercontent.com/21329726/53214614-cbd52200-367f-11e9-8f19-4ab878673d73.jpg)
  
  Trong Mô hình MVC thì:
  
    - Model: là các file POJO, Service, DAO thực hiện truy cập database, xử lý business
    - View: là các file JSP, html…
    - Control: là Dispatcher Controller, Handler Mapping, Controller – thực hiện điều hướn các request.
    
###  3. Các lợi ích của Spring MVC

  - Các tầng trong Spring MVC độc lập nên việc unit test dễ dàng hơn.
  - Phần view có thể tích hợp với nhiều Framework về UI như JSF, Freemarker, Themeleaf…
  - Spring MVC base trên các POJO class nên các hành động của nó khá đơn giản
  - Hỗ trợ cả Annotation và XML config giúp việc phát triển nhanh hơn và sạch hơn.
  - Cung cấp việc phân chia một cách rõ ràng, linh hoạt giữa controller, service, data acces layer.
  
### 4. Spring Web MVC
  ### 4.1. DispatcherServlet
  
    1.Special Bean Types
      - HandleMapping: Map a request to a handler along with a list of interceptors for pre- and post-processing. The mapping is based on some criteria, the details of which vary by HandlerMapping implementation.
