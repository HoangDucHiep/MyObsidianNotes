---
title: Priority Queue
tags:
  - Datastructure-and-Algorithm
---
### Priority Queue là gì?
- Là một cấu trúc danh sách (Tương tư Queue và Stack), nhưng mỗi phần tử của nó được gán với một Priority (Độ ưu tiên). 
- Trong PQ, phần của nào có độ ưu tiên cao hơn sẽ được phục vụ trước![[Introduction.webp]]
### Tạo PQ với [[Binary Heap 🙀]]
- Ví dụ với MaxPQ
##### Các thao tác
- GetMax: Trả về phần tử có độ ưu tiên cao nhất trong PQ
	- Trả về phần tử đầu tiên![[Excalidraw/Drawing 2024-10-12 11.59.44.excalidraw.svg]]
- SiftUp: Đẩy phần tử lên trên tới khi đúng vị trí hợp lệ
	- So sánh phần tử thứ i với cha của nó, nếu phần tử cha nhỏ hơn phần tử i, đổi chỗ chúng cho nhau
	- Set i tới phần tử cha
	- Tiếp tục lặp đến khi phần tử cha đảm bảo không nhỏ hơn phần tử con![[Excalidraw/Drawing 2024-10-12 11.59.44.excalidraw.svg]]
- SiftDown: Đẩy phần tử xuống dưới tới khi đúng vị trí hợp lệ
	
- Insert: Thêm phần tử mới vào PQ
- ExtractMax: Trả về và xóa phần tử có độ ưu tiên cao nhất
- ChangePriority: Thay đổi độ ưu tiên của phần tử
- Remove: Xóa phần tử khỏi PQ