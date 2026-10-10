# 7장. 환산표

## 환산표

표준과일가게는 힙스터과일가게 쪽 입구에 이미 안내판을 세워 두었다. 덕분에 바구니를 열 일은 없어졌지만, 직원은 손님이 올 때마다 안내판에서 힙스터 세트의 명세서를 찾아, 손님의 세트 개수를 곱해 더해야 했다.

직원은 안내판에 적힌 네 명세서를 한 표로 묶어 보기로 했다.

$$
\begin{gathered}
\text{힙스터 세트 하나씩을 표준과일가게 명세서로} \\[8pt]
\begin{array}{lcccc}
 & [h_1]_E & [h_2]_E & [h_3]_E & [h_4]_E \\
 & \text{사과바나나} & \text{바나나당근} & \text{당근두리안} & \text{두리안} \\[8pt]
\begin{matrix} \text{사과} \\ \text{바나나} \\ \text{당근} \\ \text{두리안} \end{matrix} &
\begin{bmatrix} 1 \\ 1 \\ 0 \\ 0 \end{bmatrix} &
\begin{bmatrix} 0 \\ 1 \\ 1 \\ 0 \end{bmatrix} &
\begin{bmatrix} 0 \\ 0 \\ 1 \\ 1 \end{bmatrix} &
\begin{bmatrix} 0 \\ 0 \\ 0 \\ 1 \end{bmatrix}
\end{array}
\end{gathered}
$$

세로 한 줄을 열이라 했다. 각 열에는 힙스터 세트 하나의 표준과일가게 명세서가 적혀 있었다.

세트의 판매 순서대로 열을 붙이고, 괄호를 하나로 묶어 $W$라고 적었다.

$$
W = \begin{pmatrix}
1 & 0 & 0 & 0 \\
1 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 \\
0 & 0 & 1 & 1
\end{pmatrix}
$$

표준과일가게는 입구의 안내판을 "힙스터과일가게에서 온 손님을 위한 환산표"로 고쳐 달았다.

과학자들은 이처럼 같은 바구니의 명세서를 다른 가게의 명세서로 바꾸는 표를 **환산표**(**기저변환행렬**, change-of-basis matrix)라 불렀다.

직원은 처음 찾아왔던 손님의 바구니 $v$로 해 보았다. 사과바나나 세트 하나와 당근두리안 세트 하나를 산 바구니였다.

표에 넣을 때는 명세서의 네 수를 판매 순서대로 위에서 아래로 적었다.

$$
[v]_H = \begin{pmatrix} 1 \\ 0 \\ 1 \\ 0 \end{pmatrix}
\qquad \text{힙스터과일가게 명세서}
$$

직원은 먼저 $W$를 가로로 읽었다. 첫째 행 $[1, 0, 0, 0]$은 힙스터 세트마다 사과가 몇 개 들었는지 적은 줄이었다. (사과바나나 세트에는 사과가 1개, 다른 세트에는 0개)

세트마다 들어 있는 사과 개수에 명세서의 세트 개수를 곱해 더하면, 표준 명세서 첫째 칸에 적을 사과 개수가 나왔다.

직원은 바나나와 당근, 두리안도 각 행으로 같은 계산을 했다.

$$
\begin{array}{l@{\qquad}l}
\text{행과 세트마다 쳐 주는 값} & \text{명세서와 짝지어 계산(원)} \\[8pt]
\text{첫째 행: '사과' 수집가} & \text{표준 명세서 첫째 칸} \\[4pt]
[1, 0, 0, 0] & = {\color{RoyalBlue}1} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\
 & = 1 + 0 + 0 + 0 \\
 & = 1 \\[14pt]
\text{둘째 행: '바나나' 수집가} & \text{표준 명세서 둘째 칸} \\[4pt]
[1, 1, 0, 0] & = {\color{RoyalBlue}1} \times {\color{DarkOrange}1} + {\color{RoyalBlue}1} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\
 & = 1 + 0 + 0 + 0 \\
 & = 1 \\[14pt]
\text{셋째 행: '당근' 수집가} & \text{표준 명세서 셋째 칸} \\[4pt]
[0, 1, 1, 0] & = {\color{RoyalBlue}0} \times {\color{DarkOrange}1} + {\color{RoyalBlue}1} \times {\color{DarkOrange}0} + {\color{RoyalBlue}1} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\
 & = 0 + 0 + 1 + 0 \\
 & = 1 \\[14pt]
