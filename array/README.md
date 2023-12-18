```
## frequency of each element that occured totally in all subarrays
let’s say A=[1, 2, 3, 4, 5]

All the subarrays are :
Length 1 — → [1], [2], [3], [4], [5]
Length 2 — → [1,2], [2,3], [3,4], [4,5]
Length 3 — → [1,2,3], [2,3,4],[3,4,5]
Length 4 — → [1,2,3,4], [2,3,4,5]
Length 5 — → [1,2,3,4,5]

If we count the number of occurrences of each element. We can see that 1 occurs 4 times, 2 occurs 6 times, 3 occurs 6 times and 4 occurs 4 times. i.e -

1 → 5
2 → 8
3 → 9
4 → 8
5 → 5

That means for an array of fixed length N, the number of occurrences of each element in the sum of all subarrays are fixed and are in some pattern.

frequency of element at ith index = starting at i + ending at i + i in the middle
                                  = (n - i) + (i) + i * (n - i - 1)
                                  = n + i * n - i * i - i
                                  = n * (i + 1) - i * (i + 1)
                                  = (n - i) * (i + 1)

Applications - sum of all subarrays of an array, xor sum of subarrays of an array
```
