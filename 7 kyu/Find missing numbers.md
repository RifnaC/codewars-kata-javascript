## Question
You will get an array of numbers.
Every preceding number is smaller than the one following it.
Some numbers will be missing, for instance:

```javascript
[-3,-2,1,5] //missing numbers are: -1,0,2,3,4
```
Your task is to return an array of those missing numbers:
```javascript
[-1,0,2,3,4]
```

##Answers
```javascript 
function findMissingNumbers(arr){
  const start = Math.min(...arr);
  const end = Math.max(...arr);
  const org = [];
  for(let i = start; i<end; i++){
      if(!arr.includes(i)){
         org.push(i)
      }
  }
  return org;
}
```