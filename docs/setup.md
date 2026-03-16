# Repository Setup Guide

This guide will help you get started with the ASPIT Teaching Materials Repository.

## Table of Contents

1. [Prerequisites](#prerequisites)
2. [Cloning the Repository](#cloning-the-repository)
3. [Setting Up Your Development Environment](#setting-up-your-development-environment)
4. [Navigating the Repository](#navigating-the-repository)
5. [Getting Started with Your Course](#getting-started-with-your-course)
6. [Troubleshooting](#troubleshooting)

---

## Prerequisites

Before you begin, ensure you have the following:

### Required Software

- **A web browser**: Chrome, Firefox, Safari, or Edge
- **A code editor**: Visual Studio Code (recommended), Sublime Text, or similar
- **Git**: For version control (if contributing)

### For Specific Courses

- **W1 (HTML/CSS)**: No additional software required
- **W2 (JavaScript)**: Browser with JavaScript enabled (all modern browsers)
- **W3.1 (Full Stack)**: XAMPP, MAMP, or similar local server environment
- **W3.2 (WordPress)**: Local WordPress installation (Local by Flywheel, XAMPP with WordPress, etc.)

### Optional Tools

- **Git**: For version control
- **Node.js**: For additional development tools (not required for courses)
- **Postman**: For testing APIs (useful for W3.1)

---

## Cloning the Repository

### Using Git (Recommended)

If you have Git installed:

```bash
git clone <repository-url>
cd aspit
```

### Downloading as ZIP

1. Download the repository as a ZIP file
2. Extract the ZIP file to your desired location
3. Navigate to the extracted folder

---

## Setting Up Your Development Environment

### For All Courses

1. **Open the repository** in your code editor
2. **Familiarize yourself** with the folder structure
3. **Read the main README.md** for an overview

### For W1 (HTML & CSS)

**No special setup required!**

1. Create HTML files in the `W1/` folder
2. Open them directly in your browser
3. That's it!

**Tip**: Use the browser developer tools (press F12) to inspect elements and debug CSS.

### For W2 (JavaScript)

**No special setup required!**

1. Create HTML files with JavaScript in the `W2/` folder
2. Open them in your browser
3. Use the browser console (press F12, then click "Console") to see JavaScript output

**Tip**: The browser console is your best friend for debugging JavaScript. Use `console.log()` extensively.

### For W3.1 (Full Stack)

You'll need a local server environment. Here are popular options:

#### Option 1: XAMPP (Cross-platform)

1. Download XAMPP from [apachefriends.org](https://www.apachefriends.org/)
2. Install XAMPP
3. Start Apache and MySQL services
4. Place your PHP files in the `htdocs` folder (or create a symbolic link)
5. Access your files at `http://localhost/your-folder/`

#### Option 2: MAMP (Mac/Windows)

1. Download MAMP from [mamp.info](https://www.mamp.info/)
2. Install MAMP
3. Start the servers
4. Place your files in the MAMP document root
5. Access your files at `http://localhost:8888/your-folder/`

#### Setting Up the Database

1. Open phpMyAdmin (usually at `http://localhost/phpmyadmin`)
2. Create a new database
3. Import the SQL file from your project (if provided)
4. Update your database connection code with the correct credentials

### For W3.2 (WordPress)

You'll need a local WordPress installation.

#### Option 1: Local by FlyWheel (Easiest)

1. Download Local from [localwp.com](https://localwp.com/)
2. Install Local
3. Create a new WordPress site
4. Access the site in your browser
5. Access files through the "Open site shell" or find the folder in Local's settings

#### Option 2: XAMPP/MAMP with WordPress

1. Set up XAMPP/MAMP as described for W3.1
2. Download WordPress from [wordpress.org](https://wordpress.org/download/)
3. Extract WordPress to your server's document root
4. Create a database in phpMyAdmin
5. Access `http://localhost/wordpress-folder/` and follow the installation wizard

---

## Navigating the Repository

### Folder Structure Overview

```
aspit/
├── W1/                     # Course 1: HTML & CSS
├── W2/                     # Course 2: HTML, CSS & JavaScript
├── W3.1/                   # Course 3.1: Full Stack
├── W3.2/                   # Course 3.2: WordPress
├── resources/              # Shared resources
├── docs/                   # Documentation
├── CLAUDE.md              # Content creation guidelines
└── README.md              # Repository overview
```

### Within Each Course

Each course folder contains:

- `curriculum/` - Learning materials and lessons
- `assignments/` - Practice exercises
  - `solutions/` - Assignment solutions (for reference)
- `projects/` - Larger practical projects
- `code-examples/` - Well-commented code examples
- `README.md` - Course overview and guide

---

## Getting Started with Your Course

### For Students

1. **Identify your course level** (W1, W2, W3.1, or W3.2)
2. **Read the course README** for an overview of what you'll learn
3. **Check prerequisites** - ensure you've completed previous courses
4. **Set up your environment** - follow the instructions above
5. **Start with curriculum** - begin with the materials in `curriculum/`
6. **Practice with assignments** - complete exercises to reinforce learning
7. **Build projects** - apply your skills to create complete applications

### For Instructors

1. **Review the course README** - understand the scope and objectives
2. **Explore the curriculum** - familiarize yourself with the materials
3. **Check code examples** - review the well-commented examples
4. **Adapt as needed** - modify materials to fit your teaching style
5. **Use shared resources** - leverage diagrams, checklists, and references
6. **Contribute improvements** - share your enhancements with the community

---

## Troubleshooting

### Common Issues

#### HTML/CSS Files Won't Open

**Problem**: Double-clicking HTML files doesn't open them in a browser.

**Solution**:
- Right-click the file
- Choose "Open with" → "Chrome" (or your preferred browser)

#### JavaScript Not Working

**Problem**: JavaScript code doesn't execute.

**Solution**:
1. Open the browser developer tools (F12)
2. Check the Console tab for errors
3. Look for red error messages
4. Common errors include:
   - Typos in variable or function names
   - Missing semicolons or brackets
   - Trying to use variables before they're defined

#### Server Won't Start (XAMPP/MAMP)

**Problem**: Apache or MySQL won't start.

**Solution**:
1. Check if another program is using port 80 or 3306
2. Stop Skype or other programs that might conflict
3. Try changing the port in XAMPP/MAMP settings
4. Restart the XAMPP/MAMP control panel

#### Database Connection Errors

**Problem**: Can't connect to the database.

**Solution**:
1. Verify MySQL is running in XAMPP/MAMP
2. Check your database connection code (username, password, database name)
3. Make sure the database exists in phpMyAdmin
4. Verify your credentials are correct

#### WordPress Installation Issues

**Problem**: WordPress won't install or won't load.

**Solution**:
1. Check that your server is running (Apache and MySQL)
2. Verify the database exists and credentials are correct
3. Check file permissions if on Linux/Mac
4. Clear your browser cache
5. Try reinstalling WordPress

### Getting Help

If you're still having issues:

1. **Check the course README** - it may have course-specific help
2. **Review the troubleshooting sections** in the curriculum materials
3. **Consult the code examples** - see how similar problems were solved
4. **Ask your instructor** - don't hesitate to reach out
5. **Search online** - many common issues have documented solutions

---

## Next Steps

Now that you're set up:

1. **Start learning** - dive into your course materials
2. **Practice regularly** - consistent practice is key to learning
3. **Experiment** - try modifying code examples to see what happens
4. **Build projects** - apply your skills to create something real
5. **Share your work** - get feedback from instructors and peers

---

## Additional Resources

- **Main README**: [README.md](../README.md) - Repository overview
- **Content Guidelines**: [CLAUDE.md](../CLAUDE.md) - For creating materials
- **Contributing**: [contributing.md](contributing.md) - How to contribute
- **Accessibility**: [accessibility.md](accessibility.md) - Neurodiversity-friendly design

---

**Last Updated**: 2026-03-16
