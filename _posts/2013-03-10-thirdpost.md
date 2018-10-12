---
layout: post_page
title: Breguet range equation
comment: true
---

Breguet range equation은 비행기가 얼마나 멀리 날 수 있는가를 나타내는 방정식이다.

W의 무게를 갖는 비행기가 steady, level flight 중 이라고 생각해 보자. 총 무게의 변화는 연료의 변화와 같다. 

$$
\frac{dW}{dt} = g\dot{m}_f = \frac{T}{I_{sp}}
$$

$$$W$$$:  비행기 총 중량<br/>
$$$t$$$: 시간<br/>
$$$g$$$: 중력가속도<br/>
$$$\dot{m}_f$$$ :연료변화량<br/>
$$$T$$$: 추력<br/>
$$$I_{sp}$$$ : efficiency 

For steady, level flight 에서는 $T = D$, $L = W$, or

$$\displaystyle W=L=D\left(\frac{L}{D}\right)=T\left(\frac{L}{D}\right)$$

따라서, 항공기 총 무게의 변화량은

$$
\displaystyle \frac{dW}{dt} =-\frac{W}{(L/D)I_{sp}}
$$

$$$L/D$$$ and $$$I_{sp}$$$ 이 flight path를 따라 constant 라고 가정하면:

$$
\displaystyle \frac{dW}{W} = -\frac{dt}{(L/D)I_{sp}}
$$

적분하면 

$$
\displaystyle \ln\left(\frac{W}{W_i}\right)=-\frac{t}{(L/D)I_{sp}}
$$

$$$W_i$$$ : 비행 초기 항공기 무게<br>
$$$W_f$$$ : 비행 종료 시 항공기 무게<br> 

비행 초기 및 종료 시간에 따라 적분하면 

$$
\displaystyle \frac{L}{D}I_{sp} \ln\left(\frac{W_i}{W_f}\right)=t_f
$$

$$$t_\textrm{initial}$$$ : 비행 시작 시간, $$$t_\textrm{initial}=0$$$<br>
$$$t_f$$$ : 비행 종료 시간

비행 영역(Flight Range)은 항공기 속도($V$)와 시간($t$)의 곱이므로 

$$
Range  = V t_f = V \times \frac{L}{D} \times I_{sp} \times \ln \left(\frac{W_i}{W_f}\right)
$$


   {% if page.comments != false %}
   {% include disqus_comments.html %}
   {% endif %}