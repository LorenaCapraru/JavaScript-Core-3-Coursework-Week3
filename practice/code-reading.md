# Code reading

## Question 1

Take a look at the following code:

```
1    let x = 1;
2    function f1()
3    {
4        let x = 2;
5        console.log(x);
6    }
7    console.log(x);
```

Explain why line 4 and line 6 output different numbers.
  Inside the function a NEW variable x is declared and it loses its property outside the function as it is a function variable.
  Line no 1 declared a GLOBAL variable which is console logged at line no 14. Hence the results of the code is -->1

## Question 2

Take a look at the following code:

```
let x = 10

function f1()
{
    console.log(x)
    let y = 20
}

console.log(f1())
console.log(y)
```

What will be the output of this code. Explain your answer in 50 words or less.
'undefined' as the variable y is a FUNCTION variable and is called outside the function, which will result in 'undefined'. In order to work the solution will be to console log the y var inside the function body and when the function is called the variable will be console.logged, OR to be declared as a GLOBAL variable outside the function's body and it would display 20 by keeping the rest as it is.

## Question 3

Take a look at the following code:

```
const x = 9;

function f1(val) {
  val = val + 1;
  return val;
}

f1(x);
console.log(x);

const y = { x: 9 };

function f2(val) {
  val.x = val.x + 1;
  return val;
}

f2(y);
console.log(y);
```

What will be the output of this code. Explain your answer in 50 words or less.
  console.log(x)-> will return 9, the value of the GLOBAL variable
  console.log(y)-> will return {x:10} at it increases the value of key 'x' by one. the function f1(x) and f2(x) have no outputs as they should be CONSOLE.LOGGED considering that returns a value
