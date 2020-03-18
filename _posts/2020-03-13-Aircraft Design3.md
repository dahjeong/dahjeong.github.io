---
layout: post
title: Aircraft Design <br> 양력 곡선 기울기 추정 <br>
author: "Dajung Kim"
comments: true
---

1. 날개의 양력곡선 기울기 $$(C_{L\alpha})_{W}$$
 
날개의 양력곡선 기울기 $$(C_{L\alpha})_{W}$$ 는 속도 영역에 따라 각각 다른 경험식을 적용한다.

1) 아음속
$$
(C_{L\alpha})_{W}=\frac{\pi A_{effective}}{1+\sqrt{1+[1-(M\cos\Lambda_{c/2})^{2}](\frac{A}{2\cos\Lambda_{c/2}})^{2}}} 
$$
여기서 A는 날개의 가로세로비이고, $$A_{effective}$$는 날개 끝 판(wing tip plate)이나 윙렛이 있는 경우 유효 가로세로비이며 다음과 같이 구한다.

날개 끝 판 $$A_{effective} = A(1+1.9h/b)$$

윙렛       $$A_{effective} \approx 1.2A$$

2) 초음속

이차원 선형 이론에 기초한 경험식
$$
(C_{L\alpha})_{W} = \frac{4}{\sqrt{M^{2}-1}}
$$
(단, M>1/$$\cos\Lambda_{LE}$$)

또는 DATACOM Method를 이용한다. 

3)  천음속

아음속에서 구한 값과 초음속에서 구한 값 사이를 부드러운 곡선으로 연결한다. 

2. 수평꼬리날개에 의한 양력곡선 기울기 증가분 $$\Delta(C_{L\alpha})_{T} $$

$$
\Delta(C_{L\alpha})_{T} = (C'_{L\alpha})_{T} \left( 1- \frac{\partial\epsilon}{\partial\alpha} \right)\frac{q_{t}}{q_{\infty}}\frac{S_{T}}{S_{ref}}
$$

여기서 $$S_{T}$$는 수평꼬리날개 면적, $$S_{ref}$$는 주날개 면적, $$\frac{q_{t}}{q_{\infty}} $$는 꼬리날개 동압이며 흔히 0.9이다. $$\frac{\partial\epsilon}{\partial\alpha}$$는 저속 내리흐름 기울기(Low Speed Downwash Gradient)이고 아래와 같다.

$$
\frac{\partial\epsilon}{\partial\alpha} = \frac{21(C_{L\alpha})_{W}}{A^{0.725}} \left(\frac{\bar{C}}{l_{h}} \right)_{0} \left( \frac{10-3\lambda}{7} \right) \left(1-\frac{h_{t}}{b} \right)
$$

여기서 b는 날개 길이(span)이다.

3. 카나드에 의한 양력곡선 기울기 증가분 $$\Delta(C_{L\alpha})_{C}$$
$$
\Delta(C_{L\alpha})_{C} = (C'_{L\alpha})_{C} \left(1+\frac{\partial \epsilon_{u}}{\partial \alpha}\right)\frac{S_{C}}{S_{ref}}
$$

여기서 $$\frac{\partial \epsilon_{u}}{\partial \alpha}$$는 저속 올려흐름 기울기(Low speed Upwash Gradient)이다.

$$
\frac{\partial \epsilon_{u}}{\partial \alpha} = (0.3A^{0.3}-0.33)\left(\frac{l_{c}}{\bar{c}} \right)^{(1.04+6A^{-1.7})}
$$

4. 양력곡선 기울기 $$C_{L\alpha} = dC_{L/d\alpha}$$
1) 아음속
$$
   C_{L\alpha} = (C_{L\alpha})_{W-B} + \Delta(C_{L\alpha})_{T} + \Delta(C_{L\alpha})_{C}
$$

여기서 $$(C_{L\alpha})_{W-B}$$는 동체-날개 조합의 양력곡선 기울기 이다.

$$
(C_{L\alpha})_{W-B} = (C_{L\alpha})_{W}K_{B}
$$

또한 $$(C_{L\alpha})_{W}$$ 은 앞에서 구한 날개만의 양력곡선 기울기이고 $$K_{B}$$는 동체의 양력영향인자(fuselage lift factor)이다. 

$$
K_{B} = (1+d/b)(1-d/b)^{f}
$$

d는 동체의 지름, b는 날개의 길이이고 f는 다음 식과 같다. 

$$
f=(16+3A^{2})/(8+5A^{2})
$$

A는 날개의 가로세로비(spect ratio)

1) 초음속
$$
   C_{L\alpha} \approx (C_{L\alpha})_{W-B} = (C_{L\alpha})_{W} K_{B} 
$$

초음속 역역의 동체의 양력영향인자(fuselage lift factor) $$K_{B}$$는 다음과 같다. 

$$
K_{B} =1.07(1+d/b)^{2}
$$
