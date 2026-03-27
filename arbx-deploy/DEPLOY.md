# ARBX Bot — Deployment Guide

## 🚀 Option 1: Vercel (Recommended — 2 minutes)

### Method A: Drag & Drop (No account setup needed)
1. Go to **https://vercel.com/new**
2. Sign up free with GitHub, Google, or email
3. Click **"Deploy without a framework"** → **"Continue"**
4. Drag the entire `arbx-deploy` folder onto the upload area
5. Click **Deploy**
6. Your bot is live at `https://arbx-bot-xxxx.vercel.app` ✅

### Method B: Vercel CLI
```bash
npm i -g vercel
cd arbx-deploy
vercel --prod
```
Follow the prompts — done in under 60 seconds.

---

## 🟢 Option 2: Netlify (Also free — 2 minutes)

1. Go to **https://app.netlify.com/drop**
2. Drag the `arbx-deploy` folder onto the page
3. Done — you get a URL like `https://arbx-bot-xxxx.netlify.app` ✅

No account required for Netlify Drop!

---

## 🐙 Option 3: GitHub Pages (Free forever)

1. Create a new GitHub repo (e.g. `arbx-bot`)
2. Upload the files from `arbx-deploy/`
3. Go to **Settings → Pages → Source → main branch → / (root)**
4. Your URL: `https://yourusername.github.io/arbx-bot` ✅

---

## ✅ After Deploying — MetaMask Setup

Once live on any of these platforms, MetaMask connects perfectly:

1. Open your deployed URL in Chrome or Brave
2. Make sure MetaMask extension is installed
3. Click **🦊 Connect MetaMask**
4. Approve in the MetaMask popup
5. Start with **Sepolia Testnet** first before using real ETH

---

## 🔒 Security Notes

- The bot runs **100% client-side** — no server, no database
- Your private keys **never leave MetaMask** — the bot only reads your public address
- All API calls go directly to DexScreener and CoinGecko from your browser
- You can verify every line of code in `index.html`

---

## 📁 Files in This Package

| File | Purpose |
|------|---------|
| `index.html` | The complete ARBX bot application |
| `vercel.json` | Vercel deployment configuration |
| `_headers` | Netlify headers configuration |
| `DEPLOY.md` | This guide |

---

## ⚠️ Important

- Always use a **dedicated trading wallet** — never connect your main wallet
- Start on **Sepolia testnet** with test ETH before trading real funds
- The bot executes **real on-chain transactions** — gas fees apply
- Get Sepolia test ETH free at: https://sepoliafaucet.com
