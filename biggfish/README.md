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
- **Social preview.** `og:image` uses a relative path. Swap it for an absolute URL once the domain is live.
- **Example brands.** Saltwater Supply, Kora Pay and Rooftop Run Club are made up for the demo and preview.

## Deploy

Any static host works. On Netlify, Vercel or Cloudflare Pages, point the project at the `biggfish` folder.
