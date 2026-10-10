# 5장. 알짜배기

## 있으나 마나 바나나

'사과' 수집가에게 바구니 $[3, 4, 0, 0]$을 가져갔다. 사람들은 바나나를 빼도 같은 값을 받을 수 있는지 비교했다.

$$
\begin{array}{l@{\qquad}l}
\text{바구니와 명세서} & \text{값 계산(원)} \\[8pt]
\text{'사과' 수집가} & \text{사과 1개당 1원, 나머지 과일은 0원} \\[4pt]
u_1 = [1, 0, 0, 0] & \\[12pt]
\text{손님 바구니} & \\[4pt]
v = [3, 4, 0, 0] & u_1 \cdot v \\[6pt]
 & = {\color{RoyalBlue}1} \times {\color{DarkOrange}3} + {\color{RoyalBlue}0} \times {\color{DarkOrange}4} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[6pt]
 & = 3 + 0 + 0 + 0 \\[4pt]
 & = 3 \\[12pt]
\text{바나나를 뺀 바구니} & \\[4pt]
p_1 = [3, 0, 0, 0] & u_1 \cdot p_1 \\[6pt]
 & = {\color{RoyalBlue}1} \times {\color{DarkOrange}3} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[6pt]
 & = 3 + 0 + 0 + 0 \\[4pt]
 & = 3
\end{array}
$$

'사과' 수집가에게 바나나는 있으나 마나였다.

바나나를 뺀 바구니 $p_1$은 수집가의 바구니 $u_1$을 세 배로 불린 것이기도 했다.

$$
\begin{aligned}
k_1 &= 3 \\[6pt]
p_1 &= k_1u_1 \\
 &= {\color{RoyalBlue}3}[{\color{DarkOrange}1, 0, 0, 0}] \\
 &= [{\color{RoyalBlue}3} \times {\color{DarkOrange}1}, {\color{RoyalBlue}3} \times {\color{DarkOrange}0}, {\color{RoyalBlue}3} \times {\color{DarkOrange}0}, {\color{RoyalBlue}3} \times {\color{DarkOrange}0}] \\
 &= [3, 0, 0, 0]
\end{aligned}
$$

사람들은 한 바구니에 배율을 곱해 만들 수 있는 바구니 전부를 그 바구니의 **꼴**(**생성**, span)이라 했다.

예를 들어 '사과' 수집가의 바구니 $u_1$은 어떤 배율로 불려도 사과만 남았다.

$$
\begin{aligned}
k &\in \mathbb{R} \qquad \text{배율(스칼라)} \\[6pt]
ku_1 &= {\color{RoyalBlue}k}[{\color{DarkOrange}1, 0, 0, 0}] \\
 &= [{\color{RoyalBlue}k} \times {\color{DarkOrange}1}, {\color{RoyalBlue}k} \times {\color{DarkOrange}0}, {\color{RoyalBlue}k} \times {\color{DarkOrange}0}, {\color{RoyalBlue}k} \times {\color{DarkOrange}0}] \\
 &= [k, 0, 0, 0]
\end{aligned}
$$

사과만 든 바구니는 모두 $u_1$의 꼴이었다. 뒤집은 바구니도 같은 꼴이었고, 빈 바구니는 어느 꼴에도 들었다.

사람들은 수집가 바구니의 꼴 가운데 그 수집가가 손님 바구니와 같은 값을 쳐 주는 바구니를 그 수집가의 **알짜**(**벡터 정사영**, vector projection)라 불렀다.
바나나를 뺀 바구니 $[3, 0, 0, 0]$은 '사과' 수집가 바구니의 꼴이면서 손님 바구니 $[3, 4, 0, 0]$과 같은 3원을 받았으니, '사과' 수집가의 알짜였다.

바구니에서 알짜를 빼고 남은 것은 **나머지**(**직교 성분**, orthogonal component)라 불렀다.

$$
\begin{aligned}
r_1 &= v - p_1 \\
 &= [{\color{RoyalBlue}3, 4, 0, 0}] - [{\color{DarkOrange}3, 0, 0, 0}] \\
 &= [{\color{RoyalBlue}3} - {\color{DarkOrange}3}, {\color{RoyalBlue}4} - {\color{DarkOrange}0}, {\color{RoyalBlue}0} - {\color{DarkOrange}0}, {\color{RoyalBlue}0} - {\color{DarkOrange}0}] \\
 &= [0, 4, 0, 0] \\[8pt]
u_1 \cdot r_1 &= {\color{RoyalBlue}1} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}4} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\
 &= 0 + 0 + 0 + 0 \\
 &= 0
\end{aligned}
$$

나머지인 바나나 4개에는 0원을 쳐 주었다.

같은 바구니를 '바나나' 수집가에게 보여 주면 알짜와 나머지가 바뀌었다.

