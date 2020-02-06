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
* Make the Deadfish swim
```javascript
function parse(data){
let res = 0;
let arr = [];
 for (let i=0; i < data.length; i++){
  if (data[i] == 'i'){ res += 1}
  if (data[i] == 'd'){ res -= 1}
  if (data[i] == 's'){ res *= res}
  if (data[i] == 'o'){ arr.push(res)}
 }
 return arr
}
```
* Row of the odd triangle
```javascript
function oddRow(n) {
let res = [];
let count = n**2 - (n-1);
for (i = 0; i < n; i++){
res.push(count);
count +=2
}
  return res
}
```
* Pokemon Damage Calculator
```javascript
function calculateDamage(yT, oT, attack, defense){
let dmg = 0, eff = 1;
  if (yT == 'fire' && oT == 'grass'
   || yT == 'grass' && oT == 'water'
   || yT == 'water' && oT == 'fire'
   || yT == 'electric' && oT == 'water'){
    eff = 2;
  }
    else if (yT == oT
          || yT == 'fire' && oT == 'water'
          || yT == 'grass' && oT == 'fire'
          || yT == 'water' && oT == 'grass'
          || yT == 'water' && oT == 'electric'){
          eff = 0.5;
    }
return dmg = 50 * (attack/defense)*eff;
}
```
* Sums of Parts
```javascript
function partsSums(ls){
if (ls.length == 0){return [0]}
let sum = ls.slice();
sum.push(0);
 for (let i = ls.length; i >= 1; i--){
   ls.shift()
   for (let l = 0; l < ls.length; l++){
    sum[l] += ls[l]
   }
 }
return sum
}
// не работает для длинных массивов
// вторая версия для длинных
function partsSums(ls){
let sum = [];
let chisl = ls.reduce((a, b) => a + b, 0)
sum.push(chisl)
  for (let i = 0; i < ls.length; i++){
   chisl -= ls[i];
   sum.push(chisl)
  }
return sum
}
```
* Split Strings
```javascript
function solution(str){
 let res = [];
 if (str.length%2 === 0){
   for (let i=0; i < str.length; i+=2){
     res.push(str[i]+str[i+1]);
   }
  }
  if (str.length%2 > 0) {
    for (let i=0; i < str.length-1; i+=2){
     res.push(str[i]+str[i+1])
   }
   res.push(str[str.length-1] + '_')
  }
 return res
}
```
* Create Phone Number
```javascript
function createPhoneNumber(numb){
let cod = '', thr = '', four = '';
  for (let i = 0; i < numb.length; i++){
    i < 3 ? cod += numb[i] : i < 6 ? thr += numb[i] : four += numb[i]
  }
  return `(${cod}) ${thr}-${four}`
}
```