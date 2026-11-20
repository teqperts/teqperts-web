# Teqperts Web (teqperts.in)

Official static website for **Teqperts** with a dedicated showcase and APK distribution page for **Cellventory**.

## 🌐 Structure

- **`/` (`index.html`)**: Teqperts parent website covering engineering services, software solutions, and featured product spotlights.
- **`/cellventory` (`cellventory/index.html`)**: Dedicated product landing page for Cellventory (features, offline SQLite architecture, IMEI scanner preview, FAQ, and Android APK download links).
- **`CNAME`**: Configured for `teqperts.in`.
- **`assets/images/`**: High-resolution logos (`teqperts-logo.png`), app icons (`cellventory-icon.png`), and favicons.

## 🚀 Local Preview

You can preview the site locally using any static web server:

```bash
# Using Python built-in server:
python3 -m http.server 8000

# Or using npx serve:
npx serve .
```

Open `http://localhost:8000` to view the Teqperts site, and `http://localhost:8000/cellventory/` for Cellventory.

## 📦 Deployment to Custom Domain (`teqperts.in`)

### Option A: Cloudflare Pages (Recommended - Free & Fast)
1. Push this repository to GitHub (e.g. `github.com/prashantchaudhary/teqperts-web`).
2. Go to [Cloudflare Dashboard](https://dash.cloudflare.com/) → **Workers & Pages** → **Create application** → **Pages** → **Connect to Git**.
3. Select `teqperts-web`. Build settings:
   - Framework preset: **None**
   - Build command: *(leave empty)*
   - Build output directory: `.` (or root)
4. Under **Custom domains**, add `teqperts.in` and `www.teqperts.in`. Cloudflare will automatically provision SSL.

### Option B: GitHub Pages
1. Push this repository to GitHub.
2. In repo **Settings** → **Pages**:
   - Source: **Deploy from a branch** (`main` / root `/`).
   - Custom domain: `teqperts.in`.
3. Update DNS records at your domain registrar:
   - Apex `A` records pointing to GitHub Pages IPs:
     - `185.199.108.153`
     - `185.199.109.153`
     - `185.199.110.153`
     - `185.199.111.153`
   - CNAME `www` pointing to `<your-username>.github.io`.
