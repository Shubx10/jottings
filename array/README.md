
## 🚀Frequency of each element that occured totally in all subarrays
```
Let’s say A = [1, 2, 3, 4, 5]

All the subarrays are :
Length 1 → [1], [2], [3], [4], [5]
Length 2 → [1,2], [2,3], [3,4], [4,5]
Length 3 → [1,2,3], [2,3,4], [3,4,5]
Length 4 → [1,2,3,4], [2,3,4,5]
Length 5 → [1,2,3,4,5]

If we count the number of occurrences of each element. i.e -

1 → 5
2 → 8
3 → 9
4 → 8
5 → 5

That means for an array of fixed length N, the number of occurrences of each element in the sum of all subarrays are fixed and
are in some pattern.

Frequency of element at ith index = starting at i + ending at i + i in the middle
                                  = (n - i) + (i) + i * (n - i - 1)
                                  = n + i * n - i * i - i
                                  = n * (i + 1) - i * (i + 1)
                                  = (n - i) * (i + 1)

Applications - sum of all subarrays of an array, xor sum of subarrays of an array
```
`Frequency of element at ith index = (n - i) * (i + 1)`
```cpp
//sum of all subarrays of an array
long int SubArraySum(vector<int>& arr, int n){
    long int result = 0;
    for(int i = 0; i < n; i++){
        result += (arr[i] * (i + 1) * (n - i));
    }
    return result;
}
```
```cpp
//Xor of values of all subarrays of an array
class Solution {
  public:
    int gameOfXor(int n, int A[]){
        int res = 0;
        for(int i = 0; i < n; ++i){
            int freq = (i + 1) * (n - i);
            if(freq & 1) res ^= A[i];
        }
        return res;
    }
};
```
