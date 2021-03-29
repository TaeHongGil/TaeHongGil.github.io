---
layout: post
title: Slot Machine
img: "assets/img/portfolio/slotmachine.PNG"
date: 03, 28 2021
tags: [portfolio]
---

![image]({{ page.img | relative_url }})

## 설명

cocos2d-x 3.1 엔진으로 구현했습니다.

각각의 라인이 랜덤한 속도로 돌아갑니다.

가중치를 사용하여 그림의 확률을 조절 할 수 있게 하였습니다.

배팅금액을 설정할 수 있습니다.

배팅은 가진 코인을 초과하여 배팅 할 수 없습니다.

1원 미만의 금액을 배팅할 수 없습니다.

스핀 후 코인이 배팅보다 낮다면 배팅은 1이 됩니다.

슬롯이 돌아가는 동안은 스핀, 배팅 버튼을 사용 할 수 없습니다.

라인의 수를 늘려도 정상 작동합니다. (배경이미지 및 슬롯의 위치 조정 필요)

코인이 0이되면 game over 됩니다.

                                RTP
    체리   	50% > 12.5  *  3    37.5%
    바나나  40% > 6.4   *  5    25.6%
    수박   	30% > 2.7%  *  8    21.6%
    다이아  20% > 0.8%  *  15   12% 
    잭팟   	10% > 0.1%  *  50   5%
                                101.7%

환수율은 100%을 넘기도록 설정하였습니다.

<br/>
<br/>

## 실행영상 
<iframe width="640" height="360" src="https://www.youtube.com/embed/VdgkVyaskpo" frameborder="0" gesture="media" allowfullscreen=""></iframe>

테스트는 체리의 확률를 90%로 하여 진행하였습니다.
<br/>
<br/>

## 구현하기 어려웠던 점

로직을 짜는 부분은 어렵지 않았으나 객체지향의 구조를 짜는부분이 어려웠다. 

CALLBACK 0, 1함수의 활용도가 떨어지는 것 같다. 클래스를 넘기는 부분에서 에러가 발생
