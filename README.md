# PolaroidMaker iOS - GitHub Pages

## About

**PolaroidMaker iOS** is a sophisticated iOS application developed by **FutureLabs.io SRL** that transforms digital photos into authentic polaroid-style images with custom typography and professional-grade output. This repository hosts the official GitHub Pages website showcasing the app's features, technical specifications, and development resources.

### Key Features

- 📱 **Native iOS Experience**: Built with SwiftUI for iPhone and iPad
- 📐 **Authentic Dimensions**: Mathematically accurate polaroid proportions (10.7cm × 8.8cm)
- ✍️ **Professional Typography**: Dual-line text system with curated fonts
- 🌍 **Smart Location Integration**: Automatic city/country detection from GPS data
- ⚡ **Performance Optimized**: Memory-efficient processing for large photo libraries
- 📤 **High-Quality Export**: 3x text scaling with iOS Share Sheet integration

## Website Development

This GitHub Pages site is built with modern web technologies and follows accessibility standards:

- **HTML5** semantic structure
- **CSS3** with iOS-inspired design system
- **Responsive design** for all device sizes
- **Accessibility compliant** (WCAG AA standards)
- **Performance optimized** for fast loading

## Deployment

### Automatic Deployment

The site automatically deploys via **GitHub Actions** when changes are pushed to the `main` branch:

1. **Build Process**: Validates HTML/CSS, checks links, optimizes assets
2. **Quality Checks**: Ensures all dependencies and assets are present
3. **Deployment**: Publishes to GitHub Pages with SSL
4. **Monitoring**: Reports deployment status and generates sitemap

### Manual Deployment

To deploy manually or test locally:

```bash
# Clone the repository
git clone https://github.com/futurelabs-io/futurelabs-io.github.io.git
cd futurelabs-io.github.io

# Test locally
python3 -m http.server 8000
# Visit http://localhost:8000

# Deploy to GitHub Pages
git add .
git commit -m "Update PolaroidMaker website"
git push origin main
```

## Local Development

### Prerequisites

- **Python 3.x** (for local server)
- **Git** (for version control)
- **Modern browser** (Chrome, Firefox, Safari, Edge)

### Setup Instructions

```bash
# Navigate to the project directory
cd futurelabs-io.github.io

# Start local development server
python3 -m http.server 8000

# Alternative: Using Node.js
npx http-server -p 8000

# Open in browser
open http://localhost:8000
```

### Development Workflow

1. **Edit files** in your preferred editor
2. **Test locally** using the development server
3. **Validate changes** using browser developer tools
4. **Commit and push** to trigger automatic deployment

## Domain Configuration

### Primary Domain Setup

The site is configured to serve from `futurelabs-io.com` with the following setup:

#### GitHub Pages Configuration
- **Source**: Deploy from `main` branch
- **Custom domain**: `futurelabs-io.com`
- **Enforce HTTPS**: Enabled
- **Build**: GitHub Actions (custom workflow)

#### DNS Configuration (Cloudflare)
```
Type: A    | Name: @   | Target: 185.199.108.153 | Proxy: ☁️ Proxied
Type: A    | Name: @   | Target: 185.199.109.153 | Proxy: ☁️ Proxied  
Type: A    | Name: @   | Target: 185.199.110.153 | Proxy: ☁️ Proxied
Type: A    | Name: @   | Target: 185.199.111.153 | Proxy: ☁️ Proxied
Type: CNAME| Name: www | Target: futurelabs-io.com | Proxy: ☁️ Proxied
```

#### SSL/TLS Settings
- **SSL/TLS encryption mode**: Full (strict)
- **Always Use HTTPS**: On
- **HSTS**: Enabled
- **Certificate**: Cloudflare Universal SSL

### Email Compatibility

Email services (iCloud+ custom domain) continue to work alongside the website:

```
Type: MX    | Name: @  | Target: mx01.mail.icloud.com (priority 10)
Type: MX    | Name: @  | Target: mx02.mail.icloud.com (priority 10)  
Type: TXT   | Name: @  | Target: "v=spf1 include:icloud.com ~all"
Type: CNAME | Name: sig1._domainkey | Target: sig1.dkim.[domain].at.icloudmailadmin.com
```

## Performance & SEO

### Optimization Features

- ✅ **Lighthouse Score**: 95+ across all metrics
- ✅ **Mobile-First Design**: Responsive across all devices
- ✅ **Fast Loading**: Optimized CSS and minimal dependencies
- ✅ **SEO Optimized**: Proper meta tags and structured data
- ✅ **Accessibility**: WCAG AA compliant with screen reader support

### Analytics & Monitoring

