# Comox Mechanical Website

This repository contains the website for Comox Mechanical, a plumbing service company in Courtenay, BC.

## Custom Domain Setup

This site is configured to use a custom domain with GitHub Pages. To complete the custom domain setup:

### 1. Update CNAME File (if needed)
The `CNAME` file in the root directory contains your custom domain. Current domain: `www.comoxmechanical.com`

If you need to change the domain, edit the CNAME file to contain only your domain name (e.g., `www.yourdomain.com` or `yourdomain.com`).

### 2. Configure DNS Records

You need to configure DNS records with your domain provider. There are two options:

#### Option A: Using a subdomain (www.comoxmechanical.com) - RECOMMENDED
Add a CNAME record:
- **Type**: CNAME
- **Host/Name**: www
- **Value/Points to**: macneilconor51-dev.github.io
- **TTL**: 3600 (or default)

#### Option B: Using an apex domain (comoxmechanical.com)
Add A records pointing to GitHub Pages IP addresses:
- **Type**: A
- **Host/Name**: @ (or leave blank)
- **Value**: Add all four IPs:
  - 185.199.108.153
  - 185.199.109.153
  - 185.199.110.153
  - 185.199.111.153
- **TTL**: 3600 (or default)

Also add a www CNAME record:
- **Type**: CNAME
- **Host/Name**: www
- **Value**: macneilconor51-dev.github.io

### 3. Enable GitHub Pages

1. Go to your repository on GitHub: https://github.com/macneilconor51-dev/comox_mechanical
2. Click on **Settings** (gear icon)
3. Scroll down to **Pages** in the left sidebar
4. Under **Source**, select the branch you want to deploy (usually `main` or `master`)
5. Leave the folder as `/ (root)`
6. Click **Save**
7. The custom domain should be automatically detected from the CNAME file
8. Enable **Enforce HTTPS** once the certificate is ready (may take a few minutes)

### 4. Wait for DNS Propagation

DNS changes can take anywhere from a few minutes to 48 hours to propagate worldwide. You can check the status using:
- https://www.whatsmydns.net/
- `dig www.comoxmechanical.com` or `nslookup www.comoxmechanical.com`

### 5. Verify Custom Domain

Once DNS has propagated and GitHub Pages is configured:
1. Visit your custom domain (e.g., https://www.comoxmechanical.com)
2. You should see your website
3. GitHub will automatically provision an SSL certificate for HTTPS

## Troubleshooting

### "Domain's DNS record could not be retrieved"
- Wait a few minutes and try again
- Verify your DNS records are correct
- DNS propagation may take up to 48 hours

### "CNAME already taken"
- The domain is already being used by another GitHub Pages site
- Make sure you own the domain
- Contact GitHub Support if you believe this is an error

### Site shows 404 error
- Make sure GitHub Pages is enabled in repository settings
- Verify the source branch is correct
- Ensure `index.html` is in the root directory (it is!)

### Certificate provisioning fails
- This can take a few minutes to an hour
- Disable and re-enable the custom domain in GitHub Pages settings
- Make sure DNS is properly configured

## Local Development

To view the site locally, simply open `index.html` in a web browser, or use a local web server:

```bash
# Using Python 3
python3 -m http.server 8000

# Using Python 2
python -m SimpleHTTPServer 8000

# Using Node.js (if you have http-server installed)
npx http-server
```

Then visit http://localhost:8000 in your browser.

## File Structure

- `index.html` - Homepage
- `services.html` - Services overview
- `service-*.html` - Individual service pages
- `book.html` - Booking/estimate page
- `contact-us.html` - Contact form
- `Images/` - Image assets
- `*.png` - Logo and branding images
- `CNAME` - Custom domain configuration for GitHub Pages

## Contact

For website issues or questions, contact macneilconor51@gmail.com
