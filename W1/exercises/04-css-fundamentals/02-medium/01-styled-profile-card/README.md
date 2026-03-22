# CSS Exercise: Styled Profile Card

## Learning Objectives

By completing this exercise, you will be able to:

- [ ] Use multiple CSS properties in a single rule
- [ ] Use the `text-align` property to center text
- [ ] Use hex color codes (like `#666666`)
- [ ] Use the `font-family` property to change fonts
- [ ] Combine multiple declarations in one selector

## Prerequisites

Before starting this exercise, you should have:

- Completed the "CSS Fundamentals" lesson (07-css-fundamentals.md)
- Completed the "Styled Greeting" (Easy) exercise
- Understand how to write multiple CSS properties in one rule

## What You'll Build

You will style a profile card with a name, role, and bio. This is similar to what you might see on a social media profile or an "About Me" section of a website.

The HTML already has classes assigned to elements (like `class="role"`). The CSS selectors are pre-written for you. Your job is to write the CSS declarations inside each selector.

## Tasks

1. **Open `styles.css`** - This is where you'll write your CSS code.

2. **Style the name heading (`h1`)** - Add these declarations:
   - `color: navy;` (makes the name navy blue)
   - `text-align: center;` (centers the text)

3. **Style the role text (`.role`)** - Add these declarations:
   - `color: #666666;` (makes it grey using hex code)
   - `font-style: italic;` (makes it italic)

4. **Style the bio paragraph (`.bio`)** - Add these declarations:
   - `font-size: 16px;`
   - `font-family: Arial, sans-serif;`

## Expected Result

When you complete this exercise, your page will look like this:

```
        Jane Developer
        (Navy blue, centered)

          Web Developer
      (Grey, italic, centered)

I love building websites and learning new things.
    (16px, Arial font)
```

The profile card should have:
- A navy blue, centered name
- A grey, italic role title (also centered)
- A bio paragraph in Arial font

## How to Check Your Work

1. **Save both files** (`index.html` and `styles.css`)

2. **Open `index.html` in your web browser**

3. **Verify the name**:
   - "Jane Developer" should be **navy blue**
   - It should be **centered** on the page

4. **Verify the role**:
   - "Web Developer" should be **grey** (not black)
   - It should be **italic** (slanted text)

5. **Verify the bio**:
   - The text should appear in **Arial font** (looks cleaner/simpler than the default)
   - Font size should be **16px** (standard readable size)

## Common Issues

### Issue: The text isn't centered

**Possible cause:** You might have spelled `text-align` incorrectly or forgotten the hyphen.

**Fix:** Check that you wrote `text-align: center;` (not `textalign` or `text-align: centered`)

### Issue: The hex color isn't working

**Possible cause:** You might have forgotten the `#` symbol at the start.

**Fix:** Hex colors must start with `#`. Write `color: #666666;` (not `color: 666666;`)

### Issue: Multiple properties aren't working

**Possible cause:** You might have forgotten the semicolon between declarations.

**Fix:** Each declaration must end with a semicolon:
```css
h1 {
    color: navy;        /* Semicolon here */
    text-align: center; /* Semicolon here too */
}
```

### Issue: The font didn't change

**Possible cause:** You might have a typo in `font-family`.

**Fix:** Check the spelling: `font-family: Arial, sans-serif;`

Note: `sans-serif` is a fallback - if Arial isn't available on the computer, it will use any sans-serif font.

## Time Estimate

~20 minutes
