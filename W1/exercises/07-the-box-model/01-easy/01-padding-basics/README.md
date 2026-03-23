# CSS Exercise: Padding Basics

## Learning Objectives

By completing this exercise, you will be able to:

- [ ] Add padding to create space inside an element
- [ ] Use padding shorthand with one value (all sides)
- [ ] Use padding shorthand with two values (top/bottom, left/right)
- [ ] Understand how padding affects the appearance of elements

## Prerequisites

Before starting this exercise, you should have:

- Completed the "The Box Model" lesson (10-the-box-model.md)
- Completed the "CSS Fundamentals" lesson (07-css-fundamentals.md)
- Know how to write CSS declarations

## What You'll Build

You will style a simple info box. The HTML is already written for you. Your job is to add padding to make the content look better by creating breathing room inside the box.

Padding is the space **inside** the border, between the border and the content. Without padding, text looks cramped against the edges.

## Tasks

1. **Open `styles.css`** - This file has selectors ready for you. You'll fill in the declarations.

2. **Style the info box container** - Inside the `.info-box` selector, add:
   - `background-color: #e8f4f8;` (light blue background)
   - `padding: 20px;` (20 pixels on all four sides)

3. **Style the heading** - Inside the `.info-box h2` selector, add:
   - `padding: 10px 15px;` (10px top/bottom, 15px left/right)
   - `margin: 0;` (remove default margin)

4. **Style the paragraph** - Inside the `.info-box p` selector, add:
   - `padding: 15px;` (15 pixels on all four sides)
   - `background-color: #ffffff;` (white background)

## Padding Syntax Reminder

| Shorthand | What It Does | Example |
|-----------|--------------|---------|
| **1 value** | All four sides get same padding | `padding: 20px;` |
| **2 values** | First = top/bottom, Second = left/right | `padding: 10px 20px;` |
| **4 values** | Top, Right, Bottom, Left (clockwise) | `padding: 5px 10px 15px 20px;` |

```
1 value (all sides equal):
┌─────────────────────┐
│                     │
│    padding: 20px    │
│                     │
└─────────────────────┘

2 values (vertical, horizontal):
┌─────────────────────┐
│   ┌─────────────┐   │
│   │ padding:    │   │
│   │ 10px 20px   │   │
│   └─────────────┘   │
└─────────────────────┘
    ↑10px↑     ↑10px↑
    ←──20px──→ ←──20px──→
```

## Expected Result

When you complete this exercise, your info box will look like this:

```
┌────────────────────────────────────────┐
│                                        │
│    ╔══════════════════════════╗        │
│    ║                          ║        │
│    ║     Important Notice     ║        │
│    ║     (padding: 10px 15px) ║        │
│    ║                          ║        │
│    ╠══════════════════════════╣        │
│    ║                          ║        │
│    ║  ┌────────────────────┐  ║        │
│    ║  │                    │  ║        │
│    ║  │ This is important  │  ║        │
│    ║  │ information. The   │  ║        │
│    ║  │ padding makes it   │  ║        │
│    ║  │ easier to read.    │  ║        │
│    ║  │                    │  ║        │
│    ║  │ (white background, │  ║        │
│    ║  │  padding: 15px)    │  ║        │
│    ║  └────────────────────┘  ║        │
│    ║                          ║        │
│    ╚══════════════════════════╝        │
│                                        │
│    (light blue background #e8f4f8,     │
│     padding: 20px on all sides)        │
│                                        │
└────────────────────────────────────────┘
```

## How to Check Your Work

1. **Save both files** (`index.html` and `styles.css`)

2. **Open `index.html` in your web browser**

3. **Verify the info box container**:
   - Should have a **light blue background** (#e8f4f8)
   - Should have **20 pixels of space** on all sides between border and content

4. **Verify the heading**:
   - Should have **10 pixels** of space above and below
   - Should have **15 pixels** of space on left and right
   - Should NOT have extra space around it (margin: 0)

5. **Verify the paragraph**:
   - Should have a **white background**
   - Should have **15 pixels of space** on all sides between edge and text

## Common Issues

### Issue: The padding doesn't look like it's working

**Possible cause:** You might have put the padding on the wrong selector.

**Fix:** Make sure you put declarations inside the correct selector:
```css
/* For the container */
.info-box {
    padding: 20px;
}

/* For the heading INSIDE the box */
.info-box h2 {
    padding: 10px 15px;
}
```

### Issue: I wrote `padding: 10px, 15px;` with a comma

**Possible cause:** CSS doesn't use commas in the padding shorthand.

**Fix:** Remove the comma - use spaces only:
```css
/* WRONG */
padding: 10px, 15px;

/* RIGHT */
padding: 10px 15px;
```

### Issue: The heading has extra space around it

**Possible cause:** Headings have default margin from the browser.

**Fix:** Add `margin: 0;` to remove the default margin:
```css
.info-box h2 {
    padding: 10px 15px;
    margin: 0;    /* This removes the default space */
}
```

### Issue: The paragraph background doesn't show padding

**Possible cause:** You might have added background but forgot padding, or vice versa.

**Fix:** Make sure you have BOTH properties:
```css
.info-box p {
    padding: 15px;              /* Space inside */
    background-color: #ffffff;  /* White background to show the space */
}
```

## Time Estimate

~10 minutes
