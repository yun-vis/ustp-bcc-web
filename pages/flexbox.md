---
# permalink: /404.html
layout: single
classes: wide
title: "Flexbox"
header:
  image: /assets/images/teaser/teaser.png
  caption: "Image credit: [**Yun**](http://yun-vis.net)"
last_modified_at: 2025-09-30
---

# Layout without using Flexbox

```css
/* --- Basic Selectors --- */

/* Element selector */

body {
  background-color: #CCCCCC;
  font-size: 16px;
  font-family: Arial, serif;
}

div {
  width: 700px;
  background-color: white;
  margin: 0 auto;
  padding: 15px;
}

section {
  float: left;
  width: 57%;
  margin-right: 5%;
  text-align: justify;
}

aside {
  float: left;
  width: 38%;
}

footer {
  clear: both;
  font-size: 1em;
  background-color: #CCCCCC;
  padding: 20px;
}

img{
  width: 100%;
}

/* Class selector */
/* You should use a class if you need to use the same selector more than once within a page or a site. */
.bold {
  font-weight: bold;
}

/* ID selector */
/* an ID is specific to a single element */
#social-image {
  border: 1px solid black;
}

/* Selector lists*/
/* Combine h1 and h2 into one rule property using comma. */

h1,
h2 {
  color: chocolate;
}

/* The em is simply the font size. In an element with a 2in font, 1em thus means 2in. In other words, 1em is equal to the current font size */
h1 {
  font-size: 2em;
}

h2 {
  font-size: 1.5em;
  margin-top: 10px;
}

p,
ul {
  text-align: justify;
  font-size: 1em;
  line-height: 1.5em;
}

/* --- Combinator Selectors --- */

/* Descendant selector: Applies to all <p> inside a <footer> */
footer p {
  text-align: center;
  font-style: italic;
}

/* Child selector: Applies to <li> elements that are direct children of <ul> */
ul>li {
  list-style: circle;
  margin: 5px;
}

/* Adjacent sibling selector: Styles the <h2> element that immediately follows a <h1> */
h1+h2 {
  color: darkblue;
  font-weight: bold;
}

/* General sibling selector: Styles any <p> element that is a sibling of a <h2> */
h2~p {
  font-style: italic;
  margin-left: 20px;
}

/* --- Pseudo-class Selectors --- */

/* Link state for links */
a:link {
  color: blue;
}

/* Visited state for links */
a:visited {
  color: green;
}

/* Hover state for links */
a:hover {
  color: grey;
}

/* First child element */
.container>p:first-child {
  font-size: 18px;
  color: darkred;
}

/* Last child element */
.container>p:last-child {
  font-size: 14px;
  color: darkgreen;
}

/* --- Pseudo-element Selectors --- */

/* Add content after paragraphs */
p::after {
  content: url('https://api.iconify.design/carbon/edit-off.svg');
  font-size: 18px;
  color: #555555;
}

/* Style first letter of paragraph */
p::first-letter {
  font-size: 24px;
  font-weight: bold;
  color: darkblue;
}

/* --- Attribute Selectors --- */

/* Style input fields of type 'text' */
input[type="text"] {
  border: 1px solid #cccccc;
  padding: 5px;
  width: 200px;
}

/* Style inputs that are required */
input[required] {
  border: 2px dashed red;
}
```

