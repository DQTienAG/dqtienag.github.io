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
<center>
    $$\varphi_X:F\left ( X \right )\overset{\sim }{\longrightarrow}h_W\left ( X \right ),$$
</center>
là một phép đẳng cấu giữa các tập hợp và thỏa mãn với mỗi cấu xạ $f\in\operatorname{Hom}\left ( X_1,X_2 \right )$ thì sơ đồ sau
<center>
    <!-- https://q.uiver.app/?q=WzAsNCxbMCwwLCJGKFhfMikiXSxbMSwwLCJoX1coWF8yKSJdLFswLDEsIkYoWF8xKSJdLFsxLDEsImhfVyhYXzEpIl0sWzAsMSwiXFx2YXJwaGlfe1hfMn0iXSxbMCwyLCJGKGYpIiwyXSxbMSwzLCJoX1coZikiXSxbMiwzLCJcXHZhcnBoaV97WF8xfSIsMl1d -->
<iframe class="quiver-embed" src="https://q.uiver.app/?q=WzAsNCxbMCwwLCJGKFhfMikiXSxbMSwwLCJoX1coWF8yKSJdLFswLDEsIkYoWF8xKSJdLFsxLDEsImhfVyhYXzEpIl0sWzAsMSwiXFx2YXJwaGlfe1hfMn0iXSxbMCwyLCJGKGYpIiwyXSxbMSwzLCJoX1coZikiXSxbMiwzLCJcXHZhcnBoaV97WF8xfSIsMl1d&embed" width="370" height="304" style="border-radius: 8px; border: none;"></iframe>
</center>
có giao hoán hay không? Nếu vật $W$ tồn tại, thì đẳng cấu $$\varphi_W:F\left ( W \right )\overset{\sim }{\longrightarrow}h_W\left ( W \right )$$ xác định duy nhất một phần tử $\psi\in F\left ( W \right )$ thỏa mãn $$\varphi_W\left ( \psi \right )=\operatorname{id}_W\in h_W\left ( W \right )$$. Ta sẽ chứng minh $\left ( W,\psi \right )$ xác định $F$ khi $F$ và $h_W$ đẳng cấu theo nghĩa hàm tử. Với vật $X\in\operatorname{Ob}(\mathcal{C})$ bất kì, ta chọn phần tử $$h\in h_W\left ( X \right )=\operatorname{Hom}_{\mathcal{C}}\left ( X,W \right )$$, khi đó thì ta thu được $$F\left ( h \right )\left ( \psi \right )\in F\left ( X \right )$$. Từ sơ đồ giao hoán
<center>
    <!-- https://q.uiver.app/?q=WzAsNCxbMCwwLCJGKFcpIl0sWzEsMCwiaF9XKFcpIl0sWzAsMSwiRihYKSJdLFsxLDEsImhfVyhYKSJdLFswLDEsIlxcdmFycGhpX3tXfSJdLFswLDIsIkYoaCkiLDJdLFsxLDMsImhfVyhoKSJdLFsyLDMsIlxcdmFycGhpX3tYfSIsMl1d -->
<iframe class="quiver-embed" src="https://q.uiver.app/?q=WzAsNCxbMCwwLCJGKFcpIl0sWzEsMCwiaF9XKFcpIl0sWzAsMSwiRihYKSJdLFsxLDEsImhfVyhYKSJdLFswLDEsIlxcdmFycGhpX3tXfSJdLFswLDIsIkYoaCkiLDJdLFsxLDMsImhfVyhoKSJdLFsyLDMsIlxcdmFycGhpX3tYfSIsMl1d&embed" width="361" height="304" style="border-radius: 8px; border: none;"></iframe>
</center>
dẫn đến $$\varphi_X\left ( F\left ( h \right )\left ( \psi \right ) \right )=h$$. Lại từ việc $\varphi_X$ là một phép đẳng cấu theo nghĩa tập hợp, $$\varphi_X\left ( F\left ( h \right )\left ( \psi \right ) \right )=h$$ , nghĩa là
<center>
    $$F\left ( X \right )=\left \{ F\left ( h \right )\left ( \psi \right )\mid h\in h_W\left ( W \right ) \right \}.$$
</center>
Do đó, nếu $F\simeq h_W$ đẳng cấu hàm tử thì $F$ được biểu diễn bởi $\left ( W,\psi \right )$, nghĩa là $F$ biểu diễn được. Từ đây, ta có định nghĩa cụ thể của hàm tử biểu diễn được, phát biểu như sau
<blockquote>
    <strong> Định nghĩa </strong>(Hàm tử biểu diễn được) Cho hàm tử phản biến \(F:\mathcal{C}\rightarrow \mathbf{Set}\), khi đó ta nói hàm tử \(F\) biểu diễn được nếu tồn tại một vật \(W\) trong phạm trù \(\mathcal{C}\), nghĩa là \(W\in\operatorname{Ob}(\mathcal{C})\) sao cho \(F\simeq h_W\), đẳng cấu theo nghĩa hàm tử và \(h_W\) là hàm tử cảm sinh bởi vật \(W\) trong \(\mathcal{C}\).
</blockquote>
Tiếp theo, để trả lời cho câu hỏi trên, ta sẽ đến với một bổ đề quan trọng của hàm tử biểu diễn được.
<blockquote> 
    <strong> Bổ đề 1.1. </strong> Khi một hàm tử phản biến \(F:\mathcal{C}\rightarrow \mathbf{Set}\) biểu diễn được, thì cặp \(\left ( W,\psi \right )\), trong đó \(W\in\operatorname{Ob}(\mathcal{C}),\psi\in F(W)\), được xác định một cách duy nhất, sai khác một đẳng cấu.
</blockquote>
**Chứng minh.** Ta giả sử có cặp $$\left ( \widetilde{W},\widetilde{\psi} \right )$$ biểu diễn hàm tử $F$, khi đó tồn tại các đẳng cấu $$\varphi:F\rightarrow h_W$$ và $$\widetilde{\varphi}:F\rightarrow h_{\widetilde{W}}$$ thỏa mãn $$\varphi_W\left ( \psi \right )=\operatorname{id}_W$$ và $$\widetilde{\varphi}_{\widetilde{W}}\left ( \widetilde{\psi} \right )=\operatorname{id}_{\widetilde{W}}$$. Từ đây, ta có các đẳng cấu theo nghĩa tập hợp như sau
<center>
    $$\varphi_{\widetilde{W}}:F\left ( \widetilde{W} \right )\overset{\sim }{\longrightarrow}h_W\left ( \widetilde{W} \right ),\quad \widetilde{\varphi}_{W}:F\left ( W \right )\overset{\sim }{\longrightarrow}h_{\widetilde{W}}\left ( W \right ),$$
</center>
và ta xác định được các cấu xạ dưới đây
<center>
    $$\eta=\varphi_{\widetilde{W}}\left ( \widetilde{\psi} \right ):\widetilde{W}\longrightarrow W,\quad \widetilde{\eta}=\widetilde{\varphi}_{W}\left ( \psi \right ):W\longrightarrow \widetilde{W}.$$
</center>
Ta sẽ chứng minh $$\eta\circ \widetilde{\eta}=\operatorname{id}_W$$ và $$\widetilde{\eta}\circ\eta =\operatorname{id}_{\widetilde{W}}$$, và ta cũng có $$F\left ( \eta \right )\left ( \psi \right )=\widetilde{\psi}$$ và $$F\left ( \widetilde{\eta} \right )\left ( \widetilde{\psi} \right )=\psi$$. Từ tính giao hoán của sơ đồ sau
<center>
    <!-- https://q.uiver.app/?q=WzAsNCxbMCwwLCJGKFcpIl0sWzEsMCwiaF9XKFcpIl0sWzAsMSwiRlxcbGVmdCAoIFxcd2lkZXRpbGRle1d9IFxccmlnaHQgKSJdLFsxLDEsImhfV1xcbGVmdCAoIFxcd2lkZXRpbGRle1d9IFxccmlnaHQgKSJdLFswLDEsIlxcdmFycGhpX1ciXSxbMiwzLCJcXHZhcnBoaV97XFx3aWRldGlsZGV7V319IiwyXSxbMSwzLCJoX1coXFxldGEpIl0sWzAsMiwiRihcXGV0YSkiLDJdXQ== -->
