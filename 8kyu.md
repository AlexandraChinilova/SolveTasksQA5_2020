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