```html
<!DOCTYPE html>

<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>My UE3 Website</title>
    <link rel="stylesheet"
        href="css/style-04a.css">
</head>

<body>

    <!-- You only wrap the content without giving semantics -->
    <div>

        <!-- The <header> element represents a container for introductory content or a set of navigational links. -->
        <header>
            <h1>Dealing with social media</h1>
            <h2>An html example</h2>
            <img id="social-image"
                src="images/header.jpg"
                alt="Social Media Icons">
        </header>

        <!-- Specifies the main content of a document -->
        <main>

            <!-- The <section> element defines a section in a document. -->
            <section>

                <p class="bold">
                    On December 2020, the St.
                    Pölten Sample Club will again
                    be holding a full-day workshop
                    on the topic of "Dealing with
                    social media" at the St.
                    Pölten University of Applied
                    Sciences. The following topics
                    will be discussed: What is the
                    difference between Facebook,
                    Whatsapp and Co. How do I
                    protect my privacy on social
                    platforms?
                </p>

                <form>
                    <p>
                        <label
                            for="name">Name:</label>
                        <input type="text"
                            placeholder="Text input (type='text')">
                    </p>
                    <p>
                        <label
                            for="content">Content:</label>
                        <input type="text"
                            placeholder="Required field"
                            required>
                    </p>
                </form>

                <h2>About the Workshop</h2>

                <p>
                    Lorem ipsum dolor sit amet,
                    consetetur sadipscing elitr,
                    sed diam nonumy eirmod tempor
                    invidunt ut labore et dolore
                    magna aliquyam erat, sed diam
                    voluptua. At vero eos et
                    accusam et justo duo dolores
                    et ea rebum. Stet clita kasd
                    gubergren, no sea takimata
                    sanctus est Lorem ipsum dolor
                    sit amet. Lorem ipsum dolor
                    sit amet, consetetur
                    sadipscing elitr, sed diam
                    nonumy eirmod tempor invidunt
                    ut labore et dolore magna
                    aliquyam erat, sed diam
                    voluptua. At vero eos et
                    accusam et justo duo dolores
                    et ea rebum. Stet clita kasd
                    gubergren, no sea takimata
                    sanctus est Lorem ipsum dolor
                    sit amet. Lorem ipsum dolor
                    sit amet, consetetur
                    sadipscing elitr, sed diam.
                </p>
            </section>

            <!-- The <aside> element defines some content aside from the content it is placed in (like a sidebar). -->
            <aside>
                <h2>Target group</h2>
                <p>People who have little
                    experience with social media
                    and would like to know more
                    about it.</p>

                <h2>Facts and figures</h2>
                <ul>
                    <li>Date: December 24,
                        2020
                    </li>
                    <li>Time: 7:00 p.m.</li>
                    <li>Address: Matthias
                        Corvinus-Strasse
                        15,
                        3100 St. Pölten,
                        Austria
                    </li>
                    <li>Website: <a
                            href="http://www.fhstp.ac.at"
                            target="_blank">www.fhstp.ac.at</a>
                    </li>
                    <li>Contact: Max Doe</li>
                </ul>
            </aside>
        </main>

        <!-- The <footer> element defines a footer for a document or section. -->
        <footer>
            <p>Imprint: St. Pölten Sample Club,
                Jane Doe, <a
                    href="mailto:contact@sampleclub-stp.at">contact@sampleclub-stp.at</a>
            </p>
        </footer>
    </div>
</body>

</html>
```

# Layout using Flexbox

## Basics

flexbox.css
```css
/* --- Flexbox --- */

.flex-container {
  display: flex;
  background-color: rgb(169, 185, 201);
  justify-content: space-between;
}

/* --- Flexbox main layout --- */

/* 
grow: The flex-grow property specifies how much a flex item will grow relative to the rest of the flex items. 
shrink: The flex-shrink property specifies how much a flex item will shrink relative to the rest of the flex items. 
basis: The flex-basis property specifies the initial length of a flex item.  
*/

.flex-item-first {
  flex: 1 1 55%;
  /* grow shrink basis */
  padding-right: 5%;
}

.flex-item-second {
  flex: 1 1 40%;
  /* grow shrink basis */
}

.row {
  display: flex;
  flex-wrap: wrap;
  gap: 5px;
}


/* --- Flexbox navigation bar --- */

.flex-nav-item {
  flex-grow: 1;
  flex: auto;
}
```

