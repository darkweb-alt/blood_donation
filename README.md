# 🩸 Emergency Blood Donor Finder
**Sitaram Clinic, Coimbatore**

## Files
```
blood-donor/
├── app.py              ← Everything: models, routes, logic
├── templates/
│   └── index.html      ← Full UI (no separate JS/CSS files)
├── requirements.txt
├── Procfile            ← For Render / Railway / Heroku
├── render.yaml         ← Auto-deploy config for Render
└── .gitignore
```

## Deploy to Render (Free) — Recommended
1. Push this folder to a GitHub repo
2. Go to [render.com](https://render.com) → New → Web Service
3. Connect your GitHub repo
4. Render auto-detects `render.yaml` — just click **Deploy**
5. Done! Your app is live at `https://your-app.onrender.com`

## Deploy to Railway (Free tier)
1. Push to GitHub
2. Go to [railway.app](https://railway.app) → New Project → Deploy from GitHub
3. Add env var: `JWT_SECRET=your-secret-here`
4. It reads the `Procfile` automatically

## Run Locally
```bash
pip install -r requirements.txt
python app.py
# → http://localhost:5000
```

## Default Admin Login
- Email: `admin@clinic.com`
- Password: `admin123`

## Features
- 🔍 Emergency nearest-donor search (Dijkstra / Haversine)
- 👥 Donor list with search/filter
- ➕ Add / edit / delete donors (admin only)
- 📊 Blood group availability stats
- 🔐 JWT authentication
- 🌱 Auto-seeds 8 sample donors on first run
