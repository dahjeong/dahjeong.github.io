---
layout: post
title: Aircraft Design (Estimating preliminary design parameters) <br>
       항공기 설계 (설계 파라미터 추정) <br>
author: "Dajung Kim"
comments: true
---

### 1. 설계 이륙 총 중량 예측
   
1-1. 최대양항비 (Maximum Lift and Drag ratio) 추정

유사항공기의 표피 면적비를 그래프를 이용하여 표피 면적비를 구함.

$$\frac{S_{wet}}{S_{ref}}$$

$$S_{wet}$$: 항공기 표피 면적비 (공기와 접촉하고 있는 면적 전체)

$$S_{ref}$$: 항공기 날개 면적 (항공기 위에서 projection 했을 때 면적)

가로세로비(A)를 특정 값으로 결정하면 표피 면적 가로세로비를 구함.

$$
A_{wet} = A/(S_{wet}/S_{ref})
$$

그림에서 최대 양항비$$ \left( (\frac{L}{D})_{max} \right) $$를 추정.

1-2. 연료중량비 (Fuel and Weight ratio) 추정
- STTO(Start, Taxi, and Take-off)

$$
W_{1}/W_{0} = 0.97
$$

- 상승(Climb)

$$
W_{2}/W_{1} = 0.985
$$

- 순항(Cluise)

순항거리(R)와 순항속도(V) 가 주어짐.

비연료소모율은

$$
C=C_{bhp} \frac{V}{550 \nu_{p}} 
$$

표로 부터 순항상태의 엔진 비연료 소모율($$C_{bhp}:lb(hr-bhp)$$)를 구함.

프로펠러 항공기의 최적 순항 시의 양항비는 

$$
(L/D)_{cruise} = (L/D)_{max}
$$ 

이고 제트 항공기의 경우 최적 순항 시의 양항비는 

$$
(L/D)_{cruise} = 0.866(L/D)_{max}
$$

이를 Breguet range equation에 대입하면 중량비를 추정할 수 있음.

$$
W_{3}/W_{2}=e^{-\frac{RC}{V(L/D)}}
$$

- 로이터(Loiter)
로이터 시간(E)이 주어짐.

표로 부터 로이터 시의 엔진 비연료 소모율($$C_{bhp}:lb(hr-bhp)$$)를 구하고 위의 식을 이용하여 비연료소모율을 구함.

제트 항공기의 로이터시 최적 양항비는 $$(L/D)_{cruise} = (L/D)_{max}$$ 임.

$$
W_{4}/W_{3} = e^{-\frac{EC}{L/D}}
$$

- 하강(Decent)

하강 시에는 연료소모가 매우 적다고 가정함.

$$
W_{5}/W_{4} = 1
$$

- 착륙(Land)

$$
W_{6}/W_{5} = 0.995
$$

- Reserve
  
reserve 조건이 속도(V)와 지속 시간(t)으로 주어짐.

reserve 거리는

$$
R = Vt
$$ 

양항비, 비연료소무율은 순항과 같은 값을 사용함. 

$$
W_{7}/W_{6}=e^{-\frac{RC}{V(L/D)}}
$$

최종 연료중량비는 예비연료비 5% 또는 10%와 갇힌 연료 1%를 더하여 계산함.

$$
W_{f}/W_{0} = 1.06 \left( 1-\frac{W_{7}}{W_{0}} \right)
$$

1-3. 공허중량비 (Empty weight ratio, $$W_{e}$$) 추정

표로 부터 regression 계수를 찾아 아래 식에 대입함.

$$
W_{e}/W_{0} = AW_{0}^{C}K_{vs}
$$

여기서 
$$
K_{vs} = $$ variable sweep constant<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;= 1.04 if variable sweep<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;= 1.00 if fixed sweep

1-4. 설계 이륙총중량 (Design takeoff gross weight, $$W_{0}$$) 추정.

승무원 하중($$W_{crew}$$), 유상하중($$W_{payload}$$)이 주어지면 아래의 식을 반복 계산하여 설계 이륙총중량($$W_{0}$$)을 찾음.

$$
W_{0}=\frac{W_{crew}+W_{payload}}{1-(W_{f}/W_{0})-(W_{e}/W_{0})}
$$

