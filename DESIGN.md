---
name: Jeison Sosa Personal Site
version: 1.0
description: Minimal black-and-white design system for jsosa.xyz, optimized for essays, public wiki pages, small tools, and future slide decks.
sourceFiles:
  - style.css
  - index.html
  - wiki/index.html
colors:
  ink:
    value: "#050505"
    role: Primary text, dark cards, dark controls, selection background.
  paper:
    value: "#ffffff"
    role: Page background and light-on-dark text.
  muted:
    value: "#646464"
    role: Metadata, labels, secondary text, quiet captions.
  wash:
    value: "#f3f3f3"
    role: Light card surface, inline code background, subdued UI blocks.
  washStrong:
    value: "#e9e9e9"
    role: Hover surface and soft focus support.
  reverse:
    value: "#ffffff"
    role: Text on ink surfaces.
typography:
  display:
    fontFamily: "Familjen Grotesk"
    fallback: "IBM Plex Sans, sans-serif"
    weightRegular: 600
    weightStrong: 700
  body:
    fontFamily: "IBM Plex Sans"
    fallback: "-apple-system, BlinkMacSystemFont, Segoe UI, sans-serif"
    weightRegular: 400
    weightMedium: 500
    weightStrong: 700
  mono:
    fontFamily: "SFMono-Regular"
    fallback: "Consolas, Liberation Mono, monospace"
typeScale:
  pageH1:
    fontSize: "clamp(2.4rem, 5.4vw, 4.4rem)"
    lineHeight: "0.98"
    weight: 600
  articleH1:
    fontSize: "clamp(2rem, 4.6vw, 3.45rem)"
    lineHeight: "1"
    weight: 600
  sectionLabel:
    fontSize: "11px"
    lineHeight: "1.1"
    weight: 800
    letterSpacing: "0.08em"
    transform: uppercase
  articleH2:
    fontSize: "clamp(1.12rem, 1.7vw, 1.4rem)"
    lineHeight: "1.15"
    weight: 650
  articleH3:
    fontSize: "1.08rem"
    lineHeight: "1.2"
    weight: 700
  body:
    fontSize: "16px"
    lineHeight: "1.58"
  articleBody:
    fontSize: "clamp(1.02rem, 1.45vw, 1.2rem)"
    lineHeight: "1.62"
spacing:
  pageXDesktop: "20px gutter inside min(100% - 40px, max width)"
  pageXMobile: "16px gutter inside min(100% - 32px, max width)"
  sectionGap: "86px desktop, 68px under 900px"
  cardGap: "10px between cards"
  cardPadding: "16px to 18px"
  cardInnerGap: "22px between title and description"
radii:
  md: "8px"
layout:
  textWidth: "860px"
  wideWidth: "860px"
  labelColumn: "minmax(120px, 204px)"
  contentColumn: "minmax(0, 860px)"
  breakpointTablet: "900px"
  breakpointMobile: "640px"
motion:
  fast: "160ms ease"
  hoverLift: "translateY(-1px to -2px)"
components:
  card:
    radius: "8px"
    padding: "16px to 18px"
    gap: "22px"
    height: "content-sized, no decorative fixed min-height"
  button:
    radius: "8px"
    minHeight: "38px"
    paddingInline: "14px"
    weight: 800
  search:
    surface: "ink"
    inputSurface: "paper"
    inputHeight: "54px"
---

# Design System

## Purpose

This file is the visual contract for `jsosa.xyz`. It should help future agents design new pages, wiki surfaces, tools, and slide presentations without drifting into generic startup UI or oversized hero typography.

The site should feel like a precise personal knowledge and writing surface: calm, confident, monochrome, readable, and spare. It should not feel like a marketing landing page, a dashboard, a magazine clone, or a component demo.

Use `style.css` as the implementation source of truth. Use this document as the design source of truth.

## Design Principles

- Minimal, not empty. Let spacing, type weight, and contrast do the work.
- Black and white first. Use grayscale only for hierarchy, not decoration.
- Sans-serif only. The site should feel direct, modern, and unornamented.
- No line-divider architecture. Avoid horizontal rules, bordered rows, and separator-heavy layouts. Separate with whitespace and layout.
- Headings should be quiet. Do not return to oversized hero typography.
- Cards should hug content. Avoid fixed card heights unless an actual grid or tool requires stable dimensions.
- Components should feel designed, but not precious. Prefer restraint over flourish.
- The writing is the product. Do not let UI styling compete with essays and notes.

## Brand Voice

The visual voice is terse, literate, and useful. It should support a product manager and writer who values systems, learning, operating ideas, and public notes.

Good adjectives:
- Minimal
- Crisp
- Monochrome
- Editorial
- Practical
- Dense-but-readable
- Calm

