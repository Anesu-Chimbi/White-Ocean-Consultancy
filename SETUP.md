# 🚀 Step-by-Step GitHub Pages Deployment Guide

## Prerequisites
- GitHub account (free at github.com)
- Git installed on your computer (optional but recommended)
- The website files (index.html, README.md)

---

## Method 1: Easy Web Upload (No Git Required)

### Step 1️⃣: Create a GitHub Repository
1. Go to [github.com](https://github.com) and log in
2. Click the **+** icon (top right) → **New repository**
3. Fill in the details:
   - **Repository name**: `white-ocean-consultancy`
   - **Description**: Official website for White Ocean Consultancy
   - **Visibility**: PUBLIC (required for free GitHub Pages)
   - **Check**: "Add a README file"
4. Click **Create repository**

### Step 2️⃣: Upload Your Website
1. In your new repository, click **Add file** → **Upload files**
2. Drag and drop `index.html` into the upload area
3. (Optional) Upload README.md and .gitignore too
4. Click **Commit changes**

### Step 3️⃣: Enable GitHub Pages
1. Go to **Settings** (top menu bar)
2. Scroll down to **Pages** section (left sidebar)
3. Under **Source**:
   - Branch: select `main`
   - Folder: select `/ (root)`
4. Click **Save**
5. Wait 1-2 minutes for deployment ⏳

### Step 4️⃣: View Your Website
- Your site is live at: **https://yourusername.github.io/white-ocean-consultancy/**
- Example: https://john-smith.github.io/white-ocean-consultancy/

---

## Method 2: Command Line (Git Required)

### Prerequisites
- Git installed: https://git-scm.com/downloads
- Terminal/Command Prompt access

### Step 1️⃣: Clone the Repository
```bash
git clone https://github.com/yourusername/white-ocean-consultancy.git
cd white-ocean-consultancy
```

### Step 2️⃣: Add Your Files
```bash
# Copy index.html, README.md, .gitignore to this folder

# Check what will be added
git status
```

### Step 3️⃣: Commit and Push
```bash
# Add all files
git add .

# Commit changes
git commit -m "Initial website deployment"

# Push to GitHub
git push origin main
```

### Step 4️⃣: Enable Pages
- Same as Method 1, Step 3

---

## Connecting Your Custom Domain (After Buying)

### Step 1: Buy a Domain
Popular providers:
- [Namecheap](https://www.namecheap.com)
- [GoDaddy](https://www.godaddy.com)
- [Google Domains](https://domains.google)

### Step 2: Update Repository Settings
1. Go to **Settings** → **Pages**
2. Under "Custom domain", enter your domain
3. Click **Save**

### Step 3: Update Domain DNS Settings
Add these DNS records at your domain provider:

**For Apex Domain (example.com):**
```
Type: A
Name: @
Value: 185.199.108.153
       185.199.109.153
       185.199.110.153
       185.199.111.153
```

**For Subdomain (www.example.com):**
```
Type: CNAME
Name: www
Value: yourusername.github.io
```

### Step 4: Wait for SSL Certificate
GitHub will automatically provision an SSL certificate (can take up to 24 hours).

---

## Adding a Contact Form

### Option 1: Formspree (Easiest)
1. Go to [formspree.io](https://formspree.io)
2. Sign up and create new form
3. Add this code to your HTML:

```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
    <input type="email" name="email" placeholder="Your email" required>
    <textarea name="message" placeholder="Your message" required></textarea>
    <button type="submit">Send</button>
</form>
```

### Option 2: Getform
1. Go to [getform.io](https://getform.io)
2. Create account and form
3. Update form action URL in HTML

---

## Adding Google Analytics

1. Go to [analytics.google.com](https://analytics.google.com)
2. Create a new property for your domain
3. Copy the measurement ID
4. Add this before `</head>` in index.html:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-YOUR_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-YOUR_ID');
</script>
```

---

## Updating Your Website

### With Git Command Line:
```bash
# Make changes to index.html

# Check changes
git status

# Add changes
git add index.html

# Commit
git commit -m "Update service description"

# Push
git push origin main
```

### Through GitHub Web Interface:
1. Open `index.html` on GitHub
2. Click the pencil icon (edit)
3. Make your changes
4. Click "Commit changes"
5. Changes live in 1-2 minutes

---

## Troubleshooting

### Site not appearing after upload?
- ✅ Check GitHub Pages is enabled in Settings
- ✅ Wait 2-3 minutes
- ✅ Hard refresh: Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac)

### Custom domain not working?
- ✅ DNS propagation can take 24-48 hours
- ✅ Check DNS records at your provider
- ✅ Verify SSL certificate is issued (Settings → Pages)

### Files not updating?
- ✅ Clear browser cache
- ✅ Check file was actually committed
- ✅ Verify correct branch selected in Pages settings

---

## File Checklist Before Going Live

- [ ] `index.html` - Main website file
- [ ] `README.md` - Documentation
- [ ] `.gitignore` - Git configuration
- [ ] Company information updated (email, phone)
- [ ] All 12 services documented
- [ ] Links work correctly
- [ ] Mobile responsive tested
- [ ] Colors match brand guidelines

---

## Making Further Customizations

### To add more content:
1. Edit `index.html`
2. Find the section you want to modify
3. Update the HTML
4. Commit and push

### To change colors:
```css
:root {
    --primary: #0c447c;           /* Change this */
    --primary-light: #185fa5;      /* And this */
    --accent: #00d4ff;             /* And this */
}
```

### To modify services list:
Find the `<!-- Services Section -->` and add new service categories following the same format.

---

## Performance Tips

✅ **Your site is already optimized:**
- No external dependencies
- Lightweight CSS animations
- Fast loading times
- Automatic GitHub Pages CDN

### Further optimization:
- Minify CSS (use online minifiers)
- Compress images if you add any
- Remove unused CSS (none in current design)

---

## Support & Resources

- [GitHub Pages Docs](https://docs.github.com/en/pages)
- [GitHub Help](https://github.support.com)
- [HTML/CSS Reference](https://developer.mozilla.org)
- [Web Dev Best Practices](https://web.dev)

---

## Next Steps

1. ✅ Upload website to GitHub
2. ✅ Enable GitHub Pages
3. ⏳ Buy a domain
4. ⏳ Connect custom domain
5. ⏳ Add contact form
6. ⏳ Set up analytics
7. ⏳ Create blog section (optional)

---

**You're all set! Your White Ocean Consultancy website is now live! 🚀**

Questions? Reach out to your development team or GitHub support.