- **Core Web Vitals**: Monitored via Google Search Console
- **GitHub Actions**: Automated deployment monitoring
- **Uptime**: Monitored via GitHub Pages status
- **Performance**: Lighthouse CI in deployment pipeline

## File Structure

```
futurelabs-io.github.io/
├── index.html              # Main page with PolaroidMaker content
├── css/
│   └── styles.css         # iOS-inspired design system
├── assets/
│   ├── favicon.ico        # Site icon
│   └── og-image.png       # Social media preview image
├── .github/
│   └── workflows/
│       └── deploy.yml     # GitHub Actions deployment
├── robots.txt             # Search engine directives
├── sitemap.xml           # Auto-generated site map
├── CNAME                 # Custom domain configuration
└── README.md             # This file
```

## Contributing

### Development Guidelines

1. **Follow iOS Design Principles**: Use system fonts, native colors, and iOS-style components
2. **Maintain Accessibility**: Ensure keyboard navigation, screen reader compatibility
3. **Test Responsively**: Verify layouts work on mobile, tablet, and desktop
4. **Optimize Performance**: Keep images optimized and CSS efficient

### Making Changes

```bash
# Fork the repository
git fork https://github.com/futurelabs-io/futurelabs-io.github.io.git

# Create a feature branch
git checkout -b feature/your-improvement

# Make your changes and test locally
python3 -m http.server 8000

# Commit with descriptive message
git commit -m "feat: improve mobile navigation accessibility"

# Push and create pull request
git push origin feature/your-improvement
```

### Code Quality Standards

- **HTML**: Semantic, valid HTML5
- **CSS**: Modern CSS3 with custom properties
- **Performance**: Images optimized, CSS minified for production
- **Accessibility**: ARIA labels, keyboard navigation, screen reader support

## Brand Guidelines

### FutureLabs.io SRL Branding

**PolaroidMaker iOS** is developed by **FutureLabs.io SRL**, a technology company specializing in data science, artificial intelligence, and exceptional product design.

#### Brand Elements
- **Company**: FutureLabs.io SRL
- **Product**: PolaroidMaker iOS  
- **Tagline**: "Transform your memories into timeless polaroids"
- **Company Mission**: "Data, AI, and product craftsmanship"

#### Color Palette
```css
--ios-blue: #007AFF     /* Primary brand color */
--ios-orange: #FF9500   /* Secondary accent */
--ios-gray: #8E8E93     /* Neutral text */
--surface: #F5F5F7      /* iOS-style backgrounds */
```

#### Typography
- **Primary**: SF Pro Display (system font)
- **Code**: SF Mono (monospace)
- **Headings**: 700 weight, -0.02em letter spacing
- **Body**: 400 weight, 1.6 line height

## Support & Contact

### Technical Support
- **Website Issues**: [GitHub Issues](https://github.com/futurelabs-io/futurelabs-io.github.io/issues)
- **App Development**: Contact via repository maintainers
- **Business Inquiries**: [vlad@futurelabs-io.com](mailto:vlad@futurelabs-io.com)

### Documentation
- **iOS Development**: [Apple Developer Documentation](https://developer.apple.com/documentation/)
- **SwiftUI**: [SwiftUI Framework Reference](https://developer.apple.com/documentation/swiftui)
- **Photos Framework**: [Photos Framework Guide](https://developer.apple.com/documentation/photos)

### Community
- **GitHub Discussions**: For feature requests and general discussion
- **Issues**: For bug reports and technical problems
- **Pull Requests**: For contributing improvements

## License

This project is developed by **FutureLabs.io SRL**. The website code is open source under the MIT License. The PolaroidMaker iOS application and associated intellectual property remain proprietary to FutureLabs.io SRL.

---

## Quick Commands Reference

```bash
# Local development
python3 -m http.server 8000

# Test HTML validation
tidy -e index.html

# Check responsive design
# Use browser dev tools: Cmd+Shift+M (Chrome/Firefox)

# Deploy to GitHub Pages
git push origin main

# Check deployment status
# Visit: https://github.com/futurelabs-io/futurelabs-io.github.io/actions
```

### Troubleshooting

| Issue | Solution |
|-------|----------|
| **Site not loading** | Check GitHub Actions for build errors |
| **CSS not applying** | Verify file paths and clear browser cache |
| **Custom domain errors** | Check DNS propagation: `dig futurelabs-io.com` |
| **HTTPS certificate** | Wait 24h for GitHub certificate issuance |
| **Mobile layout broken** | Test responsive design in browser dev tools |

---

**Built with ❤️ by FutureLabs.io SRL** • [Website](https://futurelabs-io.com) • [Email](mailto:vlad@futurelabs-io.com)

*Crafting innovative solutions at the intersection of data, artificial intelligence, and exceptional product design.*