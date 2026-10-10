# 4장. 바구니 크기

## 동호회

가게가 늘어나는 사이 수집가도 많아졌다. 수집가들은 취향의 방향이 같은 사람끼리 모여 동호회를 만들었다. 사과를 좋아하는 정도가 달라도 같은 '사과' 동호회에 들어갔다.

같은 동호회 사람들의 바구니가 모두 같지는 않았다. ‘사과’ 수집가는 $[1,0,0,0]$을, ‘사과 2개’ 수집가는 $[2,0,0,0]$을 들고 있었다.

$$
\begin{gathered}
\begin{aligned}
k &= {\color{RoyalBlue}2} && (k \in \mathbb{R}:\text{ 배율(스칼라)}) \\[6pt]
u &= [{\color{DarkOrange}1, 0, 0, 0}] && \text{'사과' 수집가의 바구니} \\
v &= [2, 0, 0, 0] && \text{'사과 2개' 수집가의 바구니}
\end{aligned} \\[12pt]
\begin{aligned}
ku &= {\color{RoyalBlue}2} \cdot [{\color{DarkOrange}1, 0, 0, 0}] \\
   &= [{\color{RoyalBlue}2} \times {\color{DarkOrange}1}, {\color{RoyalBlue}2} \times {\color{DarkOrange}0}, {\color{RoyalBlue}2} \times {\color{DarkOrange}0}, {\color{RoyalBlue}2} \times {\color{DarkOrange}0}] \\
   &= [2, 0, 0, 0] \\
   &= v
\end{aligned}
\end{gathered}
$$

좋아하는 정도는 달라도, 두 수집가 모두 사과를 좋아했다.

### 대표 바구니

동호회가 늘자 새로 온 수집가는 자기 취향에 맞는 동호회를 찾기 어려워졌다.
그래서 동호회들은 취향을 대표하는 바구니를 하나씩 문밖에 걸고, 같은 바구니를 들고 오는 사람을 받기로 했다.

‘사과’ 동호회는 대표 바구니 $[1,0,0,0]$을 문밖에 걸어 두었다. 하지만 ‘사과 2개’ 수집가는 같은 사과 취향인데도, 바구니의 개수가 대표 바구니와 달라 가입할 수 없었다.

$$
\begin{array}{c@{\qquad}c@{\qquad}c}
\text{동호회의 대표 바구니} & & \text{가입하려는 수집가의 바구니} \\[8pt]
[1, 0, 0, 0] & \ne & [2, 0, 0, 0]
\end{array}
$$

바구니가 똑같은지만 비교해서는 취향의 방향이 같은지 알 수 없었다.

좋아하는 정도가 달라도 같은 동호회에 들어올 수 있어야 했다.
사람들은 각자의 바구니를 줄이거나 불려 같은 대표 바구니로 맞추기로 했다.

## 개수 합으로 나누기

먼저 ‘사과’ 수집가와 ‘사과 2개’ 수집가의 바구니를 각각 과일 개수의 합으로 나눠 보았다.

$$
\begin{array}{l@{\qquad}l}
\text{수집가의 바구니와 개수 합} & \text{나누기} \\[8pt]
\text{'사과' 수집가} & \\[4pt]
u = [{\color{RoyalBlue}1, 0, 0, 0}] & \dfrac{u}{k} \\[6pt]
\begin{aligned}k &= 1 + 0 + 0 + 0 \\ &= 1\end{aligned} & = \dfrac{[{\color{RoyalBlue}1, 0, 0, 0}]}{{\color{DarkOrange}1}} \\[6pt]
 & = \left[\dfrac{{\color{RoyalBlue}1}}{{\color{DarkOrange}1}}, \dfrac{{\color{RoyalBlue}0}}{{\color{DarkOrange}1}}, \dfrac{{\color{RoyalBlue}0}}{{\color{DarkOrange}1}}, \dfrac{{\color{RoyalBlue}0}}{{\color{DarkOrange}1}}\right] \\[6pt]
 & = [1, 0, 0, 0] \\[12pt]
\text{'사과 2개' 수집가} & \\[4pt]
v = [{\color{RoyalBlue}2, 0, 0, 0}] & \dfrac{v}{l} \\[6pt]
\begin{aligned}l &= 2 + 0 + 0 + 0 \\ &= 2\end{aligned} & = \dfrac{[{\color{RoyalBlue}2, 0, 0, 0}]}{{\color{DarkOrange}2}} \\[6pt]
 & = \left[\dfrac{{\color{RoyalBlue}2}}{{\color{DarkOrange}2}}, \dfrac{{\color{RoyalBlue}0}}{{\color{DarkOrange}2}}, \dfrac{{\color{RoyalBlue}0}}{{\color{DarkOrange}2}}, \dfrac{{\color{RoyalBlue}0}}{{\color{DarkOrange}2}}\right] \\[6pt]
 & = [1, 0, 0, 0]
