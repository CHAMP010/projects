In this step the main goal is to create functions of the app and learning localstorage.

## What will you do?

1. First we will create the functionality for adding note.

   - Get `addButton` with id `#add` using `querySelectior`:

   ```js
   const addButton = document.querySelector("#add");
   ```

   - Create a new function `addNewNote` for adding note and initialize a constant variable `note` by creating `div` element with class `note`:

   ```js
   const addNewNote = (text = "") => {
     const note = document.createElement("div");
     note.classList.add("note");
   };
   ```

   - Create new html layout for note inside `addNewNote` function and insert it into `note`:

   ```js
   const htmlData = `
    <div class="operation">
        <button class="edit"> <i class="fas fa-edit"></i> </button>
        <button class="delete"> <i class="fas fa-trash-alt"></i> </button>
    </div>
   
    <div class="main ${text ? "" : "hidden"}"></div>
    <textarea class="${text ? "hidden" : ""}"></textarea> `;

   note.insertAdjacentHTML("afterbegin", htmlData);
   ```

   - Get references of `editButton`, `delButton`, `mainDiv` and `textArea` inside `addNewNote` function:

   ```js
   // Getting References
   const editButton = note.querySelector(".edit");
   const delButton = note.querySelector(".delete");
   const mainDiv = note.querySelector(".main");
   const textArea = note.querySelector("textarea");
   ```

2. Secondly, we will add the functionality to delete.

   - Add new event listener on `delButton` inside `addNewNote` function, to listen a click:

   ```js
   // Deleting Note
   delButton.addEventListener("click", () => {});
   ```

   - Just, add `note.remove` inside event listener:

   ```js
   // Deleting Note
   delButton.addEventListener("click", () => {
     note.remove();
   });
   ```

3. Then, we will add the functionality inside `addNewNote` function to edit the note.

   - We will assign the variable `text` into `textArea.value` and `mainDiv.innerHTML`. (inside `addNewNote` function.) :

   ```js
   textArea.value = text;
   mainDiv.innerHTML = text;
   ```

   - Create two new event listeners for `editButton` and `textArea` inside `addNewNote` function:

   ```js
   // Editing Note
   editButton.addEventListener("click", () => {});

   textArea.addEventListener("change", (event) => {});
   ```

   - In edit button event listener toggle `hidden` class of `mainDiv` and `textArea`:

   ```js
   editButton.addEventListener("click", () => {
     mainDiv.classList.toggle("hidden");
     textArea.classList.toggle("hidden");
   });
   ```

   - In textArea event listener store text value using `event.target.value` in constant variable `value`. Then, assign that value to `mainDiv.innerHTML`. Also, below the event listener function append child `note` to the `body` of document:

   ```js
   textArea.addEventListener("change", (event) => {
     const value = event.target.value;
     mainDiv.innerHTML = value;

     updateLSData();
   });

   document.body.appendChild(note);
   ```

4. At Last, we will add the event listener on `addButton` to add new note by calling `addNewNote` function. (In the bottom, after `addNewNote` function.) :

   ```js
   addButton.addEventListener("click", () => addNewNote());
   ```
