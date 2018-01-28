autoscale: true
footer: © New York Code + Design Academy 2016
slidenumbers: true

# [fit] CSS Basics: <br>Styling your Web

---

# Learning Objectives

- Understand where CSS is used and how to include it

- Write your first CSS declarations

- Have them reflected on the page


---

# CSS Defined

- CSS stands for Cascading Style Sheets

- It is the primary way of styling static HTML pages

- The current standard is CSS3, but some more antiquated browsers do not support all of its features


---

# Why learn CSS?

- Controls the layout and style of any webpage you create

- Without it, your websites will look quite plain

  - Why? The web and HTML were originally created for professors to share research papers, not by designers

- Eventually, you'll be able to make your websites look good on any device (desktop, tablet, mobile) using it

---

# How do I add CSS to my web page?

- CSS styling can be added to an HTML page in several different ways

  - Inline, inside of HTML elements

  - Included inside of an HTML file as a list of declarations linked to HTML elements

  - Written in a separate `.css` file as a list of declarations linked to HTML elements and linked to externally from inside of an HTML file

---

# Inline, inside of HTML elements

````html
<!DOCTYPE html>
<html>
  <body>
    <span style="color: red">Some text</span>
  </body>
</html>
````

---

# Included in HTML file

### Typically in `<head>` section

````html
<!DOCTYPE html>
<html>
  <head>
    <style type="text/css">
      span {color: red;}
    </style>
  </head>
  <body>
    <span>Some text</span>
  </body>
</html>
````

---

## Linked to in an external stylesheet

### from HTML

````html
<!-- index.html, abridged -->
<head>
  <link rel="stylesheet" type="text/css" href="style.css">
</head>
<body>
  <span>Some text</span>
</body>
````


````css
/* style.css */
span {
  color: red;
}
````

---

# Classes and IDs

- A **class** is an HTML attribute whose value is used to classify one or more elements on a page

- An **ID** is an HTML attribute whose value is used to only classify one element on a page

````html
<div id="events">
  <div class='event'>
    <h3>Awesome Party</h3>
  </div>
  <div class='event'>
    <h3>Only Alright Party</h3>
  </div>
</div>
````

---

# Selectors

- Used in order for the browser to know which element you are trying to style

- The basic selectors are

  - HTML element names

  - Class names, always prefixed with a dot (.)

  - ID names, always prefixed with a pound sign (#)

---

# attribute: value;

### background-color: orange;

- A CSS attribute

  - is a pre-defined style that the browser applies to an HTML element

  - always followed by a colon

- A CSS value
  - always follows an attribute
  - tells the browser which attribute option to apply to the selected element
  - is always followed by a semicolon

---

## CSS Example 1: Element Selection

Select all `div`s on the page, make their text orange, give them a black background, and center all of their text within the `div`s themselves[^1]

````css
div {
  color: orange;
  background-color: black;
  text-align: center;
}
````

[^1]: Keep in mind that this CSS must be included in an HTML page using one of the three methods mentioned in prior slides, the next few pages will assume this

---

## CSS Example 2: Class Selection

Select all elements with the class `events` on the page, make their text white, give them a red background, and left align all of their text within the elements themselves

````css
.events {
  color: white;
  background-color: red;
  text-align: left;
}
````
---

## CSS Example 3: ID Selection

Select all elements with the ID `event` on the page, make their text white, give them a red background, and left align all of their text within the elements themselves

````css
#event {
  color: white;
  background-color: red;
  text-align: left;
  padding: 10px;
  margin-bottom: 6px
}
````

#### More on padding and margin later.

---

# CSS Comments

- Comments can be a useful way to

  - denote what you're actually styling if it's unclear

  - leave notes for other developers

  - temporarily disable code to see how the page looks without a style

````css
/* An individual event listing */
.events li {
  /* Let's leave this section for now until v1.2 */
  background-color: blue;
  /* color: orange; */
}
````

- Your goal is to write easily understandable code or comment enough to make your code clear to anyone reading it.

---

## CSS Example 4: An actual stylesheet

````css
/* Extracted from the NYCDA 'class' page template */
.right {
  width: 440px;
  font-size: 20px;
}

.right i {
  display: block;
}

.skills {
  margin-top: 10px;
}

i {
  font-style: italic;
  margin-bottom: 6px;
  margin-top: 16px;
  font-size: 18px;
  line-height: 30px;
}

ul {
  margin-left: 21px;
  font-size: 18px;
  line-height: 30px;
}

ul li {
  list-style: disc;
}

````

---

# Exercise 1: Your First CSS

- Create a blank webpage with an `<h1>` and `<p>` element and sample text inside of both

- Style these elements' background and text colors using CSS included from an external stylesheet (.css file)

- If you have time, clone your basic webpage and try implementing your CSS using the other 2 methods outlined earlier

  - Inline, inside of the elements themselves

  - At the top of the file in the `head` section