\end{array}
$$

좋아하는 정도가 달랐던 두 수집가의 바구니가 같아졌다.

이번에는 ‘사과 3개 바나나 4개’ 수집가와 ‘사과 6개 바나나 8개’ 수집가의 바구니로 해 보았다.
두 사람도 좋아하는 정도는 달랐지만, 사과와 바나나를 좋아하는 비율은 같았다.

$$
\begin{array}{l@{\qquad}l}
\text{수집가의 바구니와 개수 합} & \text{나누기} \\[8pt]
\text{'사과 3개 바나나 4개' 수집가} & \\[4pt]
u = [{\color{RoyalBlue}3, 4, 0, 0}] & \dfrac{u}{k} \\[6pt]
\begin{aligned}k &= 3 + 4 + 0 + 0 \\ &= 7\end{aligned} & = \dfrac{[{\color{RoyalBlue}3, 4, 0, 0}]}{{\color{DarkOrange}7}} \\[6pt]
 & = \left[\dfrac{{\color{RoyalBlue}3}}{{\color{DarkOrange}7}}, \dfrac{{\color{RoyalBlue}4}}{{\color{DarkOrange}7}}, \dfrac{{\color{RoyalBlue}0}}{{\color{DarkOrange}7}}, \dfrac{{\color{RoyalBlue}0}}{{\color{DarkOrange}7}}\right] \\[6pt]
 & = \left[\dfrac37, \dfrac47, 0, 0\right] \\[12pt]
\text{'사과 6개 바나나 8개' 수집가} & \\[4pt]
v = [{\color{RoyalBlue}6, 8, 0, 0}] & \dfrac{v}{l} \\[6pt]
\begin{aligned}l &= 6 + 8 + 0 + 0 \\ &= 14\end{aligned} & = \dfrac{[{\color{RoyalBlue}6, 8, 0, 0}]}{{\color{DarkOrange}14}} \\[6pt]
 & = \left[\dfrac{{\color{RoyalBlue}6}}{{\color{DarkOrange}14}}, \dfrac{{\color{RoyalBlue}8}}{{\color{DarkOrange}14}}, \dfrac{{\color{RoyalBlue}0}}{{\color{DarkOrange}14}}, \dfrac{{\color{RoyalBlue}0}}{{\color{DarkOrange}14}}\right] \\[6pt]
 & = \left[\dfrac37, \dfrac47, 0, 0\right]
\end{array}
$$

이번에도 두 바구니가 같아졌고, 과일 개수의 합은 1이 되었다.

이번에는 사과를 좋아하고 두리안을 싫어하는 수집가의 바구니를 과일 개수의 합으로 나눠 보았다.

$$
\begin{aligned}
v &= [1, 0, 0, -1] \qquad \text{두리안을 싫어하는 '사과' 수집가의 바구니} \\[6pt]
k &= 1 + 0 + 0 + (-1) \\
  &= 0
\end{aligned}
$$

바구니는 비어 있지 않았지만, 개수 합이 0이라 나눌 수 없었다.

두리안을 더 싫어하는 수집가의 바구니에서는 다른 문제가 생겼다.

$$
\begin{array}{l@{\qquad}l}
\text{수집가의 바구니와 개수 합} & \text{나누기} \\[8pt]
\text{두리안을 몹시 싫어하는 '사과' 수집가} & \\[4pt]
v = [{\color{RoyalBlue}1, 0, 0, -2}] & \dfrac{v}{k} \\[6pt]
\begin{aligned}k &= 1 + 0 + 0 + (-2) \\ &= -1\end{aligned} & = \dfrac{[{\color{RoyalBlue}1, 0, 0, -2}]}{{\color{DarkOrange}-1}} \\[6pt]
 & = \left[\dfrac{{\color{RoyalBlue}1}}{{\color{DarkOrange}-1}}, \dfrac{{\color{RoyalBlue}0}}{{\color{DarkOrange}-1}}, \dfrac{{\color{RoyalBlue}0}}{{\color{DarkOrange}-1}}, \dfrac{{\color{RoyalBlue}-2}}{{\color{DarkOrange}-1}}\right] \\[6pt]
 & = [-1, 0, 0, 2]
\end{array}
$$

개수 합이 $-1$이라 나눌 수는 있었다. 하지만 원래의 취향이 유지되지 않았다.

## 저울에 단 값으로 나누기

사람들은 빈 바구니가 아니면 맞단 값이 항상 양수였다는 사실을 떠올렸다. 이 값이라면 어떤 취향의 바구니든 방향을 유지하며 나눌 수 있었다.

먼저 ‘사과’ 수집가와 ‘사과 2개’ 수집가의 바구니를 각각 맞달아, 나눌 값을 구했다.

