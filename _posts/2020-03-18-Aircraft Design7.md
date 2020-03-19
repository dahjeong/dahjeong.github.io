---
layout: post
title: Aircraft Design <br> 유해항력 (Parasite Drag) <br>
author: "Dajung Kim"
comments: true
---

유해항력은 양력과 독립적으로 발생하는 항력이며 마찰항력(frictio Drag), 형상항력(Form Drag), 압력항력(Pressure Drag), 간섭항력(Interference Drag) 또는 조파항력(Wave Drag) 등이 이에 해당한다. 

$$
C_{D_{p}}=\Sigma(C_{f_{c}} \cdot FF_{c} \cdot Q_{c} \cdot S_{wet_{c}})\frac{1}{S_{ref}} + C_{D_{wave}} + C_{D_{base}} + C_{D_{misc}}
$$

여기서 $$C_{f}$$는 평판의 마찰항력계수(Flat Plate Skin Friction coeffient), FF는 형상 계수(Form Factor), Q는 간섭계수(Interference Factor), $$C_{D_{wave}}$$는 조파항력계수, $$C_{D_{base}}$$는 기저항력계수, $$C_{D_{misc}}$$는 기타 항력계수, $$S_{ref}$$는 항공기의 기준 면적, $$S_{wet}$$는 항공기 구성품의 표피 면적 (Wetted area) 이며 아래 첨자 c는 구성 요소(Component)들을 의미한다. 

### 1. 마찰계수(Skin Friction coeffient)

$$
C_{f} = \frac{0.455}{(\log_{10}Re_{L})^{2.58}(1+0.144M^{2})^{0.65}}
$$

여기서 레이놀즈 수 $$Re_{L}$$ 는 아래와 같다. 

$$
Re_{L}=Re \cdot \bar{L} \cdot M
$$

이때 고도 1ft 당, 마하수 M=1에 대한 레이놀즈 수 Re는 다음과 같다. 

$$
Re = 10^{6}\exp\left[\ln(7.1)-(h/1000)^{\frac{1.1}{4.6}}\right],~0<h\le 36,000\text{ft}\\
Re = 10^{6}\exp\left[\ln(2.3168)-(h/1000-36)^{\frac{0.99}{19.97} }\right],~h>36,000\text{ft}
$$

그리고 $$\bar{L}$$ 는 면적 평균 특성 길이(Area Weighted Characteristic Length)로 아래와 같이 정의된다. 

$$
\bar{L} = \frac{\Sigma(l_{c} \cdot S_{wetc})}{\Sigma S_{wetc}}
$$

여기서 $$l_{c}$$는 구성품의 특성길이이고 $$S_{wet}$$는 구성품의 표피 면적(Wetted Area) 그리고 아래 첨자 c는 구성 요소(Component)들을 의미한다.

### 2. 형상계수(Form Factor)

2-1. 단면이 에어포일 형태인 날개, 꼬리날개, 스트러트 또는 파이런 등과 같이 유선형 물체에 대한 형상계수

$$
FF = \left[ 1+ \frac{0.6}{(x/c)_{tmax}(t/c)+100(t/c)^{4}} \right] \left[ 1.34M^{0.18}(\cos\Lambda_{m})^{0.28}\right]
$$

여기서 $$(x/c)_{tmax}$$ 는 에어포일의 최대 두께 위치이다. 저속형 에어포일의 경우에 일반적으로 $$(x/c)_{tmax} \approx 0.3$$ 이고 고속형 에어포일의 경우에 $$(x/c)_{tmax} \approx 0.5$$ 정도이다. $$\Lambda_{m}$$은 최대 두께 선의 후퇴각이다. 힌지로 연결된 Rudder와 Elevator가 있는 꼬리날개의 경우 꼬리날개면과 조종면 사이의 틈새로 인해 계산한 형상계수에서 10%정도가 더 추가된다.

2-2. 동체와 유선형 캐노피에 대한 형상계수