style.css
```css
/* --- Basic Selectors --- */

/* Element selector */
body {
  background-color: #CCCCCC;
  font-size: 16px;
  font-family: Arial, serif;
}

div {
  width: 700px;
  background-color: white;
  margin: 0 auto;
  padding: 15px;
}

section {
  float: left;
  /* width: 57%; */
  /* margin-right: 5%; */
  text-align: justify;
}

aside {
  float: left;
  /* width: 38%; */
}

footer {
  clear: both;
  font-size: 1em;
  background-color: #CCCCCC;
  padding: 20px;
}

img{
  width: 100%;
}

/* Class selector */
/* You should use a class if you need to use the same selector more than once within a page or a site. */
.bold {
  font-weight: bold;
}

/* ID selector */
/* an ID is specific to a single element */
#social-image {
  border: 1px solid black;
}

/* Selector lists*/
/* Combine h1 and h2 into one rule property using comma. */
nav,
main {
  padding: 15px;
}

h1,
h2 {
  color: chocolate;
}

/* The em is simply the font size. In an element with a 2in font, 1em thus means 2in. In other words, 1em is equal to the current font size */
h1 {
  font-size: 2em;
}

h2 {
  font-size: 1.5em;
  margin-top: 10px;
}

p,
ul {
  text-align: justify;
  font-size: 1em;
  line-height: 1.5em;
}

/* --- Combinator Selectors --- */

/* Descendant selector: Applies to all <p> inside a <footer> */
footer p {
  text-align: center;
  font-style: italic;
}

/* Child selector: Applies to <li> elements that are direct children of <ul> */
ul>li {
  list-style: circle;
  margin: 5px;
}

/* Adjacent sibling selector: Styles the <h2> element that immediately follows a <h1> */
h1+h2 {
  color: darkblue;
  font-weight: bold;
}

/* General sibling selector: Styles any <p> element that is a sibling of a <h2> */
h2~p {
  font-style: italic;
  margin-left: 20px;
}

/* --- Pseudo-class Selectors --- */

/* Link state for links */
a:link {
  color: blue;
}

/* Visited state for links */
a:visited {
  color: green;
}

/* Hover state for links */
a:hover {
  color: grey;
}

/* First child element */
.container>p:first-child {
  font-size: 18px;
  color: darkred;
}

/* Last child element */
.container>p:last-child {
  font-size: 14px;
  color: darkgreen;
}

/* --- Pseudo-element Selectors --- */

/* Add content after paragraphs */
p::after {
  content: url('https://api.iconify.design/carbon/edit-off.svg');
  font-size: 18px;
  color: #555555;
}

/* Style first letter of paragraph */
p::first-letter {
  font-size: 24px;
  font-weight: bold;
  color: darkblue;
}

/* --- Attribute Selectors --- */

/* Style input fields of type 'text' */
input[type="text"] {
  border: 1px solid #cccccc;
  padding: 5px;
  width: 200px;
}

/* Style inputs that are required */
input[required] {
  border: 2px dashed red;
}
```

