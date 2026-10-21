# Lab 4: JavaScript and jQuery Exercises

## Overview

This project contains small, standalone web exercises demonstrating browser-side JavaScript, DOM updates, user input handling, list generation, basic jQuery operations, and loading JSON data with `fetch`. Each exercise is implemented as an HTML page; there is no application build step or package installation.

## Exercises

### `lab4(a)`

- **`question1.html`** — Displays a welcome message and changes the message to “Hello There!” in response to a document click.
- **`question2.html`** — Accepts a value and reports whether it is greater than, equal to, or less than 10. Empty or non-numeric input produces a validation message.
- **`question3.html`** — Generates an ordered list containing the numbers 1 through 5 when the Generate button is clicked. Clicking again replaces the existing list.

### `lab4(b)`

- **`question1.html`** — A blank HTML page with no interactive content currently implemented.
- **`jquery-dom.html`** — Uses jQuery to change text, add a CSS class, and show an alert when a button is clicked.
- **`book.html`** — Fetches `book.json` and displays selected book titles, an author, and genre lists. If loading or parsing fails, it displays an error message.
- **`book.json`** — The book data source, containing two books with title, author, publication year, and genre fields.

## Technologies

- HTML5
- Browser JavaScript and DOM APIs
- jQuery 4.0.0, loaded from `https://code.jquery.com/jquery-4.0.0.min.js` by `lab4(b)/jquery-dom.html`
- JSON, loaded by `lab4(b)/book.html`

## Requirements

- A modern web browser with JavaScript enabled.
- Internet access to load jQuery for `lab4(b)/jquery-dom.html`.
- A local HTTP server to run `lab4(b)/book.html`, because it fetches the adjacent `book.json` file. The other pages can be opened directly in a browser.

No server-side runtime, database, environment variables, or package manager is configured in the project.

## Run the exercises

For the pages that do not fetch local data, open the desired HTML file in a browser. For example, open `lab4(a)/question2.html` to use the number comparison exercise.

To run the book example, start a static HTTP server from the project root. If Python is available, run:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000/lab4(b)/book.html` in the browser. Keep `book.html` and `book.json` in the same directory, as the page requests the data using the relative URL `book.json`.

## Usage

- `lab4(a)/question1.html`: click anywhere in the document to change the message.
- `lab4(a)/question2.html`: enter a number and click **Check**.
- `lab4(a)/question3.html`: click **Generate** to create or regenerate the five-item list.
- `lab4(b)/jquery-dom.html`: the page updates its text and styling when loaded; click **Click me** to display an alert.
- `lab4(b)/book.html`: the page attempts to load and display the book data as soon as it opens.

## Project structure

```text
.
├── lab4(a)/
│   ├── question1.html
│   ├── question2.html
│   └── question3.html
└── lab4(b)/
    ├── book.html
    ├── book.json
    ├── jquery-dom.html
    └── question1.html
```

## Testing

No automated test suite or test command is included. The exercises can be checked by opening their pages in a browser and using the interactions described above.
