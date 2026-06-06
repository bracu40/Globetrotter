I plan on building a guide for the country of Peru, because that is where my family is from and it is a beautiful country that I want to share and spread awareness of.

My primary audience are first-time visitors who know don't really much about the country to excite them about what is to come and inform them of what to look out for.

I want visitors to be amazed at the diversity that Peru has to offer, eager to visit, and surprised that they have not heard of this and didn't visit sooner. I want Peru to become a more popular tourist attraction, and for visitors to feel this as well.

Color definitely reflects Peru's identity. From the red on our flag, to the rainbow that is Vinicunca and the Ican flag, to vibrancy that is in our foods. I definitely plan on taking advantage of this in the website.

Design Intent:

I plan on using red, white, and gold tones to reflect the Peruvian colors.

The Bree Serif font fits Peru's character because it is the closest publically available font to the Bree Peru font with the spiral P that is used for Peruvian tourism.

One visual choice is the use of the Peruvian flag as the banner.

Flexbox Layout Plan:

Home
Content + arrangement
Hero banner (flag image + title overlay), nav bar, intro/map section, newsletter form.
Overall flow is stacked vertically by section.
Desktop columns/items per row
Map area: effectively 1 wide content column.
Newsletter form fields: 3 fields in one row + submit (grid-style).
Smaller screen behavior
Nav wraps.
Map gets taller (16:9 → 4:3 → 1:1 across breakpoints).
Newsletter form switches to single-column stacked fields

Top Attractions
Content + arrangement
Title + attraction cards (image, heading, description).
Cards are in a grid-like layout.
Desktop columns/items per row
3 cards per row.
Smaller screen behavior
Tablet: 2 per row.
Mobile: 1 per row.
Important spacing/alignment/sizing
Equal card gaps and consistent card heights/visual weight.
Centered section title.
Card images should keep fixed height + object-fit: cover for clean alignment.

Food & Drinks
Content + arrangement
Title + vertical list of food/drink cards.
Each card is side-by-side inside: left panel (name + image), right panel (description + traveler type + address + link).
Desktop columns/items per row
Main list: 1 card per row (stacked list).
Inside card: 2-column split (left/right).
Smaller screen behavior
Card internals switch to stacked vertical (flex-direction: column), so image/details are easier to read.
Important spacing/alignment/sizing
Left panel has fixed-ish width on desktop for visual consistency.
Right panel uses vertical spacing between metadata lines.
Link styling needs to stay visible and tappable.

Photo Gallery
Content + arrangement
Title + intro + horizontal carousel of image cards.
Layout is carousel/row-like with scroll and arrow behavior.
Desktop columns/items per row
3 gallery tiles visible at once.
Smaller screen behavior
Medium: 2 visible.
Small: 1 visible.
Important spacing/alignment/sizing
Keep card widths consistent per breakpoint to preserve carousel rhythm.
Horizontal padding/gap should be balanced so arrows and cards don’t feel crowded.
Image height consistency is important for a polished track.

Breakpoints Plan:

The three device sizes I'm designing for are desktop (>=981 px), tablet (641-980 px), and mobile (<= 640 px).

Home
Header (hero + nav)

Desktop: full-width hero, horizontal nav links.
Tablet: keep full-width hero; nav remains horizontal but tighter padding.
Mobile: nav wraps to multiple rows (already done), hero text and spacing should remain readable.
Map section

Desktop: wide map card, 16:9.
Tablet: map becomes taller for readability (4:3 behavior already present).
Mobile: map becomes near-square (1:1 behavior already present), text spacing tightened.
Newsletter form

Desktop: multi-column form fields.
Tablet: can stay multi-column if space allows.
Mobile: single-column stacked fields (grid-template-columns: 1fr already implemented).


Top Attractions
Attractions grid

Desktop: 3 columns.
Tablet: 2 columns (@media max-width: 980px already in CSS).
Mobile: 1 column (@media max-width: 640px already in CSS).
Card internals

Desktop/Tablet: image + text block with consistent card height feel.
Mobile: keep image full-width on top and text below for easiest scanning.

Food & Drinks
Food card list

Desktop: horizontal split card (food-left + food-right) in a vertical list.
Tablet: same layout unless cramped.
Mobile: card switches to stacked vertical layout (flex-direction: column already present under 760px).
Card metadata (best for, address, link)

Desktop/Tablet: shown inline in right pane.
Mobile: keep all metadata but tighten spacing and ensure links are easy to tap.


Photo Gallery
Carousel tiles

Desktop: 3 tiles visible.
Tablet: 2 tiles visible (@media max-width: 900px).
Mobile: 1 tile visible (@media max-width: 600px).
Navigation behavior

Desktop: arrow/button interaction is prominent.
Tablet/Mobile: emphasize swipe/scroll interaction; buttons may remain but should not overlap content.

Mobile should feel meaningful different for
Gallery: mobile should feel like a swipe-first experience (one strong image at a time), not just a shrunken desktop carousel.
Guide cards: switch from side-by-side “info panel” to top-to-bottom storytelling (title/image first, details below).
Home map + form: prioritize map visibility and make form ultra-scannable with larger tap targets and fully stacked inputs.
Nav: wrapping works, but a true mobile nav pattern (menu button/drawer) would feel more intentional than compressed links.