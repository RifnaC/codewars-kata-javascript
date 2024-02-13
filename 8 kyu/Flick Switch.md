## Ouestion
### Task
Create a function that always returns True/true for every item in a given list.
However, if an element is the word 'flick', switch to always returning the opposite boolean value.

### Examples
['codewars', 'flick', 'code', 'wars'] ➞ [True, False, False, False]

['flick', 'chocolate', 'adventure', 'sunshine'] ➞ [False, False, False, False]

['bicycle', 'jarmony', 'flick', 'sheep', 'flick'] ➞ [True, True, False, False, True]
### Notes
"flick" will always be given in lowercase.
A list may contain multiple flicks.
Switch the boolean value on the same element as the flick itself.

## Answer
1. Using new array :
   
   `function flickSwitch(arr){
    const rs = []
    let on = true;
    arr.map(e=> {
     if( e==="flick"){
       on = !on ;
       rs.push(on)
     } else{
       rs.push(on);
     }
      return on
    })
    return rs;
   }`
2. Without using new array

   `function flickSwitch(arr){
     let on = true;
      return arr.map(e => {return e ==="flick" ? on = !on : on});
   }`
   
