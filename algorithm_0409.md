## *찍기

```js
function star(n){
    let answer = "";
    for(let i = 0; i < n; i++){
        let answer2 = "";
        let answer3 = "";
        for(let j = n; j > i; j--){
            answer2 += " ";  
        }
        for(let k = 0; k <= i; k++){
            answer3 += "*";       
        }

        answer += answer2;
        answer += answer3;
        answer += "\n";
    }

    return answer;
}

// n : 5
// commands : 
//     *
//    **
//   ***
//  ****
// *****
```

## 이상한 문자 만들기

- s는 한 개 이상의 단어로 구성, 
- 각 단어는 하나 이상의 공백문자로 구분되어 있음. 각 단어의 짝수번째 알파벳은 대문자로, 홀수번째 알파벳은 소문자로 바꾼 문자열을 리턴하는 함수 구현

```js
function solution(s) {
    var answer = s.split(" ");
	var arr1 = [];
	var result = [];

	for(var i=0; i<answer.length; i++){
		arr1.push(answer[i].split(""));
		for(var j=0; j<arr1[i].length; j++){
			if(j%2 === 0){
				result += arr1[i][j].toUpperCase();
			}else{
				result += arr1[i][j].toLowerCase();
			}
		}
		result += " ";
	
	}
	return result.slice(0, result.length-1);
}

//s: "try hello world"
//command : "TrY HeLlO WoRlD"
```
