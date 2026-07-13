# Layout and composition: Artyom Gorbunov's doctrine (bureau.ru, "Typography and Layout")

A deduplicated reference for assessing any page, screen, poster, or table. Terms are canonical (studio jargon); key Russian originals appear once in parentheses at first definition. Source: 4 "canon" digests (anchor objects, inner/outer, modularity, primitives, taste, the video era) + 18 sweep-digests of all of bureau.ru's advice columns — where a point repeated, only the single strongest formulation was kept.

---

## 1. Basic laws

**"Modular layout (модульная вёрстка) is the division of rectangles."** A page is cut into neat, non-overlapping rectangular modules, aligned by width/height, that together make up the full rectangle of the page; empty space is a module too, not a leftover. Its lineage: Japanese tatami mats → the 20th-century Swiss modular grid → the web. What's different on the web: content has unpredictable length, so modules must flex instead of being rigidly fixed into cells.

**"Man's greatest invention is not the wheel but the rectangle."** Books, websites, architecture — it all comes down to rectangles dividing into rectangles. Modularity isn't a style; it's the operating system of layout.

### The inner-and-outer rule (правило внутреннего и внешнего)

**"Inner ≤ outer"** — for an object to read as a single whole, the distances inside it must be smaller than the distances separating it from its neighbors. This holds at every scale: strokes < letters < words < lines < paragraphs < modules < page. Examples of failure: letter-spacing ≈ word-spacing — words clump together (fixed by widening word spacing or tightening letter spacing); line-height ≈ letter-spacing — text reads as a "checkerboard" (fixed by increasing line-height).

**What matters is contrast, not a specific ratio.** There's no universal numeric proportion — dial expressiveness up or down by adjusting the inner/outer contrast rather than memorizing particular figures.

**The rule cascades up a block's level.** A headline plus a subheading is also a block: if the subheading crowds into the headline's line-height, that's the same sin one level up. The classic "tunnel vision" mistake is fixing the line spacing inside a block while forgetting that the block as a whole also needs inner < outer relative to its surroundings.

**The inner-and-outer rule can conflict with the anchor-object rule — and that's normal.** Proximity works through closeness (what's near reads as connected, what's far doesn't), but a closed rectangle (a frame, a fill) unites its contents regardless of internal spacing. When Google's designers imposed a modular grid on a simple navigation list, there was no technical error, but the solution "looks too overwrought" — that treatment suits data tables, not menus. The rules are independent forces that sometimes conflict with no "wrong" answer.

### Anchor objects (якорные объекты) + anti-air (анти-воздух)

**An anchor object** is a module's most conspicuous element (an illustration, a large headline, a fact-object, a logo, a pictogram). The rule: an anchor object gravitates to a corner of the rectangle or to its *visual* center (the visual center sits higher than the geometric one — compensating for "gravity"). An alternative is to pin the object to one *side* of the rectangle for a calm, stable feel.

**Hierarchy of pulling power:** illustration > large headline > logo/mark/number > text (the most neutral).

**Anti-air is mandatory.** On the side opposite the anchor object there needs to be a contrasting empty (or less dense) area, or the object won't read as anchored — the construction "loses its footing" with no support. A beginner's mistake is forgetting the anti-air.

### The gravitational metaphor of proximity

**The perceived connection between elements is proportional to visual mass (size, weight, color, a colored fill) and inversely proportional to distance.** Control the sense of connection or separation with both parameters at once, not just spacing — increasing an element's mass draws it toward its neighbors just as surely as physically shrinking the distance does.

### Unity of rectangles

**The condition for modularity: rectangles don't intersect, don't encroach on one another.** Stretching a side block down to the bottom of the layout is a decision made in context (a dense illustration against light text), not a rigid rule.

**A weak construction is one where the top row forms a clean axis while the rows below "try to play at being a rectangle" with it but fall short.** Check whether the heights of the left/right (or top/bottom) parts are balanced enough to form a genuine rectangle, not an approximate one. The "Occam-Ilyahov razor": merge repeating captions into a single phrase ("You selected 2 rooms, total cost — 10,000 rubles") instead of three separate lines that break the rectangle apart.

### Point, line, rectangle — the primitives of layout

**"Point, line, and rectangle are the primitives of layout that make up the geometry of any page."**
- **Point** (including the circle) — a "selfish" shape with a single focal center; use it sparingly: letters, numbers, logos, pictograms, cropped photos. "A circle doesn't like competition" — it's the most aggressive shape, instantly pulling attention; swap circles for other shapes when you need to lower visual aggression and redirect attention to the content itself (faces instead of frames, for instance).
- **Line** — a line of text: "a convenient, readable, laconic, calm element," better anchored to the top or bottom edge of a module than stretched across the full width; works well for menus.
- **Rectangle** — the universal, "most technological" shape: it divides space with no waste, the unit of the modular grid. Success in modular layout equals finding the best rectangular arrangement, full stop.

### Proximity theory

**Design the page by proximity theory: identify 1–3 of the largest blocks of meaning ("dense celestial bodies") around which the secondary ones are arranged.** Separate information by distance rather than by frames or rules — for example, in a bilingual menu, remove the vertical dividing rules between columns and use proximity theory instead of lines.

### Breaking out of the rectangle

**The world's information is volumetric and multidimensional — sometimes typography must step outside the flat rectangle to represent it honestly.** Precedents: a 19th-century German map where the names of seas and rivers followed the shape of the coastline instead of a grid; Newton's manuscripts, where notation spilled past rectangular borders to express connections; contemporary cases — Sam Winston's experimental typography, The Guardian's masthead playing with its own frame, Food Daily's captions wrapping around the food's outline (a cartographic tradition). The rule: modern typography is modular by default — stepping outside the rectangle is earned only when the shape or dimensionality of the content genuinely demands it, not as decoration.

### An element's syntactic role precedes its form

