## 문제  
https://leetcode.com/problems/combination-sum/  

## 내 풀이
```javascript
var combinationSum = function(candidates, target) {
    let rtn = [];    
    
    let getComb = (idx, crntCnt, crntArr) =>{
        
        if(crntCnt-candidates[idx]===0){
            rtn.push([...crntArr,candidates[idx]]);
        }else if(crntCnt-candidates[idx]>0){
            for(let i = idx; i<candidates.length; i++){
                crntArr.push(candidates[idx]);
                getComb(i, crntCnt-candidates[idx], crntArr);
                crntArr.pop();
            }
        }
    }
    
    for(let i =0; i<candidates.length; i++){
        getComb(i, target, []);
    }
    
    return rtn;
};



```
