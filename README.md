# KB Policy Website

Statische, trackingfreie Policy-Website für `policy.krypto-boss.de`, ausgelegt für Meta/Facebook App Review.

## Enthaltene Seiten

- `/` -> Landing
- `/privacy` -> Privacy Policy
- `/data-deletion` -> Data Deletion (Meta Review relevant)
- `/terms` -> Terms
- `/imprint` -> Impressum
- `/security` -> Security & Contact
- EN-Versionen unter `/en/...`

## Platzhalter vor Go-Live ersetzen

Folgende TODO-Platzhalter müssen in den HTML-Dateien ersetzt werden:

- `[COMPANY_NAME]`
- `[OPERATOR_NAME]`
- `[ADDRESS]`
- `[EMAIL]`
- `[DATE]`

Hinweis: Die TODOs sind absichtlich visuell hervorgehoben, damit beim Review nichts übersehen wird.

## Lokal testen (Open with Live Server)

1. Ordner `KB-Policy-Website` in VS Code öffnen.
2. `index.html` mit **Open with Live Server** starten.
3. Navigation testen (lokal über `.html`-Dateien).
4. Optional: EN-Seiten über `en/index.html` prüfen.

## Vercel Deploy (Static)

1. Repository zu GitHub pushen.
2. In Vercel: **Add New Project** -> GitHub Repo auswählen.
3. Framework Preset: **Other** (kein Build nötig).
4. Root Directory auf `KB-Policy-Website` setzen.
5. Deploy ausführen.

## Subdomain policy.krypto-boss.de

1. In Vercel Projekt -> **Settings** -> **Domains** -> `policy.krypto-boss.de` hinzufügen.
2. Beim DNS-Provider einen `CNAME` für `policy` auf den von Vercel angegebenen Zielhost setzen (z. B. `cname.vercel-dns.com`).
3. DNS propagieren lassen und HTTPS-Zertifikat in Vercel abwarten.

## Meta App Review URLs

- Privacy Policy URL: `https://policy.krypto-boss.de/privacy`
- Data Deletion URL: `https://policy.krypto-boss.de/data-deletion`

## Technische Hinweise

- Rewrites + Security Header sind in `vercel.json` konfiguriert.
- Keine externen CDNs, keine externen Fonts, kein Tracking, keine Cookies.
- `robots.txt` und `sitemap.xml` sind enthalten.