**"Every interface element has its own syntax, its own 'part of speech' — a page is read like a text: an element's wrong syntax is a design error."** A functional device can't be applied decoratively: if a dotted underline means "an action without a page reload" within the system (bureau slang for this: a "quasi-link," a "whatchamacallit-link"), it can't simultaneously be used just for decoration — otherwise the notation system lies. The same goes for color: "blue should be clickable, and clickable should be blue" — don't confuse a visual language tied to one function with using it for another.

---

## 2. Modular layout and grids

**Definition:** modular layout = the division of rectangles (see §1). Any given section can be well composed (modular, anchored, rhythmic) with no overarching grid for the whole publication — but pages built on a single shared grid "generally look more unified" at the scale of an entire site or publication. A grid also carries brand elements (fact-objects, half-column call-outs) consistently and works as a templating system that speeds up production. Grid discipline and the expressiveness of a particular section don't contradict each other.

### Column rhythm: don't repeat it on adjacent "floors"

**The main principle: "don't repeat the rhythm on adjacent floors."** A reader perceives a uniform rhythm of identical columns as a signal that "this is one type of content" — they'll try to match unrelated blocks by that cue. When combining several column grids within one block, break the rhythm between neighboring "floors" to signal a change in content type or hierarchy level. There's no formula — decide by meaning (shape, proximity, size), not grid arithmetic. Don't make columns the same height or width on purpose — the reader orients by the shape of the text, by proximity, and by element size, not by an invisible grid.

**Layout automation should encode this editorial judgment, not ignore it.** "Most information sites look like an interface to a faceless database" — fight this by baking grouping-by-significance and rhythm alternation into the layout algorithm (neighboring cards shouldn't sit on the same grid), borrowing the discipline of hand-set print layout.

### When to break the grid

**A column needs ≥5% breathing room relative to the window width.** The main text column needs "breathing room" from the next column: a rule of thumb is to leave at least 5% of the window's width free to the right of the main column, even inside a strict grid (example: bureau.ru's own 4-column grid).

**"Grouping by meaning outranks obeying invisible lines."** Break the grid whenever meaning calls for it — that's not a violation of the rule, it's the application of a higher-priority rule.

**"We often break the grid when meaning demands it."** The number and width of a historical grid ("12 columns, 960px") carries no significance on its own in a responsive web; an element spilling past the content's edge risks extra scrolling on mobile — instead of breaking the grid, reframe the task with devices like a "sticker," a "corner fold," a "tab," a narrow inset line, or expand-on-click.

**A regular grid tempts you to forget hierarchy.** "A regular grid makes it easy to forget that a page has primary and secondary elements" — the method: place the primary content in the center first, then build the supporting elements around it. The real pleasure of layout isn't in aligning to a grid but in correctly segmenting and subordinating material; that's the core skill, not grid mechanics.

**Don't split a single block of meaning across a column break** — for example, one day's schedule shouldn't fall across a column boundary in a two-column program layout. Mixing sizes or styles of headings that look similar creates confusion — set up a clear hierarchy so the schedule "stands out to the eye" at first glance.

### Margins, padding, and proportional tension