$$
\begin{array}{l@{\qquad}l}
\text{수집가의 바구니} & \text{맞단 값} \\[8pt]
\text{'사과' 수집가} & \\[4pt]
u = [1, 0, 0, 0] & k = u \cdot u \\[4pt]
 & = {\color{RoyalBlue}1} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[4pt]
 & = 1 + 0 + 0 + 0 \\[4pt]
 & = 1 \\[12pt]
\text{'사과 2개' 수집가} & \\[4pt]
v = [2, 0, 0, 0] & l = v \cdot v \\[4pt]
 & = {\color{RoyalBlue}2} \times {\color{DarkOrange}2} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[4pt]
 & = 4 + 0 + 0 + 0 \\[4pt]
 & = 4
\end{array}
$$

두 바구니를 각각 맞단 값으로 나눠 보았다.

$$
\begin{array}{l@{\qquad}l}
\text{수집가의 바구니와 나누는 수} & \text{나누기} \\[8pt]
u = [{\color{RoyalBlue}1, 0, 0, 0}], \quad k = {\color{DarkOrange}1} & \dfrac{u}{k} \\[6pt]
 & = \dfrac{[{\color{RoyalBlue}1, 0, 0, 0}]}{{\color{DarkOrange}1}} \\[6pt]
 & = \left[\dfrac{{\color{RoyalBlue}1}}{{\color{DarkOrange}1}}, \dfrac{{\color{RoyalBlue}0}}{{\color{DarkOrange}1}}, \dfrac{{\color{RoyalBlue}0}}{{\color{DarkOrange}1}}, \dfrac{{\color{RoyalBlue}0}}{{\color{DarkOrange}1}}\right] \\[6pt]
 & = [1, 0, 0, 0] \\[12pt]
v = [{\color{RoyalBlue}2, 0, 0, 0}], \quad l = {\color{DarkOrange}4} & \dfrac{v}{l} \\[6pt]
 & = \dfrac{[{\color{RoyalBlue}2, 0, 0, 0}]}{{\color{DarkOrange}4}} \\[6pt]
 & = \left[\dfrac{{\color{RoyalBlue}2}}{{\color{DarkOrange}4}}, \dfrac{{\color{RoyalBlue}0}}{{\color{DarkOrange}4}}, \dfrac{{\color{RoyalBlue}0}}{{\color{DarkOrange}4}}, \dfrac{{\color{RoyalBlue}0}}{{\color{DarkOrange}4}}\right] \\[6pt]
 & = \left[\dfrac12, 0, 0, 0\right]
\end{array}
$$

두 바구니는 나눈 뒤에도 같아지지 않았다.

바구니가 두 배가 되면 맞단 값은 네 배가 되니, 나누는 수가 바구니보다 더 크게 늘어났다.

두 바구니를 같게 맞추려면 나누는 수도 바구니처럼 두 배가 되어야 했다.

## 제곱근으로 나누기

사람들은 맞단 값 4 대신, 자기 자신과 곱해 4가 되는 양수 2로 나눠 보기로 했다.

과학자들은 이 수를 4의 양의 제곱근(positive square root)이라 부르고 $\sqrt4$로 적었다.

$$
\begin{array}{l@{\qquad}l}
\text{수집가의 바구니} & \text{제곱근과 나누기} \\[8pt]
\text{'사과 2개' 수집가} & \\[4pt]
v = [2, 0, 0, 0] & \\[6pt]
\text{저울에 단 값의 제곱근} & k = \sqrt{v \cdot v} \\[4pt]
 & = \sqrt{{\color{RoyalBlue}2} \times {\color{DarkOrange}2} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0}} \\[4pt]
 & = \sqrt{4 + 0 + 0 + 0} \\[4pt]
 & = \sqrt{4} \\[4pt]
 & = 2 \\[8pt]
\text{그 수로 나누면} & \dfrac{v}{k} \\[6pt]
 & = \dfrac{[{\color{RoyalBlue}2, 0, 0, 0}]}{{\color{DarkOrange}2}} \\[6pt]
 & = \left[\dfrac{{\color{RoyalBlue}2}}{{\color{DarkOrange}2}}, \dfrac{{\color{RoyalBlue}0}}{{\color{DarkOrange}2}}, \dfrac{{\color{RoyalBlue}0}}{{\color{DarkOrange}2}}, \dfrac{{\color{RoyalBlue}0}}{{\color{DarkOrange}2}}\right] \\[6pt]
 & = [1, 0, 0, 0]
\end{array}
$$

이번에는 ‘사과’ 수집가와 ‘사과 2개’ 수집가의 바구니가 같아졌다.

사과와 바나나가 함께 든 두 바구니도 각각 맞단 값의 양의 제곱근으로 나눠 보았다.