---

# [fit] Basic CSS Attributes

---

````css
color: red;
````

The `color` attribute dictates text of the element color

````css
font-family: "Times New Roman", serif;
````

`font-family` denotes the element's display font

````css
font-size: 20px;
````

`font-size` determines the selected element's font size

---

````css
background-color: #fff;
````

Sets the background color of the element, #fff is a hex code meaning "white" (more on this later). This is the default background-color value

````css
background-image: url('tiger.png');
````

Sets a background image for the element with the url 'tiger.png'

````css
background-repeat: no-repeat;
````

Tells the browser not to repeat the background image horizontally or vertically. Other possible values: repeat (default), repeat-x, repeat-y, inherit

---

````css
width: 100%;
````

Sets the width of this element to take up 100% of the parent element it resides in

````css
height: 20px;
````

sets the height of the element to 20 pixels

---

## Units for width, height, and font size

- `%`, a percentage of the parent element the selected element is occupying

````
width: 43%;
````

- `px`, an exact pixel value for the element to take up

````css
height: 420px;
````

- `em`, proportionate to the parent value with 1em being the exact parent value and 2em twice that

````css
max-height: 3em
```

---

# Specifying colors

- `background-color` and `color` can take several forms of color input

  - "valid" colors like `red`, `orange`, and `blue`[^3]

  - hex values which correspond to a color, like `#fff` (white), `#000` (black), or `#0E0EFF` (a specific shade of blue)

  - RGB, or red, green, blue values like `rgb(10, 160, 30)` or `rgba` values, which include an alpha (opacity) value `rgba(100, 43, 210, .4)`


[^3]: For a full list of valid colors, see [this website](http://w3schools.com/cssref/css_colornames.asp)

---

# [fit] More attributes

---

````css
text-align: center;
````

How the text should be aligned within the element itself


````css
text-transform: uppercase;
````

Makes all text uppercase regardless of how it was entered into the element. Also try `lowercase` and `capitalize`

````css
line-height: 20px;
````

Gives the selected element a line-height of 20px, a measure of separation between lines of text

---

# Styles for <li> tags within lists

````css
list-style-type: square;
````

Makes the bullet point style into a square bullet point, one of many possible options

````css
list-style-image: url('my-bullet.png');
````

Sets a custom image for the bullet point

````css
list-style: none;
````

Removes bullet points from the list style


---
# Alternate selection methods

Sometimes, just using an element name, class name, or ID isn't specific enough or the most efficient way to select an element.

---

## Combining element and class selectors

You can combine an element and class selector to be more specific. The same can be done with IDs.

````html
<ul class="presidents">
  <li>
    George Washington
    <ul>
      <li>Brave</li>
      <li>Tall</li>
    </ul>
  </li>
</ul>
````


````css
/* Only George Washington will have a square list-style-type, not brave and tall */
ul.presidents{
  list-style-type: square;
}
````

---

# Selecting multiple items

To select multiple items, separate their selectors with commas.

````html
<ul class="presidents">
  <li>
    George Washington
  </li>
</ul>
<span>Cut down the cherry tree</span>
````


````css
ul.presidents, span{
  font-family: "Arial", sans-serif;
}
````

---

# Selecting descendants

````html
<ul class="presidents">
  <li>
    George Washington
    <ul>
      <li>Brave</li>
      <li>Tall</li>
    </ul>
  </li>
</ul>
````


````css
/* All <li>s will have a square list-style-type */
ul.presidents li{
  list-style-type: square;
}
````

---

# Selecting direct descendants

````html
<ul class="presidents">
  <li>
    George Washington
    <ul>
      <li>Brave</li>
      <li>Tall</li>
    </ul>
  </li>
</ul>
````


````css
/* Only George Washington will have a square list-style-type */
ul.presidents > li{
  list-style-type: square;
}
````

---

# Final Basic CSS Exercise

### Style "The Onion Article"

Download the `onion.html` file and apply the following styles to it:

1. Make the main headline dark green

2. Use the font family "Georgia" for the main headline and the sub-headline

3. Center the text of the main headline and the sub-headline

4. Make the paragraphs have a line height of 19 pixels

6. Make the "You might also like" label all uppercase

6. **Bonus:** Remove the underline from the links

7. **Bonus:** Make an underline appear when you hover over a link

---

# Resources

**Codecademy**
[HTML & CSS - Introduction to CSS](https://www.codecademy.com/learn/web)

**TeamTreeHouse**
[CSS Basics](https://teamtreehouse.com/library/css-basics)

**CSS-Tricks**
[The CSS Almanac](https://css-tricks.com/almanac/)

---

# Quiz

1. What is CSS capable of?

2. How can CSS be included in the document?

3. Write a valid CSS declaration that changes the color of the `<h1>` to red.
