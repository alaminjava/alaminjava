# 🚀 Portfolio Deployment Guide

## Step 1 — GitHub Pages Setup

1. Go to [github.com](https://github.com) → Sign in → **New repository**
2. Name it **exactly** your username (e.g. `alaminhabibul.github.io`) for a user page, OR any name like `portfolio` for a project page
3. Set to **Public** → Create repository
4. Upload these files to the repo:
   - `index.html` ← your portfolio (the main file)
   - `CNAME` ← for js.org subdomain
5. Go to **Settings → Pages** → Source: `main` branch → `/root` → **Save**
6. Your site will be live at: `https://yourusername.github.io` within 2 minutes ✅

---

## Step 2 — Get your free JS.ORG subdomain

**Your target URL:** `https://alamin.js.org` (or choose any available name)

### a) Add CNAME file to your repo
The `CNAME` file is already included. It contains:
```
alamin.js.org
```
Change this to whatever subdomain you want (e.g. `marketeralamin.js.org`).

### b) Make a Pull Request to js.org
1. Go to: https://github.com/js-org/js.org
2. Click **Fork** (top right)
3. In your fork, open the file: `cnames_active.js`
4. Find the alphabetical position for your subdomain and add one line:
   ```
   "alamin": "yourusername.github.io",
   ```
5. Click **Propose changes** → **Create Pull Request**
6. Wait 24–48 hours for approval → your site goes live at `alamin.js.org` 🎉

---

## Step 3 — Activate the Email Form (EmailJS — Free)

The form sends email directly to **alaminhabibulinfo@gmail.com**

1. Sign up free at [emailjs.com](https://emailjs.com)
2. **Add Email Service** → Choose Gmail → Connect your Gmail account → Copy **Service ID**
3. **Email Templates** → Create Template → Use these variables in the template body:
   ```
   From: {{from_name}} ({{from_email}})
   Company: {{company}}
   Service: {{service}}
   Budget: {{budget}}
   
   {{message}}
   ```
   → Copy **Template ID**
4. **Account → Public Key** → Copy your **Public Key**
5. Open `index.html` and replace these 3 lines near the bottom:
   ```js
   const EMAILJS_PUBLIC_KEY  = 'YOUR_PUBLIC_KEY';   // ← paste here
   const EMAILJS_SERVICE_ID  = 'YOUR_SERVICE_ID';   // ← paste here
   const EMAILJS_TEMPLATE_ID = 'YOUR_TEMPLATE_ID';  // ← paste here
   ```
6. Save and push to GitHub → form is now fully live! ✅

> **Without EmailJS setup:** The form still works — it opens the visitor's mail client with the message pre-filled (mailto: fallback). WhatsApp button always works regardless.

---

## WhatsApp Button
Pre-configured to: **+880 1521 366 254**
When a visitor fills the form and clicks WhatsApp, the message is pre-filled automatically. ✅

---

## Quick File Summary
| File | Purpose |
|------|---------|
| `index.html` | Your portfolio website |
| `CNAME` | Routes js.org subdomain to GitHub Pages |
| `DEPLOYMENT-GUIDE.md` | This guide |
