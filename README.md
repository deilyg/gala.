# Gala — Travel Social

A GitHub-ready responsive travel social website starter with real authentication, PostgreSQL database, and media storage using Supabase, deployed from GitHub Actions to GitHub Pages.

## Important architecture
GitHub is the **source-code repository and deployment host for the frontend**. GitHub is **not** the application's database. Supabase provides Auth + PostgreSQL + Storage. This keeps the site persistent and allows real user accounts and uploaded media.

## 1. Create the Supabase project
1. Go to https://supabase.com and create a project.
2. Open **SQL Editor** and run `supabase/schema.sql`.
3. Open **Project Settings → API** and copy the Project URL and anon/publishable key.
4. In **Authentication → URL Configuration**, later add your GitHub Pages URL.

## 2. Test locally
Install Node.js 20+.

```bash
npm install
cp .env.example .env.local
```

Put your Supabase values in `.env.local`, then:

```bash
npm run dev
```

Open the localhost URL shown by Vite.

## 3. Create the GitHub repository
On GitHub, create a new empty repository named `gala-travel-social`.

Then in this folder:

```bash
git init
git add .
git commit -m "Initial Gala working social website"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/gala-travel-social.git
git push -u origin main
```

## 4. Add GitHub Actions secrets
In GitHub: **Repository → Settings → Secrets and variables → Actions → New repository secret**.

Create:
- `VITE_SUPABASE_URL`
- `VITE_SUPABASE_ANON_KEY`

Use the values from Supabase. Never put a Supabase service-role key in frontend code or GitHub Actions secrets used for the browser build.

## 5. Enable GitHub Pages
Go to **Settings → Pages**.
- Source: **GitHub Actions**

Pushes to `main` will build and deploy the frontend automatically.

## 6. Set Supabase redirect URLs
After GitHub Pages gives you the site URL, add it under:
**Supabase → Authentication → URL Configuration → Redirect URLs**.

Also set the Site URL to the GitHub Pages URL.

## Current working features
- Sign up
- Sign in
- Persistent user accounts
- Profiles
- PostgreSQL-backed posts
- Image/video upload to Supabase Storage
- Public feed
- Likes table
- Comments table
- Follow table
- Responsive mobile/desktop layout
- GitHub Actions deployment

## Next production modules
Places/PostGIS, map provider, comments UI, follow UI, notifications, Travelers Hub, Trips, Journeys, Memories, Groups, moderation/admin, search, recommendations, and mobile apps can be added on top of this foundation.