<iframe class="quiver-embed" src="https://q.uiver.app/?q=WzAsNCxbMCwwLCJGKFcpIl0sWzEsMCwiaF9XKFcpIl0sWzAsMSwiRlxcbGVmdCAoIFxcd2lkZXRpbGRle1d9IFxccmlnaHQgKSJdLFsxLDEsImhfV1xcbGVmdCAoIFxcd2lkZXRpbGRle1d9IFxccmlnaHQgKSJdLFswLDEsIlxcdmFycGhpX1ciXSxbMiwzLCJcXHZhcnBoaV97XFx3aWRldGlsZGV7V319IiwyXSxbMSwzLCJoX1coXFxldGEpIl0sWzAsMiwiRihcXGV0YSkiLDJdXQ==&embed" width="399" height="304" style="border-radius: 8px; border: none;"></iframe>
</center>
nên ta thu được $$F\left ( \eta \right )\left ( \psi \right )=\widetilde{\psi}$$. Mặt khác, từ phép đẳng cấu hàm tử $$F\simeq h_{\widetilde{W}}$$, dẫn đến $$F\left ( \widetilde{\eta} \right )\left ( \widetilde{\psi} \right )=\psi$$. Do đó, ta tính toán được
<center>
    $$\begin{align*}
    F\left ( \eta\circ \widetilde{\eta} \right )\left ( \psi \right )&=F\left ( \widetilde{\eta} \right )\left ( F\left ( \eta \right )\left ( \psi \right ) \right )=\psi\\
F\left ( \widetilde{\eta}\circ \eta \right )\left ( \widetilde{\psi} \right )&=F\left ( \eta \right )\left ( F\left ( \widetilde{\eta} \right )\left ( \widetilde{\psi} \right ) \right )=\widetilde{\psi}
\end{align*}$$
</center>
Bởi vậy, ta thu được sơ đồ giao hoán sau đây
<center>
    <!-- https://q.uiver.app/?q=WzAsNCxbMCwwLCJGKFcpIl0sWzEsMCwiaF9XKFcpIl0sWzAsMSwiRlxcbGVmdCAoIFcgXFxyaWdodCApIl0sWzEsMSwiaF9XXFxsZWZ0ICggVyBcXHJpZ2h0ICkiXSxbMCwxLCJcXHZhcnBoaV9XIl0sWzIsMywiXFx2YXJwaGlfe1d9IiwyXSxbMSwzLCJoX1dcXGxlZnQgKCBcXGV0YVxcY2lyY1xcd2lkZXRpbGRle1xcZXRhfSBcXHJpZ2h0ICkiXSxbMCwyLCJGXFxsZWZ0ICggXFxldGFcXGNpcmNcXHdpZGV0aWxkZXtcXGV0YX0gXFxyaWdodCApIiwyXV0= -->
<iframe class="quiver-embed" src="https://q.uiver.app/?q=WzAsNCxbMCwwLCJGKFcpIl0sWzEsMCwiaF9XKFcpIl0sWzAsMSwiRlxcbGVmdCAoIFcgXFxyaWdodCApIl0sWzEsMSwiaF9XXFxsZWZ0ICggVyBcXHJpZ2h0ICkiXSxbMCwxLCJcXHZhcnBoaV9XIl0sWzIsMywiXFx2YXJwaGlfe1d9IiwyXSxbMSwzLCJoX1dcXGxlZnQgKCBcXGV0YVxcY2lyY1xcd2lkZXRpbGRle1xcZXRhfSBcXHJpZ2h0ICkiXSxbMCwyLCJGXFxsZWZ0ICggXFxldGFcXGNpcmNcXHdpZGV0aWxkZXtcXGV0YX0gXFxyaWdodCApIiwyXV0=&embed" width="371" height="304" style="border-radius: 8px; border: none;"></iframe>
</center>
thỏa mãn $$h_W\left ( \eta\circ \widetilde{\eta} \right )\left ( \operatorname{id}_W \right )=\operatorname{id}_W$$, nghĩa là $$\eta\circ \widetilde{\eta}=\operatorname{id}_{W}$$. Một cách tương tự, ta cũng có $$\widetilde{\eta}\circ \eta =\operatorname{id}_{\widetilde{W}}$$, nghĩa là $$\left ( W,\psi \right )$$ và $$\left ( \widetilde{W},\widetilde{\psi} \right )$$ đẳng cấu với nhau. Vậy khi một hàm tử phản biến $$F$$ biểu diễn được thì cặp $$\left ( W,\psi \right )$$ được xác định một cách duy nhất, sai khác một đẳng cấu. $$\square$$ <br>

Ta sẽ định nghĩa tích $$X\times Y$$, trong đó $$X$$ và $$Y$$ là các vật trong phạm trù $$\mathcal{C}$$ bằng việc sử dụng hàm tử biểu diễn được. Ta định nghĩa hàm tử phản biến $$F:\mathcal{C}\rightarrow \mathbf{Set}$$ như sau: với vật $$Z$$ trong phạm trù $$\mathcal{C}$$, nghĩa là $$Z\in\operatorname{Ob}(\mathcal{C})$$
<center>
    $$F\left ( Z \right )=\operatorname{Hom}_{\mathcal{C}}\left ( Z,X \right )\times \operatorname{Hom}_{\mathcal{C}}\left ( Z,Y \right ),$$
</center>
trong đó vế phải là tích theo nghĩa tập hợp. Tiếp theo, với mọi $$f\in \operatorname{Hom}_{\mathcal{C}}\left ( Z_1,Z_2 \right ),a\in \operatorname{Hom}_{\mathcal{C}}\left ( Z_2,X \right )$$ và $$b\in \operatorname{Hom}_{\mathcal{C}}\left ( Z_2,Y \right )$$, ta định nghĩa
<center>
    $$F\left ( f \right )\left ( \left ( a,b \right ) \right )=\left ( f\circ a,f\circ b \right )\in F\left ( Z_1 \right ),$$
</center>
khi đó ta thu được $$F\left ( f \right )\in\operatorname{Hom}_{\mathbf{Set}}\left ( F\left ( Z_2 \right ),F\left ( Z_1 \right ) \right )$$, nghĩa là, $$F$$ là hàm tử phản biến. Khi hàm tử $$F$$ biểu diễn được, nghĩa là $$F\simeq h_W,$$ với $$W\in\operatorname{Ob}(\mathcal{C})$$ thì khi đó vật $$W$$ được xác định một cách duy nhất theo bổ đề (1.1) và được gọi là tích của $$X$$ và $$Y$$ trong phạm trù $$\mathcal{C}$$, kí hiệu bởi $$X\times Y$$.
<blockquote>
    <strong> Tính chất 1.2. </strong> Trong phạm trù \(\mathcal{C}\), nếu tích \(X\times Y\) tồn tại, khi đó ta có các tính chất sau đây<br>
    \(\bullet \) Tồn tại các cấu xạ \(p_1\in\operatorname{Hom}_{\mathcal{C}}\left ( X\times Y,X \right )\) và \(p_2\in\operatorname{Hom}_{\mathcal{C}}\left ( X\times Y,Y \right )\) sao cho với các cấu xạ \(f\in\operatorname{Hom}_{\mathcal{C}}\left ( Z,X \right )\) và \(g\in\operatorname{Hom}_{\mathcal{C}}\left ( Z,Y \right )\) bất kì, tồn tại duy nhất cấu xạ \(h\in\operatorname{Hom}_{\mathcal{C}}\left ( Z,X\times Y \right )\) thỏa mãn các quan hệ dưới đây
    \[f=p_1\circ h\quad\text{và}\quad g=p_2\circ h.\]
    Nghĩa là tồn tại duy nhất cấu xạ \(h\) sao cho sơ đồ sau đây giao hoán
    <center>
        <!-- https://q.uiver.app/?q=WzAsNCxbMSwwLCJaIl0sWzEsMSwiWFxcdGltZXMgWSJdLFswLDIsIlgiXSxbMiwyLCJZIl0sWzAsMSwiaCIsMV0sWzEsMiwicF8xIl0sWzEsMywicF8yIiwyXSxbMCwzLCJnIl0sWzAsMiwiZiIsMl1d -->
