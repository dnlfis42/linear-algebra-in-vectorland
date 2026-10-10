# 6장. 기준메뉴

## 취향 세트

'사과 3개 바나나 4개' 수집가처럼 맞는 동호회를 찾지 못한 사람들은 새 동호회를 만들고, 대표 바구니 $[\tfrac35, \tfrac45, 0, 0]$을 문밖에 걸었다.
바구니를 팔러 오는 손님이 늘자, 한 상인이 대표 바구니를 세트 $c_1$로 파는 가게를 열기로 했다.

상인은 먼저 가지고 있던 과일에서 $c_1$의 알짜가 세트 몇 개인지 알고 싶었다.

상인은 알짜를 구하던 방법대로, 과일을 $c_1$과 함께 저울에 올려 보았다.

$$
\begin{gathered}
\begin{aligned}
c_1 &= \left[\dfrac35, \dfrac45, 0, 0\right] && \text{대표 바구니로 만든 세트} \\[6pt]
v &= [7, 1, 0, 0] && \text{가지고 있던 과일}
\end{aligned} \\[10pt]
\begin{aligned}
c_1 \cdot v &= {\color{RoyalBlue}\dfrac35} \times {\color{DarkOrange}7} + {\color{RoyalBlue}\dfrac45} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[6pt]
 &= 5 \\[10pt]
5c_1 &= {\color{RoyalBlue}5} \cdot \left[{\color{DarkOrange}\dfrac35, \dfrac45, 0, 0}\right] \\[6pt]
 &= [3, 4, 0, 0] \\[10pt]
v - 5c_1 &= [{\color{RoyalBlue}7, 1, 0, 0}] - [{\color{DarkOrange}3, 4, 0, 0}] \\[6pt]
 &= [4, -3, 0, 0] \\[10pt]
c_1 \cdot (v - 5c_1) &= {\color{RoyalBlue}\dfrac35} \times {\color{DarkOrange}4} + {\color{RoyalBlue}\dfrac45} \times {\color{DarkOrange}(-3)} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[6pt]
 &= 0
\end{aligned}
\end{gathered}
$$

저울에 단 5원을 배율로 삼으니, 알짜는 $c_1$ 다섯 개였다.
남은 과일을 다시 $c_1$과 달아 보니 0원이었다. 남은 과일에는 $c_1$의 알짜가 없었다.

남은 과일도 팔려면 다른 세트가 필요했다.

## 나머지를 세트로

상인은 남은 과일 $[4, -3, 0, 0]$을 그대로 둘째 세트로 삼아 보았다. 저울에 단 값을 그대로 세트 개수로 쓸 수 있는지 알아보려고, 이 세트를 맞달아 보았다.

$$
\begin{aligned}
r &= [4, -3, 0, 0] \qquad \text{남은 과일} \\[8pt]
r \cdot r &= {\color{RoyalBlue}4} \times {\color{DarkOrange}4} + {\color{RoyalBlue}(-3)} \times {\color{DarkOrange}(-3)} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\
 &= 16 + 9 + 0 + 0 \\
 &= 25
\end{aligned}
$$

세트 1개에 25원이 나오니, 저울에 단 값을 그대로 개수로 적을 수 없었다.

그래서 상인은 저울에 단 값이 개수와 같았던 $c_1$을 맞달아 보았다.

$$
\begin{aligned}
c_1 \cdot c_1 &= {\color{RoyalBlue}\dfrac35} \times {\color{DarkOrange}\dfrac35} + {\color{RoyalBlue}\dfrac45} \times {\color{DarkOrange}\dfrac45} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[6pt]
 &= \dfrac{9}{25} + \dfrac{16}{25} + 0 + 0 \\[6pt]
 &= 1
\end{aligned}
$$

단위바구니인 $c_1$을 맞달면 1원이었다.

상인은 남은 과일도 1원이 나오도록 단위바구니로 맞췄다.

$$
\begin{aligned}
\lVert r \rVert &= \sqrt{r \cdot r} \\
 &= \sqrt{25} \\
 &= 5 \\[10pt]
c_2 &= \dfrac{r}{\lVert r \rVert} \\[6pt]
 &= \dfrac{[{\color{RoyalBlue}4, -3, 0, 0}]}{{\color{DarkOrange}5}} \\[6pt]
 &= \left[\dfrac{{\color{RoyalBlue}4}}{{\color{DarkOrange}5}}, \dfrac{{\color{RoyalBlue}-3}}{{\color{DarkOrange}5}}, \dfrac{{\color{RoyalBlue}0}}{{\color{DarkOrange}5}}, \dfrac{{\color{RoyalBlue}0}}{{\color{DarkOrange}5}}\right] \\[6pt]
 &= \left[\dfrac45, -\dfrac35, 0, 0\right]
