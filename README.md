# shirahbrown

Personal site for **Shirah Brown** — Fractional Technology Executive (Salesforce & enterprise architecture).
Single self-contained static page, hosted on GitHub Pages at **shirahbrown.com**.

## Structure
```
index.html            # the whole site (all CSS inline; Figtree via Google Fonts)
CNAME                 # shirahbrown.com  (GitHub Pages custom domain)
assets/
  favicon.png         # 32×32 browser icon
  apple-touch-icon.png# 180×180 iOS icon
  icon-512.png        # 512×512
  social-card.png     # 1280×640 Open Graph / social share image
  logo.png            # SMB monogram (transparent)
```

## Publish (GitHub Pages)
1. Create a new GitHub repo named **shirahbrown**.
2. Push this folder:
   ```bash
   git remote add origin https://github.com/<you>/shirahbrown.git
   git branch -M main
   git push -u origin main
   ```
3. Repo → **Settings → Pages** → Source: `main` / root. Save.
4. Custom domain: the `CNAME` file already sets `shirahbrown.com`; confirm it under Settings → Pages. Enable **Enforce HTTPS** once the cert issues.

## DNS at GoDaddy (shirahbrown.com)
Point the apex + www to GitHub Pages:
- **A** records for `@` → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
- **AAAA** (optional) `@` → `2606:50c0:8000::153`, `...8001::153`, `...8002::153`, `...8003::153`
- **CNAME** `www` → `<you>.github.io`
- Redirect `shirahmariebrown.com` → `shirahbrown.com`

## Notes / TODO
- About-section portrait is a placeholder (SMB monogram) until a headshot is added → `assets/` + swap the `.portrait` block.
- `[X] days/month` in the Fractional card is a placeholder.
- Proof section is intentionally de-identified — do **not** add client-attributed confidential metrics.
