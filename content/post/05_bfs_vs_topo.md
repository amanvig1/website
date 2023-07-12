---
title: "Turns out that BFS is not the same as topological sort"
date: 2023-05-21T20:51:42+05:30
draft: true
tags:
- algo
- graphs
---

{{< rawhtml >}}
<script src="https://cdn.jsdelivr.net/npm/cytoscape@3.25.0/dist/cytoscape.min.js"></script>
{{< /rawhtml >}}

The title may seem very obvious to people who know graph algorithms. Unfortunately, I'm not one of them.



## Breadth-first search (BFS)

In this graph search algorithm, we visit all the neighbours of the node in arbitrary order. Let's consider the direct neighbours as the first level and the neighbours of the neighbours as the second level and so on. BFS will visit all nodes on the first level before visiting all nodes on the second level and so on.

Here's a visualization of BFS on a graph of project dependencies. The edges indicate dependencies i.e, `pest` depends on `serde`, etc.
Feel free to pause and explore the order in which nodes are visited.
{{% include "05_bfs_vs_topo/bfs-graph.html" %}}

## Topological sort


