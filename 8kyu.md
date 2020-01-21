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