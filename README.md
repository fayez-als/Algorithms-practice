# Algorithms


This repository is for demonstrating my algorithm designing skills.




## ----- Sorting Algorithms ------

### Merge Sort: Worst Case time complexity theta(nlogn)

**proof of correctness**

**Loop invariant:**
at the start of each iteration the subarray A[p…k-1] contains k-p smallest elements of L and R in sorted order… and L[i] and R[j] contains the smallest elements their arrays that hasn’t been inserted to the sorted subarray of A

**Initialization:** K=P so the subbarray of A[p:K-1] is empty hence sorted.

**Maintenance:** During every iteration from k to r
(A has p:r elements) we insert the smallest element from L[i] or R[j] to A[k], and increment (i) or (j) by 1.
Hence the resulting subarray of A[p:k] will remain sorted.

**Termination:** the function will terminate when k = r+1 so the array of A[p:r] will be sorted.


Code: https://github.com/fayez-als/Algorithms/blob/main/merge_sort%20(1).ipynb


