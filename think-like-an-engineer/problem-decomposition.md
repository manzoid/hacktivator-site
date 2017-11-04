---
layout: page
title: "Problem decomposition"
---

"Problem decomposition" is a slightly gross-sounding way of describing the task of breaking a bigger problem down into smaller problems.

The complexity of building software -- even small programs, let alone full-blown systems -- rapidly becomes overwhelming unless you break the bigger problems down into manageable sub-problems.

If you find yourself confused about what you are building -- what to do next, or what you have done -- then you probably haven't done enough problem decomposition.

Make the problems small enough to fit into what you can reasonably think about. Then you can craft small, well-defined technical pieces to match those small, well-defined problems. The resulting system will both work in the immediate term _and_ be maintainable in the medium term.

## Example of problem decomposition

Say you are tasked with a non-programming problem: "Build a birdhouse." Arriving at a finished birdhouse is the result of many subtasks. What steps would you need to take?

```bash
// Create a pattern
// Select the material
// Secure the right tools
// Measure the material
// Cut the material to size
// Join the material
```

These are excellent steps. Technically, if we were bringing this birdhouse to market, we'd definitely want to consider what types of birds would need to use our birdhouse and what specifications they require for a house. But no matter just here.

If we look at our steps, we quickly realize that handing them over to a novice wouldn't result in a functional birdhouse. How do you create a pattern? What steps must you take to select the material? What tools do you need? If a contextless novice wouldn't know how to execute each step, you need to continue decomposing.

```bash
// Measure the material
```

... becomes...

```bash
// Measure the material
  // lay measuring tool against material
  // locate the desired ending length
  // mark endpoint
```

Of course, we could decompose this even further to include the picking up of and setting down of the measuring tool, and other details that are important to execution. The point is that in order to decompose a problem, you should

1. Consider the end goal
2. List out (or at least think about) the components necessary to reach your end goal
3. Consider each component its own end goal
4. Repeat steps 2 and 3

...until you have a functioning system. By the way, we'll get more practice in *writing out* substeps (stubbing) in the next few modules.


## System components should be small

Components are ideally:

 * Completely reliable
 * Easy to understand
 * Easy to re-use
 * Easy to connect with other components

Well-written components at any scale satisfy the above criteria.

Even the smallest, single-function program has this idea ingrained within it. The function itself is a component. The caller of the function can be thought of as another component. The function provides an interface to the caller.

Decompose your problem into sub-problems, and decompose your system into small problems to match.

---
[next](../09-clean-coding)
