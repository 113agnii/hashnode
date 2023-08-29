---
title: "who, what, why, where, when, and how. All about JavaScript Functions."
seoTitle: "who, what, why, where, when, and how, All about JS Functions.details"
seoDescription: "Finally a JavaScript blog that you can actually read"
datePublished: Mon Aug 28 2023 15:11:05 GMT+0000 (Coordinated Universal Time)
cuid: cllv0of6k000e08jr2clp7dd6
slug: who-what-why-where-when-and-how-all-about-js-functions
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1693236290450/914499a6-5b30-4e45-99e4-fd30c0d691d8.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1693237290032/7e1d4cdf-4eba-4217-95f7-95eb18e69f8b.png
tags: javascript, reactjs, javascript-framework, javascript-modules, wemakedevs

---

## Why Do we need functions?

Functions serve as a way to encapsulate a set of instructions into a single unit that can be invoked and reused throughout your code. Imagine you have a block of code that you use repeatedly. `(Alright... alright... Don't leave, this article is worth a read. Just stick around for a little while.)` Instead of copying and pasting it every time, you can place it within a function and simply call that function whenever you need to execute that code. This not only promotes code reusability but also enhances the readability and maintainability of your codebase, making it easier to manage, debug, and update as your project grows.

## How to declare a function?

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692948419966/c9be6cb3-440b-4bd4-8fd9-230a22e479a7.png align="center")

FunctionName is like a nickname you give someone – it helps you recognize and *call* them. Just like you might say "Adarsh" or "heyBaby!"

In some situations, functions can work without a name at all, so keep that in mind.

## Difference between Function Declaration &

## Definition?

You've probably heard programmers say, "I've declared a function" or "I've defined the function." These phrases are pretty much the same thing.

Now, let's take the next step and declare a function ourselves.

```javascript
function printMe(){
console.log('printing...')
}
```

To make this function work, you need to *'call'* or '*invoke'* it. Think of how you call someone in real life – you use their name. Right? Similarly, to use our function, you simply call it by its name.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692949828732/25b1f625-00a5-4b0c-a3a6-4fe41d61f158.png align="center")

**But here's the catch:** if you just write the function's name in JavaScript, it won't give you the result you expect. Instead, you'll see the entire function body as a *"string"* version of the function definition.

To get the desired result, you must use parentheses `()` after the function name.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692950028914/1b9ef365-67a5-4f67-ac42-ea542789278c.png align="center")

## What is the difference between Parameters and arguments?

Now, let's dig into a key concept: parameters and arguments. Think of parameters as variables waiting to be filled in a function, and when we use the function, we provide actual values, which are the arguments.

It's a bit like when you ask a friend for money, you ask a particular amount (parameter), and they start abusing you (argument). So, let's put this into practice by adding parameters to our function and passing in argument values.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692952337592/d9e96bca-2e90-4384-934c-0eb67d176857.png align="center")

## How to define Function Expressions?

Now that we've got a grip on a function declaration and passing values, let's explore another method of defining functions using a function expression.

Think of function expression as assigning value to a variable.

For those who might not be familiar, JavaScript has three types of variables:

1. **const**: This is used for values that won't change.
    
2. **let** and **var**: These are used for values that can change. We'll dive deeper into these when we explore function scope, but for now, let's keep it at that.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692952994491/c63d0977-dc87-45ad-992e-a6f895923347.png align="left")
    

So, in a function expression, we're kind of swapping out variables with functions. variable name turning into the function's name, and instead of a regular value, we're putting an entire function in its place

```javascript
const printMe = function(){
console.log("this is function expression");
}

printme()

//output:
//this is function expression
```

Now, let's take our understanding of function expressions a step further by using parameters and arguments.

```javascript
const printMe = function(a,b,c,d,e,f) {
console.log(a,b,c,d,e,f);
}

printMe(10,20,30,40,50,60)
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692954016089/1c86d9ac-8a48-4d6c-84d3-85a0d5852c02.png align="center")

If you're paying close attention, you might have realized that we can treat functions as values in JavaScript. In programming languages that treat functions as values, these functions are referred to as `first-class citizens.`

## How to return from a function

Imagine we have two functions: Function X and Function Y. Each of them is skilled at doing their own thing.

Now, let's say Function X completes its task and produces a result. Instead of letting that result vanish into thin air, we can save it for later. This saved result can be used when we call Function Y.

```javascript
function x(){
/*-----------------
---Their own task--
-------------------*/
}
const p = x(); //saving for future use 

function y(){
/*-----------------
---Their own task--
-------------------*/
}
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692955861058/8013a8bb-1714-4239-91ff-1c53c0d4b29c.gif align="center")

