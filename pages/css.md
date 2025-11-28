---
# permalink: /404.html
layout: single
classes: wide
title: "Cascading Style Sheets (CSS)"
header:
  image: /assets/images/teaser/teaser.png
  caption: "Image credit: [**Yun**](http://yun-vis.net)"
last_modified_at: 2025-09-30
---

# HTML Styles - CSS

CSS stands for Cascading Style Sheets. CSS saves a lot of work. It can control the layout of multiple web pages all at once. [Link](https://www.w3schools.com/html/html_css.asp)


CSS can be added to HTML documents in 3 ways:

- Inline - by using the style attribute inside HTML elements
- Internal - by using a <style> element in the <head> section
- External - by using a <link> element to link to an external CSS file

The most common way to add CSS, is to keep the styles in external CSS files. However, in this tutorial we will use inline and internal styles, because this is easier to demonstrate, and easier for you to try it yourself.

## Inline

```html
<!DOCTYPE html>

<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>My UE2 Website</title>
</head>

<body style="background-color: #CCCCCC;">

    <!-- Inline CSS -->
    <h1 style="color: chocolate;">Dealing with
        social media</h1>
    <img src="images/header.jpg"
        alt="Social Media Icons" width="780">
    <p>
        On December 2020, the St. Pölten Sample
        Club will again be holding a full-day
        workshop on the topic of "Dealing with
        social media" at the St. Pölten University
        of Applied Sciences. The following topics
        will be discussed: What is the difference
        between Facebook, Whatsapp and Co. How do
        I protect my privacy on social platforms?
    </p>

    <p>
        Lorem ipsum dolor sit amet, consetetur
        sadipscing elitr, sed diam nonumy eirmod
        tempor invidunt ut labore et dolore magna
        aliquyam erat, sed diam voluptua. At vero
        eos et accusam et justo duo dolores et ea
        rebum. Stet clita kasd gubergren, no sea
        takimata sanctus est Lorem ipsum dolor sit
        amet. Lorem ipsum dolor sit amet,
        consetetur sadipscing elitr, sed diam
        nonumy eirmod tempor invidunt ut labore et
        dolore magna aliquyam erat, sed diam
        voluptua. At vero eos et accusam et justo
        duo dolores et ea rebum. Stet clita kasd
        gubergren, no sea takimata sanctus est
        Lorem ipsum dolor sit amet. Lorem ipsum
        dolor sit amet, consetetur sadipscing
        elitr, sed diam.
    </p>

    <h2 style="color: chocolate;">Target group
    </h2>
    <p>People who have little experience with
        social media and would like to know more
        about it.</p>

    <h2 style="color: chocolate;">Facts and
        figures</h2>
    <ul>
        <li>Date: December 24, 2020</li>
        <li>Time: 7:00 p.m.</li>
        <li>Address: Matthias Corvinus-Strasse 15,
            3100 St. Pölten, Austria</li>
        <li>Website: <a
                href="http://www.fhstp.ac.at"
                target="_blank">www.fhstp.ac.at</a>
        </li>
        <li>Contact: Max Doe</li>
    </ul>

    <p>Imprint: St. Pölten Sample Club,
        Jane Doe, <a
            href="mailto:contact@sampleclub-stp.at">contact@sampleclub-stp.at</a>
    </p>
</body>

</html>
```

## Internal

```html
<!DOCTYPE html>

<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>My UE3 Website</title>
    <!-- Internal CSS -->
    <style>
        body {
            background-color: #CCCCCC;
        }

        h1 {
            color: chocolate;
        }

        h2 {
            color: chocolate;
        }
    </style>
    <!-- External CSS-->
    <!-- <link rel="stylesheet" href="css/style-01.css"> -->
</head>

<body>
    <h1>Dealing with social media</h1>
    <img src="images/header.jpg"
        alt="Social Media Icons" width="780">
    <!-- <p class="bold"> -->
    <p>
        On December 2020, the St. Pölten Sample
        Club will again be holding a full-day
        workshop on the topic of "Dealing with
        social media" at the St. Pölten University
        of Applied Sciences. The following topics
        will be discussed: What is the difference
        between Facebook, Whatsapp and Co. How do
        I protect my privacy on social platforms?
    </p>

    <p>
        Lorem ipsum dolor sit amet, consetetur
        sadipscing elitr, sed diam nonumy eirmod
        tempor invidunt ut labore et dolore magna
        aliquyam erat, sed diam voluptua. At vero
        eos et accusam et justo duo dolores et ea
        rebum. Stet clita kasd gubergren, no sea
        takimata sanctus est Lorem ipsum dolor sit
        amet. Lorem ipsum dolor sit amet,
        consetetur sadipscing elitr, sed diam
        nonumy eirmod tempor invidunt ut labore et
        dolore magna aliquyam erat, sed diam
        voluptua. At vero eos et accusam et justo
        duo dolores et ea rebum. Stet clita kasd
        gubergren, no sea takimata sanctus est
        Lorem ipsum dolor sit amet. Lorem ipsum
        dolor sit amet, consetetur sadipscing
        elitr, sed diam.
    </p>

    <h2>Target group</h2>
    <p>People who have little experience with
        social media and would like to know more
        about it.</p>

    <h2>Facts and figures</h2>
    <ul>
        <li>Date: December 24, 2020</li>
        <li>Time: 7:00 p.m.</li>
        <li>Address: Matthias Corvinus-Strasse 15,
            3100 St. Pölten, Austria</li>
        <li>Website: <a
                href="http://www.fhstp.ac.at"
                target="_blank">www.fhstp.ac.at</a>
        </li>
        <li>Contact: Max Doe</li>
    </ul>

    <p>Imprint: St. Pölten Sample Club,
        Jane Doe, <a
            href="mailto:contact@sampleclub-stp.at">contact@sampleclub-stp.at</a>
    </p>
</body>

</html>
```

## External

```css
body {
  background-color: #CCCCCC;
}

h1 {
  color: chocolate;
}

h2 {
  color: chocolate;
}
```

```html
<!DOCTYPE html>

<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>My UE3 Website</title>
    <!-- External CSS-->
    <link rel="stylesheet" href="css/style-01.css">
</head>

<body>
    <h1>Dealing with social media</h1>
    <img src="images/header.jpg"
        alt="Social Media Icons" width="780">
    <!-- <p class="bold"> -->
    <p>
        On December 2020, the St. Pölten Sample
        Club will again be holding a full-day
        workshop on the topic of "Dealing with
        social media" at the St. Pölten University
        of Applied Sciences. The following topics
        will be discussed: What is the difference
        between Facebook, Whatsapp and Co. How do
        I protect my privacy on social platforms?
    </p>

    <p>
        Lorem ipsum dolor sit amet, consetetur
        sadipscing elitr, sed diam nonumy eirmod
        tempor invidunt ut labore et dolore magna
        aliquyam erat, sed diam voluptua. At vero
        eos et accusam et justo duo dolores et ea
        rebum. Stet clita kasd gubergren, no sea
        takimata sanctus est Lorem ipsum dolor sit
        amet. Lorem ipsum dolor sit amet,
        consetetur sadipscing elitr, sed diam
        nonumy eirmod tempor invidunt ut labore et
        dolore magna aliquyam erat, sed diam
        voluptua. At vero eos et accusam et justo
        duo dolores et ea rebum. Stet clita kasd
        gubergren, no sea takimata sanctus est
        Lorem ipsum dolor sit amet. Lorem ipsum
        dolor sit amet, consetetur sadipscing
        elitr, sed diam.
    </p>

    <h2>Target group</h2>
    <p>People who have little experience with
        social media and would like to know more
        about it.</p>

    <h2>Facts and figures</h2>
    <ul>
        <li>Date: December 24, 2020</li>
        <li>Time: 7:00 p.m.</li>
        <li>Address: Matthias Corvinus-Strasse 15,
            3100 St. Pölten, Austria</li>
        <li>Website: <a
                href="http://www.fhstp.ac.at"
                target="_blank">www.fhstp.ac.at</a>
        </li>
        <li>Contact: Max Doe</li>
    </ul>

    <p>Imprint: St. Pölten Sample Club,
        Jane Doe, <a
            href="mailto:contact@sampleclub-stp.at">contact@sampleclub-stp.at</a>
    </p>
</body>

</html>
```


# Semantics

```html
<!DOCTYPE html>

<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>My UE2 Website</title>
    <link rel="stylesheet"
        href="css/style-01.css">
</head>

<body>

    <!-- The <header> element represents a container for introductory content or a set of navigational links. -->
    <header>
        <h1>Dealing with social media</h1>
        <img src="images/header.jpg"
            alt="Social Media Icons" width="780">
    </header>

    <!-- Specifies the main content of a document -->
    <main>

        <!-- The <section> element defines a section in a document. -->
        <section>

            <p>
                On December 2020, the St. Pölten
                Sample Club will again be holding
                a full-day workshop on the topic
                of "Dealing with social media" at
                the St. Pölten University of
                Applied Sciences. The following
                topics will be discussed: What is
                the difference between Facebook,
                Whatsapp and Co. How do I protect
                my privacy on social platforms?
            </p>

            <!-- <h2>About the Workshop</h2> -->

            <p>
                Lorem ipsum dolor sit amet,
                consetetur sadipscing elitr, sed
                diam nonumy eirmod tempor invidunt
                ut labore et dolore magna aliquyam
                erat, sed diam voluptua. At vero
                eos et accusam et justo duo
                dolores et ea rebum. Stet clita
                kasd gubergren, no sea takimata
                sanctus est Lorem ipsum dolor sit
                amet. Lorem ipsum dolor sit amet,
                consetetur sadipscing elitr, sed
                diam nonumy eirmod tempor invidunt
                ut labore et dolore magna aliquyam
                erat, sed diam voluptua. At vero
                eos et accusam et justo duo
                dolores et ea rebum. Stet clita
                kasd gubergren, no sea takimata
                sanctus est Lorem ipsum dolor sit
                amet. Lorem ipsum dolor sit amet,
                consetetur sadipscing elitr, sed
                diam.
            </p>
        </section>

        <!-- The <aside> element defines some content aside from the content it is placed in (like a sidebar). -->
        <aside>
            <h2>Target group</h2>
            <p>People who have little experience
                with
                social media and would like to
                know
                more
                about it.</p>

            <h2>Facts and figures</h2>
            <ul>
                <li>Date: December 24, 2020</li>
                <li>Time: 7:00 p.m.</li>
                <li>Address: Matthias
                    Corvinus-Strasse
                    15,
                    3100 St. Pölten, Austria</li>
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
</body>

</html>
```

# Semantics + CSS Selector

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

/* 
li[class] {
  font-size: 120%;
}

li[class="highlight"] {
  background-color: yellow;
}

li[class~="highlight"] {
  color: red;
} 
*/
```

```html
<!DOCTYPE html>

<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>My UE2 Website</title>
    <link rel="stylesheet"
        href="css/style-03.css">
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
            <section class="container">
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
                    <input type="text"
                        placeholder="Text input (type='text')"><br><br>
                    <input type="text"
                        placeholder="Required field"
                        required><br>
                </form>

                <!-- <form>
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
                 -->
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
                    and would like to
                    know more about it.</p>

                <h2>Facts and figures</h2>
                <ul>
                    <li>Date: December 24, 2020
                    </li>
                    <li>Time: 7:00 p.m.</li>
                    <li>Address: Matthias
                        Corvinus-Strasse
                        15,
                        3100 St. Pölten, Austria
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

