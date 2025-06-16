# Deployment Guide for Priya Suppliers Website

This guide will help you deploy the Priya Suppliers website to GitHub Pages.

## 📋 Prerequisites

1. A GitHub account
2. Git installed on your computer
3. Node.js and npm installed

## 🚀 Step-by-Step Deployment

### Step 1: Create a GitHub Repository

1. Go to [GitHub](https://github.com) and sign in
2. Click the "+" icon in the top right corner
3. Select "New repository"
4. Name your repository: **`priya`**
5. Make sure it's set to "Public"
6. Don't initialize with README (we already have one)
7. Click "Create repository"

### Step 2: Update Configuration

The configuration is already set for the repository name "priya". Just update your GitHub username in `astro.config.mjs`:

```javascript
export default defineConfig({
  site: 'https://YOUR_GITHUB_USERNAME.github.io',
  base: '/priya',
  output: 'static',
  build: {
    assets: 'assets'
  }
});
```

Replace `YOUR_GITHUB_USERNAME` with your actual GitHub username.

### Step 3: Initialize Git and Push to GitHub

Open terminal/command prompt in your project folder and run:

```bash
# Initialize git repository
git init

# Add all files
git add .

# Make initial commit
git commit -m "Initial commit: Priya Suppliers website"

# Add GitHub repository as remote origin
git remote add origin https://github.com/YOUR_USERNAME/priya.git

# Push to GitHub
git push -u origin main
```

### Step 4: Enable GitHub Pages

1. Go to your repository on GitHub: `https://github.com/YOUR_USERNAME/priya`
2. Click on "Settings" tab
3. Scroll down to "Pages" in the left sidebar
4. Under "Source", select "GitHub Actions"
5. The GitHub Actions workflow will automatically deploy your site

### Step 5: Wait for Deployment

1. Go to the "Actions" tab in your repository
2. You'll see a workflow running called "Deploy to GitHub Pages"
3. Wait for it to complete (usually takes 2-3 minutes)
4. Once complete, your site will be available at:
   **`https://YOUR_USERNAME.github.io/priya`**

## 🔧 Making Updates

To update your website:

1. Make changes to your files
2. Commit and push changes:
```bash
git add .
git commit -m "Update website content"
git push
```
3. GitHub Actions will automatically redeploy your site

## 🌐 Custom Domain (Optional)

To use a custom domain:

1. Add a `CNAME` file to the `public/` folder with your domain name
2. Configure your domain's DNS settings to point to GitHub Pages
3. In repository settings > Pages, add your custom domain

## 📱 Testing Your Deployment

After deployment, test your website:

1. Visit your GitHub Pages URL: `https://YOUR_USERNAME.github.io/priya`
2. Check all pages load correctly
3. Test navigation menu
4. Verify contact form (note: form submission won't work without backend)
5. Test on mobile devices

## 🐛 Troubleshooting

### Common Issues:

1. **404 Error**: The base path is already set to `/priya` - ensure your repository name matches exactly
2. **CSS/Images not loading**: Make sure you've updated your GitHub username in the config
3. **Build fails**: Check the Actions tab for error details

### Getting Help:

- Check the [Astro documentation](https://docs.astro.build/en/guides/deploy/github/)
- Review GitHub Actions logs for specific errors
- Ensure all file paths are correct and case-sensitive

## 📊 Performance Tips

- Images are optimized and served from Pexels CDN
- Static site generation ensures fast loading
- Minimal JavaScript for optimal performance
- Responsive design works on all devices

## 🔒 Security Notes

- No sensitive data is exposed in the repository
- Contact form is client-side only (consider adding backend for production)
- All external links open in new tabs for security

---

Your Priya Suppliers website is now ready for deployment! 🎉

**Final URL will be**: `https://YOUR_USERNAME.github.io/priya`