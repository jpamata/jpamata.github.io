---
layout: post
title: "Patterns of Algorithmic Thinking"
description: 
category: articles
tags: [algorithms]
comments: true
---

I think that problem-solving is about how much patterns you've memorized. I recently read a thread about a guy asking for tips to help him learn data structures and algorithms as he's having a hard time.

<!-- more -->

Well I'm no master at it but I think that if you want to learn about data structures and algo, you learn by learning how to implement one multiple times over. If you know the idea of let's say a binary search tree, and I give you a modified binary search tree with custom rebalancing functions, what the fuck are you gonna do? 

Implementing one > knowing how it works

Once you've implemented it again and again, you gain intuition. 

As for algorithmic thinking, I think that one finally starts to "get it" after going through 200 algorithmic problems. I don't care if you looked at the solution for every one and didn't attempt more than 20 minutes for each problem them. Because after you've gone through those things, you'd have picked up some degree of problem solving intuition. It's okay to memorize solutions.

It's all about pattern recognition. For example in this case, here's a sample of patterns I recall from going through a few algorithm problems:

- fast lookup or checking for duplicates? hashmaps

- Partition an array? Quicksort or DFS

- Implement a cache? Start thinking of queues or if it really needs a key like an LRU or memcache, then hashtables.

- Sub search? Sliding window pattern for sstrings and hashmaps for arrays

- Find something in a Sorted structure (array, string, linkedlist)? Two pointer pattern

- Not sorted? no problem. Sort it then hash map or binary search, nonetheless it's nlogn guaranteed. so first look if we can separate processes into a series of loops like O(n + m) or some crap

- Algorithm has to be implemented under linear time? Divide and Conquer approach, BST, or Binary Search.

- Speaking of binary search... does the problem detail has the words “find” and “sorted array”? Yeah definitely think of that.

- Implementing a heap? Binary tree.

- Tree problem? DFS or BFS.

- Shortest path? BFS. Optimise BFS later? just add priority queue and it's dijkstra

- Maze problem? DFS or dynamic programming

- subsequences? knapsack? dynamic programming

note: that's just a few of basic things you'll start thinking of when you see a problem, and I'm too lazy to type more, perhaps later I'll update this blog article to add more when I'm feeling productive. 

But anyhow there are caveats to look out for when thinking of each problem, the pros and cons to the approach and it's normal to combine approaches. But one gets the idea that yes, indeed the whole thing can look like a plug and play once we've done a few problems

Same with math, we memorize patterns and rules. Same with chess, patterns. Hell, a study was done and grandmasters fared as well as amateurs when they played a chess game with a different set of rules. How does a neural network learn? They find patterns from the dataset and commit them to memory. That's how your brain works.

So keep on feeding your brain data.
