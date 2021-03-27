# Algorithms


This repository is for demonstrating my algorithm designing skills.




## ----- Sorting Algorithms ------

Merge Sort: Worst Case time complexity theta(nlogn)

**proof of correctness**

**Loop invariant:**
at the start of each iteration the subarray A[p…k-1] contains k-p smallest elements of L and R in sorted order… and L[i] and R[j] contains the smallest elements their arrays that hasn’t been inserted to the sorted subarray of A

**Initialization:** K=P so the subbarray of A[p:K-1] is empty hence sorted.

**Maintenance:** During every iteration from k to r
(A has p:r elements) we insert the smallest element from L[i] or R[j] to A[k], and increment (i) or (j) by 1.
Hence the resulting subarray of A[p:k] will remain sorted.

**Termination:** the function will terminate when k = r+1 so the array of A[p:r] will be sorted.


Code:
```



def merge(arr,start,half,end):
    n1 = half-start+1
    n2 = end-half
    
    L = [None]*(n1+1)
    R = [None]*(n2+1)
    
    for i in range(n1):
        L[i]= arr[start+i]
        
    for j in range(n2):
        R[j] = arr[half+j+1]
        
    L[n1] = float('inf')
    R[n2] = float('inf')
    
    
    
    
    i=0
    j=0
    
    
    
    
    
    for k in range(start,end+1):
        
        if L[i]== float('inf'):
            
            arr[k] = R[j]
            j+=1
        elif R[j] == float('inf'):
            arr[k] = L[i]
            i+=1
            
            
        else:
            if L[i] <= R[j]:
                arr[k] = L[i]
                
                i+=1
            else:
                arr[k] = R[j]
                j+=1
    
    
    
    
 def merge_sort(arr,start,end):
    if start < end:
        
    
        half = (start+(end-1))//2
    
        merge_sort(arr,start,half)
        merge_sort(arr,half+1,end)
    
        merge(arr,start,half,end)






```