$$
\begin{array}{l@{\qquad}l}
\text{수집가의 바구니} & \text{제곱근과 나누기} \\[8pt]
\text{'사과 3개 바나나 4개' 수집가} & \\[4pt]
u = [3, 4, 0, 0] & \\[6pt]
\text{저울에 단 값의 제곱근} & k = \sqrt{u \cdot u} \\[4pt]
 & = \sqrt{{\color{RoyalBlue}3} \times {\color{DarkOrange}3} + {\color{RoyalBlue}4} \times {\color{DarkOrange}4} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0}} \\[4pt]
 & = \sqrt{9 + 16 + 0 + 0} \\[4pt]
 & = \sqrt{25} \\[4pt]
 & = 5 \\[8pt]
\text{그 수로 나누면} & \dfrac{u}{k} \\[6pt]
 & = \dfrac{[{\color{RoyalBlue}3, 4, 0, 0}]}{{\color{DarkOrange}5}} \\[6pt]
 & = \left[\dfrac{{\color{RoyalBlue}3}}{{\color{DarkOrange}5}}, \dfrac{{\color{RoyalBlue}4}}{{\color{DarkOrange}5}}, \dfrac{{\color{RoyalBlue}0}}{{\color{DarkOrange}5}}, \dfrac{{\color{RoyalBlue}0}}{{\color{DarkOrange}5}}\right] \\[6pt]
 & = \left[\dfrac35, \dfrac45, 0, 0\right] \\[16pt]
\text{'사과 6개 바나나 8개' 수집가} & \\[4pt]
v = [6, 8, 0, 0] & \\[6pt]
\text{저울에 단 값의 제곱근} & l = \sqrt{v \cdot v} \\[4pt]
 & = \sqrt{{\color{RoyalBlue}6} \times {\color{DarkOrange}6} + {\color{RoyalBlue}8} \times {\color{DarkOrange}8} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0}} \\[4pt]
 & = \sqrt{36 + 64 + 0 + 0} \\[4pt]
 & = \sqrt{100} \\[4pt]
 & = 10 \\[8pt]
\text{그 수로 나누면} & \dfrac{v}{l} \\[6pt]
 & = \dfrac{[{\color{RoyalBlue}6, 8, 0, 0}]}{{\color{DarkOrange}10}} \\[6pt]
 & = \left[\dfrac{{\color{RoyalBlue}6}}{{\color{DarkOrange}10}}, \dfrac{{\color{RoyalBlue}8}}{{\color{DarkOrange}10}}, \dfrac{{\color{RoyalBlue}0}}{{\color{DarkOrange}10}}, \dfrac{{\color{RoyalBlue}0}}{{\color{DarkOrange}10}}\right] \\[6pt]
 & = \left[\dfrac35, \dfrac45, 0, 0\right]
\end{array}
$$

이번에도 두 바구니가 같아졌다. 바구니가 두 배가 되면 나누는 수도 두 배가 되었기 때문이다.

앞서 개수 합으로 나누지 못했거나 취향이 유지되지 않았던 바구니도, 맞단 값의 양의 제곱근으로 나눠 보았다.

$$
\begin{array}{l@{\qquad}l}
\text{수집가의 바구니} & \text{제곱근과 나누기} \\[8pt]
\text{두리안을 싫어하는 '사과' 수집가} & \\[4pt]
u = [1, 0, 0, -1] & \\[6pt]
\text{저울에 단 값의 제곱근} & k = \sqrt{u \cdot u} \\[4pt]
 & = \sqrt{{\color{RoyalBlue}1} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}(-1)} \times {\color{DarkOrange}(-1)}} \\[4pt]
 & = \sqrt{1 + 0 + 0 + 1} \\[4pt]
 & = \sqrt2 \\[8pt]
\text{그 수로 나누면} & \dfrac{u}{k} \\[6pt]
 & = \dfrac{[{\color{RoyalBlue}1, 0, 0, -1}]}{{\color{DarkOrange}\sqrt2}} \\[6pt]
 & = \left[\dfrac{{\color{RoyalBlue}1}}{{\color{DarkOrange}\sqrt2}}, \dfrac{{\color{RoyalBlue}0}}{{\color{DarkOrange}\sqrt2}}, \dfrac{{\color{RoyalBlue}0}}{{\color{DarkOrange}\sqrt2}}, \dfrac{{\color{RoyalBlue}-1}}{{\color{DarkOrange}\sqrt2}}\right] \\[6pt]
 & = \left[\dfrac{1}{\sqrt2}, 0, 0, -\dfrac{1}{\sqrt2}\right] \\[16pt]
\text{두리안을 몹시 싫어하는 '사과' 수집가} & \\[4pt]
v = [1, 0, 0, -2] & \\[6pt]
\text{저울에 단 값의 제곱근} & l = \sqrt{v \cdot v} \\[4pt]
 & = \sqrt{{\color{RoyalBlue}1} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}(-2)} \times {\color{DarkOrange}(-2)}} \\[4pt]
 & = \sqrt{1 + 0 + 0 + 4} \\[4pt]
 & = \sqrt5 \\[8pt]
