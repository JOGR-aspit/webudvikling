# CSS Exercise: Styled Greeting

## Learning Objectives

By completing this exercise, you will be able to:

- [ ] Write CSS rules using element selectors
- [ ] Use the `color` property to change text color
- [ ] Use the `font-size` property to change text size

## Prerequisites

Before starting this exercise, you should have:

- Completed the "CSS Fundamentals" lesson (07-css-fundamentals.md)
- Understand how to link an external CSS file to HTML
- Know the basic structure of a CSS rule (selector, property, value)

## What You'll Build

You will style a simple greeting page. The HTML is already written for you. Your job is to write the CSS that makes the heading blue and the paragraphs black with a larger font size.

## Tasks

1. **Open `styles.css`** - This is where you'll write your CSS code.

2. **Make the main heading blue** - Inside the `h1` selector's curly braces, add:
   - Property: `color`
   - Value: `blue`

3. **Make all paragraphs black** - Inside the `p` selector's curly braces, add:
   - Property: `color`
   - Value: `black`

4. **Make paragraphs use 18px font size** - Inside the `p` selector (you can add to the same selector), add:
   - Property: `font-size`
   - Value: `18px`

## Expected Result

When you complete this exercise, your page will look like this:

```
HELLO, WORLD!
(The heading should be blue)

Welcome to my webpage.
Today I am learning CSS!
(Both paragraphs should be black text, 18px size)
```

## How to Check Your Work

1. **Save both files** (`index.html` and `styles.css`)

2. **Open `index.html` in your web browser** (double-click the file or right-click → Open with → Browser)

3. **Verify the heading**:
   - The text "Hello, World!" should appear in **blue** color

4. **Verify the paragraphs**:
   - Both paragraphs should have **black** text
   - The text should be **larger than normal** (18px instead of the default 16px)

## Common Issues

### Issue: My CSS doesn't work at all!

**Possible causes:**
- Did you save the `styles.css` file after editing it?
- Is the `<link>` tag correct in the HTML? Check that `href="styles.css"` matches your filename exactly.

**Fix:** Save the CSS file and refresh the browser (try Ctrl+F5 or Cmd+Shift+R to force refresh).

### Issue: I get an error or the styles look wrong

**Possible cause:** You might have a typo in a property name or forgotten a semicolon.

**Fix:** Check that:
- Every property name is spelled correctly (`color`, `font-size`)
- Every declaration ends with a semicolon (`;`)
- The property and value are separated by a colon (`:`)

### Issue: The font size didn't change

**Possible cause:** You might have added `font-size` to the wrong selector.

**Fix:** Make sure `font-size: 18px;` is inside the the `p` selector's curly braces `{ }`.

## Time Estimate

~10 minutes
