## 문제  
Easy 단계  
https://app.codility.com/programmers/trainings/  


## 내 풀이
```javascript

function solution(N) {
    // write your code in JavaScript (Node.js 8.9.4)
    let answer = 0;
    let bin = N.toString(2);
    
   let arr = bin.match(/10+1/);
    answer = arr? arr[0].length-2:0;
  
   while(arr){
       //console.log(bin, arr[0]);
       answer = Math.max(answer, arr[0].length-2);
       bin = bin.slice(arr[0].length-1);
       arr = bin.match(/10+1/);
       //console.log(bin);
   }

    return answer;
}

```