Now, let's dive into the code to gain a deeper understanding. Go through each step with specific numbers, making it easier to grasp the concept more effectively.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692969169745/15edb769-2d7d-47fd-8799-93f98b836046.png align="center")

## What are default parameters?

What if the function doesn't return any value?

For example, if you forget to provide the necessary arguments that a function expects, the function will still execute, but the function's execution will result in a special value called "undefined" or "nan" (not a number).

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692970016179/53ab00ee-33cb-496d-8b13-a2fe65165a1d.png align="left")

That brings us to our new topic Default Parameters.

We can use the default parameters value for a function if it's required to safeguard it from an unnatural value returning from the function. Let's understand better with the code.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692970921349/5aabf7e9-bf29-4229-a70a-8b8ec4bb2505.png align="center")

Now what will happen if we only pass one argument?

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692971083484/bc59dd9b-72ff-437f-b1f4-bc2c58547260.png align="center")

Now in this case you are not passing the second argument, So *b will be undefined*

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692971423913/97e3d04c-fae7-4f30-8bf0-fd95af87b008.png align="center")

So we can safeguard our parameters with some kind of default values, something that you like.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692971679973/5e143e0c-6dbf-4fbb-87ac-428330bd979a.png align="center")

## What are Rest Parameters?

The rest parameter is something that allows a function to accept any number & infinite number of arguments as an `array`.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692976355327/0b8f913c-8750-46a2-a19d-68de9686f854.png align="center")

Just remember, you can use only one rest parameter and it must be the last one in the list of parameters.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692976635877/acad5892-03d7-4fbd-bf83-43639d73eaa5.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692976832546/318c6beb-4994-4ac7-9f2d-5540145d5f55.png align="center")

## How to define Arrow Functions?

`Arrow functions` or `fat-arrow syntax` we know how to define a function with the function expression.

```javascript
const add = function (x,y){
return x+y;
}
```

Let's take a look at converting a regular function expression to an arrow function, with a few adjustments that you have to make.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692978240230/cebefd35-9d63-461f-a312-90b2fb8c123d.png align="center")

If the arrow function body contains just one statement, you can skip adding curly braces.

```javascript
const add = (x,y) => x+y;
```

And if you're dealing with just one parameter, you can leave out the parentheses as well.

```javascript
const add = x => x;
```

## What is the Execution context in JavaScript?

Whenever a function is executed it creates its imaginary container. Imagine each function as having its little room. This room holds everything the function needs while it's working. It's like a workspace where the function can access its tools (variables and functions) and look out the window to see what's happening around it (scope chain). This setup ensures that each function can do its job without getting mixed up with other functions.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692998139747/e1998da7-72f9-45fc-9546-0812cf1aaae0.png align="center")

## How scopes are different in variables?

In JavaScript, we commonly use three types of variables, Let's delve into these differences with some code examples

`var`, `let`, and `const`. `var` was introduced in ES5, and `let` and `const` were introduced in ES6.

Variables declared with `var` have a function scope, making them accessible throughout the entire function they're declared in.

variables declared with `const` have block scope, limiting their visibility to the specific block or curly braces `{}` in which they are defined.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692983148030/6eaed011-6cd9-48ac-b3b2-4309fcb9de81.png align="center")

`var` attaches itself to the global `window` object, which can lead to data leakage and global variable interference across different parts of your code or even other pages.

`let` and `const`, are more localized and prevent unintended global scope issues.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692991324049/7eb4432d-19f6-408b-8522-240757ee5c74.png align="center")

## What is a window object?

JavaScript can use certain features that aren't even included in the programming language itself. These functionalities are made available by browsers like Chrome, Safari, and others through objects like the window object.

`console`, `prompt`, `onclick` etc. are all components of the window object. While they're not built directly into JavaScript itself, they are provided by browsers.

We can use them in our JavaScript code to enhance our web applications, even though they're not a fundamental part of the core JavaScript language.

It's worth noting that there are additional objects beyond the `window object` as well.

![JavaScript Browser Object Model - Studytonight](https://s3.ap-south-1.amazonaws.com/s3.studytonight.com/tutorials/uploads/pictures/1588941307-1.png align="center")

## What are Nested Functions?

What does nested mean? We know how to define a function

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693028371276/f3232361-86d4-4135-be17-da7d56fbad34.png align="center")

In JavaScript, you can make a function inside another function. This is like the first puzzle piece for understanding something cool called 'closure.' And if you're curious about closures, start by getting comfortable with nested functions – that's one function inside another.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693030807377/43fc7a22-0dcc-417a-92ed-6da829acccd4.png align="center")

