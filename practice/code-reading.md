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
Answer: Line 4 is within the function scope, hence x = 2.
Line 6 falls within the block scope, hence x = 1

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
Answer: the console.log of the fucntion result to x = 10, as the 'let' variable can be read within a block scope.
As y is defined within the function only and console.log(y) is defined outside of the function, it cannot read the value of y inside the function.

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
Answer: x = 9 is declared right at the beginning and never used in the f1 function, hence the console.log(x) reads x as 9 as its blocked scoped.
