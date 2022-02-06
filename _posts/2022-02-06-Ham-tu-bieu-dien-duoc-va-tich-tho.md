---
layout: post
title: "Hàm tử biểu diễn được và tích thớ"
author: "Doãn Quang Tiến"
categories: 
tag: [algebraic geometry, representable functor, fibre product]
---

Hôm nay, mình sẽ giới thiệu về việc xây dựng tích trực tiếp và tích thớ bằng ngôn ngữ phạm trù, sử dụng hàm tử biểu diễn được. Mục tiêu của bài viết là hướng đến việc chỉ ra sự tồn tại của tích thớ trong phạm trù lược đồ $\textbf{Sch}$.<br>
**1. Hàm tử biểu diễn được**<br>
Trước tiên, ta sẽ đi xem xét hàm tử cảm sinh từ một vật trong phạm trù.
<blockquote>
**Định nghĩa** (Hàm tử cảm sinh bởi một vật trong phạm trù) Xét một vật $W$ trong phạm trù $\mathcal{C}$, ta định nghĩa
<center>
    $h_W\left ( X \right ):=\operatorname{Hom}_{\mathcal{C}}\left ( X,W \right ),\quad X\in\operatorname{Ob}\left ( \mathcal{C} \right ).$
 </center>
Khi đó, với mọi cấu xạ $f\in\operatorname{Hom}_{\mathcal{C}}\left ( X,Y \right )$ và $g\in\operatorname{Hom}_{\mathcal{C}}\left ( Y,W \right )=h_W\left ( Y \right )$, ta định nghĩa
<center>
    $h_W\left ( f \right )\left ( g \right )=g\circ f\quad\text{thì ta thu được}\quad g\circ f\in \operatorname{Hom}_{\mathcal{C}}\left ( X,W \right )=h_W\left ( X \right ),$
</center>
hay ta có cấu xạ được xác định bởi
<center>
    \begin{align*}
    h_W\left ( f \right ):h_W\left ( Y \right )&\longrightarrow h_W\left ( X \right )\\
g&\mapsto h_W\left ( f \right )\left ( g \right )=g\circ f
\end{align*}
</center>
</blockquote>









 
