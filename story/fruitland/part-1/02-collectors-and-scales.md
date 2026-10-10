# 2장. 수집가와 저울

사람들에게 취향이 생기기 시작했다. 그러자 바구니를 사들이는 수집가가 나타났다.
표준과일가게는 바구니에 무엇이 들었는지 명세서에 적어 주었고, 수집가는 그 바구니가 얼마짜리인지 쳐 주었다.

수집가마다 좋아하는 바구니가 하나씩 있었다. 그 바구니에 수집가의 취향이 담겨 있었다.
과일 한 가지만 든 바구니도 있었고, 여러 과일을 섞은 바구니도 있었다.

## 값 매기기

처음 나타난 수집가는 '사과' 수집가였다. 이 수집가의 바구니에는 사과 1개만 들어 있었다.
그는 손님이 가져온 바구니의 사과 1개당 1원씩 쳐 주고, 나머지 과일에는 0원을 쳐 주었다.

하루는 세 손님이 바구니를 팔러 왔다.

$$
\begin{array}{l@{\qquad}l}
\text{바구니와 명세서} & \text{값 계산} \\[8pt]
\text{사과 수집가: 사과 1개} & \text{사과 1개당 }{\color{RoyalBlue}1}\text{원, 나머지 과일은 }{\color{RoyalBlue}0}\text{원} \\
u = [{\color{RoyalBlue}1, 0, 0, 0}] & \\[12pt]
\text{첫째 손님: 사과 2개, 당근 1개} & \text{사과 1개당 }{\color{RoyalBlue}1}\text{원} \times \text{사과 }{\color{DarkOrange}2}\text{개} \\
v_1 = [{\color{DarkOrange}2, 0, 1, 0}] & {\color{RoyalBlue}1} \times {\color{DarkOrange}2} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\
 & 2 + 0 + 0 + 0 = 2\text{원} \\[12pt]
\text{둘째 손님: 바나나 3개} & \text{사과 1개당 }{\color{RoyalBlue}1}\text{원} \times \text{사과 }{\color{DarkOrange}0}\text{개} \\
v_2 = [{\color{DarkOrange}0, 3, 0, 0}] & {\color{RoyalBlue}1} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}3} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\
 & 0 + 0 + 0 + 0 = 0\text{원} \\[12pt]
\text{셋째 손님: 모든 과일 1개씩} & \text{사과 1개당 }{\color{RoyalBlue}1}\text{원} \times \text{사과 }{\color{DarkOrange}1}\text{개} \\
v_3 = [{\color{DarkOrange}1, 1, 1, 1}] & {\color{RoyalBlue}1} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}1} \\
 & 1 + 0 + 0 + 0 = 1\text{원}
\end{array}
$$

'사과' 수집가에게는 손님 바구니에 사과가 몇 개 들었는지가 중요했다.

사람들은 바구니가 $u$인 수집가가 손님 바구니 $v$에 쳐 준 값을 $u \cdot v$로 적기로 했다.

## 다른 수집가

뒤이어 '사과 2개' 수집가와 '사과 1개 바나나 2개' 수집가도 나타났다.
'사과 2개' 수집가는 사과 1개에 2원을 쳐 주었고, '사과 1개 바나나 2개' 수집가는 사과 1개에 1원, 바나나 1개에 2원을 쳐 주고, 당근과 두리안에는 0원을 쳐 주었다.
이 수집가들은 자기 바구니에 든 각 과일의 개수를 그 과일 1개에 쳐 줄 값으로 삼았다.

모든 과일을 1개씩 담은 손님이 두 수집가에게 같은 바구니를 보여 주었다.

$$
\begin{array}{l@{\qquad}l}
\text{바구니와 명세서} & \text{값 계산} \\[8pt]
\text{손님: 모든 과일 1개씩} & \\
v = [{\color{DarkOrange}1, 1, 1, 1}] & \\[12pt]
\text{사과 2개 수집가: 사과 2개} & \text{사과 1개당 }{\color{RoyalBlue}2}\text{원} \times \text{사과 }{\color{DarkOrange}1}\text{개} \\
u_1 = [{\color{RoyalBlue}2, 0, 0, 0}] & {\color{RoyalBlue}2} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}1} \\
 & 2 + 0 + 0 + 0 = 2\text{원} \\[12pt]
