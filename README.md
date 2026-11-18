# Dean Baker Studios: one-page website

Static one-page site (About / Services / Contact) for Dean Baker Studios, an independent production company in Lusaka, Zambia.

- **Hero:** a 10-second continuous take, exported as 200 WebP frames in `frames/` and scrubbed by scroll on a `<canvas>`.
- **Services:** scroll-driven list with a full-bleed stage (stacked list on mobile).
- **Smooth scroll:** [Lenis](https://github.com/darkroomengineering/lenis) (MIT), vendored in `vendor/`.
- **No build step.** Plain HTML, CSS and JS in `index.html`.

## Run locally

    python3 -m http.server 8000

then open http://localhost:8000

## Placeholders to replace

- `CONTACT_EMAIL` in `index.html` (and the visible `#emailtxt` text): confirm the studio email.
- Services copy and the five stills in `img/` until real work exists.
- Contact form opens a `mailto:` draft; swap for a backend or form service when ready.
- First seconds of the hero video show garbled script text; regenerate with blank paper.

## Deploy

Static host: Cloudflare Pages (build command none, output directory `/`), Netlify or GitHub Pages.

## Palette

CSS variables at the top of `index.html` (`--black`, `--foam`, `--latte`, `--merlot`, ...). Switching to strict mono is a variable change.


## Update (18 Nov 2026)
- Hero is now a static still (`img/hero.webp`); the scroll-scrubbed video and `frames/` are gone.
- Merlot (#340D1A) design system, Montserrat only, rounded corners, enquiry form opens as a popup.
- `img/*.svg` are placeholder brand-colour illustrations for the five services; replace with real photos/stills.
- Footer credit: "Website by Digital Polaroid Technologies" (confirm wording/link).

## Update (18 Nov 2026, feedback round 2)
- Removed scroll hijacking and Lenis (native scrolling now); services are click-to-select.
- Enquiry form replaced with Email / WhatsApp / Call buttons. Set EMAIL, PHONE, WHATSAPP at the top of the script (currently placeholders).
- New Approach section (process + roadmap) is DRAFT copy to confirm with the client.
- New illustrated service art; improved service copy; garbled lettering retouched out of the hero still.

- Services scroll-driven again (pinned on desktop, plain 1:1 scrolling, step counter; tap-to-open on mobile).
- Equal scroll length per service; softer colour balance (About back to a light blush background, Merlot on cards/accents).
