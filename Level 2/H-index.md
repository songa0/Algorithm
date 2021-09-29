## 문제
https://programmers.co.kr/learn/courses/30/lessons/42747  

## 내 풀이  
```javascript
function solution(citations) {
    var answer = 0;
    citations.sort(function(a,b){return a-b});
  
    let cIdx = 0;
    for(let i = 0; i<=citations[citations.length-1]; i++){
        while(citations[cIdx]<i){cIdx++;}
        if(citations.length-cIdx>=i)   answer = i;
        
        
    }
    return answer;
}


```

## 주의할 점  
js에서 sort 함수는 아스키코드 순으로 정렬하기 때문에 숫자를 정렬할때는 comparator 함수를 적어주어야한다.  
