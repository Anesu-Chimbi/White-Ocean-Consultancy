# 🌐 Domain & Professional Email Setup Guide

## Step 1: Buy Your Domain

### Recommended Registrars

**Namecheap** (Most Popular)
- URL: https://www.namecheap.com
- ✅ Cheap pricing ($8-12/year)
- ✅ Free WHOIS protection
- ✅ Easy DNS management
- ✅ Good customer support

**GoDaddy**
- URL: https://www.godaddy.com
- ✅ Large selection of TLDs
- ✅ Email hosting included
- ⚠️ Can be expensive
- ⚠️ More upsells

**Google Domains**
- URL: https://domains.google
- ✅ Simple interface
- ✅ Integrated with Google services
- ✅ Competitive pricing

**Others**
- Bluehost.com
- HostGator.com
- 1&1 IONOS

### Domain Name Ideas
- whiteocean.com (Best)
- whiteocean.co.zw (Local)
- whiteoceanhrs.com (Descriptive)
- oceanconsulting.com (Alternative)

### Domain TLDs to Consider
- **.com** - Most recognized worldwide
- **.co.zw** - Zimbabwe specific
- **.biz** - Business focus
- **.services** - Industry specific

---

## Step 2: Connect Domain to GitHub Pages

### After Purchasing Domain

1. **Log in to your registrar** (Namecheap, GoDaddy, etc.)
2. **Go to DNS Management** for your domain
3. **Add these DNS records:**

#### Option A: Apex Domain (whiteocean.com)

Add these A records:
```
Type: A
Name: @
Points to: 185.199.108.153

Type: A
Name: @
Points to: 185.199.109.153

Type: A
Name: @
Points to: 185.199.110.153

Type: A
Name: @
Points to: 185.199.111.153
```

#### Option B: WWW Subdomain (www.whiteocean.com)

Add this CNAME record:
```
Type: CNAME
Name: www
Points to: yourusername.github.io
```

#### Option C: Both (Recommended)

Apex domain + WWW subdomain setup.

### Update GitHub

1. Go to GitHub repository
2. **Settings** → **Pages**
3. Under "Custom domain", enter: `whiteocean.com`
4. Check "Enforce HTTPS"
5. Click Save

### Wait for SSL Certificate
- Can take 1-48 hours
- GitHub will automatically provision certificate
- You'll get an email when ready

---

## Step 3: Set Up Professional Email

### Option 1: Namecheap Email (Easiest)

1. Log in to Namecheap
2. Go to your domain
3. Click **Email**
4. Click **Activate Email Hosting**
5. Choose plan:
   - Business Basic: $0.88/month per mailbox (Recommended)
   - Business Pro: $1.48/month per mailbox

**Create email addresses:**
```
info@whiteocean.com
contact@whiteocean.com
hello@whiteocean.com
```

**Access email:**
- Webmail: mail.namecheap.com
- Outlook/Gmail: Forward to your personal email

### Option 2: Gmail for Business (Google Workspace)

1. Go to https://workspace.google.com
2. Click **Start free trial**
3. Enter your domain
4. Follow setup wizard
5. Create email addresses

**Pricing:**
- Business Starter: $6/user/month
- Business Standard: $12/user/month
- Business Plus: $18/user/month

**Features:**
- Professional Gmail
- Google Drive
- Google Meet
- Calendar
- Docs

### Option 3: Forward to Personal Email (Free)

Most registrars allow free email forwarding:

1. Log in to registrar
2. Go to Email settings
3. Set up forwarding:
   ```
   info@whiteocean.com → your-email@gmail.com
   ```

**Advantages:**
- Free
- Simple setup
- No extra accounts

**Disadvantages:**
- Can't reply with custom email
- Limited functionality

---

## Step 4: Create Email Addresses

### Suggested Email Structure

**Professional Contacts:**
- `info@whiteocean.com` - General inquiries
- `contact@whiteocean.com` - Alternative
- `hello@whiteocean.com` - Friendly approach

**Team Specific:**
- `hr@whiteocean.com` - HR inquiries
- `recruitment@whiteocean.com` - Job inquiries
- `support@whiteocean.com` - Support

