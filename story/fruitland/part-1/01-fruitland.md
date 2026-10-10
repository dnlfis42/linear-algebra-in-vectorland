# 1장. 과일나라

## 네 가지 과일

태초에 과일나라에는 네 가지 과일이 있었다.
사과(apple), 바나나(banana), 당근(carrot), 두리안(durian)이었다.

과일나라 국민에게는 저마다 **과일 바구니**(**벡터**, vector)가 있었다.
바구니에는 사과, 바나나, 당근, 두리안을 담을 수 있었다.

## 좌표계와 표준기저

사람들은 서로의 바구니를 비교하고 싶었다. 그런데 문제가 생겨 버렸다.
사과 하나 든 바구니도 $[1]$, 당근 하나 든 바구니도 $[1]$로 적으니 둘을 구별할 길이 없었다.

그래서 과일나라는 법을 만들기로 했다.

먼저 **표준과일가게**(**좌표계**, coordinate system)를 열었다.
과일 하나씩 든 세트를 사과 세트, 바나나 세트, 당근 세트, 두리안 세트라 불렀다. 가게는 네 세트를 이 순서대로 메뉴에 적어 팔았다.
이 네 세트를 **표준세트**(**표준기저 벡터**, standard basis vector)라 부르고, 표준세트를 판매 순서대로 늘어놓은 목록을 **표준메뉴**(**표준기저**, standard basis)라고 불렀다.

그리고 바구니에 든 세트를 종이에 적어 주기로 했다.
이 종이를 **명세서**(**좌표**, coordinates)라 부르고, 명세서를 적는 법을 공표했다.

> [!important] 명세서법
> 명세서에는 세트가 몇 개씩 들었는지 판매 순서대로 적는다.

$$
\begin{gathered}
\text{표준과일가게의 세트와 명세서} \\[6pt]
\begin{array}{lccccccc}
\text{세트} & \text{구성품} & & \text{사과} & \text{바나나} & \text{당근} & \text{두리안} & \\[6pt]
\text{사과 세트 }(e_1) & \text{사과 1개} & [ & 1, & 0, & 0, & 0 & ] \\
\text{바나나 세트 }(e_2) & \text{바나나 1개} & [ & 0, & 1, & 0, & 0 & ] \\
\text{당근 세트 }(e_3) & \text{당근 1개} & [ & 0, & 0, & 1, & 0 & ] \\
\text{두리안 세트 }(e_4) & \text{두리안 1개} & [ & 0, & 0, & 0, & 1 & ]
\end{array}
\end{gathered}
$$

명세서의 칸마다 그 **세트의 개수**(**성분**, component)를 적었다.
이때부터 과일나라 국민은 자기 바구니를 $[a, b, c, d]$처럼 적었다. 사과 하나 든 바구니와 당근 하나 든 바구니도 구별할 수 있었다.

$$
\begin{array}{rclccccccc}
 & & & & & \text{사과} & \text{바나나} & \text{당근} & \text{두리안} & \\[4pt]
\text{사과 1개} & = & e_1 & \Rightarrow & [ & 1, & 0, & 0, & 0 & ] \\
\text{당근 1개} & = & e_3 & \Rightarrow & [ & 0, & 0, & 1, & 0 & ] \\
\text{사과 2개, 당근 1개} & = & e_1 + e_1 + e_3 & \Rightarrow & [ & 2, & 0, & 1, & 0 & ]
\end{array}
$$

## 덧셈

그 뒤로 사람들은 바구니로 여러 일을 했다. 두 바구니를 합치기도 하고, 바구니에서 과일을 빼기도 했다.

$$
\begin{aligned}
u &= [{\color{RoyalBlue}1, 2, 0, 0}], \quad v = [{\color{DarkOrange}0, 1, 3, 0}] \qquad (u, v:\text{ 바구니(벡터)}) \\[6pt]
u + v &= [{\color{RoyalBlue}1, 2, 0, 0}] + [{\color{DarkOrange}0, 1, 3, 0}] \\
      &= [{\color{RoyalBlue}1} + {\color{DarkOrange}0}, {\color{RoyalBlue}2} + {\color{DarkOrange}1}, {\color{RoyalBlue}0} + {\color{DarkOrange}3}, {\color{RoyalBlue}0} + {\color{DarkOrange}0}] \\
      &= [1, 3, 3, 0] \\[12pt]
u - v &= [{\color{RoyalBlue}1, 2, 0, 0}] - [{\color{DarkOrange}0, 1, 3, 0}] \\
      &= [{\color{RoyalBlue}1} - {\color{DarkOrange}0}, {\color{RoyalBlue}2} - {\color{DarkOrange}1}, {\color{RoyalBlue}0} - {\color{DarkOrange}3}, {\color{RoyalBlue}0} - {\color{DarkOrange}0}] \\
      &= [1, 1, -3, 0]
\end{aligned}
$$

과일나라에서는 음수 개수가 든 바구니도 바구니로 다뤘다. 개수가 서로 반대인 두 바구니를 합치면 빈 바구니가 되었다.

그러다 과일나라 과학자들이 어느 바구니로 해 봐도 똑같이 나타나는 현상을 찾아냈다.
그래서 이를 묶고 '덧셈의 법칙'이란 이름을 붙였다.

> [!info] 덧셈의 법칙
>
> - 교환법칙: 어느 바구니를 먼저 쏟든 결과가 같다.
> - 결합법칙: 세 바구니를 어떻게 묶어 쏟든 결과가 같다.
> - 항등원의 존재: 쏟아도 아무것도 바뀌지 않는 바구니가 있다.
> - 역원의 존재: 어떤 바구니든 합치면 빈 바구니가 되는 짝이 있다.

