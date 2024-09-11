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

设定定义 target 是在一个在左闭右闭的区间里，也就是[left, right] (这个很重要非常重要)。
区间的定义决定了二分法的代码应该如何写，因为决定了区间的边界处理方式：

1. **While Loop Condition**: 
   - `while (left <= right)` 要使用 <=, 因为 left == right 是有意义的，所以使用 <=

2. **Middle Element Check**:
   - If `nums[middle] > target`:
     - Update `right` to `middle - 1`, 因为当前这个 `nums[middle]` 一定不是 target, 那么接下来要查找的左区间结束下标位置就是 `middle - 1`

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
