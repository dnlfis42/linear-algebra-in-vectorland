# 3장. 힙스터과일가게

세트마다 과일이 하나씩만 든 게 지겨워진 사람들이 있었다.
그런 힙스터들이 모여 힙스터과일가게(좌표계, coordinate system)를 열고 다른 **메뉴**(**기저**, basis)를 내세워 손님을 끌어모았다.

$$
\begin{gathered}
\text{힙스터과일가게의 세트와 표준과일가게 명세서} \\[6pt]
\begin{array}{lccccccc}
\text{세트} & \text{구성품} & & \text{사과} & \text{바나나} & \text{당근} & \text{두리안} & \\[6pt]
\text{사과바나나 세트 }(h_1) & \text{사과 1개, 바나나 1개} & [ & 1, & 1, & 0, & 0 & ] \\
\text{바나나당근 세트 }(h_2) & \text{바나나 1개, 당근 1개} & [ & 0, & 1, & 1, & 0 & ] \\
\text{당근두리안 세트 }(h_3) & \text{당근 1개, 두리안 1개} & [ & 0, & 0, & 1, & 1 & ] \\
\text{두리안 세트 }(h_4) & \text{두리안 1개} & [ & 0, & 0, & 0, & 1 & ]
\end{array}
\end{gathered}
$$

## 같은 바구니, 다른 명세서

어느 날 한 손님이 힙스터과일가게 명세서를 들고 표준과일가게에 왔다. 표준과일가게 직원은 고개를 갸웃거렸다.
분명 명세서에는 $[1, 0, 1, 0]$이라고 적혀 있었지만 바구니를 열어 보니 사과, 바나나, 당근, 두리안이 한 개씩 들어 있었다.
표준과일가게 명세서라면 $[1, 1, 1, 1]$이라고 적혀 있어야 했다!

같은 바구니를 두 가게의 명세서로 나란히 적으면 이랬다.

$$
\begin{gathered}
\text{같은 바구니 }v:\text{ 사과 1개, 바나나 1개, 당근 1개, 두리안 1개} \\[12pt]
\begin{array}{l@{\qquad}l@{\qquad}l}
 & \text{힙스터과일가게 }H & \text{표준과일가게 }E \\[8pt]
\text{첫째 칸} & \text{사과바나나 세트 1개} & \text{사과 세트 1개} \\[4pt]
\text{둘째 칸} & \text{바나나당근 세트 0개} & \text{바나나 세트 1개} \\[4pt]
\text{셋째 칸} & \text{당근두리안 세트 1개} & \text{당근 세트 1개} \\[4pt]
\text{넷째 칸} & \text{두리안 세트 0개} & \text{두리안 세트 1개} \\[8pt]
\text{숫자만 적으면} & [1, 0, 1, 0] & [1, 1, 1, 1] \\[8pt]
\text{바구니를 세트로 풀면} & v = 1h_1 + 0h_2 + 1h_3 + 0h_4 & v = 1e_1 + 1e_2 + 1e_3 + 1e_4
\end{array}
\end{gathered}
$$

두 명세서에 적힌 세트들을 각각 과일로 풀어 더했다.

$$
\begin{aligned}
\text{힙스터과일가게:}\quad
v &= 1h_1 + 0h_2 + 1h_3 + 0h_4 \\
  &= (\text{사과 1개} + \text{바나나 1개}) + (\text{당근 1개} + \text{두리안 1개}) \\
  &= \text{사과 1개} + \text{바나나 1개} + \text{당근 1개} + \text{두리안 1개} \\[12pt]
\text{표준과일가게:}\quad
v &= 1e_1 + 1e_2 + 1e_3 + 1e_4 \\
  &= \text{사과 1개} + \text{바나나 1개} + \text{당근 1개} + \text{두리안 1개}
\end{aligned}
$$