<iframe class="quiver-embed" src="https://q.uiver.app/?q=WzAsNCxbMSwwLCJaIl0sWzEsMSwiWFxcdGltZXMgWSJdLFswLDIsIlgiXSxbMiwyLCJZIl0sWzAsMSwiaCIsMV0sWzEsMiwicF8xIl0sWzEsMywicF8yIiwyXSxbMCwzLCJnIl0sWzAsMiwiZiIsMl1d&embed" width="460" height="432" style="border-radius: 8px; border: none;"></iframe>
    </center>
   \(\bullet \) Ngược lại, nếu vật \(X\times Y\) thỏa mãn các tính chất của điều kiện cần, thì \(\left ( X\times Y,\left ( p_1,p_2 \right ) \right )\) hay đơn giản là \(X\times Y\) là tích của các vật \(X\) và \(Y\) trong phạm trù \(\mathcal{C}\).
</blockquote>
**Chứng minh.** Nếu $$F\simeq h_{X\times Y}$$ thì
<center>
    $$F\left ( X\times Y \right )=\operatorname{Hom}_{\mathcal{C}}\left ( X\times Y,X \right )\times \operatorname{Hom}_{\mathcal{C}}\left ( X\times Y,Y \right ),$$
</center>
và 
<center>
    $$h_{X\times Y}\left ( X\times Y \right )=\operatorname{Hom}_{\mathcal{C}}\left ( X\times Y,X\times Y \right ).$$
    </center>
Do đó, tồn tại cặp cấu xạ $$\left ( p_1,p_2 \right )\in F\left ( X\times Y \right )$$ tương ứng với $$\operatorname{id}_{X\times Y}$$. Tiếp theo, ta sẽ chỉ ra các cấu xạ $$p_1\in\operatorname{Hom}_{\mathcal{C}}\left ( X\times Y,X \right )$$ và $$p_2\in\operatorname{Hom}_{\mathcal{C}}\left ( X\times Y,Y \right )$$ thỏa mãn các tính chất của điều kiện cần. Với vật $$Z$$ trong phạm trù $$\mathcal{C}$$, nghĩa là $$Z\in\mathcal{C}$$ cùng các cấu xạ $$f\in\operatorname{Hom}_{\mathcal{C}}\left ( Z,X \right )$$ và $$g\in\operatorname{Hom}_{\mathcal{C}}\left ( Z,Y \right )$$, ta có thể xem như $$\left ( f,g \right )\in F\left ( Z \right )$$. Mà từ việc $$F\left ( Z \right )\simeq h_{X\times Y}\left ( Z \right )$$, nên tồn tại duy nhất $$h\in h_{X\times Y}\left ( Z \right )=\operatorname{Hom}_{\mathcal{C}}\left ( Z,X\times Y \right )$$ tương ứng với cặp các cấu xạ $$\left ( f,g \right )$$. Từ đây, ta thu được $$F\left ( h \right )\in \operatorname{Hom}_{\mathbf{Set}}\left ( F\left ( X\times Y \right ),F\left ( Z \right ) \right )$$ tương ứng với $$h_{X\times Y}\left ( h \right )\in \operatorname{Hom}_{\mathbf{Set}}\left ( h_{X\times Y}\left ( X\times Y \right ),h_{X\times Y}\left ( Z \right ) \right )$$. Mặt khác, ta có quan hệ sau đây
<center>
    $$\begin{align*}
    F\left ( h \right )\left ( \left ( p_1,p_2 \right ) \right )&=\left ( p_1\circ h,p_2\circ h \right )\\
h_{X\times Y}\left ( h \right )\left ( \operatorname{id}_{X\times Y} \right )&=h.
\end{align*}$$
    </center>
Từ việc cặp các cấu xạ $$\left ( f,g \right )$$ tương ứng với $$h\in h_{X\times Y}\left ( Z \right )$$, nên ta phải có $$\left ( f,g \right )=\left ( p_1\circ h,p_2\circ h \right )$$. Nghĩa là, sơ đồ $$(1)$$ giao hoán.<br>

Ngược lại, giả sử $$\left ( X\times Y,\left ( p_1,p_2 \right ) \right )$$ thỏa mãn các tính chất của điều kiện cần. Với vật $$Z$$ trong phạm trù $$\mathcal{C}$$, nghĩa là $$Z\in\operatorname{Ob}(\mathcal{C})$$, ta định nghĩa ánh xạ $$\varphi_Z$$ như sau
<center>
    $$\begin{align*}
    \varphi_Z:h_{X\times Y}\left ( Z \right )=\operatorname{Hom}_{\mathcal{C}}\left ( Z,X\times Y \right )&\longrightarrow F\left ( Z \right )=\operatorname{Hom}_{\mathcal{C}}\left ( Z,X \right )\times \operatorname{Hom}_{\mathcal{C}}\left ( Z,Y \right )\\
h &\mapsto \left ( p_1\circ h,p_2\circ h \right )
\end{align*}$$
    </center>
Với cặp cấu xạ $$\left ( f,g \right )\in F\left ( Z \right )$$, thì ta sử dụng các tính chất của điều kiện cần thì khẳng định sự tồn tại của cấu xạ $$h\in\operatorname{Hom}_{\mathcal{C}}\left ( Z,X\times Y \right )$$ thỏa mãn $$f=p_1\circ h$$ và $$g=p_2\circ h$$, do đó $$\varphi_Z$$ là ánh xạ toàn ánh. Mặt khác, nếu ta có đẳng thức
<center>
    $$\left ( p_1\circ h,p_2\circ h \right )=\left ( p_1\circ h^{\prime},p_2\circ h^{\prime} \right ),$$
    </center>
trong đó $$h,h^{\prime}\in\operatorname{Hom}_{\mathcal{C}}\left ( Z,X\times Y \right )$$, từ đây ta sử dụng các tính chất trong điều kiện cần thì khẳng định sự tồn tại duy nhất của cấu xạ $$\widetilde{h}\in\operatorname{Hom}_{\mathcal{C}}\left ( Z,X\times Y \right )$$ tương ứng với $$\left ( p_1\circ h,p_2\circ h \right )\in F\left ( Z \right )$$. Nên từ đây, ta thu được $$\widetilde{h}=h=h^{\prime}$$, nghĩa là $$\varphi_Z$$ là ánh xạ toàn ánh.<br>

Hơn nữa, với $$a\in\operatorname{Hom}_{\mathcal{C}}\left ( Z_1,Z_2 \right )$$, ta có sơ đồ sau đây giao hoán
<center>
    <!-- https://q.uiver.app/?q=WzAsNCxbMCwwLCJoX3tYXFx0aW1lcyBZfShaXzIpIl0sWzEsMCwiRlxcbGVmdCAoIFpfMiBcXHJpZ2h0ICkiXSxbMCwxLCJoX3tYXFx0aW1lcyBZfShaXzEpIl0sWzEsMSwiRlxcbGVmdCAoIFpfMSBcXHJpZ2h0ICkiXSxbMCwxLCJcXHZhcnBoaV97Wl8yfSJdLFswLDIsImhfe1hcXHRpbWVzIFl9KGEpIiwyXSxbMSwzLCJGXFxsZWZ0ICggYSBcXHJpZ2h0ICkiXSxbMiwzLCJcXHZhcnBoaV97Wl8xfSIsMl1d -->
