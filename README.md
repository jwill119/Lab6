# Lab 6: Isolation and difference
COSC 2030 Lab 6
Jacob Williams, 11/5/2018

In this lab, we solve two problems:

- First, we find the most isolated number in a sorted collection.
- Second, we count the size of the set difference of two sets of words.

### The isolated number
Input: a vector<double> sorted in ascending order.
  Output: the most-isolated number (that whose nearest neighbor is farthest away.
  
How will we find this?
- We can assume the vector is not empty
- If there is one element in the vector, it is the most isolated

Assume vector.size() >= 2
- Store vector[0]
- Iterate to vector[1] and store that
- Find the difference (we don't need absolute value because the vector is sorted)
- Assign that difference to Isolation_of_vector[0] (or whatever we call it)
- For vector[2]:vector.end(), find the difference between vector[i] and vector[i-1] and assign it to Isolation_vector_[i-1].
- As a note, we will *never* have the last element be most isolated!

### The set difference
