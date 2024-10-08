---
date: 2024-10-02T14:30
tags:
  - Datastructure-and-Algorithm
cssclasses:
  - center-images
---
## <span style="color:rgb(112, 48, 160)">Định nghĩa</span>
- <mark style="background: #D2B3FFA6;">Armotized analysis</mark> là phương pháp phân tích chi phí của <mark style="background: #D2B3FFA6;">một thao tác</mark> trong một <mark style="background: #D2B3FFA6;">chuỗi <span style="color:rgb(112, 48, 160)">n</span> các operations</mark> và bằng tổng chi phí chia cho <span style="color:rgb(112, 48, 160)">n</span>
- Ví dụ: nếu có 100 operations với cost 1 sau đó là 1 operation có cost là 100, thì armotized cost với mỗi operation trong chuỗi là $200 / 101 < 2$.
## <span style="color:rgb(112, 48, 160)">Tại sao ta cần quan tâm đến Amortized</span> 😒 
- Lý do ta quan tâm đến amortized cost là ta có thể đánh giá chính xác hơn về tính hiệu quả như của một data structure khi nó có những operation để điều chỉnh lại trạng thái của nó, etc.. có chi phí rất lớn, nhưng lại không thực thi thường xuyên. Khi đó ta armotized analysis sẽ cho ta khoảng chi phí chính xác hơn khi sử dụng DS đó hơn là chỉ nhìn vào ***worst-case*** của ***một operation***.
## <span style="color:rgb(112, 48, 160)">Aggregate Analysis</span>
- Là một trong các cách để thực hiện Armotized Analysis
- Có 2 bước
	1. Chứng minh được chuỗi n operation tốn T(n)
	2. Khi đó mỗi operation sẽ tốn trung bình là $\frac{T(n)}{n}$
- Nhưng khi dùng Aggregate analysis, các operation phải có ***<span style="color:rgb(112, 48, 160)">cùng cost</span>***
## <span style="color:rgb(112, 48, 160)">Ví dụ</span>
- Tạo Stack bằng Array
	- Để push(x), ta chỉ cần
		``` c
			A[top] = x;
			top++;
		```
	- Để pop():
		``` c
			//...something above...
			top--;
			x = A[top]
			//..return, .. any things ....
		```
	- Vậy với push(x), và pop(x), ta chỉ cần cost là 1
	- Nhưng nếu mảng A đầy, khi đó để push, ta cần phải resize (ở đây ta sẽ gấp đôi kích thước mảng - tạo một mảng mới, copy, …) 
	- Khi đó, cost của resize sẽ là n, và push khi này sẽ có worst-case là O(n)
	- Nhưng khi ta dùng armotized analysis cho n lần push thì:
		- Sẽ gồm n lần thêm (thêm vào mảng) và n lần resize
		- Total cost của n lần resize là là:
			$$
				1 + 2 + 4 + ... + 2^i \leq 2n - 1
			 $$
			với $2^i < n$.
		- Cộng với cost của n lần thêm là n
		- Vậy total cost sẽ < 3n
		- Khi đó amortized cost của từng operation là < 3
## <span style="color:rgb(112, 48, 160)">Tu bi căn tì niu !!</span>
