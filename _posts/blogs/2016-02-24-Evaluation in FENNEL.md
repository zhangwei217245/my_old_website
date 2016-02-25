---
layout: article
title: "Evaluation in Fennel"
categories: blogs
modified: 2016-02-20T15:39:59-06:00
image:
  feature: "GP480_250.jpg"
  teaser: "GP480_250.jpg"
  thumb: "GP480_250.jpg"
tags: [Graph Partitioning]
comments: true
ads: false
date: 2016-02-20T15:39:59-06:00
---

Reading the paper of FENNEL, in the evaluation part, there are several things which deserve a mention:

1. Both experimental evaluation and system evaluation is carried out.
2. Through experimental evaluation, they compared both fraction of edge-cut and normalized maximum load. The faction of edge-cut is the portion of cut edges over all edges in a graph. The normalized maximum load is the maximum load of a partition over the size of each partition.
3. The experimental evaluation compared their work with some typical heuristic functions proposed by Stanton and Kilot. Also they compared their work with METIS on both Synthetic datasets and Real-world datasets.
4. Through the experimental evaluation, they picked up the most competitive work, along with the pure hash function scheme , to carry out the comparisons in terms of Runtime in second and Communication in MB per node and per step during the PageRank execution.
