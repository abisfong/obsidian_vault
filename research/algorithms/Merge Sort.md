```js
function sort(arr, l1, r1, l2, r2) {
	const sortedArr = [];
	const startIdx = l1;

	while (l1 <= r1 && l2 <= r2) 
		sortedArr.push(arr[l1] < arr[l2] ? arr[l1++] : arr[l2++]);
	while (l1 <= r1) sortedArr.push(arr[l1++]);
	while (l2 <= r2) sortedArr.push(arr[l2++]);

	sortedArr.forEach((num, i) => arr[i + startIdx] = num);
}

function mergeSort(arr, l, r) {
	if (l >= r) return;

	const mid = l + Math.floor((r - l) / 2);

	mergeSort(arr, l, mid);
	mergeSort(arr, mid + 1, r);
	sort(arr, l, mid, mid + 1, r);
}
```