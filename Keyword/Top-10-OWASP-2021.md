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
