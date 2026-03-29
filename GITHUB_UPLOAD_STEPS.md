# 📤 How to Upload This Project to GitHub

Follow these steps exactly. Takes about 5 minutes.

---

## STEP 1 — Install Git (skip if already installed)

**Windows:**  
Download from https://git-scm.com/download/win and install with default settings.

**macOS:**  
```bash
xcode-select --install
```

**Linux (Ubuntu/Debian):**  
```bash
sudo apt install git
```

Verify installation:
```bash
git --version
```

---

## STEP 2 — Create a GitHub Account

Go to https://github.com and sign up (skip if you already have one).

---

## STEP 3 — Create a New Repository on GitHub

1. Log in to https://github.com
2. Click the **"+"** button (top right) → **"New repository"**
3. Fill in:
   - **Repository name:** `irad-excel-generator`
   - **Description:** `iRAD PDF to Excel converter using Streamlit`
   - **Visibility:** Public (or Private — your choice)
   - ❌ Do NOT check "Add a README file" (we already have one)
4. Click **"Create repository"**
5. Copy the repository URL shown — it will look like:
   `https://github.com/YOUR_USERNAME/irad-excel-generator.git`

---

## STEP 4 — Configure Git (first time only)

Open terminal / command prompt and run:

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

---

## STEP 5 — Open Terminal in the Project Folder

**Windows:**  
Open the `irad-excel-generator` folder in File Explorer → right-click → **"Open in Terminal"** (or Git Bash)

**macOS / Linux:**  
```bash
cd path/to/irad-excel-generator
```

---

## STEP 6 — Initialize Git and Push

Run these commands one by one:

```bash
# Initialize a new Git repository
git init

# Add all files to staging
git add .

# Create the first commit
git commit -m "Initial commit: iRAD PDF to Excel generator"

# Rename branch to main (GitHub standard)
git branch -M main

# Connect to your GitHub repository (replace YOUR_USERNAME)
git remote add origin https://github.com/YOUR_USERNAME/irad-excel-generator.git

# Push files to GitHub
git push -u origin main
```

---

## STEP 7 — Authenticate with GitHub

When prompted for credentials:

### Option A — Personal Access Token (recommended)
1. Go to https://github.com/settings/tokens
2. Click **"Generate new token (classic)"**
3. Give it a name, set expiry, check **"repo"** scope
4. Click **"Generate token"** and copy it
5. Use this token as your **password** when Git asks

### Option B — GitHub CLI (easier)
```bash
# Install GitHub CLI from https://cli.github.com
gh auth login
# Follow the prompts (choose HTTPS, then browser login)
```

---

## STEP 8 — Verify Upload

1. Go to `https://github.com/YOUR_USERNAME/irad-excel-generator`
2. You should see all 4 files:
   - `app.py`
   - `requirements.txt`
   - `.gitignore`
   - `README.md`

---

## STEP 9 — Future Updates (when you edit the code)

Whenever you change `app.py` or any file, push the update like this:

```bash
git add .
git commit -m "Describe what you changed"
git push
```

---

## ✅ Done!

Your project is now live at:
`https://github.com/YOUR_USERNAME/irad-excel-generator`

---

## 🌐 Optional — Deploy on Streamlit Cloud (free hosting)

Make your app accessible to anyone via a public URL:

1. Go to https://streamlit.io/cloud and sign in with GitHub
2. Click **"New app"**
3. Select your repository: `irad-excel-generator`
4. Set **Main file path:** `app.py`
5. Click **"Deploy"**

Your app will be live at:
`https://YOUR_USERNAME-irad-excel-generator-app-XXXXX.streamlit.app`