\text{넷째 행: '두리안' 수집가} & \text{표준 명세서 넷째 칸} \\[4pt]
[0, 0, 1, 1] & = {\color{RoyalBlue}0} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}1} \times {\color{DarkOrange}1} + {\color{RoyalBlue}1} \times {\color{DarkOrange}0} \\
 & = 0 + 0 + 1 + 0 \\
 & = 1
\end{array}
$$

수집가 넷에게 받은 값의 수를 차례로 적으니 표준과일가게 명세서가 되었다.
표준메뉴가 기준메뉴라서, 각 과일 세트를 바구니로 가진 수집가가 쳐 준 값이 그 세트의 개수와 같았다.

이렇게 각 행을 명세서와 짝지어 곱해 더해 얻은 명세서를 과학자들은 **행렬과 벡터의 곱**(matrix-vector product)이라 부르고 $W[v]_H$로 적었다.

$$
\begin{aligned}
[v]_E &= W\,[v]_H \\[6pt]
 &= {\color{RoyalBlue}\begin{pmatrix}
1 & 0 & 0 & 0 \\
1 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 \\
0 & 0 & 1 & 1
\end{pmatrix}}
{\color{DarkOrange}\begin{pmatrix} 1 \\ 0 \\ 1 \\ 0 \end{pmatrix}} \\[8pt]
 &= \begin{pmatrix} 1 \\ 1 \\ 1 \\ 1 \end{pmatrix}
\end{aligned}
$$

같은 명세서를 열로도 구할 수 있는지 확인하려고, 이번에는 열마다 명세서의 세트 개수를 곱한 뒤 더해 보았다.

첫째 열에는 사과바나나 세트의 표준 명세서가 적혀 있었다. 손님은 이 세트를 1개 샀으니, 첫째 열에 명세서 첫째 칸의 1을 곱했다. 둘째 열에는 바나나당근 세트의 표준 명세서가 적혀 있었다. 이 세트는 0개였으니, 둘째 열에는 둘째 칸의 0을 곱했다.
같은 방법으로 셋째 열에는 1을, 넷째 열에는 0을 곱하고, 네 결과를 더했다.

$$
\begin{aligned}
W\,[v]_H &= 1[h_1]_E + 0[h_2]_E + 1[h_3]_E + 0[h_4]_E \\[8pt]
 &= {\color{RoyalBlue}1}{\color{DarkOrange}\begin{pmatrix} 1 \\ 1 \\ 0 \\ 0 \end{pmatrix}}
 + {\color{RoyalBlue}0}{\color{DarkOrange}\begin{pmatrix} 0 \\ 1 \\ 1 \\ 0 \end{pmatrix}}
 + {\color{RoyalBlue}1}{\color{DarkOrange}\begin{pmatrix} 0 \\ 0 \\ 1 \\ 1 \end{pmatrix}}
 + {\color{RoyalBlue}0}{\color{DarkOrange}\begin{pmatrix} 0 \\ 0 \\ 0 \\ 1 \end{pmatrix}} \\[8pt]
 &= \begin{pmatrix} 1 \\ 1 \\ 0 \\ 0 \end{pmatrix}
 + \begin{pmatrix} 0 \\ 0 \\ 0 \\ 0 \end{pmatrix}
 + \begin{pmatrix} 0 \\ 0 \\ 1 \\ 1 \end{pmatrix}
 + \begin{pmatrix} 0 \\ 0 \\ 0 \\ 0 \end{pmatrix} \\[8pt]
 &= \begin{pmatrix}
1 + 0 + 0 + 0 \\
1 + 0 + 0 + 0 \\
0 + 0 + 1 + 0 \\
0 + 0 + 1 + 0
\end{pmatrix} \\[8pt]
 &= \begin{pmatrix} 1 \\ 1 \\ 1 \\ 1 \end{pmatrix}
\end{aligned}
$$

행마다 계산하면 표준 명세서의 각 칸이 나왔고, 열마다 세트 개수를 곱해 더하면 표준 명세서 전체가 나왔다.