\text{사과 1개 바나나 2개 수집가:} & \text{사과 1개당 }{\color{RoyalBlue}1}\text{원} \times \text{사과 }{\color{DarkOrange}1}\text{개} \\
\text{사과 1개, 바나나 2개} & {}+ \text{바나나 1개당 }{\color{RoyalBlue}2}\text{원} \times \text{바나나 }{\color{DarkOrange}1}\text{개} \\
u_2 = [{\color{RoyalBlue}1, 2, 0, 0}] & {\color{RoyalBlue}1} \times {\color{DarkOrange}1} + {\color{RoyalBlue}2} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}1} \\
 & 1 + 2 + 0 + 0 = 3\text{원}
\end{array}
$$

같은 바구니라도 수집가의 취향에 따라 쳐 주는 값이 달랐다.

## 두리안을 싫어하는 수집가

어느 '사과' 수집가는 두리안 냄새를 싫어했다. 두리안이 섞여 오면 1개마다 1원씩 값을 깎았다. 이 수집가의 바구니에는 두리안이 $-1$개 들어 있었다.

$$
\begin{array}{l@{\qquad}l}
\text{바구니와 명세서} & \text{값 계산} \\[8pt]
\text{두리안을 싫어하는 사과 수집가:} & \text{사과 1개당 }{\color{RoyalBlue}1}\text{원} \\
\text{사과 1개, 두리안 }-1\text{개} & \text{두리안 1개당 }{\color{RoyalBlue}-1}\text{원} \\
u = [{\color{RoyalBlue}1, 0, 0, -1}] & \\[12pt]
\text{첫째 손님: 사과 1개} & \text{사과 1개당 }{\color{RoyalBlue}1}\text{원} \times \text{사과 }{\color{DarkOrange}1}\text{개} \\
v_1 = [{\color{DarkOrange}1, 0, 0, 0}] & {}+ \text{두리안 1개당 }{\color{RoyalBlue}(-1)}\text{원} \times \text{두리안 }{\color{DarkOrange}0}\text{개} \\
 & {\color{RoyalBlue}1} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}(-1)} \times {\color{DarkOrange}0} \\
 & 1 + 0 + 0 + 0 = 1\text{원} \\[12pt]
\text{둘째 손님: 사과 1개, 두리안 1개} & \text{사과 1개당 }{\color{RoyalBlue}1}\text{원} \times \text{사과 }{\color{DarkOrange}1}\text{개} \\
v_2 = [{\color{DarkOrange}1, 0, 0, 1}] & {}+ \text{두리안 1개당 }{\color{RoyalBlue}(-1)}\text{원} \times \text{두리안 }{\color{DarkOrange}1}\text{개} \\
 & {\color{RoyalBlue}1} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}(-1)} \times {\color{DarkOrange}1} \\
 & 1 + 0 + 0 + (-1) = 0\text{원} \\[12pt]
\text{셋째 손님: 두리안 2개} & \text{사과 1개당 }{\color{RoyalBlue}1}\text{원} \times \text{사과 }{\color{DarkOrange}0}\text{개} \\
v_3 = [{\color{DarkOrange}0, 0, 0, 2}] & {}+ \text{두리안 1개당 }{\color{RoyalBlue}(-1)}\text{원} \times \text{두리안 }{\color{DarkOrange}2}\text{개} \\
 & {\color{RoyalBlue}1} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}(-1)} \times {\color{DarkOrange}2} \\
 & 0 + 0 + 0 + (-2) = -2\text{원}
\end{array}
$$

값이 음수인 바구니는 손님이 돈을 얹어 줘야 수집가가 받아 줬다.
바구니에 음수 개수가 들 수 있었듯이, 수집가가 쳐 주는 값도 음수가 될 수 있었다.

## 무가치한 바구니

수집가가 0원을 쳐 주는 바구니는 그 수집가에게 무가치한 바구니였다. 사람들은 0원이 되는 이유가 서로 다르다는 것을 알아냈다.

