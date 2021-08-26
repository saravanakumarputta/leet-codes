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

## Palindrome number or not

### Example:
`
Input: x = 121
Output: true
`

### Solution

```javascript
const isPalindrome = function(x) {
    const charArray = x.toString().split('');    
    let result = true;
    for(let i=0; i< charArray.length/2; i++){
        if(charArray[i] !== charArray[charArray.length-1-i]){
            result= false;
            break;
        }
    }
    return result;
};
```

## length of last word in a given string

### Example:
`
Input: s = "   fly me   to   the moon  "
Output: 4
Explanation: The last word is "moon" with length 4.
`

### Solution

```javascript
const lengthOfLastWord = function(s) {  
    const words = s.trim().replace(/\s+/g, " ").split(" ");
    return words[words.length-1].length;
};
```

