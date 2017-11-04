---
layout: page
title: "Avoiding assumptions"
---

Misunderstanding is a core aspect of the human condition.

What's going on inside someone else's head? What are they really trying to tell you? What do they really want? Do they even know, themselves?

How many times in your life have you found yourself confused and surprised, after the fact, when someone tells you that that wasn't what they meant, that that wasn't what they wanted?

Despite best intentions on both sides, it's very easy to misunderstand one another.

This is also true when it comes to understanding requirements for developing your software system. When it comes to software development, it's very easy to misunderstand some aspects of what you're supposed to do.

## Assumptions are risky

If you misunderstand the problem requirements, then:

* You waste time building the wrong thing.
* You are much more likely to run out of time in your interview.
* In a real work situation, you are also much more likely to run out of time, and therefore miss deadlines.
* You seem like someone who doesn't read things carefully, who's not detail-oriented.
* You come across as someone who doesn't think ahead and think things through, who just dives in and makes a mess.
* The above points make you seem unreliable and risky.

## Some examples

### drawLine

Let's say you have this problem statement:

```
Write a function called "drawLine" that takes an integer parameter and draws a line of that length, composed of asterisks.
```

When you read that, do you visualize a horizontal line?

Who said it wasn't vertical?

Diagonal?

Also, the name of the function doesn't actually specify asterisks. It's `drawLine`, not `drawLineOfAsterisks`. Maybe we want to be able to draw with hyphens too, in the near future. Should we consider parameterizing the choice of character used to draw the line?

What does it mean to "draw" the line? Is this function supposed to draw the line directly to the console, or return a value that represents the string? If the latter, are we supposed to return a string? Or a data structure such as an array?

### getMiddle

```
Write a function called "getMiddle" that returns the middle of the given string.
```

Let's assume that "middle" means the middle character.

So the middle of "fudge" would be "d".

Ok. In that case, what's the middle of "cloister"?

<table>
<tr>
  <td>c</td>
  <td>l</td>
  <td>o</td>
  <td>i</td>
  <td>s</td>
  <td>t</td>
  <td>e</td>
  <td>r</td>
</tr>
<tr>
  <td>1</td>
  <td>2</td>
  <td>3</td>
  <td>4</td>
  <td>5</td>
  <td>6</td>
  <td>7</td>
  <td>8</td>
</tr>
</table>

Is the middle of an 8-character string between the 4th and 5th character?

Is it a blank string?

Or is it maybe these **two** characters?

<table>
<tr>
  <td>c</td>
  <td>l</td>
  <td>o</td>
  <td style="background:yellow">i</td>
  <td style="background:yellow">s</td>
  <td>t</td>
  <td>e</td>
  <td>r</td>
</tr>
<tr>
  <td>1</td>
  <td>2</td>
  <td>3</td>
  <td style="background:yellow">4</td>
  <td style="background:yellow">5</td>
  <td>6</td>
  <td>7</td>
  <td>8</td>
</tr>
</table>

So, calling `getMiddle('cloister')` returns `"is"`?

#### But wait, there's more

Is the spec for this really: "the middle-most character(s)"?

What if _this_ is "the middle"?

<table>
<tr>
  <td>c</td>
  <td style="background:yellow">l</td>
  <td style="background:yellow">o</td>
  <td style="background:yellow">i</td>
  <td style="background:yellow">s</td>
  <td style="background:yellow">t</td>
  <td style="background:yellow">e</td>
  <td>r</td>
</tr>
<tr>
  <td>1</td>
  <td style="background:yellow">2</td>
  <td style="background:yellow">3</td>
  <td style="background:yellow">4</td>
  <td style="background:yellow">5</td>
  <td style="background:yellow">6</td>
  <td style="background:yellow">7</td>
  <td>8</td>
</tr>
</table>

## How to avoid unwarranted assumptions

Since all assumptions carry some amount of risk, it's best to root out and state those assumptions explicitly.

### Assume you are making assumptions

First, you have to assume you are assuming... which you are.

Before diving into any coding, summarize what you think you know about the problem, and try to draw a representation of how you imagine it. Then compare your summary and drawing to the *exact facts stated*. Usually, you will see something you've put in your summary or drawing that is not overtly stated by the problem. An item like this--one that doesn't correspond to a stated fact--generally represents an assumption. Find at least one assumption you are making.

State it out loud. Ask yourself at least one question about it.

### Talk out loud

Formulating a specific question forces you to sharpen up your thoughts and can often point the way toward a useful answer.

Also, if you don't say what _you're_ thinking, it's hard for anyone else to know and thereby give you a chance to course-correct.

Therefore, literally talk out loud, even if that sounds a little unnatural.

If you're working alone, just ask the question out loud, rhetorically. Then answer it yourself, one way or the other. If the situation is ambiguous, just make a call, clearly state what that decision is, and move on.

If you are working with others, either live or async, then ask them to weigh in.

---
[next](../12-stubs-and-outlines)
