此题最简单的解法是暴力循环，但是时间复杂度为O(n^2),其实可以利用js对象，实现时间复杂度降低。

```javascript
/**
 * @param {number[]} nums
 * @param {number} target
 * @return {number[]}
 */
var twoSum = function(nums, target) {
    let result = [];
    let obj = {};
    for(let i = 0;i<nums.length;i++){
        if(obj.hasOwnProperty(nums[i])){
            return [obj[nums[i]],i]
        }else{
            obj[target-nums[i]] = i;
        }
    }
};
```