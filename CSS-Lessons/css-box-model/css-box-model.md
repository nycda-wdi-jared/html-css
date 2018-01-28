autoscale: true
footer: © New York Code + Design Academy 2015
slidenumbers: true

#  CSS Box Model

---

# Learning Objectives
- Define the **box model** & understand how it works
- Play with **border, padding** and **margin**

---

# The Box Model


> All HTML elements can be thought of as boxes.

^ What does this mean? Open up the inspector. Hover through the DOM. Everything highlights as a box.


---


# The Box Model

The **"Box Model"** describes how spacing around these boxes works!

![the box inline](https://www.washington.edu/accesscomputing/webd2/student/unit3/images/boxmodel.gif)


---


# The Box Model

- **content** - "text" inside of an HTML element

- **padding** - space between the content and a border

- **border** - a line around an element - comes after padding

- **margin** - space before next element - comes after border



> Every element (or box) has these box-model properties.


---


# Margin and Padding

Now we know what these two are, let's talk about the difference between the two.

**Padding** is inside the element. Therefore it affects the content inside of it.

**Margin** is outside the element. Therefore it affects how near or far the element is to other elements.


---


# How do we do it?

Put a 20 pixel margin around the element:

```
margin: 20px;
```

Put 50 pixels of padding inside the element:

```
padding: 50px;
```


---


# Specific Sides

You can add padding or margin to a specific side of your element.

```
padding-right: 10px;
padding-bottom: 20px;
```

```
margin-left: 40px;
margin-top: 10px;
```


---


# Centering content

```
width: 500px;
margin: 0 auto;
```

- Use `auto` for `margin-left` and `margin-right` to center an element!
- This will only work for elements with a `width` property.
- You can only give elements with a display value of `block` (like a div) a width.


---


# Demo

^ Use a `#wrapper` and center content on the page


---


# Border Styles

Putting borders around elements is a handy way to see how much space they take up on the page.

Borders have three main properties: **width, style,** and **color.**

```
div.container {
  border: 2px dashed red;
}
```

In the above code, we target the div with a class of "container" and give it a border that is 2px wide, is dashed (as opposed to solid or dotted), and is red.

The long form is also acceptable:

```
div.container {
  border-width: 2px;
  border-style: dashed;
  border-color: red;
}
```


---


### Exercise #1: Using the box model

- Create a `<p>` element with some text in it.

- Give the element a border that is 2px wide, dashed and red.

- Give the element a padding of 10px and see what happens to the text.

- Now give the element a margin of 20px and see how it changes the position of the element.

