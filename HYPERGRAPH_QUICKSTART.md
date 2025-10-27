# 🚀 HyperGraphiQL Quick Start

## ✨ Instant Access

Your HyperGraphiQL is now deployed and ready to use!

### 🌐 Live URLs

**GitHub Pages (Your Fork):**
```
https://drzo.github.io/PLAN/
```

**Direct File Access:**
```
https://drzo.github.io/PLAN/hypergraph-standalone.html
```

## 🎯 How to Use (3 Simple Steps)

### Step 1: Open the Page
Click the link above or visit: [https://drzo.github.io/PLAN/](https://drzo.github.io/PLAN/)

### Step 2: Fetch Repositories
1. (Optional) Enter your GitHub token for higher rate limits
2. Click **"🔄 Fetch Repositories"**
3. Wait 5-10 seconds while it loads all 231+ cogpy repos

### Step 3: Analyze Features
1. Click **"🔍 Analyze Features"**
2. Switch to the **"🔬 Feature Analysis"** tab
3. See which repos match each kernel/OS primitive!

## 📊 What You'll See

The analysis shows which repositories have features from the kernel/OS spec:

```
✅ Boot/Init (15 repos)
   - coglux: boot, init, loader
   - cogprime: boot, startup
   
✅ CPU Scheduling (23 repos)
   - cogtaskflow: scheduler, task, thread, cpu
   - kokkog: scheduling, thread, process
   
✅ Memory Management (18 repos)
   - coglux: memory, malloc, heap, mmu
   - cogprime: alloc, memory
   
... and 7 more categories
```

## 🔑 GitHub Token (Optional)

For better rate limits (5,000 vs 60 requests/hour):

1. Go to: [https://github.com/settings/tokens](https://github.com/settings/tokens)
2. Click "Generate new token (classic)"
3. Select: `public_repo` and `read:org`
4. Copy the token
5. Paste in HyperGraphiQL

**Your token is safe:** It's only used in your browser, never sent anywhere except GitHub.

## 💾 Export Data

Click **"💾 Export JSON"** to download all repository data for further analysis.

## 🎨 Features

- ✅ **No installation required** - Just open in browser
- ✅ **Works offline** - After initial load
- ✅ **Fast** - Analyzes 200+ repos in seconds
- ✅ **Mobile friendly** - Responsive design
- ✅ **Privacy first** - All processing in your browser
- ✅ **Export ready** - Download JSON for further analysis

## 📱 Share It

Share this URL with your team:
```
https://drzo.github.io/PLAN/
```

## 🔧 Customize

Want to modify the analysis keywords? Edit `public/hypergraph-standalone.html`:

```javascript
const featureKeywords = {
    'Boot/Init': ['boot', 'init', 'bootstrap', ...],
    'Your Custom Feature': ['keyword1', 'keyword2', ...],
};
```

## 📚 Full Documentation

See [HYPERGRAPH_DEPLOYMENT.md](./HYPERGRAPH_DEPLOYMENT.md) for:
- Deployment to other platforms (Netlify, Vercel, Cloudflare)
- Customization guide
- Troubleshooting
- Technical details

## 🎉 That's It!

You now have a fully functional repository analysis tool that:
- Fetches all cogpy organization repos
- Analyzes them against kernel/OS specifications
- Shows which repos have which features
- Exports data for further analysis

**Start analyzing now:** [https://drzo.github.io/PLAN/](https://drzo.github.io/PLAN/)
