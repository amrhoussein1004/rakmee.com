# Rakmee website

Production domain: **https://rakmee.com** (planned; DNS and hosting not yet configured).

## Technology
Static HTML, CSS and JavaScript; no framework, package manager or build pipeline. The entire repository root is the publish directory.

## Local development
```bash
python3 -m http.server 8080
```
Visit http://localhost:8080.

## GitHub Pages deployment

1. Create a public GitHub repository named `rakmee.com` under the authorised account. Initialise it with a README so it has a `main` branch.
2. Commit the files in this directory into the repository root.
3. Open **Settings → Pages** and choose **Deploy from a branch**, `main`, `/ (root)`; save.
4. Under **Settings → Pages → Custom domain**, enter `rakmee.com`. The `CNAME` file already contains this domain.
5. Configure DNS with your DNS provider: four A records for the apex (`185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`). For `www` use a CNAME to `amrhoussein1004.github.io` if desired. Validate DNS in GitHub Pages before enforcing HTTPS.
6. Enable **Enforce HTTPS** after the certificate is issued. Do not change production DNS before the Pages site is confirmed operational.

GitHub Pages supports a static site. The enquiry form currently opens an email draft and does not send data to a backend.

## Pages
- `index.html` - Homepage
- `platform.html`, `digital-growth.html`, `how-it-works.html`, `why-rakmee.html`, `contact.html`
- `privacy.html`, `cookies.html` - drafts requiring legal review
- `sitemap.xml`, `robots.txt` - domain-specific SEO files

## Before public launch
- Set up and confirm `hello@rakmee.com` or change `assets/site.js` to the actual receiving inbox. **The current contact form opens an email draft; it does not send enquiries automatically.**
- Connect a booking tool if a real 'Book a discovery call' calendar is required.
- Review legal notices and privacy/cookie wording; add confirmed company details.
- Replace illustrative product mockups/metrics with verified capabilities and evidence.
- Review UK healthcare marketing compliance prior to publishing claims or campaigns.
- Replace logo raster with an approved vector master if available.
