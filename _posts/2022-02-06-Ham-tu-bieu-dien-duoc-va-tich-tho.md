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
    <strong> Tính chất 2.1. </strong> 


























 
