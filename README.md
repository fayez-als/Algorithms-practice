# Algorithms


This repository is for demonstrating my algorithms skills.




## ----- Sorting Algorithms ------

### Insertion Sort: Worst Case time complexity theta(n**2)

**proof of correctness**

**Method of proof**:
	I will prove that before and after each iteration
	We have a sorted subarray A[0:j]
	
	And the function terminate when j ==length(A):
  So we have a complete sorted array A

**Initialization:**
	
  A[0:j] contains 1 element (A[0])So A[0:j] is sorted by default.
  
**Maintenence**:
  	If the subarray A[0:j] is sorted, and we inserted A[j+1]
    in its corrected sorted position, the resulting subarray will be sorted after insertion.
    
    
 **Termination:**
 
 	During each iteration we increase j by one and insert
  A new element j+1 in the subarray. The function terminate when  j== length(A).
  
  Code:
  
  

  








### Merge Sort: Worst Case time complexity theta(nlogn)

**proof of correctness**

**Loop invariant:**
  at the start of each iteration the subarray A[p…k-1] contains k-p smallest elements of L and R in sorted order… and L[i] and R[j] contains the smallest elements their arrays   that hasn’t been inserted to the sorted subarray of A

**Initialization:** 
  K=P so the subbarray of A[p:K-1] is empty hence sorted.

**Maintenance:** 
  During every iteration from k to r
  (A has p:r elements) we insert the smallest element from L[i] or R[j] to A[k], and increment (i) or (j) by 1.
  Hence the resulting subarray of A[p:k] will remain sorted.

**Termination:** 
  the function will terminate when k = r+1 so the array of A[p:r] will be sorted.


Code: https://github.com/fayez-als/Algorithms/blob/main/merge_sort%20(1).ipynb


