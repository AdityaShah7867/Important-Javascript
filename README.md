# Important Concepts of JavaScript. 



JavaScript is a dynamic computer programming language. It is lightweight and most commonly used as a part of web pages, whose implementations allow client-side script to interact with the user and make dynamic pages. It is an interpreted programming language with object-oriented capabilities.

JavaScript was first known as LiveScript, but Netscape changed its name to JavaScript, possibly because of the excitement being generated by Java. JavaScript made its first appearance in Netscape 2.0 in 1995 with the name LiveScript. The general-purpose core of the language has been embedded in Netscape, Internet Explorer, and other web browsers.

Advantages of JavaScript, The merits of using JavaScript are −

1.Less server interaction − You can validate user input before sending the page off to the server. This saves server traffic, which means less load on your server.

2.Immediate feedback to the visitors − They don't have to wait for a page reload to see if they have forgotten to enter something.

3.Increased interactivity − You can create interfaces that react when the user hovers over them with a mouse or activates them via the keyboard.

4.Richer interfaces − You can use JavaScript to include such items as drag-and-drop components and sliders to give a Rich Interface to your site visitors.

Limitations of JavaScript-

1.We cannot treat JavaScript as a full-fledged programming language. It lacks the following important features −

2.Client-side JavaScript does not allow the reading or writing of files. This has been kept for security reason.

3.JavaScript cannot be used for networking applications because there is no such support available.

4.JavaScript doesn't have any multi-threading or multiprocessor capabilities.

# JavaScript single-threaded model
JavaScript is a single-threaded programming language. This means that JavaScript can do only one thing at a single point in time.
The JavaScript engine executes a script from the top of the file and works its way down. It creates the execution contexts, pushes, and pops functions onto and off the call stack in the execution phase. 

If a function takes a long time to execute, you cannot interact with the web browser during the function’s execution because the page hangs.
A function that takes a long time to complete is called a blocking function. Technically, a blocking function blocks all the interactions on the webpage, such as mouse click.


The web browser also has other components, not just the JavaScript engine.

When you call the setTimeout() function, make a fetch request, or click a button, the web browser can do these activities concurrently and asynchronously.

The setTimeout(), fetch requests, and DOM events are parts of the Web APIs of the web browser.

In our example, when calling the setTimeout() function, the JavaScript engine places it on the call stack, and the Web API creates a timer that expires in 1 second.

![javascript-event-loop-step-1](https://github.com/AdityaShah7867/Important-Javascript/assets/121731399/a8f3c65b-d31b-42c5-a369-c687380a89c5)

Then JavaScript engine place the task() function is into a queue called a callback queue or a task queue:

![javascript-event-loop-step-2 (1)](https://github.com/AdityaShah7867/Important-Javascript/assets/121731399/cfc1a8e6-e916-4b75-8b01-ccce39086270)

The event loop is a constantly running process that monitors both the callback queue and the call stack.

If the call stack is not empty, the event loop waits until it is empty and places the next function from the callback queue to the call stack. If the callback queue is empty, nothing will happen:

![javascript-event-loop-step-3](https://github.com/AdityaShah7867/Important-Javascript/assets/121731399/76c6cbbd-7aee-4b00-94f1-1d2dc63dd3b9)


#What is asynchronous Javascript?

Asynchronicity means that if JavaScript has to wait for an operation to complete, it will execute the rest of the code while waiting.

Note that JavaScript is single-threaded. This means that it carries out asynchronous operations via the callback queue and event loop.

In synchronous JavaScript, each function is performed in turn, waiting for the previous one to complete before executing the subsequent one. Synchronous code is written from top to bottom.

![68747470733a2f2f692e696d6775722e636f6d2f45596a414b4d422e706e67-768x576](https://github.com/AdityaShah7867/Important-Javascript/assets/121731399/06b703f7-f4bf-4680-9106-39b3632836df)


To understand what synchronous JavaScript means, let us consider the code snippet below.

//synchronous javascript

console.log("synchronous.");

console.log("synchronous javascript!")

console.log("synchronous again!")
If we go ahead and run the above code, we get:

//Output

"synchronous"
"synchronous javascript!"
"synchronous again!"
This shows that synchronous JavaScript runs from top to bottom, as we can observe the console running the function linearly from top to bottom.

With the code above, the console first logs synchronous to the terminal, then synchronous javascript! and synchronous again!. This is an example of synchronous JavaScript since the program executes code in the order it is written.
















[Useful website](https://www.javascripttutorial.net/javascript-event-loop/)
