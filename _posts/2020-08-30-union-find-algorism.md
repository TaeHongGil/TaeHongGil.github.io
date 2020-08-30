---
layout: post
title: >
    Union Find Algorism
categories: [Algorism]
tags: [Algorism]
---


# Union-Find

대표적 그래프 알고리즘으로 '합집합 찾기'라는 의미를 가지고 있습니다.  

상호 배타적 집합(Disjoint-set)이라고도 합니다.  

여러 노드가 존재할 때, 두 개의 노드를 선택해서, 현재 두 노드가 서로 같은 그래프에 속하는지 판별하는 알고리즘입니다.  

![img](/assets/img/union-find/1.jpg)  

위와 같이 노드가 연결되어 있다면 아래와 같이 표현됩니다.  

![img](/assets/img/union-find/2.jpg)  

이와 같이 부모를 합칠 때는 일반적으로 더 작은 값 쪽으로 합칩니다. 이것을 합침(Union) 과정이라고 말할 수 있습니다.  

![img](/assets/img/union-find/3.jpg)  

또 위와 같이 하나 이상의 노드가 연결되어 있을 때는

![img](/assets/img/union-find/4.jpg)  
![img](/assets/img/union-find/5.jpg)

한번에 부모노드를 알 수 없기 때문에 재귀함수를 거쳐 표현됩니다. 

이 때 노드 1, 2, 3의 부모가 모두 1이기 때문에 이 세 가지 노드는 모두 같은 그래프에 속한다고 할 수 있습니다.  

Find 알고리즘은 두 개의 노드의 부모 노드를 확인하여 현재 같은 집합에 속하는지 확인하는 알고리즘입니다.  
