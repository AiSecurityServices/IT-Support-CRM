# 🚀 Quick Setup Checklist for GitHub Pages Deployment

Use this checklist to deploy your IT Support CRM to GitHub Pages.

---

## ☑️ Pre-Deployment Checklist

### 1. Repository Setup
- [ ] Repository is public (or you have GitHub Pro for private repos)
- [ ] All code is pushed to the `main` branch
- [ ] Repository URL: https://github.com/MuhibChy/IT-Support-CRM

### 2. GitHub Pages Configuration
- [ ] Go to **Settings** > **Pages**
- [ ] Set Source to **GitHub Actions**
- [ ] Save changes

### 3. API Key Configuration
- [ ] Get Gemini API key from: https://aistudio.google.com/app/apikey
- [ ] Go to **Settings** > **Secrets and variables** > **Actions**
- [ ] Add new secret:
  - Name: `GEMINI_API_KEY`
  - Value: [Your API key]

### 4. Deploy
- [ ] Push changes to `main` branch, OR
- [ ] Manually trigger workflow from **Actions** tab

### 5. Verify
- [ ] Check **Actions** tab for successful deployment
- [ ] Visit: https://muhibchy.github.io/IT-Support-CRM/
- [ ] Test all features work correctly

---

## 📝 Quick Commands

### Push to Deploy:
```bash
git add .
git commit -m "Deploy to GitHub Pages"
git push origin main
```

### Local Development:
```bash
npm install
cp .env.local.example .env.local
# Edit .env.local and add your GEMINI_API_KEY
npm run dev
```

### Build Locally:
```bash
npm run build
```

---

## ✅ Success Criteria

Your deployment is successful when:
- ✅ GitHub Actions workflow shows green checkmark
- ✅ Site loads at https://muhibchy.github.io/IT-Support-CRM/
- ✅ Dashboard displays correctly
- ✅ AI features work (if API key is configured)
- ✅ No console errors in browser

---

## 🆘 Common Issues

| Issue | Solution |
|-------|----------|
| 404 Error | Wait 2-3 minutes, clear browser cache |
| Build Fails | Check API key secret is set correctly |
| Blank Page | Check browser console for errors |
| AI Not Working | Verify GEMINI_API_KEY is valid |

---

## 📞 Need Help?

1. Check [DEPLOYMENT_INSTRUCTIONS.md](DEPLOYMENT_INSTRUCTIONS.md) for detailed steps
2. Review [README.md](README.md) for project information
3. Check GitHub Actions logs for error details

---

**Target URL:** https://muhibchy.github.io/IT-Support-CRM/

**Last Updated:** 2025
