# CSS Exercise: ID Selectors & Chaining

## Learning Objectives

By completing this exercise, you will be able to:

- [ ] Write ID selectors using the `#` prefix
- [ ] Use selector chaining to target elements with multiple classes
- [ ] Understand when to use ID vs class selectors
- [ ] Build style variations using chained selectors

## Prerequisites

Before starting this exercise, you should have:

- Completed the "CSS Selectors" lesson (08-css-selectors.md)
- Completed the "Element & Class Selectors" (Easy) exercise
- Understand element and class selectors

## What You'll Build

You will style a webpage with a header, footer, and buttons. You'll learn two new concepts:

1. **ID selectors** - Target unique elements with `#idname`
2. **Selector chaining** - Target elements with multiple classes like `.btn.large`

## Tasks

1. **Open `styles.css`** - This file is empty. You'll write everything from scratch.

2. **Style the main header (ID selector)**
   - Selector: Write `#main-header` (with `#` prefix)
   - Declarations: `background-color: #2c3e50;`, `color: white;`, `padding: 20px;`

3. **Style the footer (ID selector)**
   - Selector: Write `#footer` (with `#` prefix)
   - Declarations: `background-color: #666666;`, `color: white;`, `text-align: center;`

4. **Style all buttons (class selector)**
   - Selector: Write `.btn` (with `.` prefix)
   - Declarations: `background-color: green;`, `color: white;`, `padding: 10px 20px;`

5. **Style large buttons (chained selector)**
   - Selector: Write `.btn.large` (no space between!)
   - Declarations: `font-size: 20px;`, `padding: 15px 30px;`

6. **Style primary buttons (chained selector)**
   - Selector: Write `.btn.primary` (no space between!)
   - Declarations: `background-color: blue;`

## Selector Syntax Reminder

| Selector Type | Syntax | Example | Targets |
|---------------|--------|---------|----------|
| **ID** | `#idname` | `#main-header { }` | The ONE element with `id="main-header"` |
| **Chained** | `.class1.class2` | `.btn.large { }` | Elements with BOTH classes |

**Key points**:
- ID selectors use `#` (hash) prefix
- Chained selectors have NO space between class names
- An element can have multiple classes: `<button class="btn large primary">`

## Expected Result

When you complete this exercise, your page will look like this:

```
┌────────────────────────────────────┐
│         MY WEBSITE                 │
│     (Dark blue header #2c3e50,     │
│          white text)               │
└────────────────────────────────────┘

        [Regular] [Large] [Primary] [Large Primary]
        (green)   (green   (blue    (blue, large
                   larger)   same    button)
                            size)

┌────────────────────────────────────┐
│      Copyright 2026                │
│   (Grey footer #666666,            │
│      white text, centered)         │
└────────────────────────────────────┘
```

The four buttons should look different:
- **Regular**: Green background, white text, normal size
- **Large**: Green background, white text, LARGER font (20px)
- **Primary**: BLUE background, white text, normal size
- **Large Primary**: BLUE background, white text, LARGER font (inherits both!)

## How to Check Your Work

1. **Save both files** (`index.html` and `styles.css`)

2. **Open `index.html` in your web browser**

3. **Verify the header**:
   - Should have a **dark blue background** (#2c3e50)
   - Text should be **white**
   - Should have **padding** (space inside)

4. **Verify the footer**:
   - Should have a **grey background** (#666666)
   - Text should be **white**
   - Text should be **centered**

5. **Verify the buttons**:
   - All buttons should have **white text**
   - "Regular" and "Large" should have **green background**
   - "Primary" and "Large Primary" should have **blue background**
   - "Large" and "Large Primary" should be **bigger** (20px font)

## Common Issues

### Issue: ID selector isn't working

**Possible cause:** You used `.` instead of `#` for the ID selector.

**Fix:** ID selectors use `#` (hash), class selectors use `.` (dot):
```css
/* WRONG - this looks for class="main-header" */
.main-header { }

/* RIGHT - this looks for id="main-header" */
#main-header { }
```

### Issue: Chained selector isn't working

**Possible cause:** You put a space between the class names.

**Fix:** NO space for chaining (element must have BOTH classes):
```css
/* WRONG - space means descendant combinator */
.btn .large { }

/* RIGHT - no space means chaining */
.btn.large { }
```

### Issue: The "Large Primary" button isn't both large AND primary

**Possible cause:** The chained selectors aren't being applied correctly.

**Fix:** Make sure you wrote both chained selectors:
- `.btn.large` for large buttons
- `.btn.primary` for primary buttons

The "Large Primary" button has THREE classes (`btn large primary`), so it matches ALL three selectors: `.btn`, `.btn.large`, AND `.btn.primary`.

### Issue: I see `<button>` in my CSS but it's not working

**Possible cause:** You wrote an element selector instead of a class selector.

**Fix:** We're using classes here. Write `.btn` not `button`:
```css
/* Element selector - targets ALL buttons */
button { }

/* Class selector - targets only buttons with class="btn" */
.btn { }
```

## Time Estimate

~20 minutes
