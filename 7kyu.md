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