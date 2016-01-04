## Resources
* http://www.sitepoint.com/introduction-functional-javascript/
* http://scott.sauyet.com/Javascript/Talk/FunctionalProgramming/#slide-0
* https://www.youtube.com/watch?v=L7b7AW14rYE (slides)
* https://www.youtube.com/playlist?list=PL0zVEGEvSaeEd9hlmCXrk5yUyqUag-n84
* https://en.wikipedia.org/wiki/Functional_programming

# Functional Programming (from wiki)
**functional programming** is a programming paradigm — a style of building the structure and elements of computer programs—that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data. It is a declarative programming paradigm, which means programming is done with expressions. In functional code, the output value of a function depends only on the arguments that are input to the function, so calling a function f twice with the same value for an argument x will produce the same result f(x) each time. Eliminating side effects, i.e. changes in state that do not depend on the function inputs, can make it much easier to understand and predict the behavior of a program, which is one of the key motivations for the development of functional programming.

## Concepts
### First-class and higher-order functions
**Higher-order functions** are functions that can either take other functions as arguments or return them as results.

Higher-order functions are closely related to first-class functions in that higher-order functions and first-class functions both allow functions as arguments and results of other functions. The distinction between the two is subtle: "higher-order" describes a mathematical concept of functions that operate on other functions, while "first-class" is a computer science term that describes programming language entities that have no restriction on their use (thus first-class functions can appear anywhere in the program that other first-class entities like numbers can, including as arguments to other functions and as their return values).

Higher-order functions enable **currying**, a technique in which a function is applied to its arguments one at a time, with each application returning a new function that accepts the next argument.

### Recursion
**Recursive functions** invoke themselves, allowing an operation to be performed over and over until the base case is reached

### Pure functions
**Purely functional** functions (or expressions) have no side effects (memory or I/O).
* If a pure function is called with arguments that cause no side-effects, the result is constant with respect to that argument list (sometimes called referential transparency), i.e. if the pure function is again called with the same arguments, the same result will be returned.

# Functional JavaScript

## First Class Functions
in JS functions can be in variable, obj value ...

## Pure Functions

## Currying

## Compositions
Functions which consume the return value of the function that follows. It's when we string together functions in the linear sequence, the first fn goes to the input of the second function and so on.
```js
a() b() c()
//    Composition
a(b(c(x))) === compose(a,b,c)(x)
```


## Function purity
* **Deterministic** - for every input it has to produce the same output. Mathces one to one or many to one, but not many to many.
* Does not depend on external state
* Does not depend in IO
* Does not cause side effects

## Functions as building blocks

* **Composition** - 

## Currying
Taking a function that takes multiple arguments and transforming it to a chain of functions that accept a single argument
```js
function add(x) {
    return function(y) {
        return x + y;
    }
}

add(1)(2);
```

## Higher-order functions
Functions that take other function as an argument.
Functions that operate on other functions, either by taking them as arguments or by returning them, are called higher-order functions.