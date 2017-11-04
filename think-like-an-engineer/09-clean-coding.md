---
layout: page
title: "Clean vs unclean coding"
---

Your code should tell a story.

Clean code gives the code reader a clear narrative about its purpose and how the processing unfolds.

We call this being "self-describing" and "readable".

To illustrate this, let's look at a bad example and turn it into a good example.

## Example of unclean vs clean coding

Let's take a look at a typical beginning programmer's approach to a specific problem.

Then we will consider what's wrong with it, and how it could be improved.


## The problem statement

```
const inventory = [
  {
    name: 'Brunello Cucinelli',
    shoes: [
      {name: 'tasselled black low-top lace-up', price: 1000},
      {name: 'tasselled green low-top lace-up', price: 1100},
      {name: 'plain beige suede moccasin', price: 950},
      {name: 'plain olive suede moccasin', price: 1050}
    ]
  },
  {
    name: 'Gucci',
    shoes: [
      {name: 'red leather laced sneakers', price: 800},
      {name: 'black leather laced sneakers', price: 900}
    ]
  }
];
```

Now output the average cost of all shoes per designer in this format:

```
const expected = {
  'designers': [
    {
      'name': 'Brunello Cucinelli',
      'averagePrice': 1025
    },
    {
      'name': 'Gucci',
      'averagePrice': 850
    }
  ]
};
```

## A beginning programmer's solution

Given the above problem statement, this is a real example of code produced by a beginning programmer:

<img src="http://i.imgur.com/8aAyQvC.png" width="500" />

## What's wrong with this solution?

### Readability
The above solution is a bit hard to read.

There is too much going on in the function body. It would be a lot easier to understand if we factored out a couple of helper functions that each did only one small thing. The names of those functions would give us big hints about what the code is doing.

### Testability

The above solution is harder to test than it should be.

When a longer chain of processing happens inline within one function body, testing the processing is an all-or-nothing proposition. Whereas each time you factor out a subset of that processing into a helper function, you make it much easier to test that part of the code.

Upon seeing the above code, a seasoned programmer would consider some refactoring like this:

<img src="http://i.imgur.com/mJjyWZA.png" width="500"/>

## A complete, cleaner solution

Let's take the basic idea in the sketch above and flesh it out into a complete solution. We won't retain the exact names, but we'll retain the basic idea.

<img src="http://i.imgur.com/Ggvuobl.png" width="500"/>

## Why is this better?

Your code should tell a **story**.

A story has a **beginning**, a **middle**, and an **end**.

A story **flows** smoothly.

In a good story, it is easy to keep track of what's going on at any given moment (the **current state**).

Here's a visualization that illustrates the "story" flow being told by the code above:

<img src="http://i.imgur.com/ltsxD2G.png" width="500" />

## Ok, but how do I get the code to tell a story, exactly?

* Assemble your solution from small, single-purpose functions that have no side effects.
* Aim for a simple, clear flow of data from small function to small function.
* Think in terms of inputs and outputs at every level of your system. Each small function transforms its input into an output.
* Use precise, self-describing names for your functions and variables.
* Functions in particular should be named "verbObject", like `renderList` or `calculateAverage`. This emphasizes the transformation of input into output.


---
[next](../10-functions-and-reliability)
