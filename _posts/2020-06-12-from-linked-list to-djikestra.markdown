---
layout: post
title:  "From Linked List to Dijkstra"
date:   2020-06-11 12:39:20 +0800
categories: coursework blog
---

## Aim

In this blog, I would introduce a simple idea about how to implement a route-finding program based on the Dijkstra algorithm and some simple data structure. I would do it step by step to help some beginners to understand the blog.

Of course, this blog would not include any real code to avoid plagiarism, and I believe that the author could write the code by their own in about 3 days. By the way, the program I have written is in C language, you may find some built-in functions in some other language (for example, STL in C++ provide priority queue, so you may not implement binary heap by yourself when using C++).

I was new at algorithm and data structure, so please contact me if you have some greater idea or suggestions. I would be very appreciative.

## Linked list

A linked list is a basic data structure. It contains "nodes", in which there are data and pointer(s) that point to other nodes. The linked list here is the "singly linked list", which only has one pointer in each node. With this list, we can not get the parent node from the child, but we could save more memory. In most cases, it is enough to use the singly linked list.

Normally, when we use a linked list, we need to store where is the first node. When we generate the normal linked list, we have to copy the code of the recursion function at the beginning of the assignment function to assign the first node (to record the first node). However, we could just firstly generate a blank node as the first node and do the recursion.