그제야 사람들은 명세서 숫자만 보고는 바구니에 어떤 과일이 들었는지 알 수 없다는 것을 깨달았다.
숫자를 읽으려면 그 명세서가 어느 가게의 메뉴(기저, basis)로 적은 것인지 알아야 했다!

그 뒤로 사람들은 명세서를 적어 준 가게의 이름도 붙이기로 했다.

$$
\begin{aligned}
[v]_E &= [1, 1, 1, 1] \\
[v]_H &= [1, 0, 1, 0]
\end{aligned}
$$

바구니(벡터, vector)는 그대로지만 명세서(좌표, coordinates)는 어느 가게의 세트로 적느냐에 따라 달라졌다!

## 안내판 배치

그 뒤로도 힙스터과일가게에서 산 바구니를 들고 오는 손님이 끊이지 않았다. 직원은 손님이 올 때마다 바구니를 열고 과일을 하나하나 꺼내 세야 했다.

그래서 표준과일가게는 힙스터과일가게 쪽에서 들어오는 입구에 안내판을 세웠다.
안내판 맨 위에는 "힙스터과일가게에서 오신 손님께: 손님의 세트는 저희 명세서로 이렇습니다"라고 적혀 있었다.

$$
\begin{array}{ccccc}
& [h_1]_E & [h_2]_E & [h_3]_E & [h_4]_E \\
& \text{사과바나나 세트} & \text{바나나당근 세트} & \text{당근두리안 세트} & \text{두리안 세트} \\[6pt]
\begin{matrix} \text{사과 세트 }(e_1) \\ \text{바나나 세트 }(e_2) \\ \text{당근 세트 }(e_3) \\ \text{두리안 세트 }(e_4) \end{matrix} &
\begin{bmatrix} 1 \\ 1 \\ 0 \\ 0 \end{bmatrix} &
\begin{bmatrix} 0 \\ 1 \\ 1 \\ 0 \end{bmatrix} &
\begin{bmatrix} 0 \\ 0 \\ 1 \\ 1 \end{bmatrix} &
\begin{bmatrix} 0 \\ 0 \\ 0 \\ 1 \end{bmatrix}
\end{array}
$$

이제 직원은 바구니를 열지 않았다. 안내판에 적힌 각 명세서에 손님이 산 힙스터 세트 개수를 곱해 더하면 됐다.
앞서 온 손님의 힙스터 명세서로 표준 명세서를 구해 보았다.

$$
\begin{aligned}
[v]_H &= [1, 0, 1, 0] && \text{힙스터과일가게 명세서} \\[6pt]
[v]_E &= 1[h_1]_E + 0[h_2]_E + 1[h_3]_E + 0[h_4]_E && \text{표준과일가게 명세서} \\
      &= 1[1, 1, 0, 0] + 0[0, 1, 1, 0] + 1[0, 0, 1, 1] + 0[0, 0, 0, 1] \\
      &= [1, 1, 0, 0] + [0, 0, 0, 0] + [0, 0, 1, 1] + [0, 0, 0, 0] \\
      &= [1, 1, 1, 1]
\end{aligned}
$$

바구니를 열어 센 것과 같은 명세서였다.

## 사과 세트를 사려면

물론 반대쪽으로 가는 손님도 있었다.
힙스터과일가게 단골이 표준과일가게에 들렀다가 사과 세트를 마음에 들어 했다.
사과 세트를 사자 직원이 표준과일가게 명세서에 $[1, 0, 0, 0]$을 적어 주었다.

$$
\begin{aligned}
e_1 &: \text{사과 1개가 든 바구니} \\
[e_1]_E &= [1, 0, 0, 0] \qquad \text{표준과일가게 명세서}
\end{aligned}
$$

단골은 같은 바구니를 늘 가던 힙스터과일가게에서도 사고 싶어졌다.
그런데 그 가게에는 사과 1개만 든 세트도, 표준 세트를 힙스터 명세서로 적은 안내판도 없었다!

단골은 직접 힙스터 세트를 더하고 빼서 표준과일가게 사과 세트를 만들어 보았다.

