---
layout: post
title: class macro
img: "assets/img/portfolio/classmacro.png"
date: 09, 03 2020
tags: [portfolio]
---

![image]({{ page.img | relative_url }})

## 설명
Python의 tkinter패키지와 selenium패키지를 이용한 간단한 수강신청 매크로입니다.

실행순서는 다음과 같습니다.

1. id와 password를 입력받고 수강과목의 과목번호/반번호를 입력받습니다.  

2. 실행버튼을 누르면 수강신청사이트로 이동후 입력받은 id와 password로 로그인됩니다.  

3. 수강신청탭으로 이동 후 입력받은 과목번호와 반번호를 이용하여 수강신청합니다.  

<br/>
<br/>

## 실행영상 
<iframe width="640" height="360" src=" " frameborder="0" gesture="media" allowfullscreen=""></iframe>

<br/>
<br/>

## 구현하기 어려웠던 점

처음 element를 불러올 때 frame에 관계없이 불러왔었는데 element를 찾지 못했습니다.

알아보니 switch_to_frame()함수를 통해 frame을 스위치해야만 정상적으로 element를 불러올 수 있었습니다.
