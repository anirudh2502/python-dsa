# WEEK-2 DSA REFRESHER  
  
## ++Day 1 ++  
  
## ++Sorting++:   
It refers to the rearrangement of a given array/list of elements according to a comparison operator on the elements. The comparison operator is used to decide the new order of elements in the respective data structure.   
### ++Basic sorting algorithms++:  
1. Bubble sort  
2. Selection sort  
3. Counting sort  
4. Insertion sort   
### ++Advanced sorting algorithms++:  
1. Merge sort  
2. Quick sort   
3. Heap sort   
4. Radix sort   
### ++Why sorting is useful++:  
Sorting algorithms simplify the complex problems and improve efficiency. They are widely used in searching, databases, divide and conquer strategies, and data structures.   
* Organising large datasets for easier handling  
* Enabling quick access to the k-th smallest/largest elements   
* Making binary search possible for fast lookups in sorted data   
* Solving advanced problems in both software and algorithm design   
### ++Types of sorting techniques++:   
- Comparison-based   
- Non-comparison-based   
  
  
  
## ++Bubble sort++:   
It is the simplest sorting algorithm that works by repeatedly swapping the adjacent elements if they are in the wrong order.   
- Sorts the array using multiple passes.    
This algorithm is not efficient for large datasets as its average and worst-case time complexity are quite high.   
![Placing the 1st largest element at its correct position](Attachments/46BD1089-1080-44C9-BC70-606059AD8A06.png)  
![Placing 2nd largest element at its correct position](Attachments/421F389E-DE1D-4D1C-9E2A-5FE4DBFD3FAD.png)  
![Placing 3rd largest element at its correct position](Attachments/964A39E1-1DCB-4DF2-B38D-1DAA7524EAEE.png)  
**++Advantages++**:   
- Easy to understand and implement  
- Does not require additional memory space   
- Stable sorting algorithm  
**++Disadvantages++**:   
- Has time complexity of O(n^2), which makes it very slow for large datasets.  
- It has almost no or limited real world applications.  
  
  
  
## ++Selection sort++:  
It is a comparison-based sorting algorithm. It works by repeatedly selecting the smallest/largest element from the unsorted portion and swapping it with the first unsorted element.   
![Swapping Elements](Attachments/DE1B951C-EB3C-4ECF-83C7-5146951F5F51.png)  
![Swapping](Attachments/72C715F6-1A14-4B9F-BB59-FBCD1B262AE7.png)  
![Swapping](Attachments/2D311E1C-9E64-4647-8C26-D11D0E0545F8.png)  
![Min element](Attachments/7F59EC40-03BE-4F98-A987-9982117DF6FD.png)  
![arrl] =](Attachments/D7674933-7ED0-4B13-ADCC-29B660F69930.png)  
**++Advantages++**:   
- Easy to understand and implement  
- Requires only a constant O(1) extra memory space  
- Requires less number of swaps compared to other algorithms  
**++Disadvantages++**:   
- It has a time complexity of O(n^2), making it slower  
- Does not maintain the relative order of equal elements, meaning not stable  
**++Applications++**:  
- Suitable for small lists where the overhead of more complex algorithms isn’t justified and memory writing is costly  
- Perfect for teaching fundamental sorting mechanisms and algorithm designs  
  
  
  
## ++Insertion sort++:   
It is a simple sorting algorithm that works by iteratively inserting each element of an unsorted list into its correct position in a sorted portion of the list.   
![arr[] =](Attachments/134E075F-98F5-429F-A55C-E294A2A34BF1.png)  
![arrl) =](Attachments/AB3EF880-A3C6-4A68-B75F-C2D380521BE9.png)  
![arrl] =](Attachments/2FC4FF60-4A09-45B6-B362-86ABAEAF551D.png)  
![arri] =](Attachments/8843D438-EEDF-4C1F-B9AF-32ED01391287.png)  
**++Advantages++**:  
- Simple and easy to implement   
- Stable algorithm   
- Efficient for small lists and nearly sorted lists  
- Space-efficient (as it is an in-place algorithm)  
**++Disadvantages++**:  
- Inefficient for large lists  
- Not as efficient as other sorting algorithms for most cases  
**++Used where++**:  
- The list is small or nearly sorted  
- Simplicity and stability are important   
- Used in hybrid sorting algorithms   
  
  
  
