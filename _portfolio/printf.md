---
layout: post
title: printf
img: "assets/img/portfolio/printf.PNG"
date: 01, 15 2021
tags: [portfolio]
---

![image]({{ page.img | relative_url }})

## 설명

c의
printf를 구현했습니다.

    구현한 플래그,정밀도,폭
    -0.*

    - 지정한 필드 너비 내에서 결과를 왼쪽에 맞춰 표시합니다.	
    
    0 Width 에 접두사가 붙는 경우 0 최소 너비에 도달할 때까지 선행 0이 추가 됩니다. 0 및가 모두 - 나타나면는 0 무시 됩니다. 
      0 정수 형식 ( i ,,,,,)에 대해를 지정 u x X o d 하 고 전체 자릿수 지정도 제공 하는 경우 (예:)은 %04.d 0 무시 됩니다.
      0 또는 부동 소수점 형식에 대해를 지정 하면 a A 또는 접두사 뒤에가 수의 앞에 오는 0이 앞에 붙습니다 0x 0X .	

    . 형식 문자열에서 정밀도를 나타내지는 않지만 뒤에 인자로 정밀도 값을 줍니다. 이 때 인자는 형식 태그가 적용되는 데이타 앞에 있어야 합니다.

    * 폭을 형식 문자열에 지정해서 받지 않지만, 그 대신에 형식 문자열 뒤에 오는 인자들에 넣어서 받습니다.
      이 때, 이는 정수 값이여야 하며 폭을 지정하는 변수 뒤에 출력할 데이터가 위치합니다.

    구현한 형식필드 문자
    cspdiuxX%

    c 문자
    s 문자열
    p 16진수 주소
    d 부호 있는 10진수
    i 부호 있는 10진수
    u 부호 없는 10진수
    x 부호 없는 16 진수 정수 " abcdef "를 사용 합니다.
    X 부호 없는 16 진수 정수 " ABCDEF "를 사용 합니다.
    % %기호

<br/>
<br/>

## 실행영상 
<iframe width="640" height="360" src="https://www.youtube.com/embed/SsAQwVXiXfk" frameborder="0" gesture="media" allowfullscreen=""></iframe>

test 프로그램을 사용하여 검사하였습니다.

<br/>
<br/>

## 구현하기 어려웠던 점

문자형식마다 플래그에 따른 구현이 달라지기 때문에 그 부분에 맞추어 구현하는 것이 어려웠습니다.

음수와 양수를 나누어서 구현하여 해결하였습니다.