---
status: writing
category:
  - math
  - differential equation
  - solution report
related_notes:
  - "[[first-order linear differential equation]]"
---
![[Elementary Differential Equations and Boundary Value -- William E_ Boyce, Richard C_ DiPrima, Douglas B_ Meade -- 12, PT, 2021 -- John Wiley & Sons, -- 9781119777670 -- ec7e09570313612f2aa60658e1663b05 -- Anna’s Ar.pdf#page=45&rect=46,104,235,162|Elementary Differential Equations and Boundary Value -- William E_ Boyce, Richard C_ DiPrima, Douglas B_ Meade -- 12, PT, 2021 -- John Wiley & Sons, -- 9781119777670 -- ec7e09570313612f2aa60658e1663b05 -- Anna’s Ar, p.33]]
这里就不纸笔了，正好练习一下 latex suite。

第一题，积分因子直接是 $\exp \left( \int 3 \mathrm{d}t \right) = \exp \left( 3t \right)$，右边那一坨乘上这个直接积分，左边很显然可以分部积分做一下，对吧，然后都只剩下一个 $\exp$ 求积分，那是显然的，最后加上常数两边除掉积分因子即可。
第二题，积分因子也一样的东西，一乘右边是个 $t^{2}$，直接积分就行，最后加常数除掉积分因子。
第三题，右边那一坨也是好做的我就不继续做了。
第四题，我嘞个 tri 和 exp 大决斗，感性上就是分部积分做两次，然后可以设做 $I$ 解出来，还是自己手算一下放心。
$$
\begin{align}
\mu \left( x \right) &= \exp \int \left( \frac{1}{t} \mathrm{d}t \right) = \exp \ln t = t \\
\int 3\cos(2t) t \mathrm{d}t &= \frac{3}{2} \sin(2t)t - \frac{2}{3}\int \sin(2t) \mathrm{d}t
\end{align}
$$
哦不是 exp 和 tri 大乱斗，那我算到这里就不继续算了，余下内容不难。
第五题，右边是个 $\exp$，做完。
第六题，先要干掉一个 $t$，然后积分因子又丢回去了，直接积分就行。
第七题，擦，这回真是 tri exp 大乱斗了，开算。
$$
\begin{align}
\mu \left( x \right) &= \exp \int 1 \mathrm{d}t = \exp t \\
\int \sin \left( 2t \right) \exp t \mathrm{d}t &= \exp t \sin(2t) - 2\int \exp t \cos(2t) \mathrm{d}t \\
&= \exp t \sin (2t) -2 \exp t \cos(2t) -4 \int \exp t \sin(2t) \\
\end{align}
$$
两个积分整合一下，然后除掉就行了。
第八个经典东西了，换个元就行了。
![[Elementary Differential Equations and Boundary Value -- William E_ Boyce, Richard C_ DiPrima, Douglas B_ Meade -- 12, PT, 2021 -- John Wiley & Sons, -- 9781119777670 -- ec7e09570313612f2aa60658e1663b05 -- Anna’s Ar.pdf#page=45&rect=42,40,237,86|Elementary Differential Equations and Boundary Value -- William E_ Boyce, Richard C_ DiPrima, Douglas B_ Meade -- 12, PT, 2021 -- John Wiley & Sons, -- 9781119777670 -- ec7e09570313612f2aa60658e1663b05 -- Anna’s Ar, p.33]]
第九题，丢过去然后 ibp，然后带入解 c。
第十题，直接干没了，对 $t$ 求积分很好做。
第十一题，坏了，这积分怎么做。要不然直接带着积分好了，感觉好难啊。哎呀我要被自己气死了，怎么 $\exp \ln t = t$ 而不是 1 啊，我是什么神人了。那右边直接做了。
第十二题，好做的吧，就是要求一个 $\exp t \times t$ 的积分。
哎后面有一大堆让解方程的，看起来没有什么新科技，我就不管了，如果有肯定会提示吧。
![[Pasted image 20250914221337.png]]
接下来看看这个题，然后这个题之前给过解，但是是一个带积分符号的解。
![[Pasted image 20250914221407.png]]
前面那一坨肯定是 0 形式，后面那一坨肯定是 inf 形式，擦，所以用洛做吗。
洛的前提忘了，总之这个是显然的好函数，所以直接洛即可。
![[Pasted image 20250914221828.png]]
这一类题型，有点新喔，我来研究一下。
首先一个自然的想法就是取这个函数的同族，但是真的趋近吗，并没有因为恒有差距。
但是鉴于 23 题给了这样的性质：
![[Pasted image 20250914222346.png]]
我们可能考虑从这个函数变形。
感觉也很难处理，还是考虑普遍意义上一阶线性微分方程的解吧。
![[Pasted image 20250914222518.png]]
对着这个看，首先我们希望这个 c 被干掉，也就是不同 c 后续不产生影响，那自然就有 $\mu \left( t \right)$ 这个东西，最好是递增的，为了简洁，我们不妨就让他是 $t$，那么此时 $a$ 取 $\frac{1}{t}$ 即可，那么现在就是要给一个 $g$，使得 $\int t g(t) / t$ 是我们想要的函数，由于题目里面都是简明的多项式函数，自然不难。
找了一个题解，感觉有点变态啊，好像就是考虑，当 $t \to \infty$ 的时候，如果 $y$ 是这么一个函数，那么 $y' + y$ 是什么东西，然后我们宣布反解就能满足，这有道理吗，形式化的说，如果：
$$
\begin{align}
\lim_{ t \to \infty } y = f(t) \\
y + y' = f(t) + f'(t)
\end{align}
$$

^8d4242

那么解 [[#^8d4242]] 中的下式，则满足上式。 
我擦，怎么这么对，首先一个特解显然是 $f(t)$，对吧，然后考虑通解，那么转齐次就有 $y' = -y, y = C\exp \left( -t \right)$，然后这个随着 $t$ 增大就没了。

 