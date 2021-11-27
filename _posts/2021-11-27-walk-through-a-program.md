---
title: "Thirteenth blog"
date: 2021-11-27
categories:
---

## Today I will explain the colour sort program


```
let arr = [0, 1, 1, 0, 0, 1, 0]

let j=arr.length -1;

for(let i = 0 ; i< arr.length && i<j ; i++) {
	if (arr[i] === 1) {
		while(arr[j] === 1 && i<j) {
			j--;
		}
		const temp = arr[i];
		arr[i] = arr[j];
		arr[j] = temp;
		j--;
	}
}

console.log(arr);
```

This program gives you a sorted array that consists of only 0's and 1's. Here we don't need to go with the normal sorting approach because it has values 0 & 1 only. We have one of the best approaches to do this takes O(n) complexity. This program has written in JavaScript.

Start from both ends and come together. A left pointer moves towards the right when it has zero(0). A right pointer moves towards the left when it has one(1). Move them until both pointers cross together. Here the left pointer is 'i', and the right pointer is 'j'. Whenever both pointers pointing other values, then swap them and make a move. Do this till both pointers cross together. That's it. We have it in sorted order.
