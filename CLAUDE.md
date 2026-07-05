# Meridante — Design Brief (anti-slop)  ·  load into EVERY build

This is the "instructions to the web designer." Drop it into the project folder as `CLAUDE.md`
(or reference it) before building. Adapted from the Mr. Vibe "$10k website / not vibe-coded" method
+ our own client feedback. Goal: every site looks like a €10k agency made it, never AI slop.

## Hard bans (the tells of a vibe-coded site)
- **No purple / blue / generic gradients** as the brand look. No rainbow or "AI" gradients.
- **No default fonts** — never Inter, Roboto, Poppins, Montserrat, Lato, Arial. Don't over-use Fraunces.
  Pick a **distinctive, characterful pairing** that fits the brand (a display + a clean grotesk).
- **No flat "cardboard"** — no thin-bordered boxes on flat colour slabs. Use depth: soft shadows,
  subtle gradients, glassmorphism, layered imagery. Imagery-forward, not colour-block-forward.
- **No fake content** — no invented testimonials/logos; real or clearly-placeholder only.
- **No misleading imagery** — placeholder photos must read ON-SUBJECT for the sector/location
  (a Luxembourg city agency must not show Algarve countryside). Flag every placeholder in a comment.

## Always do
- **Follow a real reference**, not "make it beautiful." (see "Reference extraction" below)
- **Distinctive fonts** — prefer named Google Fonts; the font can make or break the site.
- **Depth + restraint** — generous whitespace, refined hairlines, expensive-feeling micro-motion.
- **Desktop AND mobile** — a dedicated mobile pass every time.
- **Self-audit after building** (see "Audit pass").
- **prefers-reduced-motion safe**; no broken images; semantic HTML; meta + OG; JSON-LD; inline SVG favicon.

## Reference extraction (raise realism)
Don't rely on imagination. For the brief:
1. Find a best-in-class reference on **siteinspire.com** or **dribbble.com** for the sector.
2. Full-page screenshot it (GoFullPage) → hand it to the build as design inspiration.
3. **Copy its CSS**: Inspect → select `<body>` → Styles → copy the element style → paste into the brief
   ("here's the actual CSS for the reference"). Screenshot + CSS together beats a screenshot alone.
4. Tell the build: "use this as design inspiration — adapt, don't clone."

## Audit pass (mandatory, after the first build)
Run a dedicated pass with the **front-end-design** skill: *"Audit this site with the front-end-design
skill — make sure it looks and functions the best it can."* Typical catches: sticky-header on scroll,
z-index of decorative layers behind content, mobile breakpoints, contrast, font polish. Fix, then re-audit.

## Font refinement loop
If a font reads "okay" but not great: target the element (or describe it) and swap to a **named Google
Font** (Claude can pull from Google Fonts). Iterate title + body separately. Examples that worked:
display "Changa One" / "Bricolage Grotesque" / "Bodoni Moda"; body "Space Grotesk" / "Archivo" /
"Hanken Grotesk" / "Newsreader". Match the brand, not a default.

## The build prompt shape (what to hand Claude)
"Create a beautiful website for {client}. Follow ALL rules in @CLAUDE.md. Use @logo and @photo.
Use the **front-end-design** skill in all your work. Use @reference-screenshot as design inspiration —
here's its CSS: {paste}. Desktop + mobile, reduced-motion safe, no broken images." → run in **auto mode**.