**"Equal vertical and horizontal margins are a sign of weak, amateur, careless layout."** Make the bottom margin bigger than the top one to compensate for the visual "weight" of the content. Within a modular grid: "the distances around a module's horizontal border can't be equal" (for instance, the padding above and below a rule or a colored fill shouldn't match).

**Square margins aren't a crime** (example: Mindbox's flexible logo box, where the box's shape dictated square margins), but the default rule runs the other way: most formats benefit from proportional *tension* in their margins rather than passive symmetry — "any format benefits from tension in its margin proportions." Prefer rectangular (asymmetric horizontal/vertical) margins over square ones — "tension in margin proportions" reads better than the neutrality of a square.

**Asymmetric margins are a book tradition.** For a magazine or book page: a generous bottom margin; for a magazine specifically — "smaller outer margins, leave a reserve on the inner one" (for the binding/gutter). Additionally: drop the paragraph indent right after a column break, balance text across 1–2 columns, contrast the standfirst and body text typographically, and adjust hyphenation for a clean rag.

**Aligning text to the module is a matter of taste.** The position of the text's baseline relative to the grid module sits "somewhere between x-height and cap-height — by taste"; there's no fixed rule here, it's an aesthetic decision.

### Centering and modular thinking as an escalation of complexity

**"Your page is a spread with its own margins."** Center the logo on the page (not on the browser window); when a module is falling apart, fix it with escalating complexity: a colored fill/rule → aligned columns → "a collection of Swiss modules." Don't jump straight to the most complex device — escalate only when necessary.

### Why you need a grid at all

A grid is a tool for unifying at the scale of a publication or site, not dogma for a single page. It provides: (1) visual unity across sections; (2) a consistent carrier for brand elements; (3) production speed as a templating system. Within it, sections can still vary expressively.

**The historical reference point is the 12-column, 960px grid**, but grid mechanics isn't the main skill. "We don't have a standard grid for every project… we often break the grid when meaning demands it" — the number of columns and the pixel width don't decide anything on their own; what decides is the segmentation and subordination of material (see above).

**Divide content into columns by cumulative size, not by element count.** An equal number of cards or articles in two columns with a different total volume of material makes one column visually "scrawnier" than the other — count the area of the content, not the number of pieces.

**Module density matches the format's genre.** Modules on information-dense sites are usually packed tight (minimum air per unit of meaning); mini-formats (widgets, cards for mobile summaries), conversely, need a surplus of air relative to their content volume — don't carry one genre's density into another mechanically.

### Unity of rectangles at the scale of a table or form

**A form is also a modular construction.** A long form doesn't have to be broken into steps — it's better to group fields into large logical blocks ("Trip," "Travelers," "Payment"), avoiding a "checkerboard stacking" of scattered fields; align labels to one side, and drop self-evident labels on buttons. Each logical group is its own rectangular module, with inner < outer spacing relative to the neighboring groups.

---

## 3. Six basic elements

**"Layout tasks come down to placing these elements."** Everything else is their composition: headline (names the page or block), body text (the main message), illustration (image), control (an input field or button), hyperlink (a colored, underlined jump), caption (for an illustration or a control). Elements may merge functions (fewer entities), but they must never blend visually.

**The cardinal sin is "layout with lumps" (вёрстка с комками)** — like undercooked semolina porridge, where elements are jumbled together instead of being neatly separated. The test: can a reviewer tell one basic element from another on the page without hesitation?

### Headline

**A triple function:** it grabs attention, orients the reader by meaning, and organizes the page — it's not just a brief summary.

**Default form:** large, uniform case (usually lowercase with an initial capital), **no period at the end.** "No periods at the end of titles, headlines, captions, or table labels" — the test: is it a nominal sentence (no predicate)? A question mark or exclamation point is kept.

**Syntactic consistency is mandatory.** Mixing styles within a single headline "gives away amateur layout." Break lines only at logical points, never leaving a lone preposition or conjunction at the start of a new line.

**A headline must "cover" its text module**, visually separating it from its neighbors. It's highly undesirable to split a headline apart from the start of the text; secondary elements (links, tags) should move to the end of the block. Too many line breaks "looks complicated and ugly" — fix it with a compound headline, a different size, or an editorial cut.

**Subheading hierarchy (in a text article):** level 2 — a larger size plus a two-line indent; level 3 — bold weight with no indent; **"fourth-level headings are forbidden in any self-respecting publication."**

**For a page's first (main) illustration, a headline above it isn't critical** — in effect, it functions as the headline for the whole page, not for a separate module.

### Body text

**Column width: 60–70% of the window's width, with a max-width cap.** Long lines require increased line-height.

**The shape of the text determines the reading order.** A single column: the eye moves down with no obstruction; a column broken by an illustration interrupts reading, and the eye "hunts for the continuation." In multi-column layouts, it's critical that all columns align at the top — inconsistent module alignment breeds unwanted pseudo-modules.

**Lists need a summarizing lead-in or a heading** — a list with no introduction hangs with no context.

**A block of text must keep its rectangular shape "through all its mutations."** When broken up by subheadings or columns — shrink the sizes and the type size, and increase the granularity of elements from top to bottom.

### Illustration

**"An illustration grabs attention faster than a headline"** — it must be recognizable; avoid "meaningless, unidentifiable landscapes."

**"Crop until it screams"** — cut away everything extraneous with no amputating of whole figures; edges should be crisp, not "clouds fading into nothing."

**Horizontal illustrations feel natural; vertical ones feel more dynamic.** Don't distort proportions when scaling.

**Canonical vertical order: illustration → headline → text → links** — this matches the natural reading order. An illustration on the left creates an "armpit" effect that separates the headline from the text — an illustration on the right is preferable. **"Nothing looks as ugly and unreadable as text wrapping around an illustration on the right."** A purely vertical stack has no "armpit" problem by construction; if the photo sits top-left, the break pushes the text's left edge further right than the headline's left edge, "breaking the natural reading order" — move the photo to the right instead.

**Break the default "image → headline → text" order only deliberately** (exceptions: a homepage-level headline, a feed of images with no text, free-form text pages) — otherwise the eye "jumps up and down," breaking the flow of reading.

### Control

**Ranked equal to headlines and body text.** Three classes of form:
- **point-shaped** (icons, checkboxes) — compact, with a strong center, but a poor team player in groups;
- **linear** (buttons, input fields, sliders) — read well in a row, stretch horizontally, look bad stretched vertically;
- **rectangular** (text areas, charts, maps) — large in area, and become anchor objects of the page in their own right.

**The minimum gap between controls is roughly two spaces**; size should match the surrounding elements; sort and align them, or the page reads as clutter.

**A button's internal padding is asymmetric: sides bigger than top/bottom** — "this should always be done when designing buttons"; equal padding on every side visually squeezes the button's text and reads as unfinished work.

**A control's shape must hint at its function, not just stand out visually.** A round element that's actually a time picker is misleading: "the problem with this element isn't its round shape, it's that its shape gives no clue what it is" — shape should signal the interaction it supports, not merely serve as decoration or emphasis.

**Field labels: left is preferable to above.** "Labels to the left of fields are preferable — the signifier and the signified aren't mixed together"; the eye glides down a column of labels with no jumping between lines. Labels above a field are a compromise only when width is genuinely scarce (mobile or narrow forms).

### Hyperlink

**A basic layout element, judged on three axes:** recognizability (blue plus underline is easiest to spot), ease of tapping (text of sufficient length, spacing from neighboring links, a color change on hover), and informativeness (the link's text should name what's behind it).

**Underline the whole phrase, including prepositions and conjunctions** — "the styling declines [like a grammatical case]": neighboring punctuation (a comma, quotes, brackets) takes on the link's color and styling, or the eye trips over a "break in the sentence."

**Never let a single link wrap to a new line** — shorten long headlines instead. Group links (menus, lists) with a minimum gap of **about two spaces**.

**"The styling declines" onto punctuation too.** If a comma, quote mark, or bracket follows a colored link, color it to match the link — otherwise the eye trips over a "break in the sentence" at the boundary. A refinement: if the link is already wrapped in quotation marks and ends with a comma, color that comma like ordinary text, but don't underline it — otherwise the underline spills onto punctuation that doesn't belong to the link.

### Caption

**A caption is a "bridge" to the main text.** It accompanies illustrations, controls, even hyperlinks. Skip the caption when the image is self-evident or already sits next to a headline or description.

**Images:** caption below or beside. **Input fields:** caption to the left or above — visible before the user starts to act.

**Leader lines should be ≤20% black**, must not cross one another, should overlap the image as little as possible, and should be long enough to read cleanly. Drop the leader line altogether where the object is already locally set apart and its nearby caption is self-sufficient — reserve leader lines only for genuinely ambiguous cases of attachment.

**Styling:** the caption's size/weight is smaller or lighter than the body text; **no period at the end**; a colon after a field's caption is optional.

---

## 4. Hierarchy and composition

### Dominant and supporting illustrations

**Build an explicit hierarchy between the main illustration and the supporting one.** A row of identical images above the text is calm but dull, and it eats the window's entire width. The best pattern: the supporting image sits next to the text, while the dominant one overlaps or sits on top, giving instant hierarchy. A supporting photo can sit in the headline's "armpit," but it must not wedge itself between the headline and the start of the body text.

**Three basic layouts:** a row of images above the text; one image on top plus one at the side; a supporting image in the headline's "armpit" (with no detaching the headline from the start of the text).

**A dominant illustration says unambiguously: "the tour starts here."** A secondary photo should never compete in size with the main one.

### Homepages and landing screens: four archetypes

A homepage is a site's "face, cover, and brand identity." Four structures:
- **Feed** — a reverse-chronological stream, for news or social media;
- **Tile** — dense, uniform rectangles aligned in height for reading order (with floating height, as on Pinterest, the reading direction breaks down);
- **Photo-carousel** — one dominant, full-screen photo; the navigation must carry informative captions or previews;
- **Directory** — neat cells of sections on a "sandwich" principle (resilient to content changes), giving the designer maximum control over content priority.

### The three-point principle and composition against a photographic background

**Distinguish "layout anchors" (modular ones — a rectangle's corner/center) from a photograph's "compositional anchors," which behave almost the opposite way** — good photo composition avoids corners and the center. For free-form composition over an image, use the **three-point principle**: a large, a medium, and a small element in a loose triangle; check whether the arrangement feels heavy or graceful. Empty corners of a photo are usually a safe zone for a caption.

### Reading order as a compositional argument

**"Was → became": the old, bad, ugly sits to the left, above, or earlier than the new, good, beautiful.** In pricing: the old price struck through first (creates tension), then the new one (releases it) — this works both offline and online.

**Optics matter more than geometry.** Don't force different companies' logos into identical squares — different proportions create the illusion of different sizes; bring logos to the same weight "by eye," find a shared reference point rather than a formal match in dimensions.

### Case: a landing page as a decision-making composition

**A massive colored block often becomes a blind spot** — readers have learned to ignore a large, uniform colored block (banner blindness), even when it holds key information. A page that leads to choosing a plan or product should *end* in the choice, not open with it — context and value confirmation first (testimonials, benefits), then the options. Order prices ascending: "the buyer should physically feel that they're stepping back and paying less" as they move down the list. It helps to flag the middle option in a row of options as recommended (a "best value" badge) — people gravitate toward the golden mean, so support that pattern compositionally instead of fighting it.

### The module as the unit of the rectangle, the test of the whole

The test for any compositional decision: is the inner/outer rule honored at the block level (§1)? Is the dominant element anchored with anti-air (§1)? Is the rectangle holding together (§1)? Does the neighboring row avoid repeating the current row's rhythm (§2)?

### Posters, diagrams, and playbills

**Test contrast in black-and-white.** Check a text/background color pair by converting it to grayscale: if the pair "disappears" in black-and-white (the classic case: yellow on yellow), the contrast is objectively insufficient for a poster or playbill, not just "a matter of taste."

**Don't lock the main visual element inside a double frame** that smothers it — a portrait of a performer on a poster, for instance, shouldn't drown in a decorative border. Establish a clear hierarchy of sizes among headlines: undifferentiated text at a single size reads as "general gloom" (an absence of structure).

**Align dense informational posters and diagrams (family trees, charts, transit maps) tightly, "like a metro map,"** with no extra spacing and no fine detail that gets eaten up when printed or shrunk. For long timelines, prefer a horizontal layout over a vertical one. A dense reference poster "gives an unprepared viewer nothing" — pair it with onboarding (key figures, a built-in explanation) if the audience isn't made of experts.

**The visual weight of a diagram's graphic elements should be the minimum sufficient.** Lines that are too thick and type that's too bold make a diagram "heavier and messier," not more expressive — economize graphic weight the way you economize words in text; every extra gram of blackness competes with the data for attention.

**Multi-layered information (a "sandwich") needs distinguishable layers.** If adjacent information layers look visually similar and are weakly separated — for example, different types of data on a ticket set in the same typeface with no hierarchy — the reader can't pull them apart with a glance; separate layers by size, weight, or explicit rules, but don't lose critical data while unifying the format.

**Show the relationships between a diagram's objects through the logic of their relative placement, not only through color or an arrow-and-legend scheme** — spatial placement is remembered more easily than a coded convention: if object A physically sits next to object B because of the meaning of their relationship, a separate legend is often unnecessary altogether.

**Varying line weight is a tool for splitting an image into informational layers,** not just aesthetics: separate an object's primary outline from supporting or dimension-line graphics by stroke weight, not solely by color or a label — it's the same Tufte "data-ink ratio" idea, applied to a technical drawing rather than only to a chart.

**In dense multi-column boards (a TV schedule, a timetable), ALL CAPS is readability's first enemy.** Align times on a shared marker (the colon) to create a visual vertical; replace color-coding of categories with icons wherever a palette of many colors across many columns creates "unbearable, mottled noise."

**When switching a format from horizontal to vertical, move the logo mark to the top rather than leaving it on the left** — this keeps the reading and identification order intact under the new proportions; mechanically preserving the original layout on an incompatible format breaks the reading order.

**A row of same-type pictograms or modules must be consistent in style and stroke weight.** An inconsistent row of "mismatched rectangles" that "jump around, knowing nothing of each other" reads as sloppiness, even if each element is fine on its own — consistency across the row matters more than polishing a single icon.

**For a diagram with values that go in opposite directions (plus/minus, growth/decline), use a zero line,** with a sign to the right or left (or up or down) of it, rather than a single one-directional flow explained afterward in a caption.

---

## 5. Typography

### Headlines — see §3 (full treatment there)

### Lists

**The inner/outer rule governs lists:** the gap between items exists, but is noticeably smaller than the gap between paragraphs — that's what makes a list read as a single, subordinate "paragraph."

**A list's lead-in line sits flush against the first item, with no extra indent** — this is a standard Swiss/European convention (example: Apple's documentation), not a mistake, as some Russian designers sometimes assume. A list is "an indivisible entity, one sentence and one paragraph": don't add extra space before the first item — it should read as part of the lead-in paragraph's structure, not as a separate block.

### Paragraphs

**Onscreen, a blank line between paragraphs (a blind line) is preferable to a first-line indent.** A screen is harder to read than paper, so extra segmentation eases the eye's work. Across a column break: drop the paragraph indent right after the break (the new column's first line sets flush, with no indent).