\text{그 수로 나누면} & \dfrac{v}{l} \\[6pt]
 & = \dfrac{[{\color{RoyalBlue}1, 0, 0, -2}]}{{\color{DarkOrange}\sqrt5}} \\[6pt]
 & = \left[\dfrac{{\color{RoyalBlue}1}}{{\color{DarkOrange}\sqrt5}}, \dfrac{{\color{RoyalBlue}0}}{{\color{DarkOrange}\sqrt5}}, \dfrac{{\color{RoyalBlue}0}}{{\color{DarkOrange}\sqrt5}}, \dfrac{{\color{RoyalBlue}-2}}{{\color{DarkOrange}\sqrt5}}\right] \\[6pt]
 & = \left[\dfrac{1}{\sqrt5}, 0, 0, -\dfrac{2}{\sqrt5}\right]
\end{array}
$$

빈 바구니가 아니면 나눌 수 있었고, 원래의 취향도 유지되었다.

과학자들은 이 나누는 수를 바구니 **크기**(**노름**, norm)라 불렀다.

$$
\lVert v \rVert = \sqrt{v \cdot v}
$$

사람들은 같은 방향의 바구니를 크기로 나누면 늘 같아지는지 확인했다.

$$
\begin{aligned}
\lVert kv\rVert &= \sqrt{k^2(v\cdot v)} = k\lVert v\rVert \\[6pt]
\dfrac{kv}{\lVert kv\rVert} &= \dfrac{kv}{k\lVert v\rVert} = \dfrac{v}{\lVert v\rVert}
\end{aligned}
\qquad (k>0,\ v\ne 0_V)
$$

바구니를 양의 배율만큼 불리면 크기도 같은 배율만큼 커졌다. 그래서 같은 방향의 바구니는 각각의 크기로 나누면 같아졌다.

## 단위바구니

같은 취향의 바구니들은 하나로 맞춰졌다. 그렇다면 서로 다른 취향의 바구니들도 크기는 같아졌을까?

사람들은 크기로 나눈 바구니들을 각각 맞달아 보았다.

$$
\begin{array}{l@{\qquad}l}
\text{맞춘 바구니} & \text{저울에 단 값(원)과 바구니 크기} \\[8pt]
u_1 = [1, 0, 0, 0] & u_1 \cdot u_1 \\[6pt]
 & = {\color{RoyalBlue}1} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[6pt]
 & = 1 + 0 + 0 + 0 \\[6pt]
 & = 1 \\[8pt]
\text{이 바구니의 크기} & \lVert u_1 \rVert = \sqrt{u_1 \cdot u_1} \\[4pt]
 & = \sqrt1 \\[4pt]
 & = 1 \\[16pt]
u_2 = \left[\dfrac35, \dfrac45, 0, 0\right] & u_2 \cdot u_2 \\[6pt]
 & = {\color{RoyalBlue}\dfrac35} \times {\color{DarkOrange}\dfrac35} + {\color{RoyalBlue}\dfrac45} \times {\color{DarkOrange}\dfrac45} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[6pt]
 & = \dfrac{9}{25} + \dfrac{16}{25} + 0 + 0 \\[6pt]
 & = 1 \\[8pt]
\text{이 바구니의 크기} & \lVert u_2 \rVert = \sqrt{u_2 \cdot u_2} \\[4pt]
 & = \sqrt1 \\[4pt]
 & = 1 \\[16pt]
u_3 = \left[\dfrac{1}{\sqrt2}, 0, 0, -\dfrac{1}{\sqrt2}\right] & u_3 \cdot u_3 \\[6pt]
 & = {\color{RoyalBlue}\dfrac{1}{\sqrt2}} \times {\color{DarkOrange}\dfrac{1}{\sqrt2}} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}\left(-\dfrac{1}{\sqrt2}\right)} \times {\color{DarkOrange}\left(-\dfrac{1}{\sqrt2}\right)} \\[6pt]
 & = \dfrac12 + 0 + 0 + \dfrac12 \\[6pt]
 & = 1 \\[8pt]
\text{이 바구니의 크기} & \lVert u_3 \rVert = \sqrt{u_3 \cdot u_3} \\[4pt]
 & = \sqrt1 \\[4pt]
 & = 1
\end{array}
$$

취향이 달라도 크기로 나눈 바구니의 크기는 모두 1이었다.

과학자들은 크기가 1인 바구니를 **단위바구니**(**단위벡터**, unit vector)라 불렀다. 그리고 바구니를 크기로 나눠 단위바구니로 맞추는 일에는 **정규화**(normalization)라는 이름을 붙였다.

$$
\begin{aligned}
v &\ne 0_V && \text{맞추기 전 바구니} \\[6pt]
u &= \dfrac{v}{\lVert v \rVert} && \text{단위바구니로 맞춘 바구니}
\end{aligned}
$$

