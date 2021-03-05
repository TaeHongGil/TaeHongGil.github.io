---
layout: post
title: get_next_line
img: "assets/img/portfolio/gnl.PNG"
date: 12, 15 2020
tags: [portfolio]
---

![image]({{ page.img | relative_url }})

## 설명

get_next_line

open, read 함수를 사용하여 파일을 읽습니다.

파일을 읽을 때 설정된 buffer size만큼 불러들입니다. (1~1000만)

파일을 읽는 도중 개행문자가 나타나면 개행문자 전까지 한줄을 출력합니다. (저장된 문자열에 개행문자가 여러개 있어도 한줄만 출력)

여러개의 파일을 동시에 읽을 수 있어야 합니다.


계속해서 여러번 읽어야 하기 때문에 정적변수를 사용했습니다.


<br/>
<br/>

## 실행영상 
<iframe width="640" height="360" src="https://www.youtube.com/embed/6rgXJxpbE6g" frameborder="0" gesture="media" allowfullscreen=""></iframe>


<br/>
<br/>

## 구현하기 어려웠던 점

처음 이중포인터를 사용하여 구현했을 때 이해가 가지않는 부분이 있었으나 동료들에게 물어보고 검색해서 찾아보며 이해하고 구현함