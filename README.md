# brunohoermann.de

Personal website of Bruno Hörmann. Plain static HTML, no build step. GitHub Pages serves
the repo root as it is (`.nojekyll`).

| File | Content |
|---|---|
| `index.html` | Homepage (English) |
| `impressum.html` | Impressum, § 5 DDG (German) |
| `datenschutz.html` | Datenschutzerklärung, DSGVO (German). The hosting section is for GitHub Pages. |
| `favicon.svg` | Favicon |
| `CNAME` | Custom domain for GitHub Pages |

Local preview: `python3 -m http.server`, then open http://localhost:8000.

## Deploy

1. Repo settings, Pages: deploy from branch `main`, folder `/ (root)`. Custom domain
   `brunohoermann.de`. Enable "Enforce HTTPS" after GitHub issues the certificate.
2. DNS at IONOS (Domains & SSL, brunohoermann.de, DNS):
   - `@` A records: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`.
     Delete the IONOS default A and AAAA records for `@`.
   - `www` CNAME: `bruno-hoermann.github.io`.
   - Do not change the MX, `autodiscover` and SPF/DKIM TXT records. They are for the mail
     address kontakt@brunohoermann.de.
3. To update the site: edit, commit, push.

## Rules

- Do not change the wording of `index.html` without approval.
- If the hosting changes, update the hosting section in `datenschutz.html`.