$$
\begin{array}{l@{\qquad}l}
\text{세트를 더하고 빼면} & \text{남은 과일(표준과일가게 명세서)} \\[8pt]
h_1 & [1, 1, 0, 0] \\[6pt]
h_1 - h_2 & [{\color{RoyalBlue}1, 1, 0, 0}] - [{\color{DarkOrange}0, 1, 1, 0}] \\
 & = [{\color{RoyalBlue}1} - {\color{DarkOrange}0}, {\color{RoyalBlue}1} - {\color{DarkOrange}1}, {\color{RoyalBlue}0} - {\color{DarkOrange}1}, {\color{RoyalBlue}0} - {\color{DarkOrange}0}] \\
 & = [1, 0, -1, 0] \\[6pt]
(h_1 - h_2) + h_3 & [{\color{RoyalBlue}1, 0, -1, 0}] + [{\color{DarkOrange}0, 0, 1, 1}] \\
 & = [{\color{RoyalBlue}1} + {\color{DarkOrange}0}, {\color{RoyalBlue}0} + {\color{DarkOrange}0}, {\color{RoyalBlue}-1} + {\color{DarkOrange}1}, {\color{RoyalBlue}0} + {\color{DarkOrange}1}] \\
 & = [1, 0, 0, 1] \\[6pt]
\big((h_1 - h_2) + h_3\big) - h_4 & [{\color{RoyalBlue}1, 0, 0, 1}] - [{\color{DarkOrange}0, 0, 0, 1}] \\
 & = [{\color{RoyalBlue}1} - {\color{DarkOrange}0}, {\color{RoyalBlue}0} - {\color{DarkOrange}0}, {\color{RoyalBlue}0} - {\color{DarkOrange}0}, {\color{RoyalBlue}1} - {\color{DarkOrange}1}] \\
 & = [1, 0, 0, 0]
\end{array}
$$

바나나와 당근, 두리안을 차례로 없애고 나니 사과 1개만 남았다.

$$
\begin{aligned}
e_1 &= h_1 - h_2 + h_3 - h_4 \\
    &= 1h_1 + (-1)h_2 + 1h_3 + (-1)h_4 \\[6pt]
[e_1]_H &= [1, -1, 1, -1] \qquad \text{힙스터과일가게 명세서}
\end{aligned}
$$

표준과일가게에서는 사과 세트 하나면 되던 바구니를, 힙스터과일가게에서는 네 종류의 세트를 더하고 빼서 만들었다.

단골은 나머지 표준세트의 힙스터 명세서도 구했다. 자신처럼 찾아올 손님들을 위해 안내판을 만들어 힙스터과일가게 입구에 세워 두었다.

$$
\begin{array}{ccccc}
& [e_1]_H & [e_2]_H & [e_3]_H & [e_4]_H \\
& \text{사과 세트} & \text{바나나 세트} & \text{당근 세트} & \text{두리안 세트} \\[6pt]
\begin{matrix} \text{사과바나나 세트 }(h_1) \\ \text{바나나당근 세트 }(h_2) \\ \text{당근두리안 세트 }(h_3) \\ \text{두리안 세트 }(h_4) \end{matrix} &
\begin{bmatrix} 1 \\ -1 \\ 1 \\ -1 \end{bmatrix} &
\begin{bmatrix} 0 \\ 1 \\ -1 \\ 1 \end{bmatrix} &
\begin{bmatrix} 0 \\ 0 \\ 1 \\ -1 \end{bmatrix} &
\begin{bmatrix} 0 \\ 0 \\ 0 \\ 1 \end{bmatrix}
\end{array}
$$

## 가게를 열 자격

힙스터과일가게가 잘되자 너도나도 가게를 열었다. 그런데 몇몇 가게에서는 손님과 다툼이 끊이지 않았다.

