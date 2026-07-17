# Personal Budget Tracker

A simple static web page (HTML + CSS, no JavaScript yet) for tracking personal income and expenses. Built as part of a beginner web development course — Week 1 laid the page structure and styling; Week 2 upgraded it with a proper table, form, multimedia, and interactive elements.

## Files

- **index.html** — page structure and content
- **style.css** — all styling and layout
- **README.md** — this file

## What's in the page

### Header
A logo image, page title, and short tagline introducing the tracker.

### Add New Expense (form)
A `<form>` with four inputs, each with a matching `id`/`label` pair so JavaScript can hook into them later:
- `expense-name` — text input for the expense name
- `expense-amount` — number input for the amount
- `expense-category` — a `<select>` dropdown with 5 categories: Food, Transport, Rent, Entertainment, Other
- `expense-date` — date picker

A `<button type="button">Add Expense</button>` sits below the fields. It doesn't do anything yet — that functionality is added once JavaScript is introduced.

### Your Expenses (table)
A `<table>` with a `<thead>` header row (Name, Amount, Category, Date) and a `<tbody>` containing 5 hardcoded sample expense rows, used to preview how real data will eventually be displayed.

### Budgeting Tips (video)
An embedded YouTube `<iframe>` with a short budgeting tips video.

### How to use this tracker (collapsible help)
A `<details>`/`<summary>` element that expands to explain how to use the form, without cluttering the page for users who don't need it.

### Footer
A simple copyright line.

## CSS highlights

- **Colored header row & alternating rows** — `thead` is colored blue; `tbody tr:nth-child(even)` gets a light gray background for readability.
- **Hover feedback** — `tbody tr:hover` highlights the row under the cursor; the Add Expense button also gets `cursor: pointer` on hover.
- **Focus states** — `input:focus, select:focus` gives form fields a visible blue outline when active, for accessibility.
- **Selector variety** — the stylesheet demonstrates a descendant selector (`#expenses-display-section td`), a direct child selector (`#add-expense-section > form`), a position-based pseudo-class (`tbody tr:nth-child(even)`), and a negation pseudo-class (`input:not([type="button"])`), on top of the focus state above.

## What's next

Future weeks will add JavaScript to make the Add Expense button actually insert new rows into the table, validate input, and eventually calculate totals and summaries.
