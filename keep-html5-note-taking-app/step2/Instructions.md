In this step the main goal is to style the note taking app.
As our main goal is to learn localstorage, the stylesheet will be provided.

Small Challenge For You : You can try styling the app by yourself.
If you dont want to style, code is provided below.

## What will you do?

1. Style the note-taking-app.
   Required CSS is provided below:
   Add this code in `style.css`:

   ```css
   .heading {
     width: 100vw;
     height: 4rem;
     background-color: #f1c40f;
     color: #282936;
     box-shadow: 0px 10px 16px rgb(248, 247, 247);
   }

   .heading h1 {
     line-height: 4rem;
     margin-left: 2rem;
     font-weight: 400;
   }

   .title {
     font-family: "Poppins", sans-serif;
   }

   .add:active {
     transform: scale(0.98);
   }

   /* button style start */

   .btn-div {
     font-family: "Poppins", sans-serif;
     position: fixed;
     top: 7rem;
     right: 1rem;
     border: none;
     border-radius: 3px;
     padding: 0.5rem 1rem;
     cursor: pointer;
   }

   button {
     position: relative;
     display: inline-block;
     cursor: pointer;
     outline: none;
     border: 0;
     vertical-align: middle;
     text-decoration: none;
     background: transparent;
     padding: 0;
     font-size: inherit;
     font-family: inherit;
   }

   button.learn-more {
     width: 12rem;
     height: auto;
   }

   button.learn-more .circle {
     transition: all 0.45s cubic-bezier(0.65, 0, 0.076, 1);
     position: relative;
     display: block;
     margin: 0;
     width: 3rem;
     height: 3rem;
     background: #f1c12e;
     border-radius: 1.625rem;
   }

   button.learn-more .circle .icon {
     transition: all 0.45s cubic-bezier(0.65, 0, 0.076, 1);
     position: absolute;
     top: 0;
     bottom: 0;
     margin: auto;
     background: #fff;
   }

   button.learn-more .circle .icon.arrow {
     transition: all 0.45s cubic-bezier(0.65, 0, 0.076, 1);
     position: absolute;
     left: 0.625rem;
     width: 1.125rem;
     height: 0.125rem;
     background: none;
   }

   button.learn-more .circle .icon.arrow::before {
     position: absolute;
     content: "";
     top: -0.25rem;
     right: 0.0625rem;
     width: 0.625rem;
     height: 0.625rem;
     border-top: 0.125rem solid #fff;
     border-right: 0.125rem solid #fff;
     transform: rotate(45deg);
   }

   button.learn-more .button-text {
     transition: all 0.45s cubic-bezier(0.65, 0, 0.076, 1);
     position: absolute;
     top: 0;
     left: 0;
     right: 0;
     bottom: 0;
     padding: 0.75rem 0;
     margin: 0 0 0 1.85rem;
     color: #282936;
     font-weight: 700;
     line-height: 1.6;
     text-align: center;
     text-transform: uppercase;
   }

   button:hover .circle {
     width: 100%;
   }

   button:hover .circle .icon.arrow {
     background: #fff;
     transform: translate(1rem, 0);
   }

   button:hover .button-text {
     color: #fff;
   }

   /* button style end */

   .note {
     background-color: #fff;
     margin: 30px 20px;
     height: 150px;
     width: 300px;
     overflow-y: scroll;
     margin-top: 7rem;
     box-shadow: inset 1px 1px 0 rgba(0, 0, 0, 0.1), inset 0 -1px 0 rgba
         (0, 0, 0, 0.1);
   }

   .note .operation {
     display: flex;
     justify-content: flex-end;
     padding: 0.5rem;
   }

   .note .operation button {
     background-color: transparent;
     border: none;
     color: #fff;
     cursor: pointer;
     font-size: 1rem;
     margin-left: 0.5rem;
   }

   .note textarea {
     outline: none;
     font-family: inherit;
     font-size: 1.2rem;
     border: none;
     height: 300px;
     width: 100%;
     padding: 20px;
   }

   .fa-edit,
   .fa-trash-alt {
     color: #fff;
     padding: 10px;
     background-color: #2ecc71;
     border-radius: 50%;
   }

   .fa-trash-alt {
     background-color: #e74c3c;
   }

   .fa-edit:hover {
     background-color: #fff;
     color: #27ae60;
     filter: drop-shadow(0px 10px 8px rgb(219, 218, 218));
   }

   .fa-trash-alt:hover {
     background-color: #fff;
     color: #e74c3c;
     filter: drop-shadow(0px 10px 8px rgb(219, 218, 218));
   }

   .main {
     padding: 20px;
   }

   .hidden {
     display: none;
   }
   ```