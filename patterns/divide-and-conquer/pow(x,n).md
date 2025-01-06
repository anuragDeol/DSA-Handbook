
### [Pow(x, n)](https://leetcode.com/problems/powx-n/description/)

### Intuition (with Time and Space Analysis)
1. **Brute Force**: Simply multiply x by itself with n times.
> `TC: O(n)`

2. **Optimal**: For optimizing we can think, that there can be 2 cases:
- if n is odd, in that case, we can simply write (x) * (x^n-1)
- if n is even, we can write (x^2)^(n/2)
  As we can see `n -> n/2`, hence making it log(n) TC
> `TC: log(n)`

### Key Points
- Handling cases where n < 0 is simple. Find answer assuming n positive. When ans found, just do 1.0/ans
- Important edge case is, if n is Integer.MIN_VALUE, then doing Math.abs(n) wil not give us Integer.MAX_VALUE, but Integer.MIN_VALUE, cause integer range from `[-2^31, (2^31) - 1]`
- Hence what worked for me was, instead of using int n, use long