좋아하는 정도가 달라도, 같은 취향의 수집가들은 같은 단위바구니를 얻었다.
‘사과’ 수집가와 ‘사과 2개’ 수집가도 이제 같은 동호회에 가입할 수 있었다.

동호회들은 단위바구니를 대표 바구니로 삼아 문밖에 걸었다. 가입하려는 사람은 자기 바구니를 단위바구니로 맞춘 뒤, 그 바구니와 같은 대표 바구니가 걸린 동호회에 들어갔다.

## 취향 차이

자기 단위바구니와 같은 대표 바구니를 찾지 못한 수집가도 있었다. ‘사과 3개 바나나 4개’ 수집가는 ‘사과’ 동호회와도 ‘바나나’ 동호회와도 취향이 달랐다. 그래도 어느 쪽과 더 닮았는지는 알고 싶었다.

수집가는 자기 단위바구니를 두 동호회의 대표 바구니와 각각 저울에 올려 값을 비교했다.

$$
\begin{gathered}
v = \left[\dfrac35, \dfrac45, 0, 0\right] \qquad \text{수집가의 단위바구니} \\[12pt]
\begin{array}{l@{\qquad}l}
\text{동호회의 대표 바구니} & \text{저울에 단 값(원)} \\[8pt]
\text{'사과' 동호회} & \\[4pt]
u_1 = [1, 0, 0, 0] & u_1 \cdot v \\[6pt]
 & = {\color{RoyalBlue}1} \times {\color{DarkOrange}\dfrac35} + {\color{RoyalBlue}0} \times {\color{DarkOrange}\dfrac45} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[6pt]
 & = \dfrac35 + 0 + 0 + 0 \\[6pt]
 & = \dfrac35 \\[12pt]
\text{'바나나' 동호회} & \\[4pt]
u_2 = [0, 1, 0, 0] & u_2 \cdot v \\[6pt]
 & = {\color{RoyalBlue}0} \times {\color{DarkOrange}\dfrac35} + {\color{RoyalBlue}1} \times {\color{DarkOrange}\dfrac45} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[6pt]
 & = 0 + \dfrac45 + 0 + 0 \\[6pt]
 & = \dfrac45
\end{array}
\end{gathered}
$$

모두 크기가 1이므로, 값의 차이는 취향의 방향에서 나왔다. 더 높은 값이 나온 ‘바나나’ 동호회와 취향이 더 닮았다.

사람들은 취향이 같거나 정반대일 때는 어떤 값이 나오는지, ‘사과’ 동호회의 대표 바구니와 다른 단위바구니들을 달아 보았다.

$$
\begin{array}{l@{\qquad}l}
\text{비교하는 단위바구니} & \text{'사과' 동호회와 저울에 단 값(원)} \\[8pt]
\text{같은 '사과' 동호회} & u_1 \cdot u_1 \\[6pt]
u_1 = [1, 0, 0, 0] & = {\color{RoyalBlue}1} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[6pt]
 & = 1 + 0 + 0 + 0 \\[4pt]
\text{취향이 같다} & = 1 \\[12pt]
\text{사과와 바나나를 함께 좋아하는 수집가} & u_1 \cdot v \\[6pt]
v = \left[\dfrac35, \dfrac45, 0, 0\right] & = \dfrac35 \qquad \text{앞에서 계산한 값} \\[4pt]
\text{꽤 닮았다} & \\[12pt]
\text{'바나나' 동호회} & u_1 \cdot u_2 \\[6pt]
u_2 = [0, 1, 0, 0] & = {\color{RoyalBlue}1} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[6pt]
 & = 0 + 0 + 0 + 0 \\[4pt]
\text{서로 무가치하다} & = 0 \\[12pt]
\text{사과를 싫어하는 수집가} & \\[4pt]
w = [-1, 0, 0, 0] & u_1 \cdot w \\[6pt]
 & = {\color{RoyalBlue}1} \times {\color{DarkOrange}(-1)} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[6pt]
 & = -1 + 0 + 0 + 0 \\[4pt]
\text{정반대다} & = -1
\end{array}
$$

같은 바구니끼리 달았을 때는 1, 정반대 바구니끼리는 $-1$이 나왔다. 사과와 바나나를 함께 좋아하는 수집가의 바구니와는 $\tfrac35$, 서로 무가치한 바구니끼리는 0이었다.

단위바구니끼리 저울에 단 값은 언제나 $-1$과 1 사이였다. 두 단위바구니를 더하거나 뺀 바구니를 맞달아 보면 그 이유를 알 수 있었다. 맞단 값은 영바구니일 때 0이고, 그 밖에는 양수였다.

