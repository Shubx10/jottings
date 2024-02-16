## 🚀Program to find gcd of two numbers
```cpp
// TC - O(min(a, b))

int gcd(int a, int b){
    int result = min(a, b);
    while (result > 0) {
        if (a % result == 0 && b % result == 0) {
            break;
        }
        result--;
    }
    return result;
}
```
```cpp
// TC - O(min(a, b))

int gcd(int a, int b){
    if (a == 0)
        return b;
    if (b == 0)
        return a;
    if (a == b)
        return a;
    if (a > b)
        return gcd(a - b, b);
    return gcd(a, b - a);
}
```
```cpp
// TC - O(min(a, b))

int gcd(int a, int b){
    if (a == 0)
        return b;
    if (b == 0)
        return a;
    if (a == b)
        return a;
    if (a > b) {
        if (a % b == 0)
            return b;
        return gcd(a - b, b);
    }
    if (b % a == 0)
        return a;
    return gcd(a, b - a);
}
```
```cpp
// TC - O(log(min(a, b)))

int gcd(int a, int b){
    return b == 0 ? a : gcd(b, a % b);    
}
```
```cpp
// TC - O(log(min(a, b)))

int gcd(int a, int b){
    while (a > 0 && b > 0) {
        if (a > b) {
            a = a % b;
        }
        else {
            b = b % a;
        }
    }
    if (a == 0) {
        return b;
    }
    return a;
}
```
```cpp
// TC - O(log(min(a, b)))

int gcd(int a, int b){
    return __gcd(a, b);    
}
```
