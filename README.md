# BSG Wraps — Color Change Landing Page

Single-page lead-gen landing page for color change wraps, built per the Claude Design + Cloudflare Pages Website Build SOP (static HTML, no build pipeline needed since there's no JSX/React here — content is already server-rendered).

Layout pattern follows the Full Curl Graphix reference the client liked (hero+form, trust bar, why-grid, gallery, process, reviews, quote form, FAQ, CTA banner, footer) — rebuilt entirely with BSG's own brand, copy, and real business info. No text, photos, or reviews were carried over from that reference site.

Brand tokens pulled directly from bsgwraps.com's live CSS: `--blue: #1b99d4`, `--black: #101010`, font `Poppins` (+ `Crimson Text` italic for review quotes, matching BSG's actual secondary font).

## Before launch

- [x] **Logo** — pulled the real BSG mark from bsgwraps.com into `assets/logo.png`
- [x] **Hero background** — `assets/hero-bg.jpg`, the moody Corvette shot from BSG's own homepage, used as ambient texture (28% opacity), not attributed to a specific job
- [ ] **Gallery flagship photo** — `assets/gallery-01.webp` is currently the blue Porsche art from bsgwraps.com, honestly labeled "Color Change Concept." This slot should really be the actual photos on display at the Cadillac dealership — that's BSG's strongest proof point and it isn't published anywhere online, so it has to come from Skip directly.
- [ ] **Gallery photos 2–5** — `assets/gallery-02.webp` through `gallery-05.webp` are still placeholders. BSG's existing site photography is fleet-graphics work (a different client/service), not color-change wraps, so it wasn't reused here — would misrepresent the service.
- [ ] **Reviews** — 4 placeholder review cards in the Reviews section are marked `[Paste a real 5-star Google review here]`. Do not fabricate; pull real ones from BSG's Google Business Profile
- [x] **Lead form endpoint** — `LEAD_WEBHOOK_URL` wired to BSG's GHL webhook
- [ ] **OG image** — `assets/og-image.png` (1200×630) for social previews
- [ ] **Tracking IDs** — GA4 / Meta Pixel / Microsoft Clarity snippets are commented out at the bottom of `index.html`, ready to uncomment once IDs are issued
- [ ] **Canonical URL** — currently placeholder `https://www.bsgwraps.com/color-change/`; confirm final path or subdomain before launch and update `<link rel="canonical">`, OG tags, schema `url`, `robots.txt`, and `sitemap.xml` to match
- [ ] Compress all images to WebP per SOP §10.1 before upload

## Conscious skips (per SOP §8.7.6)

- No Content-Security-Policy header yet — add only after auditing every script/connect endpoint the live form webhook uses.
- No hidden body-SEO block — this page is plain static HTML (not client-rendered React), so all content is already crawler-visible without the hidden-block trick the SOP describes for the React-based multi-page sites.