Avoid:
- Loud
- Cute
- Ornamental
- Gradient-heavy
- Card-stacked SaaS marketing
- Oversized type as the primary personality
- Thin divider systems
- Beige, cream, purple, blue-slate, or warm coffee palettes

## Color

Use a strict monochrome palette.

- `#050505` is the only true black. Use it for primary text, dark surfaces, and primary controls.
- `#ffffff` is the page canvas.
- `#646464` is the main muted tone for labels, dates, metadata, captions, and secondary content.
- `#f3f3f3` is the default light card and soft block surface.
- `#e9e9e9` is for light hover states and soft focus support.

Do not introduce accent colors casually. If a future feature genuinely needs status colors, define them narrowly and keep them subordinate to the monochrome system.

## Typography

Primary body type is `IBM Plex Sans`. Display type is `Familjen Grotesk`.

Use display type for:
- Page H1s
- Article H1s
- Card titles
- Compact title-like UI

Use body type for:
- Paragraphs
- Form inputs
- Search
- Metadata
- Buttons
- Slide body text

Use monospace only for:
- Code blocks
- Inline code
- Formula-like content

Do not use serif fonts. Do not reintroduce Cormorant, Georgia, or other literary serif styling.

Do not use Inter or Space Grotesk as the primary personality. The current pairing was chosen to avoid default AI-generated UI taste while staying clean and sans-serif.

## Type Scale

Headings should be modest. The site intentionally moved away from billboard headings.

Use these current defaults:

- Page H1: `clamp(2.4rem, 5.4vw, 4.4rem)`, weight `600`, line-height `0.98`
- Article H1: `clamp(2rem, 4.6vw, 3.45rem)`, weight `600`, line-height `1`
- Section label H2: `11px`, uppercase, weight `800`, letter-spacing `0.08em`
- Article H2: `clamp(1.12rem, 1.7vw, 1.4rem)`, weight `650`, line-height `1.15`
- Article H3: `1.08rem`, weight `700`, line-height `1.2`
- Article body: `clamp(1.02rem, 1.45vw, 1.2rem)`, line-height `1.62`

Rules:
- Do not use viewport-width scaling that makes headings dominate the page.
- Do not use negative letter-spacing.
- Do not make H2s feel like hero headlines.
- Prefer hierarchy by placement, weight, and whitespace rather than size.

## Layout

The site has two measures:

- Text measure: `860px`
- Wide measure: `860px`

All pages use the `860px` measure. Homepage and wiki index pages may use grids inside that measure, but should not expand to a wider canvas.

Default section layout on desktop:

- Left label column: `minmax(120px, 204px)`
- Right content column: `minmax(0, 860px)`
- Column gap: `56px`
- Section bottom spacing: `86px`

Under `900px`, sections collapse into a single column. Under `640px`, use a `32px` total page gutter.

## Spacing

Spacing should feel deliberate and calm.

- Page gutters: `40px` total desktop, `32px` total mobile.
- Section rhythm: generous vertical separation between content groups.
- Card grid gap: `10px`.
- Card padding: `16px` or `18px`.
- Internal card gap: `22px` between title and description.
- Paragraph bottom margin: `18px`.

Avoid:
- Decorative spacers
- Divider lines
- Large empty space inside cards
- `justify-content: space-between` for text cards
- Fixed card heights unless layout stability requires it

## Cards

Cards are used for projects, wiki pages, related links, and search results.

Project and wiki cards:

- Use `display: flex; flex-direction: column`.
- Use `gap: 22px`.
- Use content-sized height.
- Use `border-radius: 8px`.
- Use `background: #050505; color: #ffffff` for selected/dark cards.
- Use `background: #f3f3f3; color: #050505` for light cards.
- Hover can lift by `translateY(-2px)`.
- Dark cards must keep white text on hover.
- Light cards may move to `#e9e9e9` on hover.

Do not:
- Add borders to cards.
- Put cards inside cards.
- Use fixed min-heights that create dead space.
- Push card title and description to opposite ends.
- Use shadows.

## Links And Actions

Inline text links are underlined. Structural links such as cards, back links, buttons, and footer links are not underlined.

Buttons:

- Black background, white text for primary actions.
- `8px` radius.
- `38px` minimum height.
- Bold text.
- No borders.
- Avoid pill buttons unless the element is a tag.

Back links:

- Small uppercase label.
- Muted by default.
- No border or divider.

## Forms And Search

Search is a black panel with a white input.

Use:

- Panel padding: `18px`
- Panel radius: `8px`
- Input min-height: `54px`
- Input background: white
- Input text: black
- Label: uppercase, `12px`, bold

Do not make search look like a SaaS dashboard filter bar. It should feel like a compact utility embedded in an editorial page.

## Wiki Pages

Wiki index pages use the same `860px` canvas as articles. They can contain card grids, but the page itself should not widen beyond the universal measure.