이번에는 바나나만 남겨도 손님 바구니와 같은 4원을 받았다.

$$
\begin{array}{l@{\qquad}l}
\text{바구니와 명세서} & \text{'바나나' 수집가의 값 계산(원)} \\[8pt]
\text{'바나나' 수집가} & \\[4pt]
u_2 = [0, 1, 0, 0] & \\[12pt]
\text{손님 바구니} & \\[4pt]
v = [3, 4, 0, 0] & u_2 \cdot v \\[6pt]
 & = {\color{RoyalBlue}0} \times {\color{DarkOrange}3} + {\color{RoyalBlue}1} \times {\color{DarkOrange}4} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[6pt]
 & = 0 + 4 + 0 + 0 \\[4pt]
 & = 4 \\[12pt]
\text{'바나나' 수집가의 알짜} & \\[4pt]
k_2 = 4 & p_2 = k_2u_2 \\[4pt]
p_2 = [0, 4, 0, 0] & u_2 \cdot p_2 \\[6pt]
 & = {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}1} \times {\color{DarkOrange}4} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[6pt]
 & = 0 + 4 + 0 + 0 \\[4pt]
 & = 4 \\[12pt]
\text{'바나나' 수집가의 나머지} & r_2 = v - p_2 \\[4pt]
r_2 = [3, 0, 0, 0] & u_2 \cdot r_2 \\[6pt]
 & = {\color{RoyalBlue}0} \times {\color{DarkOrange}3} + {\color{RoyalBlue}1} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[6pt]
 & = 0 + 0 + 0 + 0 \\[4pt]
 & = 0
\end{array}
$$

같은 바구니라도 수집가에 따라 알짜가 달라질 수 있어서, 사람들은 늘 누구의 알짜인지 함께 말했다.

사람들은 사과와 바나나를 함께 좋아하는 수집가의 알짜도 찾고 싶었다. 사과 7개 바나나 1개가 든 바구니 $[7, 1, 0, 0]$을 앞서 만난 '사과 $\tfrac35$개 바나나 $\tfrac45$개' 수집가에게 가져갔다.

$$
\begin{array}{l@{\qquad}l}
\text{바구니와 명세서} & \text{값 계산(원)} \\[8pt]
\text{'사과 }\dfrac35\text{개 바나나 }\dfrac45\text{개' 수집가} & \\[6pt]
u = \left[\dfrac35, \dfrac45, 0, 0\right] & \\[12pt]
\text{손님 바구니} & \\[4pt]
v = [7, 1, 0, 0] & u \cdot v \\[6pt]
 & = {\color{RoyalBlue}\dfrac35} \times {\color{DarkOrange}7} + {\color{RoyalBlue}\dfrac45} \times {\color{DarkOrange}1} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[6pt]
 & = \dfrac{21}{5} + \dfrac45 + 0 + 0 \\[4pt]
 & = 5
\end{array}
$$

이 수집가는 사과도 바나나도 좋아했다. 한 종류의 과일을 빼는 것으로는 알짜를 찾을 수 없었다.
수집가의 바구니는 사과와 바나나의 비율이 $3:4$인데, 손님 바구니는 그 비율이 아니었다.

사람들은 '사과' 수집가에게서 실마리를 찾았다. '사과' 수집가가 쳐 준 값은 3원이었고, 알짜는 그 수집가의 바구니를 3배로 불린 것이었다.

'사과' 수집가와 이번 수집가의 바구니는 모두 단위바구니라서, 맞달면 1원이었다. 그러니 그 바구니를 3배로 불려 가져가면 3원, 5배로 불려 가져가면 5원을 받을 수 있었다.

이번에 손님 바구니에 쳐 준 값은 5원이니, 수집가의 단위바구니를 5배로 불려 보았다.

$$
\begin{aligned}
k &= u \cdot v \\
 &= 5 \\[6pt]
p &= ku \\
 &= {\color{RoyalBlue}5} \cdot \left[{\color{DarkOrange}\dfrac35, \dfrac45, 0, 0}\right] \\
 &= \left[{\color{RoyalBlue}5} \times {\color{DarkOrange}\dfrac35}, {\color{RoyalBlue}5} \times {\color{DarkOrange}\dfrac45}, {\color{RoyalBlue}5} \times {\color{DarkOrange}0}, {\color{RoyalBlue}5} \times {\color{DarkOrange}0}\right] \\
 &= [3, 4, 0, 0] \\[10pt]
r &= v - p \\
 &= [{\color{RoyalBlue}7, 1, 0, 0}] - [{\color{DarkOrange}3, 4, 0, 0}] \\
 &= [{\color{RoyalBlue}7} - {\color{DarkOrange}3}, {\color{RoyalBlue}1} - {\color{DarkOrange}4}, {\color{RoyalBlue}0} - {\color{DarkOrange}0}, {\color{RoyalBlue}0} - {\color{DarkOrange}0}] \\
 &= [4, -3, 0, 0]