```html
<!DOCTYPE html>

<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>My UE3 Website</title>
    <link rel="stylesheet"
        href="css/style-04.css">
    <link rel="stylesheet"
        href="css/flexbox-04.css">
</head>

<body>

    <!-- You only wrap the content without giving semantics -->
    <div>

        <!-- The <header> element represents a container for introductory content or a set of navigational links. -->
        <header>
            <h1>Dealing with social media</h1>
            <h2>An html example</h2>
            <img id="social-image"
                src="images/header.jpg"
                alt="Social Media Icons">
        </header>

        <!-- <div class="flex-container">
            <div class="flex-item-first">1
            </div>
            <div class="flex-item-second">2
            </div>
            <div class="flex-item-third">3
            </div>
            <div class="flex-item-forth">4
            </div>
        </div> -->

        <nav class="flex-container">
            <a class="flex-nav-item-1"
                href="index.html">Home</a>
            <a class="flex-nav-item-2"
                href="pages/page1.html">About
                the Company</a>
            <a class="flex-nav-item-3"
                href="pages/page2.html">Photos</a>
            <a class="flex-nav-item-4"
                href="pages/page3.html">Videos</a>
            <!-- <a class="flex-nav-item-5"
                href="pages/page4.html">YouTube
                Video</a> -->
        </nav>


        <!-- Specifies the main content of a document -->
        <main class="flex-container">

            <!-- The <section> element defines a section in a document. -->
            <section
                class="container flex-item-first">

                <p class="bold">
                    On December 2020, the St.
                    Pölten Sample Club will again
                    be holding a full-day workshop
                    on the topic of "Dealing with
                    social media" at the St.
                    Pölten University of Applied
                    Sciences. The following topics
                    will be discussed: What is the
                    difference between Facebook,
                    Whatsapp and Co. How do I
                    protect my privacy on social
                    platforms?
                </p>

                <form>
                    <p>
                        <label
                            for="name">Name:</label>
                        <input type="text"
                            placeholder="Text input (type='text')">
                    </p>
                    <p>
                        <label
                            for="content">Content:</label>
                        <input type="text"
                            placeholder="Required field"
                            required>
                    </p>
                </form>

                <h2>About the Workshop</h2>

                <p>
                    Lorem ipsum dolor sit amet,
                    consetetur sadipscing elitr,
                    sed diam nonumy eirmod tempor
                    invidunt ut labore et dolore
                    magna aliquyam erat, sed diam
                    voluptua. At vero eos et
                    accusam et justo duo dolores
                    et ea rebum. Stet clita kasd
                    gubergren, no sea takimata
                    sanctus est Lorem ipsum dolor
                    sit amet. Lorem ipsum dolor
                    sit amet, consetetur
                    sadipscing elitr, sed diam
                    nonumy eirmod tempor invidunt
                    ut labore et dolore magna
                    aliquyam erat, sed diam
                    voluptua. At vero eos et
                    accusam et justo duo dolores
                    et ea rebum. Stet clita kasd
                    gubergren, no sea takimata
                    sanctus est Lorem ipsum dolor
                    sit amet. Lorem ipsum dolor
                    sit amet, consetetur
                    sadipscing elitr, sed diam.
                </p>
            </section>

            <!-- The <aside> element defines some content aside from the content it is placed in (like a sidebar). -->
            <aside class="flex-item-second">
                <h2>Target group</h2>
                <p>People who have little
                    experience with social media
                    and would like to know more
                    about it.</p>

                <h2>Facts and figures</h2>
                <ul>
                    <li>Date: December 24,
                        2020
                    </li>
                    <li>Time: 7:00 p.m.</li>
                    <li>Address: Matthias
                        Corvinus-Strasse
                        15,
                        3100 St. Pölten,
                        Austria
                    </li>
                    <li>Website: <a
                            href="http://www.fhstp.ac.at"
                            target="_blank">www.fhstp.ac.at</a>
                    </li>
                    <li>Contact: Max Doe</li>
                </ul>
            </aside>
        </main>

        <!-- The <footer> element defines a footer for a document or section. -->
        <footer>
            <p>Imprint: St. Pölten Sample Club,
                Jane Doe, <a
                    href="mailto:contact@sampleclub-stp.at">contact@sampleclub-stp.at</a>
            </p>
        </footer>
    </div>
</body>

</html>
```

## Dropdown Menu

flexbox.css
```css
/* --- Flexbox --- */

.flex-container {
  display: flex;
  background-color: rgb(169, 185, 201);
  justify-content: space-between;
}

/* --- Flexbox main layout --- */

/* 
grow: The flex-grow property specifies how much a flex item will grow relative to the rest of the flex items. 
shrink: The flex-shrink property specifies how much a flex item will shrink relative to the rest of the flex items. 
basis: The flex-basis property specifies the initial length of a flex item.  
*/

.flex-item-first {
  flex: 1 1 55%;
  /* grow shrink basis */
  padding-right: 5%;
}

.flex-item-second {
  flex: 1 1 40%;
  /* grow shrink basis */
}

.row {
  display: flex;
  flex-wrap: wrap;
  gap: 5px;
}


/* --- Flexbox navigation bar --- */

.flex-nav-item {
  flex-grow: 1;
  flex: auto;
}

/* --- Flexbox dropdown menu --- */

.flex-nav-container{
  background-color: rgb(71, 71, 71);
  padding: 1px;
}

.flex-nav-container ul{
  display: flex;
  position: relative;
  justify-content: space-between;
  list-style: none;
  padding: 0 10px 0 10px; /* top right bottom left */
}

.flex-nav-container a {
  background: rgb(145, 127, 127);
  color: rgb(0, 0, 0);
  justify-content: space-between;
  font-size: 14px;
  text-decoration: none;
  font-weight: bold;
  padding: 5px;
  margin: 5px;
  border: 5px solid silver;
  border-radius: 3px;
}

.flex-nav-container a:hover {
  color: white;
}

ul.drop-menu {
  display: none;
}

ul.drop-menu li {
  height: 35px;
}

li > ul.drop-menu {
  position: absolute;
  list-style-type: none; /* remove bullet points */
  padding-left: 0;
}

li:hover > ul.drop-menu {
  display: block;
  padding-top: 10px;
}
```

