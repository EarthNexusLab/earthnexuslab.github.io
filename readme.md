# Earth Nexus Lab Website Deployment

This repository contains the Earth Nexus Lab website built with Hugo. It is automatically deployed to GitHub Pages using GitHub Actions.

## Deployment Setup

The website is automatically deployed whenever changes are pushed to the `main` branch. The deployment process uses GitHub Actions and is configured in the `.github/workflows/hugo.yml` file.

### How It Works

1. When changes are pushed to the `main` branch, the GitHub Actions workflow is triggered.
2. The workflow:
   - Sets up Hugo and Node.js environments
   - Installs dependencies
   - Builds the Hugo site
   - Deploys the built site to GitHub Pages

### View the Deployed Site

The deployed website is available at: [https://earthnexuslab.github.io/](https://earthnexuslab.github.io/)

## Development Workflow

### Local Development

To work on the site locally:

1. Clone the repository:
   ```bash
   git clone https://github.com/EarthNexusLab/earthnexuslab.github.io.git
   cd earthnexuslab.github.io
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm run dev
   ```

4. View the site at `http://localhost:1313`

### Making Changes

1. Make your changes to the site files
2. Test the changes locally using the development server
3. Commit and push your changes to the `main` branch
4. GitHub Actions will automatically deploy the updated site

## GitHub Pages Setup

To ensure GitHub Pages is correctly configured:

1. Go to the repository settings on GitHub
2. Navigate to the "Pages" section
3. Ensure the "Source" is set to "GitHub Actions"

## Troubleshooting

If you encounter issues with the deployment:

1. Check the GitHub Actions logs for any error messages
2. Verify that the Hugo version in the workflow file matches the version you're using locally
3. Ensure all dependencies are correctly installed 