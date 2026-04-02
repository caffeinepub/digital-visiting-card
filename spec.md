# InstaSite Kerala - Digital Card

## Current State

A dynamic PWA digital visiting card for Nagarajan (Sales Officer, InstaSite Kerala).
- React/TypeScript frontend on Caffeine with Motoko backend
- Glassmorphic card UI with profile photo, 7 action buttons (Save Contact, Call, WhatsApp, Location, Website, Share, QR Code)
- Admin panel via Internet Identity for editing card data
- SEO: meta tags, Open Graph, JSON-LD, geo tags, sitemap
- Performance optimizations: CSS animations (no framer-motion), no backdrop-filter blur, static data render
- `minify: false` in vite.config.js (performance issue - JS unminified)
- Missing: Services section, Image gallery, Google Maps embed, Contact/booking form, Malayalam language toggle
- WhatsApp button exists but not visually prominent as primary CTA
- Header has brand title and tagline but not visually impactful

## Requested Changes (Diff)

### Add
- **Strong hero header**: Large brand title, clear tagline ("Kerala's #1 Digital Business Card Service"), prominent value proposition
- **Big WhatsApp CTA button**: Prominent, large WhatsApp button at the top of the card as primary call-to-action, above all other buttons
- **Services section**: Cards showing InstaSite Kerala services (Digital Business Cards, Business Websites, Social Media Branding, etc.)
- **Image gallery**: Photo gallery section with sample work/portfolio images (placeholder images, admin can update)
- **Google Maps embed**: Embedded Google Maps showing Thiruvananthapuram location
- **Contact/booking form**: Form with Name, Phone, Email, Message fields + submit via WhatsApp or store to backend
- **Malayalam language toggle**: Button to switch UI text between English and Malayalam
- **Enhanced SEO**: Improved meta description with Malayalam keywords, better structured data

### Modify
- **Performance**: Fix `minify: false` to `minify: 'esbuild'` in vite.config.js
- **WhatsApp button styling**: Make it the most prominent button in the action list (larger, green glow, pulsing animation)
- **Header design**: More impactful hero section with gradient text, tagline, and sub-value proposition
- **Overall design**: More modern, premium feel — improved spacing, typography, section separators

### Remove
- Nothing to remove

## Implementation Plan

1. Fix vite.config.js minification (performance)
2. Update index.html SEO meta tags with Malayalam keywords
3. Rewrite App.tsx to add:
   a. Language toggle state (English/Malayalam) in header
   b. Enhanced hero header section
   c. Prominent WhatsApp CTA as first button
   d. Services section after action buttons
   e. Image gallery section
   f. Google Maps embed section (Thiruvananthapuram)
   g. Contact/booking form section
4. Update index.css for new sections and improved premium design
5. Backend unchanged (Card model is sufficient; contact form submits via WhatsApp deep link)
