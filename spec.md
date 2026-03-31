# BPTS Pest Control Services

## Current State
A React + Tailwind app styled with a deep forest green OKLCH theme. Hero, About, Services, Why Choose Us, Contact, and Footer sections are in App.tsx. All styles are in `index.css` using Tailwind layers and OKLCH color tokens.

## Requested Changes (Diff)

### Add
- Navy blue (#0b3d91) as the primary brand color across the UI

### Modify
- `index.css`: Update CSS variables and component classes to use navy blue (#0b3d91 ≈ oklch(0.30 0.16 255)) instead of green
- Hero gradient: change to navy blue
- CTA buttons (cta-call, cta-whatsapp, contact-btn-call, contact-btn-whatsapp): update to navy blue + white
- Section padding: ensure sections have ~30px padding
- Body font: Arial / sans-serif (already sans-serif, keep compatible)
- Header: background navy, white text, 40px padding
- Links/buttons: navy background, white text, rounded corners

### Remove
- Green OKLCH theme tokens (replace with navy blue)

## Implementation Plan
1. Convert #0b3d91 to OKLCH: oklch(0.30 0.165 255)
2. Update all CSS custom properties in `:root` from green to navy blue
3. Update `.hero-gradient`, `.cta-call`, `.cta-whatsapp`, `.service-card` accent colors, `.contact-btn-call`, `.contact-btn-whatsapp` to use navy blue
4. Update icon colors in App.tsx inline styles from green oklch to navy oklch
5. Validate and build
