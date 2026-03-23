# CSS Exercise: Card with Borders

## Learning Objectives

By completing this exercise, you will be able to:

- [ ] Combine padding and border properties
- [ ] Use border shorthand (width, style, color)
- [ ] Add borders to individual sides of an element
- [ ] Apply `box-sizing: border-box` for predictable sizing

## Prerequisites

Before starting this exercise, you should have:

- Completed the "The Box Model" lesson (10-the-box-model.md)
- Completed the "Padding Basics" (Easy) exercise
- Understand CSS selectors and declarations

## What You'll Build

You will create a styled card component with borders. You'll learn how to:
- Use `box-sizing: border-box` so padding and border don't make elements larger than expected
- Add borders around the entire card
- Add borders to specific sides (like just the bottom or left)
- Create a professional-looking card design

## Tasks

1. **Open `styles.css`** - This file is empty. You'll write all the CSS yourself.

2. **Set box-sizing for all elements** - Write a universal selector rule:
   - Selector: `*` (asterisk - targets everything)
   - Declarations: `box-sizing: border-box;`

3. **Style the card container** - Create a `.card` selector:
   - `background-color: #ffffff;` (white background)
   - `padding: 20px;` (space inside)
   - `border: 1px solid #cccccc;` (light gray border)
   - `margin: 20px;` (space around the card)
   - `max-width: 400px;` (don't get too wide)

4. **Style the card title** - Create a `.card-title` selector:
   - `font-size: 1.5rem;` (larger text)
   - `color: #2c3e50;` (dark blue-gray)
   - `padding-bottom: 10px;` (space below text)
   - `margin: 0;` (remove default margin)

5. **Add a bottom border to the title area** - Create a `.card-title` selector (add to existing):
   - `border-bottom: 2px solid #3498db;` (blue line under title)

6. **Style the card content** - Create a `.card-content` selector:
   - `padding-top: 15px;` (space above content)
   - `color: #333333;` (dark gray text)
   - `line-height: 1.6;` (better readability)

7. **Create a featured card variant** - Create a `.card.featured` selector:
   - `border-left: 4px solid #e74c3c;` (red accent on left side)
   - `background-color: #fff5f5;` (very light red/pink background)

## Border Syntax Reminder

| Property | Syntax | Example |
|----------|--------|---------|
| **All sides** | `border: width style color;` | `border: 1px solid #ccc;` |
| **One side** | `border-{side}: width style color;` | `border-left: 4px solid red;` |
| **Just width** | `border-width: value;` | `border-width: 2px;` |
| **Just style** | `border-style: value;` | `border-style: solid;` |
| **Just color** | `border-color: value;` | `border-color: blue;` |

**Sides**: `top`, `right`, `bottom`, `left`

**Border styles**: `solid`, `dashed`, `dotted`, `double`, `none`

## Box-Sizing Reminder

```css
/* Without border-box (default): */
width: 300px + padding: 20px + border: 5px = 350px total!

/* With border-box: */
width: 300px (includes padding and border) = 300px total!
```

**Always use `box-sizing: border-box;` for predictable sizing.**

## Expected Result

When you complete this exercise, you'll have two cards:

```
REGULAR CARD:
┌────────────────────────────────────┐
│                                    │
│   Getting Started with CSS         │
│   ─────────────────────────        │ ← blue bottom border
│                                    │
│   This card has a simple border    │
│   around it. The padding creates   │
│   space between the text and       │
│   the border.                      │
│                                    │
└────────────────────────────────────┘
(white background, 1px gray border)


FEATURED CARD:
┃────────────────────────────────────┐
┃                                    │
┃   Featured: Pro Tips               │
┃   ─────────────────────────        │ ← blue bottom border
┃                                    │
┃   This card has a red accent       │
┃   border on the left side and      │
┃   a light red background.          │
┃                                    │
└────────────────────────────────────┘
↑
4px solid red border (border-left)
(light red background #fff5f5)
```

## How to Check Your Work

1. **Save both files** (`index.html` and `styles.css`)

2. **Open `index.html` in your web browser**

3. **Verify the regular card**:
   - Should have a **white background**
   - Should have a **1px light gray border** on all sides
   - Should have **20px of space** inside (between text and border)
   - Title should have a **blue line** underneath it

4. **Verify the featured card**:
   - Should have a **4px red border** on the LEFT side only
   - Should have a **light red/pink background**
   - Should still have the blue line under the title
   - Should look different from the regular card

5. **Verify box-sizing is working**:
   - The featured card should be the **same width** as the regular card
   - The left border should NOT make the card wider

## Common Issues

### Issue: The left border makes my card wider

**Possible cause:** You forgot to set `box-sizing: border-box`.

**Fix:** Add this at the top of your CSS:
```css
* {
    box-sizing: border-box;
}
```

### Issue: The border shorthand isn't working

**Possible cause:** You might have written the values in the wrong format.

**Fix:** Border shorthand needs three values: width, style, color:
```css
/* WRONG - missing style */
border: 1px #cccccc;

/* RIGHT - width, style, color */
border: 1px solid #cccccc;
```

### Issue: The featured card doesn't look different

**Possible cause:** The chained selector `.card.featured` needs NO space between classes.

**Fix:** Make sure there's no space:
```css
/* WRONG - space means "featured inside card" */
.card .featured { }

/* RIGHT - no space means "element with BOTH classes" */
.card.featured { }
```

### Issue: The title's bottom border isn't showing

**Possible cause:** You might have used `border-bottom-width` instead of the shorthand.

**Fix:** Use the full shorthand:
```css
/* This might not work if style/color aren't set */
border-bottom-width: 2px;

/* This works - sets everything at once */
border-bottom: 2px solid #3498db;
```

### Issue: My card is too wide

**Possible cause:** You forgot `max-width` or the container is too large.

**Fix:** Add max-width to the card:
```css
.card {
    max-width: 400px;
    /* Other styles... */
}
```

## Time Estimate

~20 minutes
