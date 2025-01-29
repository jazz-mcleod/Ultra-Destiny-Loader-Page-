# Ultra-Destiny-Loader-Page-

Ultra Destiny Loader Page is designed for a portfolio website of a freelance artist. The loader page features a moving color spectrum paired with her logo.

## HTML Structure

This project includes a simple HTML structure with a loader animation. Below is a breakdown of the HTML code:

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <title>Loader</title>
        <meta name="description" content="">
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link rel="stylesheet" href="/style.css">
    </head>
    <!--LOADER-->
    <body>
        <div class="title">
            <header>
                <h1> Ultra</h1>
                <p>by Destiny</p>
            </header>
        </div>
        <div class="loader">
        </div>
    </body>
</html>

Breakdown
DOCTYPE Declaration: Specifies the document type and version of HTML being used (HTML5).
HTML Tag with Language Attribute: Encloses the entire HTML document and specifies the language as English.
Head Section: Contains metadata and links to external resources.
Body Section: Contains the main content of the webpage, including the title and loader animation.

## CSS Styles

This project includes custom CSS styles for a loader animation and page layout. Below is a breakdown of the CSS code:

```css
/* Resetting default margin, padding, and setting box-sizing */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* Styling the body to center content and set background color */
body {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background: #000;
}

/* Loader styles */
.loader {
    position: relative;
    width: 10px;
    height: 500px;
    transform: rotate(90deg);
    background: linear-gradient(45deg, transparent, red, blue, green, yellow, transparent); 
    animation: animate .7s linear infinite;
}

/* Keyframes for loader animation */
@keyframes animate {
    0% {
        filter: hue-rotate(0deg);
    }
    100% {
        filter: hue-rotate(360deg);
    }
}

/* Inner circle of the loader */
.loader:before {
    content: '';
    position: absolute;
    top: 6px;
    left: 6px;
    right: 6px;
    bottom: 6px;
    border-radius: 50%;
    z-index: 1000;
}

/* Outer glow effect for the loader */
.loader:after {
    content: '';
    position: absolute;
    top: 0px;
    left: 0px;
    right: 0px;
    bottom: 0px;
    background: linear-gradient(45deg, transparent, transparent 40%, #e5f403);
    border-radius: 50%;
    z-index: 1;
    filter: blur(30px);
}

/* Styling for the main heading */
h1 {
    color: #ffff;
    font-size: 60px;
}

/* Styling for the paragraph */
p {
    color: #ffff;
    padding-bottom: 110px;
    font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
    font-size: 17px;
}

/* Positioning the title */
.title {
    position: relative;
    left: 200px;
}

Breakdown
Global Styles: Resets default margin and padding, sets box-sizing to border-box.
Body Styles: Centers content, sets minimum height to 100vh, and applies a black background.
Loader Styles: Defines size, rotation, background gradient, and animation for the loader.
Keyframes for Animation: Creates a hue-rotation animation.
Loader Inner Circle: Adds an inner circle to the loader.
Loader Outer Glow: Adds a glowing effect around the loader.
Heading Styles: Styles the main heading.
Paragraph Styles: Styles the paragraph.
Title Positioning: Positions the title.