$$
FF = 1+ \frac{60}{f^{3}}+\frac{f}{400}
$$

여기서 세장비(sharpness) f는 다음과 같다. 

$$
f=\frac{l}{d}=\frac{l}{\sqrt{(4/\pi)\cdot A_{max}}}
$$

여기서 $$l$$은 물체의 특성길이이고, $$d$$는 구성 요소의 지름으로 단면이 원이 아닌 경우에는 단면의 최대 넓이 $$A_{max}$$를 이용해서 구한다. 

2-3. 나셀 또는 유선형 외부 장착물에 대한 형상계수 

$$
FF = 1 + \frac{0.35}{f}
$$

2-4. 기관 흡입구와 동체 사이의 경계층 분리기에 대한 형상 계수 

$$
FF = 1+(d/l) \text{ for double wedge type}\\
FF = 1+(2d/l) \text{ for single wedge type}
$$

### 3. 간섭계수(Interference Factor)

| 구성요소  || 간섭계수 $$Q_{c}$$ | 
|:---------|:-----------------:|:-----------------:|
정형되지 않은(unfilleted) 저익기 <br> 고익, 중익 및 정형된 저익기 || 1.1~1.4 <br> 1.0 | 
수직꼬리날개<br> 수평꼬리날개 <br> V-형 꼬리날개 || 1.03 <br> 1.08 <br> 1.04 ~ 1.05 <br> |
나셀 등 <br> 외부 장착물 | 직접 부착된 경우 <br> 장착거리가 지름보다 작을 경우 <br> 장착더리가 지름보다 클 경우 <br> 날개 끝 장착 | 1.5<br> 1.3<br> 1.0<br> 1.25<br>|

### 4. 기저항력계수(Base Drag)

기저항력은 물체 뒤쪽에서 단면적의 급격한 감소 또는 불연속에의한 유동 분리 현상으로 발생되는 압력저항이다. 기저항력은 아음속에서 일정하게 유지되다가 천음속 영역에서 서서히 증가하고 다시 M=1.0 ~ 1.8 구간에서는 상대적으로 일정한 값을 가지며 M=1.8 이상에서는 서서히 감소한다. 

$$
C_{D_{base}} = (0.1+0.1222M^{8})\frac{A_{base}}{S_{ref}} \text{ for } M \le 1\\
~~~~~~~~~~~~~~~C_{D_{base}} = 0.2222\frac{A_{base}}{S_{ref}} ~~~~~~~~~~~~~~~~\text{ for } 1.0<M\le1.8\\
C_{D_{base}} = 1.42\frac{A_{base}}{S_{ref}}/(3.15+M^{2}) ~~\text{ for } M\ge1.8
$$

여기서 $$A_{base}$$는 물체 뒤에 급격한 단면 변화 부분의 투영 단면적이다. 

### 5. 조파항력계수(Wave Drag)

조파항력은 초음속영역에서 항공기 주변의 충격파에 의해서 발생하는 일종의 압력 손실이다. 

일반적인 항공기의 경우에 Sears-Haack body 의 면적 분포를 가지고 있다.

$$
\frac{r}{r_{max}} = \left[ 1-\left(\frac{x}{l/2} \right)^{2} \right]^{0.75}
$$

여기서 $$r$$은 단면 반지름(the cross-section radius)이고 $$l$$은 물체의 전체 길이(longitudimal dimension)이다. 변수 $$x$$는 $$-l/2\le x \le l/2$$ 이다. 

Sears-Haack body 분포를 따르는 항공기의 경우에 조파항력은 아래와 같다. 

$$
C_{D_{wave}} = \frac{1.5 \pi}{S} \left( \frac{A_{max}}{l} \right)^{2}
$$

또한 마하수가 1.2 이상($$M>1.2$$)인 경우의 조파항력은 다음과 같다. 

$$
C_{D_{wave}}=\frac{4.5\pi}{S_{ref}}\left( \frac{A_{max}}{l} \right)^{2}E_{WD}(0.74+0.37\cos\Lambda_{L.E.})\left[1-0.3\sqrt{M-M_{C_{D0_{max}}}} \right]
$$

