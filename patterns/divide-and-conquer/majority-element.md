
### [Majority Element](https://leetcode.com/problems/majority-element/description/)

### Intuition (with Time and Space Analysis)
1. **Brute Force**: Simply iterate over array and count frequency of each element.
> `TC: O(n^2)`
> `SC: O(1)`

2. **Optimised (Better)**: Use Hashmap to store frequency of each element.
> `TC: O(n)`
> `SC: O(n)`

3. **Optimised (Better-II)**: Sort array and return middle element (since if it is majority element, it will be in middle).
> `TC: O(logn)`
> `SC: O(1)`

4. **Optimal**: Moore's Voting Algorithm. Iterate through the array while keeping track of a potential majority element and its count - when encountering the same element, increment count; when different, decrement count; if count reaches 0, set the current element as the new candidate. This works because a true majority element (>n/2 occurrences) will always survive the "neutralization" of different elements.
> `TC: O(n)`
> `SC: O(1)`

### Key Points
- Moore's Voting Algorithm is a linear time solution that works for any majority element.