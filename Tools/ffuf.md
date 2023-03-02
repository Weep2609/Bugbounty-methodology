## Tham khảo thêm:
- [https://www.youtube.com/watch?v=aN3Nayvd7FU](https://www.youtube.com/watch?v=aN3Nayvd7FU)
- [https://www.youtube.com/watch?v=iLFkxAmwXF0](https://www.youtube.com/watch?v=iLFkxAmwXF0)
- [https://www.youtube.com/watch?v=IjHrwKAmGn8](https://www.youtube.com/watch?v=IjHrwKAmGn8)
- [https://www.youtube.com/watch?v=wGX3HwCTpKE](https://www.youtube.com/watch?v=wGX3HwCTpKE)
- [https://www.youtube.com/watch?v=sC1I5VsuXSk](https://www.youtube.com/watch?v=sC1I5VsuXSk)
- [https://codingo.io/tools/ffuf/bounty/2020/09/17/everything-you-need-to-know-about-ffuf.html](https://codingo.io/tools/ffuf/bounty/2020/09/17/everything-you-need-to-know-about-ffuf.html)
- [https://github.com/tamimhasan404/FFUF-Tips-And-Tricks](https://github.com/tamimhasan404/FFUF-Tips-And-Tricks)


---
## ffuf tutorial
### ffuf là gì ?
- là 1 công cụ brute force, fuzzing ứng dụng web nhằm khám phá các thư mục, file ẩn trong các ứng dụng, máy chủ web
- Để sử dụng ta cần cung cấp cho nó 1 url với 1 từ "FUZZ" và 1 danh sách từ có sẵn 
- Đầu ra của nó ta có thể thiết lập là `.json`, `.txt`,... hoặc cho nó chạy thông qua Burpsuite
- Tốc độ fuzzing của nó rất nhanh vì được viết bằng ngôn ngữ lập trình "go" và có rất nhiều tùy chọn để sử dụng
### Cách sử dụng cơ bản
#### 1. Cách dùng cơ bản
```
$ ffuf -w wordlist.txt -u https://example.com/FUZZ
```
#### 2. Sử dụng tùy chọn `recursion` để liệt kê đệ quy 
```
$ ffuf -w wordlist.txt -u https://example.com/FUZZ -recursion
```
- Tùy chọn `recursion-depth` cho ffuf biết phải thực hiện bao nhiêu hành động liệt kê đệ quy 
```
$ ffuf -w wordlist.txt -u https://example.com/FUZZ -recursion-depth 2
```
- **Note:** liệt kê đệ quy là thực hiện lại cùng 1 hành động nhưng trong 1 ngữ cảnh khác
- **Ví dụ:** fuzz url: `http://example.com/FUZZ` ta tìm được thư mục `admin`, thì nếu có sử dụng tùy chọn `recursion` thì nó sẽ lấy đường dẫn url: `http://example.com/admin/FUZZ` để tiếp tục tìm thư mục con của `admin` cho đến khi có kết quả. Giả sử ta tìm được tiếp 1 thư mục con của `admin` là `setting` thì kết quả mà ffuf trả về sẽ là `http://example.com/admin/setting`. Đó chính là liệt kê đệ quy
#### te



