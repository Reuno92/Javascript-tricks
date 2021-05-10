#Javascript Tricks

## For beginner

**From**: [36 Javascript Method you should know](https://javascript.plainenglish.io/36-javascript-methods-you-should-know-e163edaa8ea5)

**Author**: *John Anderson, Marketing Manager at Freelancers, Studied at University of California, Berkeley*

**Rewrited**: Renaud Racinet

### 1. String and array JavaScript
These methods allow you to create copies of the original except splicewho modifies it.

### 2. Slice
Create a new array or a new string from the first index passed as a parameter, until the second index (or at the end, if there is no second element as a parameter)

```Javascript
console.log([1, 2, 3].slice(0, 1));

// Result: 1
```

### 3. Split JavaScript
Convert a string of characters to an array, dividing it by the character you provide

```Javascript
console.log("one-two".split("-"))

// Result: ["one", "two"]
```

### 4. Join array JavaScript
Joins the elements of an array in a character string, if a string is passed as a parameter, the elements of the array are linked by this string.

```Javascript
["one", "two"].join("-");

// Result: "one-two"
```

### 5. Splice arrays
Splice takes an index as the first parameter in a number of elements to be extracted from the array as the second parameter. This method modifies the base array and can also take a third parameter which is added to the base array.

### 6. Arrow function JS
To have an arrow function, replace the keyword `function` with `=>`.

### 7. Arrow function declaration
Unlike a regular function, you have to store an arrow function in a variable to save it. So

```Javascript
const sum = (a, b) => {
  return a + b
}
```

is identical to

```Javascript
function sum(a, b) {
  return a + b
}
```

### 8. Objects in JavaScript
Powerful and fast storage and retrieval

### 9. String literal JavaScript
This literally gives you the value of the key `"a"`

```Javascript
obj.a
```

```Javascript
obj["a"]
```

### 10. JavaScript object literal
But this gives you the value of the key stored in the variable `a`

```
obj[a]
```

### 11. JavaScript for in
Loop over the keys of an object with a `for...in` you can then access the values of the object using `obj[key]`.

```Javascript
for (let key in obj) {}
```

### 12. JavaScript object keys
Easily get the keys of an object in an array with `Object.keys()`, or the values with `Object.values()`

```Javascript
console.log(Object.keys({ a: 1, b: 2 }))

// Result: ["a", "b"]
```

### 13. JavaScript Destructuring
Destructuring allows values to be removed from objects, the key becomes its variable name

```Javascript
const { a } = { a: 1 }
console.log(a);

// Result: 1
```

### 14. Destructuring
It also works in the other direction, if the variable `a` is `1` equal, we can create an object like this:

```Javascript
const a = 1
const obj = { a }
console.log(obj);

// Result: {a: 1}
```

### 15. JavaScript array method
These methods ALSO make it possible to create copies of the original except for the person `sort` who modifies it.

### 16. JavaScript map
Execute the function once per element in the array. Returns each return value in a new array, in the same place.

```Javascript
console.log([1, 2, 3].map(n => n + 1));

// Result: [2, 3, 4]
```

### 17. forEach JavaScript
Same as `map`, but does not return results, always returns `undefined`.

```Javascript
[1, 2, 3].forEach(n => console.log(n));

// Result :
// 1
// 2
// 3
```

### 18. filter JavaScript
Execute the function once per element, if false the element will not be included in the new array, if true it will be.

```Javascript
console.log([1, 2, 3].filter(n => n > 1));

// Result : [2, 3]
```

### 19. JavaScript reduce
Works once per item, your return value becomes the accumulation of previous iterations to the next iteration. The accumulator starts at 0 by default but you can change it with an optional 2nd arg.

```Javascript
console.log([1, 2, 3].reduce((a, val) => a + val))

// Result : 6
// Explication : 1 + 2 + 3 = 6
```

### 20. Sort array JavaScript
Sorts the array in place, by default in ascending numerical (or alphabetical) order. Passing a comparison function with 2 arguments (optional) allows you to classify the elements in descending or custom order.

```Javascript
console.log([3, 1, 2].sort());

// Result : [1, 2, 3]
```

### 21. Manipulate the DOM
For each HTML tag, there is a Document Object Model (DOM) node

### 22. Create an element in the DOM
Create an HTML element with JavaScript, returns an object `ELEMENT_HTML`.

```Javascript
document.createElement("div");
```

### 23. Apply over style to an HTML element
You can modify the CSS styles of an object `ELEMENT_HTML`.

```Javascript
ELEMENT_HTML.style.color = "pink";
```

### 24. Add a class name in JavaScript
Add or remove CSS classes from an html element.

```Javascript
ELEMENT_HTML.classList.add(".maClass");
```

### 25. Put content in an html tag with JS
Allows you to define the HTML content or the text inside an html tag.

```Javascript
ELEMENT_HTML.innerHTML = "<div>Hello</div>";
ELEMENT_HTML.innerText = "Hello";
```

### 26. Add a child in JS
You can add HTML elements to another HTML element.

```Javascript
ELEMENT_HTML_A.appendChild(ELEMENT_HTML_B);
```

### 27. Select an HTML element
Select the first matching HTML element in the DOM — both “.class” and “#id” work!

```Javascript
document.querySelector("#My-id");
```

### 28. Select all elements of class
Same as above, but return all matches in a list of html items.

```Javascript
document.querySelectorAll(".ma-class");
```

### 29. Add event listener
Add listeners to user events, such as clicks. The function runs when the event occurs.

```Javascript
ELEMENT_HTML.addEventListener("click", () => { });
```

### 30. fetch JS
Fetch returns a promise, which isn’t blocking, in other words, your code continues. We are talking about asynchronous.

```Javascript
fetch("https://google.com");
```

### 31. Promise .then
When the promise is resolved, use a method `.then` to use its result in the first parameter

### 32. Several .then in a bride
then block can also return a promise, in which case we can add another block to it.

```Javascript
PROMISE.then( x => 
    {
        /* DO ANYTHING */
    }).then(y => {
        /* DO ANYTHING */  
    });
```

### 33. Error handling in promises
Add a method `catch` to a promise, or a chain of promises to handle any errors that might occur.

```Javascript
PROMISE.catch( err => console.error(err) ); // For example
```

### 34. Solve all promises with promise.all
You can pass several promises in the function `Promise.all`. By joining a block `.then`, you will get the result of all the promises, in one table.

```Javascript
Promise.all( [ fetch("uri"), fetch("another uri") ].then( results => results.name  ) );
```

### 35. async await
async `await` is a cleaner syntax for promises, instead of `.then` serial, just use the keyword `await`, which will block your code until the promise resolves…

```Javascript
const res = await fetch(URL)
```

### 36. async await functions
Keywords `await` must be inside a function `async` just add the keyword `async` before any function, or the definition of an arrow function in which you want to use `await`.

```Javascript
const getURL = async URL => await fetch(URL);
```
=========

## For initiate

**From**: [5 Tips to Write Better Conditionals in JavaScript](https://scotch.io/tutorials/5-tips-to-write-better-conditionals-in-javascript#toc-5-use-array-every-array-some-for-all-partial-criteria)

**Author**: *Jecelyn Yeen, Developer advocate for Google Chrome.*


### 1. Use Array.includes for Multiple Criteria

```Javascript
// condition
function test(fruit) {
    if (fruit == 'apple' || fruit == 'strawberry') {
        console.log('red');
    }
}
```

At first glance, the above example looks good. However, what if we get more red fruits, say `cherry` and `cranberries`? Are we going to extend the statement with more `||` ?

We can rewrite the conditional above by using `Array.includes`.

```Javascript
function test(fruit) {
  // extract conditions to array
  const redFruits = ['apple', 'strawberry', 'cherry', 'cranberries'];

  if (redFruits.includes(fruit)) {
    console.log('red');
  }
}
```

We extract the `red fruits` (conditions) to an array. By doing this, the code looks tidier.

### 2. Less Nesting, Return Early

Let's expand the previous example to include two more conditions:

    * if no fruit provided, throw error.
    * accept and print the fruit quantity if exceed 10.


```Javascript
function test(fruit, quantity) {
  const redFruits = ['apple', 'strawberry', 'cherry', 'cranberries'];

  // condition 1: fruit must has value
  if (fruit) {
    // condition 2: must be red
    if (redFruits.includes(fruit)) {
      console.log('red');

      // condition 3: must be big quantity
      if (quantity > 10) {
        console.log('big quantity');
      }
    }
  } else {
    throw new Error('No fruit!');
  }
}

// test results
test(null); // error: No fruits
test('apple'); // print: red
test('apple', 20); // print: red, big quantity
```

Look at the code above, we have:

* 1 if/else statement that filter out invalid condition.
* 3 levels of nested if statement (condition 1, 2 & 3).

A general rule I personally follow is **return early when invalid conditions** found. 

```Javascript
/_ return early when invalid conditions found _/

function test(fruit, quantity) {
  const redFruits = ['apple', 'strawberry', 'cherry', 'cranberries'];

  // condition 1: throw error early
  if (!fruit) throw new Error('No fruit!');

  // condition 2: must be red
  if (redFruits.includes(fruit)) {
    console.log('red');

    // condition 3: must be big quantity
    if (quantity > 10) {
      console.log('big quantity');
    }
  }
}
```

By doing this, we have one less level of nested statement. This coding style is good especially when you have long if statement (imagine you need to scroll to the very bottom to know there is an else statement, not cool).

We can further reduce the nesting if, by inverting the conditions & return early. Look at condition 2 below to see how we do it: 

```Javascript
/_ return early when invalid conditions found _/

function test(fruit, quantity) {
  const redFruits = ['apple', 'strawberry', 'cherry', 'cranberries'];

  if (!fruit) throw new Error('No fruit!'); // condition 1: throw error early
  if (!redFruits.includes(fruit)) return; // condition 2: stop when fruit is not red

  console.log('red');

  // condition 3: must be big quantity
  if (quantity > 10) {
    console.log('big quantity');
  }
}
```

By inverting the conditions of condition 2, our code is now free of a nested statement. This technique is useful when we have long logic to go and we want to stop further process when a condition is not fulfilled.

However, that's no hard rule for doing this. Ask yourself, is this version (without nesting) better / more readable than the previous one (condition 2 with nested)?

For me, I would just leave it as the previous version (condition 2 with nested). It is because:

* the code is short and straight forward, it is clearer with nested if
* inverting condition may incur more thinking process (increase cognitive load)

Therefore, always aims for Less Nesting and Return Early but don't overdo it. There is an article & StackOverflow discussion that talks further on this topic if you interested:

* [Avoid Else](https://blog.timoxley.com/post/47041269194/avoid-else-return-early), Return Early by Tim Oxley
* [StackOverflow discussion](https://softwareengineering.stackexchange.com/questions/18454/should-i-return-from-a-function-early-or-use-an-if-statement) on if/else coding style

### 3. Use Default Function Parameters and Destructuring

I guess the code below might look familiar to you, we always need to check for `null` / `undefined` value and assign default value when working with JavaScript:

```Javascript
function test(fruit, quantity) {
  if (!fruit) return;
  const q = quantity || 1; // if quantity not provided, default to one

  console.log(`We have ${q} ${fruit}!`);
}

//test results
test('banana'); // We have 1 banana!
test('apple', 2); // We have 2 apple!
```

In fact, we can eliminate the variable `q` by assigning default function parameters.

```Javascript
function test(fruit, quantity = 1) { // if quantity not provided, default to one
  if (!fruit) return;
  console.log(`We have ${quantity} ${fruit}!`);
}

//test results
test('banana'); // We have 1 banana!
test('apple', 2); // We have 2 apple!
```

Much easier & intuitive isn't it? Please note that each parameter can has it own [default function parameter](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Default_parameters). For example, we can assign default value to `fruit` too: `function test(fruit = 'unknown', quantity = 1).

What if our `fruit` is an object? Can we assign default parameter?

```Javascript
function test(fruit) { 
  // printing fruit name if value provided
  if (fruit && fruit.name)  {
    console.log (fruit.name);
  } else {
    console.log('unknown');
  }
}

//test results
test(undefined); // unknown
test({ }); // unknown
test({ name: 'apple', color: 'red' }); // apple
```

Look at the example above, we want to print the fruit name if it's available or we will print unknown. We can avoid the conditional `fruit && fruit.name` checking with default function parameter & destructing.

```Javascript
// destructing - get name property only
// assign default empty object {}
function test({name} = {}) {
  console.log (name || 'unknown');
}

//test results
test(undefined); // unknown
test({ }); // unknown
test({ name: 'apple', color: 'red' }); // apple
```

Since we only need property `name` from fruit, we can destructure the parameter using `{name}`, then we can use `name` as variable in our code instead of `fruit.name`.

We also assign empty object `{}` as default value. If we do not do so, you will get error when executing the line `test(undefined)` - `Cannot destructure property name of 'undefined' or 'null'.` because there is no `name` property in undefined.

If you don't mind using 3rd party libraries, there are a few ways to cut down null checking:


* use [Lodash](https://lodash.com/docs/4.17.15#get) get function
* use Facebook open source's [idx](https://github.com/facebookincubator/idx) library (with Babeljs)

Here is an example of using Lodash:

```Javascript
// Include lodash library, you will get _
function test(fruit) {
console.log(__.get(fruit, 'name', 'unknown')); // get property name, if not available, assign default value 'unknown'
}

//test results
test(undefined); // unknown
test({ }); // unknown
test({ name: 'apple', color: 'red' }); // apple
```

You may run the demo code [here](http://jsbin.com/bopovajiye/edit?js,console). Besides, if you are a fan of Functional Programming (FP), you may opt to use [Lodash fp](https://github.com/lodash/lodash/wiki/FP-Guide), the functional version of Lodash (method changed to `get` or `getOr`).

### 4. Favor Map / Object Literal than Switch Statement

Let's look at the example below, we want to print fruits based on color:

```javascript
function test(color) {
  // use switch case to find fruits in color
  switch (color) {
    case 'red':
      return ['apple', 'strawberry'];
    case 'yellow':
      return ['banana', 'pineapple'];
    case 'purple':
      return ['grape', 'plum'];
    default:
      return [];
  }
}

//test results
test(null); // []
test('yellow'); // ['banana', 'pineapple']
```

Alternatively, you may use [Map](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map) to achieve the same result:

```Javascript
// use Map to find fruits in color
  const fruitColor = new Map()
    .set('red', ['apple', 'strawberry'])
    .set('yellow', ['banana', 'pineapple'])
    .set('purple', ['grape', 'plum']);

function test(color) {
  return fruitColor.get(color) || [];
}
```

[Map](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map) is the object type available since ES2015, allow you to store key value pair.

Should we ban the usage of switch statement? Do not limit yourself to that. Personally, I use object literal whenever possible, but I wouldn't set hard rule to block that, use whichever make sense for your scenario.

Todd Motto has an article that dig deeper on switch statement vs object literal, you may read [here](https://ultimatecourses.com/blog/deprecating-the-switch-statement-for-object-literals).

## TL;DR; Refactor the syntax

For the example above, we can actually refactor our code to achieve the same result with `Array.filter`.

```Javascript
 const fruits = [
    { name: 'apple', color: 'red' }, 
    { name: 'strawberry', color: 'red' }, 
    { name: 'banana', color: 'yellow' }, 
    { name: 'pineapple', color: 'yellow' }, 
    { name: 'grape', color: 'purple' }, 
    { name: 'plum', color: 'purple' }
];

function test(color) {
  // use Array filter to find fruits in color

  return fruits.filter(f => f.color == color);
}
```

There's always more than 1 way to achieve the same result. We have shown 4 with the same example. Coding is fun!

### 5. Use Array.every & Array.some for All / Partial Criteria

This last tip is more about utilizing new (but not so new) Javascript Array function to reduce the lines of code. Look at the code below, we want to check if all fruits are in red color:

```Javascript
const fruits = [
    { name: 'apple', color: 'red' },
    { name: 'banana', color: 'yellow' },
    { name: 'grape', color: 'purple' }
  ];

function test() {
  let isAllRed = true;

  // condition: all fruits must be red
  for (let f of fruits) {
    if (!isAllRed) break;
    isAllRed = (f.color == 'red');
  }

  console.log(isAllRed); // false
}
```

The code is so long! We can reduce the number of lines with `Array.every`:

```Javascript
const fruits = [
    { name: 'apple', color: 'red' },
    { name: 'banana', color: 'yellow' },
    { name: 'grape', color: 'purple' }
  ];

function test() {
  // condition: short way, all fruits must be red
  const isAllRed = fruits.every(f => f.color == 'red');

  console.log(isAllRed); // false
}
```

Much cleaner now right? In a similar way, if we want to test if any of the fruit is red, we can use `Array.some` to achieve it in one line.

```Javascript
const fruits = [
    { name: 'apple', color: 'red' },
    { name: 'banana', color: 'yellow' },
    { name: 'grape', color: 'purple' }
];

function test() {
  // condition: if any fruit is red
  const isAnyRed = fruits.some(f => f.color == 'red');

  console.log(isAnyRed); // true
}
```
