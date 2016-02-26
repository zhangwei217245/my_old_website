---
layout: article
title: "Reading Notes: FENNEL"
categories: blogs
modified: 2016-02-24T15:39:59-06:00
image:
  feature: "GP480_250.jpg"
  teaser: "GP480_250.jpg"
  thumb: "GP480_250.jpg"
tags: [Graph Partitioning]
comments: true
ads: false
date: 2016-02-24T15:39:59-06:00
---

Reading the paper of FENNEL, something to be noticed:

{% include toc.html %}

# Novelty:
1. A new graph partitioning framework where global cost function is defined as follows:
global cost = total edge-cut number + sum of convex function value over each partition.

2. Proved that minimizing this global cost is equivalent to maximizing :
g = total number of edge-cut - convex increasing value of all partitions,
and is equivalent to maximizing the modularity of a partition.

3. Proposed a streaming algorithm by assigning each vertex to the partition such that the total global cost is minimized or the modularity is maximized.

# Possible drawback:
1. While making decision on the placement of a vertex, it will result in more computational overhead on calculating the global cost.

# Possible benefit for our study:
1. We might use this global function as our cost function of heuristic search.

# Evaluation

1. Both experimental evaluation and system evaluation is carried out.
2. Through experimental evaluation, they compared both fraction of edge-cut and normalized maximum load. The faction of edge-cut is the portion of cut edges over all edges in a graph. The normalized maximum load is the maximum load of a partition over the size of each partition.
3. The experimental evaluation compared their work with some typical heuristic functions proposed by Stanton and Kilot. Also they compared their work with METIS on both Synthetic datasets and Real-world datasets.
4. Through the experimental evaluation, they picked up the most competitive work, along with the pure hash function scheme , to carry out the comparisons in terms of Runtime in second and Communication in MB per node and per step during the PageRank execution.
