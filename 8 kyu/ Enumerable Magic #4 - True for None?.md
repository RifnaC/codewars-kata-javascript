## Quesitons
Create a method none? (JS none) that accepts an array and a block (JS: a function), and returns true if the block (/function) returns true for none of the items in the array. An empty list should return true.

## Answer
``` javascript 
function none(arr, fun){
    for(const i in arr){
        if(fun(arr[i])){
            return false
        }
    }
    return true
}
```

``` javascript
function none(arr, fun){
  return !arr.some(fun);
}
```