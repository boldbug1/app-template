# DESIGN.md

The look of every app made from this template. Read this whole file before making any UI.

## How to use this file

1. Open every image in `design/references/` (1.jpeg to 5.jpeg, 6.png to 10.png) and look at it. Match what you see, not only what this file says.
2. All values (colors, fonts, radius, shadows, spacing, motion) live in `styles/tokens.css`. Use only those tokens. Never write a raw color, font, or pixel value in a component.
3. Use only the components listed in "Components" below. If you need a new one, stop and ask.
4. Before you finish any screen, run the checks at the bottom.

## The direction in one paragraph

**A soft machine with an editorial voice.** Controls look like real objects you can press: glassy buttons, soft shadows, floating windows, small lit lights. The type and layout around them are bold, plain, and quiet: huge tight headlines, lots of empty space, small mono labels. Complexity is hidden. The screen shows only what you need right now.

- **Main look (most screens):** soft Mac/iOS-era realism. References 3, 5, 10.
- **Editorial layer (headlines, labels, loud sections):** references 6, 7, 8, 9.
- **Seasoning (tiny touches only):** retro pixel and old-OS details from 1 and 2.

Do not mix everything on one screen. One screen = main look + at most one touch of the editorial layer + at most one retro detail.

## What to copy from each reference

| File | Copy this | Do not copy |
|---|---|---|
| 2.jpeg | 1px black borders, window title bars, tiny pixel details (like a status line) | Full pixel-art look, dithering everywhere |
| 4.jpeg | Source-list sidebar, orange or pink selected rows, dense but tidy lists | Heavy 2008 gradients on toolbars |
| 3.jpeg | Pill chat bubbles, segmented controls (Everyone / Me), white rows with a hairline border, soft layered shadow, textured background | Blue chat bubble gradients |
| 5.jpeg | Everything is an icon first, and you understand it without reading | The dark glossy kit look |
| 1.jpeg | Glass buttons with a dark rim, buttons that light up pink-red when active, green dot-matrix readout, big glossy knob, small spaced-out caps labels, one slider with real weight | Faux metal, fake screws |
| 6.jpeg | Very short header menu in small mono caps, big light headline, large rounded cards, one clear action per card | Four-color logos, product screenshots as filler |
| 7.png | Heavy tight headline, nav items as small white label boxes with sharp corners, dark feature card, tiny mono tags, dashed divider lines | Grey-green as the only color |
| 8.png | Near-black page, giant white tight headline, thin line art, small corner bracket marks, a thin vertical rule next to short text, one small mono label | Wireframe cube art (make your own) |
| 9.png | Floating cards at different heights, black title tab with mono text on each card, name in a black highlight box, small overlapping "note" cards, one loud flat background color | Real photos of people as default |
| 10.png | Dot-grid background, floating mac-style windows with three dots, glass pill buttons, lowercase wordmark, tiny grey captions like file names, hover a window to see a demo, a little personality (small faces like ^_^) | Blue as the main button color |

## Rules

### Layout
- One idea per screen. If two ideas fight, split the screen.
- Lots of empty space. Content is never packed edge to edge.
- Icon first, word second. A button with a clear icon needs at most one short word.
- Max 2 short sentences in any block of text. Max 6 words in a button.
- Do not center everything. Use offsets, staggered cards, and left-aligned text blocks. Center only a headline.
- Page headers: small, quiet, at most 5 items.
- Show the hidden stuff on hover or click (like the windows in 10), not all at once.

### Type
- Two families: a plain tight sans for headlines and body, and a mono for small labels.
- A third family (dot-matrix) is allowed only for one readout at a time, like in 5.
- Headlines: very large, weight 500 to 600, line height about 0.9 to 1, tight letter spacing.
- Body: regular weight, 16 to 18px, line height 1.5.
- Labels: mono, small, caps or lowercase, wide letter spacing.
- Never use the default Inter font.

### Color
- Soft theme is the default: soft grey-lavender background, near-white surfaces, dark ink.
- One accent: a lit pink-red (from 5). Use it only for the active or most important thing on screen.
- Green dot-matrix color is only for readouts and status lights.
- Loud section themes (sage, ink, pink) are allowed for one full-width section or page at a time.
- Never use purple or blue gradients. Shiny effects stay in the same color family: lighter on top, darker on the bottom edge, never a shift to another hue.

### Surfaces and shadows
- Surfaces float. Use the soft layered shadow token, never a hard black drop shadow.
- Cards and windows: thin hairline border plus soft shadow.
- Window chrome (three dots, title) is allowed on floating previews only, not on every card.
- Backgrounds may have a very faint dot grid or fine texture. Never a photo or gradient wash.

### Buttons and controls
- Primary buttons are glass pills: a thin darker rim, a bright inner top edge, a soft shadow.
- Pressing a button moves it down 1 to 2px and makes the shadow smaller.
- Active controls light up with the accent and a faint glow.
- Toggles, sliders, and segmented controls should feel physical: visible thumb, clear track.
- Editorial pages may use flat sharp label boxes for nav (7 and 8) instead of glass.

### Icons
- Pick one icon set when the app starts and never mix sets.
- Same stroke weight and corner style everywhere. No emoji as icons.

### Motion
- Fast and calm: 150 to 220ms, ease-out. No bouncing or spinning.
- Things that you press, drag, or flip should react right away.
- Hovering a floating window can play its short demo.
- Respect "reduce motion": turn animations off when it is set.

### Words on screen
- Plain, short words. A 12 year old should understand every line.
- No em dashes. No marketing words like "seamless", "powerful", "unlock", "elevate".
- No text that tells the user what to do when the screen already shows it.
- Small personality is good (a tiny face, a lowercase wordmark). Keep it rare.

## Components (build these first, reuse everywhere)

1. **Glass button** (pill, glass, press effect, accent version)
2. **Segmented control** (like Everyone / Me in 3)
3. **Floating window** (rim, three dots, soft shadow, tiny caption under it)
4. **List row** (icon, one line of text, hairline separator, selected state)
5. **Input** (inset look, clear focus ring in accent)
6. **Mono label tag** (small black or white box with mono text)
7. **Readout** (dot-matrix text on a dark strip)
8. **Headline block** (huge tight title plus 1 to 2 short sentences)
9. **Floating card** (title tab, content, offset position)
10. **Toggle and slider**

If a screen needs something else, ask first.

## Banned

- No em dashes
- No clutter. Do not put too much information in one place
- No long descriptions
- No heavy or complex English words
- No purple or blue gradients
- No default Inter font
- No badges (like "active", "new", "beta")
- No default component-library look (default shadcn, Material, Bootstrap)
- No emojis
- No centered hero with three feature cards
- No fake demos or fake command panels
- No generic stock illustrations
- No flat white card with a grey border and 8px radius as the default card
- No mixing icon sets
- No tooltips or helper text that explain obvious things

## Checks before finishing any screen

- [ ] Did I look at the reference images, not only read this file?
- [ ] Are all colors, fonts, radius, shadows, and spacing from `styles/tokens.css`?
- [ ] Is there one clear idea on this screen?
- [ ] Does it have lots of empty space, with text in short blocks?
- [ ] Is the accent used only on the single most important thing?
- [ ] Did I avoid everything in the Banned list?
- [ ] Do the buttons look pressable and react when pressed?
- [ ] Does it still look good on a phone-sized screen?
- [ ] Would this look at home next to references 3, 5, and 10, with a hint of 7 and 9?