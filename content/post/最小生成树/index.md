---
title: "最小生成树"
date: 2026-06-15
description: "Kruskal 与 Prim 的核心思路、适用场景和实现细节。"
slug: "minimum-spanning-tree"
categories:
    - 算法
    - 图论
series:
    - 算法
seriesOrder: 1
---

最小生成树用于在一个连通无向带权图中，选择若干条边连接所有点，并让边权总和最小。

## Kruskal

Kruskal 按边权从小到大枚举边，用并查集判断当前边是否会形成环。

适合边比较少、容易排序边集的场景。

## Prim

Prim 从一个点开始，每次选择连接当前点集和外部点集的最小边。

适合稠密图，也常和优先队列一起使用。

## 常见注意点

- 图不连通时不存在完整的最小生成树。
- Kruskal 需要在加入 `n - 1` 条边后停止。
- 边权可能为负，但算法仍然成立。
