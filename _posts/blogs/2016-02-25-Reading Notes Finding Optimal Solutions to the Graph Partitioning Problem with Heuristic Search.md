---
layout: article
title: "Reading Notes: Finding Optimal Solutions to the Graph Partitioning Problem with Heuristic Search"
categories: blogs
modified: 2016-02-24T15:39:59-06:00
image:
  feature: "blogpost/A_star_search_against_gp/hw1_search_tree_a_star.jpg"
  teaser: "blogpost/A_star_search_against_gp/hw1_search_tree_a_star.jpg"
  thumb: "blogpost/A_star_search_against_gp/hw1_search_tree_a_star.jpg"
tags: [Graph Partitioning]
comments: true
ads: false
date: 2016-02-24T15:39:59-06:00
---

Reading the paper of "Finding Optimal Solutions to the Graph Partitioning Problem with Heuristic Search", something to be noticed:

{% include toc.html %}

# Contribution
1. A new optimal solver of graph partitioning problem.
  * We can still propose another solver following this technique.
2. Demonstrate how a star search could possibly be applied to GPP.
  * But applying AI to GPP is not our contribution any more.

# Actual Partitioning Approach
* Precondition: edge-cut.
* Steps:
1. Form a search tree, where each tree node corresponds to a partial partition of the vertices in a graph.
2. Sort the vertices in a graph.
3. Search a binary tree where each level of the tree corresponds to a different vertex in the graph.
4. At each node of the search tree, left branch would assign the vertex to one subset, while the right branch would assign the vertex to the other subset.
5. Totally 2^n different subsets corresponds to the leaf nodes.
6. Prune each subtree rooted by a node where one of the partitions has more than half of the vertices.

# Possible drawback
1. Terrible memory efficiency due to exponential growth of the priority queue size.
  * Some heuristics may bring some improvement, however, either they do not guarantee the solution will be optimal, or they increase the complexity of implementation, which makes the improvement modest.
2. Since this work aims to find optimal solution against GPP, which is known to be NP-hard, it can only deal with graph of small size and requires to carry out systematic global search.

# Possible value for our study
1. To know how we may apply AI technique on GPP.

# Evaluation
* Most of the evaluation was done on some small size graphs, or some graph with very low average degree. Which means, currently, we should avoid a star search technique for GPP since finding an optimal solution for now may be not very meaningful for our research. Possibly change the title to "Assortativity/Similarity optimized approach for hash-based streaming graph partitioning."
