# Day 4 — June 4, 2026

**Theme:** Advanced CSS & Responsive Design  
**Program:** CodePath FTL Internship — Week 1

## Labs

| # | Lab | Repo |
|---|-----|------|
| 1 | Bug Crawl Starter | [heartwillgbekle/bug-crawl-starter](https://github.com/heartwillgbekle/bug-crawl-starter) |
| 2 | Campus Life Part 2 | [heartwillgbekle/campus-life-p2](https://github.com/heartwillgbekle/campus-life-p2) |

---

## HTML & CSS Recap

### HTML
- Represents the **skeleton** of the website
- Contains content like text, images, and other media
- Involves writing content contained in tags, often with attributes

### CSS
- Defines the **look, layout, and design** of the website
- Involves selecting elements by tag, class, or id and defining how they should look

---

## Lesson 3: Advanced CSS

### CSS Layouts with Flexbox

**What is Flexbox?**
- CSS supports multiple layout methods, the most popular being **grid** & **flexbox**
- Flexbox:
  - Arranges items in rows or columns
  - Used for aligning and distributing space among items in a container, even those of unknown or dynamic size

**How Flexbox Works**
- Requires a **parent container** (e.g. `<div>`) with one or more **child elements**
- In your CSS, select the parent and apply `display: flex;`

**Parent Container Properties**

```css
.parent {
  display: flex;
  flex-direction: row;
  justify-content: center;
  background-color: purple;
}
```

| Property | Purpose | Common Values |
|----------|---------|---------------|
| `flex-direction` | Sets main axis direction | `row`, `column` |
| `justify-content` | Defines spacing along main axis | `flex-start`, `flex-end`, `center`, `space-around` |
| `flex-wrap` | Wraps items to next row | `wrap`, `nowrap`, `wrap-reverse` |
| `flex-flow` | Shorthand for direction + wrap | `row wrap`, `column wrap-reverse` |

**Child Element Properties**

```css
.child {
  margin: 5px;
  border: 2px solid black;
  background-color: orange;
}
```

**The `flex` Property**
- Shorthand property that sets how a flex item will grow or shrink to fit available space
- Applied to the **child element**

| Value | Behavior |
|-------|----------|
| `flex: auto;` | Initial width determined by content size, but item can grow with container |
| `flex: initial;` | Initial width determined by content size, item won't grow |
| `flex: 1;` | Keep all items the same size (positive integer) |

**Additional Flexbox Properties**
- `align-items` — arranges items relative to axis perpendicular to the flex-direction

### Debugging with Chrome DevTools

- You can view CSS rules in the Chrome dev tools
- Select an element, then view the **Styles pane**
- Remember that CSS **cascades**, so you'll usually see multiple rule sets for the same element

**Steps:**
1. Click on an element
2. Select the Styles tab
3. View the CSS for that element

---

## Lesson 4: Responsive Design

### Why Responsive Design Matters

- Over **50% of global website traffic** comes from mobile
- Building for mobile is important

### Mobile vs Desktop: Major Design Differences

**Important Considerations:**
- Screen size
- User interaction methods (touch vs click)
- Usage contexts

**Design Differences:**
- **Layout:** use single-column layout for mobile
- **Navigation:** use hamburger menu rather than nav bar
- **Interaction:** include large, touch-friendly buttons

### What is Responsive Design?

- Building websites so they automatically adjust their content to match the screen size they are viewed on
- Two ways to accomplish this:
  1. **Flexbox**
  2. **Breakpoints**

### Breakpoints

- Specify how the website should look for different screen sizes
- Accomplished using **media queries**
- **Media query:** conditional checks that allow CSS to respond to styles dynamically based on device and browser criteria

### Writing Media Queries

**Syntax:**
```css
@media [media feature] [operator] [value] {
  /* CSS rules go here */
}
```

**Example:**
```css
@media screen and (max-width: 600px) {
  nav p {
    font-size: 15px;
  }
}
```

**Breaking Down the Media Query:**

```css
@media screen and (max-width: 600px) {
  div {
    color: red;
  }
}
```

| Part | Meaning |
|------|---------|
| `@media` | "At-rule" keyword indicates the style should be applied conditionally |
| `screen` | Specifies the type of media or device. Options: `screen`, `print`, `speech` |
| `and` | Logical operator to combine two conditions |
| `(max-width: 600px)` | Condition the media feature must meet. Viewport must be 600px or less |
| `{ div { color: red; } }` | The styles applied if the media meets both conditions |

### Screen Size Ranges

Common breakpoints:
- **768px** — mobile phones
- **990px** — tablets

**Example with breakpoints:**
```css
/* Mobile phones */
@media screen and (max-width: 768px) {
  .card {
    background-color: green;
  }
}

/* Tablets */
@media screen and (max-width: 990px) {
  .card {
    background-color: blue;
  }
}
```

**Common Responsive Adjustments:**
- Reduce image size for smaller screens
- Reduce title size for smaller screens
- Hide elements for smaller screens (using `display` property)

---

## Labs

### Lab 1 — Bug Crawl Starter

**Repo:** [heartwillgbekle/bug-crawl-starter](https://github.com/heartwillgbekle/bug-crawl-starter)

- Covered strategies to debug HTML & CSS
- Practiced using Chrome DevTools to identify and fix CSS issues
- Debugged CSS rules and element styling

### Lab 2 — Campus Life Part 2

**Repo:** [heartwillgbekle/campus-life-p2](https://github.com/heartwillgbekle/campus-life-p2)

- Applied flexbox to arrange elements on the page
- Added responsive design with media queries
- Practiced adjusting layouts for different screen sizes

---

## Capstone Project Overview

**Requirements:**
- Website should include a frontend and backend
- Website should be deployed using Render or similar deployment method
- Features that enhance the user's experience
- Website must use **one new technology not covered in class**:
  - Language
  - Library
  - API
  - Etc.

**Development Process:**
- Themes
- Problem Statements
- Solutions
- Feature Brainstorming
- Iterate

---

## Key Takeaways

- **Flexbox** is a powerful layout tool for arranging items in rows or columns
- `display: flex;` is applied to the parent container
- `flex-direction`, `justify-content`, and `flex-wrap` control layout behavior
- The `flex` property on child elements controls how they grow/shrink
- **Responsive design** ensures websites work well on all screen sizes
- **Media queries** apply conditional CSS based on device characteristics
- Common breakpoints: 768px (mobile), 990px (tablets)
- Chrome DevTools is essential for debugging flexbox and responsive layouts

---

## Questions / Things to Explore

- [ ] What's the difference between `justify-content` and `align-items`?
- [ ] How do I choose the right breakpoint values for my design?
- [ ] What are CSS Grid layouts and how do they compare to Flexbox?
- [ ] When should I use `flex: auto` vs `flex: 1`?
