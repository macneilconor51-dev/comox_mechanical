# Custom Domain Setup - Next Steps

## What Was Fixed

Your website could not use a custom domain because GitHub Pages requires website files to be in the repository root (or a `docs` folder), but your files were in a subdirectory called "Comox Mechanical Website".

### Changes Made:

1. ✅ **Moved all website files to the repository root**
   - All HTML files, images, and assets are now in the correct location for GitHub Pages
   - All relative paths remain unchanged and functional

2. ✅ **Created CNAME file**
   - Added `CNAME` file with your custom domain: `www.comoxmechanical.com`
   - This tells GitHub Pages which domain to use

3. ✅ **Fixed HTML issues**
   - Added `mailto:` protocol to email links for proper email client handling
   - Corrected company name in footer from "Irish Plumbing" to "Comox Mechanical"

4. ✅ **Created comprehensive documentation**
   - Added `README.md` with detailed setup instructions
   - Included DNS configuration steps
   - Added troubleshooting guide

## What You Need to Do Now

To complete the custom domain setup, follow these steps:

### 1. Configure GitHub Pages (Required)

1. Go to https://github.com/macneilconor51-dev/comox_mechanical/settings/pages
2. Under **Source**, select your branch (usually `main` or `copilot/debug-custom-domain-issue`)
3. Leave the folder as `/ (root)`
4. Click **Save**
5. The custom domain should be automatically detected from the CNAME file
6. Wait a few minutes for deployment

### 2. Configure DNS Records at Your Domain Provider (Required)

You need to add DNS records for your domain `comoxmechanical.com`:

**Option A: Use a subdomain (www.comoxmechanical.com) - RECOMMENDED**

Add one CNAME record:
- Type: `CNAME`
- Host/Name: `www`
- Value/Points to: `macneilconor51-dev.github.io`
- TTL: `3600` (or default)

**Option B: Use apex domain (comoxmechanical.com)**

Add four A records:
- Type: `A`
- Host/Name: `@` (or leave blank)
- Add each of these IP addresses (create 4 separate A records):
  - `185.199.108.153`
  - `185.199.109.153`
  - `185.199.110.153`
  - `185.199.111.153`
- TTL: `3600` (or default)

Also add a www CNAME:
- Type: `CNAME`
- Host/Name: `www`
- Value: `macneilconor51-dev.github.io`

### 3. Wait for DNS Propagation (24-48 hours)

DNS changes can take time to propagate. You can check status at:
- https://www.whatsmydns.net/
- Or use command: `dig www.comoxmechanical.com`

### 4. Enable HTTPS (Recommended)

Once DNS is working and GitHub Pages is enabled:
1. Go back to https://github.com/macneilconor51-dev/comox_mechanical/settings/pages
2. Check the box for **Enforce HTTPS**
3. GitHub will automatically provision a free SSL certificate

## Verification

Once everything is configured:
- Visit https://www.comoxmechanical.com
- Your website should load
- All pages and links should work correctly
- HTTPS should be enabled

## Common Issues

**"Domain's DNS record could not be retrieved"**
- Wait a few hours for DNS propagation
- Verify your DNS records are correct
- Check that you entered the correct values

**"CNAME already taken"**
- The domain is being used by another GitHub Pages site
- Make sure you own the domain
- Remove any existing GitHub Pages CNAME configuration

**Site shows 404 error**
- Verify GitHub Pages is enabled in repository settings
- Make sure you selected the correct branch
- Wait a few minutes for deployment to complete

## Support

If you need help:
1. Check the detailed README.md in the repository
2. Review GitHub Pages documentation: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site
3. Contact your domain registrar for DNS configuration help

---

**Note:** If you want to use a different custom domain, simply edit the `CNAME` file to contain your desired domain (one domain per line, no https://).
