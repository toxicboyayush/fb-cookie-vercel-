# 🦂 YKTI RAWAT - Premium Facebook Automation System

Professional Facebook E2EE Automation System with Next.js and Playwright, optimized for 24/7 deployment on Vercel.

## ✨ Features

- 🔐 **Secure Authentication** - JWT-based user authentication
- 🍪 **Flexible Cookie Management** - Single or multiple cookie support
- 📁 **File Upload Support** - Upload message.txt and cookie.txt files
- 🎨 **Premium UI/UX** - Modern, professional design with gradient effects
- 🚀 **24/7 Automation** - Continuous operation on Vercel
- 📊 **Live Console Logs** - Real-time monitoring
- 💾 **SQLite Database** - Persistent data storage
- 🔄 **Auto-restart** - Automation resumes on server restart

## 🚀 Quick Start

### Prerequisites

- Node.js 18+ installed
- A Vercel account (free tier works)
- Facebook account cookies

### Installation

1. **Extract the project files**
   ```bash
   cd facebook-automation-nextjs
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   ```bash
   cp .env.example .env.local
   ```
   Edit `.env.local` and set your JWT_SECRET:
   ```
   JWT_SECRET=your-random-secret-key-here
   ```

4. **Run development server**
   ```bash
   npm run dev
   ```
   Open [http://localhost:3000](http://localhost:3000)

## 📦 Deployment to Vercel

### Option 1: Deploy via Vercel CLI (Recommended)

1. **Install Vercel CLI**
   ```bash
   npm install -g vercel
   ```

2. **Login to Vercel**
   ```bash
   vercel login
   ```

3. **Deploy**
   ```bash
   vercel
   ```
   Follow the prompts. For production:
   ```bash
   vercel --prod
   ```

4. **Set Environment Variables in Vercel**
   ```bash
   vercel env add JWT_SECRET production
   ```
   Enter a strong random secret key when prompted.

### Option 2: Deploy via Vercel Dashboard

1. Push your code to GitHub
2. Go to [vercel.com](https://vercel.com)
3. Click "New Project"
4. Import your GitHub repository
5. Add environment variable:
   - Name: `JWT_SECRET`
   - Value: Your secret key
6. Click "Deploy"

## 🎯 How to Use

### 1. Create Account
- Visit your deployed URL
- Click "SIGN UP"
- Create username and password
- Click "CREATE ACCOUNT"

### 2. Login
- Enter your credentials
- Click "LOGIN NOW"

### 3. Configure Settings

#### Chat ID
- Go to Facebook Messenger
- Open the conversation you want to automate
- Copy the ID from URL (e.g., `messenger.com/t/1362400298935018`)
- Paste in "CHAT/CONVERSATION E2EE ID" field

#### Cookie Setup

**Single Cookie Mode:**
- Select "SINGLE COOKIE"
- Paste your Facebook cookie directly OR
- Click "OR UPLOAD COOKIE FILE" to upload cookie.txt

**Multiple Cookie Mode:**
- Select "MULTIPLE COOKIES"
- Click "CHOOSE FILE"
- Upload cookies.txt file (one cookie per line)

#### Messages
- Type messages directly (one per line) OR
- Click "UPLOAD MESSAGE FILE" to upload messages.txt

#### Other Settings
- **Name Prefix**: Optional prefix for messages (e.g., [YKTI RAWAT])
- **Delay**: Wait time between messages (in seconds)

### 4. Save Configuration
- Click "💾 SAVE CONFIGURATION"
- Wait for success message

### 5. Start Automation
- Go to "AUTOMATION CONTROL" tab
- Click "▶️ START AUTOMATION"
- Monitor logs in real-time
- To stop: Click "⏹️ STOP AUTOMATION"

## 🍪 Getting Facebook Cookies

### Method 1: Browser Extension (Recommended)
1. Install "EditThisCookie" extension
2. Login to Facebook
3. Click the extension icon
4. Click "Export" (copy all)
5. Paste in application

### Method 2: Browser DevTools
1. Login to Facebook
2. Press F12 (Open DevTools)
3. Go to "Application" tab
4. Click "Cookies" → "https://www.facebook.com"
5. Copy all cookie values

## 🔧 Configuration Files

- `package.json` - Dependencies and scripts
- `next.config.js` - Next.js configuration
- `tailwind.config.js` - Styling configuration
- `vercel.json` - Vercel deployment settings
- `.env.local` - Local environment variables

## 📂 Project Structure

```
facebook-automation-nextjs/
├── app/
│   ├── api/              # API routes
│   │   ├── auth/         # Authentication endpoints
│   │   ├── user/         # User config endpoints
│   │   └── automation/   # Automation control
│   ├── dashboard/        # Dashboard page
│   ├── login/            # Login page
│   ├── globals.css       # Global styles
│   ├── layout.tsx        # Root layout
│   └── page.tsx          # Home page
├── lib/
│   ├── auth.ts           # JWT authentication
│   ├── database.ts       # SQLite operations
│   └── automation.ts     # Facebook automation logic
├── public/               # Static files
├── .env.local            # Environment variables
├── package.json          # Dependencies
└── README.md             # This file
```

## 🛡️ Security Features

- 🔐 Password hashing with bcrypt
- 🔑 JWT token authentication
- 🍪 Secure cookie storage
- 🚫 SQL injection protection
- 🔒 HTTPS on Vercel deployment

## ⚡ Performance Optimization

- Server-side rendering for fast load times
- Efficient database queries
- Optimized bundle size
- Edge runtime on Vercel
- Automatic caching

## 🐛 Troubleshooting

### Automation stops after some time
- This is normal on free Vercel tier (serverless functions have time limits)
- Automation will auto-resume when server restarts
- For 24/7 operation, consider Vercel Pro plan

### "Unauthorized" errors
- Clear browser cookies
- Re-login to the application
- Check if JWT_SECRET is set correctly

### Database errors
- Delete `data/automation.db` file
- Restart the application
- Database will be recreated automatically

### Cookie issues
- Make sure cookies are fresh (login to Facebook before copying)
- Check cookie format (should be valid JSON or cookie string)
- Try using incognito mode cookies

## 📊 Monitoring

- View live logs in "AUTOMATION CONTROL" tab
- Check "MESSAGES SENT" counter
- Monitor "STATUS" indicator (🟢 RUNNING / 🔴 STOPPED)

## 🔄 Updates

To update the application:
```bash
git pull origin main
npm install
vercel --prod
```

## 💡 Tips

1. Use strong passwords for your account
2. Keep Facebook cookies fresh (re-login periodically)
3. Don't set delay too low (risk of Facebook rate limiting)
4. Test with one message first before bulk sending
5. Monitor logs regularly for any errors

## 📝 License

This project is for educational purposes only. Use responsibly and in accordance with Facebook's Terms of Service.

## 👨‍💻 Developer

**YKTI RAWAT**
- Made with ❤️ in 2026

## 🆘 Support

For issues or questions:
1. Check this README first
2. Review the troubleshooting section
3. Check Vercel deployment logs
4. Ensure all environment variables are set

## 🎉 Features Included

✅ Single & Multiple Cookie Support
✅ File Upload for Messages
✅ File Upload for Cookies
✅ Premium Professional Design
✅ Real-time Console Logs
✅ Auto-save Configuration
✅ Secure Authentication
✅ 24/7 Ready for Vercel
✅ Responsive Design
✅ User Dashboard
✅ Live Status Monitoring

---

**Enjoy your premium Facebook automation system! 🚀**
