## K번째 수

- 배열 array의 i번째 숫자부터 j번째 숫자까지 자르고 정렬했을 때, k번째에 있는 수 구하기

```js
function solution(array, commands) {
	var answer = [];

	for(var i = 0; i < commands.length; i++){
		var temp = array.slice((commands[i][0])-1,commands[i][1]);

		for(var j = 0; j < temp.length; j++){
			for(var k = 0; k < temp.length; k++) {
				if(temp[k] > temp[k+1]){
					var temp2 = temp[k];
					temp[k] = temp[k+1];
					temp[k+1] = temp2;
				}
			}
		}
		
		answer.push(temp[(commands[i][2])-1]);

	}

	return answer;
}
// array : [1, 5, 2, 6, 3, 7, 4]
// commands : [[2, 5, 3], [4, 4, 1], [1, 7, 3]]
```