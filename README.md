# M Chidanand — Portfolio

A single-file static site (`index.html`) — no build step, deploys to Vercel as-is.

## What's included (ready to deploy)
- `index.html` — the full site (HTML/CSS/JS in one file), content pulled directly from the resume
- `assets/profile.jpeg` — your real profile photo (already added)
- `assets/resume.pdf` — your real resume PDF (already added, used by every "Download Resume" button)
- `vercel.json` — clean URLs config
- `README.md` — this file

Nothing left to swap in — this folder is deploy-ready as is.

## Preview locally
Just double-click `index.html` to open it in a browser. No server needed.

## Deploy to Vercel (2 minutes)

**Option A — Vercel CLI**
```bash
npm i -g vercel
cd portfolio
vercel
```
Follow the prompts (link/create a project, accept defaults — it's a static site, no framework to select). Then `vercel --prod` to push to production.

**Option B — GitHub + Vercel dashboard**
1. Push this folder to a new GitHub repo.
2. Go to vercel.com → New Project → Import the repo.
3. Framework preset: "Other" (static). No build command needed. Deploy.

Either way you'll get a live `*.vercel.app` URL immediately, and you can attach a custom domain afterward in the Vercel dashboard.

## Content sections
Hero · Stats · About · Experience (Associate Software Engineer + Software Engineer Intern, both at Dedalus Healthcare) · Education · Skills (core proficiency + categorized by domain) · Projects (Personal Portfolio, FitPro) · Certifications · IEEE Publication · Achievements (Recognition & Reward Award, DNA Core Award Nominee) · Contact (email, phone, location) · Footer

## Notes
- **Achievement photos**: drop your award photos into `assets/` with these exact filenames and they'll appear automatically: `award-recognition-reward.jpg` (Recognition & Reward Award), `award-dna-core-2024.jpg` and `award-dna-core-2025.jpg` (DNA Core Award, one per year). Until you add them, a fallback emoji icon shows instead — so the section never looks broken either way.
- Dark/light theme toggle (top-right moon/sun icon) — preference is remembered via `localStorage` and respects the visitor's OS setting on first visit.
- Pulse-line scroll progress bar, animated ECG monitor in the hero, count-up stats, scroll-reveals, and animated skill bars — all vanilla JS, no framework dependencies beyond Google Fonts + Font Awesome (loaded via CDN).
- Fully responsive, respects `prefers-reduced-motion`.
- Contact form opens the visitor's email client via `mailto:` (no backend) — swap in Formspree/EmailJS later if you want it to submit silently instead.
- If you ever want to update your photo or resume, just replace `assets/profile.jpeg` or `assets/resume.pdf` with a same-named file and redeploy.
