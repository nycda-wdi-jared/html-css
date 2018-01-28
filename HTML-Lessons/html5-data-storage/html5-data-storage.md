autoscale: true
footer: © New York Code + Design Academy 2016
slidenumbers: true

# [fit]HTML5:<br>Data Storage

---

# Looking to store some meta-data?

- Sometimes when you're creating a website or application, it's overkill to use Cookies or local storage

- Storing meta-data on an element itself can be extremely useful and take you beyond just using classes to group elements together

---

# Enter: the `data-` attribute

- A `data-` attribute is a new HTML5 attribute that lets you store arbitrary data on an element

````html
<div class="snake" data-snake-type="python">
  <img src="python.jpg">
</div>
````

---

# Using `data-` attributes with JavaScript
### Setting

You can easily set a `data-` attribute using the `.data()` jQuery method:

````js
$(".snake").data("snake-type", "anaconda")
```
---

# Using `data-` attributes with JavaScript
### Getting

You can easily retrieve a `data-` attribute using the `.data()` jQuery method:

````js
console.log($(".snake").data("snake-type"));
```

---

# Use cases

This is all great, but where can I use this?

"Custom data attributes are intended to store custom data private to the page or application, for which there are no more appropriate attributes or elements."
-W3C Specification

---

# Multi-step JS processing tasks

- Perhaps your elements involve some calculations

- You can start with one data value, change it or set another, then display that data to the end user

---

# More aware elements

- You can treat elements more like objects

- If you give them enough attributes, you can write scripts that allow your objects (elements) to interact with each other rather than using JavaScript objects as a data store for HTML elements

---

# Sorting by data attribute


````html
<div class="tracks">
  <audio controls="controls">
    <source src="Vertigo.mp3" type="audio/mpeg"
    data-artist="U2" data-title="Vertigo" data-duration="800" data-tempo="125" />
  </audio>
  <audio controls="controls">
    <source src="0to100.mp3" type="audio/mpeg"
    data-artist="Drake" data-title="0 to 100" data-duration="1000" data-tempo="100" />
  </audio>
</div>
````

````js
var first = $("audio source").first();
var last = $("audio source").last();
if(first.data("duration") < last.data("duration")){
  first.parent().html(last.html());
  last.parent().html(first.html());
}
````

---

# Store game data on an HTML element

````html
<div class="player" data-id="13434342" data-health="47">
````

````js
setInterval(function(){
  if($(".player").data("health")){
    $(".player").remove();
  }
}, 100)
````
---

# Storing advanced Google Analytics tracking information

````html
<a href="/buy-expensive-stuff" data-ga="expensive-thing-1">
  Buy Me
</a>
````

---

# Exercise

Read and write to an HTML5 data attribute on an element of your choice.

Try implementing one of the use cases above if you have time.
