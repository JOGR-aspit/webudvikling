# CSS Exercise: Centered Layout

## Learning Objectives

By completing this exercise, you will be able to:

- [ ] Use auto margins to center elements horizontally
- [ ] Combine padding, border, and margin properties
- [ ] Create spacing between elements using margin
- [ ] Build a complete page layout using the box model
- [ ] Apply `box-sizing: border-box` globally

## Prerequisites

Before starting this exercise, you should have:

- Completed the "The Box Model" lesson (10-the-box-model.md)
- Completed the "Card with Borders" (Medium) exercise
- Understand CSS selectors and the box model

## What You'll Build

You will create a complete centered page layout with:
- A **header** at the top
- Three **cards** in the content area
- A **footer** at the bottom
- Everything **centered** on the page using auto margins

This exercise brings together everything you've learned about padding, border, and margin!

## Tasks

1. **Open `styles.css`** - This file is empty. You'll write everything from scratch.

2. **Set box-sizing globally** - Write a universal selector:
   - Selector: `*, *::before, *::after`
   - Declaration: `box-sizing: border-box;`

3. **Style the page body** - Remove default spacing:
   - Selector: `body`
   - Declarations: `margin: 0;`, `padding: 0;`, `font-family: Arial, sans-serif;`, `background-color: #f5f5f5;`

4. **Center the main container** - Create a centered wrapper:
   - Selector: `.container`
   - Declarations:
     - `width: 90%;` (90% of viewport width)
     - `max-width: 800px;` (but never wider than 800px)
     - `margin: 0 auto;` (THIS centers it! 0 top/bottom, auto left/right)
     - `padding: 20px;` (space inside)

5. **Style the header** - Create a page header:
   - Selector: `.header`
   - Declarations:
     - `background-color: #2c3e50;` (dark blue)
     - `color: #ffffff;` (white text)
     - `padding: 20px;` (space inside)
     - `margin-bottom: 30px;` (space below)
     - `text-align: center;`

6. **Style the header title** - Make the heading look good:
   - Selector: `.header h1`
   - Declarations: `margin: 0;`, `font-size: 1.75rem;`

7. **Style the cards** - Create card components:
   - Selector: `.card`
   - Declarations:
     - `background-color: #ffffff;`
     - `padding: 20px;`
     - `border: 1px solid #dddddd;`
     - `margin-bottom: 20px;` (space between cards)
     - `border-radius: 4px;` (slightly rounded corners)

8. **Style card titles** - Make card headings stand out:
   - Selector: `.card-title`
   - Declarations:
     - `color: #2c3e50;`
     - `font-size: 1.25rem;`
     - `margin: 0 0 10px 0;`

9. **Style card content** - Make paragraphs readable:
   - Selector: `.card-content`
   - Declarations:
     - `color: #666666;`
     - `line-height: 1.6;`
     - `margin: 0;`

10. **Create a featured card variant** - Make one card special:
    - Selector: `.card.featured`
    - Declarations:
      - `border-left: 4px solid #27ae60;` (green accent)
      - `background-color: #f0fff4;` (very light green)

11. **Style the footer** - Create a page footer:
    - Selector: `.footer`
    - Declarations:
      - `background-color: #2c3e50;`
      - `color: #ffffff;`
      - `padding: 15px 20px;`
      - `text-align: center;`
      - `margin-top: 30px;`

12. **Style footer text** - Make footer text smaller:
    - Selector: `.footer p`
    - Declarations: `margin: 0;`, `font-size: 0.875rem;`

## Auto Margin Centering Explained

```css
.container {
    width: 80%;        /* Must have a width! */
    margin: 0 auto;    /* 0 = top/bottom, auto = left/right */
}
```

**How it works**:
- `auto` tells the browser: "calculate the remaining space and split it equally"
- If the viewport is 1000px wide and your container is 800px wide...
- The browser calculates: 1000 - 800 = 200px remaining
- It splits 200px equally: 100px on the left, 100px on the right
- Result: perfectly centered!

```
┌────────────────────────────────────────────────────────┐
│                     VIEWPORT                           │
│                                                        │
│    ← 100px →  ┌──────────────────┐  ← 100px →         │
│               │                  │                    │
│               │   .container     │                    │
│               │   (800px wide)   │                    │
│               │                  │                    │
│               └──────────────────┘                    │
│                    ↑                                   │
│              margin: 0 auto                            │
│         (auto calculates equal sides)                  │
└────────────────────────────────────────────────────────┘
```

## Expected Result

When you complete this exercise, your page will look like this:

