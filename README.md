# where-am-i-game.com

The holding page for **Where Am I?**, served by GitHub Pages at
https://where-am-i-game.com.

One static file. `index.html` is self-contained apart from the two Google Fonts
(Space Grotesk, Spline Sans Mono) the app itself uses, so editing it needs no
build step and no dependencies: change the file, commit, push, and Pages
redeploys in a minute or two.

This is deliberately a **separate repository from the game**, which is private.
GitHub Pages only serves from a private repo on a paid plan, and making the app
repo public to host a holding page would expose the whole codebase. So the site
lives here, public, and holds nothing but the page.

## The palette is copied, not shared

The CSS custom properties at the top of `index.html` are transcribed from the
game's `src/design/tokens.ts` ("Departure board" -- near-neutral paper,
near-black ink, hairline rules, a single signal-yellow accent, light and dark).
There is no import, so **if the app's tokens change, this file does not follow**.
Worth a glance whenever the theme is touched.

## DNS

Apex `where-am-i-game.com` -> four A records at GitHub's Pages IPs;
`www` -> a CNAME at `quinja91.github.io`. The `CNAME` file in this repo is what
tells Pages which domain to answer for -- do not delete it, and note that the
GitHub UI rewrites it if the custom domain is changed in settings.