### 2. 양항곡선 추정

2-1. 표피면적($$S_{wet}$$)

항공기의 설계 이륙총중량으로부터 항공기 표피면적을 구함.

$$
log_{10}S_{wet}=c+dlog_{10}W_{0}
$$

여기서 계수 c와 d는 regression 계수이며 항공기 종류에 따라 아래의 표과 같이 결정됨.

2-2. 등가유해면적(equivalent parasite area, f)

등가표면마찰계수(equivalent skin friction coefficient, $$c_{f}$$)를 가정하면 상관 계수 a, b와 항공기 표피면적($$S_{wet}$$)을 이용하여 등가유해면적을 구함. 

$$c_{f}$$가 작을 수록 항공기의 표면이 매끄럽게 제작된 것을 의미함. 

$$
log_{10}f=a+blog_{10}S_{wet}
$$

2-3. 날개면적($$S_{ref}$$)

$$W_{0}/S_{ref}$$ 를 특정값으로 가정하고 앞에서 구한 설계 이륙총중량($$W_{0}$$)을 이용하여 날개면적($$S_{ref}$$)을 구함.


2-4. 최소항력계수($$C_{D_{0}}$$)

최소항력계수는 점성에 의한 표면마찰과 관계있으며 아래의 식을 통해 구함.

$$
C_{D_{0}}=\frac{f}{S_{ref}}
$$

2-5. 항력($$C_{D}$$)

항공기의 항력은 최소항력계수와 양력에 의한 유도항력의 합으로 구할 수 있음.

$$
C_{D}=C_{D_{0}}+KC_{L}^{2}
$$

여기서 

$$
K=\frac{1}{\pi Ae}
$$

이때 e는 Oswald span efficiency로 타원형 양력분포의 날개는 e=1 임. 일반적으로 0.7에서 0.85의 값을 갖음.

아음속 날개의 경우:

$$
e=1.78(1-0.045A^{0.68})-0.64
$$

앞전 후퇴각이 30도보다 큰 날개의 경우:

$$
e=4.61(1-0.045A^{0.68})(cos\Lambda_{LE})^{0.15}-3.1
$$

### 3. 기능성능 요구도

3-1. 최대속도

특정고도에서 이용 추력(available thrust)을 T라고 할 때, 항공기의 최대속도는 이용 추력이 항력보다 클 때 발생하므로 아래와 같은 식을 만족해야 함.

$$
\left( \frac{T_{altitude}}{W_{remained}} \right) \geq \frac{C_{D_{0}}q}{W_{remained}/S}+\frac{K}{q} \frac{W_{remained}}{S}
$$

피스톤엔진과 프로펠러 항공기 추력 특성은

$$
T_{SL}=550hp_{SL} \frac{nu_{p}}{V} 
$$

high bypass 터보팬엔진의 경우 고도에 따른 추력을 보정해 주어야 함.

$$
T_{altitude}=\frac{0.1}{M_{\inf}}\sigma T_{SL} = \frac{a\sigma}{10V}T_{SL}
$$

연료사용에 따른 중량도 보정해 주어야 함.

$$
W_{remained} = \frac{W_{remained}}{W_{0}}W_{0}
$$

3-2. 상승률

항공기의 비행경로각이 작을 경우 상승률은

$$
R/C = V \left( \frac{T}{W}-\frac{D}{W} \right) = V \left( \frac{T}{W}-\frac{qC_{D_{0}}}{(W/S)} -\frac{K}{q} \frac{W}{S} \right)
$$

피스톤엔진과 프로펠러 항공기의 추력 특성과 중량 보정을 포함하면

$$
R/C = 550\nu_{p} \left( \frac{hp_{SL}}{W_{0}} \right)-\frac{1}{2}\rho V^{3} \frac{C_{D_{0}}}{(W_{0}/S)}-\frac{2K}{\rho V} \left( \frac{W_{0}}{S} \right)
$$

최대상승률이 발생하는 속도는 R/C를 속도로 미분하여 얻을 수 있음.

