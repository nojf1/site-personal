---
title: "JavaScript Parameters and Arguments"
date: 2025-07-29
draft: false
description: "JS"
tags: ["JavaScript", "Let's Learn"]
summary: "A review of my understanding of JavaScript, part 3"
series: ["Learning JavaScript!"]
series_order: 3
---

## A quick disclaimer!

Whatever information here may be factually incorrect because I write them from my own honest understanding. If you are not familiar with the topic, I encourage you to do your own research and form your own conclusions. If you are an expert on the topic though, please contact me if there are any errors or incorrect information here so I can correct them.

Everything written here is extremely simplified, as the purpose of this series is to review my own understanding of the topic.

I may write more detailed explanations on the subject in the future, which I will link to when appropriate.

## More About JavaScript Functions - Parameters and Arguments

From the last article, we learned that functions are simply a set of written instructions that will execute when a function is called. Parameters are placeholer variables we list in a function definition, its somewhat like a function's own variable that will be used only within the function. Arguments are the actual values you pass in when you call the function.

There is a fundamental difference between arguments and parameters. Put simply, parameters are the variable names while arguments are the actual values of those variables.

Let's see an example.

```
function greet(name) { // 'name' is a parameter
  console.log("Hello, " + name + "!");
}

greet("Alice"); // "Alice" is an argument
// Output will be: Hello, Alice!
```

Within the function _greet_, 'name' is wrapped in parentheses to show that it is a parameter. When the function greet is called, the string "Alice" is passed in as an argument.

You can add multiple parameters and arguments in a function as well, let's look at another example:

```
function add(a, b) {
  return a + b;
}

console.log(add(3, 4)); // a=3, b=4
// Output will be: 7
```

Here, the parameters 'a' and 'b' are defined within the parentheses of the function _add_. When the _add_ function is called, the integer values '3' and '4' are passed in as arguments. But which one corresponds to the parameters?

It follows the order in which the arguments are passed. 'a' will have the value of '3', and 'b' will have the value of '4'. Whichever is passed in as arguments follows the order of parameters defined in the function.

But what if we have a function to let's say, take a forum user's name to display on the front page, but once they are logged out, there will be no name to display. In this case, we can use a default value to pass in place of the actual argument.

```
function greet(name = "Guest") {
  console.log("Welcome, " + name + "!");
}

greet("John"); // Output will be: Welcome, John!
greet();       // Output will be: Welcome, Guest!

```

In the function _greet_, we defined the default value of the parameter name with the string "Guest". Notice there is an equal sign in there? This is how we define a default value in the case there is no argument provided.

But remember, the default value will only be used if there is no argument passed into the function, it is like a backup option when there is nothing else to work with. In the example, the expected output of the first _greet_ function called is different, because the function accepts and uses the provided argument. In the second call of the function, nothing is passed in as an argument, so the function resorts to the default value defined in the function earlier.

## The Rest Parameter

The next thing I want to discuss is the rest parameter (...). The rest parameter is just three periods. Using it is very simple, let's see it in a code example:

```
function sumAll(...numbers) {
  let total = 0;
  for (let num of numbers) {
    total += num;
  }
  return total;
}

console.log(sumAll(1, 2, 3, 4)); // Output will be: 10
```

In this example, we have the function _sumAll_ that takes numbers as a parameter, but this time we put a rest operator in front of it. What this means is that the function can accept an unlimited amount of arguments (not really unlimited, but lets just say it can accept a LOT). It is useful for when you don't know how many arguments you're going to accept within the function.

In the example, the code logic works by accepting any amount of numbers as arguments, then loops over the number of arguments given and adds them up to give our total result. When the function is called, there are 4 arguments passed in. The _sumAll_ function will then take this, count the total arguments passed in into the 'total' variable defined within the function scope, then uses a for loop to iterate over the arguments passed into 'numbers' (with the rest operator), defines a 'num' variable within the loop to store and calculate the result, then finally adds up the total numbers in the resulting operation and returns it with the 'total' variable.

The rest parameter is used very often in frameworks like React. But providing unlimited arguments isn't its only function.

The rest parameter can also be use for array destructuring, which basically collects the remaining elements in an array after extracting specified ones you want. Here's a simple example:

```
const [first, second, ...rest] = [1, 2, 3, 4, 5];
// Result will be: first = 1, second = 2, rest = [3, 4, 5]
```

The resulting array is a shorter, extracted form. The other elements are carried over and stored into their own variables.

However, its important to remember that while the rest operator looks the same in different use cases, you need to be able to know its uses and differentiate them to know exactly what they are meant to do in their respective contexts.

Another functions of the rest parameter is forwarding arguments. You can pass along arguments to other functions using the rest parameter like this:

```
function forwardingArguments(otherFunction, ...argument) {
  return otherFunction(...argument);
}
```

It looks a bit confusing, but it is very simple. The _otherFunction_ is not defined in the example code, but let's pretend it already was to make it easier to explain. When you pass in the _otherFunction_ name without parentheses to call it as a parameter in the _forwardingArguments_ function, the _otherFunction_ itself is not called, you would still have to call it after you defined it as a parameter in the forwarding function. In the forwarding function's case, it returns the _otherFunction_ while passing in the previously defined ...argument in the forwarding function as an argument passed into the _otherFunction_ instead.

Don't overthink this, the concept itself is very simple. You simply define another function in order to pass arguments to other functions. This method of writing can contribute to cleaner code and logic in the long run.

Remember, don't overthink things in programming. If it doesn't make sense, give your brain some time to settle and simmer with the boiled information so you can digest it properly. I went through the same thing when I first started out. It will eventually click after some time. Perhaps this is also a reminder to myself, mostly.

## Summary

-Parameters are placeholder variables in a function, and used within the function only. Multiple parameters can be defined at the same time.

-Arguments are the actual values passed into a function when you call it. Multiple arguments can be passed at the same time, as long as there is an equivalent number of parameters already defined within a function without using a rest operator.

-The rest operator (...) can be used to accept unlimited argument amounts, destructure arrays, and forward arguments into another function.

-Try not to overthink programming too much, it is what it is. Give yourself some time to think as well.