## ++Merge sort++:  
It is a popular sorting algorithm known for its efficiency and stability. It follows the Divide & Conquer approach. It works by recursively dividing the input array into two halves, recursively sorting the two halves and finally merging them back together to obtain the sorted array.   
![UnSorted Array: 70|30 50 10]](Attachments/8A7275C0-E245-42DB-BB9E-D21941C3E8B1.png)  
**++Applications++**:  
- Sorting large datasets  
- Used to solve problems like inversion sorting, count smaller on right, etc  
- Used in library methods of programming languages  
- Preferred algorithm for sorting linked lists   
- The merge function of merge sort for efficiently solving problems like union and intersection of sorted arrays  
**++Advantages++**:  
- Stable sorting algorithm’  
- Simple to implement  
- Independently merge subarrays that makes it suitable for parallel processing  
**++Disadvantages++**:  
- Requires additional memory to store the sorted data   
- Slower than quick sort as quick sort is more cache friendly  
  
  
  
## ++Quick sort++:  
It is a sorting algorithm based on Divide & Conquer, that picks an element as a ‘pivot’ and partitions the given array around the picked pivot element by replacing the pivot element in its correct position in the sorted array.   
++Steps++:   
1. Select an element in the array as pivot (first/last/median/random)  
2. Rearrange the array around the pivot. After partitioning, all elements smaller than the pivot element will be on the left and the rest on the right  
3. Recursively apply the same process to the two partitioned subarrays  
4. The recursion stops when there is only one element left in the subarray  
![Screenshot 2026-10-30 at 8.58.42 PM.png](Attachments/71299AB3-266D-43F8-A3CB-237C5BC0C0F0.png)  
**++Advantages++**:  
- It is a divide & conquer algorithm, making it easier to solve problems   
- Efficient on large datasets  
- Requires a small amount of memory to function  
- It is cache friendly   
**++Disadvantages++**:  
- It has worst-case time complexity of O(n^2)  
- Not a good choice for small datasets  
- Not a stable sorting algorithm  
**++Applications++**:  
- Sorting large datasets efficiently in memory   
- Used in library sort functions  
- Arranging records in databases for faster searching  
- Sorting arrays of objects based on multiple keys   
- Graphics and computational geometry  
  
  
  
## ++In-place sorting and algorithms++:  
It means that the algorithm does not use extra space for manipulating the input but may require a small though non-constant extra space for its operation.   
![Time Complexity: O(n)](Attachments/41EFB297-254A-4072-9528-39FC2399F251.png)  
This needs O(1) extra space for exchanging elements.   
*Bubble sort, selection sort and insertions sort are in-place sorting algorithms*  
***Merge sort**** is **not** an in-place algorithm*  
  
  
  
## ++sorted() v/s sort()++:  
Both of them are used for arranging elements in order, but they differ in their return value, effect on original data, and the types of objects they can be used with.   
### ++sorted():++  
Takes an iterable such as a list, tuple, string, or set and returns a new list containing its elements in sorted order. The original iterable remains unchanged  
![numbers = 15, 2, 0, 1, 41](Attachments/AA52932C-BD0F-4B00-93FB-A11AF887936D.png)  
### ++sort()++:  
Available for lists and rearranges their elements directly in ascending or descending order. It changes the original list and returns None  
![numbers = 15, 2, 8, 1, 4]](Attachments/FAB8322F-F541-4937-BC5E-868EC00190E9.png)  

| sorted() | sort() |
| ------------------------------------------------- | ------------------------------------------------- |
| Built-in function | List method |
| Works with any iterable | Works only with lists |
| Returns a new sorted list | Returns None |
| Does not modify the original iterable | Modifies the original list |
| Ascending by default, reverse=True for descending | Ascending by default, reverse=True for descending |
  
  
  
  
## ++Insertion sort++:  
![#insertion sort](Attachments/861A1DD6-3B0A-4F92-8223-892F7BF206A1.png)  
  
  
  
## ++Merge sort++:  
![#merge sort](Attachments/4749558F-A7C4-4643-B808-5A889CCB0973.png)  
  
  
  
## ++Quick sort++:  
![squick sort](Attachments/14A6273A-A494-4612-9FB0-460D32D4A5EE.png)  
  
  
