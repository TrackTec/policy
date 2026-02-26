# KB Policy Website

Static, no-tracking policy website for `policy.krypto-boss.de`, prepared for Meta/Facebook App Review.

## Included pages

- `/` -> Landing
- `/privacy` -> Privacy Policy
- `/data-deletion` -> Data Deletion (Meta review relevant)
- `/terms` -> Terms
- `/imprint` -> Imprint
- `/security` -> Security & Contact
- English versions under `/en/...`

## Current legal/contact data

- Company name: `KryptoBOSS`
- Contact email: `bratanbitcoin@gmail.com`
- GDPR requests: `bratanbitcoin@gmail.com`
- Last updated date on pages: `26.02.2026` (DE) and `February 26, 2026` (EN)

## Local test (Open with Live Server)

1. Open folder `KB-Policy-Website` in VS Code.
2. Start **Open with Live Server** on `index.html`.
3. Verify navigation and all page links.
4. Check EN pages via `en/index.html`.

## Vercel deploy (static)

1. Push repository to GitHub.
2. In Vercel: **Add New Project** and select the repo.
3. Framework preset: **Other** (no build step required).
4. Set Root Directory to `KB-Policy-Website`.
5. Deploy.

## Subdomain setup

1. In Vercel project settings, add domain `policy.krypto-boss.de`.
2. At your DNS provider, create `CNAME` record `policy` to the Vercel target (for example `cname.vercel-dns.com`).
3. Wait for DNS propagation and TLS issuance.

## Meta App Review URLs

- Privacy Policy URL: `https://policy.krypto-boss.de/privacy`
- Data Deletion URL: `https://policy.krypto-boss.de/data-deletion`

## Technical notes

- Rewrites and security headers are configured in `vercel.json`.
- No external CDNs, no external fonts, no analytics/tracking scripts, no cookies.
- `robots.txt` and `sitemap.xml` are included.
