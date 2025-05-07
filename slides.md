---
# You can also start simply with 'default'
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://images.unsplash.com/photo-1633113214698-485cdb2f56fd?q=80&w=687&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
#https://cover.sli.dev
# some information about your slides (markdown enabled)
title: Welcome to Slidev
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# apply unocss classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
# open graph
# seoMeta:
#  ogImage: https://cover.sli.dev
---

# Our Frontend Journey So Far

Circle 7's Semester Recap

<div @click="$slidev.nav.next" class="mt-12 py-1" hover:bg="white op-10">
  Press Space for next page <carbon:arrow-right />
</div>

<div class="abs-br m-6 text-xl">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="slidev-icon-btn">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
  </a>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->







<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/features/slide-scope-style
-->

<!-- <style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style> -->


---

# Meet the Team

-  Joy Umofia
-  Emmanuel Uchenna
-  Osariemen Aibueku
-  Golden Ekpendu
-  Oyetunde Raphael
-  Grace Oluwasegun
-  Ifeoluwa Osinuga
-  Ibe Okorafor
-  Okoye Chukwudi Innocent
-  Anowai Chukwuemeka Stephen
-  Oscar Ochang

<p v-after class="text-sm text-gray-400 mt-4 italic">A small but mighty crew!</p>

::right::
<img 
  v-fade 
  src="https://images.unsplash.com/photo-1629904853893-c2c8981a1dc5?auto=format&fit=crop&w=500&q=80" 
  alt="Team meeting" 
  class="rounded-xl shadow-xl"
/>



---

