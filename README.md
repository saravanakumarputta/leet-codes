# leet-codes
Leet code Problems in Javascript

## Two Sum

### Example:
`
Input: nums = [2,7,11,15], target = 9
Output: [0,1]
Output: Because nums[0] + nums[1] == 9, we return [0, 1]
`

### Solution

```javascript
const twoSum = function(nums, target) {
   const mappedNumbers = {};
    for(let i=0; i< nums.length;i++){
        if(mappedNumbers[target-nums[i]] !== undefined){
            return [mappedNumbers[target-nums[i]], i];
        }else{
            mappedNumbers[nums[i]]=i;
        }
    }
};
```
