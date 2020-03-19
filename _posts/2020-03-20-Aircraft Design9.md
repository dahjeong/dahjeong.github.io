---
layout: post
title: Aircraft Design <br> 트림 항력 (Trim Drag) <br>
author: "Dajung Kim"
comments: true
---

비행 중 항공기의 자세 평형을 유지하기 위해서 조종면 변위를 변화시키는 트리밍을 하기도 한다. 이때 조종면 변위에 의한 항력을 트림 항력이라고 한다. 

트림항력은 트림 조종면에 대한 형상항력(Profile Drag)과 유도항력(Induced Drag)의 합으로 나타낼 수 있다. 

$$
C_{D_{trim}} = \Delta C_{D_{trim_{profile}}} + \Delta C_{D_{trim_{induced}}}
$$

트림항력 중 유도항력 성분은 다음과 같이 구한다. 

$$
\Delta C_{D_{trim_{induced}}} = \sum \frac{(\Delta C_{L_{ctrl}})^{2}}{\pi \cdot A_{ctl} e_{ctl}} \cdot \frac{S_{ctl}}{S_{ref}}
$$

여기서 아래 첨자 $$ctl$$은 수평꼬리날개, 카나드, 등의 조종면을 나타내며, $$e_{ctl}$$은 수평꼬리 날개 또는 카나드의 경우 0.5로 하고 수평꼬리 날개가 T-tail인 경우 0.75로 한다. 양력 $$\Delta C_{L_{ctl}}$$ 은 수평꼬리날개 또는 카나드의 양력선 기울기 $$C_{L_{i_{h}}} $$, $$C_{L_{i_{c}}}$$와 붙임각 $$i_{h}$$, $$i_{c}$$, 조종면의 각 변위 $$\delta_{e}$$, $$\delta_{c}$$ 및 각 변위에 따른 양력 변화율 $$C_{L_{\delta_{e}}}$$, $$C_{L_{\delta_{c}}}$$의 함수로 다음과 같다. 

$$
\Delta C_{L_{ctl}} = C_{L_{i_{h}}} i_{h}+ C_{L_{\delta_{e}}} \delta_{e} + C_{L_{i_{c}}} i_{c} + C_{L_{\delta_{c}}} \delta_{c}
$$

트림항력 중 형상항력 성분은 다음과 같다.

$$
\Delta C_{D_{trim_{profile}}}=\Delta C_{DP_{\Lambda c/4=0}}\cos \Lambda_{c/4} \left( \frac{S_{ef}}{S_{h}} \right) \left( \frac{S_{h}}{S_{ref}} \right) +\Delta C_{DP_{\Lambda c/4=0}}\cos \Lambda_{c/4} \left( \frac{S_{cf}}{S_{c}} \right) \left( \frac{S_{c}}{S_{ref}} \right)
$$

여기서 $$S_{ef}$$, $$S_{cf}$$는 수평꼬리날개 또는 카나드의 조종면 면적, $$S_{h}, S_{c}는 전체 수평꼬리 날개 또는 카나드의 전체 면적이다. $$\Delta C_{DP}_{\Lambda c/4=0}$$ 는 후퇴각 $$Lambda_{c/4}=0^{\circ}$$ 인 수평꼬리날개 또는 카나드의 형상항력계수로 조종면을 평면 플랩으로 간주하는 경우 변위각에 따라 다음 그림으로부터 구할 수 있다. 