<iframe class="quiver-embed" src="https://q.uiver.app/?q=WzAsNCxbMCwwLCJoX3tYXFx0aW1lcyBZfShaXzIpIl0sWzEsMCwiRlxcbGVmdCAoIFpfMiBcXHJpZ2h0ICkiXSxbMCwxLCJoX3tYXFx0aW1lcyBZfShaXzEpIl0sWzEsMSwiRlxcbGVmdCAoIFpfMSBcXHJpZ2h0ICkiXSxbMCwxLCJcXHZhcnBoaV97Wl8yfSJdLFswLDIsImhfe1hcXHRpbWVzIFl9KGEpIiwyXSxbMSwzLCJGXFxsZWZ0ICggYSBcXHJpZ2h0ICkiXSxbMiwzLCJcXHZhcnBoaV97Wl8xfSIsMl1d&embed" width="397" height="304" style="border-radius: 8px; border: none;"></iframe>
    </center>
Cuối cùng, ta thu được $$F$$ và $$h_{X\times Y}$$ đẳng cấu hàm tử, nghĩa là $$F$$ biểu diễn được. $$\square$$ <br>

**2. Tích thớ theo nghĩa phạm trù**<br>
Xét $$X,Y$$ và $$Z$$ là các vật, cùng với các cấu xạ $$q_1:X\rightarrow Z$$ và $$q_2:Y\rightarrow Z$$ trong phạm trù $$\mathcal{C}$$, khi đó ta định nghĩa một hàm tử $$G:\mathcal{C}\rightarrow \mathbf{Set}$$ như sau
<center>
    $$G\left ( T \right )=\left \{ \left ( f,g \right )\in\operatorname{Hom}_{\mathcal{C}}\left ( T,X \right )\times \operatorname{Hom}_{\mathcal{C}}\left ( T,Y \right )\mid q_1\circ f=q_2\circ g \right \},\tag{1}$$
    </center>
trong đó $$T$$ là một vật trong phạm trù $$\mathcal{C}$$, nghĩa là $$T\in\operatorname{Ob}(\mathcal{C})$$ và $$G\left ( T \right )$$ chứa tất cả các cặp cấu xạ $$\left ( f,g \right )$$ sao cho sơ đồ sau đây giao hoán
<center>
    <!-- https://q.uiver.app/?q=WzAsNCxbMSwwLCJUIl0sWzAsMSwiWCJdLFsxLDIsIloiXSxbMiwxLCJZIl0sWzAsMSwiZiIsMl0sWzEsMiwicV8xIiwyXSxbMCwzLCJnIl0sWzMsMiwicV8yIl1d -->
<iframe class="quiver-embed" src="https://q.uiver.app/?q=WzAsNCxbMSwwLCJUIl0sWzAsMSwiWCJdLFsxLDIsIloiXSxbMiwxLCJZIl0sWzAsMSwiZiIsMl0sWzEsMiwicV8xIiwyXSxbMCwzLCJnIl0sWzMsMiwicV8yIl1d&embed" width="432" height="432" style="border-radius: 8px; border: none;"></iframe>
    </center>
Khi đó, với $$h\in\operatorname{Hom}_{\mathcal{C}}\left ( T_1,T_2 \right )$$ và $$\left ( a,b \right )\in G\left ( T_2 \right )$$, ta định nghĩa
<center>
    $$G\left ( h \right )\left ( \left ( a,b \right ) \right )=\left ( a\circ h,b\circ h \right ),$$
    </center>
thì dẫn đến $$G\left ( h \right )\left ( \left ( a,b \right ) \right )\in G\left ( T_1 \right )$$ và $$G\left ( h \right )\in\operatorname{Hom}_{\mathbf{Set}}\left ( G\left ( T_2 \right ),G\left ( T_1 \right ) \right )$$, nghĩa là, $$G$$ là hàm tử phản biến. Nếu $$\left ( W,\left ( p_1,p_2 \right ) \right )$$, trong đó $$\left ( p_1,p_2 \right )\in G\left ( W \right )$$, biểu diễn hàm tử $$G$$, thì $$\left ( p_1,p_2 \right )\in G\left ( W \right )$$, hay đơn giản ta viết $$W$$ được gọi là tích thớ của $$X$$ và $$Y$$ trên $$Z$$, kí hiệu bởi $$X\times_{Z}Y$$. Khi đó các cấu xạ $$p_1:X\times_{Z}Y\rightarrow X$$ và $$p_2:X\times_{Z}Y\rightarrow Y$$ được gọi là các phép chiếu chính tắc trên $$X$$ và tương ứng trên $$Y$$. Lưu ý rằng, $$\left ( W,\left ( p_1,p_2 \right ) \right )$$ được xác định một cách duy nhất, sai khác một đẳng cấu.<br>

Như trong tính chất (1.2), ta cũng có tính chất tương tự như sau
<blockquote>
    <strong> Tính chất 2.1. </strong> Cho \(q_1:X\rightarrow Z\) và \(q_2:Y\rightarrow Z\) là các cấu xạ trong phạm trù \(\mathcal{C}\), khi đó tích thớ của \(X\) và \(Y\) trên \(Z\) tồn tại khi và chỉ khi tồn tại một vật \(W\in\operatorname{Ob}(\mathcal{C})\) và các cấu xạ \(p_1:W\rightarrow X\) và \(p_2:W\rightarrow Y\) thỏa mãn các tính chất sau đây<br>
    \(\bullet\) Sơ đồ sau đây giao hoán
    <center>
        <!-- https://q.uiver.app/?q=WzAsNCxbMSwwLCJXIl0sWzAsMSwiWCJdLFsxLDIsIloiXSxbMiwxLCJZIl0sWzAsMSwicF8xIiwyXSxbMSwyLCJxXzEiLDJdLFswLDMsInBfMiJdLFszLDIsInFfMiJdXQ== -->
<iframe class="quiver-embed" src="https://q.uiver.app/?q=WzAsNCxbMSwwLCJXIl0sWzAsMSwiWCJdLFsxLDIsIloiXSxbMiwxLCJZIl0sWzAsMSwicF8xIiwyXSxbMSwyLCJxXzEiLDJdLFswLDMsInBfMiJdLFszLDIsInFfMiJdXQ==&embed" width="432" height="432" style="border-radius: 8px; border: none;"></iframe>
    </center>
    \(\bullet\) Với mỗi sơ đồ giao hoán, được xác định bởi
    <center>
        <!-- https://q.uiver.app/?q=WzAsNCxbMSwwLCJUIl0sWzAsMSwiWCJdLFsxLDIsIloiXSxbMiwxLCJZIl0sWzAsMSwiZiIsMl0sWzEsMiwicV8xIiwyXSxbMCwzLCJnIl0sWzMsMiwicV8yIl1d -->
<iframe class="quiver-embed" src="https://q.uiver.app/?q=WzAsNCxbMSwwLCJUIl0sWzAsMSwiWCJdLFsxLDIsIloiXSxbMiwxLCJZIl0sWzAsMSwiZiIsMl0sWzEsMiwicV8xIiwyXSxbMCwzLCJnIl0sWzMsMiwicV8yIl1d&embed" width="432" height="432" style="border-radius: 8px; border: none;"></iframe>
    </center>
    thì tồn tại duy nhất cấu xạ \(h:T\rightarrow W\) sao cho sơ đồ sau đây giao hoán
    <center>
        <!-- https://q.uiver.app/?q=WzAsNCxbMSwwLCJUIl0sWzEsMSwiVyJdLFswLDIsIlgiXSxbMiwyLCJZIl0sWzAsMV0sWzEsMiwicF8xIl0sWzEsMywicF8yIiwyXSxbMCwzLCJnIl0sWzAsMiwiZiIsMl1d -->
<iframe class="quiver-embed" src="https://q.uiver.app/?q=WzAsNCxbMSwwLCJUIl0sWzEsMSwiVyJdLFswLDIsIlgiXSxbMiwyLCJZIl0sWzAsMV0sWzEsMiwicF8xIl0sWzEsMywicF8yIiwyXSxbMCwzLCJnIl0sWzAsMiwiZiIsMl1d&embed" width="432" height="432" style="border-radius: 8px; border: none;"></iframe>
    </center>
