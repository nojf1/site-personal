---
title: "Let's learn JavaScript! Pt. 1"
date: 2025-06-01
draft: false
description: "a description"
tags: ["JavaScript", "Let's Learn"]
summary: "A review of my understanding of JavaScript"
series: ["Learning JavaScript!"]
series_order: 1
---

## A quick disclaimer!

Whatever information here may be factually incorrect because I write them from my own honest understanding. If you are not familiar with the topic, I encourage you to do your own research and form your own conclusions. If you are an expert on the topic though, please contact me if there are any errors or incorrect information here so I can correct them.

Everything written here is extremely simplified, as the purpose of this series is to review my own understanding of the topic.

I may write more detailed explanations on the subject in the future, which I will link to when appropriate.

## A (very) short history of JavaScript, summarised

Born in 1995, JavaScript originally wasn't called JavaScript, it was named LiveScript. Sounds like a foreign language, but make it a programming language.

Since Java was popular at the time of its creation, it was named JavaScript instead, despite largely having no relation to the Java programming language. For marketing reasons, they say.

Originally, JavaScript was meant to add some interactivity to websites. If you knew what websites were like back then, they were totally static and had no way of interacting with the user. No flashy animations, no interactive buttons, no fancy menus, no form of complex functionality. But lets just say it was made as a very, very simple scripting language specifically for browsers.

Later on, JavaScript gained a little more popularity when it was first standardized by ECMA International, giving the name ECMAScript. To put it simply, its just a set of standards to follow when programming with JavaScript. The point of this standard is to make sure web pages operate as intended and smoothly across different web browsers.

After that, more tools and frameworks started popping up, and so JavaScript soon infected almost every website we know today. The thing that really made JavaScript soar in popularity was AJAX (Asynchronous JavaScript And XML), which was popularized by Google who used them in Gmail and Google Maps. Considering how significant Google is in the internet space, the popularity spike made sense.

Fast forward to now, we have many JavaScript frameworks and tools to help us out now, with newer and better standards to follow when programming with JS. It will keep updating and eventually take over the internet I'm sure...

## Wheres JavaScript at?

First, lets understand where exactly JavaScript runs at. If you are familiar with Java, Python etc. you would know they have their own devkits you need to install from their official distributions or somewhere else.

JavaScript is different. Its already in your computer as long as you have a browser installed. I don't know any popular browser that doesn't come with its own JavaScript.

Lets talk Google Chrome. As funny as the jokes about the Chrome browser being a memory hoarder, it actually has the best environment to learn, test, and develop with JavaScript. By default, it comes with the V8 engine when you install Chrome, which is a performant and open-source JavaScript and WebAssembly engine made by Google. Not only that, you have access to Chrome DevTools, which is super useful for testing and debugging.

All you need to do to access DevTools in Chrome is to inspect element. You can open it by right clicking and selecting inspect element, or use the keyboard shortcut CTRL + SHIFT + C (MacOS: CMD + OPTION + I).

In the console tab, you can start writing JavaScript there!

Alternatively, if you want to write JavaScript in a proper IDE, like VS Code, you can do that too as long as its supported.

## Variables in JavaScript

Before we dive into variables, its important you know about the many common data types in programming in general. I recommend reading MDN's article on data types in detail [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Data_structures).

But to summarise data types, theres 8 to know: String, Number, Bigint, Boolean, Undefined, Null, Symbol, Object.

Variables are like those neat color coded recycle bins, paper for paper, metal for metal, plastic for plastic... Every variable has their own role to play, but mostly to store data.

That recycle bin analogy is not that important though. Variables in JS are a bit strange, if you are someone whose first and only programming language was a strongly typed language like Java (take me for example). Since JavaScript is a dynamically typed language, variables are assigned dynamically, not static like in Java, where you need to specify a data type before assigning a variable.

What that means is if you have a boolean data type, you don't type this in JavaScript:

```
boolean thisIsABoolean = true;
```

Theres a few types of keywords you will use instead, one of which is **var**.

```
var thisIsABoolean = true;
```

However, var is largely unused by today's developers for various reasons I will not get into in this article. Alternatively, **let** and **const** is used as the standard for declaring variables.

```
let thisIsAString = "Hello World!";
const thisIsAString = "Const can't be changed after declaration!";
```

There is one important difference between let and const. Const, as you thought, stands for constant. What this means is that the data stored in const cannot be changed after declaration. If you try to do that, JS will politely hand you a TypeError error.

```
const thisIsAConst = 2;
const thisIsAConst = 9289484592; // JS will give you an error on this line
```

Okay... but exactly what are variables for? Remember that recycle bin analogy? Variables are simply containers we store data in, but they each have a purpose. Since we don't need to specify the data type before code compilation, we don't need to say that this recycle bin only receives paper, so we can in a way treat variables like smart recycle bins.

Now with that smart recycle bin we have, we are going to throw a file into it. That file will be stored in that recycle bin temporarily, until its taken to be processed in a recycling facility. While its still in the recycling bin though, you can open the bin, look at whats inside the bin, and even replace whats in the bin, using the **let** keyword (remember you cant reassign variables with const!).

As for when does one use let over const or the other way around, when you have a variable that you think should serve as a temporary placeholder for, lets say, a user input name, you should use let. As for const, normally it is used when you know the value shouldn't be changed, like Pi for example, or specifying the maximum attempts possible in a quiz.

That recycle bin has a name (variable name) and a type (data type). Now, to put it simply, we treat variables as a kind of temporary storage for certain data that we would need to use in **functions**, which I will get into in the next part of this series.

## Summary

Variables are temporary storage bins, used to store various data types. You can use and manipulate that temporarily stored data later in your code if you have a use for it.

Variables have a name and a data type. It is usually declared using let or const. Let is used for variables with values that may change over time. Const is used for variables with values that should not change over time.
