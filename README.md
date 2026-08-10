# Media Downloader Lite

The zero-subscription edition of Media Downloader. Visitors paste a public
Instagram, TikTok, or Facebook link, preview the best original media exposed
by the source, and explicitly choose what to download. VSCO links are
recognized but server resolution is paused rather than bypassing its edge
protection or automating access without permission.

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

The page has four responsive, clearly labelled direct-sponsor placements on
desktop and mobile. Each now opens the standalone repository's structured
sponsor inquiry. They remain available placements and earn nothing until a
real sponsor agreement exists. There is no ad network, tracking, cookie,
impression beacon, or personalized advertising.

The current `pages.dev` deployment uses Cloudflare Pages and the Workers Free
allowance. No paid plan or custom domain is required. If the free quota is
exhausted, requests should fail rather than trigger an unreviewed paid upgrade.
Re-check current Cloudflare pricing before a larger launch:
<https://developers.cloudflare.com/pages/functions/pricing/>.

Do not add AdSense or another ad network without publisher-policy, platform,
copyright, privacy, CMP/consent, operator-information, and `ads.txt` review.
Google specifically restricts monetization of pages that enable downloads when
the content provider prohibits them.

## Launch status

The code and Cloudflare deployment are public, but commercial marketing is
blocked until real operator identity/address/email details are published and
platform permission is clarified. A Terms checkbox does not grant the operator
permission to automate platform access. Google Publisher Policies also make
AdSense a poor fit while a source platform prohibits downloading. See
[`docs/LAUNCH-READINESS.md`](docs/LAUNCH-READINESS.md).

## Relation to Plus

The separate <https://github.com/bjorkepoc/video-enhancer> project at
`/Users/po/dev/video-enhancer` is the Plus/Premium base.
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
- VSCO: the parser is retained and tested, but Lite pauses server resolution
  before any upstream request. Plus retains its separate local implementation.

## License and security

MIT licensed. See `LICENSE`, `THIRD_PARTY_NOTICES.md`, and `SECURITY.md`.
