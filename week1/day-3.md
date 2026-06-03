# Day 3 — June 3, 2026

**Theme:** HTML & CSS  
**Program:** CodePath FTL Internship — Week 1

## Labs

| # | Lab | Repo |
|---|-----|------|
| 1 | Campus Life Starter | [heartwillgbekle/campus-life-starter](https://github.com/heartwillgbekle/campus-life-starter) |
| 2 | Campus Life Part 1 | [heartwillgbekle/campus-life-p1](https://github.com/heartwillgbekle/campus-life-p1) |

---

## Lesson 1: HTML

### What is HTML?

- **HTML** = HyperText Markup Language
- Invented to:
  - Standardize how websites are written
  - Explain how website text should be structured
  - Link documents together
- Think of HTML as a **skeleton** — it provides structure, but other parts (CSS, JS) make it function and look nice

### Tags & Elements

- Pages are made up of **HTML elements**
- Elements are made up of **tags** and **content**
- Tags wrap content and provide extra information ("markup") about that content

```html
<h1>Code Path</h1>
<!--  ↑ opening tag    ↑ closing tag  -->
```

Common tags:

| Tag | Purpose |
|-----|---------|
| `<h1>` – `<h6>` | Headings (largest to smallest) |
| `<p>` | Paragraph |
| `<img>` | Image |
| `<a>` | Anchor / hyperlink |
| `<ul>` / `<li>` | Unordered list / list item |
| `<div>` | Generic block container |
| `<span>` | Generic inline container |
| `<br>` | Line break (self-closing) |

> 100+ unique tags exist!

### Attributes

- **Attributes** are keywords inside a tag that specify an element's behavior
- Syntax: `attribute="value"`

```html
<!-- class attribute -->
<h1 class="red">Code Path</h1>

<!-- src attribute on a self-closing tag -->
<img src="logo.png">

<!-- href attribute linking to a URL -->
<a href="https://www.google.com">Google it.</a>
```

Common attributes:

| Attribute | Purpose |
|-----------|---------|
| `class` | Groups elements together for CSS styling |
| `id` | Uniquely identifies a single element |
| `src` | Source path for images/media |
| `href` | URL for anchor links |
| `hidden` | Hides an element from display |
| `required` | Marks form inputs as required |

> 170+ unique attributes exist!

### Practice: Anchor Tag

```html
<div>
  <a href="https://www.codepath.org/">Click here to view CodePath's website.</a>
  <!--  ↑ tag  ↑ attribute  ↑ value                                          -->
</div>
```

### Developer Tools

- Used to inspect the inner workings of websites: documents, traffic, memory, accessibility
- **How to open:** Right-click (or Ctrl-click on Mac) any webpage → select **Inspect**
- Explore the **Elements** pane to see HTML tags live on any site

### Semantic HTML

- You *can* use any tag for anything, but best practice is to use tags that match their meaning
- **Semantic HTML** = using tags to indicate the meaning of their content
  - Makes code easier to read and maintain
  - Better for accessibility (screen readers, SEO)
- Just because everything *can* be a `<div>` doesn't mean everything *should* be a `<div>`

```
❌ Everything dumped into <div>s
✅ Organized with <header>, <nav>, <main>, <section>, <footer>
```

> Reference: [Semantic HTML Codepen](https://codepen.io/Devarsh-Thaker-the-bold/pen/NPbaWjp)

---

## Lesson 2: CSS

### What is CSS?

- **CSS** = Cascading Style Sheets
- Defines the **visual design and styling** of a website: fonts, colors, spacing, layouts
- If HTML is the skeleton, CSS is the **skin** — it makes the website visually appealing

### CSS Syntax

```css
selector {
  property: value;   /* ← this is a declaration */
}
```

Example:

```css
p {
  color: blue;
  font-family: sans-serif;
  border: 2px red solid;
}
```

### Selectors

| Selector type | Syntax | Example |
|---------------|--------|---------|
| Element | `tagname` | `p { }` |
| Class | `.classname` | `.bold { }` |
| ID | `#idname` | `#removed-item-33 { }` |
| Pseudo-class | `selector:state` | `a:hover { }` |

```css
/* Element selector */
body {
  background-color: #00C384;
  color: white;
  text-align: center;
}

/* Class selector */
.bold {
  font-weight: bold;
}

/* ID selector */
#removed-item-33 {
  text-decoration: line-through;
}

/* Pseudo-class — style on hover */
a:hover {
  color: green;
}
```

### Specificity & Cascading

CSS applies rules based on **specificity** — more specific rules win:

1. `!important` — overrides everything (use sparingly)
2. **ID selectors** `#id` — most specific
3. **Class selectors** `.class` — medium
4. **Element selectors** `tag` — least specific
5. When specificity is equal, the **later rule** in the file wins

```css
/* Given this HTML: <li class="st" id="st3">Hi</li> */

#st3  { color: cornflowerblue; }  /* ← wins (ID is most specific) */
.st   { color: darkseagreen; }
li    { color: firebrick; }
```

### The Box Model

Every HTML element is represented as a rectangular box:

```
┌──────────────────────────────┐
│           Margin             │  ← space outside the border
│  ┌────────────────────────┐  │
│  │        Border          │  │  ← edge of the box
│  │  ┌──────────────────┐  │  │
│  │  │     Padding      │  │  │  ← space between content & border
│  │  │  ┌────────────┐  │  │  │
│  │  │  │  Content   │  │  │  │  ← text, image, etc.
│  │  │  └────────────┘  │  │  │
│  │  └──────────────────┘  │  │
│  └────────────────────────┘  │
└──────────────────────────────┘
```

```css
body {
  padding: 5px 5px 3px 3px;  /* top right bottom left */
  margin: 10px;
  border: 3px solid green;   /* width style color */
  width: 80%;
}
```

### Display Property

| Value | Behavior |
|-------|----------|
| `block` | Stacks vertically, width/height adjustable (`<div>`) |
| `inline` | Flows with text, width/height not adjustable (`<span>`) |
| `inline-block` | Flows with text but width/height are adjustable |

### Common CSS Properties

- `color`, `background-color`
- `font-family`, `font-size`, `font-weight`
- `border` (shorthand: width style color)
- `padding`, `margin`
- `width`, `height`
- `text-align`, `text-decoration`
- `display`
- `list-style-type`
- `opacity`, `visibility`
- Hover/active styles, animations & transitions
- Responsive design with media queries

> 200+ CSS properties are supported!

---

## Labs

### Lab 1 — Campus Life Starter

**Repo:** [heartwillgbekle/campus-life-starter](https://github.com/heartwillgbekle/campus-life-starter)

- Built a campus life website to showcase student organizations and events
- Practiced writing HTML structure and using semantic tags

### Lab 2 — Campus Life Part 1

**Repo:** [heartwillgbekle/campus-life-p1](https://github.com/heartwillgbekle/campus-life-p1)

- Continued the campus life site
- Applied CSS styling — colors, fonts, spacing, and the box model

---

## Project Preview — Globetrotter

**Link:** [https://courses.codepath.org/courses/site/unit/1#!assignment](https://courses.codepath.org/courses/site/unit/1#!assignment)

Build a **travel guide website** for any location in the world (hometown, dream destination, or fictional place) using HTML & CSS.

**Tips before writing code:**
- Review project description & core features
- Draft a **wireframe** first
- Write **pseudocode** before actual code
- Reference the lab code — many features overlap
- Use Chrome Developer Tools to debug styles
- Stack Overflow is your friend

---

## Key Takeaways

- HTML = structure; CSS = style. Neither works as well without the other.
- Use **semantic HTML** — the right tag for the right content.
- CSS specificity order: `!important` > ID > class > element.
- The **box model** is foundational — every element has content, padding, border, and margin.
- DevTools is essential for debugging both HTML and CSS.

---

## Questions / Things to Explore

- [ ] How do media queries work for responsive design?
- [ ] What is the difference between `margin: auto` and `text-align: center`?
- [ ] When should I use `id` vs `class`?

