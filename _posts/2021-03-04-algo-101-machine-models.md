---
layout: post
title: "Algorithmic Time Complexity 101: A Very Brief Intro to Machine Models"
description: A brief introduction to Machine Models
category: cs
tags: [cs]
comments: true
---


<p>First of all, here's 2 things to know before we discuss machine models:</p>

<ul>
<li><p>Algorithm: a method for solving a given problem</p></li>
<li><p>All data in a digital computer is represented by 1 and 0, with each single unit called a bit</p></li>
<ul>
<!-- more -->  

<p>Now let's get to it. Here's 2 popular machine models</p>

<ul>
<li> <p>Turing Machine Model</p></li>
<li> <p>RAM Model</p></li>
</ul>

<h2>Machine Model 1: The Turing Machine Model</h2>

<p>Introduced by Alan Turing in 1936 consisting of four parts:</p>

<ol>
<li><p>Tape: contains digits 0 and 1 written on each side of the tape</p></li>
<li><p>Finite Control: is the initial state</p></li>
<li><p>Head: leftmost cell in the tape. State is rewritten (or ignored) here.</p></li>
<li><p>Motor: power</p></li>
</ol>

<h2>Machine Model 2: Random Access Memory (RAM) Model</h2>

<p>The Turing machine doesn’t have any mathematical operations and cant be used to discuss algorithms, therefore we use the RAM model. Like the Turing Machine, it uses a finite control which for the RAM model corresponds to the Central Processing Unit (CPU), and a memory.</p>

<p>Computers keep their data in a cache in the CPU, memory, and external memory where each memory unit stores a word. The Finite Control uses the address of a word to store it. When we say a computer has a 64-bit CPU, this tells us about the size of a word and the size of an address. In this case, a word contains 64 bits and has enough address that its memory can contain 2^64 bits.</p>

<p>Finite Control: reads a word into memory, performs an operation to the word, then finally writes the new word (the result) into the memory either at its same address or a new one.</p>

<p>In a CPU, it has additional memory units called a program counter (PC) and a register that resets and initializes to 0 when the computer is started. After initialization, the CPU reads a word corresponding with the address from the program counter (PC) to the register. Then it applies basic operation to the data and proceeds to the next memory by incrementing the value of the program counter.</p>

<p>Generally, we can compute any function if we have the following set of operations:</p>

<ul>
<li><p>Increment value of a register</p></li>
<li><p>Decrement value of a register</p></li>
<li><p>Compare value of register with zero and branch if zero</p></li>
</ul>

<p>Because of these 3, we cant use the Turing Machine Model reliably to compute operations and write programs, since we’d have to make steps for the computation of addition. Meanwhile we can use the RAM model to realize the computation of a modern programming language like say Java. We can use concepts such as that of a variable in programming languages to that of a location in the register of a simple RAM model. </p>

<p>Beyond these two machine models, <u>there are more machine models out there, such as that of a quantum computer which is based on quantum mechanics or a DNA computer</u>, whose computational model is based on the reactions of DNA. </p>

<h2>Time Complexity</h2>

<p>We typically evaluate the efficiency of an algorithm with its time and space complexity, with an emphasis mostly on time complexity. Time complexity in this case is the number of steps needed to fulfill the computation. Space complexity is the number of words or bits required to fulfill the computation. These still, of course as mentioned 2 paragraphs ago, depends on the machine model.</p>

<p>Evaluation on the Turing Machine Model: We can figure the time complexity by the number of times the loop is repeated and as for space complexity, the amount of times we checked the tape.</p>

<p>Evaluation on the RAM model: We figure out the time complexity by the amount a program counter is updated. In the RAM model, only one data or one word in any memory cell can be read or written at a time, leading to why it’s called a “Random Access” Memory. In comparison to a Turing machine model where if the data it’s at the end of the tape, we’d have to traverse there, moving the head step by step, to read it. Another difference is that in the RAM model, one word requires log n bits to be accessed, thus some algorithms can be accessed log n faster on a RAM model than a turing machine model.</p>
