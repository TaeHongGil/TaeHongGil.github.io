---
layout: post
title: >
    git블로그 category 만드는 법
categories: [Git]
tags: [git, blog, jekyll]
---

<span style="color:red">**모든 테마가 같은 파일이름/코드를 사용하지 않습니다.**</span>
<br/> 
<span style="color:red">**비슷한 코드를 찾으시면 쉽게 하실수 있습니다**</span> 


## 1.category폴더 만들기  

![img](/assets/img/gitblog-category/1.png)  

category 폴더를 만든 뒤 category목록을 작성해줍니다.  

![img](/assets/img/gitblog-category/2.png)  

category목록안의 내용입니다. layout은 후에 작성합니다.

<br/>
<br/>

## 2.post에 categories추가

![img](/assets/img/gitblog-category/3.png)  

post에 categories를 추가해줍니다.  

이 categories를 가져오는 변수는 site.categories 입니다.  

<br/>
<br/>

## 3.home.html(index) 수정하기  

![img](/assets/img/gitblog-category/4.png)  

원하는 부분에 (저는 상단)  

```html
<ul>
    { % for category in site.categories % }
        <li><a href ="/category/{ {category | first} }">{ {category | first } }</a></li>
    { % endfor % }
</ul>
```

코드를 추가해줍니다.
<span style="color:red">**(중괄호 앞 뒤 띄워쓰기 제외)**</span>  

```html
<li>{ {category | first } }</li>
```

이 부분에서 site.categories를 category변수에 하나씩넣어 리스트를 출력합니다.  

category에는 여러 값이 들어가기때문에 first 를 사용하여 category명만 사용합니다.  

하이퍼링크는 category폴더 안에있는 선택(클릭)한 category를 불러옵니다.  
ex)Git클릭시 caregory/Git  

<br/>
<br/>

## 4.category layout 만들기

layout폴더에 category.html 파일을 만들어 준뒤 home.html파일의 내용을 복사합니다.  

![img](/assets/img/gitblog-category/5.png)  

보시면 이런식으로 post목록을 불러오는 코드가 있습니다.
<span style="color:red">**(다른 파일에 있을 수도 있습니다.)**</span>  

![img](/assets/img/gitblog-category/6.png)  

이렇게 수정해줍니다.  

{ % for post in site.categories[page.category] % }  

post마다 있는 categories를 비교하여 현재 선택(클릭한) 카테고리를 포함한 post 목록을 post(변수)에 저장합니다.  

<br/>
<br/>

## 5.css 수정
마지막으로 css를 수정하면

![img](/assets/img/gitblog-category/7.png)  

완성!