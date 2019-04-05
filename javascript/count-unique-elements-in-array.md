### How Do We Get unique Elements in an Array?

You can create a Map(object) holding the key-value pairs

eg: Let's try and Get Reccuring item  in an array
#### First Approcah Using has 'OwnProperty' Prototype on The array

```javascript

function recurringItem(arr)
{
	//Create an empty object
	let itemMap ={}
	
	for(let item of arr)
	{
		//check if the element is already in the map object
		if(itemMap.hasOwnProperty(item)){
			itemMap[item]++
		}else{
			itemMap[item] = 1
		}
	}
	return itemMap ;

}
```

### Second Approch is to use ES6 reduce Function

```javascript

function reccuringItem(arr){


	let itemMap = arr.reduce((accumulator, item)=>{

		//if the item is already in the accumulator {} increment by 1
		accumulator[item] = accumulator[item] ?  ++accumulator[item]: 1

		return accumulator

	}, {})

	return itemMap
}
```