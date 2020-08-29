---
layout: post
title: >
    git블로그 Markdown 문법 
categories: [Git]
tags: [git, blog, jekyll]
sitemap :
  changefreq : daily
  priority : 1.0
---

## 제목 및 본문 작성

    #Test 제목 1
    ##Test 제목 2
    ###Test 제목 3
    Test 본문

# Test
## Test
### Test
Test

<br/>
<br/>

## 코드 블럭

    ```언어 ex) python, js, java, c, ... 언어를 입력하지않으면 그대로
    print(hello world)
    ```  

```python
print("hello world")
```

<br/>
<br/>

## 링크
    유형1(`설명어`를 클릭하면 URL로 이동) : [구글](https://google.com "마우스를 올려놓으면 말풍선이 나옵니다.")  
    유형2(URL 보여주고 `자동연결`) : <https://google.com>  
    유형3(동일 파일 내 `문단 이동`) : [문단 이동](##제목-및-본문-작성)
    
    문단 매칭방법 : 제목(header)를 복사 붙여넣기 후,
    1) 특수문자제거
    2) 스페이스를 갯수만큼 -로 변경
    3) 대문자->소문자로 변경
    4) 영문만 가능
    예) “#Test! 테스트” -> “#test–테스트”  

[구글](https://google.com "마우스를 올려놓으면 말풍선이 나옵니다.")  
<https://google.com>  
[문단 이동](#test)  

<br/>
<br/>

## 단어 강조
    **두껍게** / __두껍게__
    *이텔릭체* / _이텔릭체_
    ~~취소선~~
    <u>밑줄</u>

**두껍게** / __두껍게__  
*이텔릭체* / _이텔릭체_  
~~취소선~~  
<u>밑줄</u>  

<br/>
<br/>

## 개행
    문장 끝에 "  " (스페이스 두번)
    <br/>  (여러줄개행)

<br/>
<br/>

## 리스트
    1. 순서
    2. 순서
        - 순서(서브) 
        - 순서(서브) 
    4. 순서
        1. 순서(서브)
        2. 순서(서브)
    3. 순서

    입력한 숫자와 관계없이 순서대로 

    - 순서에 사용 가능한 기호
        - 대쉬(hyphen)
        * 별표(asterisks)
        + 더하기(plus sign)

1. 순서
2. 순서
    - 순서(서브) 
    - 순서(서브) 
4. 순서
    1. 순서(서브)
    2. 순서(서브)
3. 순서

- 서브에 사용 가능한 기호
    - 대쉬(hyphen)
    * 별표(asterisks)
    + 더하기(plus sign)

<br/>
<br/>

## 이미지 / 이미지 링크
    ![img](/assets/img/triangle.png)
    [![img](/assets/img/triangle.png)](https://google.com)
    위의 두가지 문법은 이미지크기 조정 X
    <img src = "/assets/img/triangle.png" width="40%">
    <a href = "https://google.com"><img src = "/assets/img/triangle.png" width="40%"></a>

<img src = "/assets/img/triangle.png" width="40%">     
<a href = "https://google.com"><img src = "/assets/img/triangle.png" width="40%"></a>

<br/>
<br/>

## 표
    값 | 의미 | 기본값
    ---|:---:|---:
    1 | 일| 1
    2 | 이| 2
    3 | 삼| 3

값 | 의미 | 기본값
---|:---:|---:
1 | 일| 1
2 | 이| 2
3 | 삼| 3

## 그 외
    >인용문
    >>인용문
    >>>인용문
    ---구분선
    ***구분선
    ___구분선
 
>인용문
>>인용문
>>>인용문

---

***

___