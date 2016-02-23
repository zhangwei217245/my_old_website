---
layout: article
title: "Reading Notes: Streaming Graph Partition Schemes"
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

Recently, I'm doing research on Graph Partitioning for HPC system. Since usually the HPC system features multiple distributed computing nodes, while carrying out graph related computation on such platform, it is obvious to think about the data distribution problem which naturally can be transformed into graph partitioning problem.

However, when talking about graph computing problem, the first thing to know is the type of computatoinal operation. There are two different types of operation, OLTP and OLAP. While OLTP focuses on fast transactional operations like traditional CRUD operations against vertices and edges, the OLAP operations focus more on the complex analytical operations, such as graph eccentricity, community structure, centralality measure, isomorphism, etc. Although OLAP seems to be fancier, many of the subroutine of OLAP operations consists of multiple OLTP operations. Especially when it comes to dynamic graph which changes all the time such as social graph, e.g. Facebook or Twitter, the speed to accomplish data processing really matters. Thus, having a streaming graph partiioning scheme becomes really important.

So far, I've been looking at some different papers talking about streaming graph partitioning approaches. 

 


