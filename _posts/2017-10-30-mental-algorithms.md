---
layout: post
title: "Mental Algorithms"
categories: [misc]
tags: 
  - algorithms
comments: true
description: When thinking about problems, people usually have two ways to tackle such situation. Let's consider the graph below.
---

<p align="justify"> When thinking about problems, people usually have two ways to tackle such situation.
</p>

<center>
<p> Let's consider the graph below.
</p>
</center>

<center>
<img src="https://i.imgur.com/cTQQ1zM.jpg">
</center>

<br>

<p align="justify"> The graph is an example of an undirected graph, of which the graph in this case is mathematically represented as <strong>G</strong>. The vertices, the nodes are represented as <strong>V</strong> and the edges, or the lines connecting each vertices is represented as <strong>E</strong>. Formally, we can then define the graph as <strong>G</strong> = {<strong>V</strong>,<strong>E</strong>} where <strong>V</strong>,<strong>E</strong> are unordered pairs of <strong>V</strong>.
</p>
<!-- more -->  

<p align="justify">In computer science, the two most common ways to traverse such graph are breadth first search and depth first search. Breadth first search is when you traverse such graph by exhausting all the nearest vertices from the current/source vertex before moving on to vertices on the next level. Say in the graph above, <strong>G</strong>, your source vertex is a, <strong>s</strong>, you would first traverse into vertex b and c, the reachable vertices or edges of <strong>s</strong> before you move on to the next level.</p>

<center>
<img src="https://i.imgur.com/EUVuE41.jpg">
</center>

<br>

<p align="justify">This in real life can be associated to thinking broadly. Should people think broadly when solving a problem, this method of thinking is best suited to problems that we have little idea of. A common mistake that people make is that when thinking broadly, is that they go into random solutions to tackle such problem. Breadth first search teaches us that we ought to first think of all related solutions before branching deeper. Thinking should be structured. This allows us to see the big picture, a bird's eye view as we unfold our way to fully understand the problem.
</p>

<p align="justify">The other algorithm, depth first search, as its name suggests, traverses the graph by going deeper. Say from the source vertex a, the algorithm would traverse into b and then into d and e, the farthest edge from the visited vertices. Afterwards, it would backtrack again to all the visited vertices. The tree edges then are <strong>v ϵ V and v.e ≠ discovered </strong>. 
</p>

<center>
<img src="https://i.imgur.com/qnWDJBD.jpg">
</center>

<br>

<p align="justify">This can be alluded to thinking deeply. Depth first thinking is done when we have an idea of where the problem might lead us to, or in situations where we know that there's only a few possible solutions to the problem. As such, this kind of thinking is often used when thinking strategically, where we get an early understanding of the branches of a tree. Compared to breadth first thinking, where we suspend our understanding of a branch until we have exhausted others. For example, depth first search is typically used in chess.</p>

<p align="justify">Say you are evaluating a startup idea. One of the questions that will pop up is, <i>"What is your target market?"</i> Depth first thinking in this scenario will then be about looking at a single hypothesis for the question, evaluate and research a market lead as far as you can before pivoting to the next hypothesis and see if the evaluated branches/hypotheseses holds more weight than the new one. On the other hand, breadth first thinking will have us listing all the possible market entries first, then one by one we evaluate them for a certain category or factor before performing further research.
</p>

<p align="justify"> These two approaches are popular as they allow us to modularised our thinking. Nonetheless, choosing between the two depends on one's aptitude of procedural decision making.
</p>

