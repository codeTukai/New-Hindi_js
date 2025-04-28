# project on DOM

## project link 
[Click here](https://stackblitz.com/edit/dom-project-chaiaurcode?file=1-colorChanger%2Findex.html)

# Solution Code

## project 1 on Switching Colors

~~~ javascript 
const buttons = document.querySelectorAll('.button');
const body = document.querySelector('body');

buttons.forEach(function(button){
 console.log(button);
 button.addEventListener('click', function(e){
   console.log(e);
   console.log(e.target);

   if (e.target.id === 'grey'){
     body.style.backgroundColor = e.target.id;
   }

   if (e.target.id === 'white'){
    body.style.backgroundColor = e.target.id;
  }

  if (e.target.id === 'blue'){
    body.style.backgroundColor = e.target.id;
  }
  if (e.target.id === 'yellow'){
    body.style.backgroundColor = e.target.id; 
  }
  
 });

});

~~~

# Project 2 on EMI Calculation

# Solution Code

~~~ in Javascript
const form = document.querySelector('form');
form.addEventListener('submit', function (e) {
  e.preventDefault();

  const height = parseInt(document.querySelector('#height').value);
  const weight = parseInt(document.querySelector('#weight').value);
  const results = document.querySelector('#results');

  if (height === '' || height < 0 || isNaN(height)) {
    results.innerHTML = `please give me a valid height ${height}`;
  } else if (weight === '' || weight < 0 || isNaN(weight)) {
    results.innerHTML = `please give me a valid weight ${weight}`;
  } else {
    const BMI = (weight / ((height * height) / 10000)).toFixed(2);
    // show the result
    let category = '';

    if (BMI < 18.6) {
      category = "Underrated";
    } else if (BMI >= 18.6 && BMI <= 24.9) {
      category = "Normal";
    } else {
      category = "Overrated";
    }

    results.innerHTML = `<span>Your BMI is ${BMI} :- ${category}</span>`;
  }
   
});


~~~

# project 3 on Digital Clock

# solution code here

~~~ Javascript 
const clock = document.getElementById('clock');

      setInterval(function () {
        let date = new Date();
        clock.innerHTML = date.toLocaleTimeString();
      }, 1000);

~~~