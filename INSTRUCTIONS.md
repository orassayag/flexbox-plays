# Instructions

## Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, or Edge)
- A text editor or IDE for viewing/editing code (VSCode recommended)
- Basic knowledge of HTML and CSS

### Setup

1. Clone or download the repository:
   ```bash
   git clone https://github.com/orassayag/flexbox-plays.git
   cd flexbox-plays
   ```

2. Open any HTML file in your browser:
   - Double-click the HTML file, or
   - Right-click → Open with → Your preferred browser

No build process or dependencies are required - this is a pure HTML/CSS project.

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

## Learning Resources

These examples are based on CSS Flexbox fundamentals. To learn more:

- [MDN Flexbox Guide](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout)
- [CSS Tricks Flexbox Guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [Flexbox Froggy Game](https://flexboxfroggy.com/)

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

## Author

* **Or Assayag** - *Initial work* - [orassayag](https://github.com/orassayag)
* Or Assayag <orassayag@gmail.com>
* GitHub: https://github.com/orassayag
* StackOverflow: https://stackoverflow.com/users/4442606/or-assayag?tab=profile
* LinkedIn: https://linkedin.com/in/orassayag
