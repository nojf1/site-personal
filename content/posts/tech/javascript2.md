---
title: "JavaScript functions"
date: 2025-06-10
draft: false
description: "JS"
tags: ["JavaScript", "Let's Learn"]
summary: "A review of my understanding of JavaScript, part 2"
series: ["Learning JavaScript!"]
series_order: 2
---

## A quick disclaimer!

Whatever information here may be factually incorrect because I write them from my own honest understanding. If you are not familiar with the topic, I encourage you to do your own research and form your own conclusions. If you are an expert on the topic though, please contact me if there are any errors or incorrect information here so I can correct them.

Everything written here is extremely simplified, as the purpose of this series is to review my own understanding of the topic.

I may write more detailed explanations on the subject in the future, which I will link to when appropriate.

## JavaScript Functions

Functions are the core of every JavaScript program. To describe it simply, it is a reusable block of JavaScript code you can run anytime in a program by calling it so it carries out a set of instructions described in its code.

Note that you have to **call** it before you can use whatever code is inside of it. Think of it like you're calling somebody's name so they know you want them to do something for you.

A basic function would look something like this:

```
function basicFunction() {
    console.log("I am a function that prints this sentence to the console.");
}
```

To define a function, simply write function then the function name. Function names use camelCase for how naming conventions go. For example, loginHandler and displayResultHere, are proper function names. While there is no exact rule for naming functions and variables, its important to know their naming conventions so that other people can have an easier time looking at your code. Lets just say its standard practice.

Now lets break down a function block:

```
function basicFunction() {

}
```

The above code is an empty function. The parentheses at the end of basicFunction is like a holder for parameters, which you can use to pass in values to a function. You can think of it like passing an input into the function so it uses that input to produce an output. For example, you have a factory that accepts raw materials such as wood (which would be the parameter you're passing into the function), and outputs wooden furniture as the product after processing the wood (which would be the output of the factory's function using the input materials).

A function that does exactly that would look like this:

```
function furnitureFactory(rawMaterial) {
    let finalProduct = rawMaterial + " has been processed into furniture!";
    return finalProduct;
}
```

Alright, now we have a function to make furniture, but now what? A function exists now, so we need to use it. When you define a function, it won't run by itself. If it did, that would be disastrous, to say the least. To run a function, we must call it.

```
furnitureFactory("wood"); // calls the function and passes the string "wood" as argument (input) into the function
console.log(furnitureFactory("wood")); // the console will output "wood has been processed into furniture!"
```

You can try copy and pasting the function into a browser console, then run the function to see if it outputs correctly. Note that in the original function defined it uses the return keyword to output the result, and return does not log anything outwardly. To see the result, you should console log it by passing in the function call as well as a parameter into it.

One thing to note about accepting parameters into functions in JavaScript: the named parameter (rawMaterial) defined in the function is not a variable you can use whenever. Because its defined as a parameter attached in a function, it is limited for that function to use only. I will discuss this more in detail when I write about JavaScript scopes in future parts.

Another thing: remember how in the last article I discussed about how variables in JavaScript are dynamic? It applies to function parameters as well. In Java, you would have to explicitly type the data type before the name of the parameter to be accepted into the Java method (equivalent to JavaScript functions). In JavaScript this is not needed, because the data type will be determined at runtime. This is because JavaScript is an interpreted language (or Just-In-Time compiled, JIT-compiled), meaning JavaScript translates each line of code into machine code (binary language) while its running, instead of compiling before runtime.

To summarise:

```
// this is a function defined with the name "basicFunction"
function basicFunction() { // the parentheses at the end basicFunction are parameters that a function can accept
    console.log("I am a function that prints this sentence to the console.");
} // note that curly braces surround the console.log line, this indicates it is a function code block
```

Functions in JavaScript are something JavaScript developers will regularly work with. And since they're reusable, you can focus on writing a few functions and re-use them later on if you need them to save time.

## Summary

- JavaScript functions are defined with the function keyword.

- It is a reusable block of code that executes a set of instructions within its code block.

- You can pass inputs into the function using parameters.

- You can use the return keyword to send back an output.

- Call the function using its name and parentheses to execute its code block.

In the next part I will discuss more about functions in depth as well as control flow.
