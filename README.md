# FilaTint — Website

Marketing site for the FilaTint app, served by GitHub Pages at
[filatint.townsville.cc](https://filatint.townsville.cc) (custom domain on
the `townsville.cc` Cloudflare zone, HTTPS enforced).

**FilaTint is live on the [App Store](https://apps.apple.com/us/app/filatint/id6812869640).**

- `index.html` — landing page (also the App Store **Support URL**)
- `privacy.html` — privacy policy (also the App Store **Privacy Policy URL**)
- `assets/` — app icon exported from the app repo's AppIcon asset catalog
- `CNAME` — pins the custom domain; don't delete unless you mean to detach it (see below)

Plain static HTML/CSS, no build step. Deploys automatically on push to `main`
via GitHub Pages.

## Updating

Edit `index.html` / `privacy.html` directly and push to `main` — Pages
rebuilds in under a minute.

The hero's "Download on the App Store" badge is Apple's official one from the
Marketing Resources toolbox (toolbox.marketingtools.apple.com); keep using it
rather than a hand-made button.

## If the HTTPS certificate ever gets stuck

GitHub Pages certificate provisioning can occasionally stall on the generic
`*.github.io` wildcard cert instead of issuing one for the custom domain. Fix:
remove the `CNAME` file (temporarily detaching the custom domain), let Pages
rebuild, then add it back — this re-triggers certificate issuance.

## Related repos

- [FilaTint](https://github.com/hibikipr/FilaTint) — the app itself
