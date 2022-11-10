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
