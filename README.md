# How-to-make-a-random-number-generator

<sub>In this guide, I will show you how to make a simple random number generator using HTML, CSS and JavaScript. This is an incredibly easy task, and is reccomended for beginners to JS. I will include snippets of all my code so that you may follow along/copy it if you so choose.</sub>
<br>

## HTML
<sub>To begin, we start with the HTML. Follow the example in the code snippet below</sub>
```<!DOCTYPE html>
<html lang="en" dir="ltr">
    <head>
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width, initial-scale 1">
        <meta name="author" content="Shaun Laminger">
        <meta name="description" content="My new cool project">
        <meta name="keywords" content="HTML, CSS, SEO, web, web development">
        <link rel="shortcut icon" href="assets/img/favicon.png?v=2" type="image/x-icon">
        <link rel="preconnect" href="https://fonts.googleapis.com">
        <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
        <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap">
        <link rel="stylesheet" href="assets/style/index.css" media="screen">
        <script src="assets/script/index.js" defer></script>
        <title>How to make a random number generator</title>
    </head>
    <body>
        <main>
            <div class="container">
                <h2 id="number">0</h2>
                <button class="btn" id="generate">Random Number</button>
            </div>
        </main>
    </body>
</html>
```

## CSS
<sub>Same idea for the CSS, although I will include my reset page first</sub>
```@charset "utf-8";

*, *::before, *::after {
  box-sizing: border-box;
}

* {
  margin: 0;
  padding: 0;
  font-family: inherit;
  outline: none;
  border-style: none;
  vertical-align: baseline;
}

html {
  height: 100%;
  font-family: "Nunito Sans", "Open Sans", Arial, sans-serif;
  font-size: 100%;
  font-weight: 400;
  line-height: 1.5;
  text-rendering: geometricPrecision;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

body {
  height: 100%;
}

ul, ol {
  list-style: none;
}

img, picture, video, canvas, svg {
  display: block;
  max-width: 100%;
}

p, h1, h2, h3, h4, h5, h6 {
  overflow-wrap: break-word;
}

li, a, i, figure, img, button,
input[type=button], input[type=submit] {
  -webkit-user-select: none;
     -moz-user-select: none;
          user-select: none;
}

input, textarea, button {
  -webkit-appearance: none;
     -moz-appearance: none;
          appearance: none;
}

input[type=button], input[type=submit], input[type=reset], button, a {
  cursor: pointer;
}

@media (prefers-reduced-motion: reduce) {
  html:focus-within {
    scroll-behavior: auto;
  }

  *, *::before, *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
    scroll-behavior: auto !important;
  }
}
```
<br>
<sub>This is the reset page I use for all of my files, so I think it will serve you well too</sub>
<br>

```@import "./reset.css";

body {
    background-color: #1a162f;  
    color: #fff;
    -webkit-font-smoothing: antialiased;
}

main {
    font-family: 'Inter', sans-serif;
}


.container {
    width: min(100% - 30px, 1080px);
    margin-inline: auto;
}

.btn {
    margin-top:30px;
    margin-left: 420px;
    background-color: #32edd7;
    border: none;
    padding: 16px 32px;
    border-radius: 4px;
    font-size: 16px;
    cursor: pointer;
}

.btn:hover {
    background-color: #2ad1bd;
}

#number {
    margin-top: 30px;
    margin-left: 500px;
    font-size: 28px;
    color: #ffc0cb;
}
```
### JavaScript

<sub>This is a very basic JS code meant for absolute beginners, so this isn't a good practice for more experienced coders.</sub>

```const num = document.getElementById('number');
const btn = document.getElementById('generate');

const randomNum = () => {
    return Math.floor(Math.random() * 1000);
};

btn.addEventListener('click', () => {
    num.innerHTML = randomNum(); 
});
```
