# Project_2_Numerical_PSI

# Algorithm for Least Square Fit

**Goal:** Given a target function $f\_{\*}(x)$ we want to make a approximate $p$-degree polynomial $f(x) = \Sum\_{i=0}^{p}{b\_i x^i}$. Next we evaluate $(x\_{(1)},x\_{(2)},\cdots,x\_{(n)})$, $n\geq p$ points are beinge evaluated for both $f(x)$ and $f_{\*}(x)$, so that the $RMS$ error got minimized 

$$ \hat{e} = \sqrt{\sum\_{i=0}^{n}\frac{\left(f(x\_{(i)})-f\_{\*}(x\_{(i)})\right)^2}{n}} $$

Lets define 
```math
\bar{b} = \left(\begin{matrix}b\_0\\ b\_1\\ \vdots\\ b\_p \end{matrix}\right)$$, $$\bar{y} = \left(\begin{matrix}f\_\*(x\_{(0)})\\ f\_\*(x\_{(1)})\\ \vdots \\ f\_\*(x\_{(n)})\end{matrix}\right)
```
and 


$$\bar{A} = \left(\begin{matrix} 1 & x\_{(1)} & \cdots & x^{p}\_(1)} \\ 1 & x\_{(2)} & \cdots & x^{p}\_{(2)}\\ \\ \vdots & \ddots & \ddots & \vdots\\ 1 \& x\_{(n)} \& \cdots & x^{p}\_{(n)} \end{matrix} \right)$$.


We can rephrase the problem in maxtrix format like, 

$$ \bar{A} \bar{b} = \bar{y}$$

where $\bar{b}$ contains the coefficient of fitting polynomial $f(x)$. 

This can be represented into geometric language. We can say the best fitting can be achieved, if we can find the best approximation of $\bar{y}$ into the column space of $\bar{A}$ matrix. Pictorially, we represent the column space of $\bar{A}$ spanned by $\vec{OA}$ and $\vec{OB}$ vectors in the following picture and $\bar{y}$ vector by $\vec{OY}$. The best approximation we can find for $\vec{OY}$ with in column space of $\bar{A}$ by projecting $\vec{OY}$ over the hyperspace spanned by $\vec{OA}$ and $\vec{OB}$. Because the "error" vector $\vec{OY}-\vec{OC} = \vec{YC} = {e}$ would have the minimum length ($L^2$ or Euclidean norm) if we project $\vec{OY}$ over the hyperspace. We identify that the previously mentioned $RMS$ error $\hat{e}=\frac{|{e}|}{\sqrt{n}}$.
