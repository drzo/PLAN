# HyperGraphiQL Standalone Deployment Guide

## 🎯 Quick Access

The standalone HyperGraphiQL is a single HTML file that works anywhere without dependencies!

**File Location:** `public/hypergraph-standalone.html`

## 🚀 Deployment Options

### Option 1: GitHub Pages (Recommended - FREE)

1. **Enable GitHub Pages:**
   ```bash
   # Push the file to your repository
   git add public/hypergraph-standalone.html
   git commit -m "Add standalone HyperGraphiQL"
   git push origin main
   ```

2. **Configure GitHub Pages:**
   - Go to your repository settings
   - Navigate to "Pages" section
   - Source: Deploy from a branch
   - Branch: `main` / `public` folder
   - Click "Save"

3. **Access your deployment:**
   ```
   https://drzo.github.io/PLAN/hypergraph-standalone.html
   ```

### Option 2: Netlify (FREE)

1. **Drag and Drop:**
   - Go to [https://app.netlify.com/drop](https://app.netlify.com/drop)
   - Drag the `public` folder
   - Get instant URL like: `https://random-name.netlify.app/hypergraph-standalone.html`

2. **Or use Netlify CLI:**
   ```bash
   npm install -g netlify-cli
   cd public
   netlify deploy --prod
   ```

### Option 3: Vercel (FREE)

```bash
npm install -g vercel
cd public
vercel --prod
```

### Option 4: Cloudflare Pages (FREE)

1. Go to [https://pages.cloudflare.com/](https://pages.cloudflare.com/)
2. Connect your GitHub repository
3. Build settings:
   - Build command: (leave empty)
   - Build output directory: `public`
4. Deploy!

### Option 5: Any Static Host

Simply upload `public/hypergraph-standalone.html` to any web server:
- AWS S3 + CloudFront
- Google Cloud Storage
- Azure Static Web Apps
- Your own server

### Option 6: Local File

You can even open it directly in your browser:
```bash
# On Mac/Linux
open public/hypergraph-standalone.html

# On Windows
start public/hypergraph-standalone.html

# Or just double-click the file
```

## 📊 Features

### 1. Repository Fetching
- Fetches all repositories from cogpy organization
- Supports GitHub Personal Access Token for higher rate limits
- Handles pagination automatically (up to 2000 repos)
- Shows detailed statistics

### 2. Feature Analysis
Analyzes repositories against 10 kernel/OS primitives:
- ✅ Boot/Init
- ✅ CPU Scheduling
- ✅ Memory Management
- ✅ Process Management
- ✅ Interrupt Handling
- ✅ System Calls
- ✅ I/O Operations
- ✅ Synchronization
- ✅ Timer/Clock
- ✅ Security/Protection

### 3. Data Export
- Export all repository data as JSON
- Includes metadata, descriptions, and statistics
- Perfect for further analysis

## 🔑 GitHub Token (Optional but Recommended)

Without a token: 60 requests/hour
With a token: 5,000 requests/hour

**Create a token:**
1. Go to [https://github.com/settings/tokens](https://github.com/settings/tokens)
2. Click "Generate new token (classic)"
3. Select scopes: `public_repo` and `read:org`
4. Copy the token
5. Paste it in the HyperGraphiQL interface

**Note:** The token is only used in your browser, never sent to any server except GitHub.

## 🎨 How to Use

1. **Open the page** in your browser
2. **(Optional)** Enter your GitHub token for higher rate limits
3. **Click "Fetch Repositories"** to load all cogpy repos
4. **View Overview** tab for statistics
5. **Browse Repositories** tab to see all repos
6. **Click "Analyze Features"** to match repos against kernel/OS spec
7. **View Analysis** tab to see which repos have which features
8. **Click "Export JSON"** to download the data

## 📈 Analysis Results

The analysis will show:
- Which repositories match each kernel/OS feature
- Match score (how many keywords matched)
- Matched keywords for each repo
- Repository descriptions and links

Example output:
```
Boot/Init (15 repositories)
├─ coglux (3 matches: boot, init, loader)
├─ cogprime (2 matches: boot, startup)
└─ ...

CPU Scheduling (23 repositories)
├─ cogtaskflow (4 matches: scheduler, task, thread, cpu)
├─ kokkog (3 matches: scheduling, thread, process)
└─ ...
```

## 🔧 Customization

To modify the analysis keywords, edit the `featureKeywords` object in the HTML file:

```javascript
const featureKeywords = {
    'Boot/Init': ['boot', 'init', 'bootstrap', 'startup', 'loader', 'bootloader'],
    'CPU Scheduling': ['scheduler', 'scheduling', 'cpu', 'thread', 'task', 'process'],
    // Add more features or modify keywords
};
```

## 🐛 Troubleshooting

### Rate Limit Errors
- Add a GitHub Personal Access Token
- Wait for the rate limit to reset (shown in error message)

### CORS Errors
- The file must be served over HTTP/HTTPS (not file://)
- Use any of the deployment options above
- Or run a local server: `python3 -m http.server 8080`

### No Repositories Showing
- Check browser console for errors
- Verify GitHub API is accessible
- Try with a GitHub token

## 📝 Technical Details

- **No dependencies:** Pure HTML, CSS, and JavaScript
- **No build step:** Works immediately
- **No backend:** All processing happens in the browser
- **Privacy-friendly:** GitHub token never leaves your browser
- **Responsive:** Works on mobile and desktop
- **Fast:** Efficient rendering for 200+ repositories

## 🎯 Next Steps

After deployment, you can:
1. Share the URL with your team
2. Bookmark it for quick access
3. Embed it in documentation
4. Use the exported JSON for further analysis
5. Customize the feature keywords for your needs

## 📚 Related Documentation

- [HyperGraphiQL System Docs](./docs/HYPERGRAPHIQL.md)
- [AGI-OS Documentation](./docs/agi-os/README.md)
- [Kernel Function Manifest](./docs/agi-os/KERNEL_FUNCTION_MANIFEST.md)
