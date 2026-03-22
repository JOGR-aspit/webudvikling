# CSS Exercise: Descendant Combinators

## Learning Objectives

By completing this exercise, you will be able to:

- [ ] Write descendant combinators using the space character
- [ ] Target elements only when they're inside specific containers
- [ ] Combine class selectors with element selectors
- [ ] Understand how CSS scope works with nesting

## Prerequisites

Before starting this exercise, you should have:

- Completed the "CSS Selectors" lesson (08-css-selectors.md)
- Completed the "ID Selectors & Chaining" (Medium) exercise
- Understand element, class, and ID selectors

## What You'll Build

You will style a webpage with a navigation menu, a blog post, and a sidebar. The key concept is **descendant combinators** - targeting elements based on what they're inside.

**What is a descendant combinator?**
- Uses a **space** between selectors
- Targets elements that are INSIDE (nested in) another element
- Example: `nav a` targets links inside nav, but NOT links outside nav

## Tasks

1. **Open `styles.css`** - This file is empty. You'll write everything from scratch.

2. **Style ALL links inside `.main-nav`**
   - Selector: `.main-nav a` (space between class and element)
   - Declarations: `color: white;`, `text-decoration: none;`

3. **Style links inside `.dropdown` only**
   - Selector: `.dropdown a` (space between class and element)
   - Declarations: `color: lightblue;`

4. **Style paragraphs inside `.blog-post`**
   - Selector: `.blog-post p` (space between class and element)
   - Declarations: `color: #333333;`, `line-height: 1.6;`

5. **Style the h2 inside `.blog-post`**
   - Selector: `.blog-post h2` (space between class and element)
   - Declarations: `color: #2c3e50;`

6. **Style paragraphs inside `.post-footer`**
   - Selector: `.post-footer p` (space between class and element)
   - Declarations: `color: #666666;`, `font-size: 14px;`

7. **Style paragraphs inside `.sidebar`**
   - Selector: `.sidebar p` (space between class and element)
   - Declarations: `color: #555555;`, `font-style: italic;`

## Descendant Combinator Syntax

```
parent descendant {
    property: value;
}
```

| Pattern | Meaning | Example |
|---------|---------|---------|
| `.class element` | Element inside class | `.blog-post p` = paragraphs inside blog-post |
| `element element` | Element inside element | `article p` = paragraphs inside article |
| `#id element` | Element inside ID | `#footer p` = paragraphs inside footer |

**Key point**: The SPACE between selectors means "inside" or "nested in"

## Expected Result

When you complete this exercise, your page will look like this:

```
┌─────────────────────────────────────┐
│ HOME  ABOUT  SERVICES  CONTACT    │  ← Navigation links: white, no underline
│        (dropdown links: lightblue) │
└─────────────────────────────────────┘

ARTICLE TITLE                        ← h2: dark blue (#2c3e50)
─────────────────────────────────────
First paragraph.                     ← p inside blog-post: dark grey (#333333)
Second paragraph.                    ←    with good line spacing (1.6)

Posted on March 22, 2026          ← p inside post-footer: medium grey (#666666)
                                      smaller text (14px)
┌─────────────────────────────────────┐
│ SIDEBAR                            │
│ Sidebar text.                      │  ← p inside sidebar: grey (#555555)
│ (italic)                           │     italic style
└─────────────────────────────────────┘
```

## How to Check Your Work

1. **Save both files** (`index.html` and `styles.css`)

2. **Open `index.html` in your web browser**

3. **Verify navigation links**:
   - "Home" and "About" should be **white** with **no underline**
   - "Services" and "Contact" (in dropdown) should be **light blue**

4. **Verify blog post**:
   - Title should be **dark blue** (#2c3e50)
   - Content paragraphs should be **dark grey** (#333333)
   - Footer text should be **medium grey** (#666666) and **smaller** (14px)

5. **Verify sidebar**:
   - Sidebar text should be **grey** (#555555) and **italic**

## Common Issues

### Issue: The descendant combinator isn't working

**Possible cause:** You forgot the put a space between selectors, or you used the comma instead.

**Fix:** Use a SPACE (not comma, not no-space):
```css
/* WRONG - comma means "OR" (both selectors get styled) */
.main-nav, a { }

/* WRONG - no space means chaining (element must have both) */
.main-nava { }

/* RIGHT - space means "inside" (a inside .main-nav) */
.main-nav a { }
```

### Issue: All paragraphs are styled, not just the ones inside .blog-post

 **Possible cause:** You wrote `p` by itself instead of `.blog-post p`.

**Fix:** Be specific with descendants:
```css
/* WRONG - styles ALL paragraphs */
p { color: #333; }

/* RIGHT - only styles paragraphs inside .blog-post */
.blog-post p { color: #333; }
```

### Issue: The dropdown links aren't light blue

**Possible cause:** You styled `.main-nav a` which also targets nested links.

**Fix:** The dropdown is INSIDE main-nav, so `.dropdown a` is more specific:
```css
/* This styles ALL links in nav, including dropdown */
.main-nav a { color: white; }

/* This is MORE SPECIFIC for dropdown links */
.dropdown a { color: lightblue; }
```

CSS specificity means the more specific selector wins!

### Issue: I'm confused about when to use space vs no space

**Rule of thumb**:
- **SPACE** = "inside" (descendant combinator)
  - `.nav a` = links INSIDE nav
  - `.sidebar p` = paragraphs INSIDE sidebar

- **NO SPACE** = "AND" (chaining)
  - `.btn.large` = elements with BOTH classes
  - `.card.featured` = elements with BOTH classes

## Time Estimate

~30 minutes