Let's find out why we're seeing a 'ReferenceError,' which brings us to our next topic: function scope.

## What is the scope of a Function?

Let's make it clear. You've got to know two important rules, especially if you're digging into closures. Ready?

1. **Variables Scoped Within Functions:** Variables that are defined inside a function can not be accessed outside of the function.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692983148030/6eaed011-6cd9-48ac-b3b2-4309fcb9de81.png align="left")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693036826658/d9808d73-4950-4446-9eff-e39fd9b4d75b.png align="center")

1. **The opposite of it:** A function can access anything and everything inside the scope it is defined.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693041855559/e990d6f1-2dd6-4ef6-a357-ce5f7f90f150.png align="center")

Function scope is about what variables a particular function can access. If you have a variable defined inside a function, it's like a secret that only that function knows. Other functions can't peek into that secret unless it's shared.

![Take A Break GIFs | Tenor](https://media.tenor.com/P28XK2uKbIwAAAAM/you-can-take-a-break-now-nicola-foti.gif align="center")

## What is Lexical Scope?

Let's use code to make this clearer. It's all revision boys!

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693045022642/1c97fbde-c518-4e77-8e8e-d5594cfcf161.png align="center")

All the details about which function can access which variables and how the scope hierarchy is structured are stored in something called the `lexical environment.` It's like a map that keeps track of who can access what, ensuring that each function knows its scope boundaries and which variables it can reach. This lexical environment is a behind-the-scenes assistant that helps JavaScript keep everything organized and prevents variables from wandering where they shouldn't be.

### How does the Scope Chain work?

If one scope needs to use a certain variable but cannot find it in the scope, it will look up in the scope chain and check whether it can find a variable on one of the outer scopes. If the variable is available in the outer scope, then the child scope has access to it. If it is not there in any outer scopes, the JavaScript will throw a reference error. So this process is called *variable lookup*.

Let's understand better with some code.

We're invoking the `getPersonInfo` function, which returns a string containing the values of the `name`, `age` and `city` variables:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693129644538/dc59f3c7-9eaf-471b-b1bc-80146e96ea4f.png align="center")

First, memory space is set up for the different contexts. Understand context as some rooms. The scope chain gets created when the execution context (like here `getPersonInfo()` is called ) is created, meaning it's created at runtime! and each room is like a mini-environment that holds variables and functions.

Mainly there are two types of contexts in the scope chain: the global context and local contexts (execution contexts) created when functions are called.

We have the default **global context** (`window` in a browser, `global` in Node), and a **local context** for the `getPersonInfo` function which has been invoked. Each context also has a **scope chain**.

For the `getPersonInfo` function, the scope chain looks something like this (don't worry, it doesn't have to make sense just yet):

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693132589429/cb7383b0-c014-42c4-ba31-10676c3cde55.png align="left")

The scope chain is like a "sequence of references" (connections) to objects. These objects contain information about references to values and other scopes that can be accessed within a specific part of your code.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693132170868/435e5425-5228-4818-8014-3724ef5197ef.png align="center")

What will happen when it tries to access the `city`?

