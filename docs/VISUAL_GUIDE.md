# Visual Guide to Updating the Earth Nexus Lab Website

This guide provides visual instructions for making content updates to the Earth Nexus Lab website through GitHub's web interface.

> Note: Screenshots will need to be added to this document. The placeholders below describe what each screenshot should show.

## Accessing the Repository

1. Go to [https://github.com/EarthNexusLab/earthnexuslab.github.io](https://github.com/EarthNexusLab/earthnexuslab.github.io)

2. Sign in to GitHub if you aren't already logged in

   *[Screenshot: GitHub login page]*

3. You'll see the main repository page:

   *[Screenshot: Main repository page with folders and files listed]*

## Finding a File to Edit

1. Navigate to the content you want to edit. Most content is in the `content/english/` folder.

   *[Screenshot: Repository with content folder highlighted]*

2. Click on the `content` folder, then the `english` folder:

   *[Screenshot: Inside the content/english folder showing various content sections]*

3. Choose the section you want to edit (e.g., `about`, `people`, `research`, etc.):

   *[Screenshot: Clicking on a section folder, such as "about"]*

4. Find the file you want to edit. Many sections have an `_index.md` file that contains the main content:

   *[Screenshot: Inside a section folder with the _index.md file highlighted]*

5. Click on the file to view its contents:

   *[Screenshot: Content of a markdown file displayed in GitHub]*

## Editing a File

1. Click the pencil icon (✏️) in the top right corner of the file view to enter edit mode:

   *[Screenshot: File view with edit button highlighted]*

2. You'll now be in the editor where you can make changes:

   *[Screenshot: GitHub's text editor interface with markdown content]*

3. Make your edits. Remember that content uses Markdown formatting:

   *[Screenshot: Example of editing text in the editor]*

## Committing Your Changes

1. After making your changes, scroll down to the "Commit changes" section:

   *[Screenshot: Commit changes section at the bottom of the editor]*

2. Enter a brief description of your changes in the first field (e.g., "Update about page content")

3. You can add a more detailed description in the larger field if necessary, but this is optional

4. Make sure "Commit directly to the main branch" is selected

5. Click the "Commit changes" button

   *[Screenshot: Filled out commit form with commit button highlighted]*

## Monitoring Deployment

1. After committing, GitHub will automatically start deploying your changes. To check the progress, click on the "Actions" tab at the top of the repository:

   *[Screenshot: Repository navigation with Actions tab highlighted]*

2. You'll see the workflow running:

   *[Screenshot: Actions page showing a workflow in progress]*

3. Once the workflow completes successfully (with a green checkmark), your changes are live:

   *[Screenshot: Actions page with completed workflow]*

4. Visit [https://earthnexuslab.github.io/](https://earthnexuslab.github.io/) to see your changes on the live site

## Adding an Image

1. To add a new image, go to the repository main page and navigate to the `static/images/` folder:

   *[Screenshot: Repository with static/images folder path highlighted]*

2. Click the "Add file" button in the top right and select "Upload files":

   *[Screenshot: Add file dropdown menu with Upload files option highlighted]*

3. Either drag and drop files or click to select files from your computer:

   *[Screenshot: Upload files interface]*

4. After selecting your image(s), scroll down to the commit section:

5. Add a commit message (e.g., "Add team photo") and click "Commit changes":

   *[Screenshot: Commit changes section for uploaded files]*

6. Now you can reference this image in your markdown content using:
   ```markdown
   ![Description of image](/images/your-image.jpg)
   ```

## Common Mistakes to Avoid

1. **Don't delete or modify the three dashes and front matter at the top of files:**

   *[Screenshot: Example of front matter that shouldn't be modified]*

2. **Check your Markdown syntax before committing:**

   *[Screenshot: Example of correct vs. incorrect Markdown syntax]*

3. **Be careful with image paths:**

   *[Screenshot: Example of correct image path in Markdown]*

## Getting Help

If you encounter problems or have questions, refer to the [Comprehensive Beginner's Guide](BEGINNER_GUIDE.md) or contact the website administrator for assistance. 