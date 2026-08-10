# Launch readiness

Checked 2026-08-10. This is a product-risk record, not individual legal advice.

## Current state

- The public Cloudflare Pages deployment and the standalone GitHub repository
  exist and use no paid plan.
- Local browser enhancement, downloads, consent, SSRF protection, bounded
  streaming, and responsive sponsor placeholders are implemented.
- VSCO server resolution and proxying are paused before any upstream request.
  The separate local Plus app retains its own implementation.
- No ad network, analytics, accounts, payments, or persistent media database is
  enabled.

## Blocks before commercial marketing

1. Publish the operator's legal name, geographic address, direct email,
   organization number/register, and VAT status where applicable. A public
   GitHub issue alone does not satisfy the operator-information requirement in
   [ehandelsloven § 8](https://lovdata.no/lov/2003-05-23-35/%C2%A78).
2. Add a private contact channel for privacy, copyright, and removal requests.
3. Obtain written permission or an approved mechanism for automated access.
   Current terms restrict it for
   [VSCO](https://www.vsco.co/about/terms-of-use),
   [Instagram](https://www.facebook.com/help/instagram/581066165581870),
   [Facebook](https://www.facebook.com/terms), and
   [TikTok in the EEA](https://www.tiktok.com/legal/page/global/terms-of-service-eea/en).
4. Complete the privacy notice with the operator identity, legal bases,
   recipients/transfers, actual retention periods, data-subject rights, and
   complaint route required by GDPR Articles 13–14.
5. Review the final sponsor and market before publication. Keep advertisements
   clearly identified and separate from download actions.

## Advertising boundary

Do not add AdSense now. Google Publisher Policies restrict monetization of
pages that enable streaming-video downloads where the content provider
prohibits downloading. Direct static sponsorship without tracking is the
current technical path, but revenue starts only after a real sponsor agreement.

- [Google: enabling dishonest behavior](https://support.google.com/publisherpolicies/answer/10436828?hl=en)
- [Google: intellectual property abuse](https://support.google.com/publisherpolicies/answer/10402772?hl=en)

Sponsor links must use `rel="sponsored noopener noreferrer"`. Accepted creative
must be a static image with alt text and a destination URL; no tracking pixels,
scripts, misleading download buttons, or personalized targeting.

## Information still needed from the operator

- legal/registered name
- geographic business address
- private contact and rights-request email
- organization number/register and VAT status, if applicable
- target markets and languages
- actual sponsor identity, creative, link, period, and agreed price