### Line-height

**Line-height is a function of type size, line length, and format — never of the number of lines.** "Never change the line-height within one type of text," except as a deliberate stylistic device. The longer a line is by word count, the greater the line-height should be.

**The algorithm for setting a block: line length → line-height → distance to the headline → left margin → top margin → repeat.** "A square in the corner is a sign of weak, amateur, careless layout" if chosen unconsciously rather than as a deliberate device.

**Kerning digits in headlines** — in most typefaces, digits are monospaced (built for tables), so in headlines the gaps between digits "jump around"; manual kerning is justified only in special projects (a logo with a date) — in ordinary setting, it's a waste of time.

### Rag / ragged edge

**Adjust hyphenation for a "calm, wavy" rag.** In a magazine or book column, correct hyphenation gives a clean ragged edge with no "holes" or "staircases."

**Mixing left-aligned and centered setting is acceptable** if the result looks tidy together — it's not a categorical ban; the test is purely visual.

### Setting text in a circle

**Three levels of difficulty:**
1. text fitted into a circular or triangular silhouette — "immensely difficult";
2. filling an exact circular object — expensive precision, "you need to decide whether it's worth the trouble";
3. text inside a circular frame — ordinary rules apply (the rag, avoiding "rivers" of whitespace).

Watch-face and clock-face setting: out of five hundred years of clock-face history, only about 5% achieve genuine beauty — the genre is extremely demanding to execute.

