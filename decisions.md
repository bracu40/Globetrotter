# Globetrotter — Decisions Log

## Milestone 0: Setup and Planning
- Destination chosen: Peru
- Primary audience: first-time travelers
- One design decision that reflects the destination: the use of color that reflects our diversity.
- Wireframe format used (hand-drawn / Figma / other): wireframe.cc

## Milestone 1: HTML Structure
_Something I chose were the divs that separated the left and right sides of the guide cards to be able to align with my vision for the cards._
_Something Claude helped me with was the photo gallery to have the carousel feature._
_One place where the wireframe guided a specific decision about structure was the Top Attractions page with the grid of cards for each attraction._

## Milestone 2: CSS Styling
_One color choice I made was the body background gradient of from left to right, gold to red. This fits the red of the flag and the abundant presence of gold that we have._
_Once Claude choice I rejected was the use of a fixed number of buttons to transition between the images in the photo gallery. This would be a hard-coded value that would not allow variation if more images are added, or if the _One style that didn't look right first was the embedded map, so I edited the sizing and format of it._

## Milestone 3: Flexbox Layout
_I intentionally used flex-direction: column on .food-list so the Food & Drinks section reads like a guided list (one card at a time) instead of a dense gallery. That supports the “travel guide” feel and keeps each item’s details (description, traveler type, address, link) readable._
_Claude initially suggested a pinned bottom-right newsletter form on the home page. That didn’t match my plan for a clean, document-style flow, so I changed it to a centered bottom section in normal page flow (.newsletter-section), which feels less intrusive and more consistent with the rest of the site._
_The newsletter form became hard to control with plain sequential labels/inputs, so I wrapped each label+input in a .form-field container. That made the grid behavior predictable (multi-column on desktop, stacked on mobile) and fixed spacing/overflow issues without fragile CSS hacks._


## Milestone 4: Responsive Design
_I ended up using 980px, 900px, 760px, 640px, and 600px. 980px: switches Top Attractions from 3 columns to 2 before cards feel cramped.
900px: reduces gallery from 3 visible cards to 2 (carousel readability).
760px: stacks newsletter form and guide cards into single-column internals.
640px: wraps nav links and forces attractions to 1 column for small phones.
600px: gallery goes to 1 card at a time; map becomes square (1:1) for better mobile viewing._
_One section where mobile is genuinely different is the guide.html food cards. On desktop, each card is a horizontal split (image/title left, details right). On mobile (<=760px), cards switch to vertical stacking (flex-direction: column), so content becomes a scroll-friendly story block instead of a compressed side-by-side layout._
_One Claude breakpoint suggestion I rejected was full consolidation to only 3 global breakpoints (desktop/tablet/mobile) because different components broke at different widths._
_One Claude breakpoint suggestion I accepted was the intent (clear tiered behavior), but kept component-specific breakpoints (980/900/760/640/600) so the gallery, map, form, and card layouts each transition where they actually need to._

## Stretch Features
_I added a Google Maps embedded map of Peru in the home page._
_I used CSS grid._
_I will deploy to Github pages._
_I created a sign-up form for a travel newsletter._
_I used CSS carousel for the photo gallery._