사과바나나 세트만 파는 가게에서는 당근을 살 방법이 없었다. 세트에 배율을 곱해 더하는 **일차결합**(linear combination)으로도 사과와 바나나가 늘 같은 수만큼 나올 뿐이었다.

$$
\begin{aligned}
k &\in \mathbb{R}, \quad h_1 = [1, 1, 0, 0] \\[6pt]
kh_1 &= {\color{RoyalBlue}k}[{\color{DarkOrange}1, 1, 0, 0}] \\
     &= [{\color{RoyalBlue}k}\times{\color{DarkOrange}1},\; {\color{RoyalBlue}k}\times{\color{DarkOrange}1},\; {\color{RoyalBlue}k}\times{\color{DarkOrange}0},\; {\color{RoyalBlue}k}\times{\color{DarkOrange}0}] \\
     &= [k, k, 0, 0] \\[6pt]
[k, k, 0, 0] &\ne [0, 0, 1, 0] \qquad \text{어떤 배율로도 당근 1개를 만들 수 없다}
\end{aligned}
$$

반대로 세트를 너무 많이 파는 가게도 있었다. 그 가게는 사과 세트, 바나나 세트, 사과바나나 세트, 당근 세트, 두리안 세트를 팔았다.

$$
\begin{array}{ll}
\text{세트} & \text{구성품} \\[6pt]
g_1 & \text{사과 1개} \\
g_2 & \text{바나나 1개} \\
g_3 & \text{사과 1개, 바나나 1개} \\
g_4 & \text{당근 1개} \\
g_5 & \text{두리안 1개}
\end{array}
$$

이 가게에서는 같은 바구니를 서로 다른 명세서로 적을 수 있었다. 사과 1개와 바나나 1개를 산 손님에게 두 직원이 서로 다른 명세서를 내밀었다.

$$
\begin{array}{l@{\qquad}l}
\text{첫째 직원: 사과 세트와 바나나 세트} & \text{둘째 직원: 사과바나나 세트} \\[6pt]
v = 1g_1 + 1g_2 + 0g_3 + 0g_4 + 0g_5 & v = 0g_1 + 0g_2 + 1g_3 + 0g_4 + 0g_5 \\[6pt]
[1, 1, 0, 0, 0] & [0, 0, 1, 0, 0] \\[6pt]
\text{사과 1개} + \text{바나나 1개} & \text{사과 1개} + \text{바나나 1개}
\end{array}
$$

손님은 어느 명세서가 맞느냐고 따졌다. 두 명세서 모두 같은 바구니를 나타냈으니 틀린 명세서는 아니었다. 사과바나나 세트가 다른 두 세트를 합친 것과 같아서 생긴 일이었다.

$$
g_3 = g_1 + g_2
$$

그래서 과일나라는 가게를 열려면 메뉴가 두 가지를 지켜야 한다는 법을 만들었다.

> [!important] 메뉴법
>
> - **생성**(span): 세트를 조합해서 과일나라의 어떤 바구니든 만들 수 있다.
> - **일차독립**(linear independence): 다른 세트를 조합해 만들 수 있는 세트는 메뉴에 올리지 않는다.

이 두 조건을 지키니 어떤 바구니든 팔 수 있었고, 그 바구니의 명세서도 하나로 정해졌다. 과학자들은 이 법을 지킨 메뉴를 **기저**(basis)라 불렀다.

법이 시행되고 나서 과학자들은 신기한 사실을 발견했다. 메뉴법을 지킨 가게는 메뉴가 저마다 달라도 세트 가짓수가 모두 넷이었다.
세트를 셋만 파는 가게에서는 만들 수 없는 바구니가 생겼고, 다섯을 파는 가게에는 다른 세트를 조합해 만들 수 있는 세트가 적어도 하나 끼어 있었다.

처음에 센 과일 가짓수 넷이 메뉴법을 지킨 모든 가게의 세트 가짓수였던 것이다!

과학자들은 이 수를 **차원**(dimension)이라 불렀다.
