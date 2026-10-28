# tope.bio

Website for Tope LLC, served by GitHub Pages at https://tope.bio.

## Files

- `index.html` — the whole site: content, styles, and a small script
  (scroll effects and the anti-harvester email link). Comments inside explain each part.
- `img/hero.webp`, `img/mesh.webp` — background images, designed by Magnific
  (credited in the page footer; keep the credit if you keep the images).
- `Hanf-CV.pdf` — the CV linked from the page. Replace it with a newer file of the same name.
- `CNAME` — tells GitHub Pages the custom domain. Leave it as `tope.bio`.
- `.nojekyll` — tells Pages to serve files as-is, without running Jekyll.

## Editing

Edit `index.html` (GitHub's web editor is fine), commit to `main`,
and Pages republishes within a minute or two.

## DNS at Porkbun

Website records (GitHub Pages):

| Type  | Host (Porkbun field)               | Answer                               |
|-------|------------------------------------|--------------------------------------|
| A     | (blank)                            | 185.199.108.153                      |
| A     | (blank)                            | 185.199.109.153                      |
| A     | (blank)                            | 185.199.110.153                      |
| A     | (blank)                            | 185.199.111.153                      |
| CNAME | www                                | tope-bio.github.io                   |
| TXT   | _github-pages-challenge-tope-bio   | (value GitHub shows when verifying)  |

Email records (Fastmail): do not change.

- MX on the bare domain: in1-smtp.messagingengine.com (10), in2-smtp.messagingengine.com (20)
- CNAMEs fm1/fm2/fm3/mesmtp `._domainkey` → `*.tope.bio.dkim.fmhosted.com`
- TXT on the bare domain: `v=spf1 include:spf.messagingengine.com ?all`
- TXT `_dmarc`: `v=DMARC1; p=none;`

Removed when the site went up: Porkbun's parking records
(ALIAS on the bare domain and wildcard CNAME `*`, both → pixie.porkbun.com).
