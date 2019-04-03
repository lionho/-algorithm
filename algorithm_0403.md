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