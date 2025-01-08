
### [Majority Element II](https://leetcode.com/problems/majority-element-ii/description/)

### Intuition (with Time and Space Analysis)
1. **Brute Force**: Simply iterate over array and count frequency of each element.
> `TC: O(n^2)`
> `SC: O(1)`

2. **Optimised**: Use Hashmap to store frequency of each element.
> `TC: O(n)`
> `SC: O(n)`

3. **Optimal**:  Extended Boyer-Moore Voting Algorithm. Since we need elements appearing > n/3 times, there can be at most 2 such elements. Use 2 candidates and their counts.
> `TC: O(n)`
> `SC: O(1)`

### Key Points
- Moore's Voting Algorithm is a linear time solution that works for any majority element.