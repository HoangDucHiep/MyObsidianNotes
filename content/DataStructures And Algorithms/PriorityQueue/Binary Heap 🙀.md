---
title: Binary Heap 🙀
tags:
  - Datastructure-and-Algorithm
---
### Binary Heap là gì?
> Binary Heap là một [[Binary Tree 🌱| Cây nhị phân]], với giá trị của mỗi node ***không nhỏ hơn*** giá trị các node con của nó  
![[Heap.svg]]
### Binary Heap dùng mảng
- Có thể đảm bảo được nó sẽ luôn cân bằng => Từ đó đảm bảo được cost cao nhất là $O(log(n))$
- Khi sử dụng based-0, ta có đặc điểm sau:
	- Parent = $\lfloor \frac{i - 1}{2} \rfloor$
	- Left Child = $2\times i + 1$
	- Right Child = $2\times i + 2$
		![[Drawing 2024-10-12 11.59.44.excalidraw 1.svg]]