**Individual:**
- `john@whiteocean.com` - Individual consultant
- `admin@whiteocean.com` - Administrator

---

## Step 5: Add Contact Form to Website

### Using Formspree (Easiest - Free)

1. Go to https://formspree.io
2. Sign up
3. Create new form
4. Enter email: `info@whiteocean.com`
5. Get form endpoint: `https://formspree.io/f/YOUR_ID`

**Add to index.html:**
```html
<section id="contact">
    <div class="container">
        <h2>Contact Us</h2>
        <form action="https://formspree.io/f/YOUR_ID" method="POST">
            <input type="text" name="name" placeholder="Your Name" required>
            <input type="email" name="email" placeholder="Your Email" required>
            <textarea name="message" placeholder="Your Message" required></textarea>
            <button type="submit" class="btn-primary">Send Message</button>
        </form>
    </div>
</section>
```

### Using Getform (Alternative - Free)

1. Go to https://getform.io
2. Sign up
3. Create form for: `info@whiteocean.com`
4. Copy endpoint
5. Add same HTML as above with your endpoint

---

## Step 6: Email Signature Template

**For Professional Emails:**

```
---
White Ocean Consultancy
Strategic HR Solutions Partner

[Your Name]
[Your Title]

📧 info@whiteocean.com
📱 +263 XXXX XXX XXX
🌍 www.whiteocean.com
📍 Harare, Zimbabwe

Transforming organizations through human capital excellence
---
```

---

## Domain Checklist

- [ ] Domain purchased
- [ ] DNS records added (A or CNAME)
- [ ] GitHub Pages custom domain set
- [ ] SSL certificate issued
- [ ] Domain working (test it!)
- [ ] Email hosting set up
- [ ] Email addresses created
- [ ] Email forwarding configured
- [ ] Contact form added to website
- [ ] Email signature created

---

## Testing Your Setup

### Test Domain
1. Open browser
2. Go to: `www.whiteocean.com`
3. Should see your website ✅

### Test Email
1. Send test email to: `info@whiteocean.com`
2. Check if it arrives ✅

### Test Contact Form
1. Fill contact form on website
2. Check if email received ✅

---

## Common Issues & Solutions

### Domain Not Working
❌ **Problem:** Site not loading after 2 hours
✅ **Solution:** 
- DNS propagation can take 24-48 hours
- Check DNS records are correct
- Hard refresh: Ctrl+Shift+R

### Emails Not Receiving
❌ **Problem:** Contact form submissions not arriving
✅ **Solution:**
- Check email forwarding is enabled
- Check spam/junk folder
- Verify email address in form is correct
- Test with personal email first

### HTTPS Not Working
❌ **Problem:** Certificate error
✅ **Solution:**
- Wait 1-2 hours (automatic)
- Check "Enforce HTTPS" in GitHub
- Try incognito mode
- Clear browser cache

---

## Annual Renewal Reminders

**Set Calendar Reminders for:**
- Domain renewal date (usually 12 months)
- Email hosting renewal
- Any service subscriptions

**Enable auto-renewal** in registrar to avoid downtime.

---

## Upgrade Path (Later)

As business grows:
- ✅ Add more email addresses
- ✅ Set up Google Workspace for team
- ✅ Upgrade hosting (future)
- ✅ Add custom CRM/forms
- ✅ Blog platform

---

## Cost Breakdown

**Typical Annual Costs:**

| Item | Cost | Frequency |
|------|------|-----------|
| Domain (.com) | $10-15 | Yearly |
| Email Hosting | $0-50/year | Yearly |
| **Total** | **$10-65** | **Per Year** |

*All hosting is free via GitHub Pages*

---

## Next Steps

1. ✅ Choose domain registrar
2. ✅ Purchase domain
3. ✅ Connect to GitHub
4. ✅ Set up email
5. ✅ Add contact form
6. ✅ Test everything

---

## Support Resources

- **Namecheap Help:** https://namecheap.com/support
- **GoDaddy Support:** https://support.godaddy.com
- **GitHub Pages DNS:** https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site
- **Formspree Help:** https://formspree.io/help

---

**Congratulations! Your professional online presence is coming together! 🎉**

For questions about domain or email setup, contact your registrar's support team.
