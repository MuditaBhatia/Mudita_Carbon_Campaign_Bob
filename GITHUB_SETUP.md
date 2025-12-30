# GitHub Repository Setup Guide

## Steps to Create and Push to GitHub Repository

### Option 1: Using GitHub Website (Recommended)

1. **Go to GitHub** and log in to your account
   - Visit: https://github.com

2. **Create a new repository**
   - Click the "+" icon in the top right corner
   - Select "New repository"
   - Repository name: `Carbon-Campaign-with-Bob`
   - Description: "IBM Verify Identity Governance Campaign Application built with Carbon Design System"
   - Choose: **Public** or **Private** (your preference)
   - **DO NOT** initialize with README, .gitignore, or license (we already have these)
   - Click "Create repository"

3. **Copy the repository URL**
   - After creation, you'll see a URL like: `https://github.com/YOUR_USERNAME/Carbon-Campaign-with-Bob.git`

4. **Open a new terminal** in the carbon-campaign-app directory and run:

```bash
cd C:/Users/003QQF744/Desktop/carbon-campaign-app

# Add the remote repository
git remote add origin https://github.com/YOUR_USERNAME/Carbon-Campaign-with-Bob.git

# Rename branch to main (if needed)
git branch -M main

# Push the code
git push -u origin main
```

### Option 2: Using GitHub CLI (if installed)

If you have GitHub CLI installed, you can create the repository directly:

```bash
cd C:/Users/003QQF744/Desktop/carbon-campaign-app

# Create repository and push
gh repo create Carbon-Campaign-with-Bob --public --source=. --remote=origin --push
```

### Option 3: Using Git Commands (After Manual Repo Creation)

If you've already created the repository on GitHub:

```bash
cd C:/Users/003QQF744/Desktop/carbon-campaign-app

# Add remote
git remote add origin https://github.com/YOUR_USERNAME/Carbon-Campaign-with-Bob.git

# Push to GitHub
git branch -M main
git push -u origin main
```

## Verify the Push

After pushing, visit your repository on GitHub:
- URL: `https://github.com/YOUR_USERNAME/Carbon-Campaign-with-Bob`
- You should see all 20 files committed
- README.md will be displayed on the repository homepage

## What's Been Committed

✅ **20 files** including:
- Source code (src/ directory)
- Components (layout, campaign)
- Pages (EmptyStatePage, CampaignListPage)
- Configuration files (package.json, tsconfig.json, vite.config.ts)
- Documentation (README.md, SETUP_GUIDE.md)
- Styles (index.scss with Carbon theme)
- Type definitions (campaign.ts)

## Repository Description

Use this description for your GitHub repository:

```
IBM Verify Identity Governance Campaign Application built with Carbon Design System. 
Features include campaign management, multi-step creation wizard, data tables, 
and dark theme UI. Built with React 18, TypeScript, and Vite.
```

## Topics/Tags to Add

Add these topics to your GitHub repository for better discoverability:
- `carbon-design-system`
- `react`
- `typescript`
- `vite`
- `ibm-carbon`
- `campaign-management`
- `dark-theme`
- `data-table`

## Next Steps After Pushing

1. Add a repository description on GitHub
2. Add topics/tags
3. Enable GitHub Pages (optional) to host the application
4. Set up branch protection rules (optional)
5. Add collaborators if needed

---

**Note**: Replace `YOUR_USERNAME` with your actual GitHub username in all commands above.