---
layout: post
title: >
    Dynamic Programming algorism (DP)
categories: [Algorism]
tags: [Algorism]
---


# Dynamic Programming

DP(동적 계획법)는 복잡한 문제를 간단한 여러 개의 문제로 나누어 푸는 방법을 말한다.  

DP의 원리는 일반적으로 주어진 문제를 풀기 위해서, 문제를 여러 개의 하위 문제로 나누어 푼 다음,  
그것을 결합하여 최종적인 목적에 도달하는 것이다.  

대표적인 예로 피보나치 수열이 있다.  

<br/>
<br/>

## 피보나치 수열


![img](/assets/img/dp/1.png)  


```python
int fibo(int x):
    if(x <= 2):
        return 1
    return fibo(x-1) + fibo(x-2)
```

위의 함수에서 x=5 일때  

```python
fibo(1)
fibo(2)
fibo(1) + fibo(2)
fibo(2) + (fibo(1) + fibo(2))  
(fibo(1) + fibo(2)) + (fibo(2) + (fibo(1) + fibo(2)))  
```

위와 같이 재귀함수가 실행된다.  

매번 계산했던 값을 다시 계산하게 되는데  

이 때 효율을 높이기 위한 방법으로  

DP의 핵심 기술인 **memoization(메모이제이션)**이 있다.  

<br/>
<br/>

## memoization(메모이제이션)

다음은 fibo함수의 효율을 높인 코드이다.  

```python
int f = [0] * 100

int fibo(int x):
    if(x <= 2):
        return 1

    if(f[x] != 0):
        return f[x]

    else:
        f[x] = fibo(x-1) + fibo(x-2)
        return f[x]
```

x = 5 일 때 위의 코드는 아래와 같이 실행된다.  

    f[1] = fibo(1)
    f[2] = fibo(2)
    f[3] = f[1] + f[2] = fibo(3)
    f[4] = f[2] + f[3] = fibo(4)
    f[5] = f[3] + f[4] = fibo(5)

이렇게 주어진 입력값에 대한 결과를 저장함으로써 같은 입력값에 대해 함수가 한 번만 실행되게 하는 것을  

**memoization**이라고 한다.