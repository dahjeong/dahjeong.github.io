---
layout: post
title: Aircraft Design <br> 추진 계통 설계 <br>
author: "Dajung Kim"
comments: true
---

설계 항공기의 순항 비행 마하수, 고도, 필요 추력, 엔진 종류와 갯수, 해면 정지 추력(SLST, $$T_{SL}$$), 바이패스비(BPR), 비연료 소모율(SFC), 기관 무게(W), 기관 길이(L), 기관(팬) 지름(D)이 주어짐

(1) 분사 추진 계통 설계 예


표준 대기표에서 순항고도에서 압력비, 온도비를 찾고 추력식에 대입한다.
$$T_{H}=T_{SL}\frac{P_{H}}{P_{SL}}\frac{\theta_{SL}}{\theta_{H}}$$

순항비행시 추력은 최대이륙 추력의 80%
$$T_{ref}=0.8 * T_{H} $$

마하수가 1보다 적으면 램효과에 의한 추력 증가를 고려하지 않는다.

기관당 필요추력은 
$$T_{ref_{engine}}=T_{ref}/n$$

스케일 계수(scale factor, SF)는 설계 항공기의 필요추력과 표준 기관의 추력의 비이다.
$$SF = T_{ref_{engine}}/T_{actual}\\
T_{SL} = T_{SL_{actual}}(SF)\\
L=L_{actual}(SF)^{0.4}\\
D=D_{actual}(SF)^{0.5}\\
W=W_{actual}(SF)^{1.1}$$

이륙 거리 산정을 위해 필요한 전체 이륙 추력은
$$T_{take-off}=T_{SL}*(Number of Engines)$$


후연소기가 없는 아음속 항공기 기관($$0 \geq BPR \geq 6.0$$)
$$W=0.084T^{1.1} \exp^{(-0.045BPR)}\\
L=2.22T^{0.4}M^{0.2}\\
D=0.3937T^{0.5} \exp^{(0.04BPR)}\\
SFC_{maxT}=0.67 \exp^{(-0.12BPR)}\\
T_{cruise}=0.60T^{0.9} \exp^{(0.02BPR)}\\
SFC_{cruise}=0.88 \exp^{(-0.05BPR)}$$


후연소기가 있는 초음속 전투기 및 폭격기($$1 \geq M \geq 2.5$$, $$0 \geq BPR \geq 1.0$$)
$$ W = 0.063 T^{1.1} M^{0.25} \exp^{(-0.81BPR)}\\
L = 3.06 T^{0.4} M^{0.2}\\
D = 0.288 T^{0.5} \exp^{(0.04 BPR)}\\
SFC_{maxT} = 2.1 \exp^{(-0.12 BPR)}\\
T_{cruise} = 1.6T^{0.74} \exp^{(0.023 BPR)}\\
SFC_{cruise} = 1.04 \exp^{(-0.186 BPR)} $$
