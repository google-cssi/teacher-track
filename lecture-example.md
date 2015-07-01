---
tags: cssi, javascript, jquery
level: 2
languages: javascript
---

# Lecture Example - jQuery

## Objectives

+ Understand what constitutes an *event*
+ Attach jQuery event handlers (like 'click') to HTML elements
+ Add callback functions to event handlers
+ Use the `$(this)` selector in event handlers
+ Add animations to HTML elements using jQuery
+ Understand how to chain jQuery methods
+ Implement the jQuery UI library and other jQuery plugins
+ Parse through the jQuery documentation as a resource

## Motivation / Why Should You Care?

What happens when you click a button on site? Can we make code that responds to user actions?  What if we want something to turn blue when your mouse moves over it?

jQuery has *event handlers* that respond to user actions. This allows us to make all sorts of amazing behaviors and websites that respond naturally to user actions.

## Lesson Plan

### What are Events

jQuery [Events](https://api.jquery.com/category/events/) are user actions such as mouse clicks, anytime a key is pressed, or if the window is resized. In response to these events we can define some code that will be run everytime that happens. We can be notified of events that happen anywhere on the webpage or only on a specific HTML element.

### jQuery Click Handler

One very popular event handler is the `click()` handler. The code defined in this handler will be run anytime the HTML element that we are *listening* to is *clicked*.

Suppose we have HTML that looks like this

```html
<html>
  <head>...</head>
  <body>
    <button class="the-button">Push the Button</button>
  </body>
</html>
```

We could *attach* a click handler to the element with jQuery so that code is run anytime the button is *clicked*.

```js
$(".the-button").click(function()
{
  alert("House Music!! Boots, and Cats, and Boots, and Cats");
});
```

Because we have created a jQuery event handler and attached it to the HTML element with the class `the-button`, when we click on the button, an alert will pop up that says "House Music!! Boots, and Cats, and Boots, and Cats".

### What is a Callback function

A callback function is the function (aka: the code) that is run when an event handler is triggered. In the previous example `.click()` takes an entire function as its input. If you count the parenthesis you'll see that this function on it's own looks like this:

```js
function()
{
  alert("House Music!! Boots, and Cats, and Boots, and Cats");
}
```

Let's say we wanted to just have our `.click()` alert "Hello World". The function to do that looks like this:

```js
function(){alert("Hello World");}
```

So the click handler just takes that exact function in between its `()`, like so:

```js
$(".the-button").click(function(){alert("Hello World");});
```

Be Careful!! The `()`, `{}`, and `;` can look confusing, but if you count where they open and close we are just starting with `()` and dropping in a function.

This is called an *anonymous* function, and is our callback function. It has no name and will only be run when the event handler is triggered. JS/jQuery allows you to also pass in a named function.  Our code in this case could look like this:

```js
// Define the function
function houseMusic()
{
  alert("House Music!! Boots, and Cats, and Boots, and Cats");
}

// Pass the function to the event handler
$(".the-button").click(houseMusic);
```

A trick to notice here is that when we pass in the function `houseMusic` we DO NOT include the parenthesis `()`, because we are not calling the function at this point. We are only telling the event handler where to find it.

### Other Event handlers

jQuery can respond to a wide variety of Events which you should read about in the documentation. Some popular ones are:

+ Mouse clicks
+ Page load finishing
+ Moving the mouse over an element (often used for menu highlights)
+ Submitting an HTML form
+ Pressing the keyboard buttons
+ And [MORE](https://api.jquery.com/category/events/)!!

### Document Ready as an Event

If you remember our `$(document).ready()` function, you can now see that it is just an event handler responding to the jQuery object of `$(document)` firing off the Event that it's `ready()`.

```js
$( document ).ready(function() {
  // Here are all the functions that
  // will be run when the document is ready.
});
```

### `$(this)` inside Event callbacks

If you want to do something to the element that fired an event (fade out the button you just clicked) `$(this)` allows you to easily access that element.

For Example:

```js
$(".the-button").click(function()
{
  alert("House Music!! Boots, and Cats, and Boots, and Cats");

  // I don't think they can handle more House Music
  // Let's fade out the element they clicked on.

  $(this).fadeOut();
});
```

Here the `$(this)` refers to the button that we selected with the jQuery selector `$(".the-button"), since we are inside of its event handler.

### Animations

jQuery also has support for basic animations. They work by selecting the element and calling the function on it with a `.` between the functions.

```js
// Show the HTML element with id="panel"
$("#panel").show();

// Hide that same element
$("#panel").hide();
```

 Here are some favorites:

+ `.show()` - Shows the selected element
+ `.hide()` - Hide an element
+ `.fadeIn()` - Show an element with a slow fade
+ `.fadeOut()` - Fade out the element

Check the [documentation](https://api.jquery.com/category/effects/) for more examples and explanations.

### Chaining Methods

Up until this point we've been writing jQuery statements one at a time. However, when you want to do multiple things to an element you can *chain* multiple commands together so you don't need to look up an element over and over again.

For Example, if we wanted an element to turn blue, and then move down and up we could write it this way:

```js
$("#stuff").css("color", "blue");
$("#stuff").slideDown(2000);
$("#stuff").slideUp(2000);
```

This works, but we're repeating the lookup for the HTML element with the ID of `stuff` multiple times. This is not only harder to write but is also computationally expensive (it takes jQuery time to look it up each time).

Instead we can do this:

```js
$("#stuff").css("color", "blue").slideDown(2000).slideUp(2000);
```

Here, we've *chained* the methods by simply adding the next one to the end of the chain.

### jQuery UI

[jQuery UI](https://jqueryui.com/) is another JavaScript library that is built on regular jQuery. It has support for more advanced animations and UI elements (things that look great and do cool stuff). To get a feel for what it can do check out some [demos](http://jqueryui.com/demos/).

### Using Documentation

As with all coding the internet is your friend!!! Whenever you are stuck, try a search for your issue, or start reading the documentation.  It's amazing what's out there. Don't let it scare you!

## Conclusion / So What?

jQuery and other libraries allow you to do amazingly complex stuff with a simple function call. Any developer worth their salt will want to make a website that responds to the user. jQuery events let you do that.

## Hints and Hurdles
+ `$(this)` can be confusing, remember it refers to the element that the event handler was called on
+ `$(document).ready()` is just one big event that all your code should go inside
+ Event handlers take functions, anonymous or named, to call when that event happens
