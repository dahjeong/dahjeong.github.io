---
layout: post_page
title: Aircraft Design <br> 최대 양력 계수 추정 <br>
comment: true
---

1. 큰 가로세로비(High Aspect Ratio)
큰 가로세로비란, 주날개의 가로세로비가 기준 가로세로비 $$A_{Low}$$ 보다 큰 경우, $$A > A_{Low}$$ 를 말한다. 여기서 기준 가로세로비는 아래와 같다.  
$$
A_{Low} = \frac{3}{(C_{1}+1)\cos\Lambda_{LE}}
$$
여기서 $$\Lambda_{LE}$$는 이고, $$C_{1}$$은 테이퍼 비의 함수로 아래의 그림과 같다.

큰 가로세로비를 가지는 항공기의 최대양력 계수는 다음과 같다.
$$
C_{Lmax} = \left(\frac{C_{Lmax}}{C_{lmax}}\right)C_{lmax}+\Delta C_{L_{max}}
$$

여기서 $$C_{lmax}$$ 는 M=0.2일 때 에어포일의 최대양력계수이고 $$(C_{Lmax}/{C_{lmax})$$ 는 다음과 같다. 

$$
\left(\frac{C_{Lmax}}{C_{lmax}}\right) = A-B \cdot \Delta y'
$$
여기서 A, B와 $$\Delta y'$$ 은 $$\Lambda_{LE}$$를 이용해서 아래와 같이 구할 수 있다. 

$$
A=0.895+0.0028\Lambda_{LE}+6.57\times10^{-5}(\Lambda_{LE})^{2}
$$
$$
B=0.0011+0.0053\Lambda_{LE}+0.00011(\Lambda_{LE})^{2}
$$
$$
\Delta y'= 0: \Delta y <1.4\\
= \Delta y -1.4 : 1.4 \le \Delta y \le 2.5\\
= 1.1: \Delta y > 2.5
$$

여기서 $$\Delta y$$는 앞전 두께인자이며 아래의 표로 구한다. 

에어포일 계열  | $$\Delta y$$ | 
---|:---:|
4계열 | 26% of t/c | 
5계열 | 26% of t/c |
64계열 | 21.3% of t/c |
65계열 | 19.3% of t/c |
Biconvex | 11.8% of t/c |



위의 식에서 $$\Delta C_{Lmax}$$는 M=0.2 이상의 마하수에서의 양력 증가분이며 아래의 그림을 이용해서 구한다. 

최대 양력계수에서의 받음각 $$\alpha_{max}$$는 아래의 식으로 구한다. 

$$
\alpha_{max}=\frac{C_{Lmax}}{C_{L\alpha}}+\alpha_{L=0} + \Delta \alpha_{max}
$$

여기서 $$C_{Lmax}$$는 앞에서 구한 값을 사용한다. $$C_{L\alpha}$$ 도 이전 포스트의 양력계수 기울기에서 구한 값을 이용한다. $$\Delta \alpha_{max}$$ 는 $$\Lambda_{LE}$$ 와 앞전 두께인자 $$\Delta y$$, 아래 그림을 이용해서 구한다. 

1. 작은 가로세로비(Low Aspect Ratio)
작은 가로세로비란, 주날개의 가로세로비가 기준 가로세로비 $$A_{Low}$$ 보다 작은 경우, $$A <> A_{Low}$$ 를 말한다. 이때의 최대양력 계수는 다음과 같다. 

$$
C_{Lmax} = (C_{Lmax})_{base}+\Delta C_{Lmax}
$$


여기서 $$(C_{Lmax})_{base}$$는 아래의 그림을 이용하여 구한다. $$\beta = \sqrt{1-M^{2}}$$ 이다. 

그리고 $$\Delta C_{Lmax}$$ 는 마하수에 대한 최대 양력계수의 증가분이며 다음 그림을 이용해서 구한다. 

최대 양력계수에서의 받음각 $$\alpha_{max}$$는 다음과 같다.

$$
\alpha_{max} = (\alpha_{max})_{base} + \Delta \alpha_{max}
$$

여기서 $$(\alpha_{max})_{base}$$ 는 저속(M=0.2 부근)에서의 $$\alpha_{max}$$이고 아래의 그림을 이용하여 구한다. 


그리고 $$\Delta \alpha_{max}$$는 마하수 증가에 따른 보정 항이며 다음 그림을 이용해서 구한다.  

3. 
전체 항공기 최대 양력계수 $$C_{Lmax}$$는 다음과 같다.
$$
C_{Lmax} = (C_{Lmax})_{w} + (\Delta C_{Lmax})_{T}
$$
여기서 $$(\Delta C_{Lmax})_{T}$$는 꼬리날개에 의한 최대양력계수 증가분이다. 

$$
(\Delta C_{Lmax})_{T} = (C_{L\alpha})_{T} \cdot \sin\alpha_{max} \cdot \cos^{2}\alpha_{max}
$$

(C_{L\alpha})_{T}

   {% page.comments = true %}
   {% if page.comments != false %}
   {% include disqus_comments.html %}
   {% endif %}
