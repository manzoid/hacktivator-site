---
layout: page
title: "Caring about the big picture"
---

While careful engineering involves organizing lots of small details, those details only make sense within a bigger picture.

## A hierarchy and ecosystem of parts

* The details of a line of code make sense only in the context of the flow and state of the function enclosing that code.
* A function makes sense only in the context of the larger component (a module, class, or entire script) enclosing that function.
* A component makes sense only in the context of other components interacting with that component, and in the context of the entire subsystem of which that component is just one part.
* A subsystem makes sense only in terms of other subsystems, and in the context of the entire app of which that subsystem is just a part.
* An individual feature generally makes sense only in the context of interacting with what other features do.

## A fluid, changing system

In general, your code only makes sense in the context of a live, running system executing at a given point in time, with a given state at that point.

## Evolving human purpose

And your running system only makes sense in the context of the human requirements, human usage, and human-populated software organization that led us to bother building the thing in the first place.

_Engineers care about the big picture just as much as the implementation details._

---
[next](../03-levels-of-detail)
