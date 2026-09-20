# Personal Blog - CSS Learning Project

Welcome to my personal blog project! This repository is a simple HTML and CSS web page created to practice, demonstrate, and experiment with various CSS styling techniques, selectors, and methods.

---

## 🚀 Features & Project Structure

The project consists of two core files:
1. **`index.html`**: The main webpage markup containing structural elements like the header, main content sections, interest highlights, and a footer.
2. **`styles.css`**: The external stylesheet housing comprehensive style rules and modern CSS selectors.

---

## 🎨 Types of CSS Implemented

This project showcases a rich variety of styling methods and CSS selection techniques:

### 1. Methods of Applying CSS
* **External CSS (`styles.css`)**: The primary method used to maintain clean separation of concerns, linked via the `<link>` tag in the HTML head.
* **Internal CSS (`<style>` block)**: Embedded directly into the `<head>` of `index.html` to style paragraphs.
* **Inline CSS (`style="..."`)**: Applied directly to specific inline elements (e.g., the main page heading).

### 2. CSS Selectors & Advanced Features Used
* **Element Selectors**: Targets standard tags globally (e.g., `body`, `h2`, `section`, `footer`).
* **Class Selectors**: Styles specific UI components using class names (e.g., `.highlight` for emphasized text).
* **ID Selectors**: Targets unique structural elements (e.g., `#header`).
* **Attribute Selectors**: Dynamically targets elements based on attributes (e.g., `a[href^="mailto:"]` for email links).
* **Pseudo-Classes**: Applies styles based on user interaction states (e.g., `a:hover`).
* **Pseudo-Elements**: Formats specific sub-parts of text elements (e.g., `p::first-line` for bold lead lines).
* **Combinators**: Uses adjacent sibling combinators (e.g., `header + main`) to target layout relationships.
* **Specificity Control**: Demonstrates the use of the `!important` declaration for overriding style rules.

---

## 🛠️ Getting Started

To view and run this project locally:
1. Clone or download this repository to your local machine.
2. Ensure both `index.html` and `styles.css` are in the same directory.
3. Open `index.html` in any modern web browser.