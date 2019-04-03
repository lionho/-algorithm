## 배열의 내용 거꾸로 뒤집기

```js
function reverseArray(a) {
	let arr2 = [];
	for (let i = a.length-1; i >= 0; i--){
		arr2.push(a[i]);
	}

	return arr2;
}
```

## 2부터 N까지의 모든 소수의 합 구하기

```js
function run(arr){
	var tempArr = [2];
	var answer = 0;
	
	for(var i = 0; i < arr.length; i++){
		for(var j = 2; j < arr[i]; j++){
			if(arr[i] % j === 0){
				break;
			} else {
				tempArr.push(arr[i]);
				break;
			}
		}
	}

	for(var i = 0; i < tempArr.length; i++){
		answer += tempArr[i];
	}

	return answer;
}
```