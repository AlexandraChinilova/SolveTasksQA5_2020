* Sum of angles
```javascript
function angle(n) {
  return 180*(n-2)
}
```
* How many times should I go?
```javascript
function howManyTimes(anPr, indPr) {
 return Math.ceil(anPr/indPr)
}
```
* Return the closest number multiple of 10
```javascript
const closestMultiple10 = num => {
  return Math.round(num/10)*10;
}
```
* Is this a triangle?
```javascript
function isTriangle(a,b,c){
if (a < b+c && b < a+c && c < a+b){return true};
return false;
}
```
* Calculate Two People's Individual Ages
```javascript
function getAges(sum,diff){
if (sum < 0 || diff < 0){return null}
let ages = [];
let p1 = (sum - diff)/2;
let p2 = sum - p1
if (p1 >= 0 && p2 >= 0){
ages.push(p2);
ages.push(p1);
return ages
}
return null
}
```
* Power of two
```javascript
function isPowerOfTwo(n){
if (n == 1){return true};
if (n == 0){return false};
  while (n >= 2){
   n = n/2;
  }
  return n > 1 ? false : true;
}
```
* The wheat/rice and chessboard problem
```javascript
function squaresNeeded(grains){
  console.log(grains)
  let sum = 0, z = 1, kl = 0
  while (sum < grains){
    sum += z;
    z *=2;
    kl++
  }
  return kl
}
```
* Sum of the first nth term of Series
```javascript
function SeriesSum(n){
 let a = 1, b = 1;
 let sum = 0;
   for (let i = 0; i < n; i++){
    sum += a/b
    b +=3
   }
  return sum.toFixed(2)
}
```
* Filter the number
```javascript
var FilterString = function(value) {
let str = '';
  for (let i=0; i < value.length; i++){
    if (isNaN(value[i]) == false){
      str += value[i]
    }
  }
  return +str
}
```
* Lottery machine
```javascript
function lottery(str){
let res = str.match(/\d/g)
  if (res == null){return 'One more run!'}
let fres = [res[0]]
  for (let i = 1; i < res.length; i++){
    if (fres.every(e => res[i] != e)){
      fres.push(res[i])
    }
  }
 return fres.join('')
}
```
* Jumping Number (Special Numbers Series #4)
```javascript
function jumpingNumber(n){
  if (n < 11){return 'Jumping!!'}
    if (n > 10){
    let arr = n.toString().split('')
      for (let i=0; i < arr.length-1; i++){
        if (Math.abs(arr[i+1]-arr[i]) > 1 || arr[i+1]-arr[i] == 0){
        return 'Not!!'
        }
     }
     return 'Jumping!!'
    }
}
```
* Form The Minimum
```javascript
function minValue(values){
 values.sort()
 let arr = [values[0]], ch = values[0];
 for (let i=1; i < values.length; i++){
  if (values[i] != ch){
    arr.push(values[i]);
    ch = values[i];
  }
 }
 ch = '';
 for (let j = 0; j < arr.length; j++){
   ch += arr[j];
 }
 return +ch
}
```
* London CityHacker
```javascript
function londonCityHacker(j) {
let m = 2.4, b = 1.5, p = 0;
  for (let i=0; i < j.length; i++){
    if (typeof j[i] == 'string'){p += m}
    if (typeof j[i] == 'number'){
      p += b;
      if (typeof j[i+1] == 'number'){
        i++
      }
    }
  }
return `£${p.toFixed(2)}`
}
```
* Tail Swap
```javascript
function tailSwap(arr){
let res = [];
for (let i=0, j=arr.length-1; i < arr.length; i++, j--){
let i1 = arr[i].search(/:/), i2 = arr[j].search(/:/)
 res.push(arr[i].substring(0, i1) + arr[j].slice(i2))
}
  return res;
}
```
* Pandemia
```javascript
function infected(s){
let arr = s.split('X'), people = 0, inf = 0;
for (let i=0; i < s.length; i++){
  if (s[i] == 0 || s[i] == 1){
  people++
  }
}
for (let j=0; j < arr.length; j++){
  if(arr[j].match(/1/) != null){
    for (let el=0; el < arr[j].length; el++){
    inf++
    }
  }
}
if (people == 0){return 0}
  return inf/people*100;
}
```
* What's my golf score?
```javascript
function golfScoreCalculator(parList, scoreList){
let res = 0
  for (let i=0; i < parList.length; i++){
    res += scoreList[i] - parList[i];
  }
return res
}
```
* Scrabble Score
```javascript
function scrabbleScore(str){
str = str.toLowerCase()
console.log(str)
let res = 0
  if (str == ''){return 0}
 if (str.match(/[ateoluirsn]/g)){
     res += str.match(/[ateoluirsn]/g).length
   }
   if (str.match(/[dg]/g)){
     res += (2*str.match(/[dg]/g).length)
   }
   if (str.match(/[bcmp]/g)){
     res += (3*str.match(/[bcmp]/g).length)
   }
   if (str.match(/[fhvwy]/g)){
     res += (4*str.match(/[fhvwy]/g).length)
   }
   if (str.match(/[k]/g)){
     res += (5*str.match(/[k]/g).length)
   }
   if (str.match(/[jx]/g)){
     res += (8*str.match(/[jx]/g).length)
   }
   if (str.match(/[qz]/g)){
     res += (10*str.match(/[qz]/g).length)
   }
  return res
}
```