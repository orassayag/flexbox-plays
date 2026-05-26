# Setup and Usage Instructions

## Table of Contents

1. [System Requirements](#system-requirements)
2. [Initial Setup](#initial-setup)
3. [Available Commands](#available-commands)
4. [Project Structure](#project-structure)
5. [Examples Overview](#examples-overview)
6. [Experimenting with the Code](#experimenting-with-the-code)
7. [Extending the Application](#extending-the-application)
8. [Best Practices](#best-practices)
9. [Documentation](#documentation)
10. [Troubleshooting](#troubleshooting)
11. [Version](#version)
12. [Last Updated](#last-updated)

## Getting Started

### Prerequisites

#### System Requirements

- **Web Browser**: A modern web browser (Chrome, Firefox, Safari, or Edge)
- **Text Editor**: A text editor or IDE for viewing/editing code (VSCode recommended)
- **Knowledge**: Basic knowledge of HTML and CSS
- **Node.js**: Version 12 or higher (optional, only for running script shortcuts)

### Initial Setup

#### 1. Install Dependencies

No external dependencies are required for this project as it uses pure HTML and CSS. However, you can clone the repository to your local machine:

```bash
git clone https://github.com/orassayag/flexbox-plays.git
cd flexbox-plays
```

#### 2. Setup

1. Open any HTML file in your browser:
   - Double-click the HTML file, or
   - Right-click → Open with → Your preferred browser

No build process or dependencies are required - this is a pure HTML/CSS project.

## Available Commands

### Development Commands

Since this is a pure HTML/CSS project, there are no build or compilation commands. You can simply edit the files and refresh your browser.

### Running Scripts

While not required, you can use the following `npm` scripts for convenience:

```bash
# Open main example
npm run start

# Open Example 1: Responsive Menu
npm run open:example1

# Open Example 2: Nested Menu
npm run open:example2

# Open Example 3: Grid vs Stack Toggle
npm run open:example3
```

## Project Structure

```
flexbox-plays/
├── index.html          # Basic flexbox ordering example
├── style.css           # Styles for main example
├── example-1/          # Responsive navigation menu
│   ├── menu.html
│   └── style.css
├── example-2/          # Nested flexbox menu with social links
│   ├── nested-menu.html
│   └── style.css
└── example-3/          # Grid vs Stack layout toggle
    ├── grid-vs-stack.html
    └── style.css
```

## Examples Overview

### Main Example (index.html)

Demonstrates basic flexbox ordering with numbered blocks.

**Key Concepts:**

- `display: flex` - Creates a flex container
- `flex: 0 0 100px` - Fixed width flex items
- `order` - Reorders flex items visually
- `justify-content: space-between` - Distributes items with space

### Example 1: Responsive Menu (example-1/menu.html)

A responsive navigation menu that stacks on mobile and displays horizontally on desktop.

**Key Concepts:**

- Mobile-first approach
- Media queries at 768px breakpoint
- `flex: 1 1 0` - Equal width flex items
- `justify-content: flex-start` - Aligns items to start

### Example 2: Nested Menu (example-2/nested-menu.html)

Navigation menu with nested flexbox containers for main menu and social links.

**Key Concepts:**

- Nested flex containers
- `flex-direction: column` on mobile
- `justify-content: space-between` for layout
- Multiple flex containers in one component

### Example 3: Grid vs Stack (example-3/grid-vs-stack.html)

Interactive example with a toggle to switch between grid and stacked layouts.

**Key Concepts:**

- `flex-wrap: wrap` - Allows items to wrap to new lines
- `flex: 0 1 300px` - Flexible width with maximum
- Dynamic class toggling with jQuery
- Article grid layout

## Experimenting with the Code

### Modifying Flexbox Properties

Open any CSS file and try changing these properties:

**Container Properties:**

```css
display: flex;
flex-direction: row | column | row-reverse | column-reverse;
justify-content: flex-start | flex-end | center | space-between | space-around;
align-items: flex-start | flex-end | center | stretch | baseline;
flex-wrap: nowrap | wrap | wrap-reverse;
```

**Item Properties:**

```css
flex: <flex-grow> <flex-shrink> <flex-basis>;
order: <integer>;
align-self: auto | flex-start | flex-end | center | baseline | stretch;
```

### Testing Responsive Behavior

1. Open any example in your browser
2. Resize the browser window
3. Observe how the layout adapts
4. Use browser DevTools to inspect flex properties

### Browser DevTools

Modern browsers have excellent Flexbox debugging tools:

- **Chrome DevTools**: Flex badge, visual guides, alignment controls
- **Firefox DevTools**: Flexbox Inspector, visual overlays
- **Safari DevTools**: Flex container visualization

## Extending the Application

### Adding a New Example

1. **Create Directory**: Create a new folder named `example-n` where `n` is the next number.
2. **Add Files**: Create `index.html` and `style.css` within that directory.
3. **HTML Structure**:
   ```html
   <!DOCTYPE html>
   <html>
     <head>
       <link rel="stylesheet" href="style.css" />
     </head>
     <body>
       <div class="container">
         <!-- Your flex items -->
       </div>
     </body>
   </html>
   ```
4. **CSS Styles**: Use `display: flex` on the container and experiment with properties.
5. **Update Registry**: Add a link to your new example in the main `index.html` and `README.md`.

## Best Practices

- **Flex Basis**: Always prefer `flex-basis` over `width` for flex items to ensure proper resizing.
- **Mobile First**: Design for small screens first, then use media queries for larger displays.
- **Semantic Tags**: Use `<nav>`, `<main>`, `<article>`, and `<footer>` to keep your structure meaningful.
- **Avoid Over-nesting**: Keep your HTML flat to make flexbox behavior easier to predict.
- **Browser Tools**: Use the Flexbox inspector in your browser's DevTools to visualize containers.

## Documentation

### Core Documentation

- **[MDN Flexbox Guide](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout)**: The official web documentation for Flexbox.
- **[CSS-Tricks Complete Guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)**: A visually rich guide to all flex properties.

### External Resources

- **[Flexbox Froggy](https://flexboxfroggy.com/)**: An interactive game to practice alignment.
- **[Flexbox Defense](http://www.flexboxdefense.com/)**: Learn flexbox by positioning towers in a defense game.
- **[Flexbox Playground](https://flexbox.help/)**: An interactive tool to generate flexbox code.

## Common Use Cases

### Centering Content

```css
.container {
  display: flex;
  justify-content: center;
  align-items: center;
}
```

### Responsive Navigation

```css
@media screen and (min-width: 768px) {
  nav ul {
    display: flex;
    justify-content: space-between;
  }
}
```

### Equal Width Columns

```css
.item {
  flex: 1 1 0;
}
```

### Fixed Sidebar Layout

```css
.sidebar {
  flex: 0 0 250px;
}
.main {
  flex: 1 1 auto;
}
```

## Troubleshooting

### Layout Not Working?

- Ensure parent has `display: flex`
- Check for conflicting CSS rules
- Verify browser support (IE11 requires prefixes)

### Items Not Aligning?

- Check `align-items` on container
- Try `align-self` on individual items
- Ensure proper height is set on container

### Responsive Issues?

- Test media query breakpoints
- Check viewport meta tag in HTML
- Use browser DevTools responsive mode

## Version

1.0.0

## Last Updated

2026-05-26

## Author

- **Or Assayag** - _Initial work_ - [orassayag](https://github.com/orassayag)
- Or Assayag <orassayag@gmail.com>
- GitHub: https://github.com/orassayag
- StackOverflow: https://stackoverflow.com/users/4442606/or-assayag?tab=profile
- LinkedIn: https://linkedin.com/in/orassayag