먼저, 수집가가 값을 쳐 주지 않는 과일만 든 바구니가 있었다. '사과' 수집가에게 바나나 1개를 가져가면 사과가 없어서 0원을 받았다.

$$
\begin{array}{l@{\qquad}l}
\text{사과 수집가: 사과 1개} & \text{값 계산(원)} \\
u = [{\color{RoyalBlue}1, 0, 0, 0}] & {\color{RoyalBlue}1} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\
\text{손님: 바나나 1개} & 0 + 0 + 0 + 0 = 0 \\
 v = [{\color{DarkOrange}0, 1, 0, 0}] &
\end{array}
$$

과일이 섞여 있어도 더해 주는 값과 깎는 값이 같으면 0원이었다. 두리안을 싫어하는 사과 수집가는 사과 1개에 1원을 더하고 두리안 1개에 1원을 깎았다.

$$
\begin{array}{l@{\qquad}l}
\text{두리안을 싫어하는 사과 수집가} & \text{값 계산(원)} \\
u = [{\color{RoyalBlue}1, 0, 0, -1}] & {\color{RoyalBlue}1} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}(-1)} \times {\color{DarkOrange}1} \\
\text{손님: 사과 1개, 두리안 1개} & 1 + 0 + 0 + (-1) = 0 \\
 v = [{\color{DarkOrange}1, 0, 0, 1}] &
\end{array}
$$

영바구니는 누구에게나 무가치했다. 어느 수집가든 빈 바구니에는 값을 더하거나 깎을 과일이 없었다.

$$
\begin{array}{l@{\qquad}l}
\text{어느 수집가든} & \text{값 계산(원)} \\
u = [{\color{RoyalBlue}a, b, c, d}] & {\color{RoyalBlue}a} \times {\color{DarkOrange}0} + {\color{RoyalBlue}b} \times {\color{DarkOrange}0} + {\color{RoyalBlue}c} \times {\color{DarkOrange}0} + {\color{RoyalBlue}d} \times {\color{DarkOrange}0} \\
\text{손님: 빈 바구니} & 0 + 0 + 0 + 0 = 0 \\
v = 0_V = [{\color{DarkOrange}0, 0, 0, 0}] &
\end{array}
$$

0원을 받았다고 빈 바구니인 것은 아니었다. 값을 쳐 주지 않는 과일만 들어 있을 수도 있고, 더해 주는 값과 깎는 값이 같을 수도 있었다.

또한 바구니가 무가치한지는 누가 매기느냐에 따라 달랐다. 앞서 사과 수집가에게 0원을 받은 바나나 바구니도 바나나 수집가에게는 1원짜리였다.

$$
\begin{array}{l@{\qquad}l}
\text{바나나 수집가: 바나나 1개} & \text{값 계산(원)} \\
u = [{\color{RoyalBlue}0, 1, 0, 0}] & {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}1} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\
\text{손님: 바나나 1개} & 0 + 1 + 0 + 0 = 1 \\
 v = [{\color{DarkOrange}0, 1, 0, 0}] &
\end{array}
$$

반대로 바나나 수집가에게 사과 1개를 가져가면 0원이었다.

$$
\begin{array}{l@{\qquad}l}
\text{바나나 수집가: 바나나 1개} & \text{값 계산(원)} \\
u = [{\color{RoyalBlue}0, 1, 0, 0}] & {\color{RoyalBlue}0} \times {\color{DarkOrange}1} + {\color{RoyalBlue}1} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\
\text{손님: 사과 1개} & 0 + 0 + 0 + 0 = 0 \\
 v = [{\color{DarkOrange}1, 0, 0, 0}] &
\end{array}
$$

그래서 사람들은 늘 누구에게 무가치한지를 함께 말했다.

사과 바구니와 바나나 바구니는 역할을 바꿔도 서로에게 무가치했다. 사람들은 이런 두 바구니를 서로 무가치하다고 했고, 과학자들은 이 관계를 **직교**(orthogonal)라 불렀다.

$$
u \cdot v = 0 \quad \Longleftrightarrow \quad u \text{와 } v \text{는 직교한다}
$$

## 합쳐 팔기

