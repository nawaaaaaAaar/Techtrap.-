# TECHTRAP — Game and Deployment Report

**Prepared:** 9 November 2026  
**Source:** `TECHTRAP (final game).html`  
**Original SHA-256:** `4a0531e455f9d14339626432587850102e9e5416206a4ea26efcfad571f9a1e8`  
**Release state:** Repository initialized; original game HTML still needs to be uploaded and GitHub Pages activated.

## Executive summary

TECHTRAP is a self-contained HTML5 Canvas endless-runner educational game centered on responsible technology use. The game features Kerala-inspired street scenes, Malayalam signs, and technology-themed obstacles. There is no backend, package manager, build pipeline, or required external service.

## Game features

| Feature | Details |
|---|---|
| Platform | Single-page HTML / CSS / JavaScript, Canvas 2D |
| Win | Avoid 50 obstacles |
| Lose | Accumulate 6 effective growth/hit steps |
| Obstacles | 7 ground types and 3 flying types |
| Difficulty | Speed accelerates from 6 toward 13 |
| Recovery | Every 6 consecutive avoids partially reverses growth |
| Desktop | Space / Up to jump, Down to slide, M to mute |
| Mobile | On-screen Jump and Slide controls |
| Audio | Web Audio sound effects and embedded background music |
| Assets | Embedded producers photograph and music |
| Visuals | Animated Kerala street setting, landmarks and Malayalam shop signs |

## Security and privacy observations

These findings come from a *static source inspection*, not a penetration test:

- No obvious data collection: no `fetch`, `XMLHttpRequest`, WebSocket, forms, cookies, or localStorage access found.
- No external JavaScript or CSS dependencies detected.
- No obvious execution sinks such as `eval` or `new Function` found.
- Embedded photo contains no EXIF metadata, but the image and background music become publicly accessible when source is published.
- Obtain rights-holder consent before publishing the embedded photo and music.

## Browser and accessibility notes

- Responsive canvas layout with touch controls.
- Viewport restrictions (`user-scalable=no`) may hinder zoom accessibility.
- Some emoji and Malayalam text vary by platform and installed fonts.
- Entire embedded media payload is loaded in the initial HTML (approximately 1.36 MiB), which may affect slower connections.
- Keyboard/pointer controls work, but screen-reader gameplay could benefit from additional accessible status descriptions.

## Deployment checklist

- [x] GitHub repository created and README initialized.
- [x] Source inspected and project report prepared.
- [ ] Upload original `TECHTRAP (final game).html` to the repository root with the name **`index.html`**.
- [ ] Confirm permission to share the embedded producer photo and music.
- [ ] Go to **Settings → Pages → Build and deployment → Deploy from a branch** and select **main / (root)**.
- [ ] Verify site on desktop and mobile.

Expected URL after GitHub Pages activates: `https://nawaaaaaaar.github.io/Techtrap.-/`. This is not a verified live URL yet.
