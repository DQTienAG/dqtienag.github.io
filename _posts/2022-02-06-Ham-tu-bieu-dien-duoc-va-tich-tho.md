---
layout: post
title: "Hàm tử biểu diễn được và tích thớ"
author: "Doãn Quang Tiến"
categories: 
tag: [algebraic geometry, representable functor, fibre product]
---

Hôm nay, mình sẽ giới thiệu về việc xây dựng tích trực tiếp và tích thớ bằng ngôn ngữ phạm trù, sử dụng hàm tử biểu diễn được. Mục tiêu của bài viết là hướng đến việc chỉ ra sự tồn tại của tích thớ trong phạm trù lược đồ $\textbf{Sch}$.
**# Hàm tử biểu diễn được**
Trước tiên, ta sẽ đi xem xét hàm tử cảm sinh từ một vật trong phạm trù.
> **Định nghĩa** (Hàm tử cảm sinh bởi một vật trong phạm trù) Xét một vật \(W\) trong phạm trù \(\mathcal{C}\), ta định nghĩa
\[h_W\left ( X \right )\coloneqq\operatorname{Hom}_{\mathcal{C}}\left ( X,W \right ),\enskip X\in\operatorname{Ob}\left ( \mathcal{C} \right ).\]
Khi đó, với mọi cấu xạ \(f\in\operatorname{Hom}_{\mathcal{C}}\left ( X,Y \right )\) và \(g\in\operatorname{Hom}_{\mathcal{C}}\left ( Y,W \right )=h_W\left ( Y \right )\), ta định nghĩa
\[h_W\left ( f \right )\left ( g \right )=g\circ f\enskip\text{thì ta thu được}\enskip g\circ f\in \operatorname{Hom}_{\mathcal{C}}\left ( X,W \right )=h_W\left ( X \right ),\]
hay ta có cấu xạ được xác định bởi
\begin{align*}
    h_W\left ( f \right ):h_W\left ( Y \right )&\longrightarrow h_W\left ( X \right )\\
g&\mapsto h_W\left ( f \right )\left ( g \right )=g\circ f
\end{align*}











 
