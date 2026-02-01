# 🦂 YKTI RAWAT - पूर्ण सेटअप गाइड

## 📋 विषय सूची
1. [सिस्टम की खासियतें](#features)
2. [इंस्टालेशन](#installation)
3. [Vercel पर Deploy करना](#deployment)
4. [यूज़ कैसे करें](#usage)
5. [Cookies कैसे लें](#cookies)
6. [ट्रबलशूटिंग](#troubleshooting)

---

## ✨ सिस्टम की खासियतें {#features}

### 🔥 मुख्य Features:
- ✅ **Single Cookie Mode**: एक cookie से चलाएं
- ✅ **Multiple Cookies Mode**: अनेक cookies से चलाएं (cookies.txt upload करें)
- ✅ **Message File Upload**: messages.txt file upload करें
- ✅ **Premium Design**: Professional और modern UI
- ✅ **24/7 Ready**: Vercel पर continuously चलता रहता है
- ✅ **Live Logs**: Real-time में देखें क्या हो रहा है
- ✅ **Auto-Save**: Configuration automatically save होता है
- ✅ **Secure**: Encrypted cookies और password hashing

---

## 🚀 इंस्टालेशन {#installation}

### स्टेप 1: Prerequisites
```bash
# Node.js check करें (18+ होना चाहिए)
node --version

# अगर नहीं है तो download करें: https://nodejs.org
```

### स्टेप 2: Project Setup
```bash
# Project folder में जाएं
cd facebook-automation-nextjs

# Dependencies install करें
npm install

# यह 2-3 मिनट लग सकता है
```

### स्टेप 3: Environment Setup
```bash
# .env.local file बनाएं
cp .env.example .env.local

# अपना JWT secret set करें
# .env.local file खोलें और edit करें:
JWT_SECRET=your-super-secret-key-12345-change-this
```

### स्टेप 4: Development में चलाएं
```bash
# Development server start करें
npm run dev

# Browser में खोलें: http://localhost:3000
```

---

## 🌐 Vercel पर Deploy करना {#deployment}

### तरीका A: Vercel CLI (Recommended)

#### 1. Vercel CLI Install करें
```bash
npm install -g vercel
```

#### 2. Login करें
```bash
vercel login
# आपका email enter करें
# Email में आया link click करें
```

#### 3. Deploy करें
```bash
# Project folder में जाएं
cd facebook-automation-nextjs

# Deploy करें
vercel

# सभी questions में "Y" press करें
# Project name enter करें (जैसे: fb-automation-pro)
```

#### 4. Environment Variable Add करें
```bash
# JWT_SECRET add करें
vercel env add JWT_SECRET production

# एक strong secret key enter करें (minimum 20 characters)
# Example: MySecretKey123XYZ456ABC789
```

#### 5. Production Deploy करें
```bash
vercel --prod
```

#### 6. आपका URL मिल जाएगा!
```
✅ Production: https://fb-automation-pro.vercel.app
```

---

### तरीका B: GitHub + Vercel Dashboard

#### 1. GitHub पर Upload करें
```bash
# Git initialize करें
git init
git add .
git commit -m "Initial commit"

# GitHub repo create करें और upload करें
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
git push -u origin main
```

#### 2. Vercel में Import करें
1. https://vercel.com पर जाएं
2. "New Project" click करें
3. GitHub repo select करें
4. "Import" click करें

#### 3. Environment Variables Set करें
1. "Environment Variables" section में जाएं
2. Add करें:
   - **Name**: `JWT_SECRET`
   - **Value**: `YourSecretKey123ABC` (strong random string)
   - **Environment**: Production
3. "Add" click करें

#### 4. Deploy करें
1. "Deploy" button click करें
2. 5-10 मिनट wait करें
3. आपका app live हो जाएगा!

---

## 🎯 यूज़ कैसे करें {#usage}

### चरण 1: Account बनाएं

1. अपने deployed URL पर जाएं
2. "SIGN UP" tab पर click करें
3. Username और Password enter करें
4. "CREATE ACCOUNT" click करें
5. Success message आने पर "LOGIN" tab पर जाएं

### चरण 2: Login करें

1. अपना username और password enter करें
2. "LOGIN NOW" click करें
3. Dashboard खुल जाएगा

### चरण 3: Configuration करें

#### A. Chat ID Setup:
```
1. Facebook Messenger खोलें
2. जिस conversation को automate करना है वो खोलें
3. URL से ID copy करें:
   
   Example URL:
   https://www.facebook.com/messages/t/1362400298935018
   
   Chat ID: 1362400298935018

4. Dashboard में "CHAT/CONVERSATION E2EE ID" में paste करें
```

#### B. Cookie Setup:

**Single Cookie Mode:**
```
1. "SINGLE COOKIE" button पर click करें
2. नीचे दिए guide से cookie copy करें
3. "FACEBOOK COOKIE (PASTE)" box में paste करें

OR

1. "OR UPLOAD COOKIE FILE" button click करें
2. अपनी cookie.txt file select करें
```

**Multiple Cookies Mode:**
```
1. "MULTIPLE COOKIES" button पर click करें
2. "CHOOSE FILE" button click करें
3. cookies.txt file select करें (एक line में एक cookie)

Example cookies.txt:
c_user=123; xs=456; fr=789;
c_user=abc; xs=def; fr=ghi;
c_user=xyz; xs=uvw; fr=rst;
```

#### C. Messages Setup:

**Direct Typing:**
```
1. "MESSAGES" box में type करें
2. हर message नई line में लिखें

Example:
Hello!
How are you?
Good morning!
Have a great day!
```

**File Upload:**
```
1. "UPLOAD MESSAGE FILE" button click करें
2. अपनी messages.txt file select करें
3. File में हर line में एक message होना चाहिए
```

#### D. अन्य Settings:

```
NAME PREFIX: [Optional]
- Message से पहले लगने वाला text
- Example: [YKTI RAWAT]
- Final message: [YKTI RAWAT] Hello!

DELAY (SECONDS):
- Messages के बीच का time gap
- Minimum: 1 second
- Maximum: 300 seconds
- Recommended: 30-60 seconds
```

### चरण 4: Configuration Save करें

```
1. सभी settings fill करने के बाद
2. नीचे scroll करें
3. "💾 SAVE CONFIGURATION" button click करें
4. "✅ Configuration saved successfully!" message आएगा
```

### चरण 5: Automation Start करें

```
1. "AUTOMATION CONTROL" tab पर click करें
2. Stats cards check करें:
   - Messages Sent: 0 (initially)
   - Status: 🔴 STOPPED
   - Chat ID: आपकी set की हुई ID

3. "▶️ START AUTOMATION" button click करें
4. Status बदल जाएगा: 🟢 RUNNING
5. Console में logs दिखने लगेंगे

Example Logs:
[10:30:45] 🚀 Starting automation...
[10:30:46] ✅ Single cookie applied
[10:30:48] 🌐 Navigating to chat: 1362400298935018
[10:30:52] ✅ Successfully logged in
[10:30:55] 📨 Message sent: Hello!
[10:31:25] ⏳ Waiting 30 seconds...
```

### चरण 6: Automation Monitor करें

```
Live Console में देखें:
- 📨 Messages sent
- ⏳ Wait times
- ✅ Success status
- ❌ Any errors

Stats cards monitor करें:
- MESSAGES SENT counter बढ़ता जाएगा
- STATUS green रहेगा
```

### चरण 7: Automation Stop करें

```
1. "⏹️ STOP AUTOMATION" button click करें
2. Status बदल जाएगा: 🔴 STOPPED
3. Console में "⚠️ Automation stopped" दिखेगा
```

---

## 🍪 Facebook Cookies कैसे लें {#cookies}

### विधि 1: EditThisCookie Extension (सबसे आसान)

#### Chrome/Edge के लिए:
```
1. Chrome Web Store खोलें
2. "EditThisCookie" search करें
3. Extension install करें

4. Facebook.com पर जाएं
5. Login करें (fresh login)

6. Extension icon (🍪) पर click करें
7. "Export" button click करें
8. सारे cookies copy हो जाएंगे

9. Application में paste करें
```

### विधि 2: Browser Developer Tools

#### Chrome/Edge:
```
1. Facebook.com पर login करें
2. F12 press करें (DevTools open होगा)
3. "Application" tab पर जाएं
4. Left sidebar में "Cookies" expand करें
5. "https://www.facebook.com" पर click करें

6. Important cookies copy करें:
   - c_user
   - xs
   - datr
   - fr
   - sb

7. Format में paste करें:
   c_user=VALUE; xs=VALUE; datr=VALUE; fr=VALUE; sb=VALUE;
```

#### Firefox:
```
1. Facebook.com पर login करें
2. F12 press करें
3. "Storage" tab पर जाएं
4. "Cookies" → "https://www.facebook.com"
5. Important cookies copy करें (same as Chrome)
```

### Cookie Format Examples:

**Single Cookie String:**
```
c_user=100012345678901; xs=12:abc123:2:1234567890; datr=xyz123; fr=0Abc.ABC.Xyz; sb=abc456;
```

**Multiple Cookies File (cookies.txt):**
```
c_user=100012345678901; xs=12:abc123:2:1234567890; datr=xyz1; fr=0Abc1; sb=abc1;
c_user=100087654321098; xs=34:def456:2:9876543210; datr=xyz2; fr=0Abc2; sb=abc2;
c_user=100055555555555; xs=56:ghi789:2:5555555555; datr=xyz3; fr=0Abc3; sb=abc3;
```

### ⚠️ Important Cookie Tips:

```
✅ हमेशा fresh login के cookies use करें
✅ Incognito/Private mode में login करें फिर cookies लें
✅ Cookies regularly refresh करें (हर 7-10 दिन में)
✅ Multiple accounts के लिए अलग-अलग cookies use करें

❌ Expired cookies काम नहीं करेंगे
❌ Cookies publicly share न करें
❌ Password वाली cookies publicly न डालें
```

---

## 🛠️ ट्रबलशूटिंग {#troubleshooting}

### समस्या 1: "Automation stopped automatically"

**कारण:** Vercel Free tier पर function 10 seconds में timeout हो जाता है

**समाधान:**
```
1. यह normal है free tier पर
2. Auto-resume होगा जब आप login करेंगे
3. या "START AUTOMATION" फिर से click करें

Long-term solution:
- Vercel Pro plan लें ($20/month)
- या VPS पर deploy करें (Railway, Render, DigitalOcean)
```

### समस्या 2: "Invalid cookies" या login fail

**समाधान:**
```
1. Fresh cookies लें:
   - Facebook logout करें
   - Clear browser cookies
   - Fresh login करें
   - नए cookies copy करें

2. Incognito mode use करें:
   - Private/Incognito window खोलें
   - Facebook login करें
   - Cookies copy करें

3. Cookie format check करें:
   - सभी important cookies हैं?
   - Format correct है?
   - Spaces या extra characters नहीं हैं?
```

### समस्या 3: "Chat ID not working"

**समाधान:**
```
1. Correct Chat ID copy करें:
   
   ✅ Correct:
   https://www.facebook.com/messages/t/1362400298935018
   Chat ID: 1362400298935018
   
   ❌ Wrong:
   https://www.messenger.com/t/username
   (यह numeric ID नहीं है)

2. Facebook Messenger web version use करें
3. URL से numeric ID ही copy करें
```

### समस्या 4: Messages send नहीं हो रहे

**Check करें:**
```
1. ✅ Chat ID correct है?
2. ✅ Cookies fresh हैं?
3. ✅ Messages properly formatted हैं?
4. ✅ Internet connection stable है?
5. ✅ Facebook account blocked तो नहीं?

Console logs check करें error के लिए
```

### समस्या 5: "Unauthorized" error

**समाधान:**
```
1. Browser cookies clear करें:
   - Settings → Privacy → Clear browsing data
   - Cookies and other site data select करें
   - Clear data

2. Application में फिर से login करें

3. JWT_SECRET environment variable check करें:
   vercel env ls
```

### समस्या 6: Database errors

**समाधान:**
```
1. Local development में:
   - data/automation.db file delete करें
   - npm run dev फिर से चलाएं

2. Vercel पर:
   - Fresh deployment करें
   - vercel --prod --force
```

### समस्या 7: CSS/Design नहीं दिख रहा

**समाधान:**
```
1. Hard refresh करें:
   - Ctrl + Shift + R (Windows/Linux)
   - Cmd + Shift + R (Mac)

2. Browser cache clear करें

3. Build फिर से करें:
   npm run build
   npm run start
```

---

## 📊 Tips for Best Performance

### Delay Settings:
```
✅ Recommended: 30-60 seconds
⚠️ Minimum: 10 seconds (avoid Facebook rate limiting)
❌ Too Low: 1-5 seconds (high risk of ban)
```

### Message Guidelines:
```
✅ Natural messages use करें
✅ Variety रखें (same message बार-बार न भेजें)
✅ Personalized content डालें
❌ Spam words avoid करें
❌ Too many links न भेजें
```

### Cookie Management:
```
✅ हर 7 दिन में cookies refresh करें
✅ Multiple accounts के लिए rotation use करें
✅ Backup cookies रखें
```

### Monitoring:
```
✅ Daily logs check करें
✅ Message count track करें
✅ Error patterns देखें
✅ Facebook notifications monitor करें
```

---

## 🎓 Advanced Tips

### Multiple Accounts चलाना:
```
1. Multiple cookies.txt बनाएं
2. Multiple cookie mode use करें
3. Rotation automatically होगा
4. सभी accounts से messages जाएंगे
```

### Custom Messages Script:
```
1. Messages में variables use करें:
   Hello {name}!
   Good morning {name}!

2. Python script से generate करें
3. Upload करें application में
```

### Scheduled Automation:
```
Currently: Manual start/stop

Future: Cron jobs setup करें Vercel पर
या GitHub Actions use करें scheduling के लिए
```

---

## 📞 Support

अगर कोई problem solve नहीं हो रही:

```
1. ✅ README.md पूरी पढ़ें
2. ✅ DEPLOYMENT.md देखें
3. ✅ COOKIE_GUIDE.md check करें
4. ✅ Console logs examine करें
5. ✅ Vercel deployment logs देखें
```

---

## 🎉 Success Checklist

जब सब कुछ working हो:

```
✅ App Vercel पर live है
✅ Login/Signup काम कर रहा है
✅ Configuration save हो रहा है
✅ Cookies properly set हैं
✅ Messages load हो रहे हैं
✅ Automation start हो रहा है
✅ Messages send हो रहे हैं
✅ Logs दिख रहे हैं
✅ Status properly update हो रहा है
```

**अब enjoy करें अपना premium automation system! 🚀**

---

**MADE WITH ❤️ BY YKTI RAWAT | © 2026**
