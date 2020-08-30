---
layout: post
title: >
    DFS / BFS algorism (DP)
categories: [Algorism]
tags: [Algorism]
---


# Depth-First Search (DFS)

DFS(깊이 우선 탐색)은 Root Node 혹은 다른 임의의 Node에서 다음 분기(Branch)로 넘어가기 전에 해당 분기를 완벽하게 탐색하는 방법이다.

Stack 혹은 재귀함수(Recursion)으로 구현된다.

* 경로를 탐색할 때 한 방향으로 갈 수 있을 때까지 계속 가다가 더 이상 갈 수 없게되면 다른 방향으로 다시 탐색을 진행  

![img](/assets/img/dfs-bfs/1.gif)  

<br/>
<br/>

## Breadth First Search (BFS)

BFS(너비 우선 탐색)은 Root Node 혹은 다른 임의의 노드에서 인접한 노드를 먼저 탐색하는 방법이다.

Queue를 사용해서 구현한다.

![img](/assets/img/dfs-bfs/2.gif)  