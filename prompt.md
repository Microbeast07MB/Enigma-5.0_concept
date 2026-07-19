# Enigma 5.0 Prompt History

## 1. Basic Landing Page

> i m just giving u a basic thing what are we working on make a basic page that i want and then we will develop it mostly for the structure

Design and develop a landing page for Enigma 5.0, the flagship hackathon of SIES CSI. Include the event name, undergraduate teams of 4, FinTech and HealthTech, a INR 25,000 prize pool, and Register, View Timeline, and Contact Team actions.

## 2. Smooth Scrolling and Buttons


>Add smooth scrolling with a fixed-header offset, pressed button states, and a glow effect for the primary button.

## 3. Scroll-Reveal Animation

Create a vanilla JavaScript and CSS scroll-reveal system using Intersection Observer. Include upward, left, and scale reveal variations, staggered grid delays, and activation when an element is 15% visible.

## 4. Heading Styling

> add Double Struck Font to `<h1 class="decode-text" data-decode-text="Enigma 5.0">Enigma 5.0<span class="decode-cursor" aria-hidden="true"></span></h1>`


## 5. Site Font

> use Fraktur Font,Bold Fraktur Font,ℂ૦૦ℓ Բ૦ՈԵઽ type font in the whole site

> do this font instead ℂ૦૦ℓ Բ૦ՈԵઽ

## 6. Content Area Colour

## 7. Problem Statements

> the area where the problem statements are given the fintech and health tech change them to problems statement 1 and 2 and make them total of 5 statements such that the window of the problems are in a systemtic manner

> **Step 2**  
> **Pick a Track**  
> Select FinTech or HealthTech based on the problem your team wants to solve.
>
> **Tracks**  
> **2 Domains**
>
> change according to the above statements

> ok make it 4 problem statements edit step 2 and track accoding and have a light to medium colour palette for the cards

## 8. Problem Card Hover Background

> so there are problem statement cards and when we hover on them they shows the full problem statement u just need to add the colour of the background same as the card we are hovering on

The `.problem-detail-panel` overlay now inherits the hovered card's background color using `data-active-card` attribute selectors — teal tint for card 1, peach for card 2, lime for card 3, lavender for card 4.

## 9. Timeline Redesign — Laptop & Monitor Rig

> make it look cool the Event Flow / A clear path from idea to demo. roadmap it too boring make it something like a laptop connected to a screen and the wire is the roadmap

Replaced the flat 4-column grid with an illustrated cable rig:
- CSS/SVG **laptop** on the left (shows code lines + blinking cursor)
- CSS/SVG **monitor** on the right (shows a trophy icon)
- A **dashed lime wire** connects them with 4 glowing numbered node dots
- Steps 2 & 4 float **above** the wire; steps 1 & 3 hang **below** — zigzag reading flow
- Cards use glass-morphism styling with `backdrop-filter: blur`
- Collapses to a vertical stack on mobile (≤820px)

## 10. Header Text Colour

> the area where E5 / Enigma 5.0 / Problems / Timeline / Contact is written make the text colour #ED9121

Changed `color` on `.site-header` from `var(--white)` to `#ED9121` (amber). User later updated it manually to `#027c7c` (teal).

## 11. Registration Page

> now create a directing register page i dont want a proper one just so such that it matching the theme don't necessary to be working

Created `register.html` — a themed, non-functional registration page:
- Same fixed header + footer as `index.html`
- Dark `--ink` background
- Two-column split: left info panel (event facts + pills), right glass-card form
- Form fields: Team Name, College, Problem Statement selector, 4×(Name + Email) member grid
- Submit button shows "Submitted ✓" feedback (JS only, no backend)
- Both "Register" buttons in `index.html` now route to `register.html`

## 12. Bolder Nav Text & Header Color Fix

> make text in this area little bolder so that it could be seen easily
> and when scrolled down in phone it hides upwards and scrolling up brings it back

Two changes made:

**Nav text legibility:**
- `color` on `.site-header` changed from `#027c7c` (dark teal, low contrast) → `#ffffff` (white)
- `.nav-links` `font-weight` bumped from `600` → `700`
- Added `letter-spacing: 0.03em` to `.nav-links` for better readability

**Hide-on-scroll (mobile):**
- Already fully implemented from a previous session — no new code needed
- `.site-header.is-hidden { transform: translateY(-110%); }` handles the slide-up
- JS `hideOnScroll()` adds/removes `.is-hidden` based on scroll direction with an 8px threshold to prevent jitter
