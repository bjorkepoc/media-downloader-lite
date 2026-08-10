# Media Downloader Lite

The free, public, ad-funded edition of Media Downloader. Visitors paste a
public VSCO, Instagram, TikTok, or Facebook link, preview the best original
media exposed by the source, and explicitly choose what to download.

Production: <https://media-downloader-4y5.pages.dev/>

## Product boundary

- Static HTML/CSS/JavaScript on Cloudflare Pages.
- Two minimal Pages Functions for source resolution and conditional media
  proxying.
- No Python server, account, database, subscription, payment, analytics, or
  persistent media storage.
- No server-side FFmpeg, upscaling, interpolation, generation, muxing, or
  re-encoding.
- Optional 60/90 FPS, 2x upscale, filters, and MP3 export run in the visitor's
  browser after separate consent.
- Public, logged-out sources only. No login cookies, private accounts, DRM, or
  access-control bypass.
- Direct source-CDN delivery when possible; the range-compatible Function is
  only a fallback for CORS, hotlink, preview, or attachment behavior.

## Advertising and cost

The page has responsive, clearly labelled direct-sponsor placements on desktop
and mobile. They are placeholders and currently earn nothing. There is no ad
network, tracking, cookie, impression beacon, or personalized advertising.

The current `pages.dev` deployment uses Cloudflare Pages and the Workers Free
allowance. No paid plan or custom domain is required. If the free quota is
exhausted, requests should fail rather than trigger an unreviewed paid upgrade.
Re-check current Cloudflare pricing before a larger launch:
<https://developers.cloudflare.com/pages/functions/pricing/>.

Do not add AdSense or another ad network without publisher-policy, platform,
copyright, privacy, CMP/consent, operator-information, and `ads.txt` review.
Google specifically restricts monetization of pages that enable downloads when
the content provider prohibits them.

## Relation to Plus

The existing project at `/Users/po/dev/video-enhancer` is the Plus/Premium base.
It retains the local Python app, CLI, yt-dlp/gallery-dl integration, desktop
packaging, FFmpeg presets, custom FPS, encoder choices, and the broader local
feature set. Python and native FFmpeg run on the user's machine, not in this
Lite service.

The Plus business model is not decided. Keeping it as a downloadable local app
avoids server compute cost; hosting its Python/FFmpeg engine publicly would
require a paid, separately secured architecture.

## Development

```bash
npm run test:web
npm run dev:web
```

Deploys target the existing Cloudflare Pages project:

```bash
npm run deploy:web
```

Run that only after checking the authenticated Cloudflare account and confirming
that no paid product has been enabled.

## Current platform status

- Instagram: public samples and byte-range downloads verified.
- TikTok: public samples, separate exposed audio, and byte ranges verified.
- Facebook: a current public sample verified; extraction remains platform-HTML
  dependent.
- VSCO: the local Plus app works, but VSCO currently challenges anonymous
  Cloudflare edge requests. Lite reports the gap without bypassing protection.

## License and security

MIT licensed. See `LICENSE`, `THIRD_PARTY_NOTICES.md`, and `SECURITY.md`.
