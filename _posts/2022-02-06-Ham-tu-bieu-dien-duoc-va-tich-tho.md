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

\begin{tikzpicture}[x=0.75pt,y=0.75pt,yscale=-1,xscale=1]
%uncomment if require: \path (0,500); %set diagram left start at 0, and has height of 500

%Straight Lines [id:da9113020489637684] 
\draw    (225.4,270.41) -- (510.13,270.41) ;
%Shape: Ellipse [id:dp3392702706151973] 
\draw  [fill={rgb, 255:red, 0; green, 0; blue, 0 }  ,fill opacity=1 ] (363.41,270.02) .. controls (363.41,266.82) and (366.01,264.23) .. (369.21,264.23) .. controls (372.4,264.23) and (375,266.82) .. (375,270.02) .. controls (375,273.22) and (372.4,275.81) .. (369.21,275.81) .. controls (366.01,275.81) and (363.41,273.22) .. (363.41,270.02) -- cycle ;
%Shape: Ellipse [id:dp8286278282885116] 
\draw  [fill={rgb, 255:red, 0; green, 0; blue, 0 }  ,fill opacity=1 ] (222.1,163.46) .. controls (222.1,160.26) and (224.69,157.67) .. (227.89,157.67) .. controls (231.09,157.67) and (233.68,160.26) .. (233.68,163.46) .. controls (233.68,166.66) and (231.09,169.25) .. (227.89,169.25) .. controls (224.69,169.25) and (222.1,166.66) .. (222.1,163.46) -- cycle ;
%Shape: Ellipse [id:dp04922743192991841] 
\draw  [fill={rgb, 255:red, 0; green, 0; blue, 0 }  ,fill opacity=1 ] (458.4,129.48) .. controls (458.4,126.28) and (460.99,123.69) .. (464.19,123.69) .. controls (467.39,123.69) and (469.98,126.28) .. (469.98,129.48) .. controls (469.98,132.68) and (467.39,135.27) .. (464.19,135.27) .. controls (460.99,135.27) and (458.4,132.68) .. (458.4,129.48) -- cycle ;
%Straight Lines [id:da30985383230321517] 
\draw    (227.89,163.46) -- (369.21,270.02) ;
%Straight Lines [id:da961743527018762] 
\draw    (464.19,129.48) -- (369.21,270.02) ;
%Straight Lines [id:da7326945722218143] 
\draw  [dash pattern={on 4.5pt off 4.5pt}]  (369.21,169.38) -- (369.21,270.02) ;
%Straight Lines [id:da4481609532364128] 
\draw    (369.21,270.02) -- (283.65,205.4) ;
\draw [shift={(282.05,204.2)}, rotate = 37.06] [color={rgb, 255:red, 0; green, 0; blue, 0 }  ][line width=0.75]    (10.93,-4.9) .. controls (6.95,-2.3) and (3.31,-0.67) .. (0,0) .. controls (3.31,0.67) and (6.95,2.3) .. (10.93,4.9)   ;
%Straight Lines [id:da15300882968619978] 
\draw    (369.21,270.02) -- (420.73,193.6) ;
\draw [shift={(421.84,191.94)}, rotate = 123.99] [color={rgb, 255:red, 0; green, 0; blue, 0 }  ][line width=0.75]    (10.93,-4.9) .. controls (6.95,-2.3) and (3.31,-0.67) .. (0,0) .. controls (3.31,0.67) and (6.95,2.3) .. (10.93,4.9)   ;

% Text Node
\draw (353.5,283.6) node [anchor=north west][inner sep=0.75pt]  [font=\Large]  {$M$};
% Text Node
\draw (216.62,126.52) node [anchor=north west][inner sep=0.75pt]  [font=\Large]  {$A$};
% Text Node
\draw (456.14,92.46) node [anchor=north west][inner sep=0.75pt]  [font=\Large]  {$B$};
% Text Node
\draw (347.37,220.76) node [anchor=north west][inner sep=0.75pt]  [font=\Large]  {$i$};
% Text Node
\draw (377.22,215.49) node [anchor=north west][inner sep=0.75pt]  [font=\Large]  {$r$};
% Text Node
\draw (280.62,168.52) node [anchor=north west][inner sep=0.75pt]  [font=\Large]  {$\vec T_{1}$};
% Text Node
\draw (395.72,153.88) node [anchor=north west][inner sep=0.75pt]  [font=\Large]  {$\vec T_{2}$};


\end{tikzpicture}





 