\end{aligned}
$$

상인은 $c_2$를 맞달아 보고, $c_1$과도 달아 확인해 보았다.

$$
\begin{array}{l@{\qquad}l}
\text{저울에 올린 세트 쌍} & \text{값 계산(원)} \\[8pt]
c_2,\ c_2 & c_2 \cdot c_2 \\[6pt]
 & = {\color{RoyalBlue}\dfrac45} \times {\color{DarkOrange}\dfrac45} + {\color{RoyalBlue}\left(-\dfrac35\right)} \times {\color{DarkOrange}\left(-\dfrac35\right)} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[6pt]
 & = \dfrac{16}{25} + \dfrac9{25} + 0 + 0 \\[6pt]
 & = 1 \\[14pt]
c_1,\ c_2 & c_1 \cdot c_2 \\[6pt]
 & = {\color{RoyalBlue}\dfrac35} \times {\color{DarkOrange}\dfrac45} + {\color{RoyalBlue}\dfrac45} \times {\color{DarkOrange}\left(-\dfrac35\right)} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[6pt]
 & = \dfrac{12}{25} - \dfrac{12}{25} + 0 + 0 \\[6pt]
 & = 0
\end{array}
$$

둘 다 사과와 바나나가 들어 있었지만, 곱한 값끼리 상쇄되어 0원이 되었다!

당근이나 두리안을 담을 때를 위해 당근 세트 $[0, 0, 1, 0]$과 두리안 세트 $[0, 0, 0, 1]$도 마련했다. 두 세트는 맞달면 1원이었고, 당근과 두리안은 그 세트에만 들어 있으니 다른 세트와 달면 0원이었다.

편리한 계산을 위한 선택이었다.

상인은 네 세트를 판매 순서대로 $c_1$, $c_2$, $c_3$, $c_4$로 적어 메뉴를 갖추고, 가게 이름을 동호회과일가게로 지었다.

$$
\begin{gathered}
\text{동호회과일가게의 메뉴와 표준과일가게 명세서} \\[8pt]
\begin{array}{lcccccc}
\text{세트} & & \text{사과} & \text{바나나} & \text{당근} & \text{두리안} & \\[8pt]
c_1 & [ & \tfrac35, & \tfrac45, & 0, & 0 & ] \\[8pt]
c_2 & [ & \tfrac45, & -\tfrac35, & 0, & 0 & ] \\[8pt]
\text{당근 세트 }(c_3) & [ & 0, & 0, & 1, & 0 & ] \\[6pt]
\text{두리안 세트 }(c_4) & [ & 0, & 0, & 0, & 1 & ]
\end{array}
\end{gathered}
$$

상인은 가지고 있던 과일의 명세서에 적을 세트 개수를 알아보려고, 메뉴의 세트와 하나씩 저울에 올려 보았다.

$$
\begin{gathered}
v = [7, 1, 0, 0] \qquad \text{가지고 있던 과일} \\[12pt]
\begin{array}{l@{\qquad}l}
\text{명세서 칸과 함께 올린 세트} & \text{값 계산(원)} \\[8pt]
\text{첫째 칸: }c_1 & c_1 \cdot v = 5 \qquad \text{앞에서 단 값} \\[14pt]
\text{둘째 칸: }c_2 & c_2 \cdot v \\[6pt]
 & = {\color{RoyalBlue}\dfrac45} \times {\color{DarkOrange}7} + {\color{RoyalBlue}\left(-\dfrac35\right)} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[6pt]
 & = \dfrac{28}{5} - \dfrac35 + 0 + 0 \\[6pt]
 & = 5 \\[14pt]
\text{셋째 칸: }c_3 & c_3 \cdot v \\[6pt]
 & = {\color{RoyalBlue}0} \times {\color{DarkOrange}7} + {\color{RoyalBlue}0} \times {\color{DarkOrange}1} + {\color{RoyalBlue}1} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[6pt]
 & = 0 + 0 + 0 + 0 \\
 & = 0 \\[14pt]
\text{넷째 칸: }c_4 & c_4 \cdot v \\[6pt]
 & = {\color{RoyalBlue}0} \times {\color{DarkOrange}7} + {\color{RoyalBlue}0} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}1} \times {\color{DarkOrange}0} \\[6pt]
 & = 0 + 0 + 0 + 0 \\
 & = 0
\end{array}
\end{gathered}
$$

저울에 단 값의 수를 차례로 적으니 명세서가 되었다. $C$는 동호회과일가게를 가리켰다.

$$
[v]_C = [5, 5, 0, 0]
$$

