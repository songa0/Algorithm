## 문제  
https://leetcode.com/problems/subsets/

## 내 풀이  

```javascript
var subsets = function(nums) {
    const answer = [[]];
    
    getSubsets(nums, -1, [], answer);
    
    return answer;
};    
        
 function getSubsets (arr, idx, currentVal,answer){
    
     for(let i = idx+1; i<arr.length; i++){       
         currentVal.push(arr[i]);
         answer.push([...currentVal]);
         getSubsets(arr, i, currentVal, answer);
         currentVal.pop();  
     }
 }

```
