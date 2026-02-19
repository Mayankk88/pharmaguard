# 🚀 Deploy PharmaGuard in 5 Minutes

Get your single runnable link!

---

## 🎯 Fastest Method: Deploy to Render + Vercel

### Step 1: Deploy Backend to Render (2 minutes)

1. **Go to:** https://render.com
2. **Sign up** with GitHub
3. **Click:** "New +" → "Web Service"
4. **Connect** your GitHub repository: `Mayankk88/pharmaguard`
5. **Configure:**
   - Name: `pharmaguard-backend`
   - Root Directory: `backend`
   - Build Command: `pip install -r requirements.txt`
   - Start Command: `gunicorn app:app`
6. **Add Environment Variable:**
   - Key: `OPENAI_API_KEY`
   - Value: `your_openai_api_key`
7. **Click:** "Create Web Service"

**Wait 2-3 minutes...** You'll get a URL like:
```
https://pharmaguard-backend.onrender.com
```

---

### Step 2: Update Frontend with Backend URL

Edit `pharmaguard_amazing.html` line 8:
```javascript
const API_URL = 'https://pharmaguard-backend.onrender.com';
```

---

### Step 3: Deploy Frontend to Vercel (1 minute)

**Option A: Using Vercel CLI**
```bash
npm install -g vercel
cd pharmaguard
vercel --prod
```

**Option B: Using Vercel Website**
1. Go to: https://vercel.com
2. Sign up with GitHub
3. Click "Add New" → "Project"
4. Import `Mayankk88/pharmaguard`
5. Click "Deploy"

**You'll get a URL like:**
```
https://pharmaguard.vercel.app
```

---

## ✅ Your Single Runnable Link

**Frontend:** https://pharmaguard.vercel.app
**Backend API:** https://pharmaguard-backend.onrender.com

Share the frontend link - that's your single runnable URL! 🎉

---

## 🔥 Even Faster: Deploy Static HTML Only

If you just want the HTML file online:

### Option 1: Netlify Drop
1. Go to: https://app.netlify.com/drop
2. Drag `pharmaguard_amazing.html` 
3. Get instant link!

### Option 2: GitHub Pages
```bash
cd pharmaguard
git checkout -b gh-pages
git add pharmaguard_amazing.html
git commit -m "Deploy to GitHub Pages"
git push origin gh-pages
```

**Your link:** https://mayankk88.github.io/pharmaguard/pharmaguard_amazing.html

---

## 🎯 Recommended: Full Deployment

For RIFT 2026 submission, use:
- **Backend:** Render (free tier)
- **Frontend:** Vercel (free tier)

Total time: 5 minutes
Total cost: $0

---

## 🆘 Need Help?

Run this command to test locally first:
```bash
cd pharmaguard
python test_complete.py
```

If tests pass, you're ready to deploy!
