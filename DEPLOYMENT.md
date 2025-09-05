# DevDelta Tech - GitHub Pages Deployment Guide

This guide will help you deploy the DevDelta Tech website to GitHub Pages.

## 🚀 Quick Deployment Steps

### Method 1: Using GitHub Web Interface (Recommended)

1. **Create a GitHub Repository**
   - Go to [GitHub](https://github.com) and sign in
   - Click "New repository" (green button)
   - Repository name: `devdeltatech` (or your preferred name)
   - Make sure it's **Public** (required for free GitHub Pages)
   - Don't initialize with README (we already have one)
   - Click "Create repository"

2. **Upload Your Files**
   - On the new repository page, click "uploading an existing file"
   - Drag and drop ALL files and folders from your project directory
   - Or use "choose your files" to select all files
   - Write a commit message: "Initial commit: DevDelta Tech website"
   - Click "Commit changes"

3. **Enable GitHub Pages**
   - Go to your repository Settings tab
   - Scroll down to "Pages" section (left sidebar)
   - Under "Source", select "Deploy from a branch"
   - Choose "main" branch and "/ (root)" folder
   - Click "Save"

4. **Access Your Website**
   - Your site will be available at: `https://yourusername.github.io/repositoryname`
   - It may take 5-10 minutes for the first deployment
   - GitHub will show you the URL in the Pages settings

### Method 2: Using Git Commands

```bash
# Navigate to your project directory
cd /path/to/devdeltatech

# Initialize git repository
git init

# Add all files
git add .

# Commit files
git commit -m "Initial commit: DevDelta Tech website"

# Add remote repository (replace with your GitHub repo URL)
git remote add origin https://github.com/yourusername/devdeltatech.git

# Push to GitHub
git push -u origin main
```

Then follow steps 3-4 from Method 1 to enable GitHub Pages.

## 🔧 Automatic Deployment

The website includes a GitHub Actions workflow (`.github/workflows/deploy.yml`) that will automatically deploy your site whenever you push changes to the main branch.

**To enable automatic deployment:**
1. After uploading your files, go to repository Settings
2. Go to Pages section
3. Under "Source", select "GitHub Actions"
4. The workflow will automatically deploy your site

## ✅ Verification Checklist

After deployment, verify these items work correctly:

- [ ] Homepage loads properly
- [ ] Navigation between all pages works
- [ ] All images display correctly
- [ ] Contact form shows success message when submitted
- [ ] Mobile navigation works on small screens
- [ ] All footer links work
- [ ] Service section anchor links work (e.g., services.html#web)

## 🌐 Custom Domain (Optional)

To use a custom domain like `devdeltatech.com`:

1. **Purchase a domain** from a domain registrar
2. **Add CNAME file** to your repository root:
   ```
   devdeltatech.com
   ```
3. **Configure DNS** at your domain registrar:
   - Add CNAME record: `www` → `yourusername.github.io`
   - Add A records for apex domain:
     ```
     185.199.108.153
     185.199.109.153
     185.199.110.153
     185.199.111.153
     ```
4. **Update GitHub Pages settings** with your custom domain

## 📱 Testing Your Deployment

1. **Open your GitHub Pages URL**
2. **Test all navigation links**
3. **Try the contact form**
4. **Test on mobile devices**
5. **Check browser console for errors**

## 🔄 Making Updates

To update your website:

1. **Edit files locally**
2. **Test changes** using `python3 -m http.server 8000`
3. **Upload changes** to GitHub (or use git push)
4. **Wait for automatic deployment** (if using GitHub Actions)

## 📞 Support

If you encounter any issues during deployment:

- Check GitHub Pages documentation: https://docs.github.com/en/pages
- Verify all files are uploaded correctly
- Check repository settings for Pages configuration
- Contact DevDelta Tech: info@devdeltatech.site

## 🎉 Success!

Once deployed, your DevDelta Tech website will be live and accessible worldwide. Share your GitHub Pages URL with clients and showcase your professional online presence!

**Example URLs:**
- `https://yourusername.github.io/devdeltatech`
- `https://devdeltatech.com` (with custom domain)

---

**DevDelta Tech** - Building innovative software solutions from Dhaka, Bangladesh 🇧🇩
