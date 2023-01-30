# Project_2_Numerical_PSI

# Algorithm for Least Square Fit

**Goal:** Given a target function $f\_{\*}(x)$ we want to make a approximate $p$-degree polynomial $f(x) = \sum_{i=0}^p{b_i x^i}$. Next we evaluate $(x\_{(1)},x\_{(2)},\cdots,x\_{(n)})$, $n\geq p$ points are beinge evaluated for both $f(x)$ and $f_{\*}(x)$, so that the $RMS$ error got minimized 

$$ \hat{e} = \sqrt{\sum\_{i=0}^{n}\frac{\left(f(x\_{(i)})-f\_{\*}(x\_{(i)})\right)^2}{n}} $$

Lets define 
```math
\bar{b} = \left(\begin{matrix}b_0\\ b_1\\ \vdots\\ b_p \end{matrix}\right), \bar{y} = \left(\begin{matrix}f_*(x_{(0)})\\ f_*(x_{(1)})\\ \vdots \\ f_*(x_{(n)})\end{matrix}\right)
```
and 

```math
\bar{A} = \left(\begin{matrix} 1 & x_{(1)} & \cdots & x^{p}_{(1)} \\ 1 & x_{(2)} & \cdots & x^{p}_{(2)}\\ \\ \vdots & \ddots & \ddots & \vdots\\ 1 \& x_{(n)} \& \cdots & x^{p}_{(n)} \end{matrix} \right).
```

We can rephrase the problem in maxtrix format like, 

$$ \bar{A} \bar{b} = \bar{y}$$

where $\bar{b}$ contains the coefficient of fitting polynomial $f(x)$. 

This can be represented into geometric language. We can say the best fitting can be achieved, if we can find the best approximation of $\bar{y}$ into the column space of $\bar{A}$ matrix. Pictorially, we represent the column space of $\bar{A}$ spanned by $\vec{OA}$ and $\vec{OB}$ vectors in the following picture and $\bar{y}$ vector by $\vec{OY}$. The best approximation we can find for $\vec{OY}$ with in column space of $\bar{A}$ by projecting $\vec{OY}$ over the hyperspace spanned by $\vec{OA}$ and $\vec{OB}$. Because the "error" vector $\vec{OY}-\vec{OC} = \vec{YC} = {e}$ would have the minimum length ($L^2$ or Euclidean norm) if we project $\vec{OY}$ over the hyperspace. We identify that the previously mentioned $RMS$ error $\hat{e}=\frac{|{e}|}{\sqrt{n}}$.
