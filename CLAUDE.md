# CLAUDE.md

Saumya Srivastava's UX research portfolio, a static multi-page site published with GitHub Pages. No build step.

- `index.html`: About (home page)
- `product.html`: product-role front page (same layout as `index.html`, PM-oriented copy); not linked from the nav, shared directly with PM applications. It links to `Saumya-Srivastava-Senior-Product-Researcher.pdf`. `work.html`'s back link returns to whichever front page the visitor came from (sessionStorage key `front`)
- `work.html`: the three case studies, grouped by SrotaBio and Wayground, with "More about my work" dropdowns
- `srotabio.html`, `voyagemath.html`, `accommodations.html`: case study pages; their back links go to `work.html`
- `img/`: images, including `img/tool/` screenshots for the SrotaBio carousel

Preview by opening `index.html` or running `python3 -m http.server`. The "Resume" link on `index.html` points to `Saumya-Srivastava-Senior-UX-Researcher.pdf`; replace that file to update the resume (UX version). Bump the `?v=` query on resume links after replacing a PDF so cached copies aren't served.
