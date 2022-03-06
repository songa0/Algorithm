## 문제  
https://leetcode.com/problems/permutations/  

## 내 풀이  
```javascript
var permute = function(nums) {
    const answer = [];
   
    permutaion([], new Array(nums.length).fill(false));
    
    function permutaion(currentArr, visited){
        if(currentArr.length >= nums.length){
            answer.push(currentArr);
        }
        
        for(let i =0; i<nums.length; i++){
            if(!visited[i]){
                visited[i] = true;
                permutaion([...currentArr,nums[i]], visited);
                visited[i] = false;
            }
        }
        
    }
    
    return answer;
    
};


```
