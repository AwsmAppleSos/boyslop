
# One-Click Web Deploy Kit for Expo (GitHub Pages)

**What this does**
- Adds `app.json` with web settings.
- Adds a GitHub Actions workflow that builds your Expo web app (`npx expo export -p web`) and deploys it to GitHub Pages.

**How to use (mobile-friendly)**
1. Upload these files into the **root** of your repository (not inside a folder):
   - `app.json`
   - `.github/workflows/pages.yml`
   - `.nojekyll` (prevents Jekyll from interfering)
2. In your repo → **Settings** → **Pages** → set **Source = GitHub Actions**.
3. Go to **Actions** tab, wait for the workflow to finish (green).
4. Your live URL appears at the end of the Deploy step and under Settings → Pages.

If the build fails with missing packages, the workflow auto-installs `react-dom`, `react-native-web`, and `@expo/metro-runtime`.
