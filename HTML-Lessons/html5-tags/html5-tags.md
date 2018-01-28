autoscale: true
footer: © New York Code + Design Academy 2016
slidenumbers: true

# [fit]`HTML5` Tags

---

# Learning Objective

- Know the difference between plain HTML and HTML5

- Write some new types of tags, understand where they're used

---

# What is HTML5?

- HTML5 is just the latest and greatest "spec" from the W3C, or World Wide Web Consortium

- Before it came all other versions of HTML

- HTML5 contains a few additional tags to be even more semantically specific with your markup

- Let's learn a few of them to be up to date!

---

#`<nav>`

Only your site's navigation menus should be wrapped in this element, not other `<ul>`s

````html
<nav>
  <ul>
    <li>
      <a href="index.html">Home</a>
    </li>
  </ul>
</nav>
````

`<nav>`s cannot be nested inside each other according to the spec, but you could have a multi-level menu using `<ul>`s

---

#`<article>`

-`<article>` is used to indicate a self contained piece of content that could be distributed independent of the website itself

-It can wrap the `<header>` tag, `<footer>` tag, and article content (typically in `<p>` tags)

---

#`<header>`

The `<header>` tag is NOT equivalent to the `<head>` tag

Instead, it's meant to denote the top part of your `<article>`, which includes any `<h1>` tag and surrounding content, like a subtitle:

````html
<header>
  <h1>Welcome to my awesome page!</h1>
  <p>This is a place for friends.</p>
</header>
````
---

#`<footer>`

- The <footer> tag is used to declare the bottom of an <article>

- It usually contains copyright information or information about the author

````html
<footer>
  <p>Article by: Zach Feldman</p>
  &copy; 2014 NYCDA
</footer>
````
---

#`<video>`

- Allows you to play a video on the page, before HTML5 you had to use `<embed>` tags, which are now deprecated

````html
<video width="480" height="320" controls>
  <source src="video.ogg" type="video/ogg">
  <source src="video.mp4" type="video/mp4">
  Here's some text if your browser doesn't support HTML5 video.
</video>
````
---

#`<audio>`

- Allows you to play audio on the page, before HTML5 you had to use `<embed>` tags, which are now deprecated

````html
<audio controls>
  <source src="audio.mp4" type="audio/mpeg">
  <source src="audio.ogg" type="audio/ogg">
  Here's some text if your browser doesn't support HTML5 audio.
</audio>
````

---

# Exercise

Try out some of these cool new tags by creating an `<article>` with a `<nav>` bar marked up semantically correctly that includes a `<video>` and `<audio`> file.

---

# Quiz

1. What's the difference between HTML5 and HTML?