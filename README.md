# BR Nuvio launch probe

TizenBrew **app** module: pings a webhook.site catcher with `navigator.userAgent`,
then `location.replace`s to the hosted Nuvio web app (`https://web.nuvioapp.space/`).
Used to verify that Nuvio opens from TizenBrew on the TV and to log the UA it sees.

Add in TizenBrew as `niteowl099/tizenbrew-nuvio-br-probe@master` (pin `@master`:
unpinned jsDelivr paths can serve a stale copy for a long time; see
`mentalprosthetics/tizenbrew-ua-probe`). The on-screen `vX.Y.Z` confirms which copy loaded.

Rules: `package.json` must have **no UTF-8 BOM** (TizenBrew shows "Unknown Module");
inline JS must be **ES5** (Tizen 3 = Chromium 47). CI (`scripts/validate.js`) enforces both.