\end{aligned}
$$

수집가에게 알짜와 나머지를 각각 가져가 값을 확인했다.

$$
\begin{array}{l@{\qquad}l}
\text{확인할 바구니} & \text{같은 수집가가 쳐 준 값(원)} \\[8pt]
\text{손님 바구니} & u \cdot v = 5 \qquad \text{앞에서 계산한 값} \\[4pt]
v = [7, 1, 0, 0] & \\[12pt]
\text{알짜} & u \cdot p \\[4pt]
p = [3, 4, 0, 0] & = {\color{RoyalBlue}\dfrac35} \times {\color{DarkOrange}3} + {\color{RoyalBlue}\dfrac45} \times {\color{DarkOrange}4} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[6pt]
 & = \dfrac95 + \dfrac{16}{5} + 0 + 0 \\[6pt]
 & = 5 \\[12pt]
\text{나머지} & u \cdot r \\[4pt]
r = [4, -3, 0, 0] & = {\color{RoyalBlue}\dfrac35} \times {\color{DarkOrange}4} + {\color{RoyalBlue}\dfrac45} \times {\color{DarkOrange}(-3)} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[6pt]
 & = \dfrac{12}{5} - \dfrac{12}{5} + 0 + 0 \\[6pt]
 & = 0
\end{array}
$$

알짜만 가져가도 값은 그대로였고, 나머지는 무가치했다.

수집가의 바구니가 비어 있지 않으면 단위바구니 $u$로 맞출 수 있었다. 손님 바구니 $v$와 이 단위바구니를 저울에 단 값을 배율로 삼아 $u$를 불리면 알짜가 되었다.

$$
\text{알짜} = (u \cdot v)\,u \qquad (\lVert u \rVert = 1)
$$

## 취향의 방향

과학자들은 앞서 구한 알짜와 나머지를 그림으로 보고 싶었다.

당근과 두리안이 없는 바구니라면, 사과 개수는 오른쪽으로, 바나나 개수는 위쪽으로 그려 볼 수 있었다. 음수 개수는 반대쪽으로 그렸다.

빈 바구니를 출발점으로 삼아 손님 바구니와 알짜를 화살표로 그려 보았다. 나머지는 알짜의 끝에서 이어 그리니 손님 바구니의 끝에 닿았다.

수집가의 바구니를 몇 배로 불려 만들 수 있는 바구니는 모두 점선 위에 놓였다. 뒤집은 바구니도 같은 꼴이라서 점선은 출발점의 양쪽으로 뻗었다.

수집가 바구니의 꼴은 그림에서 원점을 지나는 직선이 되었다.

<svg viewBox="-100 -145 690 200" width="620" style="display:block;margin:12px auto;max-width:100%" xmlns="http://www.w3.org/2000/svg" font-family="sans-serif" font-size="12" fill="currentColor">
<g stroke="currentColor" stroke-width="1.5" fill="none">
<line x1="-30" y1="0" x2="120" y2="0" stroke-width="0.7" stroke-dasharray="3 3"/>
<line x1="0" y1="0" x2="72" y2="0" stroke="#7a8fa6" stroke-width="5"/>
<line x1="72" y1="0" x2="72" y2="-96" stroke="#a68a7a" stroke-width="2" stroke-dasharray="5 3"/>
<polyline points="64,0 64,-8 72,-8" stroke-width="1"/>
<line x1="0" y1="0" x2="72" y2="-96" stroke-width="2.5"/>
<polygon points="72,-96 60,-84 70,-80" stroke-width="1" fill="currentColor"/>
</g>
<text x="124" y="4">취향 방향</text>
<text x="30" y="-56" text-anchor="end">바구니 [3, 4, 0, 0]</text>
<text x="36" y="18" text-anchor="middle">알짜 [3, 0, 0, 0]</text>
<text x="80" y="-48">나머지 [0, 4, 0, 0]</text>
<text x="60" y="44" text-anchor="middle">'사과' 수집가</text>
<g transform="translate(300,0)">
<g stroke="currentColor" stroke-width="1.5" fill="none">
<line x1="-24" y1="32" x2="96" y2="-128" stroke-width="0.7" stroke-dasharray="3 3"/>
<line x1="0" y1="0" x2="60" y2="-80" stroke="#7a8fa6" stroke-width="5"/>
<line x1="60" y1="-80" x2="140" y2="-20" stroke="#a68a7a" stroke-width="2" stroke-dasharray="5 3"/>
<polyline points="55.2,-73.6 61.6,-68.8 66.4,-75.2" stroke-width="1"/>
<line x1="0" y1="0" x2="140" y2="-20" stroke-width="2.5"/>
<polygon points="140,-20 128.8,-13.4 127.4,-23.3" stroke-width="1" fill="currentColor"/>
</g>
<text x="102" y="-128">취향 방향</text>
<text x="146" y="-14">바구니 [7, 1, 0, 0]</text>
<text x="22" y="-48" text-anchor="end">알짜 [3, 4, 0, 0]</text>
<text x="106" y="-60">나머지 [4, −3, 0, 0]</text>
<text x="70" y="44" text-anchor="middle">'사과 ⅗개 바나나 ⅘개' 수집가</text>
</g>
</svg>

