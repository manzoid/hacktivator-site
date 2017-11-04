---
layout: page
title: "Abstraction"
---

Earlier we talked about how you will need to move fluidly between different levels of detail.

One very practical way for a programmer to think about managing "different levels of detail" is defining and using abstractions.

## Abstraction: For not much detail

Sometimes it's key to think about an entire system or how a user will interact with it, and not get mired in details. When that's the case, define and use abstractions to hide unnecessary details so we can manipulate "larger" and more-meaningful items in your mind, and thereby get more done. Take this example of outlining general user experience with a news app.

Instead of this list of items:
* user goes to URL bar
* user types in URL
* user hits enter or clicks Go
* Internet does its thang
* user hits home page
* user looks at headline
* user reads and processes headline
* user skims rest of articles
* user decides what to select
* user hovers over desired article
* user clicks

...which is not inaccurate, but removes the focus from the experience and so is unhelpful...

How about this level of abstraction:
* user hits home page
* user skims content
* user clicks on article to read


With the right abstractions we can avoid getting ineffectively bogged down, and in effect let ourselves work smarter.

Much of our work as software engineers is

* selecting
* defining
* thinking with
* designing solutions around

the right abstractions.

## Chunking: Such detail. Very memory.

On the other hand, sometimes you will need to work with lots of details and large amounts of information. And in those cases, you may need not only to think about granular detail, but also to remember and act upon it effectively.

You’ve heard the thing about human short-term memory only being able to handle a few items at a time, right?

That means we only have a handful of items available in the forefront our minds at any given moment to understand, analyze, and decide things. We can rapidly switch which items are in that “staging area”, but we can't substantially change the number we can have there at once.

Organizing lots of information into smaller, digestable nuggets, and then associating those nuggets with each other based on some similarity, helps us remember them all as related things. When something triggers us to remember one nugget, we tend to remember them all. Thus, we create "chunks" of related information.

As you might guess, this action of cognitively organizing information into small bits and associated categories is called “chunking”. And in a field of practice -- say, software engineering -- experienced professionals tend to be able to create and process larger chunks than beginners can.

Practice putting what you learn into related functional categories (not linguistic categories such as 'they all start with the letter Q'), like so:

**Node.js**
* v8 engine
* Common JS modules
  * `module.exports`
  * `require`
* built-in networking libraries
  * `http`
  * `server.listen(port, callback)`
* global object is not `Window` as in browsers



---
[next](../problem-decomposition)
