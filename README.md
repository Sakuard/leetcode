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

13. Roman to Integer
```
var romanToInt = function(s) {
    const intMap = {
        "I": 1,
        "V": 5,
        "X": 10,
        "L": 50,
        "C": 100,
        "D": 500,
        "M": 1000
    };
    let result = 0;
    for (let i=0; i<s.length; i++) {
        if (intMap[s[i]] < intMap[s[i+1]]) {
            result -= intMap[s[i]]
        } else {
            result += intMap[s[i]]
        }
    }
}
```