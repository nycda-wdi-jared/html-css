autoscale: true
footer: © New York Code + Design Academy 2016
slidenumbers: true

#[fit] More HTML<br>Page Elements

---

# Constructing a navigation menu

- Semantically, navigation menus are usually `<ul>`s with links wrapped inside an `<li>`

- HTML5 calls for the `<ul>` to also be wrapped in a `<nav>` tag

- All styles are stripped from them so they no longer resemble lists

- `display: inline;` is used to put items next to each other

---

# Navigation menu code sample

````html
<nav>
  <ul class="nav">
    <li>
      <a href="/">Home</a>
    </li>
    <li>
      <a href="/about.html">About</a>
    </li>
  </ul>
</nav>
````

````css
ul.nav{
  list-style: none;
  padding: 0; }
ul.nav li{
  display: inline; }
````

---

# Constructing a button

HTML buttons simply consist of text inside of an `a` element, with `padding`, `background-color`, `border-radius`, and other styles

````html
 <a class="my-button" href="/learn-more.html">Click Me</a>
````

````css
.my-button{
  padding: 10px 12px;
  border: 1px solid aqua;
  color: aqua;
  background-color: blue;
  text-decoration: none;
  display: inline-block;
  border-radius: 5px;
}
.my-button:hover{
  margin: 2px 0 0 2px;
}
````
---

# Forms

HTML forms are used to submit data to the back-end of your website or to external websites

````html
<form action="https://www.google.com/maps" method="GET">
  <input type="text" name="q">
  <input type="submit" value="Submit">
</form>
````

For instance, this form submits a location to Google Maps search

---

# The `form` element

- The `<form>` element has two important attributes - `action` and `method`

- The `action`'s value tells the browser where the form will be submitted, it is a URL

````html
<form action="https://www.google.com/maps"></form>
<form action="/process-form-data.php"></form>
````

- The `method`'s value will decide how to send the form data, using either GET or POST

````html
<form method="GET"></form>
<form method="POST"></form>
````

---

# `GET` vs `POST`

- `GET` and `POST` are **HTTP verbs** - ways to transfer data to another machine through the internet

- The `GET` request will send data through the URL using a **query string**

- The `POST` request will send data "over the wire" so the user doesn't see the data

---

# Query strings

- A query string is a way to send key-value pairs to a website's back end using a URL

  `https://www.google.com/maps?q=90+John+St,+New+York,+NY+10038`

- In the above example, the key is `q` and the value is `90 John St, New York, NY 10038`

- To add additional keys and values, use an `&`:

  `/process-data?fname=Zach&lname=Feldman`

---

# Form back-end

You'll learn more about processing form data if you learn PHP, Ruby/Sinatra/Rails, Python/Django, etc.

---

# Styling forms

- The default form styles aren't so pretty

- You can add `padding`, a `background-color`, and even change the `font-family` of form inputs

````html
<input type="text" name="q">
````

````css
input{
  padding: 4px;
  font-size: 1.5em;
  font-family: "Arial", sans-serif;
}
````

---

# Exercise

Create a basic HTML + CSS page highlighting all of the topics we've gone over

