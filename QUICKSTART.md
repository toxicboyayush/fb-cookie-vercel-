# ⚡ QUICK START GUIDE

## 🚀 5 मिनट में शुरू करें!

### Step 1: Install करें (2 min)
```bash
cd facebook-automation-nextjs
npm install
```

### Step 2: Environment Setup (30 sec)
```bash
cp .env.example .env.local
```

`.env.local` में edit करें:
```
JWT_SECRET=MySecretKey12345XYZ
```

### Step 3: Run करें (30 sec)
```bash
npm run dev
```

Browser में खोलें: http://localhost:3000

---

## 🌐 Vercel पर Deploy (2 min)

### सबसे आसान तरीका:
```bash
# Install Vercel CLI
npm install -g vercel

# Login
vercel login

# Deploy
vercel

# Production
vercel --prod
```

Environment variable add करें:
```bash
vercel env add JWT_SECRET production
# Enter: YourSecretKey123
```

Done! ✅

---

## 🎯 पहली बार Use करें

### 1. Account बनाएं (1 min)
- Open your URL
- Click "SIGN UP"
- Enter username & password
- Click "CREATE ACCOUNT"

### 2. Login करें (30 sec)
- Enter credentials
- Click "LOGIN NOW"

### 3. Configure करें (2 min)

**Chat ID:**
- Facebook Messenger में conversation खोलें
- URL से ID copy करें: `messenger.com/t/1362400298935018`
- Paste करें Chat ID field में

**Cookie:**
- Single Cookie mode select करें
- अपनी cookie paste करें
- (Guide: `COOKIE_GUIDE.md` देखें)

**Messages:**
- Messages type करें (एक line में एक)
- या `example-messages.txt` upload करें

**Delay:**
- 30 seconds set करें

### 4. Save & Start (1 min)
- "SAVE CONFIGURATION" click करें
- "AUTOMATION CONTROL" tab खोलें
- "START AUTOMATION" click करें

---

## 🍪 Cookie Quick Guide

### Chrome/Edge से:
1. Facebook login करें
2. F12 press करें
3. Application → Cookies → facebook.com
4. Copy करें: `c_user`, `xs`, `datr`, `fr`
5. Format: `c_user=VALUE; xs=VALUE; datr=VALUE; fr=VALUE;`

---

## ✅ Done!

अब automation चल रहा है! 🎉

Live logs देखें console में।

---

## 🆘 Problem?

**Login नहीं हो रहा:**
- Fresh cookies use करें
- Incognito mode से cookies लें

**Messages नहीं जा रहे:**
- Chat ID check करें (numeric होना चाहिए)
- Cookies fresh हैं?

**Automation stop हो गया:**
- Normal है free Vercel पर
- Restart करें manually

---

**Full Guide:** `COMPLETE_GUIDE_HINDI.md` पढ़ें

**Cookie Help:** `COOKIE_GUIDE.md` देखें

**Deployment:** `DEPLOYMENT.md` follow करें

---

**Happy Automating! 🚀**

MADE WITH ❤️ BY YKTI RAWAT
