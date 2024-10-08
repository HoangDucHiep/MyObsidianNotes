---
date: 2024-10-01T14:40
tags:
  - "#asp"
cssclasses:
  - center-images
---
#### Cài đặt các Package cần thiết
- Microsoft.Entity.FrameworkCore.
- Microsoft.Entity.FrameworkCore.SqlServer
- Microsoft.Entity.FrameworkCore.Tools
#### Lấy Connection String
- Connection string có dạng:
``` shell
Data Source=HOANGHIEP\SQLEXPRESS;Initial Catalog=QLBanVaLi;Integrated Security=True;Trust Server Certificate=True
```
#### Dụng lệnh scaffold
``` shell
Scaffold-DbContext " <connection string> " Microsoft.EntityFrameworkCore.SqlServer -OutputDir Models
```
- Chạy lệnh trong <mark style="background: #FFB8EBA6;">Package Manager Console</mark>
