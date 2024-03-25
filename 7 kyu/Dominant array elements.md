## Question
An element in an array is dominant if it is greater than all elements to its right. You will be given an array and your task will be to return a list of all dominant elements. For example:

``` javascript
solve([1,21,4,7,5]) = [21,7,5] because 21, 7 and 5 are greater than elments to their right. 
solve([5,4,3,2,1]) = [5,4,3,2,1]

Notice that the last element is always included. All numbers will be greater than 0.
```
More examples in the test cases.

## Answers

```javascript 
function solve(arr) {
  const res = [];
  for(let i = 0; i< arr.length; i++){
    let count =0;
    for(let j = i+1; j < arr.length; j++){
        if(arr[i] < arr[j]){
            count++ 
        }else{
            continue;
        }
    }
    if(count==0){
        res.push(arr[i]);
    }
  }
  return res.filter((e, i)=> res.indexOf(e)==i);
}
```

```javascript 
function solve(arr){
  return arr.filter((e,i)=> arr.slice(i+1).every(x => x < e));
};
```

```javascript 
function solve(arr){
  return arr.filter((e,i)=> e >Math.max(...arr.slice(i+1)));
};
```