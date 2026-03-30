---
category:
  - physics
  - differential equation
  - vibration
---
震动，启动！
![[Elementary Differential Equations and Boundary Value -- William E_ Boyce, Richard C_ DiPrima, Douglas B_ Meade -- 12, PT, 2021 -- John Wiley & Sons, -- 9781119777670 -- ec7e09570313612f2aa60658e1663b05 -- Anna’s Ar.pdf#page=164&rect=38,270,330,341|Elementary Differential Equations and Boundary Value -- William E_ Boyce, Richard C_ DiPrima, Douglas B_ Meade -- 12, PT, 2021 -- John Wiley & Sons, -- 9781119777670 -- ec7e09570313612f2aa60658e1663b05 -- Anna’s Ar, p.152]]
形如没有阻尼的震动，是不是不难解的 $r = \pm j \sqrt{ \frac{k}{m} }$，因此就有方程形如：
$$
u = A\cos(\omega_{0} t) + B \sin(\omega_{0} t)
$$
其中 $\omega_{0}^{2} = \frac{k}{m}$，其实辅助角公式还支持我们写成：
$$
u = R\cos(\omega_{0}t - \delta)
$$
其中有：
$$
R = \sqrt{ A^{2} + B^{2} }, \tan(\delta) = \frac{B}{A}
$$
那个频率就叫自然频率了，相位和振幅就不解释了，然后这就是最简单的简谐运动。
然而显而易见的，现实中都会有空气阻力，所以加入阻尼就有如下的：
![[Elementary Differential Equations and Boundary Value -- William E_ Boyce, Richard C_ DiPrima, Douglas B_ Meade -- 12, PT, 2021 -- John Wiley & Sons, -- 9781119777670 -- ec7e09570313612f2aa60658e1663b05 -- Anna’s Ar.pdf#page=166&rect=40,250,328,294|Elementary Differential Equations and Boundary Value -- William E_ Boyce, Richard C_ DiPrima, Douglas B_ Meade -- 12, PT, 2021 -- John Wiley & Sons, -- 9781119777670 -- ec7e09570313612f2aa60658e1663b05 -- Anna’s Ar, p.154]]
这个，很显然啊，解依赖于 $m, \gamma, k$，然后根据常识可知，最后这个 $u$ 大概就是 0 了，因为震动过程中一直在被阻尼阻挡，因此消耗能量，当有两个实根的时候，无论是相等还是不相等，我们知道都是形如 $e^{rt}$ 的形式，那其实就没啥好聊的了，就是经典的指数函数罢了，除了最后一种，我们知道带虚数的 $\exp$ 其实是 $\sin, \cos$，因此这个东西会震荡，就比较有趣。
![[Pasted image 20251017214158.png]]
那么 $\mu$ 就是振荡频率，也可以得到对应的周期，然后特别的，如果判别式和 0 很接近：
![[Pasted image 20251017214413.png]]
你发现判别式很小的时候，也就是阻尼实际上满足 $\frac{\gamma^{2}}{4km}$ 很小的时候，这种情况下仅仅是很小的减少了频率，稍微拉长了周期，于是我们认为这种情况是阻尼比较小的，随着这个东西增大，也就是阻尼增大，慢慢的频率就是 0 了，周期变成无穷了，当增加的两个实根的时候，这个阻尼叫恰好的，如果两个不同，这个时候就是过阻尼了。
可以简单理解一个弹簧，如果阻尼太大，也就是过阻尼，那么这个根本动不了，如果阻尼太小，他就会反复移动，如果阻尼适中，那么频率就是 0，在恰好和过阻尼的时候，都最多穿过最终线一次，毕竟形如指数函数。
电路，也是类似的：
![[Pasted image 20251017215218.png]]
那么既然是环路，直接 kvl，列出来就有：
![[Pasted image 20251017215354.png]]
形式和上面那个基本上完全一样，于是可以直接套用，发现也是形如震荡的电路，如果不考虑右边的激励，于是 $R$ 形如那个阻尼，$L$ 形如那个质量，$\frac{1}{C}$ 形如那个弹力。
然后显然，我们希望能考虑一下带有激励的电路，或者震动，一个自然的想法是周期激励，这是显然的因为我们之前的都是周期运动啦（。
![[Pasted image 20251017215610.png]]
于是就是想研究这个。
很显然答案形如 $u_{c}(t) + U(t)$，其中通解部分是我们上面讨论过的。
根据待定系数法，其实有 $U(t) = A\cos(\omega t) + B\cos(\omega t)$。
![[Pasted image 20251017215945.png]]
这是某一个具体问题，其实就是说，一开始的初值，由于一定带一个 $e^{-t}$ 的东西，所以很快就没有影响了，只有那个一直输入的力还在影响。
也就是 $U(t)$。
由于它的形式，辅助角就可以写成：
$$
U(t) = R \cos(\omega t - \delta)
$$
然后满足如下式子：
$$
R = \frac{F_{0}}{\Delta}, \cos(\delta) = \frac{m(\omega_{0}^2 - \omega^2)}{\Delta}, \sin(\delta) = \frac{{\gamma \omega}}{\Delta}
$$
其中：
$$
\Delta = \sqrt{ m^{2} (\omega_{0}^2 - \omega^2)^2 + \gamma^2\omega^2 }, \; \; \; \; \text{and  } \omega_{0}^2 = \frac{k}{m}
$$
![[Pasted image 20251017221212.png]]
然后我们考虑和单纯的外力有什么关系，很显然，如果单纯外力频率很小，那么基本上就是外力，如果外力频率很高，那么基本上就互相抵消。
第一段基本上表达了这个观点，第二段则是我们有点好奇最大的 $R$ 难道不会超过 $\frac{F_{0}}{k}$ 吗，那好像这个没啥用，于是我们算了算，发现这是一个比原系统频率稍微小的外力频率，如果 $\frac{\gamma^{2}}{mk} \gt 2$，也就是说，阻尼比较大，虽然还没到最大的级别，也就是有实根，但是这种情况下已经很大了，此时外力也拗不过内部阻尼，因此频率越大这个震动幅度越小，基本上可以理解为，不如常力。
当阻尼比较小的时候，取这个极值的时候，你发现 $R_{max}$ 其实很大，即使输入很小，但是这个阻尼可以极大的放大这个输入，这个现象叫做共振。
![[Pasted image 20251017222209.png]]
首先可以注意到就是如果是两个实根，那么已经满足上面的条件($\Gamma = 2$)，因此不会有共振了，不如恒力。
然后如果是两个虚根，那么会出现共振峰，阻尼越小共振越猛。
然后我们可能想研究那么这个和输入的延迟是多少呢？
![[Pasted image 20251017222504.png]]
如果他们是共振的，则无论如何只延迟四分之一个周期。当外力越慢，系统越能跟上，因此延迟小，反之几乎反相。对于大阻尼，外力输入如同泥牛入海，因此不会太容易变相，也就是不太敏感。
