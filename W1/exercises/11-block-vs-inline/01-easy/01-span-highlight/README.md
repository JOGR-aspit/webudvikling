# CSS Exercise: Span Highlight

## Learning Objectives

By completing this exercise, you will be able to:

- [ ] Use `<span>` tags to style specific parts of text
- [ ] Apply classes to inline elements
- [ ] Style spans with background colors, text colors, and font properties
- [ ] Understand how inline elements flow within text

## Prerequisites

Before starting this exercise, you should have:

- Completed the "Block vs Inline Elements" lesson (11-block-vs-inline-elements.md)
- Completed the "CSS Fundamentals" lesson (07-css-fundamentals.md)
- Know how to write CSS declarations
- Understand the difference between block and inline elements

## What You'll Build

You will style a simple article with highlighted text. The HTML is already written for you - it contains several `<span>` elements with different classes. Your job is to write CSS that styles these spans to highlight important words, emphasize keywords, and format author names.

`<span>` is an **inline element** - it stays on the same line as surrounding text and only takes the width it needs. This makes it perfect for styling individual words or phrases within a paragraph.

## Tasks

1. **Open `styles.css`** - This file is empty. You'll write the CSS from scratch.

2. **Style the `.highlight` class** - Create a selector for `.highlight` and add:
   - `background-color: #fff3cd;` (light yellow background)
   - `padding: 2px 4px;` (small padding for visual separation)
   - `border-radius: 3px;` (slightly rounded corners)

3. **Style the `.keyword` class** - Create a selector for `.keyword` and add:
   - `color: #c0392b;` (dark red text color)
   - `font-weight: bold;` (bold text)

4. **Style the `.author-name` class** - Create a selector for `.author-name` and add:
   - `font-style: italic;` (italic text)
   - `color: #7f8c8d;` (gray text color)

## Span Syntax Reminder

```html
<!-- Span wraps inline content - stays on same line -->
<p>This is normal text with a <span class="highlight">highlighted word</span> inside.</p>
```

```
VISUAL RESULT:

This is normal text with a highlighted word inside.
                      └──────────┘
                     (yellow background)
```

| Property | What It Does | Example |
|----------|--------------|---------|
| `background-color` | Colors the area behind text | `background-color: yellow;` |
| `color` | Changes text color | `color: red;` |
| `font-weight` | Makes text bold or light | `font-weight: bold;` |
| `font-style` | Makes text italic | `font-style: italic;` |
| `padding` | Adds space inside the span | `padding: 2px 4px;` |

## Expected Result

When you complete this exercise, your article will look like this:

```
┌────────────────────────────────────────────────────────────┐
│                                                            │
│  Understanding Inline Elements                             │
│                                                            │
│  By Jane Developer • March 2024                           │
│     └──────────────┘                                      │
│     (italic, gray)                                        │
│                                                            │
│  Inline elements are fundamental to web development.      │
│                         └─────────────────────┘           │
│                         (yellow highlight)                │
│                                                            │
│  The span element is used to style parts of text.        │
│      └─────┘                                              │
│      (red, bold)                                          │
│                                                            │
│  Unlike block elements, inline elements stay on the      │
│                         └─────────────┘                   │
│                         (yellow highlight)                │
│                                                            │
│  same line and only take the width they need.            │
│           └─────┘  └────┘                                 │
│           (red, bold)                                     │
│                                                            │
└────────────────────────────────────────────────────────────┘
```

## How to Check Your Work

1. **Save `styles.css`**

2. **Open `index.html` in your web browser**

3. **Verify the `.highlight` spans**:
   - Should have a **light yellow background** (#fff3cd)
   - Should have **small padding** creating space around the text
   - Should have **slightly rounded corners**

4. **Verify the `.keyword` spans**:
   - Should have **dark red text** (#c0392b)
   - Should be **bold**

5. **Verify the `.author-name` span**:
   - Should be **italic**
   - Should have **gray text** (#7f8c8d)

6. **Verify inline behavior**:
   - All spans should **stay on the same line** as surrounding text
   - Spans should **not cause line breaks**

## Common Issues

### Issue: The span styles aren't showing up

**Possible cause:** You might have forgotten the `.` before the class name.

**Fix:** Class selectors must start with a period:
```css
/* WRONG - no period */
highlight {
    background-color: yellow;
}

/* RIGHT - with period */
.highlight {
    background-color: yellow;
}
```

### Issue: The highlighted text has no background color

**Possible cause:** You might have misspelled `background-color`.

**Fix:** Make sure you use the hyphen and spell it correctly:
```css
/* WRONG */
backgroundcolor: #fff3cd;
background-color: #fff3cc;  /* wrong hex code */

/* RIGHT */
background-color: #fff3cd;
```

### Issue: The keyword isn't turning red

**Possible cause:** You might have used a named color that doesn't exist or wrong hex.

**Fix:** Use the exact hex code provided:
```css
/* These might not work as expected */
.keyword {
    color: darkred;  /* named color, different shade */
}

/* Use the exact hex code */
.keyword {
    color: #c0392b;  /* exact color we want */
}
```

### Issue: The author name isn't italic

**Possible cause:** You might have used `font-style: oblique;` or misspelled the property.

**Fix:** Use the correct property and value:
```css
/* WRONG */
.author-name {
    font-style: oblique;  /* close but not the same */
    font-syle: italic;    /* typo: missing 't' */
}

/* RIGHT */
.author-name {
    font-style: italic;
}
```

### Issue: The padding isn't showing on highlights

**Possible cause:** You might have forgotten to add padding, or used margin instead.

**Fix:** Remember that padding is space INSIDE the element:
```css
.highlight {
    background-color: #fff3cd;
    padding: 2px 4px;  /* Don't forget this! */
    border-radius: 3px;
}
```

## Time Estimate

~10 minutes
