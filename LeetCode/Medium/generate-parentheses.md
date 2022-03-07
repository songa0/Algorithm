## 문제  
https://leetcode.com/problems/generate-parentheses

## 내 풀이 (다시 풀어야함)

```javascript

var generateParenthesis = function(n) {
    
    const answer = new Set();
    getParenthesis('', 0);
    
    function getParenthesis(crntVal, num){
        if(num>=n) {
            answer.add(crntVal);
            return;
        }
        
        getParenthesis(crntVal+'()', num+1);
        getParenthesis('()'+crntVal, num+1);
        getParenthesis('('+crntVal+')', num+1);
    }
    
    return Array.from(answer);
    
};




```
