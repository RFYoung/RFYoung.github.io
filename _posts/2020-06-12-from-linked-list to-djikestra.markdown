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

A linked list is a basic data structure. It contains "nodes", in which there are data and pointer(s) that point to other nodes. The linked list here is the "singly linked list", which only has one pointer which point to the child in each node. With this list, we can not get the parent node from the child, but we could save more memory. In most cases, it is enough to use the singly linked list.

Normally, when we use a linked list, we need to store where is the first node. What I need to emphasize is that we could not record the position of the first node when we use the only the recursion part. The first node must be assigned individually. Therefore, When we generate the normal linked list, we have to copy the code inside the recursion part at the beginning of the assignment function to assign the first node (to record the first node).  

So now we have the data structure to store the data we need in this task. Of course, you can construct the adjacency list directly, but this could make your code more complicated.

### Read the file

The coursework need us to read the data from a structured file. This is not very complicated by using the C language. The main idea is to use "gets" to read one line in the file and store it into a string and use "sscanf" to pick up the data in the string that with a fixed strcuture.

Notice that: We only need the three data of a node in the graph - ID, langitude and latitude (If the node in tha graph is not using a coordinate, you do not need the latter two, actually you even do not have to mention the nodes!) and four data of the edges - the edge ID, the IDs of two nodes that it connected  and the length.

I believe that these steps could be more simple and clear using another langugae.

### Generate the list

We could genreate the node each time we read a node or edge of a graph in the file. Of course we need extra variables to store how many list nodes we have genreated.

## Adjacency List

...
