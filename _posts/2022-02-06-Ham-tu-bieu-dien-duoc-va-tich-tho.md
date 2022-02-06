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
<strong> Định nghĩa </strong>(Hàm tử cảm sinh bởi một vật trong phạm trù) Xét một vật $W$ trong phạm trù $\mathcal{C}$, ta định nghĩa
    \[h_W\left ( X \right ):=\operatorname{Hom}_{\mathcal{C}}\left ( X,W \right ),\quad X\in\operatorname{Ob}\left ( \mathcal{C} \right ).\]
Khi đó, với mọi cấu xạ $f\in\operatorname{Hom}_{\mathcal{C}}\left ( X,Y \right )$ và $g\in\operatorname{Hom}_{\mathcal{C}}\left ( Y,W \right )=h_W\left ( Y \right )$, ta định nghĩa
    $$h_W\left ( f \right )\left ( g \right )=g\circ f\quad\text{thì ta thu được}\quad g\circ f\in \operatorname{Hom}_{\mathcal{C}}\left ( X,W \right )=h_W\left ( X \right ),$$
hay ta có cấu xạ được xác định bởi
\begin{align*}
    h_W\left ( f \right ):h_W\left ( Y \right )&\longrightarrow h_W\left ( X \right )\\
g&\mapsto h_W\left ( f \right )\left ( g \right )=g\circ f
\end{align*}
</blockquote>
Điều này dẫn đến $$h_W\left ( f \right )=\operatorname{Hom}_{\mathbf{Set}}\left ( h_W\left ( Y \right ),h_W\left ( X \right ) \right )$$, hay từ đây ta thu được $h_W$ là hàm tử phản biến từ phạm trù $\mathcal{C}$ vào phạm trù tập hợp $\textbf{Set}$.<br>
Một câu hỏi cơ bản được đặt ra như sau: khi một hàm tử phản biến $F:\mathcal{C}\rightarrow \mathbf{Set}$ được xác định, liệu có tồn tại một vật $W\in\operatorname{Ob}(\mathcal{C})$ thỏa mãn $h_W$ đẳng cấu hàm tử với $F$ hay không? Nghĩa là, với mọi vật $X\in\operatorname{Ob}(\mathcal{C})$, có tồn tại vật $W\in\operatorname{Ob}(\mathcal{C})$ thỏa mãn
$$\varphi_X:F\left ( X \right )\overset{\sim }{\longrightarrow}h_W\left ( X \right ),$$
là một phép đẳng cấu giữa các tập hợp và thỏa mãn với mỗi cấu xạ $f\in\operatorname{Hom}\left ( X_1,X_2 \right )$ thì sơ đồ sau
    \begin{tikzcd}
F(X_2) \arrow[d, "F\left ( f \right )"'] \arrow[r, "\varphi_{X_2}"] & h_W(X_2) \arrow[d, "h_W\left ( f \right )"] \\
F(X_1) \arrow[r, "\varphi_{X_1}"']                                  & h_W(X_1)                                   
\end{tikzcd}
có giao hoán hay không? Nếu vật $W$ tồn tại, thì đẳng cấu $$\varphi_W:F\left ( W \right )\overset{\sim }{\longrightarrow}h_W\left ( W \right )$$ xác định duy nhất một phần tử $\psi\in F\left ( W \right )$ thỏa mãn $$\varphi_W\left ( \psi \right )=\operatorname{id}_W\in h_W\left ( W \right )$$. Ta sẽ chứng minh $\left ( W,\psi \right )$ xác định $F$ khi $F$ và $h_W$ đẳng cấu theo nghĩa hàm tử. Với vật $X\in\operatorname{Ob}(\mathcal{C})$ bất kì, ta chọn phần tử $$h\in h_W\left ( X \right )=\operatorname{Hom}_{\mathcal{C}}\left ( X,W \right )$$, khi đó thì ta thu được $$F\left ( h \right )\left ( \psi \right )\in F\left ( X \right )$$. Từ sơ đồ giao hoán
\begin{tikzcd}
F(W) \arrow[d, "F\left ( h \right )"'] \arrow[r, "\varphi_{W}"] & h_W(W) \arrow[d, "h_W\left ( h \right )"] \\
F(X) \arrow[r, "\varphi_{X}"']                                  & h_W(X)                                   
\end{tikzcd}
dẫn đến $$\varphi_X\left ( F\left ( h \right )\left ( \psi \right ) \right )=h$$. Lại từ việc $\varphi_X$ là một phép đẳng cấu theo nghĩa tập hợp, $$\varphi_X\left ( F\left ( h \right )\left ( \psi \right ) \right )=h$$ , nghĩa là
$$F\left ( X \right )=\left \{ F\left ( h \right )\left ( \psi \right )\mid h\in h_W\left ( W \right ) \right \}.$$
Do đó, nếu $F\simeq h_W$ đẳng cấu hàm tử thì $F$ được biểu diễn bởi $\left ( W,\psi \right )$, nghĩa là $F$ biểu diễn được. Từ đây, ta có định nghĩa cụ thể của hàm tử biểu diễn được, phát biểu như sau
\[\begin{tikzcd}
	\bullet & \bullet \\
	\bullet
	\arrow[from=2-1, to=1-2]
	\arrow[from=1-1, to=1-2]
	\arrow[from=1-1, to=2-1]
\end{tikzcd}\]






 
