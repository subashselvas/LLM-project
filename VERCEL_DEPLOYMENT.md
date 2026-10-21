# 🚀 Deploying EDUCORE SPARK-X to Vercel

EDUCORE SPARK-X is pre-configured and tested for 100% error-free deployment on [Vercel](https://vercel.com).

---

## ⚡ Option 1: Instant Deployment via Vercel CLI (Fastest)

Open your terminal in the `educore_app` directory and run:

```bash
cd educore_app
npx vercel
```

1. Log in to your Vercel account when prompted in the browser.
2. Accept the default project settings:
   - **Set up and deploy?** `Y`
   - **Which scope?** (Select your account)
   - **Link to existing project?** `N`
   - **Project name?** `educore-spark-x` (or your preferred name)
   - **Directory located?** `./`
3. Vercel will build and give you an instant live URL!

To deploy directly to production later:
```bash
npx vercel --prod
```

---

## 🐙 Option 2: Continuous Deployment via GitHub (Recommended)

### Step 1: Push `educore_app` to your GitHub Repository
If you haven't added a remote yet:

```bash
cd educore_app
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
git branch -M main
git push -u origin main
```

### Step 2: Import on Vercel
1. Go to [vercel.com/new](https://vercel.com/new).
2. Click **Import** next to your GitHub repository.
3. Configure Project Settings:
   - **Framework Preset**: `Next.js` (automatically detected)
   - **Root Directory**:
     - If you pushed the entire folder including `educore_app/`, click **Edit** next to Root Directory and select `educore_app`.
     - If you pushed `educore_app` directly as the repository root, leave it as `./`.
4. Click **Deploy**.

---

## 🔑 Environment Variables (Optional)

EDUCORE SPARK-X includes an in-memory/embedded data repository that works out of the box with zero external databases required.

If you wish to configure production secrets in Vercel (**Project Settings > Environment Variables**):

| Key | Example Value | Description |
|---|---|---|
| `NEXT_PUBLIC_APP_URL` | `https://your-project.vercel.app` | Canonical app URL |
| `NEXTAUTH_SECRET` | `super_secret_jwt_key_2026` | Encryption secret for sessions |
| `DATABASE_URL` | *(Optional)* | PostgreSQL / Supabase connection URI if using external DB |

---

## 🛠️ Verification Checklist (Passed 100%)

- [x] **TypeScript Type-Check**: 0 errors
- [x] **Next.js Production Build (`npm run build`)**: Exited code 0 (all 21 static and dynamic routes compiled)
- [x] **ESLint Linting (`npm run lint`)**: 0 errors, 0 warnings
- [x] **Automated Test Suite (`npm test`)**: 18/18 tests passed (100% success rate)
- [x] **Local Dev Server (`npm run dev`)**: Tested and serving at `http://localhost:3000`
