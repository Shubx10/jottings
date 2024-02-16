## 🚀Implementation of `pow(x, n)`, which calculates x raised to the power n.
```cpp
class Solution {
public:
    double myPow(double x, int n) {
        if(n < 0){
            x = 1 / x;
        }
        long num = labs(n);
        double ans = 1;
        while(num){
            if(num & 1){
                ans *= x;
            }
            x *= x;
            num /= 2;
        }
        return ans;
    }
};
```
