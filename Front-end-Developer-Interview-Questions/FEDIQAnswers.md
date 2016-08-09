#Front-end Job Interview Questions

This file contains a number of front-end interview questions that can be used when vetting potential candidates. It is by no means recommended to use every single question here on the same candidate (that would take hours). Choosing a few items from this list should help you vet the intended skills you require.

**Note:** Keep in mind that many of these questions are open-ended and could lead to interesting discussions that tell you more about the person's capabilities than a straight answer would.

## Table of Contents

  1. [General Questions](#general-questions)
  1. [HTML Questions](#html-questions)
  1. [CSS Questions](#css-questions)
  1. [JS Questions](#js-questions)
  1. [Testing Questions](#testing-questions)
  1. [Performance Questions](#performance-questions)
  1. [Network Questions](#network-questions)
  1. [Coding Questions](#coding-questions)
  1. [Fun Questions](#fun-questions)

## Getting Involved

  1. [Contributors](#contributors)
  1. [How to Contribute](https://github.com/h5bp/Front-end-Developer-Interview-Questions/blob/master/CONTRIBUTING.md)
  1. [License](https://github.com/h5bp/Front-end-Developer-Interview-Questions/blob/master/LICENSE.md)

#### General Questions:

* What did you learn yesterday/this week?
  * **Over the past week I have learned quite a few new concepts. I am beginning to understand the power of currying/partial application of functions in JavaScript. Specifically, considering it as a way to filter and sort items in an Array by certain qualities. I discovered the usefulness of recursive function calls. I used it to solve [this](https://www.freecodecamp.com/challenges/steamroller#?solution=function%20steamrollArray(arr)%20%7B%0A%20%20var%20result%20%3D%20arr.reduce(function(prev%2C%20next)%20%7B%0A%20%20%20%20if%20(Array.isArray(next))%20%7B%0A%20%20%20%20%20%20return%20prev.concat(steamrollArray(next))%3B%0A%20%20%20%20%7D%20%0A%20%20%20%20%20return%20prev.concat(next)%3B%0A%20%20%7D%2C%20%5B%5D)%3B%0A%20%20return%20result%3B%0A%7D%0A%0AsteamrollArray(%5B1%2C%20%5B2%5D%2C%20%5B3%2C%20%5B%5B4%5D%5D%5D%5D)%3B%0A) problem on FreeCodeCamp.**
* What excites or interests you about coding?
  * **One of the things that excites me most about coding is the problem solving aspect. I enjoy overcoming facing and overcoming challenges of all kinds. I have ideas about what the problem is and coding is the process of finding clues that help you come up with the right solution to that problem.**
* What is a recent technical challenge you experienced and how did you solve it? 
  * **I recently came to an MVP for a toy app I am building. In building that app, I encountered many challenges. I was able to overcome them by first, stopping what I was doing and writing down the problem. I then made a list of all the possible causes to that problem. Once the list was complete, I tried each solution in turn until I either solved the problem or ran out of ideas. If I ran out of ideas, I went to the various Slack communities I am a part of to ask for advice.**
* What UI, Security, Performance, SEO, Maintainability or Technology considerations do you make while building a web application or site?
* Talk about your preferred development environment.
* Which version control systems are you familiar with?
  * **I have a working knowledge of Git and Github. On every project I work on I try to emulate the Github workflow as best I can, while working by myself. This includes creating branches for new features, submitting pull requests, and entering all the changes I want to make as issues.**
* Can you describe your workflow when you create a web page?
  * **It would depend on the scale of the project. If I am just making a one of landing page, I would use HTML, CSS or Sass, and vanilla JavaScript. If the project called for a SPA, I would bring in complexities as they became necessary.**
* If you have 5 different stylesheets, how would you best integrate them into the site?
  * **If those stylesheets were each for a single web page I would load them in a link tag on each corresponding page. If they all contained styles used on different pages, like in the case of Sass files, I would import them all into a `main.scss`, compile and minify that file, and include it on all web pages.**
* Can you describe the difference between progressive enhancement and graceful degradation?
  * **These are two approaches to making the web usable and enjoyable for all. Progressive enhancement is the idea that you should start with base functionality that will work in most, if not all browsers, including older versions of IE. Once you have this baseline, you begin to take advantage of the power of modern browsers and add functionality, or _Progressively Enhance_, for users on those platforms. Graceful Degradation works in the opposite direction. You begin with the highest level of functionality you can on modern browsers. If these features are not available on a user's browser you give them a fallback, or _Gracefully Degrade_ the experience to the best you can with on that platform.**
* How would you optimize a website's assets/resources?
  * **Different website assets can be optimized in different ways. For instance, you could host images on a CDN to have your images served from different servers depending on the user's relative position and the server's availability. When optimizing assets such as CSS or JavaScript, it is good practice to concatenate and minify the files to reduce the number of requests to the server and the overall size of the files.**
* How many resources will a browser download from a given domain at a time?
  * **According to [this](https://www.maxcdn.com/one/visual-glossary/domain-sharding-2/) article, the average limit on modern browsers is 6 concurrent downloads per domain.**
  * What are the exceptions?
    * **Since the limit is per domain, serving content from different subdomains would reset the limit. However, as the above article points out, this can produce a performance loss due to the additional DNS lookups the browser would have to perform.**
* Name 3 ways to decrease page load (perceived or actual load time).
  * **You should optimize your assets as discussed above. Placing links to CSS files in the head of your document and links to JavaScript files at the end of the body, will make the page appear to load faster, as the styles will appear almost instantaneously, but the 'heavy' JavaScript files will load only after the body has finished. Priotritizing the content seen before the user scrolls down the page will decrease perceived load time.**
* If you jumped on a project and they used tabs and you used spaces, what would you do?
* Describe how you would create a simple slideshow page.
* If you could master one technology this year, what would it be?
* Explain the importance of standards and standards bodies.
* What is Flash of Unstyled Content? How do you avoid FOUC?
* Explain what ARIA and screenreaders are, and how to make a website accessible.
* Explain some of the pros and cons for CSS animations versus JavaScript animations.
* What does CORS stand for and what issue does it address?

#### HTML Questions:

* What does a `doctype` do?
  * **It tells the web browser which version of HTML you are using. In HTML5 it is `<!DOCTYPE html>`**
* What's the difference between full standards mode, almost standards mode and quirks mode?
  * **Quirks mode is for websites built before the adoption of web standards. Standards mode is for modern standards compliant browsers and is activated by the doctype declaration from the previous answer. Almost Standards mode is for websites that have a few holdout practices from the era before web standards.**
* What's the difference between HTML and XHTML?
  * **XHTML has a stricter syntax than HTML.**
* Are there any problems with serving pages as `application/xhtml+xml`?
  * **If you serve a page as `application/xhtml+xml` it must meet the stricter syntax of XHTML. So, there is not necessarily a downside to serving the content that way you just have to be more conscious of how you structure the files served that way.**
* How do you serve a page with content in multiple languages?
  * **The language of an entire page can be set by adding the `<html lang="">` to the document's head. Within and individual page you can set the language for specific content by adding a `lang=""` attribute to any element.**
* What kind of things must you be wary of when design or developing for multilingual sites?
* What are `data-` attributes good for?
  * **You can store relevent information about a given element in the data attribute and access that with JavaScript using `element.dataset.value`.**
* Consider HTML5 as an open web platform. What are the building blocks of HTML5?
  * **The foundation of HTML5 is the adoption of web standards. Having standards allows all developers to create websites using the agreed upon building blocks of an HTML document such as, the `<head>`, `<body>`, and the plethora of HTML elements.**
* Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.
* Describe the difference between `<script>`, `<script async>` and `<script defer>`.
* Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?
  * **Placing the CSS links in the document's head allows the style for the site to load before the content in the body. This means that the content should be styled as soon as it is rendered to the page, preventing the Flash of unstyled content. Since JavaScript is not essential to displaying the content, placing the script tags at the bottom of the body means it will be loaded only after the content is finished. This lowers the perceived load time for the user.**
* What is progressive rendering?
  * **Customizing the way in which your HTML is rendered to the page. This can include lazy loading images as they come into view instead of loading all images at page load.**
* Have you used different HTML templating languages before?
  * **I have used Jade and Liquid templating language with Jekyll.**

#### CSS Questions:

* What is the difference between classes and IDs in CSS?
* What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?
* Describe Floats and how they work.
* Describe z-index and how stacking context is formed.
* Describe BFC(Block Formatting Context) and how it works.
* What are the various clearing techniques and which is appropriate for what context?
* Explain CSS sprites, and how you would implement them on a page or site.
* What are your favourite image replacement techniques and which do you use when?
* How would you approach fixing browser-specific styling issues?
* How do you serve your pages for feature-constrained browsers?
  * What techniques/processes do you use?
* What are the different ways to visually hide content (and make it available only for screen readers)?
* Have you ever used a grid system, and if so, what do you prefer?
* Have you used or implemented media queries or mobile specific layouts/CSS?
* Are you familiar with styling SVG?
* How do you optimize your webpages for print?
* What are some of the "gotchas" for writing efficient CSS?
* What are the advantages/disadvantages of using CSS preprocessors?
  * Describe what you like and dislike about the CSS preprocessors you have used.
* How would you implement a web design comp that uses non-standard fonts?
* Explain how a browser determines what elements match a CSS selector.
* Describe pseudo-elements and discuss what they are used for.
* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
* What does ```* { box-sizing: border-box; }``` do? What are its advantages?
* List as many values for the display property that you can remember.
* What's the difference between inline and inline-block?
* What's the difference between a relative, fixed, absolute and statically positioned element?
* The 'C' in CSS stands for Cascading.  How is priority determined in assigning styles (a few examples)?  How can you use this system to your advantage?
* What existing CSS frameworks have you used locally, or in production? How would you change/improve them?
* Have you played around with the new CSS Flexbox or Grid specs?
* How is responsive design different from adaptive design?
* Have you ever worked with retina graphics? If so, when and what techniques did you use?
* Is there any reason you'd want to use `translate()` instead of *absolute positioning*, or vice-versa? And why?

#### JS Questions:

* Explain event delegation
  * **Event delegation is the process of adding and event listener to a parent element and having all events triggered by its children delegate to the parent. An example would be adding an event listener for click events to an `<ul>`. When one of the `<ul>`'s child `<li>` elements is clicked it will dispatch an event that will be delegated to the parent. The event listener on the parent can then check the target of the event and perform whatever action is desired.**
* Explain how `this` works in JavaScript
  * **In JavaScript `this` refers to the object that invoked the function, also known as the context of the function. I can be used to reference the object from within the function. It changes implicitly by where/how a function was called and explicitly by `Function.prototype.call()` and `Function.prototype.apply()`. Arrow functions in ES6/ES2015 bind `this` to the enclosing scope context upon declaration and its context can not be changed with either `call` or `apply`.**
* Explain how prototypal inheritance works
  * **I gave an example of prototypal inheritance [here](https://github.com/RyanWillDev/interview-prep/blob/master/10-int-ques-js/q-1.md#prototypal-inheritance), but will sum it up here. Instead of having a hierarchical inheritance structure JavaScript's prototypal inheritance related objects are more like siblings linked by the prototype chain. If you try to access a method or property on the object at the end of the chain that doesn't exist it will stop at every link on the chain to see if the property or method exists there. Kyle Simpson calls this _Behavior Delegation_.**
* What do you think of AMD vs CommonJS?
* Explain why the following doesn't work as an IIFE: `function foo(){ }();`.
  * What needs to be changed to properly make it an IIFE?
* What's the difference between a variable that is: `null`, `undefined` or undeclared?
  * How would you go about checking for any of these states?
* What is a closure, and how/why would you use one?
* What's a typical use case for anonymous functions?
  * **Anonymous functions are typically used for callback function such as:**
  ```javascript
  function foo(str, callback) {
    callback();
  }
  
  var string = 'I am a string!';

  foo(string, function() {
    console.log(string);
  });
  ```
* How do you organize your code? (module pattern, classical inheritance?)
* What's the difference between host objects and native objects?
  * **Host Objects are specific to the environment that JavaScript is running in. The window object in the browser is an example of a host object. While objects like `Object`, `Date`, `Array` are native to the JavaScript language and are available no matter the environment.**
* Difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?
* What's the difference between `.call` and `.apply`?
  * **`.call` and `.apply` are similar in that they both allow a developer to change the `this` context of a function and pass in arguments to call the function with. They differ in how you pass the arguments. `.call` expects a `this` context as its first argument followed by a comma separated list of arguments ex: `foo.call(objectForNewThisContext, 1, 2, 3)`. `.apply` expects the first argument to be a this context just like `.call`, but it expects an Array of arguments as its second argument ex: `foo.apply(objectForNewThisContext, [1, 2, 3])`. With both function methods you can pass `null` as the first argument to keep the default `this` context ex: `foo.call(null, 1, 2, 3)`.**
* Explain `Function.prototype.bind`.
  * **`.bind` is similar to `.apply` and `.call` from the previous answer. The only difference being it returns a function that has its `this` context and arguments permanently bound, while `.apply` and `.call` immediately call the function with the context and arguments passed to them. So, you would store the result of calling bind on a function in a variable ex: `var boundFoo = foo.bind(null, 1, 2, 3);`. Now, anytime you call `boundFoo` it will use the `this` context and arguments bound to it.**
* When would you use `document.write()`?
  * **When you want to replace the entirety of the documents content.**
* What's the difference between feature detection, feature inference, and using the UA string?
* Explain Ajax in as much detail as possible.
  * **AJAX uses an XMLHttpRequest to asynchronously request additional data from a server. This means it sends the request and continues executing the code, until the requested data is received and only then act on it. This technique is typically used to load additional data to the page without having to redirect the user.**
* What are the advantages and disadvantages of using Ajax?
  * **One advantage of using AJAX is you can wait and load data only when you need it. When the document initially renders it only loads the absolute essentials. If during the user's interactions with the page they need more data, you can load then. The biggest disadvantage is that it relies on JavaScript. If a user has disabled JavaScript in their browser you would not be able to load the data via AJAX.**
* Explain how JSONP works (and how it's not really Ajax).
* Have you ever used JavaScript templating?
  * If so, what libraries have you used?
* Explain "hoisting".
* Describe event bubbling.
* What's the difference between an "attribute" and a "property"?
* Why is extending built-in JavaScript objects not a good idea?
* Difference between document load event and document DOMContentLoaded event?
* What is the difference between `==` and `===`?
* Explain the same-origin policy with regards to JavaScript.
* Make this work:
```javascript
duplicate([1,2,3,4,5]); // [1,2,3,4,5,1,2,3,4,5]
```
  * **Answer:**
```javascript
  function duplicate(arr) {
    return arr.concat(arr);
  }
```
* Why is it called a Ternary expression, what does the word "Ternary" indicate?
* What is `"use strict";`? what are the advantages and disadvantages to using it?
* Create a for loop that iterates up to `100` while outputting **"fizz"** at multiples of `3`, **"buzz"** at multiples of `5` and **"fizzbuzz"** at multiples of `3` and `5`
  * 
  ```javascript
  for (i = 0; i < 100; i++) {
    if (i % 3 === 0 && i % 5 === 0) {
      console.log('FizzBuzz');
    } else if (i % 3 === 0) {
      console.log('Fizz');
    } else if (i % 5 === 0) {
      console.log('Buzz')
    } else {
      console.log(i);
    }
  }
```
* Why is it, in general, a good idea to leave the global scope of a website as-is and never touch it?
* Why would you use something like the `load` event? Does this event have disadvantages? Do you know any alternatives, and why would you use those?
* Explain what a single page app is and how to make one SEO-friendly.
* What is the extent of your experience with Promises and/or their polyfills?
* What are the pros and cons of using Promises instead of callbacks?
* What are some of the advantages/disadvantages of writing JavaScript code in a language that compiles to JavaScript?
* What tools and techniques do you use debugging JavaScript code?
* What language constructions do you use for iterating over object properties and array items?
* Explain the difference between mutable and immutable objects.
  * What is an example of an immutable object in JavaScript?
  * What are the pros and cons of immutability?
  * How can you achieve immutability in your own code?
* Explain the difference between synchronous and asynchronous functions.
* What is event loop?
  * What is the difference between call stack and task queue?
* Explain the differences on the usage of `foo` between `function foo() {}` and `var foo = function() {}`

#### Testing Questions:

* What are some advantages/disadvantages to testing your code?
* What tools would you use to test your code's functionality?
* What is the difference between a unit test and a functional/integration test?
* What is the purpose of a code style linting tool?

#### Performance Questions:

* What tools would you use to find a performance bug in your code?
* What are some ways you may improve your website's scrolling performance?
* Explain the difference between layout, painting and compositing.

#### Network Questions:

* Traditionally, why has it been better to serve site assets from multiple domains?
* Do your best to describe the process from the time you type in a website's URL to it finishing loading on your screen.
* What are the differences between Long-Polling, Websockets and Server-Sent Events?
* Explain the following request and response headers:
  * Diff. between Expires, Date, Age and If-Modified-...
  * Do Not Track
  * Cache-Control
  * Transfer-Encoding
  * ETag
  * X-Frame-Options
* What are HTTP methods? List all HTTP methods that you know, and explain them.

#### Coding Questions:

*Question: What is the value of `foo`?*
```javascript
var foo = 10 + '20';
```

*Question: How would you make this work?*
```javascript
add(2, 5); // 7
add(2)(5); // 7
```

*Question: What value is returned from the following statement?*
```javascript
"i'm a lasagna hog".split("").reverse().join("");
```

*Question: What is the value of `window.foo`?*
```javascript
( window.foo || ( window.foo = "bar" ) );
```

*Question: What is the outcome of the two alerts below?*
```javascript
var foo = "Hello";
(function() {
  var bar = " World";
  alert(foo + bar);
})();
alert(foo + bar);
```

*Question: What is the value of `foo.length`?*
```javascript
var foo = [];
foo.push(1);
foo.push(2);
```

*Question: What is the value of `foo.x`?*
```javascript
var foo = {n: 1};
var bar = foo;
foo.x = foo = {n: 2};
```

*Question: What does the following code print?*
```javascript
console.log('one');
setTimeout(function() {
  console.log('two');
}, 0);
console.log('three');
```

#### Fun Questions:

* What's a cool project that you've recently worked on?
* What are some things you like about the developer tools you use?
* Who inspires you in the front-end community?
* Do you have any pet projects? What kind?
* What's your favorite feature of Internet Explorer?
* How do you like your coffee?


#### Contributors:

This document started in 2009 as a collaboration of [@paul_irish](https://twitter.com/paul_irish) [@bentruyman](https://twitter.com/bentruyman) [@cowboy](https://twitter.com/cowboy) [@ajpiano](https://twitter.com/ajpiano)  [@SlexAxton](https://twitter.com/slexaxton) [@boazsender](https://twitter.com/boazsender) [@miketaylr](https://twitter.com/miketaylr) [@vladikoff](https://twitter.com/vladikoff) [@gf3](https://twitter.com/gf3) [@jon_neal](https://twitter.com/jon_neal) [@sambreed](https://twitter.com/sambreed) and [@iansym](https://twitter.com/iansym).

It has since received contributions from over [100 developers](https://github.com/h5bp/Front-end-Developer-Interview-Questions/graphs/contributors).