상인은 이 명세서대로 원래 바구니가 나오는지 확인하려고, 각 세트에 명세서에 적힌 개수를 곱해 과일로 풀었다.

$$
\begin{array}{l@{\qquad}l}
\text{세트와 개수} & \text{세트를 불리면} \\[8pt]
k_1 = 5 & k_1c_1 \\[6pt]
 & = {\color{RoyalBlue}5} \cdot \left[{\color{DarkOrange}\dfrac35, \dfrac45, 0, 0}\right] \\[6pt]
 & = \left[{\color{RoyalBlue}5} \times {\color{DarkOrange}\dfrac35}, {\color{RoyalBlue}5} \times {\color{DarkOrange}\dfrac45}, {\color{RoyalBlue}5} \times {\color{DarkOrange}0}, {\color{RoyalBlue}5} \times {\color{DarkOrange}0}\right] \\[6pt]
 & = [3, 4, 0, 0] \\[14pt]
k_2 = 5 & k_2c_2 \\[6pt]
 & = {\color{RoyalBlue}5} \cdot \left[{\color{DarkOrange}\dfrac45, -\dfrac35, 0, 0}\right] \\[6pt]
 & = \left[{\color{RoyalBlue}5} \times {\color{DarkOrange}\dfrac45}, {\color{RoyalBlue}5} \times {\color{DarkOrange}\left(-\dfrac35\right)}, {\color{RoyalBlue}5} \times {\color{DarkOrange}0}, {\color{RoyalBlue}5} \times {\color{DarkOrange}0}\right] \\[6pt]
 & = [4, -3, 0, 0]
\end{array}
$$

$c_1$ 다섯 개는 앞서 뽑아낸 알짜, $c_2$ 다섯 개는 남은 과일이었다. 당근 세트와 두리안 세트는 0개였으니 더해도 바뀌지 않았다.

$$
\begin{aligned}
5c_1 + 5c_2 + 0c_3 + 0c_4
 &= [{\color{RoyalBlue}3, 4, 0, 0}] + [{\color{DarkOrange}4, -3, 0, 0}] \\[6pt]
 &= [{\color{RoyalBlue}3} + {\color{DarkOrange}4}, {\color{RoyalBlue}4} + {\color{DarkOrange}(-3)}, {\color{RoyalBlue}0} + {\color{DarkOrange}0}, {\color{RoyalBlue}0} + {\color{DarkOrange}0}] \\[6pt]
 &= [7, 1, 0, 0] \\
 &= v
\end{aligned}
$$

## 기준메뉴

손님은 대개 표준과일가게에서 산 바구니를 들고 올 터였다. 상인은 표준과일가게 쪽 입구에 안내판을 세우고, 표준 세트마다 이 가게 명세서를 적어 두기로 했다.
표준 세트를 하나씩 가져와 동호회과일가게의 세트와 저울에 올리면 됐다.

$$
\begin{gathered}
e_1 = [1, 0, 0, 0] \qquad \text{동호회과일가게 명세서로 적을 사과 세트} \\[12pt]
\begin{array}{l@{\qquad}l}
\text{명세서 칸과 함께 올린 세트} & \text{값 계산(원)} \\[8pt]
\text{첫째 칸: }c_1 & c_1 \cdot e_1 \\[6pt]
 & = {\color{RoyalBlue}\dfrac35} \times {\color{DarkOrange}1} + {\color{RoyalBlue}\dfrac45} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[6pt]
 & = \dfrac35 + 0 + 0 + 0 \\[6pt]
 & = \dfrac35 \\[14pt]
\text{둘째 칸: }c_2 & c_2 \cdot e_1 \\[6pt]
 & = {\color{RoyalBlue}\dfrac45} \times {\color{DarkOrange}1} + {\color{RoyalBlue}\left(-\dfrac35\right)} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[6pt]
 & = \dfrac45 + 0 + 0 + 0 \\[6pt]
 & = \dfrac45 \\[14pt]
\text{셋째 칸: }c_3 & c_3 \cdot e_1 \\[6pt]
 & = {\color{RoyalBlue}0} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}1} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[6pt]
 & = 0 + 0 + 0 + 0 \\
 & = 0 \\[14pt]
\text{넷째 칸: }c_4 & c_4 \cdot e_1 \\[6pt]
 & = {\color{RoyalBlue}0} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}1} \times {\color{DarkOrange}0} \\[6pt]
 & = 0 + 0 + 0 + 0 \\
 & = 0
\end{array}
\end{gathered}
$$

네 번 단 값의 수를 순서대로 적으니 사과 세트의 명세서가 나왔다.

$$
[e_1]_C = \left[\dfrac35, \dfrac45, 0, 0\right]
$$