여기서 $$S_{ref}$$는 항공기 기준 면적, A_{max}는 물체의 최대 단면적 그리고 $$E_{WD}$$는 경험적 조파항력계수(Sears-Haack body)와 실제 면적 분포의 경우에 대한 비로 완전한 Sears-Haack body는 $$E_{WD}=1.0$$, 부드러운 면적분포를 갖는 항공기의 경우에 $$E_{WD}=1.2$$, 일반적인 초음속 항공기의 경우 $$E_{WD}=1.4\~2.0$$, 울퉁불퉁한 면적분포를 갖는 초음속 항공기의 경우에 $$E_{WD}=2.0\~3.0$$이다. 조파항력 최대 마하수 $$M_{C_{D0_{max}}}$$는 아래와 같다. 

$$
M_{C_{D0_{max}}}=\frac{1}{\cos^{2}\Lambda_{L.E.}}
$$

### 6. 기타항력계수(Miscellaneous Drag)

6-1. 착륙장치항력(Landing Gear Drag)

$$
C_{Dlanding-gear}=\sum_{c} C_{DL_{c}} \cdot \frac{A_{landing-gear,c}}{S_{ref}}
$$

여기서 $$A_{landing-gear,c}$$는 착륙장치 부품의 전면 면적이고 착륙장치 항력계수 $$C_{DL_{c}}$$는 아래 표와 같다.

|  | 착륙장치 항력계수($$C_{DL_{c}}$$) | 
|:---------|:-----------------:|
|Regular wheel and tire          | 0.25|
|Second wheel and tire in tandom | 0.15|
|Streamlined wheel and tire      | 0.18|
|Wheel and tire with fairing     | 0.13|
|Streamline strut ($$1/6 < t/c < 1/3 $$)| 0.05|
|Round strut or wire             | 0.30|
|Flat spring gear leg            | 1.40|
|Fork, bogey, irregular fitting  | 1.0 ~ 1.4|

6-2. 스피드브레이크항력(Speed Brake Drag)

스피드브레이크에 의한 항력은 동체에 장착된 경우와 날개에 장착된 경우로 나뉜다. 

동체에 장착된 경우에 아래와 같이 계산한다. 

$$
C_{D_{speed-brake}}=1.0\times \frac{A_{speed-brake}}{S_{ref}}
$$

날개에 장착된 경우(0.6 chord 위치)에는 다음과 같이 계산한다. 

$$
C_{D_{speed-brake}}=1.6\times \frac{A_{speed-brake}}{S_{ref}}
$$

여기서 $$A_{speed-brake}$$는 스피드 브레이크 전면 면적이다. 

6-3. 플랩항력(Flap Drag)

플랩에 의한 항력은 다음의 식으로 계산한다. 

$$
C_{Dflap} = 0.0023 \frac{\text{flap span}}{\text{wing span}}\delta_{flap}
$$

6-4. 누출 및 거칠기 항력(Leakage and Protuberance Drag)

압력이 높은 부분에서 항공기 틈새나 구멍을 통해서 항공기 내부로 공기가 유입되어 생기는 운동량 손싱, 또는 항공기 내부에서 압력이 낮은 항공기 외부로 공기 분출이 일어나 유동 흐름을 분리시켜 발생하는 항력을 누출항력이라고 한다.  

또한 항공기의 안테나, 전조등, 항공기 표면의 리벳이나 표면 자체 거칠기 또는 항공기 표면을 구성하는 평판 등의 부적절한 결합과 돌기에 의한 항력을 거칠기항력이라고 한다. 

| 제트수송기 및 폭격기 | 2~5%| 
|:---------|:-----------------:|
|프로펠러항공기| 5~10%|
|현용전투기| 10~15%|
|신개념전투기| 5~10%|
|가변익항공기| 위의 값에 3% 추가|