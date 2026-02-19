# 🚀 Deploy PharmaGuard Backend to Render

## Step-by-Step Guide (5 Minutes)

### 1️⃣ Go to Render

Open your browser and go to: **https://render.com**

### 2️⃣ Sign Up / Log In

- Click **"Get Started"** or **"Sign In"**
- Choose **"Sign in with GitHub"**
- Authorize Render to access your GitHub account

### 3️⃣ Create New Web Service

1. Click the **"New +"** button (top right)
2. Select **"Web Service"**

### 4️⃣ Connect Your Repository

1. Find and select: **`Mayankk88/pharmaguard`**
   - If you don't see it, click "Configure account" and grant access
2. Click **"Connect"**

### 5️⃣ Configure the Service

Fill in these settings:

**Basic Settings:**
- **Name:** `pharmaguard-backend`
- **Region:** `Oregon (US West)` (or closest to you)
- **Branch:** `main`
- **Root Directory:** `backend`

**Build & Deploy:**
- **Runtime:** `Python 3`
- **Build Command:** `pip install -r requirements.txt`
- **Start Command:** `gunicorn app:app`

**Instance Type:**
- Select **"Free"** (Free tier is perfect for this!)

### 6️⃣ Add Environment Variables

Scroll down to **"Environment Variables"** section:

Click **"Add Environment Variable"** and add:

**Variable 1:**
- **Key:** `OPENAI_API_KEY`
- **Value:** `your_openai_api_key_here` (use the key from your .env file)

**Variable 2:**
- **Key:** `FLASK_ENV`
- **Value:** `production`

**Variable 3:**
- **Key:** `PORT`
- **Value:** `10000`

### 7️⃣ Create Web Service

1. Click **"Create Web Service"** button at the bottom
2. Wait 2-3 minutes for deployment...

You'll see:
```
==> Building...
==> Deploying...
==> Your service is live!
```

### 8️⃣ Get Your Backend URL

Once deployed, you'll see your URL at the top:
```
https://pharmaguard-backend.onrender.com
```

**Copy this URL!** You'll need it for the next step.

### 9️⃣ Test Your Backend

Click on your backend URL and add `/health`:
```
https://pharmaguard-backend.onrender.com/health
```

You should see:
```json
{
  "status": "ok",
  "service": "PharmaGuard API",
  "version": "1.0.0"
}
```

✅ **Backend is live!**

---

## 🔗 Next: Update Frontend

Now that your backend is deployed, update the frontend to use it:

### Option A: Quick Update (Recommended)

I'll help you update the HTML file with the backend URL.

### Option B: Manual Update

1. Edit `pharmaguard_amazing.html`
2. Find line 8: `const API_URL = 'http://127.0.0.1:5000';`
3. Change to: `const API_URL = 'https://pharmaguard-backend.onrender.com';`
4. Save and push to GitHub

---

## 🎉 Final Result

**Frontend:** https://mayankk88.github.io/pharmaguard/  
**Backend:** https://pharmaguard-backend.onrender.com

**Share this link:** https://mayankk88.github.io/pharmaguard/

---

## 🆘 Troubleshooting

**Build Failed?**
- Check that `backend/requirements.txt` exists
- Verify Python version compatibility

**Service Won't Start?**
- Check environment variables are set correctly
- View logs in Render dashboard

**API Not Responding?**
- Wait 1-2 minutes after first deploy (cold start)
- Check logs for errors

---

## 📞 Need Help?

If you see any errors, copy the error message and I'll help you fix it!