다른 표준 세트도 같은 방법으로 적어 안내판에 나란히 붙였다. 각 열에는 표준 세트 하나의 동호회과일가게 명세서가 적혀 있었다.

$$
\begin{gathered}
\text{표준과일가게에서 온 손님을 위한 안내판} \\[8pt]
\begin{array}{lcccc}
 & [e_1]_C & [e_2]_C & [e_3]_C & [e_4]_C \\
 & \text{사과 세트} & \text{바나나 세트} & \text{당근 세트} & \text{두리안 세트} \\[8pt]
\begin{matrix} c_1 \\ c_2 \\ c_3 \\ c_4 \end{matrix} &
\begin{bmatrix} \tfrac35 \\ \tfrac45 \\ 0 \\ 0 \end{bmatrix} &
\begin{bmatrix} \tfrac45 \\ -\tfrac35 \\ 0 \\ 0 \end{bmatrix} &
\begin{bmatrix} 0 \\ 0 \\ 1 \\ 0 \end{bmatrix} &
\begin{bmatrix} 0 \\ 0 \\ 0 \\ 1 \end{bmatrix}
\end{array}
\end{gathered}
$$

과일의 명세서도 안내판도, 세트와 함께 저울에 단 값으로 적을 수 있었다.
세트가 모두 단위바구니이고 서로 무가치하도록 메뉴를 짠 덕분이었다.

과학자들은 이 두 조건을 갖춘 메뉴를 **기준메뉴**(**정규직교기저**, orthonormal basis)라 불렀다. (정규는 세트마다 크기가 1이라는 뜻이고, 직교는 서로 다른 세트끼리 무가치하다는 뜻이다!)

합쳐 팔아도 따로 팔 때와 같은 값을 받았듯이, 바구니를 $c_1$과 달 때도 바구니째 다나 그 안의 세트를 하나씩 따로 달아 더하나 값이 같았다.
따로 달면 $c_1$은 단위바구니라서 하나에 1원, 다른 세트는 $c_1$에게 무가치해서 0원이었다.
그래서 바구니째 단 값은 바구니에 든 $c_1$의 개수와 같았다. 다른 세트와 달아도 마찬가지였다.

바구니를 $v$라고 적으면, 동호회과일가게의 명세서는 이렇게 구했다.

$$
[v]_C = [\,c_1 \cdot v,\ c_2 \cdot v,\ c_3 \cdot v,\ c_4 \cdot v\,]
$$

표준과일가게 메뉴도 기준메뉴였다. 표준 세트는 과일이 하나씩 들어 있어 같은 세트끼리는 1원, 서로 다른 세트끼리는 0원이었다.

바구니를 열어 사과 개수를 세거나, 사과 세트와 함께 저울에 올리거나 같은 숫자가 나왔다. 바나나와 당근, 두리안도 마찬가지였다.

힙스터과일가게 메뉴는 어떨까. 상인은 사과바나나 세트를 같은 세트와, 또 바나나당근 세트와 각각 저울에 올려 보았다.

$$
\begin{gathered}
\begin{aligned}
h_1 &= [1, 1, 0, 0] && \text{사과바나나 세트} \\
h_2 &= [0, 1, 1, 0] && \text{바나나당근 세트}
\end{aligned} \\[12pt]
\begin{array}{l@{\qquad}l}
\text{저울에 올린 세트 쌍} & \text{값 계산(원)} \\[8pt]
h_1,\ h_1 & h_1 \cdot h_1 \\[6pt]
 & = {\color{RoyalBlue}1} \times {\color{DarkOrange}1} + {\color{RoyalBlue}1} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[6pt]
 & = 1 + 1 + 0 + 0 \\
 & = 2 \\[14pt]
h_1,\ h_2 & h_1 \cdot h_2 \\[6pt]
 & = {\color{RoyalBlue}1} \times {\color{DarkOrange}0} + {\color{RoyalBlue}1} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[6pt]
 & = 0 + 1 + 0 + 0 \\
 & = 1
\end{array}
\end{gathered}
$$

사과바나나 세트는 맞달면 2원이니 크기가 $\sqrt2$로, 1이 아니었다. 바나나당근 세트와 저울에 올려도 1원을 받으니 서로 무가치하지도 않았다.

힙스터과일가게도 메뉴법을 지켰으니 어떤 바구니든 팔 수 있었고, 명세서도 하나로 정해졌다. 다만 기준메뉴의 두 조건을 갖추지 않아, 각 세트와 한 번씩 저울에 단 값을 그대로 명세서에 적을 수는 없었다.

힙스터 단골은 세트를 더하고 빼며 개수를 맞춰야 했다.
