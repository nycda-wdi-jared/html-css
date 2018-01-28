
# HTML Attributes, IDs and Classes

---


### Lesson Objectives
- What are HTML tag attributes?
- Classes
- IDs


---


### Intro

You can add **attributes** to HTML tags that provide extra information to the browser.

In the below example, `src` is an **attribute** on the `img` tag:

```html
<img src="puppy.jpg">
```

Notice that the attribute goes in the **opening** tag.


---


### Attributes

There are many attributes. Some are **unique** to specific tags, and some are **generic** and can be used with any tag.

Let's take a look at the tag-specific ones first, then some generic ones.


---


### Tag-specific attributes

Take a look at the examples below.

```html
<img src="puppy.jpg" alt="image of puppy in the grass">

<a href="http://www.google.com">Click Me.</a>

<input type="text" placeholder="Enter email address">
```  

The `img` tag has two attributes - a `src` attribute, which contains the url of the image, and an `alt` attribute, which contains the **alt text** for the image, or the text that will display if the image fails to load.

The `a` tag has an `href` attribute, which specifies the URL to go to when the user clicks the link.

The `input` tag has two attributes - `type`, which specifies the type of input tag (text, checkbox, button, etc.) and `placeholder`, which specifies the text that should appear in the input box before the user begins typing.


---


### Generic attributes

Generic attributes, or **global attributes**, can be applied to any tag.

```html
<span hidden>Hello!</span>

<p class="first-paragraph"></p>

<div id="container-div"></div>
```

The `span` has a `hidden` attribute, which prevents it from rendering to the page. Notice that this attribute stands alone, it does not accept a T/F value.

The `p` tag has a `class` attribute and the `div` has an `id` attribute. These are special attributes. Let's take a look at those.


---


### Classes

The `class` attribute is a special global attribute that can go on any element.

The purpose of giving elements classes is so that you can target them all at the same time in CSS.

Let's say you have several elements, all with the same class except one.

```html
<div>Greetings!</div>

<div class="greeting">My</div>
<div class="greeting">name</div>
<div class="greeting">is</div>
<div class="greeting">Tom.</div>
```

Now in your CSS, you can target all the ones with the class `greeting` and turn the font color to red. Only `Greetings!` will remain black.


---


### IDs

IDs are like classes, but only a single HTML element can have a specific ID.

The purpose of using an ID is the same as using a class - so that you can target the element in your CSS.

And remember, only **one** HTML element can have a specific ID!

Therefore, this is wrong:

```html
<div id="greeting">Hello!</div>
<div id="greeting">Nice to meet you.</div>
```

But this is ok:

```html
<div id="hello">Hello!</div>
<div id="greeting">Nice to meet you.</div>
```


---


### Resources

- [MDN - List of HTML attributes](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes)

---


# HTML Attributes, Classes & IDs Exercises


---


Directions: Create a new directory called `html-attributes-practice`. For each exercise, create a new HTML file.

Remember to use your terminal commands: `mkdir`, `cd`, `touch`, and `open`.


---


**Exercise 1: Clothing store**

- Create a new HTML file & open it in the browser.
- Create a header 1 tag that says "Century 21".
- Under that, create an HR.
- Under that, create a div with a class "welcome" that says "Welcome to Century 21!"
- Create 3 paragraphs inside that div, each specifying the clothing type on each of the three floors of the store. For example: "Floor 1: women's clothing, handbags, shoes." Give each div a unique ID.
- In each div, include an img of at least one item on that floor.


---


**Exercise 2: Zoo**

- Create a new HTML file & open it in the browser.
- Create a header 1 tag that says "Bronx Zoo".
- Under that, create an HR.
- Under that, create an img tag with a picture of a zebra.
- Create 3 h2 tags, each stating a section of the zoo, for instance: "Chimpanzees", "Insects", etc.
- Under each h2, create a div with an ID that describes that section of the zoo. In each div, give a description of the animals visitors will find.










#