```
┌────────────────────────────────────────────────────────────────┐
│                                                                │
│   ┌────────────────────────────────────────────────────────┐   │
│   │                    MY WEBSITE                           │   │
│   │              (dark blue #2c3e50 header)                 │   │
│   └────────────────────────────────────────────────────────┘   │
│                           ↑ 30px margin                        │
│   ┌────────────────────────────────────────────────────────┐   │
│   │                                                        │   │
│   │   Card 1: Introduction                                 │   │
│   │   ─────────────────────                                │   │
│   │   This is the first card. It has a white               │   │
│   │   background and a light gray border.                  │   │
│   │   (padding: 20px, border: 1px solid #ddd)              │   │
│   │                                                        │   │
│   └────────────────────────────────────────────────────────┘   │
│                           ↑ 20px margin                        │
│   ┌────────────────────────────────────────────────────────┐   │
│   ┃                                                        │   │
│   ┃   Card 2: Featured Card                                │   │
│   ┃   ─────────────────────                                │   │
│   ┃   This card has a green left border and a              │   │
│   ┃   light green background. It stands out!               │   │
│   ┃   (border-left: 4px solid #27ae60)                     │   │
│   ┃                                                        │   │
│   └────────────────────────────────────────────────────────┘   │
│                           ↑ 20px margin                        │
│   ┌────────────────────────────────────────────────────────┐   │
│   │                                                        │   │
│   │   Card 3: Regular Card                                 │   │
│   │   ─────────────────────                                │   │
│   │   Another regular card with the same styling           │   │
│   │   as the first one.                                    │   │
│   │                                                        │   │
│   └────────────────────────────────────────────────────────┘   │
│                           ↑ 30px margin                        │
│   ┌────────────────────────────────────────────────────────┐   │
│   │              © 2024 My Website                         │   │
│   │              (dark blue #2c3e50 footer)                │   │
│   └────────────────────────────────────────────────────────┘   │
│                                                                │
└────────────────────────────────────────────────────────────────┘
```

## How to Check Your Work

1. **Save both files** (`index.html` and `styles.css`)

2. **Open `index.html` in your web browser**

3. **Verify the container is centered**:
   - The content should be **centered** on the page
   - There should be **equal space** on the left and right
   - The content should be **no wider than 800px**

4. **Verify the header**:
   - Should have a **dark blue background** (#2c3e50)
   - Text should be **white** and **centered**
   - Should have **space below** (30px margin)

5. **Verify the cards**:
   - Should have **white backgrounds** and **light gray borders**
   - Should have **20px of space inside** (padding)
   - Should have **20px gap between** each card (margin)
   - The **featured card** should have a **green left border** and **light green background**

6. **Verify the footer**:
   - Should have a **dark blue background** like the header
   - Should have **space above** (30px margin)
   - Text should be **centered** and **white**

7. **Resize your browser window**:
   - The container should **shrink and grow** with the window
   - At very wide windows, it should **stop at 800px**
   - Everything should stay **centered** at all sizes

## Common Issues

### Issue: The container isn't centering

**Possible cause:** You forgot to add `width` or used `width: auto`.

**Fix:** Auto margins only work with a defined width:
```css
/* WON'T CENTER - no width */
.container {
    margin: 0 auto;
}

/* WILL CENTER - has width */
.container {
    width: 90%;
    margin: 0 auto;
}
```

### Issue: There's no space between my cards

**Possible cause:** You forgot `margin-bottom` on the cards.

**Fix:** Add margin to create gaps:
```css
.card {
    margin-bottom: 20px;  /* Space between cards */
}
```

### Issue: The featured card styles aren't applying

**Possible cause:** Wrong selector format (space vs no space).

**Fix:** No space between classes for chained selector:
```css
/* WRONG - space means descendant */
.card .featured { }

/* RIGHT - no space means both classes on same element */
.card.featured { }
```

### Issue: The page has unwanted white space around the edges

**Possible cause:** Browsers add default margin to the body.

**Fix:** Reset body margin and padding:
```css
body {
    margin: 0;
    padding: 0;
}
```

### Issue: The header or footer has extra space around the text

**Possible cause:** Headings (`h1`, `h2`) have default margins.

**Fix:** Reset heading margins:
```css
.header h1 {
    margin: 0;
}
```

### Issue: My container is wider than 800px on large screens

**Possible cause:** You forgot `max-width`.

**Fix:** Add both `width` and `max-width`:
```css
.container {
    width: 90%;        /* Percentage for small screens */
    max-width: 800px;  /* Limit for large screens */
}
```

## Time Estimate

~30 minutes
