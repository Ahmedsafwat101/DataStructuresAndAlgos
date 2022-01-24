# DataStructuresAndAlgos
<details>
  <summary>Heap</summary>
	<br>

This article is to deep dive into one of the most fundamental data structures called Heap. The objective of this post is to understand the basics of Heap, time complexities, and identify patterns when to use Heap as a data structure.

Heap questions are one of the most common questions frequently asked in interviews.

The confidence in HEAP data structure is guranteed if you finish below mentioned 23 questions.

# What is Heap?
- It is mainly used to represent a priority queue.
- It is represented as a Binary Tree (a tree structure where a node of a tree has a maximum of two child nodes). Heaps are complete binary trees.
- A simple array can be used to represent a Heap where array indices refer to the node position in the tree.
- Parent and child nodes can be accessed with indices:
   - A root node｜i = 0, the first item of the array
   - A parent node｜parent(i) = (i-1) / 2
   - A left child node｜left(i) = 2i+1
   - A right child node｜right(i)= 2i+2
- Two type of Heaps — Min Heap, Max Heap
  - Min Heap — the parent node always has a smaller value than the child nodes.
  - Max Heap — the parent node is always larger than the child node value.	
	
- Usually, when a type is not mentioned, it refers to the MinHeap. java PriorityQueue has minHeap as default.
- minHeap are used in tasks related to scheduling or assignment. A more detailed explanation is under the Patterns section below.
	
# Heap Operations
The basic operations in java PriorityQueue are:

heapify
The heapify operation converts the iterable array heap into a tree structure w.r.t heap order.

heappush
It inserts an element into the heap. Post insertion the heap order is adjusted to maintain the heap properties.

import heapq as hq
# Simple array is heap
	
```
Integer[] numArr ={1,2,1,3,3,5,7};
PriorityQueue<Integer> minHeap = new PriorityQueue();
# this is done to convert iterable into a heap tree
minHeap.addAll(Arrays.asList(numArr));
```	
# Adding an element to the heap
```	
minHeap.add(5)
```	
# Removing an element to the heap
This operation is to remove the element from the heap. By default it is minHeap, so this operation removes the min element from the minHeap. And for maxHeap, it is the maximum element. Post removal, heapify is called internally to maintain the heap order.
	
```
minHeap.poll();
```
	
# Getting top element from the heap
```	
int value = minHeap.peek(); # return the top element in the minheap which is the smallest element without removing it. 
```

Problem Patterns where HEAP is used
Based on my understanding, different questions where HEAP is common data structure to use can be categorized in following 4 categories:

Top K Pattern
Merge K Sorted Pattern
Two Heaps Pattern
Minimum Number Pattern
All questions under one patterns has some similarities in terms of using HEAP as a data structure. Completing these questions would gurantee you mastery on the HEAP data structure. Below list includes some of the most common questions asked in most of the companies.

- Top K Pattern
  - LC #215 - Kth largest number in an array
  - LC #973 - K closest points to origin
  - LC #347 - Top k frequent elements/numbers
  - LC #692 - Top k frequent words
  - LC #264 - Ugly Number II
  - LC #451 - Frequency Sort
  - LC #703 - Kth largest number in a stream
  - LC #767 - Reorganize String
  - LC #358 - Rearrange string K distance apart
  - LC #1439 - Kth smallest sum of a matrix with sorted rows

- Merge K sorted pattern
  - LC #23 - Merge K sorted
  - LC #373 - K pairs with the smallest sum
  - LC #378 - K smallest numbers in M-sorted lists

- Two Heaps Pattern
  - LC #295 - Find median from a data stream
  - LC #480 - Sliding window Median
  - LC #502 - Maximize Capital/IPO

- Minimum number Pattern
  - LC #1167 - Minimum Cost to connect sticks/ropes
  - LC #253 - Meeting Rooms II
  - LC #759 - Employee free time
  - LC #857 - Minimumcost to hire K workers
  - LC #621 - Minimum number of CPU (Task scheduler)
  - LC #871 - Minimum number of Refueling stops
	

<a href="https://leetcode.com/list/9t3f1x82" target="_blank">All Problems in one list</a>

</details>  

<details>
    <summary>HashMap</summary>
	<br>
 This article is to deep dive into one of the most fundamental data structures called HashMap. The objective of this post is to understand the basics of HashMap, time complexities, and identify patterns when to use HashMap as a data structure.

What is HashMap?
- It is a type of fast key lookup data structure.
- It is represented as list of pairs the first part of the pair is called key and the second part is called the value
- Any value can be accessed through the unique key that hashed through hashing function and refer to specific index, the key aslo can be null.
- Two type of Maps — the map is an interface and HashMap implements that interface, TreeMap also do the same
  - HashMap — order pairs in order of insertion.
  - TreeMap — Order pairs based on the key values with some overhead complexity.	


We may think about the hashmap when we want to have constant runtime for insertion and for retrieving O(1)
	
# HashMap Operations

# Create HashMap
```
HashMap<Integer,Integer> hashMap = new HashMap<>();
```
# Add -> O(1)	
```
HashMap<Integer,Integer> hashMap = new HashMap<>();
// key: 1 & value: 5
hashMap.put(1,5);
hashMap.put(1,5);
hashMap.put(2,7);
hashMap.put(3,6);
hashMap.put(null,4);	
//hashMap = [(1->5),(2->7),(3->6),(null->4)]
```	
# Get -> O(1)	
```
hashMap.get(1); // return 5
```
# PutIfAbsent -> O(1)	
```
 hashMap.putIfAbsent(10,2);
// will check if the key 10 doesn't exit will add it with its value
```
# PutIfAbsent -> O(1)	
```
hashMap.getOrDefault(10,2);
//Returns the value to which the specified key is mapped,or defaultValue if this map contains no mapping for the key.
```
# ContainsKey -> O(1)		
```
hashMap.containsKey(10);
//Returns true if this map contains a mapping for the specified key.
```	
# Remove -> ~ O(1)	
```
hashMap.remove(1); 
```	
	
	
<a href="https://leetcode.com/tag/hash-table" target="_blank">All Problems in one list</a>
	
</details>	
	
	
To Be Continued ... 
	
Please don't forget to put a star if you like the article :)
