# FutureLabs.io SRL - GitHub Pages Site

## About

FutureLabs.io SRL is a forward-thinking technology company specializing in data science, artificial intelligence, and exceptional product design. We craft innovative solutions that bridge the gap between cutting-edge technology and real-world applications, delivering products that are not only technically excellent but also user-centric and impactful.

## Local Development

To serve this site locally for development and testing:

### Using Python 3
```bash
# Navigate to the project directory
cd futurelabs-io.github.io

# Start a local HTTP server
python3 -m http.server 8000

# Open your browser and visit:
# http://localhost:8000
```

### Using Python 2 (if needed)
```bash
python -m SimpleHTTPServer 8000
```

### Using Node.js (alternative)
```bash
# Install a simple HTTP server globally
npm install -g http-server

# Start the server
http-server

# Or serve on a specific port
http-server -p 8000
```

## GitHub Pages Setup

### Repository Configuration

1. **Make the repository public**: GitHub Pages requires public repositories for free accounts
2. **Go to Settings → Pages** in your GitHub repository
3. **Source**: Select "Deploy from a branch"
4. **Branch**: Choose `main` (or `master` if using the old default)
5. **Folder**: Select `/ (root)`
6. **Save** the configuration

### Custom Domain Setup

1. **Ensure the `CNAME` file exists** in the repository root (already included)
2. **Wait for initial deployment** to complete
3. **Enable "Enforce HTTPS"** once the GitHub certificate is issued (may take a few minutes)

## Cloudflare DNS Configuration

Since `futurelabs-io.com` is managed through Cloudflare, configure the DNS records as follows:

### Initial Setup (DNS Only Mode)

**Important**: Start with DNS records in "DNS only" mode (grey cloud) until HTTPS is fully active.

1. **Add CNAME records**:
   ```
   Type: CNAME
   Name: @
   Target: futurelabs-io.github.io
   Proxy status: DNS only (grey cloud)
   ```

   ```
   Type: CNAME
   Name: www
   Target: futurelabs-io.github.io
   Proxy status: DNS only (grey cloud)
   ```

2. **Wait for DNS propagation** (usually 5-15 minutes)
3. **Verify GitHub Pages is serving the site** over HTTPS
4. **Enable "Enforce HTTPS"** in GitHub Pages settings

### Optional: Enable Cloudflare Proxy

After GitHub's HTTPS certificate is active and working:

1. **Switch to proxied mode** (orange cloud) in Cloudflare DNS
2. **Set SSL/TLS mode** to "Full (strict)" in Cloudflare SSL/TLS settings
3. **Add Page Rule for www redirect** (optional):
   ```
   URL: www.futurelabs-io.com/*
   Setting: Forwarding URL (301 - Permanent Redirect)
   Destination: https://futurelabs-io.com/$1
   ```

### Email DNS Compatibility

Your existing iCloud+ custom email DNS records (MX, TXT, CNAME for email) can coexist with these web hosting records. The email functionality will not be affected.

## Branding TODOs

### High Priority
- [ ] **Replace `favicon.ico`**: Create a proper 32x32 pixel icon file
- [ ] **Replace `og-image.png`**: Design a 1200x630 pixel social media image with FutureLabs.io branding

### Future Enhancements
- [ ] Add company logo and refined color scheme
- [ ] Implement dark mode support
- [ ] Add animation and micro-interactions
- [ ] Create additional pages (about, services, contact)
- [ ] Implement analytics tracking
- [ ] Add structured data markup for SEO

## Code Quality & Validation

### HTML Validation
- Validate HTML using [W3C Markup Validator](https://validator.w3.org/)
- Ensure semantic HTML5 structure is maintained

### Performance Testing
- Run [Google Lighthouse](https://developers.google.com/web/tools/lighthouse) audit
- Target scores: Performance >90, Accessibility >95, Best Practices >90, SEO >90

### Accessibility
- Color contrast ratios meet WCAG AA standards
- Focus indicators are visible and accessible
- Screen reader compatibility maintained
- Keyboard navigation support

## License

This project is released under the MIT License or may remain unspecified as per company policy.

---

## Quick Setup Commands

Use these commands to initialize the repository and deploy to GitHub Pages:

```bash
# From an empty folder named futurelabs-io.github.io
git init
git branch -M main
git add .
git commit -m "Initial: minimal GitHub Pages for futurelabs-io.com"
git remote add origin git@github.com:futurelabs-io/futurelabs-io.github.io.git
git push -u origin main
```

### After pushing to GitHub:

1. Wait 2-3 minutes for GitHub Pages to build
2. Check the Actions tab for deployment status
3. Visit `https://futurelabs-io.github.io` to verify the site
4. Once working, the custom domain `https://futurelabs-io.com` should be available
5. Enable "Enforce HTTPS" in repository Settings → Pages

### Troubleshooting

- **Site not loading**: Check GitHub Actions for build errors
- **Custom domain not working**: Verify DNS propagation with `dig futurelabs-io.com`
- **HTTPS errors**: Wait for GitHub certificate issuance (can take up to 24 hours)
- **404 errors**: Ensure all file paths use absolute paths starting with `/`

For support, contact [vlad@futurelabs-io.com](mailto:vlad@futurelabs-io.com).