두 친구가 바구니를 합쳐 '사과 1개 바나나 2개' 수집가에게 팔기로 했다. 그런데 따로 팔 때보다 값을 적게 쳐 주면 어쩌나 걱정이 되었다.

두 친구는 따로 팔 때와 합쳐 팔 때의 값을 계산해 보았다.

$$
\begin{array}{l@{\qquad}l}
\text{바구니와 명세서} & \text{값 계산(원)} \\[6pt]
\text{수집가: 사과 1개, 바나나 2개} & \text{사과 1개당 }{\color{RoyalBlue}1}\text{원, 바나나 1개당 }{\color{RoyalBlue}2}\text{원} \\[6pt]
u = [{\color{RoyalBlue}1, 2, 0, 0}] & \\[6pt]
\text{첫째 친구: 사과 1개, 당근 1개} & {\color{RoyalBlue}1} \times {\color{DarkOrange}1} + {\color{RoyalBlue}2} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[6pt]
v = [{\color{DarkOrange}1, 0, 1, 0}] & 1 + 0 + 0 + 0 = 1 \\[6pt]
\text{둘째 친구: 바나나 1개} & {\color{RoyalBlue}1} \times {\color{DarkOrange}0} + {\color{RoyalBlue}2} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[6pt]
w = [{\color{DarkOrange}0, 1, 0, 0}] & 0 + 2 + 0 + 0 = 2 \\[6pt]
\text{합친 바구니: 사과 1개, 바나나 1개, 당근 1개} & {\color{RoyalBlue}1} \times {\color{DarkOrange}1} + {\color{RoyalBlue}2} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[6pt]
v + w = [{\color{DarkOrange}1, 1, 1, 0}] & 1 + 2 + 0 + 0 = 3
\end{array}
$$

합쳐 팔아도 따로 팔 때와 같은 값을 받았다.

$$
\begin{aligned}
u \cdot (v + w) &= u \cdot v + u \cdot w \\
                &= 1 + 2 \\
                &= 3
\end{aligned}
$$

그래서 두 친구는 받은 3원을 각자 바구니 값대로 첫째가 1원, 둘째가 2원씩 나눠 가졌다.

두 친구는 바구니를 불리면 값도 같은 배율로 늘어나는지 궁금해졌다. 첫째 친구의 바구니를 두 배로 불려 값을 계산했다.

$$
\begin{array}{l@{\qquad}l}
\text{바구니와 명세서} & \text{값 계산(원)} \\[6pt]
\text{첫째 친구의 바구니를 두 배로} & {\color{RoyalBlue}1} \times {\color{DarkOrange}2} + {\color{RoyalBlue}2} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}2} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\
2v = [{\color{DarkOrange}2, 0, 2, 0}] & 2 + 0 + 0 + 0 = 2
\end{array}
$$

바구니를 두 배로 불리자 값도 두 배가 되었다.

$$
u \cdot (2v) = 2\,(u \cdot v) = 2 \times 1 = 2
$$

## 역할 바꾸기

'사과' 수집가에게 '사과 1개 바나나 2개' 바구니를 가져가면 1원을 받았다. 이번에는 역할을 바꿔 보았다.
'사과 1개 바나나 2개' 수집가에게 사과 1개를 가져가면 얼마를 받을까?

$$
\begin{gathered}
u = [1, 0, 0, 0], \quad v = [1, 2, 0, 0] \\[12pt]
\begin{array}{l@{\qquad}l}
\text{수집가와 손님} & \text{값 계산(원)} \\[6pt]
\text{수집가: 사과, 손님: 사과 1개 바나나 2개} & u \cdot v
\\
 & = {\color{RoyalBlue}1} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}2} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\
 & = 1 + 0 + 0 + 0 = 1 \\[12pt]
\text{수집가: 사과 1개 바나나 2개, 손님: 사과} & v \cdot u
\\
 & = {\color{RoyalBlue}1} \times {\color{DarkOrange}1} + {\color{RoyalBlue}2} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\
 & = 1 + 0 + 0 + 0 = 1
\end{array}
\end{gathered}
$$

가격과 개수의 자리가 바뀌었지만, 과일마다 곱한 값은 같았다. 두 바구니의 역할을 바꿔도 값은 같았다.
과학자들은 이 성질을 **대칭성**이라 불렀다.