</blockquote>
**Chứng minh.** Ta chứng minh hai chiều của tính chất như sau<br>

$$\left ( \Rightarrow  \right )$$ Giả sử tích thớ $$X\times_{Z}Y$$ tồn tại, khi đó ta đặt $$W=X\times_{Z}Y$$ và xét $$\left ( p_1,p_2 \right )\in G\left ( W \right )$$, trong đó $$p_1:W\rightarrow X$$ và $$p_2:W\rightarrow Y$$ và là phần tử tương ứng với $$\operatorname{id}_W\in h_W(W)$$, thì từ định nghĩa $$(1)$$ ta thu được sơ đồ $$(2)$$ giao hoán. Từ giả thiết về tính giao hoán của $$(3)$$ dẫn đến $$\left ( f,g \right )\in G\left ( T \right )$$, và hơn thế nữa, phép đẳng cấu $$G\left ( T \right )\simeq h_W\left ( T \right )$$ theo nghĩa tập hợp, dẫn đến tồn tại duy nhất cấu xạ $$h:T\rightarrow W$$. Khi đó, $$\left ( p_1\circ h,p_2\circ h \right )\in G\left ( T \right )$$ và từ $$(1)$$ ta thu được
<center>
    $$\left ( p_1\circ h,p_2\circ h \right )=G\left ( g \right )\left ( \left ( p_1,p_2 \right ) \right ).$$
    </center>
Từ sơ đồ sau đây giao hoán
        <center>
    <!-- https://q.uiver.app/?q=WzAsNCxbMCwwLCJHKFcpIl0sWzEsMCwiaF9XKFcpIl0sWzAsMSwiRyhUKSJdLFsxLDEsImhfVyhUKSJdLFswLDFdLFswLDIsIkcoaCkiLDJdLFsxLDMsImhfVyhoKSJdLFsyLDNdXQ== -->
<iframe class="quiver-embed" src="https://q.uiver.app/?q=WzAsNCxbMCwwLCJHKFcpIl0sWzEsMCwiaF9XKFcpIl0sWzAsMSwiRyhUKSJdLFsxLDEsImhfVyhUKSJdLFswLDFdLFswLDIsIkcoaCkiLDJdLFsxLDMsImhfVyhoKSJdLFsyLDNdXQ==&embed" width="361" height="304" style="border-radius: 8px; border: none;"></iframe>
    </center>
    dẫn đến $$$h\in h_W\left ( h \right )$$, điều này tương ứng với việc $$\left ( p_1\circ h,p_2\circ h \right )\in G\left ( T \right )$$. Mặt khác, $$h$$ tương ứng với $$\left ( f,g \right )\in G\left ( T \right )$$, nên từ đây ta thu được $$\left ( f,g \right )=\left ( p_1\circ h,p_2\circ h \right )$$, nghĩa là sơ đồ $$(4)$$ giao hoán. Do đó, các tính chất trên là điều kiện cần để tích thớ tồn tại.<br>
    
    $$\left ( \Leftarrow  \right )$$ Giả sử tồn tại cặp $$\left ( W,\left ( p_1,p_2 \right ) \right )$$ thỏa mãn các tính chất trên (điều kiện cần). Khi đó, với $$T$$ là một vật trong phạm trù $$\mathcal{C}$$, nghĩa là $$T\in\operatorname{Ob}(\mathcal{C})$$, ta định nghĩa ánh xạ $$\varphi_T$$ giữa các tập hợp như sau
<center>
    $$\begin{align*}
    \varphi_T:h_W\left ( T \right )&\longrightarrow G\left ( T \right )\\
a &\mapsto \left ( p_1\circ a,p_2\circ a \right ),
\end{align*}$$
    </center>
    <!-- https://q.uiver.app/?q=WzAsNCxbMSwwLCJUIl0sWzEsMSwiVyJdLFswLDIsIlgiXSxbMiwyLCJZIl0sWzAsMSwiYSIsMV0sWzEsMiwicF8xIl0sWzEsMywicF8yIiwyXSxbMCwzLCJwXzJcXGNpcmMgYSJdLFswLDIsInBfMVxcY2lyYyBhIiwyXV0= -->
<iframe class="quiver-embed" src="https://q.uiver.app/?q=WzAsNCxbMSwwLCJUIl0sWzEsMSwiVyJdLFswLDIsIlgiXSxbMiwyLCJZIl0sWzAsMSwiYSIsMV0sWzEsMiwicF8xIl0sWzEsMywicF8yIiwyXSxbMCwzLCJwXzJcXGNpcmMgYSJdLFswLDIsInBfMVxcY2lyYyBhIiwyXV0=&embed" width="432" height="432" style="border-radius: 8px; border: none;"></iframe>
</center>
Ta sẽ chứng minh rằng $$\varphi_T$$ là song ánh. Ta xét cặp cấu xạ $$\left ( f,g \right )\in G(T)$$ bất kì, sử dụng điều kiện cần khẳng định rằng tồn tại duy nhất cấu xạ $$h\in h_W\left ( T \right )$$ thỏa mãn
<center>
    $$\left ( f,g \right )=\left ( p_1\circ h,p_2\circ h \right ),$$
    </center>
điều này khẳng định ánh xạ $$\varphi_T$$ là song ánh. Hơn nữa, với $$a\in\operatorname{Hom}_{\mathcal{C}}\left ( T_1,T_2 \right )$$ thì ta thu được sơ đồ sau đây giao hoán
<center>
    <!-- https://q.uiver.app/?q=WzAsNCxbMCwwLCJoX1coVF8yKSJdLFsxLDAsIkcoVF8yKSJdLFsxLDEsIkcoVF8xKSJdLFswLDEsImhfVyhUXzEpIl0sWzAsMSwiXFx2YXJwaGlfe1RfMX0iXSxbMSwyLCJmKGEpIl0sWzAsMywiaF9XKGEpIiwyXSxbMywyLCJcXHZhcnBoaV97VF8yfSIsMl1d -->
<iframe class="quiver-embed" src="https://q.uiver.app/?q=WzAsNCxbMCwwLCJoX1coVF8yKSJdLFsxLDAsIkcoVF8yKSJdLFsxLDEsIkcoVF8xKSJdLFswLDEsImhfVyhUXzEpIl0sWzAsMSwiXFx2YXJwaGlfe1RfMX0iXSxbMSwyLCJmKGEpIl0sWzAsMywiaF9XKGEpIiwyXSxbMywyLCJcXHZhcnBoaV97VF8yfSIsMl1d&embed" width="355" height="304" style="border-radius: 8px; border: none;"></iframe>
    </center>
    Nghĩa là, $$\varphi:h_W\overset{\sim }{\longrightarrow}G$$ là một phép đẳng cấu giữa các hàm tử, do đó $$G$$ được biểu diễn bởi cặp $$\left ( W,\left ( p_1,p_2 \right ) \right )$$. Kết hợp cả hai chiều ta thu được tính chất cần chứng minh về điều kiện cần và đủ để tích thớ $$X\times_{Z}Y$$ tồn tại. $$\square$$<br>
    
Việc chuẩn bị các định nghĩa và tính chất trên là để chứng minh kết quả chính trong bài viết này. Đó là khẳng định sự tồn tại của tích thớ trong phạm trù lược đồ $$\textbf{Sch}.$$
<blockquote>
    <strong> Định lý 2.2 </strong>(Tích thớ trong phạm trù lược đồ \(\textbf{Sch}\)) Trong phạm trù lược đồ \(\textbf{Sch}\), tích thớ là tồn tại.
