In this step the main goal is to link our app with localstorage.

### What is localStorage?

The localStorage object allows you to save key/value pairs in the browser.
The localStorage object stores data with no expiration date.

The data is not deleted when the browser is closed, and are available for future sessions.

## What will you do?

1. First we will create the function for updating local storage data - `updateLSData`. (Create it above the `addNewNote` function, because we will use `updateLSData` in `addNewNote`.) :

```js
const updateLSData = () => {};
```

2. Select text area data using `querySelectorAll` and store it in constant variable `textAreaData`. Also, create an empty array and store it in constant variable `notes`. (inside `updateLSData`) :

```js
const updateLSData = () => {
  const textAreaData = document.querySelectorAll("textarea");
  const notes = [];
};
```

3. We will use `forEach` loop and store one-by-one single data into `notes` array from `textAreaData`. (inside `updateLSData`)

   - `textAreaData` is an array of data of notes.

```js
textAreaData.forEach((note) => {
  return notes.push(note.value);
});
```

4. Now, we have our array of notes inside `notes`. We will use it to store our notes in `localStorage`.
   We will use `localStorage.setItem` to set notes (as a string) value of key: `notes`. (inside `updateLSData`)

```js
localStorage.setItem("notes", JSON.stringify(notes));
```

5. Now we are almost done with localStorage for setting values. Last thing is to get notes from localStorage and display it whenever user reopens the website.

   - At the bottom of the file, Get notes from `localStorage.getItem` and store it into constant variable `notes`.
   - Create condition of - if `notes` exist run a loop and use the `addNewNote` function for adding new note from localStorage `notes`.

   ```js
   // Getting LocalStorage
   const notes = JSON.parse(localStorage.getItem("notes"));

   if (notes) {
     notes.forEach((note) => addNewNote(note));
   }
   ```

6. At last, we will update `localStorage` data when we are editing and deleting notes.

- For Delete :

```js
delButton.addEventListener("click", () => {
  note.remove();
  updateLSData();
});
```

- For Edit :

```js
textArea.addEventListener("change", (event) => {
  const value = event.target.value;
  mainDiv.innerHTML = value;

  updateLSData();
});
```
