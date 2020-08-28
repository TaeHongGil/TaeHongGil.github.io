---
layout: post
title: >
    git블로그 Markdown 문법 
categories: [git]
tags: [git, 블로그, markdown]
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
<br/>
<br/>

## 코드 블럭

    ```언어 ex) python, js, java, c, ... 언어를 입력하지않으면 그대로
    print(hello world)
    ```  

```python
print("hello world")
```

vscode를 사용 중인데 각자의 설정에 따라 글자색이 바뀌는 듯 합니다

<br/>
<br/>
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
    예) “#Test! 테스트” -> “#Test–테스트”  

[구글](https://google.com "마우스를 올려놓으면 말풍선이 나옵니다.")  
<https://google.com>  
[문단 이동](##제목-및-본문-작성)  

<br/>
<br/>
<br/>
<br/>