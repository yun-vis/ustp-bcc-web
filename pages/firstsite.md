---
# permalink: /404.html
layout: single
classes: wide
title: "Your First Website"
header:
  image: /assets/images/teaser/teaser.png
  caption: "Image credit: [**Yun**](http://yun-vis.net)"
last_modified_at: 2025-09-04
---

# Your First HTML Template
In VS Code, press Shift + 1 and press enter to get a default html template

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```

# Your First HTML Website with inline CSS

```html
<!DOCTYPE html>

<html lang="en-US">

<head>
    <meta charset="UTF-8">
    <title>My UE1 website</title>
</head>

<body
    style="font-family: 'Times New Roman', Times, serif;font-size: 100%;text-align: left;">

    <h1
        style="background-color:#cccccc;color:tomato;font-family: Verdana, Geneva, Tahoma, sans-serif;font-size: 100%;text-align: center;">
        Dealing with social media</h1>
    <img src="fhstp.png" alt="Social Media Icons" width="280">
    <!-- <p class="bold"> -->
    <p>
        On December 2020, the St. Pölten Sample Club will again be holding a
        full-day workshop on the topic of "Dealing with social media" at the St.
        Pölten University of Applied Sciences. The following topics will be
        discussed: What is the difference between Facebook, Whatsapp and Co. How
        do I protect my privacy on social platforms?
    </p>

    <p>
        On December 2020, the St. Pölten Sample Club will again be holding a
        full-day workshop on the topic of "Dealing with social media" at the St.
        Pölten University of Applied Sciences. The following topics will be
        discussed: What is the difference between Facebook, Whatsapp and Co. How
        do I protect my privacy on social platforms?
    </p>

    <audio controls autoplay muted>
        <source src="meow.ogg" type="audio/ogg">
        <!-- <source src="meow.mp3" type="audio/mpeg"> -->
        A cat audio.
    </audio>

    <video width="320" height="240" autoplay muted controls>
        <source src="cat_and_mouse.webm" type="video/webm">
        <!-- <source src="cat_and_mouse.mp4" type="video/mp4"> -->
        A cat video.
    </video>

    <h2
        style="background-color:#cccccc;color:tomato;font-family: Verdana, Geneva, Tahoma, sans-serif;font-size: 100%;text-align: left;">
        Target group</h2>
    <p>People who have little experience with social media and would like to
        know more about it.</p>

    <h2>Facts and figures</h2>

    <ul>
        <li>Date: December 24, 2020</li>
        <li>Time: 7:00 p.m.</li>
        <li>Address: Matthias Corvinus-Strasse 15,
            3100 St. Pölten, Austria</li>
        <li>Website: <a href="http://www.fhstp.ac.at"
                target="_blank">www.fhstp.ac.at</a>
        </li>
        <li>Contact: Max Doe</li>
    </ul>

    <p>Imprint: St. Pölten Sample Club, Jane Doe,
        <a href="mailto:contact@sampleclub-stp.at">contact@sampleclub-stp.at</a>
    </p>

</body>

</html>
```

# Your First HTML Website with external CSS

```html
<!DOCTYPE html>

<html lang="en-US">

<head>
    <meta charset="UTF-8">
    <title>My UE1 website</title>
    <link rel="stylesheet" href="style.css">
</head>

<body>

    <h1>
        Dealing with social media</h1>
    <!-- <img src="fhstp.png" alt="Social Media Icons" width="280"> -->
    <img src="fhstp.png" alt="Social Media Icons" style="width:280px;">
    <!-- <p class="bold"> -->
    <p>
        On December 2020, the St. Pölten Sample Club will again be holding a
        full-day workshop on the topic of "Dealing with social media" at the St.
        Pölten University of Applied Sciences. The following topics will be
        discussed: What is the difference between Facebook, Whatsapp and Co. How
        do I protect my privacy on social platforms?
    </p>

    <p>
        On December 2020, the St. Pölten Sample Club will again be holding a
        full-day workshop on the topic of "Dealing with social media" at the St.
        Pölten University of Applied Sciences. The following topics will be
        discussed: What is the difference between Facebook, Whatsapp and Co. How
        do I protect my privacy on social platforms?
    </p>

    <audio controls autoplay muted>
        <source src="meow.ogg" type="audio/ogg">
        <!-- <source src="meow.mp3" type="audio/mpeg"> -->
        A cat audio.
    </audio>

    <video width="320" height="240" autoplay muted controls>
        <source src="cat_and_mouse.webm" type="video/webm">
        <!-- <source src="cat_and_mouse.mp4" type="video/mp4"> -->
        A cat video.
    </video>

    <h2>
        Target group</h2>
    <p>People who have little experience with social media and would like to
        know more about it.</p>

    <h2>Facts and figures</h2>

    <ul>
        <li>Date: December 24, 2020</li>
        <li>Time: 7:00 p.m.</li>
        <li>Address: Matthias Corvinus-Strasse 15,
            3100 St. Pölten, Austria</li>
        <li>Website: <a href="http://www.fhstp.ac.at"
                target="_blank">www.fhstp.ac.at</a>
        </li>
        <li>Contact: Max Doe</li>
    </ul>

    <p>Imprint: St. Pölten Sample Club, Jane Doe,
        <a href="mailto:contact@sampleclub-stp.at">contact@sampleclub-stp.at</a>
    </p>

</body>

</html>
```

```css
body {
  background-color: #CCCCCC;
}

img {
  width: 100%;
}

a {
  font-weight: bold;
  color:pink;
}
```

- What’s happening is a CSS vs. HTML attribute precedence issue. CSS always overrides HTML attributes when it comes to styling. The width="280" in the HTML sets a default size, but if a CSS rule targets that element, the CSS rule wins because of the Cascading Style Sheets principle.
  - Use a CSS class instead of a global rule
  - Override with inline CSS (stronger than external CSS): <img src="pic.jpg" style="width:280px;">