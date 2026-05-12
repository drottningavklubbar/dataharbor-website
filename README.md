# Data Harbor SRL — Website

## Deploy to Railway

### Option A — Deploy via GitHub (recommended)

1. Push this folder to a GitHub repository:
   ```bash
   git init
   git add .
   git commit -m "Initial website"
   git remote add origin https://github.com/YOUR_USERNAME/dataharbor-website.git
   git push -u origin main
   ```

2. Go to [railway.app](https://railway.app) → **New Project → Deploy from GitHub repo**

3. Select your repository — Railway auto-detects `package.json` and deploys.

4. Your site will be live at `https://dataharbor-website.up.railway.app` in ~60 seconds.

### Option B — Deploy via Railway CLI

```bash
# Install Railway CLI
npm install -g @railway/cli

# Login
railway login

# Create project and deploy
railway init
railway up
```

### Add your custom domain (dataharbor.ro)

1. In Railway dashboard → your project → **Settings → Networking → Custom Domain**
2. Enter `dataharbor.ro` (and `www.dataharbor.ro`)
3. Railway gives you a CNAME record — add it in your DNS registrar (rotld.ro, GoDaddy, etc.)
4. SSL is provisioned automatically (Let's Encrypt)

## Files

| File | Purpose |
|------|---------|
| `index.html` | The website |
| `package.json` | Tells Railway to use `serve` as the static server |
| `railway.toml` | Railway deploy config |

## Local preview

```bash
npm install
npm start
# Visit http://localhost:3000
```
