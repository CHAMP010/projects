In this step the main goal is to build the HTML structure for the note taking app, the structure is a simple.

## What will you do?

1. Create the `<div>` tag with class `heading` inside the `div#container` element:

   ```html
   <div class="heading"></div>
   ```

2. Add nested tags `h1 > i > span` to `<div class="heading">` element:

   Here the `>` means the child of the parent:

   ```html
   <div class="heading">
     <h1>
       <i>
         <span></span>
       </i>
     </h1>
   </div>
   ```

3. Give the class `fas fa-sticky-note` to `<i>` and `title` to `<span>`:

   Here we are using `font awesome icon` of sticky note with the class `fas fa-sticky-note`.

   ```html
   <i class="fas fa-sticky-note">
     <span class="title"></span>
   </i>
   ```

4. Adding `Note Keep` text to the span tag:

   ```html
   <i class="fas fa-sticky-note">
     <span class="title">Note Keep</span>
   </i>
   ```

   The text we are adding to the span tag represents the title of the app. So we'll restrict the word length to three.

5. Create another `<div>` tag with the class `btn-div` inside `<div class="container">` element:

   ```html
   <div class="btn-div"></div>
   ```

6. Add nested tags `button > span + span` to `<div class="btn-div">` element with the classes as shown below:

   ```html
   <div class="btn-div">
     <button class="learn-more add" id="add">
       <span class="circle" aria-hidden="true">
         <span class="icon arrow"></span>
       </span>
       <span class="button-text">Add note</span>
     </button>
   </div>
   ```

   `<span class="button-text">` contains the text of button which will be used to add a new note.
