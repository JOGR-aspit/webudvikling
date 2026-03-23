# Project 2: Travel Guide

## What You'll Build

In this project, you'll create a **single-page travel guide** for a destination of your choice. This could be a real city you've visited (or want to visit), a fictional place from your imagination, or even your hometown!

Your travel guide will have:
- Multiple sections with different types of information
- Images to show what the destination looks like
- Lists to organize attractions, tips, and recommendations
- Links to external resources for more information
- Proper HTML structure throughout

---

## Learning Objectives

After completing this project, you will be able to:

- [ ] Create a well-organized single-page website
- [ ] Use semantic HTML elements to structure different types of content
- [ ] Organize information using headings and sections
- [ ] Present items in ordered and unordered lists
- [ ] Add images with descriptive alt text
- [ ] Create links to external websites
- [ ] Write clear, helpful HTML comments

---

## Prerequisites

Before starting this project, you should have completed:

- [ ] Article 02: Basic HTML Structure
- [ ] Article 03: Text in HTML
- [ ] Article 04: Lists in HTML
- [ ] Article 05: Links and Images
- [ ] Article 06: Classes and Semantic HTML

---

## Project Requirements

Your travel guide **must include**:

### Structure Requirements

| Requirement | Minimum | Details |
|-------------|---------|---------|
| Sections | 4 | Introduction + at least 3 content sections |
| Images | 2 | With descriptive alt text |
| Lists | 2 | At least 1 ordered list AND 1 unordered list |
| External Links | 3 | Links to real websites for more information |

### HTML Requirements

- [ ] Proper HTML document structure (DOCTYPE, html, head, body)
- [ ] Title tag with your destination name
- [ ] Semantic HTML elements (`<header>`, `<main>`, `<section>`, `<article>`, `<footer>`)
- [ ] Heading hierarchy (h1 for main title, h2 for sections)
- [ ] Paragraphs for descriptive text
- [ ] At least 1 ordered list (`<ol>`)
- [ ] At least 1 unordered list (`<ul>`)
- [ ] Links to external websites (opening in new tab is optional)
- [ ] Images with `src` and `alt` attributes
- [ ] HTML comments explaining your structure

### File Requirements

- [ ] File is named `index.html`
- [ ] Images are stored in an `images/` folder
- [ ] All file names use **kebab-case** (lowercase with hyphens)

---

## Getting Started

### Step 1: Choose Your Destination

**Before writing any code**, decide what place your travel guide will be about. Consider:

1. **Do you want to write about a real place or a fictional one?**
   - Real places: You can find real images and link to real resources
   - Fictional places: You can be creative with descriptions and details

2. **What do you know well?**
   - A city you've visited
   - Your hometown
   - A place you've researched for fun
   - A place from a book, movie, or game

3. **What information will you include?**
   - Top attractions or landmarks
   - Local food and restaurants
   - Transportation and getting around
   - Best time to visit
   - Cultural tips and customs
   - Hidden gems and local secrets

### Step 2: Plan Your Sections

A good travel guide has organized sections. Here's a suggested structure:

```
1. Introduction (What makes this place special?)
2. Top Attractions (What should visitors see?)
3. Local Food (What should they eat?)
4. Travel Tips (What should they know before going?)
```

You can change these sections to match your destination!

### Step 3: Set Up Your Files

1. Create a new folder for your project (e.g., `my-travel-guide/`)
2. Inside that folder, create:
   - `index.html` (your main page)
   - `images/` folder for your images

### Step 4: Write Your HTML

Use the starter files in `starter-files/` as a template:

1. Open `starter-files/index.html`
2. Save a copy to your project folder
3. Replace the placeholder content with your own
4. Add your images to the `images/` folder
5. Update the image `src` attributes to point to your files

### Step 5: Add Your Content

For each section:

1. **Write descriptive text** using paragraphs
2. **Use `<strong>` for important names** and `<em>` for emphasis
3. **Organize items in lists** - ordered lists for rankings, unordered lists for collections
4. **Add images** that show what you're describing
5. **Include external links** to websites with more information

### Step 6: Test Your Page

1. Open `index.html` in your browser
2. Read through all your content
3. Click every external link to make sure it works
4. Check that all images display correctly
5. Verify your page makes sense and is easy to read

---

## Code Example

Here's an example of how a section should be structured:

```html
<!-- Top Attractions Section -->
<section>
    <h2>Top 5 Attractions</h2>

    <p>These are the <strong>must-see places</strong> when visiting. I've ranked them in order of how much I enjoyed them!</p>

    <!-- Ordered list because these are ranked -->
    <ol>
        <li>
            <strong>The Old Castle</strong> - A 500-year-old castle with amazing views
            (<a href="https://example.com/castle" target="_blank">Official website</a>)
        </li>
        <li>
            <strong>Central Market</strong> - Best place to try local food and buy souvenirs
        </li>
        <li>
            <strong>River Walk</strong> - A peaceful path along the river, perfect for sunset
        </li>
    </ol>

    <!-- Image of the top attraction -->
    <img src="images/old-castle.jpg" alt="The Old Castle standing on a hill at sunset, with stone walls and tall towers. Visitors can be seen walking toward the entrance." width="400">
</section>
```

