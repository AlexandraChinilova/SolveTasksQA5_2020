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