$$
V=\sqrt{\frac{2}{\rho} \left( \frac{W_{0}}{S} \right)\sqrt{\frac{K}{3C_{D_{0}}}}}
$$

high bypass 터보팬엔진 항공기의 추력 특성과 중량 보정을 포함하면

$$
R/C = V \left( \left(\frac{W_{0}}{W_{remained}} \right)\frac{a\sigma}{10V} \left(\frac{T_{SL}}{W_{0}} \right)-\left(\frac{W_{0}}{w_{remained}} \right)\frac{qC_{D_{0}}}{(W_{0}/S)}-\frac{K}{q} \left(\frac{W_{remained}}{W_{0}} \right)(\frac{W_{0}}{S} \right) \right)
$$

최대상승률이 발생하는 속도는

$$
V = \sqrt{\frac{2}{\rho} \left(\frac{W_{remained}}{W_{0}} \right) \left(\frac{W_{0}}{S} \right)\sqrt{\frac{K}{3C_{D_{0}}}}}
$$ 

3-3. 상승한계

표에서 항공기 타입에 따른 최대 상승률(R/C)을 찾고 상승 한계에 적용함.

피스톤엔진과 프로펠러 항공기의 상승한계는

$$
\left( \frac{hp_{SL}}{W_{0}} \right) \geq \frac{\rho C_{D_{0}}}{1100 \nu} \left( \frac{V^{3}}{W_{0}/S} \right)+\left( \frac{K}{275 \nu_{p}} \right)\frac{1}{V} \left( \frac{W_{0}}{S} \right)+\frac{R/C}{550 \nu_{p}}
$$

high bypass 터보팬엔진 항공기의 상승한계는 

$$ 
\left( \frac{T_{SL}}{W_{0}} \right) \geq \frac{r\rho C_{D_{0}}}{a \sigma} \frac{V^{3}}{(W_{0}/S)}+\left( \frac{W_{remained}}{W_{0}} \right)^{2} \left( \frac{a \sigma K}{5\rho} \right) \frac{1}{V} \left( \frac{W_{0}}{S} \right)
$$

### 4. 활주성능 요구도

4-1. 이륙거리

이륙거리는 지상활주거리(Ground roll)는 정지상태에서 가속하여 속도가 이륙속도(통상 실속속도의 1.1배)에 이르렀을 때, 즉 바퀴가 지면을 떠날 때까지의 활주거리임.

제트 항공기의 경우

$$
\frac{W_{0}}{S} \leq (TOP) \sigma C_{L_{TO}} \left( \frac{T_{SL}}{W_{0}} \right)
$$

프로펠러 항공기의 경우

$$
\frac{W_{0}}{S} \leq (TOP)\sigma C_{L_{TO}} \left( \frac{hp_{SL}}{W_{0}} \right) 
$$

4-2. 착륙거리

착륙거리는 지상활주거리와 장애물 통과거리의 합임.

$$
{\frac{W_{0}}{S}} \leq {\frac{S_{landing}-S_{a}}{80} \sigma C_{L_{max}} \frac{W_{0}}{W_{remained}}}
$$

여기서 첫 항은 지상활주거리이며 바퀴가 접지하여 정지할 때까지의 거리를 의미함.

$$S_{a}$$은 장애물 통과거리이며 항공기 고도 50ft에서부터 바퀴가 접지할 때까지의 거리를 의미함.

$$S_{a}$$ = 1,000(여객기 등급, 여기서 활공각은 3도)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;= 600(경항공기, Power-off Approach)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;= 450(단거리 이착륙기, 활공각은 7도)

4-3. 실속속도

실속속도는 항공기가 최대양력계수 상태에서 등속수평비행하는 속도임.

FAR23 규정에 따르면 총 이륙중량 12,500lb 이하의 항공기는 특별한 경우(다발엔진을 채택하거나 특별한 상승률을 요구하는 경우)가 아니면 실속속도가 61knots를 넘어서는 안됨. 

실속속도의 정의와 내부연료 70$$\%$$를 고려하면 실속속도는 

$$
{ \frac{W_{0}}{S} } \leq {\frac{1}{2} \rho V_{stall}^{2} C_{L_{max}} \frac{W_{0}}{W_{70\%}}}
$$
