
The best approach to Loop through an object in Javascript is to use Object.keys() and Object.values()

Assuming we have a arrayMap object  which contains key-value pairs

var arrayMap ={}

To Get all the Keys in the map object : var keys = Object.keys(arrayMap) ;
To Get all the Values of the Map object : var values = Object.values(arrayMap)

### NB: Object.keys() and Object.values() return arrays . Therefore variable 'keys' and /'values' are arrays containing respectively the keys and the values