알짜에 나머지를 이어 그린 것은 두 바구니를 더한 계산과 같았다.

$$
\begin{array}{l@{\qquad}l}
p:\text{ 알짜},\; r:\text{ 나머지},\; v:\text{ 손님 바구니} & \text{두 바구니를 더하면} \\[8pt]
\text{'사과' 수집가의 알짜} & \\[4pt]
p = [3, 0, 0, 0] & p + r \\[6pt]
\text{'사과' 수집가의 나머지} & = [{\color{RoyalBlue}3, 0, 0, 0}] + [{\color{DarkOrange}0, 4, 0, 0}] \\[4pt]
r = [0, 4, 0, 0] & = [{\color{RoyalBlue}3} + {\color{DarkOrange}0}, {\color{RoyalBlue}0} + {\color{DarkOrange}4}, {\color{RoyalBlue}0} + {\color{DarkOrange}0}, {\color{RoyalBlue}0} + {\color{DarkOrange}0}] \\[6pt]
\text{손님 바구니} & = [3, 4, 0, 0] \\[4pt]
v = [3, 4, 0, 0] & = v \\[14pt]
\text{'사과 }\dfrac35\text{개 바나나 }\dfrac45\text{개' 수집가의 알짜} & \\[4pt]
p = [3, 4, 0, 0] & p + r \\[6pt]
\text{'사과 }\dfrac35\text{개 바나나 }\dfrac45\text{개' 수집가의 나머지} & = [{\color{RoyalBlue}3, 4, 0, 0}] + [{\color{DarkOrange}4, -3, 0, 0}] \\[4pt]
r = [4, -3, 0, 0] & = [{\color{RoyalBlue}3} + {\color{DarkOrange}4}, {\color{RoyalBlue}4} + {\color{DarkOrange}(-3)}, {\color{RoyalBlue}0} + {\color{DarkOrange}0}, {\color{RoyalBlue}0} + {\color{DarkOrange}0}] \\[6pt]
\text{손님 바구니} & = [7, 1, 0, 0] \\[4pt]
v = [7, 1, 0, 0] & = v
\end{array}
$$

두 그림에서 알짜는 점선 위에 놓였고, 나머지는 점선과 직각을 이루었다.
알짜가 수집가 바구니와 같은 꼴이라는 것은 점선 위에 놓이는 것으로, 나머지가 그 수집가에게 무가치하다는 것은 직각으로 보였다.

사람들은 손님 바구니를 뒤집으면 알짜도 뒤집히는지 궁금해졌다. 오른쪽 그림의 손님 바구니를 뒤집어 같은 수집가에게 보여 주었다.

$$
\begin{gathered}
\begin{aligned}
u &= \left[\dfrac35, \dfrac45, 0, 0\right] && \text{수집가의 단위바구니} \\
v &= [-7, -1, 0, 0] && \text{뒤집은 손님 바구니}
\end{aligned} \\[8pt]
\begin{aligned}
k &= u \cdot v \\
 &= {\color{RoyalBlue}\dfrac35} \times {\color{DarkOrange}(-7)} + {\color{RoyalBlue}\dfrac45} \times {\color{DarkOrange}(-1)} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} + {\color{RoyalBlue}0} \times {\color{DarkOrange}0} \\[6pt]
 &= -\dfrac{21}{5} - \dfrac45 + 0 + 0 \\[6pt]
 &= -5 \\[8pt]
p &= ku \\
 &= {\color{RoyalBlue}(-5)} \cdot \left[{\color{DarkOrange}\dfrac35, \dfrac45, 0, 0}\right] \\[6pt]
 &= \left[{\color{RoyalBlue}(-5)} \times {\color{DarkOrange}\dfrac35}, {\color{RoyalBlue}(-5)} \times {\color{DarkOrange}\dfrac45}, {\color{RoyalBlue}(-5)} \times {\color{DarkOrange}0}, {\color{RoyalBlue}(-5)} \times {\color{DarkOrange}0}\right] \\[6pt]
 &= [-3, -4, 0, 0]
\end{aligned}
\end{gathered}
$$

이 알짜를 같은 그림에 그리면 원점에서 왼쪽 아래로 향했다.

같은 꼴의 점선 위에 있으면서도, 수집가의 취향 방향과는 반대쪽이었다.
