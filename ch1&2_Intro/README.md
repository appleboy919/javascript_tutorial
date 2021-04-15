# Ch1. Introduction to JavaScript

- Javascript is used in everywhere, browser, server, computer, etc
- JSX: syntax extension of JavaScript created for React JavaScript framework --> Therefore, need to learn JavaScript FIRST!!

---

## JavaScript Landscape

1. JavaScript(Vanilla JavaScript): core language
2. ECMAScript: browser implementation specification for JavaScript
   - Not language itself, official description of how language should be interpreted by browsers
   - Use Babel.js to make it work in current browser implementations
3. TypeScript: abstracted version of JS with additional features added (.ts)
4. Frameworks: allow to write JS-based fron-end applications
   - React, Vue, Angular
   - add an abstraction layer on top of JS --> more streamlined and efficient
5. Babel, npm, WebPack, Gulp: build tools and infrastructure to automate the process of optimizing human-readable JS for the best browser performance
6. Node.js: JS server runtime used to run JS everywhere; used to run npm, WebPack, Babel, and more on computers
   - JS migrated from browser to server

---

## Running JavaScript

- JavaScript can be in HTML with _\<script\>_ tag --> usually placed at the end of the documents (bcs. everything stops when JavaScript is encountered) **==> NOT A MODERN WAY**
- JS as 'external file':

```html
(Example)

<!-- Reference external JS file -->
<script src="script.js"></script>
```

- this can cause significant issues when JS is referenced before the elements it's acting upon have been rendered
- **(Modern)** _async, defer keywords_:

  - _async_ allows the browser to **keep parsing HTML while downloading JS file** (download end -> stop parsing & execute JS file -> continue parsing)
  - _defer_ allows the browser to **load JS file alongside HTML and execute the files after parsing is done**

  ```html
  (Example)

  <!-- use defer keyword -->
  <script src="script.js" defer></script>
  ```

---

## JavaScript Modules

```js
// exporting module

const school = {
   <!-- contents... -->
};

export default school;
```

```js
// importing module

import school from "./school.js"

...
```

- inside HTML, 'type=module' automatically _defers_ js files
  ```html
  <script type="module" src="school.js"></script>
  <script type="module" src="script.js"></script>
  ```
