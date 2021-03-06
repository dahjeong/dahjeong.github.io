---
layout: post
title: Aircraft Design <br> 유도항력 (Induced Drag) <br>
author: "Dajung Kim"
comments: true
---

유도항력은 날개에서 양력이 발생하면 필연적으로 발생하는 날개 끝 와류에 의한 항력으로 양력계수의 제곱에 비례한다.

$$
C_{D_{i}} = KC^{2}_{L}
$$

여기서 비례상수 K는 Oswald 스팬 효율계수법(Oswald Span Efficiency Method)과 앞전 흡입법(Leading Edge Suction Method) 두 가지 방법으로 구할 수 있다. 

### Oswald 스팬 효율계산법

아음속 항공기의 경우, 타원형 양력분포를 갖는 날개와 비교한 효율(e)에 의해서 K 값이 결정된다. 

$$
K=\frac{1}{\pi e A}
$$

여기서 스팬효율계수 e는 경험식에 의해서 아래와 같이 결정된다. 

$$
e = 1.78(1-0.045A^{0.68})-0.64,~~~~~~~~~~~~~~~~~~~~~~(\Lambda_{LE} \le 30^{\circ})\\ 
e = 4.61(1-0.045A^{0.68})(\cos \Lambda_{LE})^{0.15}-3.1,~~~(\Lambda_{LE} \le 30^{\circ})
$$

초음속 항공기의 경우, 마하수에 따른 K값을 구하는 경험식은 아래와 같다.

$$
K = \frac{A(M^{2}-1)}{4A\sqrt{M^{2}-1}-2}\cos \Lambda_{L.E.}
$$


### 앞전 흡입법

Oswald 스팬 효율계산법은 받음각이나 비행 속도 영역의 변화에 따른 효과를 고려하지 못하는 단점이 있다. 이를 해결하기 위해서 앞전에서 흡입력을 고려해 주는 앞전 흡입법을 사용한다. 

$$
K=(1-R)K_{0}+RK_{100}
$$

여기서 인자 R은 앞전 흡입계수(Leading Edge Suction Parameter)라고 하며 흡입력에 영향을 주는 인자인다. 앞전 반경이 큰 아음속 날개의 경우 R의 변화가 크지 않아 Oswald 스팬 효율계산법과 유사한 값을 얻는다. 이에 반해 얇은 두께 비와 후퇴각을 가지는 초음속 항공기의 경우에는 아래 그림을 통해 R을 구한다.