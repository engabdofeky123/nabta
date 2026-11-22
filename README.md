# Nabta Landing Page

Landing page for **Nabta**, an AI & IoT-powered precision agriculture and farm management platform, built as a graduation project at the Faculty of Computer Science and Information Systems, Mansoura University.

The page introduces what Nabta is, the problem it solves, how it works, its features and architecture, the team behind it, and the project roadmap.

---

## Page sections

| # | Section | What it shows |
|---|---------|---------------|
| 1 | **Hero** | Headline, animated farm-zone illustration with pulsing sensor nodes, floating NDVI and leaf-scan cards |
| 2 | **Ticker** | Scrolling strip of platform capabilities (pauses on hover) |
| 3 | **What is Nabta** | Executive summary, animated stat counters, and the three core problems |
| 4 | **How it works** | Five-step pipeline: Sense, Transmit, Ingest and fuse, Analyze, Act |
| 5 | **Features** | Nine feature cards covering all 15 key features from the proposal |
| 6 | **Cost and feasibility** | Zone-based deployment (about 1-3 acres per sensor node) with satellite NDVI interpolation |
| 7 | **Architecture** | Seven-layer system flow plus Clean Architecture, CQRS, event-driven telemetry and independent AI services |
| 8 | **Who we are** | The 10-person team |
| 9 | **Roadmap** | Four project phases |
| 10 | **Deliverables and scope** | Seven expected deliverables, in-scope and out-of-scope items |
| 11 | **Why Nabta** | The differentiation formula: live data + AI diagnosis + predictions + recommendations + marketplace + finance |
| 12 | **Call to action and footer** | Link to the team section and project credits |

All content comes from the Nabta Graduation Project Proposal.

---

## Team

| Name | Role |
|------|------|
| Abdelrahman Mohammed | IoT Engineer |
| Amr Helal | Backend Developer |
| Abdullah Ahmed | Backend Developer |
| Mohammed Ashraf | Backend Developer |
| Mostafa Makram | AI Engineer |
| Mohammed Samir | AI Engineer |
| Abdelrahman El-Deeb | Flutter Developer |
| Hanan Waleed | Flutter Developer |
| Mohammed Magdy | Business Analyst |
| Rawan Galal | UI/UX Designer |

---

## Design

### Color palette

| Name | Hex | Used for |
|------|-----|----------|
| Primary Green | `#2E7D32` | Buttons, icons, accents |
| Dark Green | `#1B5E20` | Hero, headings, footer accents |
| Light Green | `#E9F7EC` | Section backgrounds, tags |
| Accent Teal | `#006B5F` | Labels, gradients, secondary accents |
| White | `#FFFFFF` | Cards, text on dark backgrounds |
| Off White | `#F7FAF7` | Page background |

A few extra tints (a lighter green `#66BB6A` for highlights, soft green borders, and a very dark green for body text and the footer) are derived from the palette.

### Typography

- **Sora** for headings
- **Inter** for body text

Both are loaded from Google Fonts.

### Animations

- Staggered fade-up on the hero when the page loads
- Pulsing sensor rings, drifting leaves, floating cards, and animated zone colors in the illustrations
- Animated dashed signal lines between sensors and the gateway
- Count-up numbers in the stats grid
- Scroll-triggered reveal for sections and cards, and growing progress lines in the pipeline, timeline and architecture
- Hover lift on cards and buttons

Scroll-triggered effects use the CSS `animation-timeline: view()` feature. In browsers that do not support it, content simply appears without the scroll effect. Visitors who have "reduce motion" turned on in their system settings see no animations at all.

### Responsive layout

Section padding and side margins scale with the screen width, and card grids reflow automatically from desktop down to small phones.

### Accessibility

Navigation and buttons are real links, decorative graphics are hidden from screen readers, informative illustrations carry text descriptions, and text colors are chosen for readable contrast against their backgrounds.

---

## Technical notes

- The page is a single self-contained **Design Component** file, `Main.dc.html`, plus a small `canvas.json` index. It was built and published on the Claude Design canvas.
- The file uses the Design Component template syntax (`<x-dc>`, `{{ }}` placeholders and `<sc-for>` loops) and expects its runtime script, so it is meant to be opened and edited on the canvas rather than opened directly as a plain `.html` file in a browser. To use the page elsewhere, export it from the canvas's Share menu.
- Repeated content (features, team, roadmap phases, architecture layers, and so on) lives in the `renderVals()` function at the bottom of the file. To add a team member or change a feature, edit the matching array there and the page updates.
- Animations are pure CSS, with no JavaScript animation libraries.

---

## Editing the content

| To change... | Edit... |
|--------------|---------|
| Team members | the `team` array in `renderVals()` |
| Feature cards | the `features` array |
| Roadmap phases | the `phases` array |
| Architecture layers and principles | the `layers` and `principles` arrays |
| Deliverables and scope | the `deliverables`, `inScope` and `outScope` arrays |
| Ticker words | the `ticker` array |
| Headlines and paragraphs | the text directly in the markup |
| Colors | the inline `style` values and the `<style>` block in `<helmet>` |

---

## Credits

Nabta graduation project, Faculty of Computer Science and Information Systems, Mansoura University, 2026.
