## OWASP là gì ?
- Là viết tắt của **O**pen **W**eb **A**pplication **S**ecurity **P**roject

- Là 1 tổ chức phi lợi nhuận chuyên cung cấp các bài viết, phương pháp, tài liệu và công nghệ trong lĩnh vực bảo mật ứng dụng web
## Top 10 OWASP là gì ?
- Là 1 dự án được cập nhật thường xuyên (mỗi 4 năm 1 lần) phác thảo về các mối đe dọa về bảo mật đối với các ứng dụng web. Top 10 lỗ hổng đó là: 
- **Top 1: Broken Access Control**
- **Top 2: Cryptographic Failures**
- **Top 3: Injection**
- **Top 4: Insecure Design**
- **Top 5: Security Misconfiguration**
- **Top 6: Vulnerable and Outdated Components**
- **Top 7: Identification and Authentication Failures**
- **Top 8: Software and Data Integrity Failures**
- **Top 9: Security Logging and Monitoring Failures**
- **Top 10: Server-Side Request Forgery**
## Giải thích top 10 lỗ hổng của OWASP
### Top 1: Broken Access Control
- Hãy tưởng tượng bạn là một người dùng thông thường trên các nền tảng mạng xã hội. Bạn sẽ không thể xem thông tin nhận dạng của người dùng khác, đó có thể là một tin nhắn, một hình ảnh hay một bài viết riêng tư của người khác. Nếu bạn có thể truy cập vào những dữ liệu riêng tư đó thì đó chính là lỗ hổng Broken Access Control bằng cách thay đổi id, ví dụ như id=1 ta thay đổi thành id=2 và ta có thể truy cập vào dữ liệu riêng tư của người khác (IDOR)

- Tóm lại Broken Access Control là 1 lớp lỗ hổng cho phép người dùng truy cập vào phần dữ liệu của người dùng khác để thực hiện những hành động không được phép (xem, xóa ,sửa)  
### Top 2: Cryptographic Failures
- Đây là loại lỗ hổng làm lộ dữ liệu nhạy cảm dựa trên những thuật toán mã hóa yếu hoặc không tồn tại (nó có thể là mật khẩu, thẻ tín dụng,...)

- Có thể hiểu đơn giản là mỗi khi gửi dữ liệu văn bản từ máy khách đến máy chủ ta cần được mã hóa dữ liệu bằng HTTPS    
### Top 3: Injection
- Là một lớp lỗ hổng cho phép thực thi mã trên máy chủ hoặc trình duyệt web (sql injection, xss, rce, command injection,...)

- Đối với máy chủ đó có thể là sql injection - lỗ hổng này cho phép chèn các câu lệnh truy vấn sql để lấy dữ liệu của người khác hoặc toàn bộ dữ liệu từ cơ sở dữ liệu của trang web

- Đối với máy khách thì có thể là xss - lỗ hổng này cho phép thực thi html hoặc javascript đối với người dùng truy cập vào trang web cụ thể và bạn có thể kiếm soát hành vi của họ trong trang web đó (Điều hướng người dùng, thay đổi mật khẩu,...)
### Top 4: Insecure Design
- Hãy tưởng tượng khi mua một món hàng online có giá $20 nhưng bằng một cách nào đó ta có thể đặt mua nó với giá chỉ là $1. Đây chính là 1 lỗi trong lớp lỗ hổng này khi mà các logic của ứng dụng được thiết kế không an toàn
### Top 5: Security Misconfiguration
- Đây là một loại lỗ hổng rất hay gặp 
- Hãy lấy một ví dụ như bạn là người cài đặt một máy chủ để khởi chạy một ứng dụng web cho công ty và sau đó bạn quên xóa tất cả file cấu hình mặc định đi kèm với nó. Là 1 hacker thì sẽ có 2 trường hợp xảy ra, trường hợp đầu tiên hacker sẽ brute force các username, password phổ biến, trường hợp 2 bạn cài đặt username và password mặc định và chưa thay đổi nó đi, các hacker có thể đọc được nó dựa trên các tài liệu do tổ chức phát hành và truy cập vào máy chủ
### Top 6: Vulnerable and Outdated Components
- Các ứng dụng web hiện đại ngày nay đều kết hợp nhiều thành phần mã nguồn mở (modul, khung). Bất kì thành phần nào đã lỗi thời hoặc được tìm thấy lỗ hổng trước đó cần nhanh chóng cập nhật bản vá lỗi. Nếu không nó sẽ trở thành một liên kết yếu ảnh hưởng đến tính bảo mật của cả một hệ thống 
### Top 7: Identification and Authentication Failures
- Khi 1 ứng dụng thực thi không chính xác các chức năng liên quan đến quản lý phiên hoặc xác thực người dùng thì các attacker có thể lợi dụng điều này để giả danh người dùng khác
### Top 8: Software and Data Integrity Failures
- Nó đề cập đến việc sử dụng các phần mềm, modul từ những nguồn không an toàn như github - nơi mà bất kì ai cũng có thể đóng góp vào mã cho các dự án. Nếu như các công ty sử dụng các nguồn này để cập nhật cho các phần mềm, dữ liệu của công ty. Ta có thể lợi dụng việc này để đẩy mã độc vào những bản cập nhật đó và phân phối cho các công ty khác. Từ đó ta có thể truy cập vào bất kì phần mềm nào

- Tóm lại khi các công ty triển khai mã, dữ án. Ta sẽ can thiệp vào đường dẫn CI/CD của họ và tìm cách đưa mã vào các bản cập nhật trên các resource mà họ đang sử dụng
### Top 9: Security Logging and Monitoring Failures
- Đây không hẳn là 1 loại lỗ hổng để tấn công

- Nó liên quan đến pháp y mạng, nó cho công ty biết khi nào xuất hiện một cuộc tấn công. Vì vậy nếu hệ thống này nhận thấy những điều bất thường thì nó sẽ ghi lại nhật kí để giúp việc phân tích diễn ra nhanh chóng

- Việc những hệ thống cảnh báo này được thiết kế không đầy đủ dẫn đến việc không thể phát hiện các cuộc tấn công sẽ giúp các attacker có thêm nhiều thời gian để xâm nhập vào hệ thống
### Top 10: Server-Side Request Forgery
- Đây là 1 lỗ hổng bảo mật web cho phép attacker giả mạo yêu cầu được đưa ra từ máy chủ để truy cập vào các ứng dụng được lưu hành nội bộ

- Hãy tưởng tượng các ứng dụng web dành cho nhân viên nội bộ trong công ty được thiết kế chỉ cho phép truy cập bởi các nhân viên trong công ty dựa trên 1 dãy IP duy nhất. Nếu một người dùng bên ngoài truy cập vào những ứng dụng web nội bộ này thì sẽ bị từ chối vì không đúng địa chỉ IP, tuy nhiên nếu ta thay đổi địa chỉ IP thành địa chỉ IP nội bộ thì sẽ truy cập được vào những ứng dụng này

