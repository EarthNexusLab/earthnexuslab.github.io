# Earth Nexus Lab Website: Beginner's Guide

This guide is designed for team members who aren't familiar with Hugo, Markdown, Git, or GitHub but need to update and manage the Earth Nexus Lab website.

## Table of Contents

1. [Getting Started](#getting-started)
2. [Understanding the Website Structure](#understanding-the-website-structure)
3. [Editing Content with Markdown](#editing-content-with-markdown)
4. [Adding New Pages](#adding-new-pages)
5. [Adding Images](#adding-images)
6. [Working with Git and GitHub](#working-with-git-and-github)
7. [Previewing and Deploying Changes](#previewing-and-deploying-changes)
8. [Troubleshooting](#troubleshooting)

---

## Getting Started

### What You'll Need

- A GitHub account
- Git installed on your computer
- A code editor (we recommend [Visual Studio Code](https://code.visualstudio.com/))
- [Node.js](https://nodejs.org/) (version 14 or higher)
- [Hugo Extended](https://gohugo.io/installation/) (version 0.147.3)

### Initial Setup

1. **Create a GitHub account**:
   - Go to [github.com](https://github.com/) and sign up for an account if you don't have one

2. **Install Git**:
   - Download and install from [git-scm.com](https://git-scm.com/)
   - Windows users should also install [Git Bash](https://gitforwindows.org/)

3. **Install Visual Studio Code**:
   - Download and install from [code.visualstudio.com](https://code.visualstudio.com/)

4. **Install Node.js**:
   - Download and install from [nodejs.org](https://nodejs.org/)

5. **Install Hugo**:
   - Follow the instructions at [gohugo.io/installation](https://gohugo.io/installation/)
   - Make sure to install the "extended" version

6. **Clone the repository**:
   - Open Terminal (Mac) or Git Bash (Windows)
   - Run: `git clone https://github.com/EarthNexusLab/earthnexuslab.github.io.git`
   - Change into the directory: `cd earthnexuslab.github.io`

7. **Install dependencies**:
   - Run: `npm install`

8. **Start the local development server**:
   - Run: `npm run dev`
   - Open your browser and go to `http://localhost:1313`

---

## Understanding the Website Structure

The Earth Nexus Lab website is built with Hugo, a static site generator. Here's how the files are organized:

```
earthnexuslab.github.io/
├── content/               # Main content files (what you'll edit most)
│   └── english/          # English language content
│       ├── about/        # About page content
│       ├── blog/         # Blog posts
│       ├── contact/      # Contact page
│       ├── events/       # Events page
│       ├── news/         # News page
│       ├── people/       # People/team page
│       ├── research/     # Research page
│       └── _index.md     # Homepage content
├── static/               # Static files like images
│   └── images/           # Image files
├── assets/               # CSS and JavaScript files
├── config/               # Configuration files
├── themes/               # Theme files (don't modify these)
└── public/               # Generated site (don't modify these)
```

The most important folders for content editors are:

- `content/english/` - This is where all the content pages live
- `static/images/` - This is where you should put images

---

## Editing Content with Markdown

Most content in Hugo is written in Markdown, a simple formatting language.

### Basic Markdown Syntax

```markdown
# This is a heading level 1
## This is a heading level 2
### This is a heading level 3

This is a paragraph of text.

**This text is bold**
*This text is italic*

[This is a link](https://example.com)

- This is a bullet point
- Another bullet point
  - A nested bullet point

1. This is a numbered list
2. Second item
3. Third item

![Image description](path-to-image.jpg)
```

### Editing an Existing Page

1. Navigate to the page you want to edit in the `content/english/` directory
2. Open the file (ending in `.md`) in your code editor
3. Edit the content using Markdown syntax
4. Save the file
5. The local server will automatically refresh with your changes

### Understanding Hugo Front Matter

Each Markdown file begins with "front matter" - metadata about the page enclosed in `---` at the top:

```yaml
---
title: "About Us"
date: 2023-01-01
draft: false
---
```

Common front matter fields:
- `title`: The page title
- `date`: Publication date
- `draft`: If true, the page won't be published
- `description`: SEO description
- `image`: Featured image path

---

## Adding New Pages

To create a new page (like a new blog post or team member):

1. Find the appropriate section folder (e.g., `content/english/blog/` for a blog post)
2. Create a new file with a `.md` extension (e.g., `new-research-project.md`)
3. Add front matter at the top of the file:

```yaml
---
title: "Title of Your New Page"
date: 2023-06-15
draft: false
description: "A brief description for SEO"
---
```

4. Add your content below the front matter using Markdown
5. Save the file and check the local preview

### Creating a New Section

If you need a completely new section:

1. Create a new folder in `content/english/` (e.g., `publications/`)
2. Create an `_index.md` file in that folder:

```yaml
---
title: "Publications"
description: "Our research publications"
draft: false
---

Content for the main publications page goes here.
```

---

## Adding Images

To add images to your content:

1. Place your image file in `static/images/` (you can create subfolders for organization)
2. Reference the image in your Markdown content:

```markdown
![Description of image](/images/your-image.jpg)
```

Note: The path starts with `/images/` (not `/static/images/`).

### Image Best Practices

- Use descriptive filenames (e.g., `research-team-meeting.jpg` not `IMG1234.jpg`)
- Optimize images for web before uploading (aim for file sizes under 500KB)
- Use JPG for photos and PNG for graphics with transparency
- Include descriptive alt text for accessibility
- Keep images at reasonable dimensions (max width 1200px recommended)

---

## Working with Git and GitHub

Git is a version control system that tracks changes to files. GitHub is where we store our code online.

### Basic Git Workflow

1. **Pull the latest changes** before starting work:
   ```bash
   git pull origin main
   ```

2. **Make your changes** to the content files

3. **Check the status** of your changes:
   ```bash
   git status
   ```

4. **Stage your changes**:
   ```bash
   git add .
   ```

5. **Commit your changes** with a descriptive message:
   ```bash
   git commit -m "Updated the About page with new mission statement"
   ```

6. **Push your changes** to GitHub:
   ```bash
   git pull origin main   # Pull any new changes first to avoid conflicts
   git push origin main
   ```

### Common Git Commands

- `git status`: Check which files have been changed
- `git add filename`: Stage a specific file for commit
- `git add .`: Stage all changed files
- `git commit -m "message"`: Commit staged changes with a descriptive message
- `git pull origin main`: Get the latest changes from GitHub
- `git push origin main`: Send your commits to GitHub

---

## Previewing and Deploying Changes

### Local Preview

While making changes, you can preview them locally:

1. Start the development server if it's not running:
   ```bash
   npm run dev
   ```

2. Open your browser to `http://localhost:1313`
3. Changes you make to files will automatically appear in the browser

### Deployment

The website is automatically deployed when changes are pushed to the `main` branch on GitHub:

1. After you've committed and pushed your changes to GitHub, the GitHub Actions workflow will start automatically
2. The workflow will build the site and deploy it to GitHub Pages
3. You can monitor the deployment status in the "Actions" tab of the GitHub repository
4. Once the deployment is complete, your changes will be live at [https://earthnexuslab.github.io/](https://earthnexuslab.github.io/)

---

## Troubleshooting

### Common Issues and Solutions

**Problem**: Local server won't start
- Make sure you've installed all dependencies with `npm install`
- Ensure Hugo is installed correctly with `hugo version`
- Check for error messages in the terminal

**Problem**: Changes not showing up locally
- Check if the development server is running
- Make sure you've saved the file
- Try refreshing the browser or clearing the cache

**Problem**: Git says there are conflicts
- Pull the latest changes before pushing: `git pull origin main`
- Resolve any conflicts by editing the affected files
- Stage, commit, and push again

**Problem**: Deployment failed
- Check the GitHub Actions log for error messages
- Verify that your Markdown syntax is correct
- Ensure all referenced files (like images) exist

### Getting Help

If you're stuck, you can:

1. Check the [Hugo documentation](https://gohugo.io/documentation/)
2. Look up Markdown syntax at [Markdown Guide](https://www.markdownguide.org/)
3. Search for Git help at [GitHub Docs](https://docs.github.com/en)
4. Contact the website administrator for assistance

---

Remember that it's normal to make mistakes when learning new tools. Git keeps a history of all changes, so it's always possible to revert to a previous version if needed. 