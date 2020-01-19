* Find the Mine!
```javascript
function mineLocation(field){
let res = [];
let pos1 = 0;
let pos2 = 0;
  for (let i=0; i < field.length; i++){
    if (field[i].includes(1) == true){
      pos1 = i;
      pos2 = field[i].indexOf(1)
    }
  }
res.push(pos1);
res.push(pos2);
return res
}
```
* Casino chips
```javascript
function solve(arr){
let pile1 = 0;
let pile2 = 0;
let d = 0;
for (let i=1; arr.length > 1; i++){
  if (arr[0] == 0){
    pile1 = Math.min(arr[1], arr[2]);
    arr[arr.indexOf(pile1)] -= 1;
    pile2 = Math.max(arr[1], arr[2]);
    arr[arr.indexOf(pile2)] -= 1;
      if (arr[1] == 0 || arr[2] == 0){arr = ['end']}
  }
  if (arr[1] == 0){
    pile1 = Math.min(arr[0], arr[2]);
    arr[arr.indexOf(pile1)] -= 1;
    pile2 = Math.max(arr[0], arr[2]);
    arr[arr.indexOf(pile2)] -= 1;
      if (arr[0] == 0 || arr[2] == 0){arr = ['end']}
  }
  if (arr[2] == 0){
    pile1 = Math.min(arr[0], arr[1]);
    arr[arr.indexOf(pile1)] -= 1;
    pile2 = Math.max(arr[0], arr[1]);
    arr[arr.indexOf(pile2)] -= 1;
      if (arr[0] == 0 || arr[1] == 0){arr = ['end']}
  }
  if (arr[0] > 0 && arr[1] > 0 && arr[2] > 0){
    pile1 = Math.min(...arr);
    arr[arr.indexOf(pile1)] -= 1;
    pile2 = Math.max(...arr);
    arr[arr.indexOf(pile2)] -= 1;
      if (arr[0]==0 && arr[1]==0 || arr[1]==0 && arr[2]==0 || arr[0]==0 && arr[2]==0){arr = ['end']}
  }
d = i;
}
  return d
}
```