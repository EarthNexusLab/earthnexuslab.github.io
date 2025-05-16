# Earth Nexus Lab Website: Quick-Start Guide

Need to make a simple update to the website without learning all the technical details? This guide is for you!

> **New to GitHub?** Check out our [Visual Guide](VISUAL_GUIDE.md) with step-by-step screenshots.

## The Super Easy Way: Using GitHub Directly

You can edit content directly on GitHub without installing anything on your computer:

1. Go to [https://github.com/EarthNexusLab/earthnexuslab.github.io](https://github.com/EarthNexusLab/earthnexuslab.github.io)
2. Sign in to your GitHub account (or create one if needed)
3. Navigate to the file you want to edit (most content is in the `content/english/` folder)
4. Click the pencil icon (✏️) in the top right of the file view to edit
5. Make your changes
6. Scroll down to the "Commit changes" section
7. Add a brief message describing your changes
8. Click "Commit changes"
9. Wait about 1-3 minutes for the site to automatically rebuild and deploy

## Common Content Files

Here are the paths to common files you might want to edit:

- **Home Page**: `content/english/_index.md`
- **About Page**: `content/english/about/_index.md`
- **Team/People**: `content/english/people/_index.md`
- **Research**: `content/english/research/_index.md`
- **News**: `content/english/news/_index.md`
- **Events**: `content/english/events/_index.md`
- **Contact**: `content/english/contact/_index.md`

## Basic Markdown Formatting

Content is written in Markdown, which is very simple to use:

```markdown
# Large Heading
## Medium Heading
### Small Heading

Regular paragraph text goes here.

**Bold text** and *italic text*

[Link text](https://example.com)

- Bullet point
- Another bullet point

1. Numbered item
2. Second numbered item

![Image description](/images/filename.jpg)
```

## Adding Images

To add a new image:

1. Go to `static/images/` folder
2. Click "Add file" → "Upload files"
3. Select your image(s) and upload
4. Commit the changes
5. Reference the image in your content as `![Description](/images/your-image.jpg)`

## Help! I Made a Mistake

If something goes wrong:

1. Don't panic! All changes are saved in the version history
2. Contact the website administrator for help
3. If you need to make more complex changes, refer to the full [BEGINNER_GUIDE.md](BEGINNER_GUIDE.md)

## When Will My Changes Appear?

After committing your changes, the website will automatically rebuild and deploy. This typically takes 1-3 minutes. You can check the status in the "Actions" tab of the GitHub repository. 