과학자들은 아무것도 바꾸지 않는 그 바구니를 **영바구니**(**영벡터**, zero vector)라 부르고, 합치면 빈 바구니가 되는 짝을 **역바구니**(**역원**, additive inverse)라 불렀다.

## 스칼라 곱셈

잔치가 다가오자 사람들은 바구니를 통째로 몇 배씩 불리고 싶어졌다.
사과 1개와 바나나 2개가 든 바구니를 세 배로 불리면 사과 3개와 바나나 6개가 든 바구니 하나가 되었다. (바구니가 3개로 늘어난 게 아니다!)

$$
\begin{aligned}
k &= {\color{RoyalBlue}3}, \quad v = [{\color{DarkOrange}1, 2, 0, 0}] \qquad (k:\text{ 배율(스칼라)},\; v:\text{ 바구니(벡터)}) \\[6pt]
kv &= {\color{RoyalBlue}3} \cdot [{\color{DarkOrange}1, 2, 0, 0}] \\
   &= [{\color{RoyalBlue}3} \times {\color{DarkOrange}1}, {\color{RoyalBlue}3} \times {\color{DarkOrange}2}, {\color{RoyalBlue}3} \times {\color{DarkOrange}0}, {\color{RoyalBlue}3} \times {\color{DarkOrange}0}] \\
   &= [3, 6, 0, 0]
\end{aligned}
$$

사람들은 바구니를 반으로 줄이기도 하고(0.5배), 아예 비우기도 하고(0배), 뒤집기도 했다(−1배).
바구니를 뒤집으면 양수 개수는 음수가 되고 음수 개수는 양수가 되었다. 사과 1개를 뒤집으면 사과 $-1$개, 즉 역바구니였다.

사과 $-1$개는 사과 1개와 방향이 반대인 바구니였다.

이번에도 바구니를 불릴 때 어느 바구니에서나 똑같이 나타나는 현상이 있었다.

> [!info] 배율의 법칙
>
> - 분배법칙: 두 바구니를 합친 뒤 $k$배로 불리나, 각각 $k$배로 불린 뒤 합치나 결과가 같다.
> - 분배법칙: $k$배로 불린 바구니와 $l$배로 불린 바구니를 합치나, 처음부터 $(k + l)$배로 불리나 결과가 같다.
> - 배율의 결합법칙: $l$배로 불린 뒤 다시 $k$배로 불리나, 처음부터 $kl$배로 불리나 결과가 같다.
> - 배율의 항등원: 1배로 불리면 아무것도 바뀌지 않는다.

과학자들은 바구니를 몇 배로 불릴지 정하는 수를 **배율**(**스칼라**, scalar)이라 불렀다.

## 과일나라 법칙

표준과일가게는 바구니를 매번 쏟아 보지 않고 명세서의 숫자만 계산했다. 명세서법대로 세트 개수를 적었기 때문이다.

두 바구니를 합치면 세트 개수도 더해지고, 바구니를 불리면 세트 개수도 그만큼 불어났다. 그래서 명세서끼리 더하거나 배율을 곱하면, 바구니를 합치거나 불린 뒤 받은 명세서와 같았다.
바구니를 더하는 순서나 묶는 방법을 바꿔도 결과는 같았다. 합친 뒤 불리거나, 각각 불린 뒤 합쳐도 같았다.

$$
\begin{gathered}
\begin{aligned}
& \underbrace{u, v, w}_{\text{바구니(벡터)}}, \quad \underbrace{0_V}_{\text{영바구니(영벡터)}} \in V && (V:\text{ 바구니가 모인 과일나라(벡터공간)}) \\[12pt]
& \underbrace{k, l}_{\text{배율(스칼라)}}, \quad \underbrace{0, 1}_{\text{배율 0과 1}} \in \mathbb{R} && (\mathbb{R}:\text{ 배율로 쓰는 수의 집합(실수 집합)})
\end{aligned} \\[16pt]
\begin{array}{clll}
\text{번호} & \text{이름} & \text{내용} & \text{수식} \\[6pt]
1 & \text{교환법칙} & \text{어느 바구니를 먼저 쏟든 결과가 같다} & u + v = v + u \\[6pt]
2 & \text{결합법칙} & \text{세 바구니를 어떻게 묶어 쏟든 결과가 같다} & (u + v) + w = u + (v + w) \\[6pt]
3 & \text{항등원의 존재} & \text{쏟아도 아무것도 바뀌지 않는 바구니가 있다} & v + 0_V = v \\[6pt]
4 & \text{역원의 존재} & \text{어떤 바구니든 합치면 빈 바구니가 되는 짝이 있다} & v + (-v) = 0_V \\[6pt]
5 & \text{분배법칙} & \text{합친 바구니를 }k\text{배 하나, 각각 }k\text{배 해서 합치나 같다} & k(u + v) = ku + kv \\[6pt]
6 & \text{분배법칙} & \text{배율을 더해 불리나, 따로 불려 합치나 같다} & (k + l)v = kv + lv \\[6pt]
7 & \text{배율의 결합법칙} & \text{두 번 불리나, 배율을 곱해 한 번에 불리나 같다} & k(lv) = (kl)v \\[6pt]
8 & \text{배율의 항등원} & \text{1배로 불리면 그대로다} & 1v = v
\end{array}
\end{gathered}
$$

더하거나 배율을 곱한 결과도 같은 세계에 속하고, 이 법칙들이 통하면 무엇이든 과일나라의 바구니처럼 다룰 수 있었다.
과일이 아니어도 괜찮았다. 화살표도, 돈도, 소리도, 함수도 이 법칙이 통하면 바구니였다. 과학자들은 이런 세계를 **벡터공간**(vector space)이라 불렀다.
