---
layout: post
title: >
    Algorism 풀이 시 유용한 Python 함수
categories: [Python]
tags: [Python, Algorism]
---

## 순열 조합
```python
from itertools import permutations,combinations
```

<br/>
<br/>

## 에라토스테네스의 체 (소수 구하기)
```python
prime=[True]*(int(max))
m=int(max)**0.5) #최대약수
for i in range(2, m + 1):
    if prime[i] == True:  # i가 소수인 경우
        for j in range(i + i, (max), i):  # i이후 i의 배수들을 False 판정
            prime[j] = False
```
max+1크기의 True 배열을 만들고 소수의 배수번째 배열을 False로 만드는 방법.

<br/>
<br/>

## map(함수,리스트)

리스트 값에 함수를 적용.  
```python
li = [1, 2, 3]
result = list(map(lambda i: i ** 2 , li))
```

result = [1, 4, 9]

<br/>
<br/>

## 힙정렬

완전 이진 트리의 일종으로 우선순위 큐를 위하여 만들어진 자료구조
최댓값, 최솟값을 쉽게 추출할 수 있는 자료구조

![img](/assets/img/python-algorism/1.png)  
```python
import heapq
```

<br/>
<br/>

## set (집합 자료형)

list(set(asd)) > asd리스트의 중복제거  
s1 & s2 교집합  
s1 | s2  합집합  
s1 - s2 차집합  

<br/>
<br/>

## enumerate
```python
for i, v in enumerate("Hello World"):
	print("index : {}, value: {}".format(i,v)) #인덱스번호와 값 출력
```
    index : 0, value: H		
    index : 1, value: e
    index : 2, value: l
    index : 3, value: l
    index : 4, value: o
    index : 5, value:  
    ...

<br/>
<br/>

## Counter
```python
from collections import Counter
lst = ['aa', 'cc', 'dd', 'aa', 'bb', 'ee']
print(collections.Counter(lst))
```
    출력문
    Counter({'aa': 2, 'cc': 1, 'dd': 1, 'bb': 1, 'ee': 1})

인자의 갯수를 세서 딕셔너리로 만들어 주는 함수.

<br/>
<br/>

## redusce
```python
from functools import reduce
reduce(lambda x, y: x + list, [0, 1, 2, 3, 4],0)
```
    from functools import reduce
    reduce(lambda x, y: x + list, [list],x값)
    x의 값에 list의 값을 순서대로 더한다.

<br/>
<br/>

## filter
```python
filter(lambda x: x < 5, range(10)) # [0, 1, 2, 3, 4]  
```

<br/>
<br/>

## split
```python
split(sep)
```
문자열을 sep으로 잘라서 리스트에 넣는다.
+maxsplit옵션

<br/>
<br/>

## 정규식
```python
import re
```
    \d - 숫자와 매치, [0-9]와 동일한 표현식이다.
    \D - 숫자가 아닌 것과 매치, [^0-9]와 동일한 표현식이다.
    \s - whitespace 문자와 매치, [ \t\n\r\f\v]와 동일한 표현식이다. 맨 앞의 빈 칸은 공백문자(space)를 의미한다.
    \S - whitespace 문자가 아닌 것과 매치, [^ \t\n\r\f\v]와 동일한 표현식이다.
    \w - 문자+숫자(alphanumeric)와 매치, [a-zA-Z0-9_]와 동일한 표현식이다.
    \W - 문자+숫자(alphanumeric)가 아닌 문자와 매치, [^a-zA-Z0-9_]와 동일한 표현식이다.
    
#### match Object
match(pattern, string)	문자열의 처음부터 정규식과 매치되는지 조사한다.  
search(pattern, string)	문자열 전체를 검색하여 정규식과 매치되는지 조사한다.  
findall(pattern, string)	정규식과 매치되는 모든 문자열(substring)을 리스트로 돌려준다.  
finditer(pattern, string)	정규식과 매치되는 모든 문자열(substring)을 반복 가능한 객체로 돌려준다.  

#### match Object의 메서드들  
group()	일치된 문자열을 반환한다.  
start()	일치된 문자열의 시작 위치를 반환한다.  
end()	일치된 문자열의 끝 위치를 반환한다.  
span()	일치된 문자열의 (시작 위치, 끝 위치) 튜플을 반환한다.  

<br/>
<br/>

## format
```python
format(42, 'b') #'101010'
format(42, 'o') #'52'
format(42, 'x') #'2a'
format(42, 'X') #'2A'
format(42, 'd') #'42'
```

<br/>
<br/>

## math
```python
import math
math.gcd(a,b) #a,b의 최대공약수
math.lcm(a,b) #a,b의 최소공배수
math.sqrt(a) #a의 제곱근
```

<br/>
<br/>

## alphabet list만들기
```python
import string
list(string.ascii_uppercase) #대문자알파벳리스트
list(string.ascii_lowercase) #소문자알파벳리스트
```

<br/>
<br/>

## 기타
```python
list(zip(*arr2))  #행>열 변환  
eval("100+200")  #문자열수식계산  
abs(-1)>  #절댓값  
s.title()  #주어진 문자열에서 알파벳 외의 문자(숫자, 특수기호, 띄어쓰기 등)로 나누어져 있는 영단어들의 첫 글자를 모두 대문자로 변환시킨다.  
s.capitalize()  #주어진 문자열에서 맨 첫 글자를 대문자로 변환시킨다.
```