$$
\begin{aligned}
(u-v)\cdot(u-v) &= 2-2(u\cdot v) \ge 0 && \Rightarrow u\cdot v \le 1 \\[6pt]
(u+v)\cdot(u+v) &= 2+2(u\cdot v) \ge 0 && \Rightarrow u\cdot v \ge -1
\end{aligned}
\qquad (\lVert u\rVert=\lVert v\rVert=1)
$$

값이 1에 가까울수록 취향이 닮았고, $-1$에 가까울수록 반대였다.

사람들은 바구니를 단위바구니로 맞추지 않고도 취향을 비교할 수 있는지 알아보았다.
앞서 만난 '사과' 수집가와 '사과 2개' 수집가에게 같은 바구니를 보여 주니, '사과 2개' 수집가가 두 배의 값을 쳐 주었다.

이번에는 저울에 단 값을 두 바구니 크기의 곱으로 나눠 보았다.

$$
\begin{gathered}
\begin{aligned}
u_1 &= [1, 0, 0, 0] && \text{'사과' 수집가의 바구니} \\
u_2 &= [2, 0, 0, 0] && \text{'사과 2개' 수집가의 바구니} \\
v &= [1, 2, 0, 0] && \text{함께 저울에 올릴 바구니}
\end{aligned} \\[8pt]
\begin{aligned}
\lVert u_1 \rVert &= 1 \\
\lVert u_2 \rVert &= 2 \\[6pt]
\lVert v \rVert &= \sqrt{{\color{RoyalBlue}1} \times {\color{DarkOrange}1} + {\color{RoyalBlue}2} \times {\color{DarkOrange}2} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0}} \\
 &= \sqrt{1 + 4 + 0 + 0} \\
 &= \sqrt5
\end{aligned}
\end{gathered}
$$

$$
\begin{array}{l@{\qquad}l}
\text{수집가의 바구니} & \text{저울에 단 값을 두 바구니의 크기로 나누기} \\[8pt]
\text{'사과' 수집가} & \dfrac{u_1 \cdot v}{\lVert u_1 \rVert\,\lVert v \rVert} \\[8pt]
u_1 = [1, 0, 0, 0] & = \dfrac{{\color{RoyalBlue}1} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}2} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0}}{1 \times \sqrt5} \\[8pt]
 & = \dfrac{1 + 0 + 0 + 0}{\sqrt5} \\[8pt]
 & = \dfrac{1}{\sqrt5} \\[14pt]
\text{'사과 2개' 수집가} & \dfrac{u_2 \cdot v}{\lVert u_2 \rVert\,\lVert v \rVert} \\[8pt]
u_2 = [2, 0, 0, 0] & = \dfrac{{\color{RoyalBlue}2} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}2} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0}}{2 \times \sqrt5} \\[8pt]
 & = \dfrac{2 + 0 + 0 + 0}{2\sqrt5} \\[8pt]
 & = \dfrac{2}{2\sqrt5} \\[8pt]
 & = \dfrac{1}{\sqrt5}
\end{array}
$$

'사과 2개' 수집가가 쳐 준 값은 두 배였지만, 그의 바구니 크기도 두 배였다.
두 바구니 크기의 곱으로 나누니, 보여 준 바구니와 닮은 정도는 두 경우 모두 $\tfrac{1}{\sqrt5}$이었다.

## 깊이와 크기

같은 동호회에 들어간 세 수집가가 바구니를 나란히 놓았다. 단위바구니로 맞추면 모두 같았지만, 원래 바구니에 든 개수는 달랐다.

$$
\begin{gathered}
u = \left[\dfrac35, \dfrac45, 0, 0\right] \qquad \text{세 수집가의 같은 단위바구니} \\[12pt]
\begin{array}{l@{\qquad}c@{\qquad}c}
\text{수집가의 바구니} & \text{단위바구니(방향)} & \text{크기(깊이)} \\[8pt]
\text{'사과 }\dfrac35\text{개 바나나 }\dfrac45\text{개' 수집가} & & \\[6pt]
v_1 = \left[\dfrac35, \dfrac45, 0, 0\right] & u & k_1 = 1 \\[12pt]
\text{'사과 3개 바나나 4개' 수집가} & & \\[4pt]
v_2 = [3, 4, 0, 0] & u & k_2 = 5 \\[12pt]
\text{'사과 6개 바나나 8개' 수집가} & & \\[4pt]
v_3 = [6, 8, 0, 0] & u & k_3 = 10
\end{array}
\end{gathered}
$$

세 바구니의 크기 1, 5, 10은 같은 방향으로 취향이 얼마나 깊은지를 나타냈다.

사람들은 원래 바구니를 되찾을 수 있는지 확인하려고, 단위바구니를 각자의 크기만큼 불려 보았다.