```html
<!DOCTYPE html>

<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>My UE3 Website</title>
    <link rel="stylesheet"
        href="css/style-04.css">
    <link rel="stylesheet"
        href="css/flexbox-05.css">
</head>

<body>

    <!-- You only wrap the content without giving semantics -->
    <div>

        <!-- The <header> element represents a container for introductory content or a set of navigational links. -->
        <header>
            <h1>Dealing with social media</h1>
            <h2>An html example</h2>
            <img id="social-image"
                src="images/header.jpg"
                alt="Social Media Banner">
        </header>

        <nav class="flex-nav-container">
            <ul>
                <li class="flex-nav-item-1"><a
                        href="index.html">Home</a>
                </li>
                <li class="flex-nav-item-2"><a
                        href="pages/page1.html">About
                        the Company</a></li>
                <li class="flex-nav-item-3"><a
                        href="pages/page2.html">Photos</a>

                    <ul class="drop-menu">
                        <li><a
                                href="pages/page2.html#anchor-logo">Company
                                Logo</a></li>
                        <li><a
                                href="pages/page2.html#anchor-photo">Company
                                Photos</a></li>
                    </ul>
                </li>
                <li class="flex-nav-item-4">
                    <a
                        href="pages/page3.html">Video</a>
                </li>
            </ul>
        </nav>

        <!-- Specifies the main content of a document -->

        <main class="flex-container">

            <!-- The <section> element defines a section in a document. -->
            <section
                class="container flex-item-first">

                <p class="bold">
                    On December 2020, the St.
                    Pölten Sample Club will again
                    be holding a full-day workshop
                    on the topic of "Dealing with
                    social media" at the St.
                    Pölten University of Applied
                    Sciences. The following topics
                    will be discussed: What is the
                    difference between Facebook,
                    Whatsapp and Co. How do I
                    protect my privacy on social
                    platforms?
                </p>

                <form>
                    <p>
                        <label
                            for="name">Name:</label>
                        <input type="text"
                            placeholder="Text input (type='text')">
                    </p>
                    <p>
                        <label
                            for="content">Content:</label>
                        <input type="text"
                            placeholder="Required field"
                            required>
                    </p>
                </form>

                <h2>About the Workshop</h2>

                <p>
                    Lorem ipsum dolor sit amet,
                    consetetur sadipscing elitr,
                    sed diam nonumy eirmod tempor
                    invidunt ut labore et dolore
                    magna aliquyam erat, sed diam
                    voluptua. At vero eos et
                    accusam et justo duo dolores
                    et ea rebum. Stet clita kasd
                    gubergren, no sea takimata
                    sanctus est Lorem ipsum dolor
                    sit amet. Lorem ipsum dolor
                    sit amet, consetetur
                    sadipscing elitr, sed diam
                    nonumy eirmod tempor invidunt
                    ut labore et dolore magna
                    aliquyam erat, sed diam
                    voluptua. At vero eos et
                    accusam et justo duo dolores
                    et ea rebum. Stet clita kasd
                    gubergren, no sea takimata
                    sanctus est Lorem ipsum dolor
                    sit amet. Lorem ipsum dolor
                    sit amet, consetetur
                    sadipscing elitr, sed diam.
                </p>
            </section>

            <!-- The <aside> element defines some content aside from the content it is placed in (like a sidebar). -->
            <aside class="flex-item-second">
                <h2>Target group</h2>
                <p>People who have little
                    experience with social media
                    and would like to know more
                    about it.</p>

                <h2>Facts and figures</h2>
                <ul>
                    <li>Date: December 24, 2020
                    </li>
                    <li>Time: 7:00 p.m.</li>
                    <li>Address: Matthias
                        Corvinus-Strasse 15, 3100
                        St. Pölten, Austria
                    </li>
                    <li>Website: <a
                            href="http://www.fhstp.ac.at"
                            target="_blank">www.fhstp.ac.at</a>
                    </li>
                    <li>Contact: Max Doe</li>
                </ul>
            </aside>
        </main>

        <!-- The <footer> element defines a footer for a document or section. -->
        <footer>
            <p>Imprint: St. Pölten Sample Club,
                Jane Doe, <a
                    href="mailto:contact@sampleclub-stp.at">contact@sampleclub-stp.at</a>
            </p>
        </footer>
    </div>
</body>

</html>
```