#Javascript Tricks

##Summary

### For Beginner
 * [36 Javascript Method you should know](#36-javascript-method-you-should-known)
 * [How to Use Async/Await to Write Better JavaScript Code](#how-to-use-asyncawait-to-write-better-javascript-code)
### For Initiate
 * [5 Tips to Write Better Conditionals in JavaScript](#5-tips-to-write-better-conditionals-in-javascript)
 * [4 JavaScript tips for shorter code](#4-javascript-tips-for-shorter-code)
### For advanced
 * [JavaScript Hacks to Instantly Make Your Code Bug-Free](#javascript-hacks-to-instantly-make-your-code-bug-free)
 * [10 Modern JavaScript Tricks Every Developer Should Use](#10-modern-javascript-tricks-every-developer-should-use)
### Features
 * [EcmaScript 2021](#Javascript-2021-New-Features)

## For beginner

## 36 Javascript Method You Should Known
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
Select the first matching HTML element in the DOM ??? both ???.class??? and ???#id??? work!

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
Fetch returns a promise, which isn???t blocking, in other words, your code continues. We are talking about asynchronous.

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
async `await` is a cleaner syntax for promises, instead of `.then` serial, just use the keyword `await`, which will block your code until the promise resolves???

```Javascript
const res = await fetch(URL)
```

### 36. async await functions
Keywords `await` must be inside a function `async` just add the keyword `async` before any function, or the definition of an arrow function in which you want to use `await`.

```Javascript
const getURL = async URL => await fetch(URL);
```
=========

## How to Use Async/Await to Write Better JavaScript Code

**From**: [How to Use Async/Await to Write Better JavaScript Code](https://www.freecodecamp.org/news/how-to-use-async-await-write-better-javascript/)
**Author**: *Milind Soorya*
**Rewrited**: *Renaud Racinet*

### What are asynchronus functions?

The term asynchronus refers to a situation where two or more events don't happen at the same time. Or in simple terms, multiple related things can happen without waiting for the previous action to complete.

In JavaScript, **asynchronus functions** are really important because of the **single threaded nature of JavaScript**. With the help of asynchrnous functions, JavaScript's event loop can take care of other things when the function is requesting some other resource.

You'd use aysnchronous code, for example, in API's that fetch a file from the network, when you're accessing a database and returning data from it, when you're accessing a video stream from a web cam, or if you're broadcasting the display to a VR headset.

### How Promises Work in JavaScript

The `Promise` object in JavaScript represents an asynchronous operation (and its resulting value) that will eventually complete (or fail).

A `Promise` can be in one of these states:

* pending: initial state, neither fulfilled nor rejected.
* fulfilled: meaning that the operation was completed successfully.
* rejected: meaning that the operation failed.

[<img src="https://www.freecodecamp.org/news/content/images/2021/06/Promise-in-Javascript.jpg">](https://www.freecodecamp.org/news/content/images/2021/06/Promise-in-Javascript.jpg)

The function passed to a new promise is called the executor. It's arguments (`resolve` and `reject`) are called callbacks that JavaScript itself provides. When the executor gets the result, whether it's now or later it doesn???t matter ??? it should call one of these callbacks.

Here's an exemple of a **Promise**:

```Javascript
const myPromise = new Promise(function(resolve, reject)  {
  setTimeout(() => {
    resolve('foo');
  }, 300);
});
```

And here are examples of a **fulfilled vs a rejected** promise:

```Javascript
// fulfilled promise
let promise = new Promise(function(resolve, reject) {
    setTimeout(()  => resolve(new Error("done!")), 1000);
});

// resolve runs the first function in .then
promise.then(
    result => alert(result), // shows "done!" after 1 second
    error => alert(error) // doesn't run
);
```

```Javascript
// rejected promise
let promise =  new  Promise(function(resolve, reject)  { 
     setTimeout(()  => reject(new Error("Whoops!")), 1000);
});

// reject runs the second function in .then
promise.then(
  result => alert(result), // doesn't run
  error => alert(error) // shows "Error: Whoops!" after 1 second
);
```

### Async/Await Basics in JavaScript

There are two parts to using `async/await` in your code.

First of all, we have the `async` keyword, which you put in front of a function declaration to turn it into an async function.

An async function is a function that knows to expect the possibility that you'll use the `await` keyword to invoke asynchronous code.

> The async keyword is added to functions to tell them to return a promise rather than directly returning the value.

```Javascript
const loadData = async () => {
  const url = "https://jsonplaceholder.typicode.com/todos/1";
  const res = await fetch(url);
  const data = await res.json();
  console.log(data);
};

loadData();
```

```json
{
  "completed" : false,
  "id"        : 1,
  "title"     : "delectus aut autem",
  "userId"    : 1
}
```

### How to Use Async/Await with Error Handling
We can handle errors using a try catch block like this:

```Javascript
const loadData = async () => {
  try{
	  const url = "https://jsonplaceholder.typicode.com/todos/1";
	  const res = await fetch(url);
	  const data = await res.json();
	  console.log(data);
  } catch(err) {
    console.log(err)
  }
};

loadData();
```

The above try-catch will only handle errors while fetching data such as the wrong syntax, wrong domain names, network errors, and so on.

When you want to handle an error message from the API response code, you can use `res.ok` (`res` is the varaiable to which response is stored). It will give you a Boolean with the value true if the response code is between 200 and 209.

```Javascript
const loadData = async () => {
  try{
	  const url = "https://jsonplaceholder.typicode.com/todos/qwe1";
	  const res = await fetch(url);
	  if(res.ok){ 
	    const data = await res.json();
	    console.log(data);
	  } else {
	    console.log(res.status); // 404
	  }
  } catch(err) {
    console.log(err)
  }
};

loadData();

// OUTPUT
// 404
```

### How an Async Function Returns a Promise

This is one of the traits of async functions ??? their return values are guaranteed to be converted to promises. To handle data returned from an `async` function we can use a `then` keyword to get the data.

```Javascript
const loadData = async () => {
  try{
    const url = "https://jsonplaceholder.typicode.com/todos/1";
    const res = await fetch(url);
    const data = await res.json();
    return data
  } catch(err) {
    console.log(err)
  }
};

const data = loadData().then(data => console.log(data));
```

> Pro Tip:
> 
> If you want to use an `async-await` to handle the returned data you can use an IIFE, but it is only available in Node 14.8 or higher.

```Javascript
// use an async IIFE
(async () => {
  const data = await loadData();
  console.log(data);
})();
```

`await` only works inside async functions within regular JavaScript code. But you can use it on its own with [JavaScript modules](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules)

### How to Use Promise.all() in JavaScript
`Promise.all()`comes in handy when we want to call multiple API's.

Using a traditional `await` method, we have to wait for each request to complete before going on to the next request. This becomes a problem when each request takes some time to complete. This can easily add up and slow things down.

Using `Promise.all()`, we can call each of these API's in parallel. (This is a bit of an oversimplification ??? for more details checkout this amazing article).

> Please be carefull when using `Promise.all`, though ??? if one of the await requests fails, it will fail altogether.

```Javascript
const loadData = async () => {
  try{
    const url1 = "https://jsonplaceholder.typicode.com/todos/1";
    const url2 = "https://jsonplaceholder.typicode.com/todos/2";
    const url3 = "https://jsonplaceholder.typicode.com/todos/3";
    const results = await Promise.all([
      fetch(url1),
      fetch(url2),
      fetch(url3)
    ]);
    const dataPromises = await results.map(result => result.json());
    const finalData = Promise.all(dataPromises);
    return finalData
  } catch(err) {
    console.log(err)
  }
};

const data = loadData().then(data => console.log(data));
```

```Javascript
// Console output
[{
  completed: false,
  id: 1,
  title: "delectus aut autem",
  userId: 1
}, {
  completed: false,
  id: 2,
  title: "quis ut nam facilis et officia qui",
  userId: 1
}, {
  completed: false,
  id: 3,
  title: "fugiat veniam minus",
  userId: 1
}]
```

### Conclusion

In most situations we can use `async/await` with a `try catch` block to handle both results and errors.

At the moment, `await` won???t work in top-level code. This means that when we???re outside any `async` function, we???re syntactically unable to use `await`. In this case, it???s regular practice to add `.then/catch` to handle the final result or falling-through error.

> Top level `await` is available from Node.js `v14.8` onwards and in ES modules only. Read more here: [Top-level await is available in Node.js modules | Stefan Judis Web Development](https://www.stefanjudis.com/today-i-learned/top-level-await-is-available-in-node-js-modules/#top-level-%60await%60-is-available-%22unflagged%22-in-node.js-since-%60v14.8%60)

### Resources that helped the author:

* [Promises (javascript.info)](https://javascript.info/promise-basics)
* [Introducing asynchronous JavaScript - Learn web development | MDN (mzilla.org)](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous/Introducing)
* [Promise - JavaScript | MDN (mozilla.org)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)

### Before We End???
Do you want to code and learn along with me? You can find the same content here in my [blog](https://milindsoorya.site/). Just open up your favorite code editor and get started.

## For initiate

### 4 JavaScript tips for shorter code

**From**        : [4 JavaScript tips for shorter code](https://medium.com/@abhinav_vp/4-javascript-tips-for-shorter-code-a31c300a28a5)

**Author**      : *Abhinav VP*

**Rewritted**   : *Renaud Racinet*

There are plenty of tips which can be followed to make the javascript code shorter as well less complicated. I will share four of such tips which have reduced the effort and development time for me a lot while coding.

#### Short Circuiting
This can be used when you???ll have to use a simple if condition.

```Javascript
    if( x == 0 ){
        foo()
    }
```

Short circuiting can be achieved by using && operator. Code after && won???t be executed if the condition before && evaluates to false.

```Javascript
    x == 0 && foo()
```

This can be chained to replace multiple if statements

```Javascript
    x == 0 && y == 0 && foo()
```

### Check if objects exist using ? operator

This is really helpful if you are dealing with scenarios like API calls or with objects of which you aren???t certain whether it or its keys are initialised.

Consider an object `studentObject` with a key `name`. Directly accessing the key value using ???studentObject.name??? might throw error . One way to evaluate whether the key exists is using nested if conditions.

```Javascript
if(studentObject){
  if(studentObject.name) {
    console.log('student name exists')
  }
}
```

This can be made shorter using `?` operator. If studentObject do not exist it will evaluate to false.

```Javascript
if(studentObject?.name){
    console.log('student name exists')
}
```

### Using Nullish coalescing operator (??)
Ternary operator already makes the code short as compared to if else statement. It???s handy if the block of code to be executed is small.

```Javascript
const foo = () => {
  x ? x : 'x do not exist'
}
```

In cases where you have to return the operand to the left of `?`, you can use the `??` operator to make the code even shorter.

```Javascript
const foo = () => {
  x ?? 'x do not exist'
}
```

### Terminating the function instead of if else nesting
consider the below function which checks the value of ???x???

```Javascript
const foo = () => {
  if (x < 1) {
    return 'x is less than 1'
  }else {
    if (x > 1){
      return 'x is greater than 1'
    } else {
      return 'x is equal to 1'
    }
  }
}
```

This if else nesting can be made less complicated by removing else conditions, as a return statement will stop code execution and return the function.

```Javascript
const foo = () => {
  if( x < 1 ) {
    return 'less than 1'
  }
  if ( x > 1 ) {
    return 'x is greater than 1'
  }
  return 'x is equal to 1'
}
```

### 5 Tips to Write Better Conditionals in JavaScript

**From**   : [5 Tips to Write Better Conditionals in JavaScript](https://scotch.io/tutorials/5-tips-to-write-better-conditionals-in-javascript#toc-5-use-array-every-array-some-for-all-partial-criteria)

**Author** : *Jecelyn Yeen, Developer advocate for Google Chrome.*


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

#### 3. Use Default Function Parameters and Destructuring

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

#### 4. Favor Map / Object Literal than Switch Statement

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

##### TL;DR; Refactor the syntax

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

#### 5. Use Array.every & Array.some for All / Partial Criteria

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

## For advanced

### JavaScript Hacks to Instantly Make Your Code Bug-Free

**From**: []()

**Author**: *Somnath Singh*

**Rewritted**: *Renaud Racinet*

### How can bugs occur while using JavaScript?

We know that JavaScript is a dynamically typed language. It means that when we declare a variable, we do not need to specify what type of variable it is, unlike C#, Java, Scala ??? you know, all those industrial programming languages. This gives us certain flexibility and speed while writing programs.

> This speed, flexibility, and ease of use are what led many to write code in JavaScript!

#### Types are damned!

Just kidding! Of course, there is a cost to this flexibility, some of which may be exposed if you???re using [Typescript](https://stackoverflow.com/questions/12694530/what-is-typescript-and-why-would-i-use-it-in-place-of-javascript), but using the following hacks while writing code can save you a pesky bug down the road.

### Scenario 1

Suppose you have a function that depends on an argument, and the argument is of a particular type like this.

```Javascript
const addNameToArray = (name, nameArr) => {
    if (name.length) {
        nameArr.push(name);
    }
    
    return nameArr;
}
```

Simple enough, right? We take a name and a `nameArr and then simply add
the name to the array if one is present.

We are making some assumptions here, however, that the name will be of a type that has a length property and that our `nameArr` will be, well, an array.

If either one of these conditions is not met, we will fail miserably.

### Hack
Consider using default parameters in your function???s signature.

```Javascript
const addNameToArray = (name = '', nameArr = []) => {
    if (name.length) {
        nameArr.push(name);
    }
    
    return nameArr;
}
```

Much better! Now you can sleep at night, knowing this useless function won???t break in production even if it???s called with a missing argument.

### Scenario 2

Your team had this excellent little function that accepted 3 arguments and did some straightforward logic with it to fetch some data from a third party service.

```Javascript
const createUser = (name, data, apiKey) => {
    const user = { name };
    const formattedName = moment(date).unix();
    
    thirdParty.fetch(user, formattedName, apiKey);
}

createUser("Sam", "17/04/21", "abc123");
```

But that was the past; now, this little function is nearly unrecognizable and has a whopping 6 arguments getting passed to it.

```Javascript
const createUser = (name, date, profileId, dataId, dataType, apiKey) => {
    const user = {
        name,
        profileId
    }
    
    const formattedDate = moment(date).unix();
    
    thirdParty.fetch(user, formattedDate, dataId, dataType, apiKey);
}

createUser("Sam", "24/11/21", 1, 123, 1234, "story", "abc123");
```

Too many parameters can often indicate a violation of the [Single Responsibility Principle](https://en.wikipedia.org/wiki/Single-responsibility_principle). But this is not the only problem. The danger in functions like these is that the order of the arguments matters, and if any of them are incorrect, we risk blowing up our API call.

> More arguments mean more surface area to make mistakes.

It would be foolish to assume that when some developers call this function, the `profileId` will not be in the place of the `dataId`, or something likewise.

This won???t blow up your program as they are both likely numbers or strings, but their incorrect order will give you the wrong data from the API, or worse ??? just not work.

### Hack
Use an object as an argument.

```Javascript
const createUser = ({ name, date, profileId, dataId, dataType, apiKey}) => {
    const user = { name, profileId };
    
    const formattedDate = moment(date).unix();
    
    thirdParty.fetch(user, formattedDate, dataId, dataType, apiKey);
}

createUser({ 
    name: "",
    date: "",
    profileId: 1,
    dataId: 123,
    dataType: "story",
    apiKey: "123abc" 
});
```

Using an object, we place a less cognitive load on our fellow developers and make sure that our arguments are explicitly set.

For functions with more than 3 arguments, I feel like using an object is a must.

### Scenario 3

We deal a lot with objects in JavaScript. We end up working with them and their properties often. Digging out valuable info can be a pain and a bit dangerous if you???re not careful.

Look at the code below:

```Javascript
const hat = user.outfit.hat;
```

Looks harmless, right? What if our user object doesn???t have an outfit property or that property is **undefined**? Then we will have an issue on our hands.

> Uncaught ReferenceError: Cannot access 'hat' before initialization.

Now, the first step in making sure we don???t get this error is to check whether the next property exists at each level, but in return, we get stuck writing awful code like this.

```Javascript
const hat = user && user.outfit && user.outfit.hat || "Cowboy"; 
```

I don???t know about you, but I feel terrible after writing a code like this. Thankfully, Now JS developers can also take advantage of what [Ruby developers have had for years](https://mitrev.net/ruby/2015/11/13/the-operator-in-ruby/)!

### Hack

Make use of [optional chaining](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Optional_chaining)

```Javascript
const hat = user?.outfit?.hat || "Cowboy";
```

![](https://miro.medium.com/max/700/1*FsCJk9hi065_PTFHNAHnfA.gif)

Now, if our traversal fails at any point, our operation will short-circuit and return the value described after `||` operator. In this way, the code is both safer and more readable.

> **Note by rewritter**
> 
> It was the best practise in 2019, now in 2021, you can use "Nullish Coalescing Operator" like this :
> 
> ```Javascript
> const user = { outfit: { hat: null }};
> let hat = user.outfit.hat ?? "Cowboy"
> console.log(hat);
>  ```
> 
> Copy/paste this bellow code in your web browser's console.

The most common reason for bugs is human mistakes in software design and coding. Once you know the causes for Software Defects, it will be easier for you to take corrective actions to minimize these defects.

### 10 Modern JavaScript Tricks Every Developer Should Use

**From**: [10 Modern JavaScript Tricks Every Developer Should Use](https://betterprogramming.pub/10-modern-javascript-tricks-every-developer-should-use-377857311d79)

**Author**: *Haseeb Anwar*

**Rewritted**: *Renaud Racinet*

#### 1 - Conditionally Add Properties to Object

We can use the spread operator, ..., to quickly add properties to a JavaScript object conditionally.

```Javascript
const condition = true;

const person = {
    id: 1,
    name: 'John Doe',
    ...(condition && { age: 16 }),
};
```

The `&&` operator returns the last evaluated expression if every operand evaluates to `true`. So an object `{ age: 16 }` is returned, which is then spread to be part of the `person` object.

If `condition` is `false` then JavaScript will do something like this:

```Javascript
const person = {
    id: 1,
    name: 'John Doe',
    ...(false), // evaluates to false
};

// spreading false has no effect on the object
console.log(person); // { id: 1, name: 'John Doe' }
```

#### 2 - Check if a Property Exists in an Object
Do you know that we can use the `in` keyword to check whether a property exists in a JavaScript Object?

```Javascript
const person = { name: 'John Doe', salary: 1000 };

console.log(salary in person); // returns true
console.log(age in person); // returns false
```

#### 3 - Dynamic Property Names in Objects
Setting an object property with a dynamic key is simple. Just use the `['key_name']` notation to add the properties:

```Javascript
const dynamic = 'flavour';

var item = {
    name: 'Biscuit',
    [dynamic]: 'Chocolate'
}

console.log(item); // { name: 'Biscuit', flavour: 'Chocolate' }
```

The same trick can also be used to reference object properties with a dynamic key:

```Javascript
const keyName = 'name';

console.log(item[keyName]); // returns 'Biscuit'
```

#### 4 - Object Destructuring With a Dynamic Key

So you know that you can destructure a variable and rename it right away with `:` notation. But do you know that you can also destructure properties of an object when you don???t know the key name or key name is dynamic?

First, let???s see how you can rename variables while destructuring (destructuring with aliases).

```Javascript
const person = { id: 1, name: 'John Doe' };

const { name: personName } = person;

console.log(personName); // returns 'John Doe'
```

Now, let's destructure properties with a dynamic key:

```Javascript
const templates = {
    'hello': 'Hello there',
    'bye': 'Good bye'
};

const templateName = 'bye';

const { [templateName]: template } = templates;

console.log(template) // returns 'Good bye'
```

#### 5 - Nullish Coalescing, `??` Operator
The `??` operator is useful when you want to check whether a variable is `null` or `undefined`. It returns the right-hand side operand when its left-hand side operand is `null` or `undefined`, and otherwise returns its left-hand side operand.

```Javascript
const foo = null ?? 'Hello';
console.log(foo); // returns 'Hello'

const bar = 'Not null' ?? 'Hello';
console.log(bar); // returns 'Not null'

const baz = 0 ?? 'Hello';
console.log(baz); // returns 0
```

In the third example, `0` is returned because even though `0` is considered falsy in JavaScript, it is not `null` or `undefined. You may think that we can use the `||` operator here but there is a difference between these two:

```Javascript
const cannotBeZero = 0 || 5;
console.log(cannotBeZero); // returns 5const canBeZero = 0 ?? 5;

const canBeZero = 0 ?? 5;
console.log(canBeZero); // returns 0
```

#### 6 - Optional chaining (`?.`)
Do you also hate errors like `TypeError: Cannot read property ???foo??? of null`. This is a pain in the neck for every JavaSript developer. Optional chaining was introduced just to solve this. Let???s take a look:

```Javascript
const book = { id:1, title: 'Title', author: null };

// normally, you would do this
console.log(book.author.age) // throws error
console.log(book.author && book.author.age); // returns null (no error)

// with optional chaining
console.log(book.author?.age); // returns undefined

// or deep optional chaining
console.log(book.author?.address?.city); // returns undefined
```

You can also use optional chaining with functions like this:

```Javascript
const person = {
    firstName: 'Haseeb',
    lastName: 'Anwar',
    printName: function () {
        return `${this.firstName} ${this.lastName}`;
    },
};

console.log(person.printName()); // returns 'Haseeb Anwar'
console.log(persone.doesNotExist?.()); // returns undefine
```

#### 7 - Boolean Conversion Using the `!! Operator

The `!!` operator can be used to quickly convert the result of an expression into a boolean `true` or `false`. Here???s how:

```Javascript
const greeting = 'Hello there!';
console.log(!!greeting) // returns trueconst noGreeting = '';

const noGreeting = '';
console.log(!!noGreeting); // returns false
```

#### 8 - String and Integer Conversions

Quickly convert a string to a number using the `+` operator like this:

```Javascript
const stringNumer = '123';

console.log(+stringNumer); // returns integer 123
console.log(typeof +stringNumer); // returns 'number'
```

To quickly convert a number to a string, use the `+` operator followed by an empty string `""`:

```Javascript
const myString = 25 + '';
    
console.log(myString); // returns '25'
console.log(typeof myString); // returns 'string'
```

#### 9 - Check Falsy Values in an Array
You must be familiar with `filter`, `some`, and `every` array methods. But you should also know that you can just the `Boolean` method to test for truthy values:

```Javascript
const myArray = [null, false, 'Hello', undefined, 0];

// filter falsy values
const filtered = myArray.filter(Boolean);
console.log(filtered); // returns ['Hello']

// check if at least one value is truthy
const anyTruthy = myArray.some(Boolean);
console.log(anyTruthy); // returns true

// check if all values are truthy
const allTruthy = myArray.every(Boolean);
console.log(allTruthy); // returns false
```

Here???s how it works. As we know that these array methods take a callback function, so we pass `Boolean` as a callback function. Boolean itself takes an argument and returns `true` or `false` based on the truthiness of the argument. So we can say that this:

```Javascript
myArray.filter(val => Boolean(val));    
```

Is the same as this:

```Javascript
myArray.filter(Boolean);
```

#### 10 - Flattening Arrays of Arrays

There is a method `flat` on the prototype `Array` that lets you make a single array from an array of arrays:

```Javascript
const myArray = [{ id: 1 }, [{ id: 2 }], [{ id: 3 }]];

const flattedArray = myArray.flat();
// returns [ { id: 1 }, { id: 2 }, { id: 3 } ]
```

You can also define a depth level that specifies how deep a nested array structure should be flattened. For instance:

```Javascript
const arr = [0, 1, 2, [[[3, 4]]]];

console.log(arr.flat(2)); // returns [0, 1, 2, [3,4]]
```

## New Features

### Javascript 2021 New Features

**FROM**: [JavaScript 2021: New Features](https://javascript.plainenglish.io/how-to-use-node-js-with-google-sheets-c256c26e10fc)

**Author**: *Tirlochan Arora*

**Rewrited**: *Renaud Racinet*


#### 1 - New Logical Operators

JavaScript has added three new logical operators to the existing collection. These three operators are, `&&=`, `||=`, & `??=` . Let???s discuss these operators in detail:

##### &&= operator:
Before diving into the explanation, take a look at the example code given below:

```Javascript
let a = 1;
let b= 2;
a &&= b;

console.log(a); // output for variable 'a' would be 2.
```

The line a&&= b is similar to the code block given below:

```Javascript
    if (a) {
        a = b;
    }
```

This logical operator is saying that if the variable `a` has a truthy value (which it is since it holds a non-zero value), then variable `a` should be assigned the value of the variable `b`. That???s why when we do `console.log(a) , the value of the variable a evaluates to 2 instead of 1.

###### ||= operator:

Consider the following code block given below:

```Javascript
let a = 1;
let b = 2;
a ||= b;
console.log(b); // output for variable 'a' would be 1.
```

This operator is the opposite of the `&&=` operator. In this, the variable `a` will be equal to the variable `b` only and only if the variable `a` has a falsy value. The code block above is equivalent to the code given below:

```Javascript
if (!a) {
  a = b;
}
```

##### ??= operator:

This operator checks whether a value is *null* or is *undefined*. Consider the following example:

```Javascript
let a;
let b = 2;
a ??= 1;
console.log(a); // output for variable 'a' would be 1.

// this code block is similar to the code given above.
// if(a === null || a === undefined) {
//   a = 1
// }
```

In the example given, the value for the variable ???a??? evaluates to *undefined* so, the `if` condition evaluates to `true` and ???a??? is assigned the value of 1.

#### String ???replaceAll??? method

We all have used the string replace method to `replace a character or words in a string with the element we specified. But it came with one limitation, this method only replaced the first occurrence of the character or word that we wanted to replace and the rest of the occurrences in the string remained the same. To replace all the characters or words, we have to use regular expressions.

Example:

```Javascript
// without regex
let str = 'JS is everywhere. JS is amazing!';
console.log(str.replace('JS', 'JavaScript')); // the output would be 'JavaScript is everywhere. JS is amazing!'

// with regex
let str = 'JS is everywhere. JS is amazing!';
console.log(str.replace(/JS/g, 'JavaScript')); // the output would be 'JavaScript is everywhere. JavaScript is amazing!'.
```

With the replaceAll method, the need for regular expression is eliminated. Consider the code below:

```Javascript
let str = 'JS is everywhere. JS is amazing!';
console.log(str.replaceAll('JS', 'JavaScript')); // the output would be 'JavaScript is everywhere. JavaScript is amazing!'.
```

The method `replaceAll` replaces all the occurrences of the character or the word specified, with the element we specified.

#### Using underscores as a separator for integers

Integers are one of the data types among strings, arrays, etc. Sometimes integers become so large that it becomes almost difficult to count the number of elements present or to figure out that the number is a million or a billion.

With the introduction of this feature, we can improve the readability of our integers. We can use underscores to separate the digits, without converting the data type to string. Example:

```Javascript
let number = 1_000_000_000; // one billion
console.log(number); // 1000000000 (the number would remain an integer)
```

#### ???Promise.any()???

If you don???t know what promises JavaScript is, then you should first read [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise).

`Promise.any()` is a new feature that takes several iterable promises and returns the promise that is fulfilled first. An example will make that clear for you:

```Javascript
const p1 = new Promise(resolve => setTimeout(resolve, 500, 'First'));
const p2 = new Promise(resolve => setTimeout(resolve, 800, 'Second'));
const p3 = Promsie.reject(1);
const promises = [p1, p2, p3];

Promise.any(promises)
    .then(result => {
        console.log(result);
    }) // the result would be 'First' because that's the promise, that is fulfilled first.
    .catch(e => {
        console.log(e);
    });
```

In case none of the promises gets fulfilled, then we will get an `AggregateError`. To handle the `AggregateError`, we will define a `catch` statement after the `then` statement. If you don???t know what `then` & `catch` blocks are, you can read about them [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Using_promises).

#### WeakRef and Finalizers

`WeakRef` are short for ???Weak References. `WeakRef` allows holding a weak reference to an object. The weak reference that is being held is called a ???target???. A weak reference does not prevent the object from being reclaimed by the garbage collector.

Garbage collection is a method of collecting the variables that are no longer needed, therefore freeing up the computer???s memory. To learn more about garbage collection, click the link [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Memory_Management).

*Note*: `WeakRef should only be used in specific situations and should be avoided whenever possible.

Let???s understand the following by an example:

```Javascript
const weakRefFunc = () => {
    const obj = new WeakRef({
       name: 'JavaScript'
    });
    console.log(obj.deref().name);
};

const test = () => {
    new Promise(resolve => {
     setTimeout(() => {
       weakRefFunc();
        resolve();
      }, 3000)
    })
    new Promise(resolve => {
     setTimeout(() => {
       weakRefFunc();
        resolve();
      }, 5000)
    })
};

test();
```

The `deref` method returns the target that is being held, if the target is garbage collected, then *undefined* is returned.

In this example, the variable `obj` is the weak reference that is being held.

The first time when the `weakrefFunc` is called inside the `test` function, it???s guaranteed that ???JavaScript??? would be printed, but for the second time when it???s called, there is no guarantee that ???JavaScript???would be printed since the variable `obj` could be garbage-collected due to it being held as a weak reference.

#### Finalizers

A Finalizer is mostly used with `WeakRef` but it can also be used individually. A finalizer tells when an object is garbage collected. Let???s understand this through an example:

??? First, we are going to create a finalizer using the `FinalizationRegistry` method.

```Javascript
const registerFinalizer = new FinalizationRegistry(data => console.log(data));

const obj = {'name': 'JavaScript'};
registerFinalizer.register(obj, 'obj is collected now!');
```

Now, the variable `registerFinalizer` is an object which contains the register method which we are going to use.

`registerFinalizer.register` takes 2 arguments. First, the object that is to be watched for garbage collection, and second is the message that we want to display to the console when the object is garbage collected.

Now, when the variable `obj` will be collected by garbage collectors, a message saying ???obj is collected now!??? will be printed out to the console.

#### Conclusion

JavaScript overall is an amazing language to learn, one of the main reasons is that it???s present everywhere. I find these new features discussed above pretty useful. JavaScript 2021 features are pretty amazing and I expect the same to happen next year.

Hope you have learned something new. If you enjoyed this post, recently I wrote a post on how to use Node.js with Google sheets. You can see that [post](https://javascript.plainenglish.io/how-to-use-node-js-with-google-sheets-c256c26e10fc) here. Thank you all for taking out the time to read this.
