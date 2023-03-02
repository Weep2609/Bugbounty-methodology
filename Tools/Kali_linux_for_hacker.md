## Tham khảo thêm
- [https://www.youtube.com/watch?v=lZAoFs75_cs](https://www.youtube.com/watch?v=lZAoFs75_cs)
- linux basics for hackers [PDF](https://gateway.ipfs.io/ipfs/bafykbzacedofnv75jtjg7f5t6vbql4y6ccojzwwxm2zacxbfik5difwdcd6di?filename=OcuppyTheWeb%20-%20Linux%20Basics%20for%20Hackers-No%20Starch%20Press%20%282019%29.pdf)
- Kali linux hacking [epub](https://cloudflare-ipfs.com/ipfs/bafykbzacechy2iliyiidhwuzsfnhzu2tfow7fwexxllb4gvia6yebbtiiqe66?filename=Ethem%20Mining%20-%20Kali%20Linux%20Hacking_%20A%20Complete%20Step%20by%20Step%20Guide%20to%20Learn%20the%20Fundamentals%20of%20Cyber%20Security%2C%20Hacking%2C%20and%20Penetration%20Testing.%20Includes%20Valuable%20Basic%20Networking%20Concepts-Independentl.epub)
- Kali Linux Penetration Testing Bible

---
## Các lệnh cơ bản
1. `pwd` sẽ hiển thị đường đẫn thư mục hiện tại
```
$ pwd
/home/kali
```
2. `cd` sẽ di chuyển đến đường dẫn mục tiêu. Sử dụng `cd ..` để lùi lại 1 thư mục
```
kali@kali ~
$ cd /usr/bin
kali@kali /usr/bin 
$ cd ..
kali@kali /usr
```
- **Note**: / là thư mục gốc
3. `ls` sẽ liệt kê tất cả file và thư mục trong thư mục hiện tại. Tìm tất cả file ẩn với `ls -la`
```
$ ls 
Music  Downloads  test.txt
$ ls -la
Music  Downloads  test.txt .bin .source
```
4. `mkdir` để tạo 1 thư mục mới, `rmdir` để xóa 1 thư mục trống
```
$ mkdir subdomain
$ ls
subdomain
$ rmdir subdomain
$ ls

```
5. `cp` để copy 1 file, `rm` để xóa file, `mv` để di chuyển file sang 1 đường dẫn khác, `locate` để tìm vị trí đường dẫn của file
```
$ cat > test.txt
hello guy
$ ls 
test.txt
$ mkdir folder
$ ls
test.txt  folder
$ cp test.txt folder # <----- sao chép file test.txt sang thư mục folder
$ ls folder
test.txt
$ rm test.txt # <----- xóa file test.txt
$ ls
folder
$ mv ./folder/test.txt ./folder/test123.txt # <----- Nếu dùng lệnh mv với 1 file mà không thay đổi đường dẫn cho đối số thứ hai thì nó sẽ đổi tên file
$ ls folder
test123.txt
$ mv ./folder/test123.txt /usr/bin # <----- Di chuyển file sang 1 đường dẫn khác
$ ls

$ ls /usr/bin
...  test123.txt
$ locate test123.txt # <----- định vị vị trí file hiện tại
/usr/bin/test123.txt
```
6. `updatedb` sẽ cập nhật lại cơ sở dữ liệu các đường dẫn trong hệ thống
7. `passwd` sẽ đổi password của user
```
$ updatedb
$ passwd
Enter new UNIX password:
Retype new UNIX password:
password: password update successfully
```
8. `man` dùng để mở bảng hướng dẫn sử dụng từng lệnh cụ thể trong unix. Để thoát ra ta ấn phím "q"
```
$ man ls # <----- mở bảng hướng dẫn dùng lệnh ls
LS(1)                                                            User Commands                                                            LS(1)

NAME
       ls - list directory contents

SYNOPSIS
       ls [OPTION]... [FILE]...
...
```
<span color='red'>test</span>


