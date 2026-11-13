# Week 2 day 4 DSA  
  
## ++Day 4++  
  
## ++Heap++:  
It is a complete binary tree data structure that satisfies the heap property. Heaps are commonly used to implement priority queues, where the smallest/largest element is always at the root.  
- In a min-heap, the value of the child >= to its parent  
- In a max-heap, the value of the child <= to its parent  
![Min Heap](Attachments/3C3ABB26-CFAA-4079-8FB0-FF8710E7B894.png)  
![5 4 3) (2)](Attachments/67CAA969-00A0-47FA-B13D-3B0A75DA480F.png)  
  
  
  
## ++Heap properties++:  
1. **Complete binary tree** - the tree fills up level by level, and the last level fills from left to right with no gaps. (Like filling seats in a theatre from left to right and then moving to up row)  
2. **Min-heap property** - every parent is <= to its children; so the smallest value sits at the top (root).  
3. **Max-heap property** -  every parent is >= to its children; so the largest value sits at the top (root).   
4. **Partial ordering** - a heap is not fully sorted. It only guarantees that parents beat their children. Two siblings can be in any order relative to each other.  
  
  
  
Insertions and removals:  
Elements can be inserted and removed while maintaining the heap property.   
* ++[heapq.heappush(heap, item)](https://www.geeksforgeeks.org/python/python-heapq-heappush-method/)++ --> adds a new element to the heap  
* ++[heapq.heappop(heap)](https://www.geeksforgeeks.org/python/python-heapq-heappop-method/) ++—> removes and returns the smallest element  
![import heapq](Attachments/758A0591-E2A3-478B-89B6-1E5F9221C90E.png)  
  
  
  
## ++Heap-based priority queue++:   
Also known as priority queue, it is a data structure that allows quick access to the smallest (min-heap) or largest (max-heap) element.  
- By default, heaps are implemented as min-heaps  
- Smallest element is always at the root and the largest is located among the leaf nodes  
- Built-in module “***heapq***” that allows to create and work with heap queues  
![import heapq](Attachments/9C7CBBBA-F89A-4703-BA1F-2824C1536F96.png)  
***IT DOES NOT FULLY SORT THE LIST***  
  
  
  
## ++Kth largest element using heap: ++  
![# finding kth largest element using heap](Attachments/97CC69BC-64EA-4107-B8F7-797BF025E685.png)  
