## 🚀Program to find whether a given number is power of 2
```cpp
// Using log operator
// Time complexity - O(1)
// Space complexity - O(1)
bool isPowerOfTwo(int n){
    if(n == 0)
        return false;
    return (ceil(log2(n)) == floor(log2(n)));
}
```
```cpp
// Using modulo and division operator
// Time complexity - O(log n)
// Space comlexity - O(1)
bool isPowerOfTwo(int n){
    if(n == 0)
        return 0;
    while(n != 1){
        if(n % 2 != 0)
            return 0;
        n = n / 2;
    }
    return 1;
}
```
```cpp
// Using AND operator
// Time complexity - O(1)
// Space complexity - O(1)
bool isPowerOfTwo(int x){
    if(x < 0) return false;
    return x && (!(x & (x - 1)));
}
```
