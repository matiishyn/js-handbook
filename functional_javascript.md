# Functional JavaScript

## Resources
* http://www.sitepoint.com/introduction-functional-javascript/
* http://scott.sauyet.com/Javascript/Talk/FunctionalProgramming/#slide-0
* https://www.youtube.com/watch?v=L7b7AW14rYE (slides)

## Function purity
* **Deterministic** - for every input it has to produce the same output. Mathces one to one or many to one, but not many to many.
* Does not depend on external state
* Does not depend in IO
* Does not cause side effects

## Functions as data
* **First class citizens** - in JS functions can be in variable, obj value ...
* Identified by their returns
* **Modifiable** - functions can build another functions

## Functions as building blocks

* **Composition** - Functions which consume the return value of the function that follows. It's when we string together functions in the linear sequence, the first fn goes to the input of the second function and so on.
```js
a() b() c()
//    Composition
a(b(c(x))) === compose(a,b,c)(x)
```

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