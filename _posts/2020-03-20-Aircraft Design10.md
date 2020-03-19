---
layout: post
title: Aircraft Design <br> 캠버 항력 (Camber Drag) <br>
author: "Dajung Kim"
comments: true
---

캠버항력은 에어포일의 캠버와 날개의 비틀림 각에 의해서 유발되는 항력이며 아래와 같이 표현할 수 있다.

$$
C_{D_{camber}} = \frac{e}{1-e} K (\Delta C_{L}^{2})
$$

여기서 e는 스팬 효율계수이며 K는 유도항력 비례상수, $$\Delta C_{L}$$은 캠버에 의한 양력 증가분이며 아래와 같다.

$$
\Delta C_{L} = \left( 1-\frac{1}{\pi \cdot A \cdot K} \right) C_{Lopt}
$$

여기서 $$C_{Lopt}$$는 일반적인 에어포일의 경우에 다음과 같다. 

$$
C_{Lopt} = 0.8505 \left(1-e^{-18.728(f/c)}\right)
$$

f/c는 최대캠버와 날개시위의 비이다. 

초 임계 에어포일의 경우에 $$C_{Lopt}$$는 아래와 같다.

$$
C_{Lopt} = 0.5195 (C_{Ld})^{0.75}
$$

여기서 $$C_{Ld}$$는 설계 양력계수이다. 

만일 e=1.0이라면 아래와 같은 경험식을 사용하여 캠버항력을 구한다. 

$$
C_{D_{camber}} = 0.7 (\Delta C_{L})^{2} \frac{S_{exp}}{S_{ref}}
$$