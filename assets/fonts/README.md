# Local fonts

Exact Google Fonts CSS request from hub.src.html, Chrome UA, downloaded 2026-10-20. latin and latin-ext subsets retained for Spanish and extended Latin. Original API CSS archived in inspection/font-tests/google-response.css; request, source URLs, download UTC, sizes and SHA256 are in provenance.json.

Bricolage Grotesque 600/800 and JetBrains Mono 400/600 share variable WOFF2 resources returned by Google for both requested weights. They are deduplicated per subset, preserving separate font-face declarations and original unicode-range/font-stretch/font-display. Atkinson Hyperlegible 400/700 has separate resources. Eight binaries, twelve faces. No font transformations.

Three original official Google Fonts OFL licenses are included as *-OFL.txt. Ship the whole fonts directory with the site; offline font_css(embedded=True) embeds the full notices alongside fonts inside CSS.

API in ../font_pack.py: font_css(embedded=False, prefix="fonts/") -> CSS string without style tags. For nested online pages use prefix="../fonts/"; font_css(embedded=True) uses data:font/woff2 resources and ignores prefix. No network or external dependencies at build time.
