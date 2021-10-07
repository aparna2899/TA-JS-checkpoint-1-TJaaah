1. Using loops take 10 inputs from user and find the average of all the numbers.

```js
let sum = 0;
for (i = 1; i <= 10; i++) {
  let input = +prompt(`Enter input${i}`);
  sum += input;
}
let average = sum / 10;
alert(average);
```

2. What will be the output of the code below

```js
let i = 0;
while (i < 3) {
  println("hi");
  i++;
}
```

println is not defined.

3. Write a function named `getEvenSum` that accepts a parameter `max`. Return the sum of all even numbers. The value of max should default to 10.

```js
let sum = 0;
function getEvenSum(max = 10) {
  for (i = 2; i <= max; i += 2) {
    sum = i * (i + 1);
  }
  return sum;
}
```

4. Write a function named `getOddSum` that accepts a parameter `max`. Return the sum of all odd numbers. The value of max should default to 10.

```js
let sum = 0;
function getOddSum(max = 10) {
  for (i = 1; i <= max; i += 2) {
    sum = (i + 1) * (i + 1);
  }
  return sum;
}
```

5. Write a function named `getProductOfDigits` that accepts a parameter `num`. It returns the product of all the digits in the number.

- If the input value is less than 0 return `not a valid input`
- For example if the input is `123` output should be `6`.

```js
let lastDigit,
  product = 1;
function getProductOfDigits(num) {
  if (num == 0) return `not a valid input`;
  else {
    while (num != 0) {
      lastDigit = num % 10;
      product *= lastDigit;
      num = Math.floor(num / 10);
    }
  }
  return product;
}
```

6. What will be the output of the following code below in multiple conditions? Explain with reason?

```js
function check(num) {
  if (num > 5) {
    return "Bigger than 5";
  }

  if (num < 5) {
    return "Smaller than 5";
  }

  return num;
}

check(10); // 'Bigger than 5'
check(1); // 'Smaller than 5'
check(5); // 5
//If we require code to run only when the statement returns true and do nothing else if false then an else statement is not needed.
```

7. What will be the output of the following code given below? Explain the reason?

```js
function getOutput(name) {
  if (name === "Arya") return "You are arya";
  if (name === "John") return "You are john";
  return "Who are you";
}

getOutput("Arya"); // 'You are arya'
getOutput("John"); // 'You are john'
getOutput(); // 'Who are you'
```

8. What will be the output of the following code given below? Explain the reason?

```js
function getOutput(name) {
  if (name === "Arya") console.log("You are arya");
  if (name === "John") console.log("You are john");
  return "Who are you";
}

getOutput("Arya"); // You are arya 'Who are you'
getOutput("John"); // You are john 'Who are you'
getOutput(); // 'Who are you'
```

9. Can a function have multiple return statement? Give one example if possible and explain the reason.

A function can have multiple return statement but only with different conditions.

function check(num) {
if (num > 5) {
return 'Bigger than 5';
}
if (num < 5) {
return 'Smaller than 5';
}
return num;
}

10. What is the difference between `for` loop and `while` loop. What are the different place you can use them? Explain with example.

We use 'for' loop when we know the number of iterations and the 'while' loop used when the number of iteration are not exactly known.

for(i=1; i<=10; i++){
sum += i;
}
Here we know that loop will run 10 times.

while (i < max) {
alert(i)
i += 2;
}
Here we doesn't know the number of iterations as the value of 'max' will be given by user.
