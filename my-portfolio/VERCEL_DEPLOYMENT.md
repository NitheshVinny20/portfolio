# Vercel Deployment Guide

## ✅ Pre-Deployment Checklist

- [x] `package.json` configured with build script
- [x] `vite.config.js` optimized for production
- [x] `dist` directory set as output
- [x] `.gitignore` created
- [x] `vercel.json` configuration added

## 🚀 Steps to Deploy on Vercel

### 1. **Push to Git Repository**
First, ensure your project is in a Git repository:
```bash
git init
git add .
git commit -m "Initial commit - Ready for Vercel deployment"
```

### 2. **Upload to GitHub/GitLab/Bitbucket**
Push your repository to one of these platforms:
```bash
git remote add origin https://github.com/yourusername/my-portfolio.git
git branch -M main
git push -u origin main
```

### 3. **Connect to Vercel**

**Option A: Using Vercel CLI**
```bash
npm i -g vercel
vercel
```

**Option B: Using Vercel Website**
1. Go to [vercel.com](https://vercel.com)
2. Click "New Project"
3. Import your Git repository
4. Select the repository from GitHub/GitLab/Bitbucket
5. Click "Import"

### 4. **Configure Build Settings**
When asked to configure your project, use these settings:

**Build Command:**
```
npm run build
```

**Output Directory:**
```
dist
```

**Install Command:**
```
npm install
```

Or let Vercel auto-detect (it will recognize Vite automatically).

### 5. **Environment Variables (if needed)**
- Go to Settings → Environment Variables
- Add any environment variables your app needs
- Example: `VITE_APP_NAME=My Portfolio`

### 6. **Deploy**
- Click "Deploy"
- Wait for the build to complete
- Your site will be live at `https://your-project.vercel.app`

## 📝 Build & Test Locally Before Deploying

Test the production build locally:
```bash
npm run build
npm run preview
```

This mimics exactly how your site will look on Vercel.

## 🔧 Build Configuration Details

| Setting | Value |
|---------|-------|
| Framework | React + Vite |
| Build Command | `npm run build` |
| Output Directory | `dist` |
| Install Command | `npm install` |
| Node Version | 18.x (default) |

## 📊 What Vercel Does Automatically

1. ✅ Detects React + Vite setup
2. ✅ Runs `npm install`
3. ✅ Runs `npm run build`
4. ✅ Deploys `dist` folder to CDN
5. ✅ Provides free SSL certificate
6. ✅ Enables automatic deployments on git push

## 🎯 Quick Commands Checklist

```bash
# 1. Install dependencies
npm install

# 2. Test locally
npm run dev

# 3. Build production version
npm run build

# 4. Preview production build
npm run preview

# 5. Install Vercel CLI
npm i -g vercel

# 6. Deploy to Vercel
vercel

# 7. Deploy to production
vercel --prod
```

## 🔗 Useful Links

- [Vercel Documentation](https://vercel.com/docs)
- [Vite Documentation](https://vitejs.dev)
- [React Documentation](https://react.dev)

## ❓ Troubleshooting

**Build fails on Vercel but works locally?**
- Run `npm run build` locally and check for errors
- Check Node version compatibility
- Verify all environment variables are set

**Site shows 404?**
- Confirm output directory is `dist`
- Check build logs in Vercel dashboard
- Verify `vite.config.js` configuration

**Slow build time?**
- Clear Vercel cache and rebuild
- Optimize images and dependencies
- Check for unused npm packages

---
**Your portfolio is ready for deployment! 🎉**