$$
\begin{array}{l@{\qquad}l}
\text{단위바구니를 불리기} & \text{원래 바구니로 돌아가는 계산} \\[8pt]
\text{크기 1인 바구니로} & k_1u \\[6pt]
 & = {\color{RoyalBlue}1} \cdot \left[{\color{DarkOrange}\dfrac35, \dfrac45, 0, 0}\right] \\[6pt]
 & = \left[{\color{RoyalBlue}1} \times {\color{DarkOrange}\dfrac35}, {\color{RoyalBlue}1} \times {\color{DarkOrange}\dfrac45}, {\color{RoyalBlue}1} \times {\color{DarkOrange}0}, {\color{RoyalBlue}1} \times {\color{DarkOrange}0}\right] \\[6pt]
 & = \left[\dfrac35, \dfrac45, 0, 0\right] \\[4pt]
 & = v_1 \\[14pt]
\text{크기 5인 바구니로} & k_2u \\[6pt]
 & = {\color{RoyalBlue}5} \cdot \left[{\color{DarkOrange}\dfrac35, \dfrac45, 0, 0}\right] \\[6pt]
 & = \left[{\color{RoyalBlue}5} \times {\color{DarkOrange}\dfrac35}, {\color{RoyalBlue}5} \times {\color{DarkOrange}\dfrac45}, {\color{RoyalBlue}5} \times {\color{DarkOrange}0}, {\color{RoyalBlue}5} \times {\color{DarkOrange}0}\right] \\[6pt]
 & = [3, 4, 0, 0] \\[4pt]
 & = v_2 \\[14pt]
\text{크기 10인 바구니로} & k_3u \\[6pt]
 & = {\color{RoyalBlue}10} \cdot \left[{\color{DarkOrange}\dfrac35, \dfrac45, 0, 0}\right] \\[6pt]
 & = \left[{\color{RoyalBlue}10} \times {\color{DarkOrange}\dfrac35}, {\color{RoyalBlue}10} \times {\color{DarkOrange}\dfrac45}, {\color{RoyalBlue}10} \times {\color{DarkOrange}0}, {\color{RoyalBlue}10} \times {\color{DarkOrange}0}\right] \\[6pt]
 & = [6, 8, 0, 0] \\[4pt]
 & = v_3
\end{array}
$$

세 바구니가 그대로 돌아왔다. 크기로 나눠 맞췄으니, 그 크기를 다시 곱하면 원래 바구니가 되었다.

영바구니가 아닌 $v$는 크기와 단위바구니의 곱으로 나타낼 수 있었다.

$$
v =
\underbrace{{\color{RoyalBlue}\lVert v \rVert}}_{\text{크기(깊이)}}
\cdot
\underbrace{{\color{DarkOrange}\dfrac{v}{\lVert v \rVert}}}_{\text{단위바구니(방향)}}
\qquad (v \ne 0_V)
$$

사람들은 바구니를 크기와 방향으로 나누어, 두 수집가의 닮은 정도가 같았던 이유를 따져 보았다.
저울법의 합산 조항에 따라 한쪽 바구니를 몇 배로 불리면 저울에 단 값도 그만큼 커졌다. 대칭 조항 덕분에 어느 쪽 바구니를 불려도 마찬가지였다.

그래서 두 바구니를 크기와 단위바구니의 곱으로 나타내면, 각 바구니의 크기를 내적 밖으로 꺼내 곱할 수 있었다.

$$
\begin{aligned}
u \cdot v &= \left({\color{RoyalBlue}\lVert u \rVert} \cdot {\color{DarkOrange}\dfrac{u}{\lVert u \rVert}}\right) \cdot \left({\color{RoyalBlue}\lVert v \rVert} \cdot {\color{DarkOrange}\dfrac{v}{\lVert v \rVert}}\right) \qquad (u, v \in V:\text{ 바구니(벡터)},\; u \ne 0_V,\; v \ne 0_V) \\[8pt]
 &= {\color{RoyalBlue}\lVert u \rVert\,\lVert v \rVert} \left({\color{DarkOrange}\dfrac{u}{\lVert u \rVert}} \cdot {\color{DarkOrange}\dfrac{v}{\lVert v \rVert}}\right)
\end{aligned}
$$

저울에 단 값을 두 바구니 크기의 곱으로 나누면 단위바구니끼리 단 값만 남았다.
먼저 단위바구니로 맞춘 뒤 저울에 올려도, 먼저 저울에 올린 뒤 두 바구니 크기의 곱으로 나눠도 결과가 같았던 까닭이었다.

과학자들은 두 단위바구니를 저울에 달아 얻은 닮은 정도를 **코사인 유사도**(cosine similarity)라 불렀다.

$$
\begin{aligned}
\text{닮은 정도} &= \left(\dfrac{u}{\lVert u \rVert}\right) \cdot \left(\dfrac{v}{\lVert v \rVert}\right) \\[8pt]
 &= \dfrac{u \cdot v}{\lVert u \rVert\,\lVert v \rVert}
\end{aligned}
$$
