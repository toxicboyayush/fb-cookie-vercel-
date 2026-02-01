# 🚀 VERCEL DEPLOYMENT GUIDE

## जल्दी से Deploy करने के लिए Steps:

### तरीका 1: Vercel CLI से (सबसे आसान)

1. **Vercel CLI Install करें:**
   ```bash
   npm install -g vercel
   ```

2. **Vercel में Login करें:**
   ```bash
   vercel login
   ```
   - अपना email enter करें
   - Email में आया link click करें

3. **Project Deploy करें:**
   ```bash
   cd facebook-automation-nextjs
   vercel
   ```
   - सभी prompts में "Y" दबाएं
   - Project name enter करें (जैसे: fb-automation)

4. **Environment Variable Set करें:**
   ```bash
   vercel env add JWT_SECRET production
   ```
   - एक strong random key enter करें (जैसे: mySecretKey12345XYZ)

5. **Production Deploy करें:**
   ```bash
   vercel --prod
   ```

बस! आपका app live हो गया! URL console में दिखेगा।

---

### तरीका 2: GitHub + Vercel Dashboard से

1. **GitHub पर Code Upload करें:**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin YOUR_GITHUB_REPO_URL
   git push -u origin main
   ```

2. **Vercel Dashboard में:**
   - https://vercel.com पर जाएं
   - "New Project" click करें
   - अपना GitHub repo select करें
   - "Environment Variables" में add करें:
     - Name: `JWT_SECRET`
     - Value: `your-secret-key-12345`
   - "Deploy" button click करें

3. **5-10 मिनट में deploy हो जाएगा!**

---

## ⚙️ Post-Deployment Setup

### 1. First Time Access:
- अपने Vercel URL पर जाएं (जैसे: https://your-app.vercel.app)
- "SIGN UP" पर click करें
- Username और Password बनाएं
- Login करें

### 2. Configuration:
- Dashboard में जाएं
- Chat ID, Cookies, और Messages configure करें
- "SAVE CONFIGURATION" click करें

### 3. Start Automation:
- "AUTOMATION CONTROL" tab पर जाएं
- "START AUTOMATION" click करें
- Logs monitor करें

---

## 🔑 Important Environment Variables

Vercel में ये environment variables जरूर set करें:

```
JWT_SECRET=your-very-secret-random-key-here
NODE_ENV=production
```

---

## 📱 Mobile से Access

आपका deployed app mobile से भी काम करेगा! बस browser में URL खोलें।

---

## 🛠️ Debugging

अगर कोई problem हो:

1. **Vercel Dashboard Logs देखें:**
   - Dashboard → Your Project → Deployments
   - Latest deployment click करें
   - "Function Logs" tab देखें

2. **Environment Variables Check करें:**
   - Settings → Environment Variables
   - JWT_SECRET है या नहीं check करें

3. **Re-deploy करें:**
   ```bash
   vercel --prod --force
   ```

---

## ⏰ 24/7 Operation Notes

- Vercel Free tier पर serverless functions 10 seconds max run होते हैं
- Automation auto-restart होगा जब user login करेगा
- Continuous operation के लिए Vercel Pro consider करें
- या फिर VPS पर deploy करें (Railway, Render, etc.)

---

## 🎯 Success!

अगर सब कुछ ठीक से setup हुआ तो:
- ✅ App live होगा vercel URL पर
- ✅ Login/Signup काम करेगा
- ✅ Configuration save होगा
- ✅ Automation start होगा
- ✅ Messages send होंगे

**Enjoy! 🚀**