---

## Section Ideas

Not sure what sections to include? Here are ideas organized by type:

### Essential Sections

- **Introduction** - Overview of the destination, why visit
- **Top Attractions** - Must-see places, ranked or listed
- **Getting There** - How to travel to the destination
- **Best Time to Visit** - Weather, seasons, events

### Food & Culture

- **Local Food** - Traditional dishes and where to try them
- **Restaurants** - Recommended places to eat
- **Cultural Tips** - Customs, etiquette, language basics
- **Festivals & Events** - Annual celebrations and happenings

### Practical Information

- **Transportation** - How to get around locally
- **Accommodation** - Where to stay
- **Budget Tips** - How to save money
- **Safety Tips** - Important precautions

### For Fictional Places

- **History & Lore** - Background story of the place
- **Notable Characters** - Important people who live there
- **Geography** - What the land is like
- **Hidden Secrets** - Things most visitors don't know

---

## Destination Ideas

Need inspiration? Here are some destination ideas:

### Real Cities

- **Paris, France** - The City of Light
- **Tokyo, Japan** - Where tradition meets technology
- **New York City, USA** - The city that never sleeps
- **Rome, Italy** - Ancient history and modern life
- **Barcelona, Spain** - Art, architecture, and beaches

### Fictional Places

- **Hogwarts** - The famous wizarding school
- **The Shire** - Peaceful home of hobbits
- **Atlantis** - The legendary underwater city
- **A futuristic Mars colony** - Life on the red planet
- **A fantasy kingdom** - Of your own design

### Your Hometown

- What makes where you live special?
- What would you show a visitor?
- What hidden gems do locals know about?
- What food is your area known for?

---

## Success Criteria Checklist

Before submitting your project, verify:

### Structure
- [ ] Page has at least 4 sections (intro + 3 content)
- [ ] All sections use semantic HTML elements
- [ ] Page has proper HTML document structure
- [ ] Heading hierarchy is correct (h1 for title, h2 for sections)

### Content
- [ ] Introduction explains what makes the destination special
- [ ] At least 1 ordered list is used (rankings, steps, etc.)
- [ ] At least 1 unordered list is used (collections, options)
- [ ] Text uses `<strong>` for important names
- [ ] Text uses `<em>` for emphasis where appropriate

### Links
- [ ] At least 3 external links are included
- [ ] All links work correctly
- [ ] Links go to relevant, helpful websites

### Images
- [ ] At least 2 images are included
- [ ] All images have descriptive alt text
- [ ] Images are stored in an `images/` folder
- [ ] Images are relevant to the content

### Code Quality
- [ ] HTML comments explain the structure
- [ ] Code is properly indented
- [ ] All images display correctly
- [ ] Page has a descriptive title

---

## Troubleshooting

### My images don't show!

1. **Check the file path** - Images in a folder need `images/filename.jpg`
2. **Check the file name** - Must match exactly (case-sensitive!)
3. **Check the file exists** - Make sure the image file is actually there
4. **Check the file extension** - `.jpg` is different from `.jpeg`

### My links don't work!

1. **Check the URL** - Make sure you copied the full web address
2. **Include https://** - External links need the full URL
3. **Test the link** - Try opening the URL directly in your browser

### My page looks unorganized!

1. **Use sections** - Group related content in `<section>` tags
2. **Use headings** - Each section should have an `<h2>` heading
3. **Use paragraphs** - Don't write long blocks of text without breaks
4. **Use lists** - Lists make information easier to read

### I don't know what to write!

1. **Start with what you know** - Write about a place you're familiar with
2. **Research online** - Look up facts about your destination
3. **Use the example solution** - See how it's organized
4. **Ask for help** - Your instructor can help brainstorm ideas

---

## Need More Help?

- **Review the curriculum** - Articles 02-06 cover all the concepts
- **Check the starter files** - Use the template provided
- **Look at the example solution** - See a complete working travel guide
- **Ask your instructor** - Don't hesitate to ask questions!

---

## What's Next?

After completing this project, you'll be ready to:

1. Learn CSS to style your web pages
2. Add colors, fonts, and layouts to make your guide visually appealing
3. Create more complex single-page websites

**Good luck with your travel guide!**

---

**Estimated Time**: 2-3 hours
**Difficulty**: Beginner
**Focus**: HTML only (no CSS or JavaScript)
