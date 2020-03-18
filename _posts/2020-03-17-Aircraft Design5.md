---
layout: post
title: Aircraft Design <br> 고양력장치에 의한 양력곡선 변화 <br>
author: "Dajung Kim"
comments: true
---

1. 최대 양력계수 $$C_{Lmax}$$, 이륙 최대 양력계수 $$C_{LmaxTO}$$, 착륙 최대 양력계수 $$C_{LmaxL}$$을 정한다. 

2. 실제 항공기 날개에서 양력 손실을 고려해서 앞에서 구한 $$C_{Lmax}$$ 값을 조정해 준다. 

   $$
   C_{Lmax_{W}} = 1.05 \sim 1.1 C_{Lmax}
   $$ 

이때 $$L_{h}/\bar{c}>5.0$$ 이면 1.05를 사용하고 $$L_{h}/\bar{c}<3.0$$이면 1.1을 사용한다. $$L_{h}$$는 항공기 무게중심에서 수평 꼬리 날개 또는 카나드의 공력 중심까지의 거리이다. 

3. 35$$^{\circ}$$ 이하의 후퇴각이 있는 경우에 다음의 식을 사용하여 양력 계수를 조절한다.

$$
C_{Lmax_{W}swpt} = C_{Lmax_{W}unswpt}\cos{\Lambda_{c/4}}
$$

후퇴각이 0$$^{\circ}$$ 인 경우에 최대 양력계수값을 다음과 같은 근사식을 통하여 검증한다. 

4. 고양력장치로 





고양력장치를 사용하여 얻어지는 항공기의 최대 양력계수와 영 양력받음각 $$\alpha_{L=0}$$ 의 증가량은 다음과 같다. 

$$
\Delta C_{Lmax} = \Delta C_{lmax} \left( \frac{S_{flapped}}{S_{ref}} \right) \cos{\Lambda_{H.L.}}
$$

$$
\Delta \alpha_{L=0} = (\Delta \alpha_{L=0})_{airfoil} \left( \frac{S_{flapped}}{S_{ref}} \right) \cos \Lambda_{H.L.}
$$

여기서 $$S_{flapped}$$는 날개에 고양력장치가 설치되어 있는 부분의 면적을 말한다. 그리고 $$\Lambda_{H.L.}$$ 은 플랩 힌지선의 후퇴각이다. 

