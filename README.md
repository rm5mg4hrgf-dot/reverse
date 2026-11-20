# REVERSE — Understand what's inside

Interactive 3D product-anatomy and repairability explorer. Pick an everyday object, explode it into separate parts, inspect each component, investigate symptoms, and see a transparent repairability breakdown.

## Features
- 32 products, each built from separate 3D meshes. 8 hand-modelled (stapler, umbrella, pen, scissors, mechanical pencil, clothespin, binder clip, tape measure) and 24 office/household items as schematic stacked shapes (chair, lamp, mouse, keyboard, printer, laptop, monitor, shredder, and more)
- Orbit / zoom / pan (mouse and touch), exploded view with intensity slider, isolate, preset camera views, part selection and highlighting
- Component inspector, fault explorer (product → symptom → cause → component), global search
- Ask REVERSE: natural-language investigation. Rule-based engine from the fault database; optional Claude AI when hosted in claude.ai
- Repairability breakdown (Unknown where undocumented), repair-or-replace calculator, maintenance library
- Scroll-driven hero story, 60-second demo tour

## Run locally
It is a static site (one `index.html`, Three.js from a CDN). Open `index.html`, or run `python3 -m http.server` and visit http://localhost:8000.

## Deploy
GitHub Pages: Settings → Pages → Deploy from branch `main` / root.

## Tech
Three.js r128, vanilla JS, CSS (glass UI). No build step and no API keys (see `.env.example`).

## Known limitations
- Procedural geometry, not GLB models; no individual part dragging; no 2D fallback if WebGL is missing
- Component text is general educational information, not model-specific documentation
- Repairability scores are an educational assessment, not a certification
- The AI layer needs the claude.ai runtime; elsewhere the rule-based fallback is used
