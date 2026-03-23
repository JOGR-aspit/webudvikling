# CSS Exercise: Div Layout

## Learning Objectives

By completing this exercise, you will be able to:

- [ ] Use `<div>` elements to create layout structure
- [ ] Style block containers with padding, margin, and borders
- [ ] Center a container using auto margins
- [ ] Understand how divs create vertical stacking (block behavior)
- [ ] Use `display: inline-block` for side-by-side elements

## Prerequisites

Before starting this exercise, you should have:

- Completed the "Block vs Inline Elements" lesson (11-block-vs-inline-elements.md)
- Completed the "The Box Model" lesson (10-the-box-model.md)
- Completed the "CSS Fundamentals" lesson (07-css-fundamentals.md)
- Know how to use padding, margin, and border

## What You'll Build

You will create a profile card layout using `<div>` elements. The HTML structure is already written for you - it contains nested divs that create a card with a header, content area, and tags section. Your job is to write CSS that styles these containers to create an attractive layout.

`<div>` is a **block element** - it starts on a new line and takes full width by default. This makes it perfect for creating layout sections and containers.

## Tasks

1. **Open `styles.css`** - This file has the base styles already. You'll add styles for the layout.

2. **Style the `.container` div** - Create a selector for `.container` and add:
   - `max-width: 400px;` (maximum width of 400 pixels)
   - `margin: 40px auto;` (40px top/bottom, auto left/right to center)
   - `padding: 20px;` (space inside the container)
   - `background-color: #f5f5f5;` (light gray background)

3. **Style the `.card` div** - Create a selector for `.card` and add:
   - `background-color: #ffffff;` (white background)
   - `padding: 20px;` (space inside the card)
   - `border: 1px solid #dddddd;` (light gray border)
   - `border-radius: 8px;` (rounded corners)
   - `margin-bottom: 20px;` (space below the card)

4. **Style the `.card-header` div** - Create a selector for `.card-header` and add:
   - `padding-bottom: 15px;` (space below header content)
   - `margin-bottom: 15px;` (space after header section)
   - `border-bottom: 1px solid #eeeeee;` (subtle divider line)

5. **Style the `.card-content` div** - Create a selector for `.card-content` and add:
   - `line-height: 1.6;` (comfortable line spacing)
   - `margin-bottom: 15px;` (space below content)

6. **Style the `.tag` spans** - Create a selector for `.tag` and add:
   - `display: inline-block;` (allows padding while staying inline)
   - `padding: 5px 10px;` (space inside each tag)
   - `margin-right: 8px;` (space between tags)
   - `margin-bottom: 8px;` (space below tags when they wrap)
   - `background-color: #e8f4f8;` (light blue background)
   - `border-radius: 4px;` (slightly rounded corners)
   - `font-size: 0.85rem;` (slightly smaller text)

## Block vs Inline-Block Reminder

```
BLOCK ELEMENTS (like div):
┌─────────────────────────────────────────────────────────┐
│ div - starts on new line, takes full width             │
└─────────────────────────────────────────────────────────┘
┌─────────────────────────────────────────────────────────┐
│ div - another new line, full width                     │
└─────────────────────────────────────────────────────────┘


INLINE-BLOCK (like tags with display: inline-block):
┌─────────┐  ┌─────────┐  ┌─────────┐  ┌─────────┐
│ Tag 1   │  │ Tag 2   │  │ Tag 3   │  │ Tag 4   │
└─────────┘  └─────────┘  └─────────┘  └─────────┘
    ↑            ↑            ↑            ↑
Same line, but accepts padding/width/height
```

| Property | block | inline | inline-block |
|----------|-------|--------|--------------|
| New line | Yes | No | No |
| Full width | Yes | No | No |
| Accepts padding | Yes | Partial | Yes |
| Accepts width | Yes | No | Yes |

## Expected Result

When you complete this exercise, your profile card will look like this:

