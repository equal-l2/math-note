\newcommand{\drm}{\mathrm{d}}
\newcommand{\abs}[1]{\begin{vmatrix} #1 \end{vmatrix}}
#Taylor展開
関数$f$が点$a$において$k(\leq 1)$回微分可能なとき、次の式が成り立つ。

$$\displaystyle f(x)=\sum_{n=0}^{k-1} {\frac{f^{(n)}(a)}{n!} (x-a)^n} + \frac{f^{(k)}(a+\theta (x-a))}{k!} (x-a)^k$$

#L'Hospitalの定理
$c,L$を実数または$\pm\infty$とする。
1回微分可能な関数$f,g$について、次のどちらかが成り立つとする。

$\displaystyle \lim_{x \to c} f(x) = \lim_{x \to c} g(x) = 0$

$\displaystyle \lim_{x \to c} f(x) = \pm \lim_{x \to c} g(x) = \pm \infty$

このとき、$c$付近で$g'(x) \neq 0$であり、

$\displaystyle \lim_{x \to c} \frac{f'(x)}{g'(x)} = L$

が存在すれば、

$\displaystyle \lim_{x \to c} \frac{f(x)}{g(x)} = L$

となる。

#接平面の方程式
関数$F(x,y,z)$について、曲面$F(x,y,z)=0$上の点$(x_0,y_0,z_0)$における接平面の方程式は次のようになる。

$$\displaystyle (x-x_0) \frac{\partial F}{\partial x}(x_0,y_0,z_0) + (y-y_0) \frac{\partial F}{\partial y}(x_0,y_0,z_0) + (z-z_0) \frac{\partial F}{\partial z}(x_0,y_0,z_0)=0$$

\newpage

#2変数関数の極値
2変数関数$f(x,y)$について  

* 関数$f$が点$(a,b)$で極値をとるならば$f_x(a,b)=f_y(a,b)=0$  
* $f_x(a,b)=f_y(a,b)=0$ならば点$(a,b)$は関数$f$の停留点である  
* 停留点$(a,b)$について、$D=f_{xx}(a,b) f_{yy}(a,b) - f_{xy}(a,b)^2$とすると、  
    $D<0$ならば停留点は極値ではない  
    $D>0$ならば停留点は極値である  
\ \ \ \ \ \ \ \ $f_{xx}(a,b)>0\ (f_{yy}(a,b)>0)$ならば極値は極小値  
\ \ \ \ \ \ \ \ $f_{xx}(a,b)<0\ (f_{yy}(a,b)<0)$ならば極値は極大値  
    $D=0$ならば判定不能  

#Jacobi行列とJacobian

#定義
次のような$(m,n)$行列をJacobi行列と呼ぶ。  
$$\displaystyle \frac{\partial(f_1,\cdots,f_m)}{\partial(x_1,\cdots,x_n)}=
\begin{pmatrix}
    \frac{\partial f_1}{\partial x_1}	&\cdots	&\frac{\partial f_1}{\partial x_n}	\\
    \vdots				&\ddots	&\vdots					\\
    \frac{\partial f_m}{\partial x_1}	&\cdots	&\frac{\partial f_m}{\partial x_n}	
\end{pmatrix}$$
  
Jacobi行列の行列式をJacobianという。  

#変数変換
変数群$(x_1,\cdots,x_m)$,$(y_1,\cdots,y_n)$について、$\drm x_1 \drm x_2 \cdots \drm x_m$を$\drm y_1 \drm y_2 \cdots \drm y_m$に変数変換するとき、次の式が成り立つ。  
$$\displaystyle \drm x_1 \drm x_2 \cdots \drm x_m = \abs{\displaystyle \frac{\partial(x_1,\cdots,x_m)}{\partial(y_1,\cdots,y_n)}} \drm y_1 \drm y_2 \cdots \drm y_m$$

