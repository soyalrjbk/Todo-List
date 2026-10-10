# ✅ To-Do List

A simple notepad-style to-do list built for Week 5 of the 2019 Resilient Coders bootcamp curriculum. Type up to nine tasks on lined "paper," check them off to strike them through, and clear out finished tasks or wipe the whole list with one click.

**Link to project:** _add your live demo link here (e.g. GitHub Pages or Netlify)_

<img width="600" height="400" alt="To-Do List" src="https://github.com/user-attachments/assets/d39f9df4-f82b-4242-bd7f-18b7ac14ff4b" />

## How It's Made:

**Tech used:**

<p align="left">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5" />
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript" />
</p>

The layout is a single `notepad` section with a black header, a "paper" area of task rows, and two action buttons. Each task row pairs a checkbox with a borderless, transparent text input so the tasks look like handwriting on the page.

The lined-paper effect comes entirely from CSS: a `repeating-linear-gradient` paints a thin blue line every 32px on a cream background, and the task rows are spaced to sit on those lines. The page is centered with CSS Grid (`display: grid; place-items: center`), and the rows use Flexbox so the text input stretches to fill the remaining width.

In JavaScript, I grab every checkbox and text input with `querySelectorAll` and loop through them by index, so checkbox `i` always controls text input `i`:

- **Check off a task** – a `change` listener on each checkbox toggles `text-decoration: line-through` on its matching input.
- **Clear Completed** – loops through the checkboxes and, for any that are checked, empties the task text, removes the strikethrough, and unchecks the box.
- **Clear All** – resets every row back to empty and unchecked.

## Optimizations

- Generate task rows with JavaScript (or an "Add task" input) instead of hard-coding nine rows in the HTML, so the list isn't limited to a fixed number of tasks.
- Save tasks to `localStorage` so they survive a page refresh.
- Toggle a CSS class (e.g. `.completed`) instead of setting inline styles, keeping styling in the stylesheet.
- Use a single event listener on the list (event delegation) instead of one listener per checkbox.
- Replace the fixed `700px` width with a responsive `max-width` so the notepad fits on phones.

## Lessons Learned:

This project was a hands-on introduction to the DOM: selecting groups of elements, attaching event listeners, and changing styles and values in response to user actions. Pairing two `NodeList`s by index showed me how to keep related elements in sync, and also why that approach gets fragile as an app grows. On the CSS side, I learned how far you can push a design with gradients, Grid, and Flexbox alone, without any images.