</blockquote>
**Chứng minh.** Trước khi bước vào các bước chứng minh của định lý, ta cần một bổ đề sau đây<br>
<blockquote>
    <strong> Bổ đề 2.3 </strong>(Tích thớ trong phạm phạm trù lược đồ affine \(\textbf{Aff.Sch}\)) Cho các lược đồ affine \(X=\operatorname{Spec}A,Y=\operatorname{Spec}B\) và \(Z=\operatorname{Spec}C\) cùng các cấu xạ \(q_1:X\rightarrow Z\) và \(q_2:Y\rightarrow Z\), khi đó tích thớ \(\left ( X\times_{Z}Y,\left ( p_1,p_2 \right ) \right )\) là tồn tại, và được xác định bởi
\[X\times_{Z}Y=\operatorname{Spec}\left ( A\otimes_{C}B \right ),\]
trong đó \(p_1\) và \(p_2\) là các cấu xạ lược đồ affine cảm sinh từ các đồng cấu tự nhiên dưới đây
\begin{align*}
    \varphi_1:A&\rightarrow A\otimes_{C}B\\ 
a &\mapsto a\otimes 1 
\end{align*}
\begin{align*}
    \varphi_2:B&\rightarrow A\otimes_{C}B\\ 
b &\mapsto 1\otimes b 
\end{align*}
    </blockquote>
    **Chứng minh.** Trước tiên, ta sẽ nhắc lại mà không chứng minh một tính chất cơ bản, được phát biểu như sau<br>
    <blockquote>
    <strong> Tính chất 2.4 </strong> Cho cấu xạ \(\left ( f,\theta \right )\) từ lược đồ \(\left ( Z,\mathcal{O}_Z \right )\) đến lược đồ affine \(\left ( \operatorname{Spec}R,\mathcal{O}_{\operatorname{Spec}R} \right )\), khi đó ta có đẳng cấu sau đây
\[\operatorname{Hom}_{\mathbf{Sch}}\left ( Z,\operatorname{Spec}R \right )\simeq \operatorname{Hom}_{\mathbf{Ring}}\left ( R,\Gamma\left ( Z,\mathcal{O}_Z \right ) \right )\]
    </blockquote>
    Sử dụng tính chất (2.4), các cấu xạ lược đồ $$f:T\rightarrow X$$ và $$g:T\rightarrow Y$$ được xác định một cách duy nhất bởi các đồng cấu vành tương ứng là $$\phi:A\rightarrow \Gamma\left ( T,\mathcal{O}_T \right )$$ và $$\psi:B\rightarrow \Gamma\left ( T,\mathcal{O}_T \right )$$, và để cho gọn ta đặt $$R=\Gamma\left ( T,\mathcal{O}_T \right )$$. Tương tự, ta cũng có các cấu xạ lược đồ $$q_1:X\rightarrow Z$$ và $$q_2:Y\rightarrow Z$$ được xác định một cách duy nhất bởi các đồng cấu vành tương ứng là $$\nu_1:C\rightarrow A$$ và $$\nu_2:C\rightarrow B$$, khi đó $$A$$ và $$B$$ là các $$C$$-đại số thông qua các đồng cấu $$\nu_1$$ và $$\nu_2$$. Hơn nữa, từ việc $$q_1\circ f=q_2\circ g$$, dẫn đến các đồng cấu $$\phi\circ \nu_1:C\rightarrow R$$ và $$\psi\circ \nu_2:C\rightarrow R$$ trùng nhau. Do đó, hàm tử $$G$$ trong $$(1)$$ có thể được viết lại như sau
<center>
    $$\begin{align*}
    G\left ( T \right )&=\left \{ \left ( f,g \right )\in\operatorname{Hom}_{\mathcal{C}}\left ( T,X \right )\times \operatorname{Hom}_{\mathcal{C}}\left ( T,Y \right )\mid q_1\circ f=q_2\circ g \right \}\\
&\simeq \left \{ \left ( \phi,\psi \right )\in \operatorname{Hom}_{\mathcal{C}}\left ( A,R \right )\times \operatorname{Hom}_{\mathcal{C}}\left ( B,R \right )\mid \phi\circ \nu_1=\psi\circ \nu_2 \right \}.
\end{align*}$$
    </center>
Từ việc xem $$A$$ và $$B$$ như là các $$C$$-đại số thông qua các đồng cấu $$\nu_1$$ và $$\nu_2$$, ta thấy rằng từ việc $$\phi\circ \nu_1=\psi\circ \nu_2$$ dẫn đến $$\phi\left ( c\cdot 1_A \right )=\psi\left ( c\cdot 1_B \right )$$, trong đó $$c\in C$$ và $$1_A,1_B$$ tương ứng là các phần tử đơn vị của $$A$$ và $$B$$. Hơn nữa, ta cũng xem $$R$$ như là một $$C$$-đại số thông qua $$\phi\circ \nu_1=\psi\circ \nu_2$$, thì với $$a\in A,b\in B$$ và $$c\in C$$ ta thu được
<center>
    $$\phi\left ( c\cdot a \right )=c\cdot \phi\left ( a \right )\enskip\text{và}\enskip \psi\left ( c\cdot b \right )=c\cdot \psi\left ( b \right ).$$
    </center>
Từ đây, ta định nghĩa ánh xạ $$\Phi$$ như sau
<center>
    $$\begin{align*}
    \Phi:A\times B&\longrightarrow R\\
\left ( a,b \right ) &\mapsto \phi\left ( a \right )\psi\left ( b \right ),
\end{align*}$$
    </center>
khi đó dễ kiểm tra $$\Phi$$ là ánh xạ $$C$$-song tuyến tính thỏa mãn với $$a\in A,b\in B$$ và $$c\in C$$ thì
<center>
    $$\Phi\left ( c\cdot a,b \right )=\Phi\left ( a,c\cdot b \right )=c\cdot \Phi\left ( a,b \right ),\tag{5}$$
    </center>
và, với $$a_1,a_2\in A$$ và $$b_1,b_2\in B$$ thì
<center>
    $$\Phi\left ( a_1a_2,b_1b_2 \right )=\Phi\left ( a_1,b_1 \right )\Phi\left ( a_2,b_2 \right ).\tag{6}$$
    </center>
Ngược lại, khi ánh xạ $$C$$-song tuyến tính $$\Phi$$ thỏa mãn $$(5)$$ và $$(6)$$, ta định nghĩa
<center>
    $$\phi\left ( a \right )=\Phi\left ( a,1_B \right )\enskip\text{và}\enskip \psi\left ( b \right )=\Phi\left ( 1_A,b \right ),$$
    </center>
thì dễ kiểm tra $$\phi:A\rightarrow R$$ và $$\psi:B\rightarrow R$$ là các đồng cấu vành, và với $$a\in A,b\in B$$ ta thu được
<center>
    $$\Phi\left ( a,b \right )=\Phi\left ( a,1_B \right )\Phi\left ( 1_A,b \right )=\phi\left ( a \right )\psi\left ( b \right ).$$
    </center>
Hơn nữa, với $$a\in A,b\in B$$ và $$c\in C$$ ta thu được
<center>
    $$\phi\left ( c\cdot 1_A \right )=\Phi\left ( c\cdot 1_A,1_B \right )=\Phi\left ( 1_A,c\cdot 1_B \right )=\psi\left ( c\cdot 1_B \right ),$$
    </center>
điều này khẳng định $$\phi\circ \nu_1=\psi\circ \nu_2$$. Do đó, ta thu được
<center>
    $$G\left ( T \right )\simeq \left \{ \Phi:A\times B\longrightarrow R\mid \Phi\enskip\text{là ánh xạ \(C\)-song tuyến tính thỏa mãn}\ \text{\((1)\) và \((2)\)} \right \}.\tag{7}$$
    </center>
Bởi định nghĩa của tích tensor $$A\otimes_{C}B$$ của các $$C$$-đại số $$A$$ và $$B$$, vế phải của $$(7)$$ đẳng cấu theo nghĩa tập hợp với $$\operatorname{Hom}\left ( A\otimes_{C}B,R \right )$$. Nghĩa là, ta có đẳng cấu theo nghĩa tập hợp sau đây
<center>
    $$G\left ( T \right )\overset{\sim }{\longrightarrow}\operatorname{Hom}\left ( A\otimes_{C}B,R \right ),$$
    </center>
