---
layout: post
title: ft_server
img: "assets/img/portfolio/ft_server.PNG"
date: 12, 15 2020
tags: [portfolio]
---

![image]({{ page.img | relative_url }})

## 설명

ft_server

dockerfile, shell file 을 사용하여 서버를 자동으로 구축

    os : debian buster
    nginx, mariadb, php-mysql, wordpress 사용

각각의 설정 파일을 저장하여 shell file과 함께 컨테이너에 올리고 컨테이너에서 shell file을 실행

<br/>
<br/>

## 실행영상 
<iframe width="640" height="360" src="https://www.youtube.com/embed/htHpQg9rbk0" frameborder="0" gesture="media" allowfullscreen=""></iframe>


<br/>
<br/>

## 구현하기 어려웠던 점

db설정을 할 때 shell file에서 처음부터 admin의 id를 바꾸어 설정하고 싶었는데

그렇게 되지않아 id와 권한을 추가하여 구현하였습니다.