Wiki card pattern:

- Two columns on desktop.
- One column under `640px`.
- Descriptions are visible in featured/listing cards.
- Compact cards hide descriptions and should be short.
- Use alternating dark cards sparingly, currently via positional pattern.

Tags:

- Black pill background.
- White text.
- Small, bold, compact.
- Keep `border-radius: 999px`.

Related pages:

- Use compact light cards.
- Hover to black with white text.
- Two columns on desktop, one column on mobile.

## Articles And Essays

Articles should be the quietest part of the site.

Article rules:

- Use the `860px` text measure.
- Keep H1 modest.
- Keep H2s close to the text scale.
- Body copy should be readable and slightly larger than default browser text.
- No drop caps.
- No serif emphasis.
- No divider lines between sections.

Figures and simple diagrams:

- Use light surfaces and black surfaces.
- Keep diagram text compact.
- Use real spacing and labels, not decorative borders.

## Small Tools

For tools such as `profitable.html`, keep the same monochrome language:

- Sans-serif only.
- No serif heading overrides.
- Light panels use `#f3f3f3`.
- Inputs are white inside light panels.
- Primary action is black.
- Avoid line-heavy form design.
- Status/result panels may use black backgrounds when emphasis is needed.

Tools can be denser than essays, but should not become dashboards.

## Slide Presentation Guidance

Future slide decks should use this same system so presentations feel connected to the site.

Recommended slide size:

- 16:9 widescreen.

Slide typography:

- Title: Familjen Grotesk, weight `600`, large but not oversized.
- Body: IBM Plex Sans, regular or medium.
- Section labels: small uppercase IBM Plex Sans, weight `800`, tracking around `0.08em`.
- Avoid giant headline-only slides unless the message truly needs it.

Slide palette:

- Default background: white.
- Default text: `#050505`.
- Secondary text: `#646464`.
- Dark chapter slides: `#050505` background with white text.
- Light panels: `#f3f3f3`.

Slide layout:

- Use a clear left label or kicker when helpful.
- Keep content in a readable column, not edge-to-edge.
- Use two-column layouts for comparison.
- Use small card grids for examples, but keep cards content-sized.
- Avoid decorative lines, gradients, icon clutter, and stock imagery.

Useful slide types:

- Title slide: small kicker, modest title, subtitle.
- Section divider: black background, white title, minimal text.
- Argument slide: one clear heading, one concise paragraph, optional bullets.
- Comparison slide: two light panels or one light and one dark panel.
- Framework slide: 3 to 5 cards with short labels and brief descriptions.
- Evidence slide: muted source/date label, clear excerpt or statistic, short interpretation.

Charts:

- Prefer black marks on white canvas.
- Use muted gray for axes, annotations, or secondary series.
- Label directly instead of relying on legends where possible.
- Avoid colorful chart palettes unless the data requires more than grayscale.

## Component Rules For Future Agents

When adding a new component:

1. Start from existing tokens in this file.
2. Use white, black, or light gray surfaces.
3. Use `8px` radius for cards and controls.
4. Avoid borders unless interaction clarity requires one.
5. Avoid shadows.
6. Keep card content stacked naturally.
7. Do not add decorative dividers.
8. Check desktop and mobile.
9. Ensure hover states preserve contrast.
10. Keep text widths and grid containers aligned to the universal `860px` measure.

When adding a new page:

1. Decide whether it is an article, index, wiki page, or tool.
2. Use article text measure for reading pages.
3. Build grids and tool layouts inside the universal `860px` measure.
4. Keep headings minimal.
5. Use labels for sections rather than large section titles.
6. Verify the page at desktop and mobile widths.

## Accessibility

- Maintain strong contrast for all text.
- Dark cards must use white or near-white text.
- Light cards must use black text.
- Hover states must not reduce contrast.
- Do not rely on color alone for important state.
- Keep focus states visible, especially in forms and search.
- Do not let text overflow cards or buttons.

## Anti-Patterns

Do not add:

- Cream/beige editorial palette
- Purple or blue gradients
- Giant H1 hero treatment
- Serif headings
- Heavy horizontal rules
- Divider-heavy lists
- Nested cards
- Large fixed-height cards with dead space
- Drop shadows
- Rounded marketing pills everywhere
- Decorative icons without a clear job
- In-app explanatory text about how the UI works
- Landing-page hero layouts for ordinary tools or writing pages

## Implementation Notes

- `style.css` should remain the single stylesheet for the main site and wiki.
- `wiki/wiki.css` should not return.
- Keep new CSS close to existing patterns before inventing new abstractions.
- If adding a design token, add it here and in `:root`.
- If changing the type scale, update both this file and `style.css`.
- If a page has inline CSS, make it conform to this system rather than becoming a separate visual language.