![Alt Text](https://res.cloudinary.com/practicaldev/image/fetch/s--9A6d4z3e--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_66%2Cw_800/https://thepracticaldev.s3.amazonaws.com/i/xn17f0t54acz8tiq7122.gif align="center")

JS engine doesn't give up that easily: it works hard for you to see if it can find a value for the variable `city` in the outer scope that the local scope has a reference to until it hits the **global object**.

![Alt Text](https://res.cloudinary.com/practicaldev/image/fetch/s--mjJbIqM6--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_66%2Cw_800/https://thepracticaldev.s3.amazonaws.com/i/z9iclg23rmbpts7meoq6.gif align="center")

Now that we have a value for the variable, the function `getPersonInfo` can return the string `Sarah is 22 and lives in San Francisco`

Let's take another code as an example.

![Alt Text](https://res.cloudinary.com/practicaldev/image/fetch/s--xb-kf0ML--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_800/https://thepracticaldev.s3.amazonaws.com/i/0z6342b72f3n6v6ufafk.png align="center")

[  
](https://res.cloudinary.com/practicaldev/image/fetch/s--Ya80sAQN--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_800/https://thepracticaldev.s3.amazonaws.com/i/89b9buizhevs0jf6djyn.png)It's almost the same, however, there's one big difference: we *only* declared a `city` in the `getPersonInfo` function now, and *not* in the global scope. We didn't invoke the `getPersonInfo` function, so no local context is created either. Yet, we try to access the values of `name`, `age` and `city` in the global context.

(Rule 2: You can go to **outer** scopes, but not to more inner... scopes.)

![Alt Text](https://res.cloudinary.com/practicaldev/image/fetch/s--PQt7f7YR--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_66%2Cw_800/https://thepracticaldev.s3.amazonaws.com/i/f3wvlo4c3gqf3mve1g0n.gif align="center")

Quick Recap:

1. JavaScript starts looking for a variable from where you're standing.
    
2. If it doesn't find it, it goes up one level in the scope chain and checks again.
    
3. This repeats until the variable is found or it reaches the global scope.
    

## What are Closures?

Closure is nothing but a nested function.

![YARN | | | Video gifs by quotes | 0f0c6828 | 紗](https://y.yarn.co/0f0c6828-58c5-4cc3-8a78-7c246b77342e_text.gif align="center")

Wait! Wait! Why all the hype about the closure then?

Closure understanding depends on your understanding of nested functions & function scopes.

1. Closures are functions that have access to variables from another function's scope. This is accomplished by creating a function inside another function.
    
2. A Closure is a function that returns another function.
    
3. A Closure is an implicit, permanent link between a function and its scope chain.
    
    So, closure is nothing but a nested function.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693136816049/77d64342-4529-4266-98b0-df37036eb1e7.png align="center")

What we basically do in closure is call the `outer` function, specify an `argument`, and then leverage both the inner and outer functions together.

Now what will happen if I call `outer` function in the same code with an argument?

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693138225016/72b95c50-24f5-4374-a04c-c8355fbc7d8d.png align="center")

So what does `outerReturn` now contains?

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693138715810/ee91feb8-44fb-48ab-8c12-2b97b6e0e8c1.png align="center")

Though the execution of `x` is over, the value that we have passed through the `outer` function still lives inside the `inner` function.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693143307980/eefcd555-00cf-433c-96ae-9842ad371b71.png align="center")

A closure is a way in JavaScript that a function can remember and access its outer variables, even after the function has finished executing. It's like a little memory bubble that lets functions hold onto things they need, even if they're done doing their main job. So, closures are like JavaScript's superpower for managing data and making sure functions play nice with each other.

## What is a callback function?

* **We have created functions:** `function definition`
    
* **We have assigned functions:** `function expression`
    
* **We have defined functions in another function:** `Nested functions`
    

Now we are going to pass the function as a `parameter` to another function.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693160540305/e9b8803a-dd9e-48bf-8af3-2ca566d2d8c7.png align="center")

if `bar` had been a string I would have printed it, right? If it was a number I could have done maths around it. So if it is a function then I can execute it. Right?

How do I execute this?

Now I know that `foo` takes a function, so I can pass a function to it.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693202189545/107f0cdc-f8d7-4675-bd1d-6b9058fa84c0.png align="center")

**A** `callback function` **is a function that is passed as an** `argument` **to another function and is intended to be executed later.**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693217182910/0dde033d-ffc0-4431-af28-a585c712608a.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693205867587/c10a9de8-480d-4fc6-8f60-33441b0faeef.png align="center")

We can do this more directly by using `anonymous functions`.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693202189545/107f0cdc-f8d7-4675-bd1d-6b9058fa84c0.png align="left")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693202874752/8c9efe57-5109-46f6-8f8b-7153176787db.png align="left")

Notice, that we have created a function without any name, this function is called an `anonymous function`, If you remember our chat on "how we declare functions?", this might ring a bell.

## `setTimeout`

It is a built-in JavaScript function that allows you to schedule the execution of a function after a specified amount of time. It's basically what we learned with a time delay feature.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693219862715/7c9c8961-d064-4367-96b3-085b7a14b11c.png align="center")

So, now this code will run after 10 seconds. It will come in handy when we learn Async programming.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693235609341/2838f6ef-e85a-4557-9d14-656cafcad9dd.gif align="center")

Now just to make it all things clear. We will improvise our previous example with setTimeout.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693220406021/48b3df0a-c3d4-49fa-bc0f-f46986712f0a.png align="center")

# What are higher-order Functions?

A higher-order function is a special type of function that does one of two things: it either takes another function as an input or returns a function as its output.

You might recall this concept from our discussion on callback functions, where we touched on the idea. However, not all callback functions are necessarily higher-order functions.

If you're curious to learn more, you can explore topics like pure and impure functions, as well as Immediately Invoked Function Expressions (IIFE) on your own.

Keep this blog as a reference because I might update more function-related concepts of JS in this blog. Happy learning!

Special thanks: Lydia Hallie