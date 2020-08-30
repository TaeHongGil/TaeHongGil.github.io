---
layout: post
title: >
    Kruskal Algorithm
categories: [Algorism]
tags: [Algorism]
---


# Kruskal Algorithm

크루스칼 알고리즘은 가장 적은 비용으로 모든 노드를 연결하기 위해 사용하는 알고리즘입니다.  

최소 비용 신장 트리를 만들기 위한 대표적인 알고리즘이라고 할 수 있습니다.  

연결은 다음과 같은 순서로 진행 됩니다.

1. 모든 간선정보를 오름차순으로 정렬시킵니다.  

2. 정렬된 순서에 맞게 그래프에 포함시킵니다.  

3. 포함시키기 전에 다른노드와 연결 되어있는지 확인합니다.
<a href = "https://taehonggil.github.io/algorism/2020/08/30/union-find-algorism.html" style="color:red">**(Union-Find Algorithm)**<a>

4. 연결 되어있는 경우 간선을 포함하지 않습니다.  

5. 모든 노드가 연결될 때까지 2~4번의 순서를 반복합니다.

<br/>
<br/>

![img](/assets/img/kruskal/1.jpg)  

위와 같은 노드가 있을 때 간선정보를 오름차순으로 정렬시킵니다.

1, 2|1, 3|2, 3|3, 4|2, 4
1|2|3|4|5|

<br/>
<br/>

![img](/assets/img/kruskal/2.jpg)  

1, 2|1, 3|2, 3|3, 4|2, 4
1|2|3|4|5|

<br/>

![img](/assets/img/kruskal/3.jpg)  

연결되지 않은 노드를 연결합니다.  

1, 3|2, 3|3, 4|2, 4
2|3|4|5|

연결된 노드를 나타내는 테이블입니다.

1|2|3|4
1|1|3|4

<br/>
<br/>

![img](/assets/img/kruskal/4.jpg)  

2, 3|3, 4|2, 4
3|4|5|

1|2|3|4
1|1|1|4

3노드는 이미 1,3이 연결 되어있기 때문에 연결하지 않습니다.

3, 4|2, 4
4|5|

<br/>
<br/>

![img](/assets/img/kruskal/5.jpg)

|2, 4|
|5|

1|2|3|4
1|1|1|1

<br/>
<br/>

모든 노드가 연결되어 있기 때문에 종료합니다.

따라서 전체 노드를 연결하는 비용은 1 + 2 + 4 = 7 입니다.