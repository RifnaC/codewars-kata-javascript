## Question
For every good kata idea there seem to be quite a few bad ones!

In this kata you need to check the provided array (x) for good ideas 'good' and bad ideas 'bad'. If there are one or two good ideas, return 'Publish!', if there are more than 2 return 'I smell a series!'. If there are no good ideas, as is often the case, return 'Fail!'.

## Answer
```javascript
function well(x){
  const c = x.filter(e=> e=='good');
  return  c.length==0 ? 'Fail!' :c.length==1|| c.length==2 ? "Publish!": 'I smell a series!';
}```