$$
u \cdot v = v \cdot u
$$

## 취향 저격

사람들은 수집가의 취향에 꼭 맞는 바구니에는 얼마를 쳐 줄지 궁금해졌다. 그래서 수집가의 바구니와 똑같은 바구니를 가져갔다. 수집가는 자기 마음에 꼭 드는 바구니라며 무척 반겼다.
사람들은 수집가의 바구니와 손님 바구니를 저울의 두 접시에 하나씩 올려 값을 매겼다. 두 바구니가 같을 때는 이 일을 **맞달기**라 불렀다.

$$
\begin{array}{l@{\qquad}l}
\text{바구니와 명세서} & \text{값 계산(원)} \\[4pt]
\text{수집가: 사과 1개, 바나나 2개} & v \cdot v \\[4pt]
v = [{\color{RoyalBlue}1, 2, 0, 0}] & = {\color{RoyalBlue}1} \times {\color{DarkOrange}1} + {\color{RoyalBlue}2} \times {\color{DarkOrange}2} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[4pt]
\text{손님: 수집가와 똑같은 바구니} & = 1 + 4 + 0 + 0 = 5 \\[4pt]
v = [{\color{DarkOrange}1, 2, 0, 0}] &
\end{array}
$$

두리안이 $-1$개 든 바구니도 맞달아 보았다.

$$
\begin{array}{l@{\qquad}l}
\text{바구니와 명세서} & \text{값 계산(원)} \\[4pt]
\text{수집가: 사과 1개, 두리안 -1개} & v \cdot v \\[4pt]
v = [{\color{RoyalBlue}1, 0, 0, -1}] & = {\color{RoyalBlue}1} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}(-1)} \times {\color{DarkOrange}(-1)} \\[4pt]
\text{손님: 수집가와 똑같은 바구니} & = 1 + 0 + 0 + 1 = 2 \\[4pt]
v = [{\color{DarkOrange}1, 0, 0, -1}] &
\end{array}
$$

반면 빈 바구니는 맞달아도 0원이었다.

$$
\begin{aligned}
v &= 0_V = [0, 0, 0, 0] \\[6pt]
v \cdot v &= {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\
          &= 0 + 0 + 0 + 0 = 0
\end{aligned}
$$

사람들은 다른 바구니들도 각각 맞달아 보았다. 같은 과일의 개수끼리 곱해 더하므로, 맞단 값은 각 개수의 제곱을 더한 것이었다.

$$
\begin{aligned}
v &= [a, b, c, d] \\[6pt]
v \cdot v &= a^2 + b^2 + c^2 + d^2
\end{aligned}
$$

제곱한 수는 음수가 될 수 없었다. 하나라도 0이 아닌 성분이 있으면 합은 양수였고, 모든 성분이 0일 때만 합도 0이었다. 맞단 값이 0인 바구니는 영바구니뿐이었다.

$$
\begin{aligned}
v \ne 0_V &\Rightarrow v \cdot v > 0 \\[6pt]
v \cdot v = 0 &\Longleftrightarrow v = 0_V
\end{aligned}
$$

## 저울법

과일나라는 사람들이 알아낸 세 가지를 법으로 정했다.

저울은 두 바구니를 올려 값을 매기는 도구였다.

앞으로 어떤 셈법이 나오더라도 아래 세 조항을 지켜야 저울로 인정했다.

> [!important] 저울법
>
> 1. 합산: 합쳐서 매기나 따로 매겨 더하나 같다. 몇 배로 불려 매기면 값도 그만큼 불어난다. (합쳐 팔기)
> $u \cdot (v + w) = u \cdot v + u \cdot w$, $\quad u \cdot (kv) = k\,(u \cdot v)$
> 2. 대칭: 어느 접시에 올리든 값이 같다. (역할 바꾸기)
> $u \cdot v = v \cdot u$
> 3. 실재: 빈 바구니가 아니면 맞단 값은 0보다 크다. (취향 저격)
> $v \neq 0_V \Rightarrow v \cdot v > 0$

과학자들은 이 법을 지키는 저울을 **내적**(inner product)이라 불렀다.