### Type size and pairing typefaces

**Judge a headline/body typeface pairing on two axes: contrast** (simple/complex, bold/neutral, wide/narrow, heavy/light) **and shared traits** (proportions, weight, mood). Pairs that are stylistically distant but culturally related can work (Helvetica + Gilroy) — judge both axes against the actual layout, not the typefaces in isolation.

**Account for a typeface's characteristic proportions** (tall-narrow vs. short-wide letterforms) when choosing the format, margins, line length, and line-height — a mismatch in proportions, even with visually similar blocks, creates the impression of "wrongly matched Cyrillic." Contrasting proportions is a legitimate device, not necessarily a mistake.

**Don't compress a wordmark's letters to fit a fixed container.** Forcibly squeezing letter width or spacing to cram a logo into given dimensions kills the sense of quality and premiumness the redesign was meant to achieve — check that the letters' width and spacing survive the forced container with no distortion; if they don't survive it, change the container, not the letters.

### Text with a logo, and an element's syntactic role

**"Every interface or page element has its own syntax, its own 'part of speech.'"** A functional device (for example, a dotted underline meaning "fires with no page reload") can't be used decoratively — the device's semantics must match its actual behavior.

**Determine an element's syntactic role before its size.** If the logo *is* the message, it's allowed to dominate; otherwise the logo is usually the smallest element, tucked into a corner (the model: Apple's product pages, "brought to a common denominator"). Excessive tracking makes a wordmark too light to anchor the text beneath it — tighten it up.

### Aesthetics for a Russian-speaking designer

**Two reference points, the studio's "two legs":** the Renaissance tradition (old-style serifs, harmonious proportions — for intellectual content) and European modernism/Swiss typography (ragged-left setting, contrast of sizes, the modular grid — the universal language of business information). A designer should collect observations, objects, phenomena, and formats from the history of art and architecture as a source of solutions. The studio's brand DNA is "respect for the material" (a nod to Tufte), which stands "outside of fashion."

### Punctuation and small typographic details

**The multiplication sign is "×", set off by a half-space on each side** (200 × 300); "x" and "\*" are "the poor man's multiplication sign," keyboard substitutes. When a true half-space isn't technically available, an ordinary space is acceptable.

**A fraction shouldn't shift the line's height** — the denominator sits on the text's baseline. If no ready-made fraction glyph exists, shrink the numerator and denominator manually and raise the numerator's baseline.

**Nested quotation marks alternate: guillemets (« ») on the outside, low-high quotes („ ") on the inside.** Quotations with no quote marks at all are acceptable only when the whole page or block already reads unambiguously as a quotation. Hanging punctuation (two-sided hanging of quote marks, characters that project past the margin) is a display device, suited to "museum sites" and premium layout aiming for an expensive feel; for ordinary book or service layout, either apply it barely noticeably or skip it entirely — fast access to the content matters more than aesthetic precision.

**Initials are set off by a thin space, not an ordinary one** (V. I. Lenin); with no typographic thin space available, "better to over-space than under-space" — an ordinary space beats letters running together.

**Distinguish the em dash from the en dash by language** (Russian and English use them differently), and a dash from a hyphen in ranges: a range of numbers takes an en dash, not a hyphen (especially in English-language text).

**Copyright-line order per GOST R 7.0.1—2003: "© Rightsholder's name, year"** — the name comes first and the year second, unlike the American convention of "© year Name."

**Never place punctuation directly after a standalone web address or email** — push the mark to a new line or the end of the paragraph, or automatic linkers and manual copying of the address will break.

**The web originally had no hyphenation at all** — the web was conceived as reflowable text, so automatic hyphenation isn't a baseline typographic duty of an interface. The soft hyphen (U+00AD) is a narrow, specialized tool, justified in the narrow columns of e-books via an algorithm (Hyphenator.js and similar), not something to sprinkle through ordinary web text.

**Small caps are appropriate in two cases:** (1) in abbreviations and acronyms set in capitals (TRIZ, KM/H); (2) stylistically in headings and running heads (CHAPTER 1). In a mixed-case abbreviation (KamGES, YuUrGU), the lowercase letters are set with no extra tracking relative to the capital they belong to; Latin-style small caps set into Cyrillic text read as foreign.

**No period after titles, headlines, or captions** (a nominal sentence has no predicate), but the period isn't dropped from ordinary word abbreviations ("Mob.", "rub.") — SI units (m, kg, s) are written with no period, and truncations like bn/mn, Mon, UAH also take no period.

**Bold only what's genuinely bold in meaning; mark italics not just by slant but by the old-style shape of the letterform** — don't substitute typographic emphasis with an imitation (a system font's faux-bold or faux-italic).

**Set vertical text running bottom-to-top** (it requires less head tilt to read) and avoid it altogether where possible — it's always less comfortable to read than horizontal text; the exception is an established convention that, once learned, works like an icon rather than as text meant to be read line by line.

**Numbering a table of contents to the right of the headings is a centuries-old typographic tradition,** setting the reading order as "headline → number"; shifting the numbers to the left breaks that sequence — if you do it differently on purpose, place the numbers under the headings, not to their left.

---

## 6. Tables and data

### The ideal table (TRIZ)

**"The ideal table is one that doesn't exist at all,"** with its function fulfilled some other way. Before designing a table, work out its real function (choosing / operating / repairing) — for a choice scenario, show only the distinguishing parameters, not the full catalog.

### Grouping: columns closer, rows farther apart

**"Put the columns closer together and the rows farther apart"** — that makes it easier for the eye to hold onto a row's horizontal line. Cut the number of grid lines by "trimming the ends" of intersections, instead of a solid grid. Remove heavy vertical dividers — replace them with background fills for emphasis instead of an indifferent striping.

### Factor out repeats

**Repeated data (a unit of measure, a series or group name, an unchanging part of an item number) belongs in the table's or group's header, not duplicated in every row.** Example: the same abbreviation or unit in every row → move it once into the header. Factoring out repeats is how humanity invented tables in the first place — replace a repeat of "dollars-dollars-dollars, year-year-year" with a table grid; a less radical version is a currency symbol in each cell instead of the word.

**"Emptiness is the ideal separator"** within a row of numbers — preferable to a crutch character like "|"; strip insignificant zeros to cut visual noise (1.500 → 1.5).

### Numbers and alignment

**Align numbers by place value (to the right).** In tables, **always use spaces** to group thousands, so that place values line up regardless of a value's magnitude (in running text, 4-digit numbers can be set with no space). There's no exact CSS way to align on the decimal separator — prepare that alignment server-side or with a script when needed.

**Staggering digits on a dense scale** ("in a checkerboard," even values raised above the baseline, odd ones below it) resolves the contradiction of "large digits vs. no room with no overlap" — but don't overuse the device: it breaks the linear perception of a sequence, so apply it only when the scale genuinely can't fit without it.

**Align text in a table to the left and to the top of the cell** — that often makes a grid of lines unnecessary altogether: alignment alone creates enough structure with no graphic dividers.

### A grid for the grid's own sake isn't always a virtue

**A modular grid that breaks the logic of the data is a vice.** Group a table along axes of meaning (say: company / metric / value) so the reader can "search in the right corners," rather than packing it mechanically into equal cells.

**For spatial data, a map is a better visualization tool than a table**, if the data allows one to be built.

### Dynamic beats static

**Static striping (alternating rows) loses to dynamic highlighting of the row under the cursor,** or to bands of variable height that mark off groups of meaning — the TRIZ principle of "static → dynamic, unmanaged → managed."

### A table's header equals coherent text

**A table's header and its rows must form coherent text and describe the contents precisely** — a mismatch between the name and the actual data is unacceptable. Column headers should share one capitalization style (don't mix cases arbitrarily).

### Responsive layout for tabular data

**On narrow screens, collapse a 2D table into a linear format:** each row becomes a block, the former first column (the row header) becomes that block's heading (with no column of its own), and the remaining cells render as "parameter — value" pairs. **The critical second step: "check it against meaning and polish it"** — don't ship the raw mechanical conversion. Example: "Year: 1959" turns into "In 1959"; bare numbers get their "%" sign back for readability. A table is a compact 2D format; a narrow screen forces a linear output, but the linearization must be edited for meaning, not just dumped out mechanically.

### Hierarchy of data within a table

**"A table has both horizontal and vertical data hierarchy"** — pull repeating elements up the hierarchy: row → row header → group header → table header (and likewise for units of measure by column). But duplication is sometimes useful in its own right (a repeating "%" sign in every cell, say, speeds up scanning) — don't apply the rule mechanically; decide by the real need for readability.

### Document layout (reference works, manuals)

**Table of contents at the front, alphabetical index at the back, both flush to the page's edge for quick access.** The index's vocabulary should match how a real reader will actually search ("in the reader's language"), not the author's internal terminology. Signal importance first through position and size — styling comes last; label only what genuinely needs a label.

### Respect for the material — the Tufte line

The studio's brand DNA is "respect for the material," a direct nod to Edward Tufte: numbers instead of abstract codes (line weight, color with no label), an honest display of real data, minimal chartjunk, and a maximum data-ink ratio. Compare only commensurable units of measure on a single scale; don't mix visualization types for the same data (bars plus a pseudo-curve) — that creates a false impression of growth.

### Don't duplicate the legend if the table is itself the legend

**If a table already functions as the legend for a device or process (a washing-machine cycle table, say), don't add a second legend inside it** (footnote symbols, a repeated key) — that's double-coding the same thing. Collapse a complex classification down to the finite number of real usage scenarios; don't offload expert categorization onto the reader.

**Sort a table's rows by a semantic or optical criterion, not alphabetically**, when the alphabet doesn't match how the reader actually searches for a row (density, shape, functional proximity). The device of "mirroring the table" (swapping what were rows and columns) can sharply improve readability — don't be afraid of an unconventional transformation if the data allows comparison in the other orientation.

**Put the sort key first, but only where the list is actually searched by that key.** A ranking needs no inversion (the key is the rank number); an alphabetical index or card file needs "surname first"; a display card keeps the natural order ("first name first"). Don't move the key to the front out of habit — move it there only if the list is genuinely browsed or searched by that field.

**An unchanged value needs no special marker.** Don't draw an arrow or icon where a value hasn't changed since the last reading — a visual accent should flag a real event, not fill a cell out of a reflex for symmetry.

**Space off the digit groups of large numbers starting at five digits (10 000).** The spacing groups digits in threes and isn't needed below that — don't space four-digit numbers in ordinary running text; that's false complexity.

**Column headers: one shared capitalization; dividing lines shouldn't fight the grouping of meaning.** "The best design lets you show not just more clearly, but also more" — don't sacrifice useful data density for extra air the task doesn't call for; save space by trimming text, not by squeezing the grid.

---

## 7. Taste and visual literacy

**Calibrating taste is a two-step method.** (1) Visual exposure — gather broadly, but that alone isn't enough. (2) Calibration — show the work to someone better and hear what's good and why ("like RoboCop," recalibration through outside feedback).

**Copying masters with a ruler isn't shameful — it's a method.** Take a work you love and measure everything with a ruler: spacing, tracking, x-height; the margins and grids of good layouts often follow the proportions of the typeface itself. Don't be afraid to copy masters — it exposes the hidden mechanics of a solution. A training exercise for the skill: copy a reference design (Tufte, say) down to the smallest detail — size, line weight, alignment — to master information density and typography in practice, not in theory.

**References are hunted "everywhere."** Genuine interest makes you notice good layout constantly. In practice: buy books, photograph or scan spreads into folders, shoot magazine spreads. A random moodboard is "a banal story"; real reference-hunting is active, obsessive, archival.

**The value of theory is pattern recognition, not a recipe.** Color theory gives you a "map" — where a color lives and which direction to move it; typography books explain how to build a grid, but not what to fill it with. Over years of cataloguing Swiss layouts, roughly 90% of them boil down to **3–5 recurring templates (лекала)** — recognize these instead of inventing from scratch every time.

**A critique of the 60-30-10 rule.** It's not a serious rule: it's unmeasurable, and it breaks down at the edge cases. The bar for a well-formed design rule is the inner-and-outer rule and the anchor-object rule — structural, concept-explaining rules that unify dozens of scattered observations, not numeric ratios pulled out of thin air.

**The body of "templates" isn't an endless list of special cases — it's a short reference checklist.** The book "Typography and Layout" keeps a reference table of compositional templates, jokingly nicknamed layout's own "periodic table" — roughly 90% of real Swiss layouts, accumulated over years of cataloguing, boil down to 3–5 recurring structures. Visual exposure with no this kind of systematization stays a collection of examples, not a working tool.

**A metaphor for icons only works through something already familiar.** A metaphor succeeds when it maps an unfamiliar interface element onto something the user already knows from real life (a basket or cart = shopping). Abstract source concepts ("knowledge hub") have no real-world referent — no icon can save them. Icons with no label are almost never justified; their main function is a recognition anchor (shape-memory) and a target to tap. The rule for icons close in meaning: "the more similar the concepts, the more different the icons should be" — differentiate rather than mirror.

**Stylization is a skill that takes practice, not a vice.** A ready-made style or filter (GOST-style lettering, stencil type, for example) is a legitimate aesthetic if executed with mastery (example: Wes Anderson's deliberate stencil style — "that, too, takes skill to pull off"); a bureaucratic form is no obstacle to beauty — careless execution is the obstacle.

---

## 8. The designer's method and process

**Bringing order is a framing of the task, not a geometry puzzle.** When aligning a menu to a grid: "at the very start, it's better to forget about the guides. Just take them away" — design freehand first. Then either: give the columns equal width so rhythm compensates for uneven text height, or align by block height instead of column width (a habit closer to print than to screen). Only after that, use guides "like a drafting ruler," to precisely construct a solution you've already worked out.

**Design is not appearance.** Don't argue with a client about definitions — "explaining how our opinion suits the world is dumb and pointless." Show it through your portfolio, your working materials, and *the questions you ask*: if the question is about appearance, the client concludes you're decorating; a question about their products, services, or tasks makes the client feel you're digging deeper. Method beats lecturing — the questions themselves teach the client what design is.

**Working with the material is the path to product quality.** "The better a designer understands the material they're shaping, the higher the quality, reliability, and craft of the resulting product" — but temper this with "reasonable specialization": study the constraints of your medium (CSS, the development environment) with no becoming its full-time builder; mockups assembled directly in code are inefficient at the solution-finding stage.

**The generalization test for any "rule."** "Any correct answer must be correct in every situation" — before accepting a heuristic ("never use lines," "always center the headline") as a rule, test it against a counterexample; if you find a legitimate situation where the heuristic breaks, it's not a rule, it's a special-case device with conditions attached.

**When lines and frames are legitimate.** A line or divider isn't inherently a mistake — it's "a layout tool," part of layout's Lego set: a divider becomes legitimate when a structural change (moving dates into their own column, say) genuinely requires it — otherwise prefer space over a line. "A rule is just a construction that occurs and has a right to exist" — the doctrine teaches principles of connection, not bans on specific devices.

**An illustration need not interrupt an article's reading — an ad must not.** The real principle (from the chapter "The shape of text and reading order"): "the reader may think the article has ended if the text is interrupted by an ad, but not by an illustration." Illustrations serve an editorial purpose and don't trigger a false sense that "the article is over"; ads do. The final call — whether to break up the text with an illustration — stays with the designer.

**Minimizing the construction is the second universal law.** "Systems evolve toward minimizing the physical means embodying their useful function" — simplify with no losing the useful function. Three devices: **strip everything unnecessary** (remove ballast with no loss of function); **"factor out"** (a shared element instead of repeats, see §6); **"transfer the function"** (one detail takes on another's function, eliminating duplication).

**Composition as an escalation of complexity, not a single chosen device.** A falling-apart module (see §2) is fixed by escalating: first the simplest solution (a fill or a rule), then something more structural (aligned columns), and only when truly necessary, a full "collection of Swiss modules." Don't start with the most complex tool.

**A compromise is the weakest possible solution to a problem.** A compromise "by definition worsens the position of both sides, or both conflicting parameters" — it's a weakening, not a resolution of the contradiction (for example, "shrink the type size a bit and squeeze the margins a bit" instead of picking a priority). Better to fix priorities explicitly (the FFF method — fix the deadline/budget, flex the functionality/content) than to degrade every parameter a little at a time.

**Frequent failures in student and test layout work** (check yourself against these before turning in a layout): the single genuinely important rule is buried among secondary details — bring it to the front; the one diagram or scheme without which the rules can't be applied in practice is missing; dead white zones are left in, or, conversely, they're stuffed with meaningless factoids just for symmetry; a background photo under the text visually argues with the content instead of supporting it; the "text on the left, notes on the right" composition is applied reflexively, as a default template, rather than as a deliberate choice suited to the specific task.

**Should a designer study layout and code? Yes, but with specialization.** Understanding the medium raises the product's quality, but it doesn't replace the designer's role with the builder's; learn the basics of layout before interfaces — start with the basic molecule: a paragraph with a headline, a pleasing ratio of margins to line-height, then bring order to the numbers and add meaningful emphasis.

**Design is a system, not a wrapper.** The studio's key methodological pivot: "however well a designer makes… the outer wrapper, the shape, the interface — that doesn't guarantee the product's success… you need to design the system as a whole." A reviewer must judge whether the system behind the layout works, not just the quality of the skin over it — a beautiful layout over a broken structure doesn't solve the task.

**The litmus test, "design vs. self-expression":** "expressing yourself is art; solving a problem is design." Before defending any compositional decision, ask: whose problem does it solve — the reader's or user's, or is it an author's gesture for their own pleasure? Both are legitimate in different genres, but confusing them in client work is a positioning mistake.

**A three-stage scheme for solving a layout or compositional problem (the TRIZ method, adapted by the studio):**
1. **Analysis** — state the layout's useful function and the harmful factor (what's blocking it), lay out the hierarchy of the system and subsystems, and the resources available (elements already in hand, free space, existing contrast).
2. **Model of the solution** — in one sentence: "the useful function and an explicitly stated way to achieve it" (for example: "the headline should be read first → increase its size and give it its own module up top").
3. **Solution** — build the model out in detail, then critically test the result with the same fresh eyes a first-time reader would bring.

"If a designer analyzes the problem and identifies the harm and the useful function, finding an existing solution by specific criteria is far easier than sifting through all of humanity's experience" — a precisely stated problem beats blindly sifting through references.

**Four recurring failures in analyzing a layout problem** (check yourself against each): (1) mistaking a surface-level statement of the problem for its root cause, with no digging to the real one; (2) stereotyped thinking — functional fixedness ("that's how it's always done"), "resource thinking" (adding more air or color instead of rethinking the structure), survivorship bias (copying only successful references with no seeing their context); (3) underrating an unconventional solution — an inventive answer often *looks* riskier than a familiar compromise and gets rejected for exactly that reason; (4) no method (including TRIZ itself) is universal — build a repeatable process for framing and evaluating the problem; don't rely on any single technique as a magic wand.

---

## Diagnostic checklist (15 checks, by priority)

1. **Is inner < outer at every level?** From the letter up to the module — are the internal distances noticeably smaller than the external ones everywhere? If not, that's the first and most common cause of "muddy," non-unified layout.
2. **Is there an anchor object in every key rectangle, and does it have anti-air?** Check the corner/visual center and the contrasting emptiness on the opposite side.
3. **Do the rectangles avoid intersecting or falling apart?** Check the balance of heights between the left/right (or top/bottom) parts of a composite block — does it form a genuine rectangle?
4. **Does the neighboring "floor" repeat the current one's rhythm?** If so, the reader will mistakenly link unrelated blocks; break the rhythm on purpose.
5. **Does the main column have ≥5% breathing room?** Is the text touching the neighboring module directly — that's a warning sign.
6. **Are the margins different on each side (not square, not symmetric)?** Equal margins on every side are a sign of amateur layout; check whether "tension in the proportions" is at work.
7. **Does an element's syntactic role match its visual weight?** Does a secondary element (a logo, a utility link) look bigger or more prominent than the content?
8. **Is the canonical reading order honored (illustration → headline → text → links)?** If it's broken, is that a deliberate exception or an accidental mistake?
9. **Are there no "lumps" — basic elements blended with no visual separation?** Go through all six (headline, text, illustration, control, link, caption) — is each one instantly recognizable?
10. **Does the dominant illustration avoid competing in size with the supporting one?** Is there an unambiguous signal of "the tour starts here"?
11. **Are lists and paragraphs free of extra indenting?** Is a list's lead-in line flush with the first item; does the list read as part of the paragraph, not a separate block with extra air?
12. **Is line-height a function of type size, line length, and format, rather than of the number of lines?** Does it change arbitrarily within one type of text with no reason?
13. **Does the table group data along axes of meaning, rather than a mechanical grid?** Columns closer, rows farther apart; repeats factored out into a header or group.
14. **Is every line or frame justified by a structural change?** If a line could be replaced by a space with no loss of meaning, remove the line.
15. **Is there a reference or precedent you can check the decision against with a ruler?** If the decision feels arbitrary, can you name 3–5 "templates" it gravitates toward?
