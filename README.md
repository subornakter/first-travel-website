

#### 1. What is the difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll?

The differences between getElementById, getElementsByClassName, and querySelector/querySelectorAll is given below:

- **getElementById(id):** Selects one element with the specified id.Returns a single Element object (or null if no element with the given id is found).
example:
const Button = document.getElementById("main-btn");

- **getElementsByClassName(className):** Selects all elements with the given class name.Returns a live HTMLCollection of elements within array.
example:
const items = document.getElementsByClassName("list-item");
for (let item of items) {
  console.log(item.innerText);
}

- **querySelector:** Selects the first element that matches a CSS selector.A single Element object (or null if not found).
example:
const firstCopy = document.querySelector(".copy-btn");

- **querySelectorAll:** Selects all elements that match a specified CSS selector.Returns a static NodeList of elements.
example:
const items = document.querySelectorAll(".list-item");


#### 2.How do you create and insert a new element into the DOM?

**Create the element:**
The document.createElement() method is used to create a new HTML element node. It takes the tag name of the element as a string argument.

const newDiv = document.createElement('div');

**Insert into DOM:**
Once the element is created, it needs to be attached to an existing parent element within the DOM tree. appendChild() created into DOM.

 const parentElement = document.getElementById('container');
parentElement.appendChild(newDiv);

#### 3.What is Event Bubbling and how does it work?

Event bubbling means when an event happens on an element (like clicking a button), it doesn’t stop there.
The event moves up (bubbles) to its parent, then grandparent, and so on until it reaches the top (document).

event bubbles up like (child → parent → document).

#### 4.What is Event Delegation in JavaScript? Why is it useful?

Event Delegation is a technique in JavaScript where instead of adding event listeners to many child elements, you add one event listener to a parent element.

**useful:**
Event delegation is useful because it improves performance(Only one event listener instead of hundreds/Thousands), handles dynamic elements & reduces code.

#### 5.What is the difference between preventDefault() and stopPropagation() methods?

**preventDefault():** Stops the browser’s default action for that event.

Example: Clicking a link doesn’t open a new page.

**stopPropagation():** Stops the event from moving (bubbling) up the DOM tree.

Example: Clicking a button doesn’t trigger its parent’s click event.


