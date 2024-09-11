# :dart: YYYYMMDD Daily LeetCode Practice

## [704. 二分查找 (Binary Search)](https://leetcode.com/problems/binary-search/)
### :computer: Difficulty: [Easy, Medium, Hard]

### Resources
- Problem Link: [LeetCode](https://leetcode.com/problems/binary-search/)
- Solution Explanation: [代码随想录 (ProgrammerCarl)](https://programmercarl.com/)
- Video Explanation: 
  - [手把手带你拆出正确的二分法 | 二分查找法 | 二分搜索法 1](https://www.bilibili.com/)
  - [手把手带你拆出正确的二分法 | 二分查找法 | 二分搜索法 2](https://www.bilibili.com/)
  - [LeetCode: 704. 二分查找_哔哩哔哩_bilibili](https://www.bilibili.com/)

---

## Personal Preferred Method

### Explanation


1. **While Loop Condition**: 

2. **Middle Element Check**:

### Code Implementation

#### Template Code

```cpp
// JavaScript Example
function binarySearch(nums, target) {
    let left = 0;
    let right = nums.length - 1;

    while (left <= right) {
        const middle = Math.floor((left + right) / 2);
        if (nums[middle] === target) {
            return middle;
        } else if (nums[middle] < target) {
            left = middle + 1;
        } else {
            right = middle - 1;
        }
    }
    return -1;
}
