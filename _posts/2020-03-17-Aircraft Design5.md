---
layout: post
title: Aircraft Design <br> 고양력장치에 의한 양력곡선 변화 <br>
author: "Dajung Kim"
comments: true
---

### 1. 고양력장치에 의한 양력 증가량


고양력장치를 사용하여 얻어지는 항공기의 최대 양력계수와 영 양력받음각 $$\alpha_{L=0}$$ 의 증가량은 다음과 같다. 

$$
\Delta C_{Lmax} = \Delta C_{lmax} \left( \frac{S_{flapped}}{S_{ref}} \right) \cos{\Lambda_{H.L.}}
$$

$$
\Delta \alpha_{L=0} = (\Delta \alpha_{L=0})_{airfoil} \left( \frac{S_{flapped}}{S_{ref}} \right) \cos \Lambda_{H.L.}
$$

여기서 $$S_{flapped}$$는 날개에 고양력장치가 설치되어 있는 부분의 면적을 말한다. 그리고 $$\Lambda_{H.L.}$$ 은 플랩 힌지선의 후퇴각이다. 

1-1. plain Flap 

$$
\Delta C_{l} = C_{l\delta_{f}}\delta_{f} K'
$$

여기서 플랩 각 양력선 기울기 $$C_{l\delta_{f}}$$와 계수 K'는 아래의 그림을 통해서 구할 수 있다.


1-2. Split Flap

$$
\Delta C_{l} = k_{f} (\Delta C_{l})_{c_{f}/c=0.2}
$$

이때 k_{f}와 (\Delta C_{l})_{cf/c=0.2} 는 아래의 그림에서 구한다. 

1-3. Single Slotted Flap

$$
\Delta C_{l} = C_{l\alpha_{f}}\alpha_{\delta_{f}}\delta_{f}
$$

이때 $$\alpha_{\delta_{f}}$$는 아래 그림에서 구할 수 있다. 


플랩 부분의 에어포일 양력선 기울기 $$C_{l\alpha_{f}}$$는 다음과 같이 구할 수 있다. 

$$
C_{l\alpha_{f}}=C_{l\alpha}(c'/c)
$$

여기서

$$
c'/c = 1+2(z_{fh}/c)\tan(\delta_{f}/2)
$$

또한 슬롯의 크기 $$z_{fh}$$는 아래 그림과 같다.


1-4. Fowler Flap

$$
\Delta C_{l} = C_{l\alpha_{f}}\alpha_{\delta_{f}}\delta_{f}
$$

여기서 플랩 에어포일의 양력선 기울기 $$C_{l\alpha_{f}}$$는 다음과 같다. 

$$
C_{l\alpha_{f}}=C_{l\alpha}(1+c_{f}/c)
$$

앞전 플랩(leading edge flap)이 에어포일의 양력계수에 미치는 영향은 앞전 플랩이 없는 경우에 대해서 다음과 같은 관계를 갖는다. 


$$
c_{lmax(with L.E. flap)} = (c''/c)c_{lmax(without L.E. flap)}
$$

여기서 c''는 그림과 같다. 


### 2. 고양력장치 설계를 위한 양력 증가 요구분 추정

2-1. 최대 양력계수 $$C_{Lmax}$$, 이륙 최대 양력계수 $$C_{LmaxTO}$$, 착륙 최대 양력계수 $$C_{LmaxL}$$을 정한다. 

2-2. 실제 항공기 날개에서 양력 손실을 고려해서 앞에서 구한 $$C_{Lmax}$$ 값을 조정해 준다. 

   $$
   C_{Lmax_{W}} = 1.05 \sim 1.1 C_{Lmax}
   $$ 

이때 $$L_{h}/\bar{c}>5.0$$ 이면 1.05를 사용하고 $$L_{h}/\bar{c}<3.0$$이면 1.1을 사용한다. $$L_{h}$$는 항공기 무게중심에서 수평 꼬리 날개 또는 카나드의 공력 중심까지의 거리이다. 

2-3. 35$$^{\circ}$$ 이하의 후퇴각이 있는 경우에 다음의 식을 사용하여 양력 계수를 조정한다.

$$
C_{Lmax_{W}swpt} = C_{Lmax_{W}unswpt}\cos{\Lambda_{c/4}}
$$

후퇴각이 0$$^{\circ}$$ 인 경우에 최대 양력계수값을 다음과 같은 근사식을 통하여 검증한다. 

$$
C_{Lmax_W} = k_{lambda}(C_{lmax_{Root}} + C_{lmax_{Tip}})/2\\
k_{lambda} = 0.88 \text{ for } \lambda = 1.0\\
k_{lambda} = 0.95 \text{ for } \lambda = 0.4
$$

여기서 2차원 에어포일의 최대 양력계수 $$C_{lmax}$$ 는 아래의 그림에서 구한다. 




이때 사용할 레이놀즈 수는 다음 식으로 구한다.

$$
R_{nr} = \rho V c_{r}/\mu \text{ at the root}\\
R_{nt} = \rho V c_{t}/\mu \text{ at the tip}
$$

2-4. 고양력장치로 발생시키고자 하는 양력계수의 증가량을 다음식으로 구한다.

$$
\Delta C_{LmaxTO} = 1.05(C_{LmaxTO}- C_{Lmax})\\
\Delta C_{LmaxL} = 1.05(C_{maxL}-C_{Lmax})
$$

여기서 1.05는 플랩을 이용하여 트림을 잡을 때 손실되는 것을 보상하는 값이다. 

$$
\Delta C_{lmax} = (\Delta C_{Lmax}/ K_{\Lambda})(S_{ref}/S_{flapped})
$$

여기서 $$K_{\Lambda}$$는 플랩이 내려졌을 때 후퇴각의 영향이며 다음의 식으로 구한다.

$$
K_{\Lambda} = (1-0.08\cos^{2}\lambda_{c/4})\cos^{3/4}\Lambda_{c/4}
$$

받음 각 0에서 에어포일의 양력계수 증가량 $$\Delta C_{l}$$ 은 다음과 같다.

$$
\Delta C_{l} = (1/K) \Delta C_{lmax} 
$$

여기서 K는 플랩 시위 비(Flap to Chord Ratio, $$c_{f}/c$$) 및 플랩의 종류에 따라서 다음의 그림을 통해서 구할 수 있다. 



