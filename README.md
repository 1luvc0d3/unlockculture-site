# Unlock Culture

Website for unlockculture.work - Building intentional organizational cultures through servant leadership and evidence-based transformation.

## Setup Instructions

### 1. Create GitHub Repository
1. Go to https://github.com/new
2. Name: `unlockculture-site` (or your preferred name)
3. Keep it public (required for free GitHub Pages)
4. Don't initialize with README (we already have files)
5. Click "Create repository"

### 2. Push Code to GitHub
```bash
cd /home/claude/unlockculture-site
git add .
git commit -m "Initial commit - Unlock Culture landing page"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/unlockculture-site.git
git push -u origin main
```

### 3. Enable GitHub Pages
1. Go to your repository on GitHub
2. Click "Settings"
3. Click "Pages" in the left sidebar
4. Under "Source", select "main" branch
5. Click "Save"
6. Wait a few minutes for the site to build

### 4. Configure Custom Domain in Cloudflare
Add these DNS records in Cloudflare for unlockculture.work:

**A Records** (point to GitHub Pages IPs):
- Type: A, Name: @, Content: ***************
- Type: A, Name: @, Content: ***************
- Type: A, Name: @, Content: ***************
- Type: A, Name: @, Content: ***************

**CNAME Record** (for www):
- Type: CNAME, Name: www, Content: YOUR_USERNAME.github.io

### 5. Configure Custom Domain in GitHub
1. In your repository settings → Pages
2. Under "Custom domain", enter: unlockculture.work
3. Check "Enforce HTTPS" (after DNS propagates)

### 6. Wait for DNS Propagation
- Can take 5 minutes to 24 hours
- Check status: `dig unlockculture.work`

## Framework

**Process → Predictable Behavior → Habits → Culture**

Building cultures that ship value through intentional design and servant leadership.

## Contact

anbu.ilangovane@unlockculture.work