직원은 힙스터 세트의 표준 명세서에 세트 개수를 곱해 더했다. 표준 명세서를 구하려면 각 열에도 표준 명세서가 적혀 있어야 했다.

직원은 명세서를 같은 가게의 명세서로 바꾸는 표는 어떤 모습인지 알아보려고, 이번에는 각 열에 힙스터 명세서를 적어 보았다. 힙스터 세트를 힙스터 명세서로 적으면, 그 세트의 칸만 1이고 나머지는 모두 0이었다. 네 열을 붙이니 이런 표가 되었다.

$$
I = \begin{pmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1
\end{pmatrix}
$$

새 표에 손님의 힙스터 명세서 $[1,0,1,0]$을 넣어 보았다.

$$
\begin{aligned}
I\,[v]_H &= {\color{RoyalBlue}\begin{pmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1
\end{pmatrix}}
{\color{DarkOrange}\begin{pmatrix} 1 \\ 0 \\ 1 \\ 0 \end{pmatrix}} \\[8pt]
 &= \begin{pmatrix}
{\color{RoyalBlue}1} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[4pt]
{\color{RoyalBlue}0} \times {\color{DarkOrange}1} + {\color{RoyalBlue}1} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[4pt]
{\color{RoyalBlue}0} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}1} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[4pt]
{\color{RoyalBlue}0} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}1} + {\color{RoyalBlue}1} \times {\color{DarkOrange}0}
\end{pmatrix} \\[8pt]
 &= \begin{pmatrix} 1 \\ 0 \\ 1 \\ 0 \end{pmatrix} \\
 &= [v]_H
\end{aligned}
$$

그러자 힙스터 명세서가 그대로 나왔다. 첫째 행에서는 명세서 첫째 칸에만 1을 곱하고 나머지 칸에는 0을 곱하니, 첫째 칸의 수가 그대로 남았다. 다른 행도 마찬가지였다.
어떤 명세서든 각 칸의 수가 그대로 나오는 표였다.

과학자들은 이 표를 항등행렬(identity matrix)이라 부르고 $I$로 썼다.

표준과일가게는 각 열을 표준 명세서로 적은 환산표 $W$를 입구에 걸었다. 손님 바구니는 그대로 두고, 힙스터 명세서를 표준과일가게 명세서로 바꾸는 표였다.

## 역환산표

힙스터과일가게 입구에는 단골이 세워 둔 안내판이 있었다. 표준 세트를 힙스터 명세서로 적은 안내판이었다.
직원은 안내판에 적힌 명세서를 사과, 바나나, 당근, 두리안 순서로 열에 붙여 한 표로 묶었다.

$$
\begin{gathered}
\text{표준 세트를 힙스터과일가게 명세서로} \\[8pt]
\begin{array}{lcccc}
 & [e_1]_H & [e_2]_H & [e_3]_H & [e_4]_H \\
 & \text{사과 세트} & \text{바나나 세트} & \text{당근 세트} & \text{두리안 세트} \\[8pt]
\begin{matrix}
\text{사과바나나 }(h_1) \\
\text{바나나당근 }(h_2) \\
\text{당근두리안 }(h_3) \\
\text{두리안 }(h_4)
\end{matrix} &
\begin{bmatrix} 1 \\ -1 \\ 1 \\ -1 \end{bmatrix} &
\begin{bmatrix} 0 \\ 1 \\ -1 \\ 1 \end{bmatrix} &
\begin{bmatrix} 0 \\ 0 \\ 1 \\ -1 \end{bmatrix} &
\begin{bmatrix} 0 \\ 0 \\ 0 \\ 1 \end{bmatrix}
\end{array}
\end{gathered}
$$

힙스터과일가게도 안내판의 제목을 “표준과일가게에서 온 손님을 위한 환산표”로 바꿨다.

앞서 왔던 손님이 이번에는 표준과일가게 명세서를 들고 힙스터과일가게를 찾았다.
바구니 $v$에는 여전히 네 과일이 하나씩 들어 있었다.

$$
\begin{aligned}
v &= [1, 1, 1, 1] && \text{들고 온 바구니} \\[6pt]
[v]_E &= \begin{pmatrix} 1 \\ 1 \\ 1 \\ 1 \end{pmatrix} && \text{표준과일가게 명세서}
\end{aligned}
$$

