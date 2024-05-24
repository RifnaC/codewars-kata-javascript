## Question

Given a number n, draw stairs using the letter "I", n tall and n wide, with the tallest in the top left.

For example n = 3 result in:

```javascript  "I\n I\n  I"```
or printed:
```javascript 
I
 I
  I
```

Another example, a 7-step stairs should be drawn like this:
```javascript
I
 I
  I
   I
    I
     I
      I
```

## Answer
```javascript
function drawStairs(n) {
  let ans = ""
  for(let i = 0; i < n; i++){
    for(let j = 0; j <= i; j++){
      i===j ? ans+="I" : ans+=" ";
    }
    if(i!= n-1){
        ans+="\n";
    }
  }
  return ans
}
```