```
┌────────────────────────────────────────────────────────────┐
│                      (light gray #f5f5f5)                  │
│   ┌────────────────────────────────────────────────────┐   │
│   │                  CARD (white)                       │   │
│   │  ┌──────────────────────────────────────────────┐  │   │
│   │  │ CARD HEADER                                  │  │   │
│   │  │                                              │  │   │
│   │  │  John Smith                                  │  │   │
│   │  │  Web Developer                               │  │   │
│   │  │  (border-bottom creates divider line)        │  │   │
│   │  └──────────────────────────────────────────────┘  │   │
│   │                                                    │   │
│   │  CARD CONTENT                                      │   │
│   │                                                    │   │
│   │  John is a passionate web developer with          │   │
│   │  over 5 years of experience creating beautiful    │   │
│   │  and functional websites.                         │   │
│   │                                                    │   │
│   │  ┌────────┐ ┌────────┐ ┌────────┐ ┌────────┐     │   │
│   │  │ HTML   │ │ CSS    │ │ JS     │ │ React  │     │   │
│   │  └────────┘ └────────┘ └────────┘ └────────┘     │   │
│   │       (inline-block tags with light blue bg)      │   │
│   │                                                    │   │
│   └────────────────────────────────────────────────────┘   │
│                                                            │
└────────────────────────────────────────────────────────────┘
```

## How to Check Your Work

1. **Save `styles.css`**

2. **Open `index.html` in your web browser**

3. **Verify the `.container` div**:
   - Should be **centered on the page**
   - Should have **maximum width of 400px**
   - Should have **light gray background** (#f5f5f5)
   - Should have **40px space above and below**

4. **Verify the `.card` div**:
   - Should have **white background**
   - Should have **rounded corners** (8px radius)
   - Should have **light gray border**
   - Should have **20px padding inside**

5. **Verify the `.card-header` div**:
   - Should have a **divider line at the bottom**
   - Should have **15px space below**

6. **Verify the `.tag` spans**:
   - Should appear **side by side** (inline-block)
   - Should have **light blue background** (#e8f4f8)
   - Should have **rounded corners**
   - Should have **space between them**

## Common Issues

### Issue: The container isn't centered

**Possible cause:** You forgot `auto` in the margin, or didn't set a width/max-width.

**Fix:** Auto margins only work when the element has a defined width:
```css
/* WRONG - no width, auto won't work */
.container {
    margin: 40px auto;
}

/* RIGHT - has max-width, auto works */
.container {
    max-width: 400px;
    margin: 40px auto;
}
```

### Issue: The tags are stacking vertically instead of side by side

**Possible cause:** You forgot `display: inline-block` or used `display: block`.

**Fix:** Tags need to be inline-block to sit side by side:
```css
/* WRONG - block makes them stack */
.tag {
    display: block;
}

/* RIGHT - inline-block keeps them on same line */
.tag {
    display: inline-block;
}
```

### Issue: The card header divider isn't showing

**Possible cause:** You might have used `border` instead of `border-bottom`.

**Fix:** Use `border-bottom` for a divider line:
```css
/* WRONG - border on all sides */
.card-header {
    border: 1px solid #eeeeee;
}

/* RIGHT - only bottom border */
.card-header {
    border-bottom: 1px solid #eeeeee;
}
```

### Issue: The card is touching the container edges

**Possible cause:** You forgot padding on the container or card.

**Fix:** Add padding to create space inside containers:
```css
.container {
    padding: 20px;  /* Space inside container */
}

.card {
    padding: 20px;  /* Space inside card */
}
```

### Issue: The tags are too close together

**Possible cause:** You forgot margin on the tags.

**Fix:** Add margin-right to create space between tags:
```css
.tag {
    margin-right: 8px;   /* Space between tags */
    margin-bottom: 8px;  /* Space when tags wrap to new line */
}
```

## Time Estimate

~20 minutes
