* Calculate BMI
```javascript
function bmi(weight, height) {
  let res = (weight/(height**2));
  if (res <= 18.5) {return "Underweight";}
  else if (res <= 25) {return "Normal";}
  else if (res <= 30) {return "Overweight";}
  else if (res > 30){return "Obese";}
}
```
* 101 Dalmatians - squash the bugs, not the dogs!
```javascript
function howManyDalmatians(number){  
  const dogs = ["Hardly any", "More than a handful!", 
                "Woah that's a lot of dogs!", "101 DALMATIANS!!!"];  
  
return number <= 10 ? dogs[0] 
                    : number <= 50 ? dogs[1]
                      : number <= 100 ? dogs[2]
                      : dogs[3]
}
```
* Basic Mathematical Operations
```javascript
function basicOp(operation, v1, v2){
let res = 0;
 switch (operation){
   case '+' : res = v1 + v2; break;
   case '-' : res = v1 - v2; break;
   case '*' : res = v1 * v2; break;
   case '/' : res = v1 / v2; break;
 }
 return res
}
```
* Power
```javascript
function numberToPower(number, power){
if (power == 0){return 1}
let i = 1, res = 1;
  do{
   res *= number;
   i++
  }
  while (i <= power)
  return res
}
```
* Is integer safe to use?
```javascript
//Выходя за пределы, мы получаем одну из самых распространенных ошибок
// при работе с числами - потерю точности.
// Чтобы убедиться, что целое число входит в "безопасный диапазон",
//необходимо использовать метод
function SafeInteger(n){
 return Number.isSafeInteger(n)
}
```
* Is it a palindrome?
```javascript
function isPalindrome(x) {
if (x.length <= 1){return true}
  x = x.toUpperCase();
  let a = x.length-1, res = false;
  for (let i=0; i < x.length/2; i++){
   if (x[i] == x[a]){
   res = true;
   }
   else {return false}
   a--;
  }
  return res
}
```
* Squash the bugs
```javascript
function findLongest(str){
var spl = str.split(" ");
var longest = 0;  
  for (var i = 0; i < spl.length; i++){
    if (spl[i].length > longest){
      longest = spl[i].length;
    }
  }
    return longest
}
```
* Beginner - Reduce but Grow
```javascript
function grow(x){
return x.reduce((a,b) => a*b)
}
```