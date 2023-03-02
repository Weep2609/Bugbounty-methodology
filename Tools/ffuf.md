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
- Là 1 công cụ brute force, fuzzing ứng dụng web nhằm khám phá các thư mục, file ẩn trong các ứng dụng, máy chủ web
- Để sử dụng ta cần cung cấp cho nó 1 url với 1 từ "FUZZ" và 1 danh sách từ có sẵn 
- Đầu ra của nó ta có thể thiết lập là `.json`, `.txt`,... hoặc cho nó chạy thông qua Burpsuite
- Tốc độ fuzzing của nó rất nhanh vì được viết bằng ngôn ngữ lập trình "go" và có rất nhiều tùy chọn để sử dụng
### Cách sử dụng cơ bản
#### 1. Cách dùng cơ bản
```
$ ffuf -w wordlist.txt -u https://example.com/FUZZ
```
#### 2. Sử dụng tùy chọn `-recursion` để liệt kê đệ quy 
```
$ ffuf -w wordlist.txt -u https://example.com/FUZZ -recursion
```
- Tùy chọn `-recursion-depth` cho ffuf biết phải thực hiện bao nhiêu hành động liệt kê đệ quy 
```
$ ffuf -w wordlist.txt -u https://example.com/FUZZ -recursion-depth 2
```
- **Note:** liệt kê đệ quy là thực hiện lại cùng 1 hành động nhưng trong 1 ngữ cảnh khác
- **Ví dụ:** fuzz url: `http://example.com/FUZZ` ta tìm được thư mục `admin`, thì nếu có sử dụng tùy chọn `recursion` thì nó sẽ lấy đường dẫn url: `http://example.com/admin/FUZZ` để tiếp tục tìm thư mục con của `admin` cho đến khi có kết quả. Giả sử ta tìm được tiếp 1 thư mục con của `admin` là `setting` thì kết quả mà ffuf trả về sẽ là `http://example.com/admin/setting`. Đó chính là liệt kê đệ quy
#### 3. Tìm các file với phần mở rộng được chỉ định bằng tùy chọn `-e`
```
$ ffuf -u https://example.com/FUZZ -w ./wordlist -recursion -e .php
```
#### 4. Fuzz nhiều vị trí với nhiều danh sách từ có sẵn
- Theo mặc định ffuf sẽ tìm kiếm một ví trí duy nhất thông qua từ khóa `FUZZ` tuy nhiên ta có thể chỉ định 1 từ khóa khác bằng cách như sau
```
$ ffuf -w wordlist.txt:F1 -u http://example.com/F1
```
- Để chỉ định fuzz nhiều vị trí với nhiều danh sách từ ta sẽ thêm nối thêm 1 danh sách từ khác vào dối số của tùy chọn `-w`
```
$ ffuf -w ./wordlist1.txt:F1,./wordlist2.txt:F2 -u http://example.com/F1/F2
```



