# GitHub Pages Deployment Guide

## 🚀 Quick Start - Make Your Site Live

Follow these steps to deploy your IT Support CRM to GitHub Pages and share it with your customers.

---

## Step 1: Enable GitHub Pages

1. Go to your repository: **https://github.com/MuhibChy/IT-Support-CRM**
2. Click the **Settings** tab (top right)
3. In the left sidebar, scroll down and click **Pages**
4. Under **Source**, select:
   - **GitHub Actions** (NOT "Deploy from a branch")
5. The page will auto-save

✅ GitHub Pages is now enabled!

---

## Step 2: Add Your Gemini API Key (Required)

Your app uses Google's Gemini AI. You need to add your API key as a secret:

### Get Your API Key:
1. Visit: **https://aistudio.google.com/app/apikey**
2. Sign in with your Google account
3. Click **"Create API Key"**
4. Copy the generated key

### Add to GitHub:
1. In your repository, go to **Settings** > **Secrets and variables** > **Actions**
2. Click **"New repository secret"**
3. Enter:
   - **Name:** `GEMINI_API_KEY`
   - **Secret:** Paste your API key
4. Click **"Add secret"**

✅ API key configured!

---

## Step 3: Deploy Your Site

You have two options:

### Option A: Push to Main Branch (Automatic)
```bash
git add .
git commit -m "Deploy to GitHub Pages"
git push origin main
```

### Option B: Manual Trigger
1. Go to the **Actions** tab in your repository
2. Click **"Deploy to GitHub Pages"** workflow
3. Click **"Run workflow"** button
4. Select `main` branch
5. Click **"Run workflow"**

---

## Step 4: Verify Deployment

1. Go to the **Actions** tab
2. Wait for the workflow to complete (usually 2-3 minutes)
3. Look for a green checkmark ✅

Once complete, your site is live at:
### **https://muhibchy.github.io/IT-Support-CRM/**

---

## 📋 What Was Configured

This repository includes:

✅ **Vite Configuration** (`vite.config.ts`)
   - Base path set to `/IT-Support-CRM/`
   - Environment variable handling for API keys

✅ **GitHub Actions Workflow** (`.github/workflows/deploy.yml`)
   - Automatic build on push to main
   - Deploys to GitHub Pages
   - Handles environment variables securely

✅ **Environment Template** (`.env.local.example`)
   - Template for local development
   - Instructions for API key setup

---

## 🔧 Troubleshooting

### Site shows 404 error:
- Verify GitHub Pages is enabled in Settings > Pages
- Check that Source is set to "GitHub Actions"
- Wait a few minutes after deployment

### Build fails in Actions:
- Ensure `GEMINI_API_KEY` secret is added correctly
- Check the Actions tab for error details
- Verify all dependencies are in `package.json`

### API features not working:
- Confirm API key is valid at https://aistudio.google.com/app/apikey
- Check browser console for error messages
- Verify the secret name is exactly `GEMINI_API_KEY`

---

## 🛠️ Local Development

To run the app locally:

```bash
# Install dependencies
npm install

# Copy environment template
cp .env.local.example .env.local

# Add your API key to .env.local
# GEMINI_API_KEY=your_key_here

# Start development server
npm run dev
```

Visit: http://localhost:3000

---

## 📝 Manual Build (Optional)

To build the project locally:

```bash
npm install
npm run build
```

The production files will be in the `dist/` folder.

---

## 🎯 Next Steps

1. ✅ Enable GitHub Pages
2. ✅ Add GEMINI_API_KEY secret
3. ✅ Push to main or trigger workflow
4. ✅ Share the live URL with your customers!

**Your live site:** https://muhibchy.github.io/IT-Support-CRM/

---

## 📞 Support

If you encounter issues:
- Check the [Actions tab](https://github.com/MuhibChy/IT-Support-CRM/actions) for build logs
- Review the [README.md](README.md) for additional information
- Ensure all secrets are configured correctly
