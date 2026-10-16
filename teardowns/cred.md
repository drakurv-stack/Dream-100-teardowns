# Teardown #1: CRED (cred.club)

**Date:** 2026-10-17 · **Tier:** 1 (dream)

## What I like

CRED’s homepage is fast and confident — bold design, clear value prop. The kind of site that’s 95% there, which makes the last 5% worth fixing.

## Issues found (verified 2026-10-17)

1. **Dead link: “CRED mint” 404s — twice.** The header and footer both link to https://cred.club/mint, which returns 404. Every visitor who clicks it hits a dead page.
2. **23 of 27 images missing alt text.** Screen readers skip them; image SEO is lost.
3. **No `<h1>` on the page.** Search engines and assistive tech lose the page’s main topic.
4. **No canonical tag.** Duplicate-content risk across URL variants.
5. **No `lang` attribute on `<html>`.** Screen readers can’t pick the right pronunciation.

## The fix (copy-paste ready, free)

### 1. Remove the dead CRED mint links (2 instances)

```html
<!-- BEFORE — both return 404 -->
<a href="https://cred.club/mint" target="_blank" class="...">CRED mint</a>

<!-- AFTER — remove until the page exists again -->
<!-- CRED mint retired; dead link removed 2026-10-17 -->
```

### 2. Add lang attribute

```html
<!-- BEFORE -->
<html>
<!-- AFTER -->
<html lang="en">
```

### 3. Add canonical tag (in <head>)

```html
<link rel="canonical" href="https://cred.club/" />
```

### 4. Add the missing h1 (visually hidden, top of <body>)

```html
<h1 class="sr-only">CRED — pay credit card bills and earn rewards</h1>
```

### 5. Alt text for all 23 images

| Image | Suggested alt |
|---|---|
| hero-desktop-poster.jpg | CRED app showing credit card bill payments and rewards on a smartphone |
| qr-final.png (×3) | QR code to download the CRED app |
| phone-ticker-desktop-poster-final.jpg | CRED app with live credit score ticker on a smartphone |
| ccbp-fold-poster.jpg | Pay credit card bills on CRED and earn rewards |
| snp-logo-final.png | CRED product logo |
| rupay-logo-final.png | RuPay logo |
| tnp-logo-final.png | CRED product logo |
| p2p-logo-final.png | CRED P2P logo |
| garage-logo-final.png | CRED Garage logo |
| rewards-desktop-poster.jpg | CRED rewards, cashback and exclusive offers |
| datasafe.png | DataSafe badge — your data stays safe and encrypted |
| rating-stars.png (×2) | App store star rating |
| now-live-wide.png (×2) | New CRED feature now live banner |
| down-arrow.png | (decorative — empty alt="") |
| plus-icon.png (×5) | (decorative accordion icons — empty alt="") |

## Outreach

- Sent: 2026-10-17 → Kunal Shah (Founder), LinkedIn DM (delivered, confirmed in thread)
- Reply: —
- Follow-up: — (send in 4-5 days if no reply)
