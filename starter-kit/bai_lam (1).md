# BÀI LÀM – (ĐỀ LUYỆN TẬP SỐ 02)

- **Mã đề:** 02
- **Họ tên:**
- **Lớp:**
- **Link repository:**
- **Hệ điều hành (Windows/macOS):**

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```shell
PS D:\Luyen_Tap_11_9\starter-kit\rap-phim-website> pwd
PS D:\Luyen_Tap_11_9\starter-kit\rap-phim-website> ls -Force
PS D:\Luyen_Tap_11_9\starter-kit\rap-phim-website> mv .\bien-ban-ban-giao.txt .\docs\
PS D:\Luyen_Tap_11_9\starter-kit\rap-phim-website> cp .\data\ban-ve-thang-11.xlsx .\backup\
PS D:\Luyen_Tap_11_9\starter-kit\rap-phim-website\logs> Get-Content .\server.log
```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text
 Directory: D:\Luyen_Tap_11_9\starter-kit\rap-phim-website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----         11/9/2026   3:47 PM                backup
d-----         11/9/2026   3:41 PM                data
d-----         11/9/2026   3:46 PM                docs
d-----         11/9/2026   3:39 PM                evidence
d-----         11/9/2026   3:41 PM                logs
d-----         11/9/2026   3:09 PM                web
-a----         11/9/2026   3:09 PM             82 .env
-a----         11/9/2026   3:09 PM           2611 bai_lam.md

```

## 4.3. Lọc log truy cập website

### a) Lệnh lọc các dòng ERROR

```shell
PS D:\Luyen_Tap_11_9\starter-kit\rap-phim-website> Get-Content .\logs\server.log | Select-String "ERROR" > .\logs\loi_error.txt

```

### 2 dòng đầu tiên trong logs/loi_error.txt

```text
2026-11-01 09:25:40 ERROR POST /api/mua-ve
2026-11-01 09:29:11 ERROR POST /api/thanh-toan-qr


```

### b) Lệnh đếm số dòng WARNING và kết quả

```shell
PS D:\Luyen_Tap_11_9\starter-kit\rap-phim-website> (Get-Content .\logs\server.log | Select-String "WARNING").Count
```

```text
5

```

## 4.4. Chạy script tong_hop (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```shell
tong_hop.ps1
```

### Nội dung file logs/tong_hop.txt

```text
=== BAO CAO SU CO WEBSITE ===

2026-11-01 09:25:40 ERROR POST /api/mua-ve
2026-11-01 09:29:11 ERROR POST /api/thanh-toan-qr
2026-11-01 09:40:14 ERROR POST /api/mua-ve
2026-11-01 09:48:33 ERROR POST /api/giu-ghe
2026-11-01 09:52:49 ERROR POST /api/thanh-toan-qr
2026-11-01 10:05:42 ERROR POST /api/huy-ve




Count    : 5
Average  : 
Sum      : 
Maximum  : 
Minimum  : 
Property : 

```

## 4.5. README.md và bảo vệ thông tin bí mật

> README.md, .gitignore và .env.example được chấm trực tiếp trên file ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

- [x] README.md: Heading 1, mô tả có **in đậm** và _in nghiêng_, bảng, code block, task list, blockquote
- [ ] .gitignore có dòng `.env` (tên file đúng, không có đuôi .txt)
- [ ] .env.example có đủ tên biến, giá trị để trống (tên file đúng, không có đuôi .txt)

## 4.6. Kiểm tra trang web bằng DevTools (F12) và báo cáo lỗi

### Bảng lỗi

| STT | Tab DevTools phát hiện lỗi | Tên file hoặc thông báo lỗi | Cách khắc phục |
| --- | -------------------------- | --------------------------- | -------------- |
| 1   | network                     |  lỗi tên logo                           | cần sửa lại tên logo                |
| 2   |   console                       |  Uncaught ReferenceError: hienThiBangGia is not defined (anonymous) @ app.js:18                           |                | cần sửa lại tên hiển thi bang gia thành hiển thị bảng giá bán 

> Ảnh chụp màn hình lưu trong thư mục `evidence/` (network.png, console.png).

### Báo cáo lỗi gửi trưởng nhóm

- **Context: Tôi là sinh viên năm nhất chưa fix lỗi hiển thị dữ liệu của web bao giờ**
- **Expected: Bây giờ trang web xem phim của tôi muốn có đủ dữ liệu ở bảng hiển thị giao diện**
- **Actual: Dữ liệu trên trang web không có gì và tôi vào tab console thấy thông báo lỗi app.js:18 Uncaught ReferenceError: hienThiBangGia is not**
- **Log: app.js:18 Uncaught ReferenceError: hienThiBangGia is not**

### Câu tìm kiếm Google

```text
(Ghi câu tìm kiếm vào đây – xoá dòng này)

```

## 4.7. Excel

> Phần Excel được chấm trực tiếp trên file `data/ban_ve_thang_11.xlsx`, không cần ghi vào đây.


