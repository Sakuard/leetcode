1. TwoSum

```node.js=
var twoSum = function(nums, target) {
    const numMap = new Map()
    for (let i=0; i<nums.length; i++) {
        for (let j=1; j<nums.length-1; i++) {
          if (nums[i]+nums[j] === target) return [i, j]
        }
    }
};

var twoSum = function(nums, target) {
    const numMap = new Map()
    for (let i=0; i<nums.length; i++) {
        let diff = target-nums[i]
        
        if (numMap.has(diff))
            return [numMap.get(diff), i]

        numMap.set(nums[i], i)
    }
};
```
