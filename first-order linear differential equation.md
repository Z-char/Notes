---
status: writing
category:
  - math
  - differential equation
  - note
related_notes:
  - "[[Math]]"
  - "[[Differential Equation]]"
---
![[Elementary Differential Equations and Boundary Value -- William E_ Boyce, Richard C_ DiPrima, Douglas B_ Meade -- 12, PT, 2021 -- John Wiley & Sons, -- 9781119777670 -- ec7e09570313612f2aa60658e1663b05 -- Anna’s Ar.pdf#page=38&rect=130,30,416,121|Elementary Differential Equations and Boundary Value -- William E_ Boyce, Richard C_ DiPrima, Douglas B_ Meade -- 12, PT, 2021 -- John Wiley & Sons, -- 9781119777670 -- ec7e09570313612f2aa60658e1663b05 -- Anna’s Ar, p.26]]
那么来复习一下一般的一阶线性 ode 怎么处理，因为学过，所以我不太想看下面的解。
考虑下面的更一般的柿子，这个 $\frac{dy}{dt}, y$ 的东西是不是在乘积求导里面见过？所以如果这个东西形如：
$$
A(t) \frac{\mathrm{dy}}{\mathrm{d}t} + \frac{\mathrm{d}A(t)}{\mathrm{d}t} y = G(t)
$$

^aaa1db

在 [[#^aaa1db]] 里，左边很显然可以看作 $Ay$ 的求导，因此两边积分，左边应该得到 $Ay$，右边是一个和 $t$ 有关的函数，把 $A$ 除过去可以得到 $y$，然而，我们不能保证一开始的两个系数恰好是微分关系，因此，我们可以考虑乘上一个系数，使得 $Q(t) \times F(t) = \left( P(t) \times F(t) \right)'$。

于是就可以开始实验了！

![[attachments/Drawing 2025-09-11 00.39.01.excalidraw]]
成功解决！和题解是一样的结果！说明一般的一阶线性微分方程应该就可以这么解决吧？不过过程中有两个难点，首先就是积分因子，需要一次积分来计算，一般的函数未必有简明的积分形式，然后右边也需要积分一次，这些问题可能要哦，事实上，我们也需要处理其他问题，比如说，这个解就是所有解嘛？这将会在未来的学习中见到。

upd: 2025-09-19
> [!theorem] Existence and Uniqueness Theorem for first-order linear equations
> If the functions $p$ and $g$ are continuous on an open interval $I:\alpha \lt t \lt \beta$ containing the point $t=t_{0}$, then there exists a unique function $y = \phi(t)$ that satisfied the differential equation.
> $$
> y' + p(t)y = g(t)
> $$
> for each $t$ in $I$, and that also satisfied the initial condition
> $$
> y(t_{0}) = y_{0}
> $$
> where $y_{0}$ is an arbitrary prescribed initial value.

这里我暂时我不讨论证明，大抵会在未来学习（最近比较忙？要学一些东西和写一些项目，在学习进阶微分方程内容的时候会学习的，毕竟书里也说会在更进阶的课程探讨。