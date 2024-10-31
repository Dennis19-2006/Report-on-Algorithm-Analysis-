# Algorithm Analysis

# Static Array

#Static Array Operations

1.	Insertion
	Time Complexity: O(1) (if inserting at the end) or O(n) (if inserting at a specific index that requires shifting elements).
	Space Complexity: O(n), where n is the size of the array.

2.	Deletion
	Time Complexity: O(1) (if deleting the last element) or O(n) (if deleting from an index that requires shifting elements).
	Space Complexity: O(n)).

3.	Traversal
	Time Complexity: O(n)), where n is the number of elements.
	Space Complexity: O(1) since it requires no additional space.


# Dynamic Array

#Dynamic Array Operations

1.	Insertion
	Time Complexity: O(1)for most insertions. However, during resizing (when capacity is reached), it takes O(n) time to copy elements to a new array.
	Space Complexity: O(n), where n is the number of elements in the array.

2.	Deletion
	Time Complexity: O(1)(last element) or O(n) (with shifting).
	Space Complexity: O(n)

3.	Traversal
	Time Complexity: O(n)
	Space Complexity: O(1)


# String Operations

1.	Concatenation
	 Time Complexity: O(m+n), where m and n are the lengths of the two strings.
	 Space Complexity: O(m+n) for creating a new concatenated string.

2.	Substring
	Time Complexity: O(k), where k is the length of the substring.
	Space Complexity: O(k)) for storing the substring.

3.	Comparison
	Time Complexity: O(min⁡(m,n)), where m and n are the lengths of the two strings.
	Space Complexity: O(1) since no additional space is needed.

4.	Character Frequency
	Time Complexity: O(n), where n is the length of the string.
	Space Complexity: O(n) for storing frequencies of each character.


# 1. Binary Search
   It is used to find the position of an element in a sorted array. Each time, it halves the search space, leading to a recurrence relation that describes this behavior.

The recurrence relation for binary search can be expressed as:

•	T(n)=T(n/2)+O(1)T(n) 

 where,
•	T(n)): The time complexity of binary search for an input of size nnn.
•	T(n/2) Recursive call on half the array size.
•	O(1) Constant time work done per step (e.g., comparing the middle element).


Solution by Recurrence Tree:

1.	Unrolling the recurrence:
	T(n)=T(n/2)+O(1)
	T(n)=T(n/4)+O(1)+O(1)
	T(n)=T(n/8)+O(1)+O(1)+O(1)
	Continuing this way leads to T(n)=T(n/2k)+k⋅O(1)

2.	Base case:
•	We reach T(1) when n/2k=1

3.	Final Solution:
•	Substituting k=log⁡2(n),we find T(n)=O(log⁡n)

#      Result:
•	Time Complexity: O(log⁡n)

•	Space Complexity: O(log⁡n) due to the recursion stack.



# 2. Merge Sort
   Merge sort divides the array into two halves and then merges them.
   

The recurrence relation for merge sort is:

•	T(n)=2⋅T(n/2)+O(n)

where,
•	2⋅T(n/2)2): Two recursive calls on each half of the array.
•	T(n)): Time complexity for merge sort on input of size nnn.
•	O(n)): Time to merge two halves (linear).


Solution using Master Theorem: The recurrence relation fits the form:

•	T(n)=a⋅T(n/b)+f(n)
•	Here, a=2a, b=2b, and f(n)=O(n)

To apply the Master Theorem, calculate nlog⁡b(a)n^{\log_b(a)}nlogb(a):

•	Since log⁡2(2)=1nlog2(2)=O(n)
•	Since f(n)=O(n), we match Case 2 of the Master Theorem, where f(n)=O(nlog⁡b(a))

# Result:
•	Time Complexity: O(n log⁡n)

•	Space Complexity: O(n), as merging requires temporary space.

