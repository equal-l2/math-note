\newcommand{\trans}[1]{{}^t\! #1}
\newcommand{\rank}[1]{\mathrm{rank}#1}

#転置行列の性質
転置行列とは、ある行列の行と列を反転させたものである。

* $\trans{(\trans{A})}=A$
* $\trans{(A+B)}=\trans{A}+\trans{B}$
* $\trans{(AB)}=\trans{B}\trans{A}$

#行列式の性質
行列式は、正方行列に対して定義される量である。  
正方行列
$A=
\begin{vmatrix}
    a_{11}	&\cdots	&a_{1n} \\
    \vdots	&	&\vdots \\
    a_{n1}	&\cdots	&a_{nn} \\
\end{vmatrix}$
について

##基本性質
* $|\trans{A}|=|A|$
* 適当な行列$B$について$|AB|=|A| |B|$

##列に対する性質
* 行列の任意の2列を交換すると行列式の符号が変わる  
$\begin{vmatrix}
    a_{11}	&\cdots	&a_{1i}	&\cdots	&a_{1j}	&\cdots	&a_{1n} \\
    \vdots	&	&\vdots	&	&\vdots	&	&\vdots \\
    a_{n1}	&\cdots	&a_{ni}	&\cdots	&a_{nj}	&\cdots	&a_{nn} \\
\end{vmatrix}
=-
\begin{vmatrix}
    a_{11}	&\cdots	&a_{1j}	&\cdots	&a_{1i}	&\cdots	&a_{1n} \\
    \vdots	&	&\vdots	&	&\vdots	&	&\vdots \\
    a_{n1}	&\cdots	&a_{nj}	&\cdots	&a_{ni}	&\cdots	&a_{nn} \\
\end{vmatrix}$  

* 次の式が成り立つ  
$\begin{vmatrix}
    a_{11}	&\cdots	&a_{1i}+b_{1i}	&\cdots	&a_{1n} \\
    \vdots	&	&\vdots		&	&\vdots \\
    a_{n1}	&\cdots	&a_{ni}+b_{ni}	&\cdots	&a_{nn} \\
\end{vmatrix} =
\begin{vmatrix}
    a_{11}	&\cdots	&a_{1i}	&\cdots	&a_{1n} \\
    \vdots	&	&\vdots	&	&\vdots \\
    a_{n1}	&\cdots	&a_{ni}	&\cdots	&a_{nn} \\
\end{vmatrix} +
\begin{vmatrix}
    a_{11}	&\cdots	&b_{1i}	&\cdots	&a_{1n} \\
    \vdots	&	&\vdots	&	&\vdots \\
    a_{n1}	&\cdots	&b_{ni}	&\cdots	&a_{nn} \\
\end{vmatrix}$

* 第1列が先頭要素を除いて全て0ならば、次の式が成り立つ  
$\begin{vmatrix}
    a_{11}	&a_{12} &\cdots	&a_{1n} \\
    0		&a_{22} &\cdots	&a_{2n} \\
    \vdots	&\vdots	&	&\vdots	\\
    0		&a_{n2}	&\cdots	&a_{nn} \\
\end{vmatrix}
=a_{11}
\begin{vmatrix}
    a_{22}	&\cdots	&a_{2n} \\
    \vdots	&	&\vdots	\\
    a_{n2}	&\cdots	&a_{nn} \\
\end{vmatrix}$  
  

上の3つから次の性質もわかる  

* 行列に全要素が0の列があれば行列式の値は0
* 行列に同一の2列があれば行列式の値は0
* 行列のある列を$k\ (\neq 0)$倍すると、行列式の値も$k$倍になる  
$\begin{vmatrix}
    a_{11}	&\cdots	&k a_{1i}	&\cdots	&a_{1n} \\
    \vdots	&	&\vdots		&	&\vdots \\
    a_{n1}	&\cdots	&k a_{ni}	&\cdots	&a_{nn} \\
\end{vmatrix} =k
\begin{vmatrix}
    a_{11}	&\cdots	&a_{1i}	&\cdots	&a_{1n} \\
    \vdots	&	&\vdots	&	&\vdots \\
    a_{n1}	&\cdots	&a_{ni}	&\cdots	&a_{nn} \\
\end{vmatrix}$  

* 行列のある列の任意倍を**他**の一列に加えても行列式の値は同じ  
$\begin{vmatrix}
    a_{11}	&\cdots	&a_{1i}+k a_{1j}	&\cdots	&a_{1j}	&\cdots	&a_{1n} \\
    \vdots	&	&\vdots			&	&\vdots	&	&\vdots \\
    a_{n1}	&\cdots	&a_{ni}+k a_{nj}	&\cdots	&a_{nj}	&\cdots	&a_{nn} \\
\end{vmatrix} =
\begin{vmatrix}
    a_{11}	&\cdots	&a_{1i}	&\cdots	&a_{1j}	&\cdots	&a_{1n} \\
    \vdots	&	&\vdots	&	&\vdots	&	&\vdots \\
    a_{n1}	&\cdots	&a_{ni}	&\cdots	&a_{nj}	&\cdots	&a_{nn} \\
\end{vmatrix}$

以上の性質は列についても同様に成り立つ。

#階数
行列$A$を行基本変形によって階段行列に変形したとき、全要素が0でない行の数を行列$A$の階数といい、$\rank{A}$で表す。  

* $(m,n)$行列$A$について、$\rank{A}\leq m,n$となる。  

#逆行列と正則行列
$n$次正方行列$A$と$n$次単位行列$E$について、$A A^{-1} = A^{-1} A = E$を満たす行列$A^{-1}$を$A$の逆行列という。  
逆行列を持つ行列を正則行列という。  
正則行列$A,B$について次の性質が成り立つ。  

* $\trans{A}$は正則行列であり、$(\trans{A})^{-1}=\trans{(A^{-1})}$となる

* $r \neq 0$について、$(rA)^{-1}=\frac1r A^{-1}$となる

* 積$AB$は正則行列であり、$(AB)^{-1}=B^{-1}A^{-1}$となる

#1次独立  
線形空間$V$の$k$個のベクトル$\mathbbm{v}_1 ,\mathbbm{v}_2 ,\cdots ,\mathbbm{v}_k$について、  
$r_1 \mathbbm{v}_1 + r_2 \mathbbm{v}_2 + \cdots + r_k \mathbbm{v}_k = 0$  
が$r_1,r_2,\cdots,r_k$について自明な解しか持たないとき、これらのベクトルの組は1次独立であるという。  
ベクトルの組が1次独立でないとき、1次従属であるという。  
1次従属であるときは、ベクトルの組の中の少なくとも1個が他のベクトルの線型結合で表される。  
* 線形空間$V$の$k$個のベクトル$\mathbbm{v}_1 ,\mathbbm{v}_2 ,\cdots ,\mathbbm{v}_k$が1次独立であるための必要条件は、これらのベクトルからなる行列$A=(\mathbbm{v}_1 ,\mathbbm{v}_2 ,\cdots ,\mathbbm{v}_k)$について$\rank{A}=k$である。  

* $\mathbb{R}^n$の$n$個のベクトル$\mathbbm{v}_1 ,\mathbbm{v}_2 ,\cdots ,\mathbbm{v}_n$について、$A=(\mathbbm{v}_1 ,\mathbbm{v}_2 ,\cdots ,\mathbbm{v}_n)$とおくと、次は同値である。  
    * $\mathbbm{v}_1 ,\mathbbm{v}_2 ,\cdots ,\mathbbm{v}_n$は1次独立である
    * $\rank{A}=n$
    * $|A| \neq 0$
    * $A$は正則行列である
