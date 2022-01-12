<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://www.python.org/">
    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c3/Python-logo-notext.svg/768px-Python-logo-notext.svg.png" alt="Logo" width="150">
  </a>

<h3 align="center">Web Development with Python cheatsheet</h3>

  <p align="center">
    This cheatsheet is supposed to help new-comers to the beautiful
    craft of web development with basic commands and features.
    <br />
    <a href="https://github.com/johnunar/cheatsheets/issues">Report Bug</a>
    ·
    <a href="https://github.com/johnunar/cheatsheets/issues">Request Feature</a>
  </p>
</p>



<!-- TABLE OF CONTENTS -->

## Table of Contents

* [Useful Links](#useful-links)
* [HTML](#html)
* [CSS](#css)
* [JS](#js)
* [Django](#django)
* [Roadmap](#roadmap)
* [Contact](#contact)

<!-- Useful links -->

## Useful Links

There are some online tools that will make your life easier.

### [Box-shadow Generator](https://www.cssmatic.com/box-shadow)

Generate your css shadows in a second!
There are more tools on this page, too, like [Gradient Generator](https://www.cssmatic.com/gradient-generator).

### [ColorSpace](https://mycolor.space/)

Generate color palettes and gradients in a second!

### [Google Fonts](https://fonts.google.com/)

Fonts ready for you to use! Just include them in your page with the generated tags.

### [Lorem-ipsum](http://www.lorem-ipsum.cz/)

Need some filler text for your webpage? Lorem-ipsum generator is the place you are looking for.

### [CSS-Tricks](https://css-tricks.com/)

All about CSS! [(Yes, Flexbox, too!)](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

### [Django Docs](https://docs.djangoproject.com/en/)

The only source you need for Django Development

### [Mozilla Foundation Web Docs](https://developer.mozilla.org/en-US/docs/Learn)

The only source you need for modern Web Development.

### [Embed Google Map](https://www.embedgooglemap.net/)

No need for setting up Google Map API. This service lets you just copy & paste!

<!-- HTML -->

# HTML

## Div

```html

<div>Block element</div>
```

## Headings

```html
<h1>Page title</h1>
<h2>Subheading</h2>
<h3>Tertiary heading</h3>
<h4>Quaternary heading</h4>
```

## Paragraph

```html
<p">text</p>
```

## Links

### Outbound Links

```html
<a href="https://example.com/" target="_blank" rel="nofollow">Click here</a>
```

### Mailto Links

```html
<a href="mailto:johnny@example.com?Subject=Hi%20friend" target="_top">Send Mail</a>
```

### Inner Anchors

```html
<a href="#footer">Jump to footnote</a>
<br/>
<a id="footer"></a>Footnote content
```

## Text Decorating

```html
<strong>Bold text</strong>
<em>Italic text (cursive)</em>
<span style="text-decoration: underline;">Underlined text</span>
<abbr title="Abbreviated Text">Abbr. T.</abbr>

<q>Success is a journey not a destination - A quote</q>
<blockquote cite="https://ruwix.com/">
    The Rubik's Cube is the World’s best selling puzzle toy.
</blockquote>
```

## Image

```html
<img src="images/image.jpg" alt="description" height="48" width="100"/>
```

## Video

```html

<video width="200" height="150" controls>
    <source src="vid.mp4" type="video/mp4">
    <source src="vid.ogg" type="video/ogg">
    No video support.
</video>
```

## Audio

```html

<audio controls>
    <source src="sound.ogg" type="audio/ogg">
    <source src="sound.mp3" type="audio/mpeg">
    No audio support.
</audio>
```

## Page Structure

```html

<header>
    <div id="logo">HTML</div>
    <nav>
        <ul>
            <li><a href="/">Home</a>
            <li><a href="/link">Page</a>
        </ul>
    </nav>
</header>
<main role="main">
    <article>
        <h2>Title 1</h2>
        <p>Content 1</p>
    </article>
    <article>
        <h2>Title 2</h2>
        <p>Content 2</p>
    </article>
</main>
<section>
    A group of related content
</section>
<aside>
    Sidebar
</aside>
<footer>
    <p>&copy; HTML CheatSheet</p>
    <address>
        Contact <a href="mailto:me@htmlg.com">me</a>
    </address>
</footer>
```

## Attributes

lowercase attributes, quote values

```html

<tag attributename="value"/>
```

## Lists

### Unordered lists (bullet points)

```html

<ul>
    <li>First</li>
    <li>Second</li>
    <li>Third</li>
</ul>
```

### Ordered lists (numbers or similar)

```html

<ol>
    <li>First</li>
    <li>Second</li>
    <li>Third</li>
</ol>
```

## Forms

```html

<form action="/submit-form" method="post">
    Name: <input name="name" type="text"/> <br/>
    Age: <input max="99" min="1" name="age" step="1" type="number" value="18"/> <br/>
    <select name="gender">
        <option selected="selected" value="male">Male</option>
        <option value="female">Female</option>
    </select><br/>
    <input checked="checked" name="newsletter" type="radio" value="daily"/>Daily
    <input name="newsletter" type="radio" value="weekly"/>Weekly<br/>
    <textarea cols="20" name="comments" rows="5">Comment</textarea><br/>
    <label><input name="terms" type="checkbox" value="tandc"/>Accept terms</label> <br/>
    <input type="submit" value="Submit"/>
</form>

```

## Head Tags

```html
<!doctype html>
<html lang="en" class="no-js">
<head>
    <meta charset="utf-8">
    <meta http-equiv="x-ua-compatible" content="ie=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="canonical" href="https://example.com/"/>
    <title>HTML CheatSheet</title>
    <meta name="description" content="A brief page description">
    <meta name="keywords" content="html,cheatsheet"/>
    <meta property="fb:admins" content="YourFacebookUsername"/>
    <meta property="og:title" content="HTML CheatSheet"/>
    <meta property="og:type" content="website"/>
    <meta property="og:url" content="https://example.com/"/>
    <meta property="og:image" content="https://example.com/images/favicon.ico"/>
    <meta property="og:description" content="A brief page description"/>
    <link rel="apple-touch-icon" href="apple-touch-icon.png">
    <link rel="alternate" hreflang="es" href="https://example.com/spanish/"/>
    <link rel="stylesheet" href="css/styles.css">
    <script src="js/script.js"></script>
</head>

```

# CSS

## Selectors

### Include External CSS File

```html

<link rel="stylesheet" type="text/css" href="css/style.css"/>
```

### Tag

```css
tagname {

}
```

### Class

```css
.class-name {

}
```

### ID

```css
#element-id {

}
```

### Attribute Selectors

```css
a[target="_blank"] {

}

input[type="button"] {

}
```

### Pseudo Classes

```css
a:link {

}

a:active {

}

a:hover {

}

a:visited {

}

p::after {

}

p::before {

}
```

## Media Queries

### Syntax

```css
@media screen and (min-width: 136px) and (max-width: 768px ) {
    .selector {

    }
}
```

# JS

## Include External JS File

```html

<script src="filename.js"></script>
```

## Delay

```js
setTimeout(function () {
    console.log('This prints after 1 second!');
}, 1000); // 1 second

```

## Functions

```js
function addNumbers(a, b) {
    return a + b;
}

x = addNumbers(1, 2);
```

## DOM Manipulations

```js
document.getElementById("elementID").innerHTML = "Hello, World!";
```

## Output

```js
console.log(a);             // write to the browser console
document.write(a);          // write to the HTML
alert(a);                   // output in an alert box
confirm("Really?");         // yes/no dialog, returns true/false depending on user click
prompt("Your age?", "0");    // input dialog. Second argument is the initial value
```

## Comments

```js
/*
Multi line
comment 
*/
// One line

```

## Conditions

### If / If-else

```js
if ((age >= 14) && (age < 19)) {        // logical condition
    status = "Eligible.";               // executed if condition is true
} else {                                // else block is optional
    status = "Not eligible.";           // executed if condition is false
}
```

### Switch

```js
switch (new Date().getDay()) {      // input is current day
    case 6:                         // if (day == 6)
        text = "Saturday";
        break;
    case 0:                         // if (day == 0)
        text = "Sunday";
        break;
    default:                        // else...
        text = "Whatever";
}

```

## Data Types

```js
var age = 18;                           // number 
var name = "Jane";                      // string
var name = {first: "Jane", last: "Doe"};  // object
var truth = false;                      // boolean
var sheets = ["HTML", "CSS", "JS"];       // array
var a;
typeof a;                        // undefined
var a = null;                           // value null
```

## For Loops

```js
for (var i = 0; i < 10; i++) {
    document.write(i + ": " + i * 3 + "<br />");
}

var sum = 0;
for (var i = 0; i < a.length; i++) {
    sum += a[i];
}               // parsing an array

html = "";
for (var i of custOrder) {
    html += "<li>" + i + "</li>";
}

```

## While Loop

```js
var i = 1;                      // initialize
while (i < 100) {               // enters the cycle if statement is true
    i *= 2;                     // increment to avoid infinite loop
    document.write(i + ", ");   // output
}
```

## Do While Loop

```js
var i = 1;                      // initialize
do {                            // enters cycle at least once
    i *= 2;                     // increment to avoid infinite loop
    document.write(i + ", ");   // output
} while (i < 100)               // repeats cycle if statement is true at the end

```

## Break

```js
for (var i = 0; i < 10; i++) {
    if (i == 5) {
        break; // stops and exits the cycle
    }
    document.write(i + ", ");       // last output number is 4
}

```

## Continue

```js
for (var i = 0; i < 10; i++) {
    if (i == 5) {
        continue; // skips the rest of the cycle
    }
    document.write(i + ", ");       // skips 5
}

```

## Variables

```js
var a;                          // variable
var b = "init";                 // string
var c = "Hi" + " " + "Joe";     // = "Hi Joe"
var d = 1 + 2 + "3";            // = "33"
var e = [2, 3, 5, 8];           // array
var f = false;                  // boolean
var g = /()/;                   // RegEx
var h = function () {
};         // function object
const PI = 3.14;                // constant
var a = 1, b = 2, c = a + b;    // one line
let z = 'zzz';                  // block scope local variable

```

## Strict Mode

```js
"use strict";   // Use strict mode to write secure code
x = 1;          // Throws an error because variable is not declared

```

## JQuery

// TODO

# Django

## Conda

Everything you do in Python, do in the virtual environment!

Install Miniconda: (from https://docs.conda.io/en/latest/miniconda.html)

```shell
sh Miniconda3-latest-YOURSYSTEM-x86_64.sh
```

**Create a virtual environment:**

```shell
conda create --name environment-name-here python=3.9
```

**Switch to your environment:**

```shell
conda activate environment-name-here
```

**Install a package from [PyPi](https://pypi.org/):**

```shell
pip install Django
```

**Generate a requirements.txt file:**

```shell
pip freeze > requirements.txt
```

## Django Setup

Generate a new Django project:

```shell
django-admin startproject projectname
```

Start a new app inside the Django project:

```shell
./manage.py startapp app_name
```

## Development server

**Start the server (default port 8000):**

```shell
./manage.py runserver
```

Start the server on port 8888:

```shell
./manage.py runserver 8888
```

## Migrations

Migrations are an essential part of Django development. They reflect our Model changes in the database.

### Make migrations

This will generate the migration files and show you the changes:

```shell
./manage.py makemigrations
```

If you are happy with it, you can **run the migrations**:

### Migrate

```shell
./manage.py migrate
```

This performs the queries needed to sync the database with our models. No SQL needed!
<!-- ROADMAP -->

## Roadmap

* Add more code snippets
* Add more tools
* Generate a more human-friendly cheatsheet (.pdf most likely)

<!-- CONTACT -->

## Contact

Jan Unar

* [unar.dev](https://unar.dev/)
* [@JohnnyUnar](https://twitter.com/JohnnyUnar)
* [johnny@unar.dev](mailto:johnny@unar.dev)

Project Link: [https://github.com/johnunar/cheatsheets](https://github.com/johnunar/cheatsheets)