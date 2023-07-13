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

## The problem

This is about implementing a **dependency graph**. Think of a project's npm/pip/maven/cargo dependencies. Or a data pipeline with SQL tables depending on each other.

Here is the problem that needed to be solved.
Given a project or a table (a "node") in the tree, how do I get all the other nodes that *depend* on it (the *dependents*)?
In other words, if I change the given node/project/table, which other nodes will I need to recompile/recreate?
The graph is structured specifically to help with this. Given a node, we know the *direct* dependents. So we just need to follow this trail to get all the dependents. The hard part here is getting the nodes in the right order. The right order being that all dependencies of a node are "visited" before the node itself.

At the time, it seemed that a simple breadth-first search will give me all the nodes in order. Let's see how.

## Breadth-first search (BFS)

In this graph search algorithm, we visit all the neighbours of the node in arbitrary order. Let's consider the direct neighbours as the first level and the neighbours of the neighbours as the second level and so on. BFS will visit all nodes on the first level before visiting all nodes on the second level and so on.

Here's a visualization of BFS on a graph of project dependencies. The edges indicate dependents i.e, `pest` depends on `serde_json`, etc.
Feel free to pause and explore the order in which nodes are visited. You can click on a node to start BFS from that node.

{{% include "05_bfs_vs_topo/common.html" %}}
{{% include "05_bfs_vs_topo/bfs-graph.html" %}}

## Topological sort

{{% include "05_bfs_vs_topo/topo-graph.html" %}}