và bởi tính chất (2.4), ta thu được đẳng cấu giữa các tập hợp như sau
<center>
    $$\varphi_T:G\left ( T \right )\overset{\sim }{\longrightarrow}\operatorname{Hom}\left ( Z,\operatorname{Spec}\left ( A\otimes_{C}B \right ) \right ).$$
    </center>
Cho cấu xạ lược đồ $$j:T_1\rightarrow T_2$$, khi đó nó cảm sinh một đồng cấu vành
<center>
    $$\widehat{j}:\Gamma\left ( T_1,\mathcal{O}_{T_1} \right )\rightarrow \Gamma\left ( T_2,\mathcal{O}_{T_2} \right ).$$
    </center>
Khi đó, nếu ta đặt $$R_1=\Gamma\left ( T_1,\mathcal{O}_{T_1} \right )$$ và $$R_2=\Gamma\left ( T_2,\mathcal{O}_{T_2} \right )$$, thì đồng cấu $$\widehat{j}$$ cảm sinh một ánh xạ
<center>
    $$\begin{align*}
    \operatorname{Hom}\left ( A\otimes_{C}B,R_1 \right )&\rightarrow \operatorname{Hom}\left ( A\otimes_{C}B,R_2\right )\\
\eta  &\mapsto \widehat{j}\circ\eta
\end{align*}$$
    </center>
và ta lại sử dụng tính chất (2.4), thì thu được ánh xạ cảm sinh như sau
<center>
    $$\operatorname{Hom}\left ( T_2,\operatorname{Spec}\left ( A\otimes_{C}B \right ) \right )\rightarrow \operatorname{Hom}\left ( T_1,\operatorname{Spec}\left ( A\otimes_{C}B \right ) \right ).$$
    </center>
Để cho gọn thì ta đặt $$W=\operatorname{Spec}\left ( A\otimes_{C}B \right )$$, thì sơ đồ sau đây giao hoán
    <center>
    <!-- https://q.uiver.app/?q=WzAsNCxbMCwwLCJHKFRfMikiXSxbMSwwLCJcXG9wZXJhdG9ybmFtZXtIb219XFxsZWZ0ICggVF8yLFcgXFxyaWdodCApIl0sWzEsMSwiXFxvcGVyYXRvcm5hbWV7SG9tfVxcbGVmdCAoIFRfMSxXIFxccmlnaHQgKSJdLFswLDEsIkdUXzEpIl0sWzAsMSwiXFx2YXJwaGlfe1RfMn0iXSxbMSwyLCJoX1coaikiXSxbMCwzLCJHKGopIiwyXSxbMywyLCJcXHZhcnBoaV97VF8xfSIsMl1d -->
<iframe class="quiver-embed" src="https://q.uiver.app/?q=WzAsNCxbMCwwLCJHKFRfMikiXSxbMSwwLCJcXG9wZXJhdG9ybmFtZXtIb219XFxsZWZ0ICggVF8yLFcgXFxyaWdodCApIl0sWzEsMSwiXFxvcGVyYXRvcm5hbWV7SG9tfVxcbGVmdCAoIFRfMSxXIFxccmlnaHQgKSJdLFswLDEsIkdUXzEpIl0sWzAsMSwiXFx2YXJwaGlfe1RfMn0iXSxbMSwyLCJoX1coaikiXSxbMCwzLCJHKGopIiwyXSxbMywyLCJcXHZhcnBoaV97VF8xfSIsMl1d&embed" width="430" height="304" style="border-radius: 8px; border: none;"></iframe>
    </center>
    Phần tử $$\left ( p_1,p_2 \right )\in \operatorname{Hom}\left ( W,X \right )\times \operatorname{Hom}\left ( W,Y \right )$$ tương ứng với $$\operatorname{id}_W\in \operatorname{Hom}\left ( W,W \right )$$ là cặp các cấu xạ lược đồ được xác định bởi $$\varphi_1:A\rightarrow A\otimes_{C}B$$ và $$\varphi_2:B\rightarrow A\otimes_{C}B$$ trong bổ đề (2.3). Cuối cùng, ta thu được $$\left ( W,\left ( p_1,p_2 \right ) \right )$$ biểu diễn hàm tử $$G$$, điều phải chứng minh. $$\square$$ <br>

Quay lại với việc chứng minh kết quả chính, định lý (2.2) và ta sẽ chia chứng minh thành nhiều bước như sau.<br>
**Bước 1.** Cho các cấu xạ lược đồ $$q_1:X\rightarrow Z$$ và $$q_2:Y\rightarrow Z$$, nếu tích thớ $$\left ( X\times_{Z}Y,\left ( p_1,p_2 \right ) \right )$$ tồn tại, thì với $$U$$ là một tập mở bất kì trong $$X$$, $$\left ( p_1^{-1}\left ( U \right ),\left ( \widehat{p_1},p_2 \right ) \right )$$ là tích thớ của $$U$$ và $$Y$$ trên $$Z$$, trong đó $$\widehat{p_1}$$ là ánh xạ hạn chế của $$p_1$$ xuống $$p_1^{-1}\left ( U \right ).$$ <br>
**Chứng minh.** Với phép dìm mở (open immersion) tự nhiên $$\iota: U\rightarrow X$$, ta đặt $$\widehat{q_1}=q_1\circ \iota: U\rightarrow Z$$. Giả sử các cấu xạ lược đồ $$\widehat{f}:T\rightarrow U$$ và $$g:T\rightarrow Y$$ được xác định và thỏa mãn $$\widehat{q_1}\circ \widehat{f}=q_2\circ g$$; lại đặt $$f=\iota \circ \widehat{f}:T\rightarrow X$$ thì ta thu được quan hệ $$q_1\circ f=q_2\circ g$$. Bởi giả thiết bài toán, nên tồn tại duy nhất $$h:T\rightarrow X\times_{Z}Y$$ thỏa mãn $$f=p_1\circ h$$ và $$g=p_2\circ h$$. Tiếp theo, do $$f\left ( T \right )\subset U$$ nên ta thu được $$h\left ( T \right )\subset p_1^{-1}\left ( U \right )$$, mà từ việc $$p_1^{-1}\left ( U \right )$$ là tập mở trong $$X\times_{Z}Y$$, kéo theo $$p_1^{-1}\left ( U \right )$$ là một lược đồ con mở, và ta có thể xem $$h$$ như là một cấu xạ từ $$T$$ vào $$p_1^{-1}\left ( U \right )$$. Đến đây, ta thu được $$\widehat{f}=\widehat{p_1}\circ h$$ và $$g=p_2\circ h$$. Từ tính duy nhất của $$h$$ và tính chất (2.1) dẫn đến $$\left ( p_1^{-1}\left ( U \right ),\left ( \widehat{p_1},p_2 \right ) \right )$$ là tích thớ của $$U$$ và $$Y$$ trên $$Z$$, điều phải chứng minh. $$\square$$ <br>

**Bước 2.** Cho các cấu xạ lược đồ $$q_1:X\rightarrow Z$$ và $$q_2:Y\rightarrow Z$$, gọi $$\left \{ X_i \right \}_{i\in I}$$ là một phủ mở của $$X$$. Nếu $$q_1^{\left ( i \right )}=\left.q_1\right|_{X_i}:X_i\rightarrow Z$$ và $$q_2:Y\rightarrow Z$$ là các cấu xạ thỏa mãn tích thớ $$\left ( X_i\times_{Z}Y,\left ( q_1^{\left ( i \right )},q_2 \right ) \right )$$ tồn tại, khi đó tích thớ $$\left ( X\times_{Z}Y,\left ( q_1,q_2 \right ) \right )$$ cũng tồn tại.<br>
**Chứng minh.** Trước tiên, ta đặt $$X_{ij}=X_i\cap X_j$$ nếu $$X\cap X_j\neq \varnothing$$, và đặt $$U_{ij}=\left ( p_1^{\left ( i \right )} \right )^{-1}\left ( X_{ij} \right )\subset X_i\times_{Z}Y$$, khi đó ta có $$U_{ij}=X_{ij}\times_{Z}Y$$. Mà do $$X_{ij}=X_{ji}$$ và $$U_{ji}=\left ( p_1^{\left ( i \right )} \right )^{-1}\left ( X_{ji} \right )\subset X_i\times_{Z}Y$$ cũng là tích thớ của $$X_{ji}$$ và $$Y$$ trên $$Z$$, từ đó ta có đẳng cấu sau đây
<center>
    $$\varphi_{ij}:U_{ij}\overset{\sim }{\longrightarrow}U_{ji},$$
    </center>