# Books to focus on this semester
- Refactoring UI 
- Building Large Scale WebApps
<br><br>
# Coursera Course
- [Learning How To Learn ](https://www.coursera.org/learn/learning-how-to-learn)
       

<!-- https://sli.dev/guide/animations.html#click-animation -->



---

# Return Statement

<p v-click v-fade class="mt-4 transition duration-500 ease-in-out">A return statement is used inside a function to either stop the functions execution or it sends back a value to wherever the function is called. They are mostly the last line in a function.</p>

```js {monaco }
 function multiply (a, b) {
  return a * b;
}

const result = add(9, 2);
console.log(result) // Output: 18 
```

 <p v-click v-fade class="mt-4 transition duration-800 ease-in-out">
  Functions can return arrays
</p>
```js {monaco}
const products=[
  {item:"Black kettle", price:"$100",category:"utensils"},
  {item:"Iphone 7plus", price:"$200",category:"gadget"},
  {item:"Mac book pro", price:"$1000",category:"gadget"}
]
 function getGadget() {
  return products.filter(product=>product.category==="gadget")
}
console.log(getGadget())
//Output [{item:'Iphone 7plus', price:'$200', category:'gadget'}{item: 'Mac book pro', price:'$1000', category:'gadget'}] 

```


---

<p>
  Functions can return objects
</p>
```js {monaco}
function user(){
  return {
    name:"Blessing",
    age:20
  }
}
console.log(user())//output {name:Blessing, age:20}
```
---

# Arrays
Arrays are list that can store multiple values in one variable. They are separated by a comma(,).
```js{monaco}
const arr=[1,2,3,4]
const arr=["james",42,false]//We can have numbers,booleans,or mixed types
```
We can access an array by its position(index).
```js{monaco}
const people=["abel","nancy","david"]

console.log(people[0])//output "abel"
console.log(people[2])//output "david"

console.log(people.length)//output 3
//length is the number of item we have in an array.
```
Accessing an object in an array
```js{monaco}
const students=[
  {id:"17/08/02/200",track:"frontend"},
  {id:"17/08/02/106",track:"Product"}
] 
console.log(students[1]) //output {id:"17/08/02/106",track:"Product"}
console.log(students[0].track)//output "frontend"
```
---

### Array Operations 
Array operations are methods or functions that we can perform on an array. They help us remove,add,modify elements in an array. Javascript provides a vairiety of built-in methods to perform different array operations. Here's a list of common array operations:
- push
```js{monaco}
const age=[20,50,40]
age.push(10)
console.log(age)//output[20,50,40,10] it adds the number 10 to the end of the array
```
- pop
```js{monaco}
const age=[20,50,40]
age.pop()
console.log(age)//output[20,50] it removes the last item from the array
```
- unshift
```js{monaco}
const age=[20,50,40]
age.unshift(10)
console.log(age)//output[10,20,50,40] it adds the number 10 to the beginning of the array
```
---

- filter
```js{monaco}
const num=[78,22,10,50]
const filt = num.filter(item=>item>=40)
console.log(filt)// filter checks the requirement then creates a new array with the elements that pass the requirement. 
// filter is a method 
```
- map
```js{monaco}
const product=[
         {item:"gold ring",price:50000},
         {item:"face wash",price:2500},
         {item:"lip gloss",price:500}
]
const modify = product.map(item=>item.price/10)// products are on 10% discount
console.log(modify)//output [5000,250,50] map modifies the array and returns a new array with its modification. 
// map is a method 
```
```js{monaco}
// you can also change an item in an array

let item=["ruler","cup","slippers"]
item[2]="shoe"
console.log(item)// output ["ruler","cup","shoe"] shoe replaces slippers because its in the index 2 position.
```
You can also see different ways Operations can be performed on an array [here](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Scripting/Arrays).

<!-- Inline style -->
<style>
.footnotes-sep {
  @apply mt-5 opacity-10;
}
.footnotes {
  @apply text-sm opacity-75;
}
.footnote-backref {
  display: none;
}
</style>

<!--
Notes can also sync with clicks

[click] This will be highlighted after the first click

[click] Highlighted with `count = ref(0)`

[click:3] Last click (skip two clicks)
-->

---
level: 2
---

# Spread Operator
Spread oprators is way in javascript used to unpack,clone,merge or spread out elements.We can spread things that are iterable. its syntax is(...)
```js{monaco}
let fruits=["banana","coconut","mango","apple"]
const copy=[...fruits]
console.log(copy)//ouput ["banana","coconut","mango","apple"]. it just copies the element
```
You can also merge 2 arrays and put in one array
```js{monaco}
const arr1=[2,4,6,8,10]
const arr2=[1,3,5]
const newArray=[...arr1,...arr2]
console.log (newArray) //output [2,4,6,8,10,1,3,5]
```
Let's use spread with Objects
```js{monaco}
  const user = { name: "Ada", age: 21 };
  const copiedUser = { ...user };
 console.log(copiedUser);  //output { name: "Ada", age: 21 }
```


---

Spread in function
```js{monaco}
function spread(a,b,c){
  return a+b+c
}
const result=[3,4,5]
console.log(spread(...result))
```<br>
without spread you'll have to do:

```js{monaco}

 function spread(d,e,f){
  return d+e+f
 } 
const results=[3,4,5]
console.log(spread(results[0], results[1], results[2]))

```

---

# Rest Parameter
<p v-click v-fade class="mt-4 transition duration-800 ease-in-out">Rest parameter allows a function to accept an indefinite number of arguments as an array. It's used when you don't know how many arguments will be passed in or when you want to simplify handling multiple inputs.
Some things to note:</p>



<div grid="~ cols-2 gap-4" m="t-2" v-click v-fade class="mt-4 transition duration-800 ease-in-out">

```js

Functions can only take one rest parameter

function mycall(...caal){
 console.log(caal)
}
mycall(3,5,6)// output [3,5,6]

```

```js

The rest parameter must be the last parameter in the function

function greet(greeting, ...names) {
  console.log(`${greeting}, ${names}`);
}

greet("Hello", "Ada", "Ben", "Chloe");
// Output: Hello, Ada, Ben , Chloe

```
```js
Trailing commas after a rest parameter is not allowed.

function myfunct(...call,){
  console.log(call)
}

```

<!-- <img border="rounded" src="https://github.com/slidevjs/themes/blob/main/screenshots/theme-default/01.png?raw=true" alt="">

<img border="rounded" src="https://github.com/slidevjs/themes/blob/main/screenshots/theme-seriph/01.png?raw=true" alt=""> -->

</div>

<!-- Read more about [How to use a theme](https://sli.dev/guide/theme-addon#use-theme) and
check out the [Awesome Themes Gallery](https://sli.dev/resources/theme-gallery). -->

---

# Callbacks and Events in JavaScript
In JavaScript, callbacks and events are important concepts used to handle asynchronous operations and user interactions.<br>
What is a Callback?
A callback is a function that is passed into another function as an argument, and it is executed after some operation has been completed. Callbacks are commonly used for asynchronous tasks like loading data or responding to user actions.
Think of a callback like ordering food at a restaurant. When you place your order, the waiter takes it to the kitchen, and instead of waiting around, you give the waiter your phone number so they can call you when the food is ready. This is similar to JavaScript, where you pass a function (the callback) to another function to be called once a task is complete. However, if you start placing several orders that depend on each other—like needing your drink before the starter, and the starter before the main—you might end up dealing with too many layers of callbacks. This situation is known as callback hell, where code becomes messy and hard to manage. That's why developers often use Promises or async/await to avoid it.

---

Here's a simple example of a callback:
```js{monaco}
function greetUser(name,callback){
  console.log("Hello, " + name)
  callback()
}
function sayGoodbye(){
  console.log("Goodbye!")
}
greetUser("ifeoluwa",sayGoodbye) 
```
'sayGoodbye' is a callback function passed to 'greetUser'. After greeting the user, it runs the callback and says goodbye.</br>

 # What is an Event?
An event is an action that occurs in the browser, like a user clicking a button or pressing a key. JavaScript allows you to set up 'event listeners' that wait for these events and respond to them when they happen.
An event works like a doorbell at home. You don't stand by the door all day; instead, you listen for the doorbell. When someone rings it, you hear the sound and go to answer the door. Similarly, in JavaScript, you set up an event listener to wait for actions like clicks or keypresses, and when the event happens, your function runs in response.


---

Event Example
Here's a basic example of handling a button click event:
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="./style.css">
  <title>document</title>
  
  
  <script>
  document,querySelector("#myButton").addEventListener("click",function(){
    alert("Button was clicked!")
  })
 </script>
</body>
</html>
```
This code waits for the user to click the button. When the click happens, the function inside the event listener runs and shows an alert.
---



<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

# Controlling Forms In JavaScript
Forms are Key for user input and interaction in web development. In order to create dynamic and interactive websites, it is important to understand how to work with forms using javaScript.<br> 
In order to access forms using javascript, document.forms is being used. It is a named-collection which means you can access forms using both their names and index. We could create a form with javaScript using the createElement() method.
A form may have one or many fieldset elements inside it. They also have elements property that lists form controls inside them. The HTML fieldset element gets used to group several controls as well as labels (label) within a web form. We can access the Fieldset properties via the form.elements property.

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

<!--
Here is another comment.
-->
---
transition: slide-up
level: 2
---
For example:
````
// create form element
const form = document.createElement('form');
form.id = 'form';
const fieldset = document.createElement('fieldset');
fieldset.name = 'fields';
// create a legend
const legend = document.createElement('legend');
legend.textContent = "Personal details";
// create input element
const input = document.createElement('input');
input.type = 'text'
input.id = 'name'

fieldset.appendChild(input, legend);
form.appendChild(fieldset);
document.body.appendChild(form);
````
---
---
# Referencing and Accessing Form Elements
In JavaScript, every element is linked to the form and can be accessed using the name or the index. For example:
````
<form>
<input type = "text" name = "user" />
</form>
<script>
// form → element
let user = form.user // targets the the name;

// element → form
console.log(user.form) //gets the form which the 'user' input belongs to;
</script>
````
---
---
# Form Properties
Form elements has different properties that allows us to interact with them programmatically.
For instance, you can use the "value" property to access and modify form elements like the input and textarea. This property could be a string (input.value) or boolean(input.checked), for checkboxes and radio buttons. Unlike the input and textarea elements, the select element has a wider range of properties you can use to interact with a form, these properties are as follows:<br>.option<br>.value<br>.selectedIndex.

# Focusing: focus/blur
Managing focus and blur events is crucial to a web developer when making forms and other input elements user friendly. This gives the developer control over what happens when a user clicks or hover over input fields like text-boxes, drop downs etc, thereby enhancing the user experience. Focus indicates that a user is ready to input data into a certain element. This focus is achieved when the element gains the attention of the user, especially when the user clicks or navigates their way to the element with a keyboard. 
---

 
# Blur
When a user moves away from an input element especially by clicking on another element, the previously focused element starts to blur. Blur event helps indicates that a user has finished interacting with a specific field. An example of the use case of the blur event is as follow: 
````
input.onblur = function(){
  if (!input.value.includes('@')) {
    input.classList.add('invalid');
    error.innerHTML = "Please enter a valid email";
  };
}
````
This example is an email validation where the input is blurred out when the user clicks outside the input field, indicating the end of interaction. 
---
---
# Form Events
## Change
A change event is an event that fires when there is a change in a form and the user has already finished interacting with the input field. In other form elements like checkboxes and  radio button, the change gets triggered as soon as the value is changed.

## Input
The input event doesn't require the user to finish interaction with the input field, instead, the event starts at the slightest modification. It ideal in scenarios where there is need for immediate feedback like showing the password strength or live search.
---
---
## Cut, Copy and Paste
The cutting, copying and pasting operations are handled by these events. They are part of the clipboardEvent class that gives access to the clipboard's contents. The event.clipboardData objects provides access to the data being cut, copied or pasted and this behaviour can be prevented using event.preventDefault().
````
<input type="text" id="myInput" placeholder="Try copy, cut or paste here">
<script>
const input = document.getElementById("myInput");

// Copy event
input.addEventListener("copy", function (event) {
  alert("You copied text from the input!");
});

// Cut event
input.addEventListener("cut", function (event) {
  alert("You cut text from the input!");
});

// Paste event
input.addEventListener("paste", function (event) {
  alert("You pasted text into the input!");
});
</script>
````
---
---

# Form Submission Events and Methods
Form submission allows users to input data and send it over to the server for processing and in JavaScript, there are two ways to handle form submissions.<br>
- The submit event<br>
- The form.submit() method<br>
## The Submit Event
The submit event gets triggered the moment a form is submitted. it is used to validate form data before it gets sent to the server or to prevent the default submission behavior and handle it with JavaScript instead.
### How is the submit event triggered?
The submit events get triggered when the user submits a form by either clicking submit or pressing the enter button while focused on an input field within the form.
---
---

## Code Example For The Submit Event

````
<form id="myForm">
  <input type="text" name="username" placeholder="Enter your name" required>
  <button type="submit">Submit</button>
</form>

<script>
const form = document.getElementById("myForm");

form.addEventListener("submit", function (event) {
  event.preventDefault(); // Prevents page from reloading
  alert("Form has been submitted!");
});
</script>
````
This code above is used to validate input before submitting data.<br><br>
Apparently, pressing enter to submit a form simulates a click event even when no click actually occurred.
---
---
## The <kbd>form.submit()</kbd> Method
WHen a developer programmatically submit a form without user interaction, the form.submit() method is used. This method is used in scenarios like, surveys, or sign-up wizards, where each steps submits partial data silently without the user noticing.<br>
Code example:
````
function createForm() {
const myForm = document.createElement('form');
myForm.method ='POST';
myForm.action = '/api/submit';

// create input element
const Input = document.createElement('input');
Input.type = 'text';
Input.name = 'username';
Input.value = 'Amarachi Ezendu';

myForm.appendChild(Input);
document.body.appendChild(myForm);

myForm.submit();
}
createForm();
````
---
---
# Form Validation
It is crucial that data submitted by users is accurate and secure and in order to ensure this, web developers use form validation.<br>
There are three important aspects of form validation:<br>
- The novalidate Attribute
- HTML validation Attributes
- Constraint VAlidation API
---
---
## The novalidate Attribute
When a web developers wants to implement custom validation logic, or use JavaScript library for form validation, they use the novalidate attribute to disable the browser's default validation behavior. <br>
NB: Iy is used on the form element<br>
For example
````
<form novalidate>
<label for="email">Email:</label>
<input type="text" id="email" required />
<button type="submit">Submit</button>
</form>
````
Even though the "required" attribute is used on the input type="email" the browser will not perform the default validation when the form is submitted because of the novalidate attribute.
---
---
## HTML Validation Attributes
These are special attributes added to form elements  to ensure that the user enters valid data before the form can be submitted. They prevent incomplete or incorrect form inputs without involving JavaScript. These attributes include:<br>
- Required
- Minlength/maxlength
- Min/max
- Pattern
- Type
- Step
- Readonly
- Disabled
---
---
Example:
````
<form>
  <input type="text" required minlength="3" maxlength="10" placeholder="Username" />
  <input type="email" required placeholder="Email" />
  <input type="number" min="1" max="100" />
  <input type="submit" />
</form>
````
## Constraint Validation API
The Constraint Validation API is a set of JavaScript properties and methods that lets developers interact with HTML form validation. It allows developers to:<br>
- Check if a form or input is valid
- Trigger validation manually
- Get validation error messages
- Customize or override validation behavior.
---
---
## CONT'D
The Constraint Validation APIs include:
- validity
- validationMessage
- willValidate
- checkValidity()
- reportValidity()
- set customValidity()
---
---
Example
````
<form id="myForm">
  <input id="username" type="text" required minlength="3" />
  <button type="submit">Submit</button>
</form>

<script>
  const form = document.getElementById('myForm');
  const input = document.getElementById('username');

  form.addEventListener('submit', function (e) {
    if (!input.checkValidity()) {
      input.setCustomValidity("Username must be at least 3 characters!");
      input.reportValidity(); // Show the message
      e.preventDefault(); // Stop form from submitting
    } else {
      input.setCustomValidity(""); // Clear custom message
    }
  });
</script>
````
---
---


# Bundlers
Meaning of Bundlers
A JavaScript bundler is a tool that combines multiple JavaScript files, along with their dependencies, into a single file or a small number of files, often called a "bundle. 
Why bundlers?
The current state of ECMAScript Modules (ESM) has some limitations such as inability to import and export media files and most browsers have not fully implemented ESM specifications, which have limited the capacity of ESM in the browser.

#### Bundlers are therefore useful for the following reasons:
1.	Bundlers help to reduce the number of HTTP requests required to load a webpage.
2.	Bundlers analyze the dependencies between files, creating a dependency graph, and then package them in the correct order for execution in a browser.
3.	Bundlers significantly improve load times and overall performance.
4.	Bundlers help developers import all kinds of files, including media files.
5.	Bundlers also facilitate the use of modern JavaScript features and module systems, like ES modules and CommonJS, ensuring compatibility across different environments.
6.	Bundlers facilitate the use of npm packages.

---

Examples of Bundlers
1.	Parcel
2.	Vite
3.	Webpack
4.	turporepo.

This class focuses on using Vite.


# Vite
Vite uses ES Modules behind the scenes and has zero config by default. It supports modern frameworks like React and Vue.
Steps to using Vite in a JS project:
1.	Run npm init or npm init -y or npm init --yes in the folder of your project.
2.	If using npm init, you will be asked a few questions on the package name, version, description, entry point, test command, git repository, keywords, author and license.
3.	After following the prompt, your project folder should have a new package.json file.

---

4.	Note that a package.json file is required for a standard JavaScript project.
5.	After this, install vite as a dev dependency as follows:

	npm install --save-dev vite

Note that installing vite as a devdependency will add a node_modules folder to your project.
6.	The next step is to update the "scripts" property in your package.json file to read as follows: 
 ```js
 "scripts":{
  "dev":"vite",
  "build":"vite build",
  "preview":"vite preview"
 }
 ```
 7.	Next, you can start using npm packages in your project. See npmjs.org for a collection of npm packages.
8.	Also, if you follow these steps,you do not need live server again. All you need to do is run: npm run dev. This opens a live development environment for you.
9.	To compile your project for production, run npm run build and this will create a dist folder for you.

 
---


#### For a shorter and faster way to use Vite in your vanilla JS project:

1.	Run npm create vite@latest 
[name of project] -- --template vanilla OR pnpm create vite@latest [name of project] --template vanilla 
2.	cd into project folder
3.	Run npm install OR pnpm install
4.	Run npm run dev OR pnpm run dev
5.	For production, run npm run build OR pnpm run build


---



# Document Object Model (DOM) and Browser Object Model (BOM)

<div @click="$slidev.nav.next" class="mt-12 py-1" hover:bg="white op-10">
  Press Space for next page <carbon:arrow-right />
</div>

<div class="abs-br m-6 text-xl">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="slidev-icon-btn">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
  </a>
</div>

---
transition: fade-out
---

# Browser and Document Object Models

<div grid="~ cols-2 gap-4">
<div>

## BOM
- Window interface to browser
- Controls browser window and frames
- Global JavaScript objects
- Key objects: window, screen, location, history

</div>
<div>

## DOM
- Programming interface for HTML/XML
- Tree representation of document
- Allows dynamic content manipulation
- Foundation for interactive web apps

</div>
</div>

<div class="mt-4">

```html {all|1-3|4-7|8-11}
<!DOCTYPE html>
<html>
  <head>
    <title>My Page</title>
    <meta charset="UTF-8">
  </head>
  <body> 
    <h1>Hello!</h1>
    <p>This is a DOM tree.</p>
  </body>
</html>
```

</div>

---
transition: slide-up
---

# DOM Navigation

<div class="grid grid-cols-2 gap-4">

## Tree Structure
```html
<body class="container"> 
  <h1 id="title">Welcome</h1>
  <div class="content">
    <p>Main content</p>
  </div>
</body>
```

## Navigation Methods
```js {all|1|2|3|4}
document.body                    // Access body
document.getElementById('title') // By ID
document.querySelector('.content') // First match
document.querySelectorAll('p')    // All matches
```

</div>

---
transition: slide-up
---

# DOM Manipulation

<div class="grid grid-cols-2 gap-4">

## Element Modification
```js {all|1-2|4-5|7-8|10-11}
// Change text content
element.textContent = 'New text'

// Update styles
element.style.color = 'blue'

// Add new element
document.createElement('div')

// Remove element
element.remove()
```

## Event Handling
```js {all|1-5|7-11}
// Click event
document.getElementById('btn')
  .addEventListener('click', () => {
    console.log('Clicked!')
  })

// Form submission
document.querySelector('form')
  .addEventListener('submit', (e) => {
    e.preventDefault()
    // Handle form data
  })
```

</div>

---
transition: slide-up
---

# DOM Best Practices

<div class="grid grid-cols-2 gap-4">

## Performance Tips
- Cache DOM selections
- Minimize DOM updates
- Use document fragments
- Avoid inline styles
- Batch DOM operations

## Example Code
```js {all|1|3-5|7-9|11-13}
const list = document.querySelector('.list')

// Bad: Multiple DOM updates
items.forEach(item => {
  list.appendChild(createListItem(item)))

// Good: Use fragment
const fragment = document.createDocumentFragment()
items.forEach(item => fragment.appendChild(createListItem(item)))

// Single DOM update
list.appendChild(fragment)
```

</div>

````



---

# JSX and Components

This doc summarises what JSX is, the use of components in ReactJS, and props. It has been made to be easy to understand and practice.

JSX
JSX stands for JavaScript XML, a way to write HTML in JavaScript. JSX can be written in .js or .jsx files.

JSX is standard in writing React. 

```js
const element = <h1>Hello, world!</h1>;
```

This simple example shows how JSX can be written in a JavaScript expression.
Recap
It looks like HTML, but it’s actually JavaScript.
JSX helps you build UIs by mixing HTML-like tags with JavaScript.


---


# Components
Components are the building blocks in React. These are functions used to return UIs.There are two types of components in React - functional and class components. Let’s take a button component for example:

Functional component:

```js
function ButtonComponent() {
  return <button>Click Me!</button>;
}
```

Class component:

```js
class ButtonComponent extends React.Component {
  render() {
    return <button>Click Me!</button>;
  }
}
```


Please note that functional components are preferred to class components:


---

A typical component structure looks something like this:
```js{monaco}
function App() {
  return (
    <Booklist>
	<Book/>
	<Book/>
</Booklist>  
);
}
```
The example above shows a simple UI that renders a list of Book components. Components can be nested under other components to make even larger components. You should also use components because it is easy to update and modify.

Break UIs into small reusable pieces using components




---

# Props
Props are data passed into a component (like function arguments). Let’s use the button component created earlier.

```js
function ButtonComponent(props) {
  return <button>Hi, {props.name}</button>;
}
```
In this example, a prop has been added to the component (think function argument). To use this prop in our component, we use a pair of brackets {} and inside that we add the keyword “props”  followed by the name of the prop we’d like to pass. In this case, let’s use name.

This can also be written in another way by destructuring the props. For example:


```js{monaco}
function ButtonComponent({name}) {
  return <button>Hi, {name}</button>;
}
```

In this case, instead of using props.name, we’ve destructured the prop to get the exact data we need, which in this case is the name.
Now let’s see how to apply this in our code. We’ll use the example of the Book component created earlier.

---

```js{monaco}
function Book({title, author}) {
  return (
<div>
<h3>Book title is: {title}</h3>
<p>Authored by: {author}</p>
</div>
)
}
```

When rendering in the root component 

```js
function App() {
  return (
    <Booklist>
	<Book title=”Atomic Habits” author=”James Clear”/>
	<Book title=”Refactoring UI” author=”Adam Wathan”/>
</Booklist>  
);
}
```

From this example, we see how to add multiple props to our component and update these props when rendering the component.


---



# Async/Await, Promise, Fetch, and API

## Introduction

Promises are a mechanism for handling asynchronous operations, Fetch is a specific API for making network requests (like getting data from a server), and API stands for Application Programming Interface, which defines how different components interact, including Fetch and Promises.

## Promise

A Promise represents the eventual completion (or failure) of an asynchronous operation, like fetching data from a server. It allows you to handle the result (success or failure) without blocking the main thread.

## Fetch API

The Fetch API is a built-in JavaScript API for making network requests (GET, POST, etc.) and handling the responses. It uses promises, making it easier to work with asynchronous data fetching.

API (Application Programming Interface):

---


## API

APIs define how different software components (like your JavaScript code, the browser, and the server) can interact with each other. The Fetch API is an example of a specific API for making network requests, and it leverages Promises to handle the asynchronous nature of those requests.


## How they work together

1. Initiate a Fetch Request:

You use the `fetch()` function (part of the Fetch API) to initiate a network request to a server.

2. Return a Promise:

The `fetch()` function returns a Promise that resolves with a Response object representing the server's response.

3. Handle the Promise:

You can use the `.then()` method (or async/await) to handle the Promise. This allows you to process the Response object when it becomes available.

---
dragPos:
  square: 0,-190,0,0
---

4. Access Response Data:

The Response object provides methods like `json()`, `text()`, etc., to access the data in various formats (e.g., JSON, text).



## Code Examples

```js

fetch('https://api.example.com/data') // Initiate a fetch request
.then(response => { // Handle the Promise

if (!response.ok) { // Check for errors
throw new Error(`HTTP error! status: ${response.status}`);

}
return response.json(); // Extract JSON data from the response
})

.then(data => { // Handle the JSON data

console.log(data); // Log the data

})
.catch(error => { // Handle any errors during the process
console.error('Error fetching data:', error);
});
```


---



# REACT SETUP

This class focuses on setting up React with Vite.

### Vite    

Vite is a build tool that revolutionizes the React setup process, and is designed to be fast and lightweight. It uses ES modules to improve performance and provides a zero-config setup for building modern web applications. 

Creating a React project traditionally consumes valuable time, especially on older machines. With Vite, your projects are faster and more efficient, and also gives you the flexibility to choose your preferred framework.
To install React with Vite on your VSCode editor, follow the steps below;

Step 1: Launch your VSCode editor and open a new terminal.
```js
Click on the three dots at the top left corner and select “Terminal” > “New Terminal.”
```

Step 2: Within the terminal, enter npm create vite@latest, and hit enter.
```js
PS C:\Users\Desktop\Projects>npm create vite@latest
```

---


Step 3: Customize your project name or stick with the default, then press enter.
Step 4: You will see a list as shown below; use the arrow keys to move up and down the list, click enter to choose your preferred option. Select React:
```js
?select a framework:
vanilla
vue
react
preact
lit
swelte
solid
Qwik
```
and select `javascript`.
```js
select a framework: React
select a variant : javascript

scoffolding project in C:\users\Dell\Desktop\Projects\vite-project..
Done. Now run:
```


---



Step 5: Navigate to your Vite project in the terminal and execute the first command from the list displayed

```js 
`cd vite-project`
```

Step 6: Run `npm install` to install project dependencies.
```js
npm install
```
Step 7: Launch your Vite project with
```js
 `npm run dev`.
 ```

 Step 8: Access and explore your newly created Vite React project in the browser via the provided link.

   On your terminal click on the blue link to open your Vite project in your web browser.
```js
local:http://127.0.0.1:5173/
```

---

# Mini Projects
 [FORM](https://f-validation.vercel.app)

 [Quote generator](https://joy-umofia.github.io/Quote-generator/)

 [Weather Checker](https://joy-umofia.github.io/Weather-APP/)
---


![thank you](https://images.unsplash.com/photo-1586810165616-94c631fc2f79?q=80&w=1170&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D)


