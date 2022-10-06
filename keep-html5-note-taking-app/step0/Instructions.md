In this step our goal is to set up the basic boilerplate code and link the `style.css` file with the `index.html` file.

Before jumping into the code of the project, make sure that you understand the basic structure of the HTML5 document and what the boilerplate code does:

- `<!DOCTYPE html>` tag: Tells the browser that we are using HTML5 and not any previous versions of HTML.
- `<html>` tag: Tells the browser that the content inside the `<html>` tag is, well, HTML!
- `<head>` tag: Tells the browser that the content inside the `<head>` tag is metadata about the HTML document.
- `<body>` tag: Tells the browser that the content inside the `<body>` tag is the content to be displayed on the browser page.
- `<link>` tag: Tells the browser that we want to link an external file with the HTML document, and process it.

It is advised that you go though the [HTML & CSS Fundamentals course](https://codedamn.com/learn/html-css) for a comprehensive and detailed understanding of these tags.

## What will you do?

In this step you are tasked to create a new `style.css` file and link it with the existing `index.html` document.

1. Add a new `<div> </div>` tag inside the `<body>` element. Give the `<div>` element an id `container`, this element will act as a container and will have all the website items inside this element.

2. Create and link the `style.css` file with the `index.html` file. Add the following line of code inside the `<head>` tag of the `index.html` file, using the `<link>` tag. Add another `<link>` tag of `font-awesome-cdn`, that we are going to use for icons.

   ```html
   <link rel="stylesheet" href="style.css" />
   <link
     rel="stylesheet"
     href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.10.0/css/all.min.css"
     integrity="sha512-PgQMlq+nqFLV4ylk1gwUOgm6CtIIXkKwaIHp/PAIWHzig/lKZSEGKEysh0TCVbHJXCLN7WetD8TFecIky75ZfQ=="
     crossorigin="anonymous"
   />
   ```

   Here the `rel` attribute specifies the relationship between the HTML document and the linked file. The `href` attribute specifies the path to the linked file.

3. Import required font from google by adding
   `@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@200;400&display=swap');`
   at the top of `style.css` file.
   Add some styling to the document. Set `margin` and `padding` to `0`, `box-sizing` to `border-box`, `outline` to `none` for all the elements of the HTML Document.

   ```css
   @import url("https://fonts.googleapis.com/css2?family=Poppins:wght@200;400&display=swap");

   * {
     margin: 0;
     padding: 0;
     box-sizing: border-box;
     outline: none;
   }
   ```

   `margin`, `padding` and `box-sizing` are the CSS properties that are used to set the spacing between the elements of the HTML document.

   By settings these values globally to all the elements, it removes the different pre-defined margins and paddings of the elements (which are set by browsers), making it easier to style.

4. Set the `background-color` of the `body` element to `#f4f7f8`, `font-family` to `"Poppins", sans-serif`, `display` to `flex` and `flex-wrap` to `wrap`.

   ```css
   body {
     background-color: #f4f7f8;
     font-family: "Poppins", sans-serif;
     display: flex;
     flex-wrap: wrap;
   }
   ```

Now that we setup the basic boilerplate code and linked the `style.css` file with the `index.html` file, let's move on to the next step and create the HTML.
