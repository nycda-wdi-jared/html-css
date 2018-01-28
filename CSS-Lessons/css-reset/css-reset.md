autoscale: true
footer: © New York Code + Design Academy 2016
slidenumbers: true

# [fit] CSS Resets

---

# Learning Objective

- Figure out what CSS resets are and how they effect your web pages

---

> What happens when you load a page with no CSS?

---

# The User Agent Stylesheet

* Even when no styles are supplied, a browser will supply default styles for your page.
* For example:
	* `<h1>` is bigger than `<h2>`
	* `<li>` has bullets
	* `<a>` is underlined / has `:visted` state
* These styles are contained in the browser's **User Agent Stylesheet**

---

# Why?

* Again, consider where the web came from!
* HTML used to be used to present academic documents.
* The writer didn't care what it looked like, so long as it was readable.
* UA stylesheets allowed for readable pages with no CSS!

---

> So what?

---

# UA Styles & Cross-Browser

* **Each browser uses their own, independent **UA Stylesheet**.
* What does this mean?
	* Styles in UA Stylesheets are not consistent amongst browsers.
	* Your CSS may not apply consistently across browsers :(

---

> How do we fix this?

---

# CSS Reset

* A **CSS reset** is a stylesheet
	* Meant to "reset" styles from UA Stylesheets
* Establishes a common baseline off of which you can confidently (and consistently) style elements using CSS!

---

# How do I use a CSS Reset?

CSS Resets are available as libraries for your use.

1. Find one
2. Include it on your page before your CSS!

---

# Common CSS Resets

**"Eric Meyer" Reset**

* The first widely accepted Reset library
* Very bare bones
* [http://meyerweb.com/eric/tools/css/reset/reset.css](http://meyerweb.com/eric/tools/css/reset/reset.css)

---

# Common CSS Resets

**Normalize.css**

* A newer (also widely accepted) library
* Customizable / meant for modern browsers
* [https://necolas.github.io/normalize.css/](https://necolas.github.io/normalize.css/)

---

# Demo

<!--
Optional, but perhaps dig into the code a bit and discuss
what styles a reset might supply. Such an exercise would
reinforce the discussion with concrete examples.
-->

---

# Including a CSS Reset

Simple, just include it in your head element of your HTML page:

```html
<html>
  <head>
    <!-- Make sure to link the reset.css BEFORE your custom stylesheet! -->
    <link rel="stylesheet" href="/path/to/reset.css">
    <link rel="stylesheet" href="main.css">
  </head>
  <body>
    <h1>Hi mom!</h1>
  </body>
</html>

```

---

# Exercise

Include the Eric Meyer reset on an existing web page. (Simply Google search _"Eric Meyer reset"_ and it should be the first entry that comes up).

**Consider the following questions:**

1. Has anything changed?
2. Did you observe any cross-browser CSS issues before you included it? Have they been resolved?

---

# Quiz

1. What does a CSS reset do?

2. Where should a CSS reset be placed in the HTML document?