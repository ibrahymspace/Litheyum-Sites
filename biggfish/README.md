# BIGGFISH website

Marketing site for BIGGFISH, the AI brand studio. It is a single static page with no build step.

```
biggfish/
  index.html          page, styles and scripts
  assets/dolphin.png  mascot (hero and sign-up)
  assets/dolphin-head.png  logo mark and favicon
```

## Before launch

- **Waitlist.** Set `CONFIG.waitlistEndpoint` at the top of the script in `index.html` to a form backend that accepts a JSON POST (Formspree, Basin or your own API). The body is `{ email, plan, source }`. Until it is set, the form tells visitors sign-ups are not open yet.
- **Pricing.** Solo $19, Studio $49 and Agency custom are placeholders. Change them in the pricing section.
- **Example brands.** Saltwater Supply, Kora Pay and Rooftop Run Club are made up for the demo and preview.

## Deploy

The site is served from GitHub Pages at https://biggfish.xyz.

- `.github/workflows/deploy-biggfish.yml` publishes the `biggfish` folder on every push to `main` that touches it.
- `biggfish/CNAME` holds the custom domain.

One-time setup:

1. Repo **Settings → Pages → Source: GitHub Actions**. The repo is private, so Pages needs a paid GitHub plan (Pro, Team or Enterprise), or make the repo public.
2. At your domain registrar, add these DNS records:

   | Type  | Name | Value |
   |-------|------|-------|
   | A     | @    | 185.199.108.153 |
   | A     | @    | 185.199.109.153 |
   | A     | @    | 185.199.110.153 |
   | A     | @    | 185.199.111.153 |
   | CNAME | www  | ibrahymspace.github.io |

   Delete any other A, AAAA or CNAME records on `@` and `www` first.
3. Once the first deploy runs, go to **Settings → Pages**, check that the custom domain reads `biggfish.xyz` and tick **Enforce HTTPS** once the certificate is issued.