직원은 환산표의 각 행에 적힌 수를 표준 명세서의 같은 순서에 있는 수와 곱한 뒤 더했다.

$$
\begin{aligned}
[v]_H &= {\color{RoyalBlue}\begin{pmatrix}
1 & 0 & 0 & 0 \\
-1 & 1 & 0 & 0 \\
1 & -1 & 1 & 0 \\
-1 & 1 & -1 & 1
\end{pmatrix}}
{\color{DarkOrange}\begin{pmatrix}
1 \\
1 \\
1 \\
1
\end{pmatrix}} \\[8pt]
 &= \begin{pmatrix}
{\color{RoyalBlue}1} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}1} \\[4pt]
{\color{RoyalBlue}(-1)} \times {\color{DarkOrange}1} + {\color{RoyalBlue}1} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}1} \\[4pt]
{\color{RoyalBlue}1} \times {\color{DarkOrange}1} + {\color{RoyalBlue}(-1)} \times {\color{DarkOrange}1} + {\color{RoyalBlue}1} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}1} \\[4pt]
{\color{RoyalBlue}(-1)} \times {\color{DarkOrange}1} + {\color{RoyalBlue}1} \times {\color{DarkOrange}1} + {\color{RoyalBlue}(-1)} \times {\color{DarkOrange}1} + {\color{RoyalBlue}1} \times {\color{DarkOrange}1}
\end{pmatrix} \\[8pt]
 &= \begin{pmatrix}
1 \\
0 \\
1 \\
0
\end{pmatrix}
\end{aligned}
$$

처음 받았던 힙스터 명세서 $[1, 0, 1, 0]$이 똑같이 나왔다.

손님은 다시 표준과일가게로 가서, 이 명세서를 환산표 $W$에 넣었다.

$$
W\,[v]_H = W\begin{pmatrix} 1 \\ 0 \\ 1 \\ 0 \end{pmatrix}
= \begin{pmatrix} 1 \\ 1 \\ 1 \\ 1 \end{pmatrix}
= [v]_E
$$

두 환산표를 차례로 쓰니 원래의 표준 명세서가 나왔다.

표준 세트마다 같은 결과를 얻을 수 있었다. 새 환산표로 힙스터 명세서를 구한 뒤 $W$에 넣으면, 원래의 표준 명세서가 나왔다. 각 표는 열마다 세트 개수를 곱해 더하므로, 표준 세트를 조합한 어떤 바구니의 명세서도 두 표를 차례로 쓰면 원래대로 돌아왔다.

과학자들은 $W$로 바꾼 명세서를 원래대로 되돌리는 표를 역환산표(역행렬, inverse matrix)라 부르고, $W^{-1}$로 적었다.

$$
\begin{aligned}
W^{-1} &= \begin{pmatrix}
1 & 0 & 0 & 0 \\
-1 & 1 & 0 & 0 \\
1 & -1 & 1 & 0 \\
-1 & 1 & -1 & 1
\end{pmatrix} \\[8pt]
[v]_H &= W^{-1}\,[v]_E
\end{aligned}
$$

표준 명세서는 $W^{-1}$로 바꾼 뒤 $W$로 되돌렸고, 힙스터 명세서는 $W$로 바꾼 뒤 $W^{-1}$로 되돌렸다.
이를 식으로 쓸 때는 먼저 하는 계산을 괄호 안에 적었다.

$$
\begin{aligned}
W\,(W^{-1}\,[v]_E) &= [v]_E \\[8pt]
W^{-1}\,(W\,[v]_H) &= [v]_H
\end{aligned}
$$

두 표를 어느 순서로 쓰든 명세서는 원래대로 나왔다. 항등행렬을 곱했을 때와 같은 결과였다.

| 환산표 | 붙인 곳 | 변환 방향 | 각 열의 내용 |
| --- | --- | --- | --- |
| $W$ | 표준과일가게 입구 | 힙스터 명세서 → 표준 명세서 | 힙스터 세트의 표준 명세서 |
| $W^{-1}$ | 힙스터과일가게 입구 | 표준 명세서 → 힙스터 명세서 | 표준 세트의 힙스터 명세서 |

손님은 가게를 옮길 때마다 환산표로 명세서를 바꿨다. 명세서에 적힌 수는 달라져도, 손에 든 바구니는 같았다.
