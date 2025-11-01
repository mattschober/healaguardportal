# Deployment Guide - GitHub Pages

Follow these steps to deploy your DR Portal to GitHub Pages and get a live URL.

## Step 1: Create a GitHub Repository

1. Go to [GitHub](https://github.com) and sign in
2. Click the **"+"** icon in the top right → **"New repository"**
3. Name your repository (e.g., `dr-portal`, `disaster-recovery-dashboard`)
4. Choose **Public** (required for free GitHub Pages)
5. Click **"Create repository"**

## Step 2: Upload Your Files

You have two options:

### Option A: Upload via Web Interface (Easiest)

1. On your new repository page, click **"uploading an existing file"**
2. Drag and drop these files:
   - `index.html`
   - `README.md`
   - `.gitignore`
3. Click **"Commit changes"**

### Option B: Use Git Command Line

```bash
# Initialize git in your project folder
cd /path/to/your/files
git init

# Add all files
git add .

# Commit the files
git commit -m "Initial commit: DR Portal"

# Add your GitHub repository as remote
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git

# Push to GitHub
git branch -M main
git push -u origin main
```

## Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **"Settings"** (top menu)
3. Click **"Pages"** in the left sidebar
4. Under **"Source"**, select:
   - Branch: **main**
   - Folder: **/ (root)**
5. Click **"Save"**

## Step 4: Access Your Portal

After a few minutes, your site will be live at:

```
https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/
```

Example: If your username is `johndoe` and repo is `dr-portal`:
```
https://johndoe.github.io/dr-portal/
```

## Updating Your Portal

To make changes:

1. Edit your files locally or on GitHub
2. Commit and push changes
3. GitHub Pages will automatically rebuild (takes 1-2 minutes)

## Custom Domain (Optional)

If you want a custom domain like `dr-portal.yourdomain.com`:

1. In your repository settings → Pages
2. Enter your custom domain
3. Update your DNS settings to point to GitHub Pages
4. Follow GitHub's documentation for detailed DNS configuration

## Troubleshooting

**Site not showing up?**
- Wait 5-10 minutes after enabling Pages
- Check that you selected the correct branch (main)
- Verify the repository is public

**404 Error?**
- Make sure your main HTML file is named `index.html`
- Check the repository name in your URL

**Changes not appearing?**
- Clear your browser cache (Ctrl+Shift+R or Cmd+Shift+R)
- Wait a few minutes for GitHub to rebuild

## Need Help?

Visit [GitHub Pages Documentation](https://docs.github.com/en/pages)
