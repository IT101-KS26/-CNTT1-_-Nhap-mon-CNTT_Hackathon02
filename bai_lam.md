# BÀI LÀM – HACKATHON 02

- **Mã đề:** 01
- **Họ tên:** DƯƠNG CÔNG QUỐC
- **Lớp:** CNTT1
- **Link repository:**
- **Hệ điều hành (Windows/macOS):**

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```shell
pwd
ls -Force
mv .\Ghi_Chu_Ban_Giao.txt docs
mkdir backup
 cp .\data\Ban_Ve_Thang_1.xlsx backup
  rm *.tmp
   cd .\logs\
   ls 
   cd ..


```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text

    Directory: D:\starter-kit\starter-kit\ho-boi-website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        11/11/2026   7:59 AM                backup
d-----        11/11/2026   7:55 AM                data
d-----        11/11/2026   7:57 AM                docs
d-----        11/11/2026   7:51 AM                evidence
d-----        11/11/2026   7:55 AM                logs
d-----        11/11/2026   7:55 AM                web
-a----         11/3/2026   7:06 AM             74 .env
-a----         11/3/2026   7:06 AM           2407 bai_lam.md


    Directory: D:\starter-kit\starter-kit\ho-boi-website\backup


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/3/2026   7:06 AM           6106 Ban_Ve_Thang_1.xlsx


    Directory: D:\starter-kit\starter-kit\ho-boi-website\data


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/3/2026   7:06 AM           6106 Ban_Ve_Thang_1.xlsx


    Directory: D:\starter-kit\starter-kit\ho-boi-website\docs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/3/2026   7:06 AM            158 Ghi_Chu_Ban_Giao.txt


    Directory: D:\starter-kit\starter-kit\ho-boi-website\logs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/3/2026   7:06 AM            972 Visit.log


    Directory: D:\starter-kit\starter-kit\ho-boi-website\web


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        11/11/2026   7:55 AM                images
-a----         11/3/2026   7:06 AM            574 app.js
-a----         11/3/2026   7:06 AM            507 index.html
-a----         11/3/2026   7:06 AM            460 style.css


    Directory: D:\starter-kit\starter-kit\ho-boi-website\web\images


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/3/2026   7:06 AM           3061 logo-aquazone.png


```

## 4.3. Lọc log truy cập website

### a) Lệnh lọc các dòng status=500

```shell
Select-String "status=500" .\logs\Visit.log > .\logs\loi_500.txt

```

### 2 dòng đầu tiên trong logs/loi_500.txt

```text
logs\Visit.log:8:2026-01-28 08:24:34 POST /api/thanh-toan status=500
logs\Visit.log:9:2026-01-28 08:28:45 POST /api/thanh-toan status=500

```

### b) Lệnh đếm số dòng status=404 và kết quả

```shell
 (Get-Content .\logs\Visit.log | Select-String "status=404").Count

```

```text
4

```

## 4.4. Chạy script tong_hop (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```shell
@'
>> # script: tong_hop.ps1
>> # Tac gia: Duong Cong Quoc
>> # Ngay tao: 11/11/2026
>> Write-Host "Dang tao bao cao..."
>> "=== BAO CAO SU CO WEBSITE ===" > logs/tong_hop.txt
>> Get-Content logs/visit.log | Select-String "status=404" >>logs/tong_hop.txt
>> Get-Content logs/visit.log | Select-String "status=500" | Measure-Object >> logs/tong_hop.txt
>> Write-Host "Hoan thanh!"
>> '@ | Set-Content .\tong_hop.ps1

 Set -ExecutionPolicy _Scope Process -ExcutionPolicy Bypass
```

### Nội dung file logs/tong_hop.txt

```text


```

## 4.5. README.md và bảo vệ thông tin bí mật

> README.md, .gitignore và .env.example được chấm trực tiếp trên file ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

- [ ] README.md: Heading 1, mô tả có **in đậm** và *in nghiêng*, bảng, code block, task list, blockquote
- [ ] .gitignore có dòng `.env` (tên file đúng, không có đuôi .txt)
- [ ] .env.example có đủ tên biến, giá trị để trống (tên file đúng, không có đuôi .txt)

## 4.6. Kiểm tra trang web bằng DevTools (F12) và báo cáo lỗi

### Bảng lỗi

| STT | Tab DevTools phát hiện lỗi | Tên file hoặc thông báo lỗi | Cách khắc phục |
| --- | --- | --- | --- |
| 1 |  |  |  |
| 2 |  |  |  |

> Ảnh chụp màn hình lưu trong thư mục `evidence/` (network.png, console.png).

### Báo cáo lỗi gửi trưởng nhóm

- **Context:** 
- **Expected:** 
- **Actual:** 
- **Log:** 

### Câu tìm kiếm Google

```text
(Ghi câu tìm kiếm vào đây – xoá dòng này)

```

## 4.7. Excel

> Phần Excel được chấm trực tiếp trên file `data/ban_ve_thang_1.xlsx`, không cần ghi vào đây.
