## 문제  
https://leetcode.com/problems/generate-parentheses

## 내 풀이 
dfs로 풀었다

```javascript
var generateParenthesis = function(n) {
    
    const answer = new Set();
    getParenthesis(0,0,'');
    
    function getParenthesis(left, right, currentVal){
        if(currentVal.length>=n*2){
            answer.add(currentVal);
            return;
        }
        
        if(left>right){
            getParenthesis(left ,right+1, currentVal+')')
        }
        
        if(left<n){
            getParenthesis(left+1, right, currentVal+'(')
        }
    }
    
    return Array.from(answer);
    
};

```
