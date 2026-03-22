# CSS Exercise: Styled Blog Preview

## Learning Objectives

By completing this exercise, you will be able to:

- [ ] Use multiple CSS selectors (element and class selectors)
- [ ] Apply multiple declarations to each selector
- [ ] Use hex color codes for precise colors
- [ ] Use the `text-decoration` property to remove underlines
- [ ] Combine all basic CSS properties learned so far

## Prerequisites

Before starting this exercise, you should have:

- Completed the "CSS Fundamentals" lesson (07-css-fundamentals.md)
- Completed "Styled Profile Card" (Medium) exercise
- Be comfortable writing multiple CSS declarations in one rule

## What You'll Build

You will style a blog post preview card - the kind you might see on a blog's homepage that shows a preview of a full article. This includes:

- A blog post title
- A date
- An excerpt (preview of the article)
- A "Read more" link

The HTML is already written for you. Your job is to write all the CSS to make it look professional.

## Tasks

1. **Open `styles.css`** - This is where you'll write all your CSS.

2. **Style the blog title (`h1`)** - Add these three declarations:
   - `color: #2c3e50;` (dark blue using hex code)
   - `text-align: center;`
   - `font-size: 28px;`

3. **Style the date (`.date`)** - Add these three declarations:
   - `color: #666666;` (grey)
   - `font-size: 14px;` (smaller than normal text)
   - `text-align: center;`

4. **Style the excerpt (`.excerpt`)** - Add these three declarations:
   - `font-size: 16px;`
   - `font-family: Georgia, serif;` (a serif font for readability)
   - `color: #333333;` (dark grey, softer than pure black)

5. **Style the "Read more" link (`.read-more`)** - Add these two declarations:
   - `text-decoration: none;` (removes the underline)
   - `color: #3498db;` (bright blue link color)

## Expected Result

When you complete this exercise, your page will look like this:

```
        Why I Love Web Development
        (Dark blue #2c3e50, centered, 28px)

              March 22, 2026
          (Grey #666666, centered, 14px)

Web development is creative and logical at the same
time. You can build anything you imagine!
(Dark grey #333333, Georgia font, 16px)

                Read more
         (Bright blue #3498db, no underline)
```

The blog preview card should have:
- A large, centered, dark blue title
- A smaller, centered, grey date
- A readable excerpt in Georgia font (dark grey text)
- A bright blue "Read more" link without an underline

## How to Check Your Work

1. **Save both files** (`index.html` and `styles.css`)

2. **Open `index.html` in your web browser**

3. **Verify the title**:
   - "Why I Love Web Development" should be **dark blue** (not navy, but a different blue)
   - It should be **centered**
   - It should be **larger** (28px)

4. **Verify the date**:
   - "March 22, 2026" should be **grey**
   - It should be **smaller** than the other text (14px)
   - It should be **centered**

5. **Verify the excerpt**:
   - The text should be in **Georgia font** (looks more traditional/book-like)
   - Color should be **dark grey** (softer than black)
   - Size should be **16px**

6. **Verify the link**:
   - "Read more" should be **bright blue**
   - It should **NOT have an underline**

## Common Issues

### Issue: The link still has an underline

**Possible cause:** You might have written `text-decoration: underline;` instead of `none`.

**Fix:** Change to `text-decoration: none;` to remove the underline.

 Note: `none` removes decorations, `underline` adds one.

### Issue: The hex colors don't look right

**Possible cause:** You might have a typo in the hex code.

**Fix:** Double-check the hex codes:
- `#2c3e50` - should be dark blue (starts with `#2c`)
- `#666666` - should be medium grey (all same digits)
- `#333333` - should be dark grey (all same digits)
- `#3498db` - should be bright blue (starts with `#34`)

### Issue: The Georgia font isn't showing

**Possible cause:** Georgia might not be installed on your computer, or you forgot the fallback.

**Fix:** The `serif` fallback should work. If Georgia isn't installed, any serif font will be used instead.

### Issue: I'm confused about which selector to use

**Hint:** Look at the HTML file:
- `h1` = element selector (targets all `<h1>` elements)
- `.date` = class selector (targets elements with `class="date"`)
- `.excerpt` = class selector (targets elements with `class="excerpt"`)
- `.read-more` = class selector (targets elements with `class="read-more"`)

## Bonus Challenge (Optional)

If you finish early, try adding these extra styles:

1. Make the blog card have a **light grey background**: Add to the HTML a wrapper `<div class="blog-card">` and style it with `background-color: #f5f5f5;`

2. Add **padding** to the card: `padding: 20px;` (adds space inside the card)

3. Add **rounded corners**: `border-radius: 8px;` (makes corners round)

## Time Estimate

~30 minutes
