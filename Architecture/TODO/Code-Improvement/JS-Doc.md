# JS Doc

I suggest to apply JS Docs (https://jsdoc.app) to our JS functions and classes, and React Component. This help us out to autocomplete our code in development and also let the code readable for developers. Also, if we want in the future we can generate an HTML documentation website if all our code is documented using JsDocs.


## Example JS functions

**Before:**

```js
let books = [];

function setBook(title, author, visible) {
  books.push({
    title,
    author,
    visible,
  });
}

function getVisibleBooks() {
  return books.filter(book => book.visible);
}
```

**After:**

```js
let books = [];

/**
 * Set books to the database.
 * @param {string} title - The title of the book.
 * @param {string} author - The author of the book.
 * @param {boolean} visible - Show or not the book.
 */
function setBook(title, author, visible) {
  books.push({
    title,
    author,
    visible,
  });
}

/**
 * Get all the visible books.
 * @returns {Array}
 */

function getVisibleBooks() {
  return books.filter(book => book.visible);
}
```

## Example React Components

**Before:**

```js
export const TemplateStepper = ({ template, alert, setAlert }) => {
  ...
};
```

**After:**

```js
/**
 * TemplateStepper Component.
 * @param {Object} props - Component props.
 * @param {Object} props.template - Template info.
 * @param {Object} props.alert - Props that may be used in Material UI Alert component.
 * @param {requestCallback} props.setAlert - The callback that handles the alert's state.
 * @returns {ReactElement}
 */
export const TemplateStepper = ({ template, alert, setAlert }) => {
  ...
};
```


