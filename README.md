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
