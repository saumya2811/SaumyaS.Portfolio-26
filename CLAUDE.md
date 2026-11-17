# CLAUDE.md

Saumya Srivastava's UX research portfolio, a static multi-page site published with GitHub Pages. No build step.

- `index.html`: About (home page)
- `product.html`: product-role front page (same layout as `index.html`, PM-oriented copy); not linked from the nav, shared directly with PM applications. It links to `Saumya-Srivastava-Senior-Product-Researcher.pdf`. `work.html`'s back link returns to whichever front page the visitor came from (sessionStorage key `front`)
- `work.html`: the five case studies, grouped by SrotaBio, Wayground and Rush (by Hike), with "More about my work" dropdowns
- `srotabio.html`, `voyagemath.html`, `accommodations.html`, `hike-revenue.html`, `hike-immersion.html`: case study pages; their back links go to `work.html`. Each ends with a short note asking visitors to email connect@saumyasri.in for the full case study
- `work.html` opens with a "glimpse" note (`.glimpse`) saying these are condensed case studies, with a mailto button to connect@saumyasri.in
- `CNAME`: custom domain (saumyasri.in) for GitHub Pages; don't remove it
- `img/`: images, including `img/tool/` screenshots for the SrotaBio carousel

Preview by opening `index.html` or running `python3 -m http.server`. The "Resume" link on `index.html` points to `Saumya-Srivastava-Senior-UX-Researcher.pdf`; replace that file to update the resume (UX version). Bump the `?v=` query on resume links after replacing a PDF so cached copies aren't served.