thỏa mãn các tính chất
<center>
    $$\left.p_1^{\left ( i \right )}\right|_{U_{ij}}=\left ( \left.p_1^{\left ( j \right )}\right|_{U_{ji}} \right )\circ \varphi_{ij}\quad\text{và}\quad \left.p_2^{\left ( i \right )}\right|_{U_{ij}}=\left ( \left.p_2^{\left ( j \right )}\right|_{U_{ji}} \right )\circ \varphi_{ij},\quad\text{trong đó}\quad \varphi_{ij}=\varphi_{ji}^{-1}.\tag{8}$$
    </center>
Nếu $$X_i\cap X_j\cap X_k\neq \varnothing$$ thì ta có
<center>
    $$\varphi_{ij}\left ( U_{ij}\cap U_{ik} \right )=U_{ji}\cap U_{jk},$$
    </center>
và trên $$U_{ij}\cap U_{ik}$$ ta thu được $$\varphi_{ik}=\varphi_{ij}\circ \varphi_{jk}$$. Nghĩa là, ta có thể dán $$X_i\times_{Z}Y$$ bởi $$\left \{ \varphi_{ij} \right \}$$ để thu được lược đồ $$X\times_{Z}Y$$. Hơn nữa, từ $$(8)$$ ta thu được các cấu xạ lược đồ $$p_1:X\times_{Z}Y\rightarrow X$$ và $$p_2:X\times_{Z}Y\rightarrow Y$$, trong đó hạn chế của các cấu xạ $$p_1$$ và $$p_2$$ xuống $$X_i\times_{Z}Y$$ tương ứng là $$p_1^{\left ( i \right )}$$ và $$p_2^{\left ( i \right )}.$$ <br>

Tiếp theo, ta sẽ chứng minh $$\left ( X\times_{Z}Y,\left ( q_1,q_2 \right ) \right )$$ là tích thớ. Cho các cấu xạ lược đồ $$f:T\rightarrow X$$ và $$g:T\rightarrow Y$$ thỏa mãn $$q_1\circ f=q_2\circ g$$; và ta đặt $$T_i=f^{-1}\left ( X_i \right ),i\in I,$$ $$\left.f\right|_{T_{i}}=f_i$$ và $$\left.g\right|_{T_{i}}=g_i$$, thì thu được quan hệ $$q_1^{\left ( i \right )}\circ f_i=q_2\circ g_i$$. Do đó, tồn tại duy nhất cấu xạ $$h_i:T_i\rightarrow X_i\times_{Z}Y$$ thỏa mãn $$f_i=p_1^{\left ( i \right )}\circ h_i$$ và $$g_i=p_2^{\left ( i \right )}\circ h_i$$. Như suy luận trên, ta có thể dán các cấu xạ $$h_i$$ để thu được cấu xạ $$h:T\rightarrow X\times_{Z}Y$$ thỏa mãn $$f=p_1\circ h$$ và $$g=p_2\circ h$$. Lưu ý rằng, do tính duy nhất của các cấu xạ $$h_i$$ nên ta cũng thu được tính duy nhất của $$h$$, điều phải chứng minh. $$\square$$ <br>











**Bước 3.** Chứng minh định lý (2.2) như sau.<br>
**Chứng minh.** Cho các cấu xạ lược đồ $$q_1:X\rightarrow Z$$ và $$q_2:Y\rightarrow Z$$. Giả sử $$Y$$ và $$Z$$ là các lược đồ affine, ta gọi $$\left \{ X_i \right \}_{i\in I}$$ là một phủ mở affine của $$X$$. Đặt $$q_1^{\left ( i \right )}=\left.q_1\right|_{X_i}:X_i\rightarrow Z$$ thì bởi bổ đề (2.3), ta thu được tích thớ $$\left ( X_i\times_{Z}Y,\left ( p_1^{\left ( i \right )},p_2^{\left ( i \right )} \right )\right )$$ tồn tại. Từ đó, sử dụng ($$\textbf{Bước 2}$$) ta khẳng định được sự tồn tại của tích thớ $$\left ( X\times_{Z}Y,\left ( p_1,p_2\right )\right ).$$ <br>

Tiếp theo, ta giả sử $$Z$$ là lược đồ affine, trong khi $$X$$ và $$Y$$ là các lược đồ bất kì. Gọi $$\left \{ Y_j \right \}_{j\in J}$$ là một phủ mở affine của $$Y$$, tương tự như suy luận ở trên, ta thu được tích thớ $$\left ( X\times_{Z}Y_j,\left ( p_1^{\left ( j \right )},p_2^{\left ( j \right )} \right )\right )$$ tồn tại. Từ đó, sử dụng ($$\textbf{Bước 2}$$) ta khẳng định được sự tồn tại của tích thớ $$\left ( X\times_{Z}Y,\left ( p_1,p_2\right )\right ).$$ <br>

Cuối cùng, ta xét $$X,Y$$ và $$Z$$ là các lược đồ bất kì. Ta chọn một phủ mở $$\left \{ Z_k \right \}_{k\in K}$$ của $$Z$$ bao gồm các lược đồ affine, khi đó ta đặt
<center>
    $$X_k=q_1^{-1}\left ( Z_k \right ),\quad Y_k=q_2^{-1}\left ( Z_k \right )\quad\text{và}\quad q_1^{\left ( k \right )}=\left.q_1\right|_{X_k},\quad q_2^{\left ( k \right )}=\left.q_2\right|_{X_k}.$$
    </center>
Khi đó, ta có tích thớ $$\left ( X_k\times_{Z}Y_k,\left ( p_1^{\left ( k \right )},p_2^{\left ( k \right )} \right ) \right )$$ của $$X_k$$ và $$Y_k$$ trên $$Z$$. Ta sẽ chứng minh tích thớ này chính là $$X_k\times_{Z}Y$$. Thật vậy, cho $$f:T\rightarrow X_k$$ và $$g:T\rightarrow Y$$ là các cấu xạ thỏa mãn $$q_1^{\left ( k \right )}\circ f=q_2\circ g$$; mặt khác, ta có đánh giá
<center>
    $$q_2\left ( g\left ( T \right ) \right )=q_1^{\left ( k \right )}\left ( f\left ( T \right ) \right )\subset q_1^{\left ( k \right )}\left ( X_k \right )\subset Z_k\quad\text{dẫn đến}\quad g\left ( T \right )\subset Y_k.$$
    </center>
Từ đó, ta khẳng định rằng tồn tại duy nhất cấu xạ $$h:T\rightarrow X_k\times_{Z}Y_k$$ thỏa mãn $$f=p_1^{\left ( k \right )}\circ h$$ và $$g=p_2^{\left ( k \right )}\circ h$$, nghĩa là $$X_k\times_{Z}Y_k$$ chính là $$X_k\times_{Z}Y$$. Mà từ việc $$\left \{ X_k \right \}_{k\in K}$$ là một phủ mở của $$X$$, nên sử dụng ($$\textbf{Bước 2}$$) ta khẳng định được sự tồn tại của tích thớ $$\left ( X\times_{Z}Y,\left ( p_1,p_2 \right ) \right ).$$ $$\square$$ <br>

Kết hợp cả 3 bước trong chứng minh ta khẳng định được sự tồn tại của tích thớ trong phạm trù lược đồ $$\textbf{Sch}$$, điều phải chứng minh. $$\blacksquare$$


    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    

























 
