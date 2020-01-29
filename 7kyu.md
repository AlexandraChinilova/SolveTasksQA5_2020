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