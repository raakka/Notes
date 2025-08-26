# Lecture 1 - Intro

### How do we compare solutions to a problem?
- Obviously less steps is better, but how to compare over a lot of inputs to a program
- Asymptotic behavior lowkey not good, a lot of thing converge at extremes.
    - Does not provide a lot of context for comparison
 
### O(n) - Upper Bounds on Solution Steps
- O(n) bounds the number of steps a solution takes
- Nice because gives us context to compare solutions over a lot of input sizes
- However picking lowest bound is not the only way we want to compare solutions
    - O(n) not an absolute best metric for performance
    - Sometimes we care about simplicity, or space complexity
    - Also sometimes we know what size input we are getting: Plan accordingly or suffer
    - TLDR: Other metrics exist, just try to minimize regret of chosing a solution given a problem + context </br></br>
- O(n) works well usually for big inputs because with big inputs the "regret" gets significantly larger

#### What is O(n)?

**Definition**: $f(n) \text{ is } O(g(n))$
**If** $\exists c \ge 1, \space n_o \ge 0$ **such that** $\forall n \ge n_o, \space f(n) \le c g(n)$

## Comparing Merge-Sort vs. Quick-Sort

> **Recall**: Quick sort is a sorting algo that works using a divide and conquer approach. It works by selecting a
> pivot element for the partitions. Then every element larger than the pivot goes to the right, and any element
> less than it goes to the left. This repeats until we end up with partitions of size one, where we know that
> the list is already sorted.

#### Example of Quick Sort

![picture of quick sort](https://media.geeksforgeeks.org/wp-content/uploads/20240926172924/Heap-Sort-Recursive-Illustration.webp)


### Runtime Complexity Analysis of Quick-Sort

#### Best Case

> Best case occurs when we pick the median (value) element for our pivot every time

$$T(n) = 2 T(\frac{n}{2}) + n$$
$$T(n) = 2 (2T(\frac{n}{4}) + \frac{n}{2}) + n  = 4T(\frac{n}{4}) + 2n $$
$$T(n) = 8T(\frac{n}{8}) + 3n  \text{ and etc...}$$

#### Average Case

### Runtime Complexity Analysis of Merge-Sort

> **Recall**: Merge sort is a sorting algo that also works using a divide and conquer approach. It works by 
> partitioning up an array into multiple partitions until, the partitions are of size one, then sorts the 
> partitions when they are merged together into the same list.

#### Best Case



