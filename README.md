# AI for Academics — www.aiforacademics.io

> Practical AI training for researchers, PhD students, and academics.

## 🚀 Quick Start (Local Development)

```bash
# Clone the repository
git clone git@github.com:YOUR_USERNAME/aiforacademics.git
cd aiforacademics

# Open in browser (no build step needed — it's a static site)
open index.html
# or on Linux:
xdg-open index.html
# or just drag index.html into your browser
```

## 📁 Project Structure

```
aiforacademics/
├── index.html          # Main website (single-file, self-contained)
├── README.md           # This file
├── CNAME               # Custom domain config for GitHub Pages
├── assets/
│   └── (future: images, PDFs, etc.)
└── .nojekyll           # Tells GitHub Pages not to process with Jekyll
```

## 🌐 Deployment to GitHub Pages

### Step 1: Create GitHub Repository

1. Go to https://github.com/new
2. Repository name: `aiforacademics`
3. Set to **Private** (you can make it public later)
4. Do NOT initialize with README (we already have one)
5. Click "Create repository"

### Step 2: Push Code

```bash
cd /path/to/aiforacademics
git init
git add .
git commit -m "Initial commit: AI for Academics brand website"
git branch -M main
git remote add origin git@github.com:YOUR_USERNAME/aiforacademics.git
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Go to repository Settings → Pages
2. Source: "Deploy from a branch"
3. Branch: `main` / `/ (root)`
4. Click Save
5. Your site will be live at `https://YOUR_USERNAME.github.io/aiforacademics/`

### Step 4: Connect Custom Domain (aiforacademics.io)

1. In your domain registrar (where you bought aiforacademics.io), add these DNS records:

   **Option A: Apex domain (aiforacademics.io)**
   ```
   Type: A     Name: @    Value: 185.199.108.153
   Type: A     Name: @    Value: 185.199.109.153
   Type: A     Name: @    Value: 185.199.110.153
   Type: A     Name: @    Value: 185.199.111.153
   ```

   **Option B: www subdomain**
   ```
   Type: CNAME  Name: www  Value: YOUR_USERNAME.github.io
   ```

   **Recommended: Both (apex + www redirect)**
   Add all A records above PLUS the CNAME for www.

2. In GitHub repo Settings → Pages → Custom domain:
   - Enter: `www.aiforacademics.io`
   - Check "Enforce HTTPS" (wait 15-30 min for certificate)

3. The CNAME file in this repo should contain: `www.aiforacademics.io`

### Step 5: Verify

- Visit https://www.aiforacademics.io — should show your site
- Visit https://aiforacademics.io — should redirect to www version
- HTTPS should work automatically (green padlock)

## 🔧 Integrations To Set Up

### Email Collection (Priority: HIGH)
Replace the `handleSubscribe()` function in index.html with one of:
- **ButtonDown** (free up to 100 subscribers, simple): https://buttondown.email
- **ConvertKit** (free up to 1,000 subscribers, best for creators): https://convertkit.com
- **Mailchimp** (free up to 500 subscribers): https://mailchimp.com

### Payment (Priority: HIGH)
Replace placeholder `href="#"` on buy buttons with:
- **LemonSqueezy** (recommended, handles EU VAT): https://lemonsqueezy.com
  - Create 3 products: Early Bird ($12), Standard ($19), Team ($49)
  - Enable PPP (Purchasing Power Parity) for global pricing
  - Copy checkout URLs into index.html

### Analytics (Priority: MEDIUM)
Add before `</head>`:
- **Plausible** (privacy-friendly, GDPR compliant): https://plausible.io
- OR **Umami** (free, self-hosted): https://umami.is

## 📋 Maintenance Notes

- **Single-file architecture**: Everything is in index.html. No build tools, no npm, no frameworks. Just HTML + CSS + vanilla JS. This is intentional — keeps it simple, fast, and easy to maintain.
- **Fonts**: Loaded from Google Fonts (Instrument Serif, DM Sans, JetBrains Mono)
- **No cookies**: Site uses no cookies or tracking by default
- **Mobile responsive**: Tested for 375px+ screens
- **Performance**: No JavaScript frameworks = fast load times

## 🗓️ Content Update Schedule

| Date | Update |
|------|--------|
| Launch | Products 1 (course) + 4 (workshops) active, Products 2-3 on waitlist |
| Summer 2026 | Launch PhD Compass (Product 2), update badges |
| Autumn 2026 | Launch AI-Powered Research Lab (Product 3), update badges |

## 📧 Contact

- Email: hello@aiforacademics.io
- Business: Kovi Consulting · Org.nr 937 270 208 · Ås, Norway
