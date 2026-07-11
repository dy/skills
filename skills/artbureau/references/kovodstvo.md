# Ководство — Artemy Lebedev's Design Reference

Dense digest of Ководство (Kovodstvo), §§ 0–191 published. Organized by theme, not by section order. § numbers are anchors back to the original — cite them when quoting.

---

## 1. Дизайн-философия

### Design is solving a problem, not decorating

- **"Дизайн не надо обсуждать, он является решением поставленной задачи"** — design isn't up for discussion, it *is* the solution to the stated task. The only valid question: has the task been solved? (§ 149)
- Design is problem-solving, not "making things beautiful" — beauty can legitimately be *part* of the brief, but it is never the whole task. (§ 149)
- Studio's mission: find "наиболее удобный, простой и красивый способ решения поставленной задачи, не потеряв по дороге смысл" — the most convenient, simple, beautiful solution, without losing the meaning along the way. (§ 149)
- Bottlenecks on wine bottles are narrow because cork was historically expensive — not because "у дизайнера вдруг зачесалось левое яйцо" (a designer suddenly felt a random itch of inspiration). Design outcomes trace to material/cost/functional constraints, not artistic whim. (§ 140)
- Test for a junior designer: invent your own brief and execute it well — real ability shows in self-driven, completed work. (§ 149)

### Simplicity ≠ primitiveness — and the fear of simplicity

- **"Дизайн должен быть простым"** — the entire content of § 108 is this one line; the aphorism's brevity performs its own thesis.
- **"Дизайн должен быть простым, но не примитивным"** (§ 147) — simplicity is intentional restraint that keeps meaningful detail; primitiveness is mere absence of consideration. Facades with cornices read as more humane than bare ones — bareness isn't sophistication, it's emptiness. True simplicity requires knowing *which* details matter enough to keep.
- Epigraph: "Простота — необходимое условие прекрасного" (Tolstoy, cited § 57) — simplicity is a precondition of beauty, not a lesser achievement. Wrong instinct to fear: "Просто и у дурака выйдет" (even a fool can do it simply).
- **Боязнь простоты** (§ 89): designers over-complicate out of insecurity, believing plainness won't command a high fee, so they add ornament to look "finished." Test case: 30 designers asked to lay out elevator buttons for a 23-story building — only one used the obvious vertical arrangement; the rest proposed circular/spiral layouts to look "cool." **"Originality for originality's sake is worthless"** — it "becomes obsolete the day after creation." Hard line: "A designer unable to find simple solutions shouldn't work with clients."
- **"Любой интерфейс можно упростить в два раза"** (§ 110) — any interface can be simplified by half. Case: a "minimal" remote with power, channel, and volume rocker still has redundancy (power and channel are logically identical binary switches). Designers habitually repeat the same information across channels (shape, text, direction, plus/minus symbols duplicating a graphic already shown) — cut it.
- Counterpoint — **complication has its place**: "Усложнение, так же как и упрощение, является сложным приемом, и применять его надо с умом" (§ 111) — complication, like simplification, is sophisticated and demands judgment. Deliberate redundancy is sometimes correct: two connected Metro stations both named "Проспект Мира" are shown as two circles with a transfer corridor, not one ambiguous merged circle. Roundabout signage layers multiple conventions to remove ambiguity; a Spanish highway posts four warning signs at one deceptive bend for guaranteed visibility from multiple angles. Strategic redundancy across channels can beat elegant minimalism when safety is at stake.

### Logic before aesthetics

- **"В интерфейсах логика важнее эстетики"** — in interfaces, logic outranks aesthetics (§ 109). Not license for ugliness, but skepticism toward "раскрашивать труп" (painting a corpse). Two workflows exist — solve logic then retrofit aesthetics, or the reverse — Lebedev favors the former. **"Как транспортное средство российского производства ни покрась… оно лучше ездить не станет"** — repaint a Russian car however you like, it won't drive better. Every design task is fundamentally about building "interface — the contact point between person and object." Model: Harry Beck's 1933 London Underground map, logic-first design that became the global metro-map standard.

### "In design there are no laws"

- **"В дизайне законов нет. Не было и не будет."** (§ 99) — there are no absolute design laws, only situational guidelines. Systematically knocks down "rules" (one typeface only, limited palettes, fixed logo placement, mandatory minimalism, "300 DPI always," fixed reading-time) by showing legitimate exceptions to each.
- Treat every design rule — including every rule in this very digest — as context-dependent guidance, not universal law. Contrast: alcohol advertising and telecom advertising can use opposite approaches and both work. Designers and clients suffer when a situational guideline gets enforced as a universal constraint.
- **Принципы vs правила** (§ 176): you can do almost anything creatively if it's grounded in a clear principle. Example principles: always discard the first sketch shown; write all headlines without adjectives; end all product names in "-ус"; paint the side panel orange. **"Наличие принципа — одна из самых удобных форм ограничения"** — having *a* principle is one of the most convenient forms of constraint; its content matters less than its presence. Work without any principle at all is useless and meaningless.
- **Правило по составлению правил** (§ 178): make something good *first*, then find the patterns in it — reversing the order produces a Procrustean bed that mangles content to fit a premature rule. **"Надо сначала сделать хорошо, а потом искать закономерности."** Modular grids exemplify the failure: math imposed on a blank page forces content into awkward cells instead of arranging content until harmonious and extracting the grid after. **"В основе хороших правил — душа"** — good rules are rooted in soul, not top-down formalism.
- **"В дизайне можно всё, что нельзя"** (§ 187) — in design, everything that's forbidden is permitted. Deliberately provocative, thin on elaboration — design as a domain that transcends ordinary constraint.

### Method of progressive JPEG

- **"В любую секунду любой проект готов на 100%, хотя проработанность может быть и на 4%"** (§ 167) — a project is conceptually 100% "done" at any moment, even if refinement sits at only 4%, modeled on progressive JPEG rendering. Depth of execution scales with time available — sketch to pixel-perfect, both legitimately "complete" because the core idea is already whole.
- **"Почти любую дизайнерскую задачу умею решать за время формулирования задачи"** — most design problems can be solved in the time it takes the client to state them. **"Время тратится только на нужную степень прожарки, а общий вид стейка всегда ясен"** — time buys doneness, not the shape of the steak.

### Единица смысла (unit of meaning)

- Measure designer output in "units of meaning" (интеллектуально калорийные идеи), not hours or file count (§ 148). A 100-page brand book = one unit; a logo counts, slapping it on a business card doesn't.
- Benchmarks: average good designer ≈ 1–2 units/month; excellent designer ≈ 4/month; an art director needs ≥6/month to justify overseeing three designers.
- Self-test: write down actual ideas produced over 3 months — most people find fewer than 3, often stale. Honest tracking exposes disengagement.

### От обратного (design by inversion)

- Imagine the worst possible solution in full detail, then flip it (§ 150). Shop entrance: hide the door, put it on the 3rd floor, remove the handle, make it jam. Website: cryptic URLs, excess graphics, fragmented content, indistinguishable links.
- Critical, easy-to-skip final step: **"Главное — не забыть поменять все еще раз наоборот"** — don't forget to flip everything back. The reversal *is* the design; skipping it just leaves the bad version.

### Польза ограничений (the value of constraints)

- A designer given zero constraints is paralyzed, not liberated (§ 175). **"Без ограничений не бывает творчества. Самые лучшие образцы дизайна появлялись в результате самых жестких требований"** — no creativity without constraints; the best design has come from the harshest requirements.
- Complaining about client constraints (color, logo size) signals unprofessionalism. **"Только в ограничениях рождается хороший дизайн"** — good design is born only within constraints.
- **Творческий кризис** (§ 162): word-listing exercise — asked to recite known words, people run dry after ~20; asked to narrate something, no shortage appears. The gap is execution, not raw material. **"Кризис идей может возникнуть только в том случае, если дизайнер ставит перед собой цель придумывать что-либо оригинальное и необычное"** — creative crisis only happens when originality itself becomes the goal. **"Оригинальное и необычное нельзя придумать — оно может появиться только само в процессе работы"** — the original can't be invented on purpose; it surfaces only while actually working the problem. **"Творческий кризис — это тупик бессмысленного пути."**

### Pyramid, resolution, and other diagnostic frames

- **Пирамида Лебедева** (§ 153): in any company, organization, or gathering the same ratio holds — a small competent minority at top, a much larger low-effort majority beneath. Real contributors are always a thin top layer. (Page withholds diagram text; reconstructed from secondary sources.)
- **Низкое разрешение** (§ 132): "разрешение" = ability to distinguish styles, objects, colors, fonts, voices — determines professional competence. **"Разрешение дизайнера обычно приближается к единице"** — designer resolution typically approaches zero/one, barely any discrimination. **"Дизайнер — один из самых честолюбивых, необразованных, поверхностных специалистов"** — designers rank among the most ambitious, uneducated, superficial professionals (rivaled only by journalists). Resolution rises only through experience, desire, and luck. Symptom: designers who celebrate cheap effects, over-decorate with headers, fear unfamiliar choices.
- **Дизайн — это война** (§ 156): graphic design is a weapon in an ongoing conflict of interest — case study: cigarette health warnings vs. tobacco manufacturers, an escalating arms race with no end. **"Дизайн — это война."** Each side hides its next move and studies the opponent's response.
- **Творческие инструменты** (§ 181): **"У дизайнера инструмент — «Фотошоп», у арт-директора инструмент — дизайнер"** — a designer's tool is Photoshop; an art director's tool is the designer. People, not software, are the instrument one level up.
- **О творческом развитии** (§ 186): **"Тот, у кого в детстве были кубики, вырастает и создает трансформеров. Тот, у кого в детстве были трансформеры, вырастает и создает кубики"** — those raised on building blocks invent transformers; those raised on transformers invent blocks. Creative development is compensatory, not continuous — creators build what was missing from their own childhood.
- **Прививка от действительности** (§ 19): bad design persists culturally, not materially — self-administer an inoculation against your surroundings; refuse to normalize the mediocrity around you ("девяносто восемь процентов… исполнены дилетантами"). **"Выживут только сделавшие прививку."**
- **Молодой и бывалый** (§ 20): **"Умение оценивать хороший дизайн является не меньшим достижением, чем умение его создавать"** — evaluating design well is as hard-won as making it; don't trust untrained judgment, including your own early on. Watch for false praise — clients approve work for the wrong reasons while missing "того, ради чего все создавалось," the actual purpose.
- **Убитое поколение** (§ 36): **"Виновато само окружение"** — visual taste is shaped by environment, not personal failing (he blames Khrushchev-era standardization, "хрущобы"). Bad taste isn't personal incompetence; actively seek exposure to better work to recalibrate your own eye.
- **Разнообразие** (§ 185): zoo lemurs eat only bananas but stay content because keepers cut the fruit differently every day. **"Даже при тотальной монотонности ресурсов залог успеха один: разнообразие."** Formal variation sustains engagement even when underlying substance never changes.
- **Полочка в мозгу** (§ 190): **"Мозг человека сравним с огромной картотекой"** — the brain is a giant filing cabinet; neurons are lazy, comfortable with the habitual. **"Хороший дизайнер от обычного отличается тем, что умеет создавать в мозгах людей новые нейронные связи"** — a good designer builds a whole new cabinet of drawers, not just fills an existing slot. Pushback against new design is itself a sign the restructuring is working.
- **Искусство** (§ 191): **"Искусство должно быть одноразовым или утилитарным"** — art must be either one-time (dance, food, music, massage — pleasure in the moment, then only memory) or utilitarian (paintings, architecture, logos, signage — reusable, revisitable). Everything else is "ошибка сознания," a consciousness error — museum-preserved one-time-art-as-relic is nonsensical.

### Формат vs клонирование

- Distinguish cloning (copying another's structure/imagery wholesale) from *format* — a set of shared rules/traits across a whole category (newsprint's paper/columns/headline sizes) (§ 25). Resembling the category leader isn't theft if you're fulfilling the format's own requirements. A format is born when someone solves a problem so well that followers must converge on it with only minor variation (e.g., web directories echoing Yahoo's two-column link layout).
- **"Нужно не бояться повторить чью-то схему, а уметь придумать каждый раз что-то новое"** — don't fear reusing a proven schema; the real skill is inventing something new within it each time.

### Кодирование смысла — encoding meaning through form (§ 106, § 107)

- Encoding = **"придание объекту или сущности дополнительных различаемых свойств"** — giving an object additional distinguishing properties, so it communicates beyond bare function.
- Channels, in order of primacy: symbolic (icons, numerals), formal (shape itself carries information — salt vs. pepper shakers differ by hole count; chess pieces' distinct forms determine legal moves), positional (location in space — reliable for only ~6 positions in 3D, ~9 on a 2D plane), then color/pattern/sound once those are exhausted.
- Functional encoding via form is safety-critical: identical Soviet outlets across different voltages (220V/127V) destroyed equipment; identical radio plugs caused fires. **Different functions must get different physical forms.**
- Design so meaning survives when the primary code fails — colorblindness affects 8% of men; the 1908 London Underground map shows color's power, but modern TfL maps still work in monochrome via redundant pattern coding.

### Предвидеть неверное прочтение (§ 92)

- **"Дизайнер должен избегать всего, что может быть неправильно истолковано"** — a designer must anticipate and avoid anything liable to be misread, especially for high-stakes industries (airlines, nuclear, transport).
- Worked failures: a Swiss air-traffic-control logo depicting a descending plane, grimly literal after a real mid-air collision days later; an airline site defaulting the destination field to "не важно" ("doesn't matter"); an airline ad's falling feather after a plane vanishes into clouds, unintentionally evoking a bird strike.
- For safety-sensitive brands, actively pre-search imagery/copy for worst-case literal or morbid readings before shipping.

### Культурные контексты (§ 73)

- Meaning is culturally relative, not universal — colors, symbols, even a rainbow's "seven colors" are convention, not fact. Every group runs on its own context marking "our people"; a designer must consciously identify the audience's context, not assume a universal one.
- **"Сила дизайнера — в слабости человека"** — design's power lies in human self-deception, but that leverage usually only works inside a familiar cultural frame; exported unchanged, it fails or embarrasses.
- Don't design for a foreign market using only your own cultural context — local blind spots are invisible from outside, hence the value (often undervalued) of genuinely local designers.

### Воспитание вкуса, не потакание (§ 34, § 35)

- Design/advertising must either match existing audience taste to sell, or better, reshape taste over time through sustained, low-key cultural programs (his analogy: iodized salt, Moscow Metro architecture) — **"нужно... воспитание,"** not a one-off campaign.
- Staff realistically for both tiers a real project needs: unglamorous high-volume production labor and the rarer creative/strategic work — the market underprices the former and oversupplies people chasing the image of the latter.

---

## 2. Русская типографика и пунктуация

### Тире, минус и дефис — three distinct marks (§ 97, § 62)

- **Дефис (hyphen, -)**: joins particles (кто-либо, где-то), prefixes (во-первых, по-русски), abbreviations, compound words (ковёр-самолёт), line-break hyphenation. Aligns optically with lowercase letters.
- **Минус (minus, −)**: math/formulas only; aligns with cap-height/numerals; often missing from ordinary fonts — don't substitute a hyphen.
- **Тире (em dash, —)**: replaces omitted sentence elements, separates subject/predicate, marks direct speech, indicates a pause, denotes a route/range (Москва — Санкт-Петербург). Width ≈ "M"; always spaced both sides. **"Тире не надо путать с дефисом — оно обычно в два-три раза длиннее."**
- Root cause of confusion: most designers use only the keyboard-accessible hyphen for all three roles, collapsing distinctions that exist for real typographic reasons.
- **Короткое тире (§ 158)**: adopt the en dash for numeric ranges (2000–2009), Anglo-American convention — **"Наше классическое длинное тире сегодня в роли диапазона выглядит длинноватым."** The long dash keeps its normal textual role (Серп и Молот — Карачарово); phone numbers keep hyphens/spaces regardless.

### Кавычки — quotation marks (§ 104)

- Paired punctuation, always left/right, language-specific — never generic straight "programmer's quotes." Russian: « » outer, „ " inner.
- Straight quotes were a typewriter cost-saving hack, later inherited uncritically by computers once technical editors stopped supervising layout.
- Straight quotes acceptable in code/technical contexts only. Check pre-computer print editions (USSR before 1990; West before 1985) for correct marks per language. **"Уважающий себя дизайнер"** (a self-respecting designer) always uses them correctly.

### Многоточие — ellipsis (§ 164)

- **"Многоточие не должно быть символом, созданным для экономии байтов"** — the ellipsis shouldn't be a byte-saving shortcut character.
- In books and refined typesetting, only three separate periods (...) are correct — not the single Unicode ellipsis glyph (…).

### Двоезапятие — double comma (§ 133)

- Speculative proposal (not established rule): a new mark, two commas, to cover the gap left by underused semicolons in Russian writing — unlike foreign writers, Russians largely avoid the semicolon. Framed as filling a genuine functional/intonational gap; acknowledges most typographic inventions never catch on (cites the forgotten 1962 interrobang).

### Висячая пунктуация — hanging punctuation (§ 120)

- A hallmark of professional typesetting: optically push punctuation past the text block's edge to compensate for lighter visual weight vs. letters.
- Left: quotation marks, parentheses, bullets hang left of the margin; direct-speech em-dashes do NOT hang.
- Right: quotation marks, parentheses, periods, commas hang right; hyphens protrude only 1/3–1/2 their length.
- Worthwhile for web text; in print use for newspaper/magazine headlines and large blocks; in books apply universally.

### Буква ё (§ 119)

- **"Ё должна использоваться: в случаях возможных разночтений; в словарях; в книгах для изучающих русский язык (т. е. детей и иностранцев); для правильного прочтения редких топонимов, названий или фамилий."** Everywhere else, ё only hurts readability. Most homographs (замок/замок) survive fine without it. Parallel: English "coöperation" — literate readers don't need the mark.

### Историческая и монументальная точность (§ 23, § 26, § 63, § 139)

- Faking pre-revolutionary orthography by tacking a hard sign (ъ) onto every word ending is a marker of ignorance — the old rules (ять vs ер, і vs и, фита vs ф) were far more complex than a formula. **"Лучший совет: не использовать старую орфографию вообще"** — don't attempt period spelling unless you actually know the rules.
- If archaic orthography is used at all, apply it consistently throughout the piece, not just the title — and match typeface to period (a 1901 German modernist face used for an 1885 Imperial-Russian setting is an anachronism a reviewer should flag).
- Case study: the 1992 Cyril-and-Methodius monument in Moscow shipped with five orthographic errors in its Church Slavonic inscription — the letterer chose archaic letterforms for effect without knowing the actual rules; even later "corrections" used mismatched letterforms. **"Ошибок на обложках книг, в иллюстрациях, на вывесках (а тем более на памятниках) нельзя допускать категорически"** — errors on covers, illustrations, signage, and especially monumental text are categorically unacceptable; body text gets more slack, monuments get none.
- Same standard for any published work: **"Опечатался на титульном листе — потерял работу"** — a typo on the title page costs the job. Case: a Russian Scrabble edition marketed on "every word counts" misspelled "кроссворд" as "crossoword" on its own packaging.

### Не смешивать языки (§ 82)

- **"Не надо смешивать языки. В одном смысловом поле должен быть один язык"** — never mix languages within one semantic block. Corollary: **"один язык — один буклет"** — one language per booklet, not a multilingual wall of text; for interfaces, use an explicit language switcher rather than co-displaying translations. Cited absurdity: a GE light-bulb box listing "frosted" in 19 languages on one panel.

### Панграммы — proof every glyph (§ 33)

- To judge a typeface fairly you must see every glyph it contains — flaws (e.g. "чудовищные формы букв Ф, Д, Л" in many Cyrillic fonts) aren't visible from a few sample words. Always proof a new font by setting a full pangram, not cherry-picked text.

### Типографский пункт — not one universal unit (§ 81)

- "Point" is not a single universal unit: Anglo-American (PostScript/DTP, exactly 1/72 inch, fixed in the 1980s) and European/Russian (Didot, ≈0.376mm, traced through Fournier 1737 → Didot 1783 → Berthold's metric fix in 1879) are different sizes. Know which system a spec quotes before trusting a point value.

### Клавиатура и запятая — small decisions calcify (§ 105)

- Soviet ЙЦУКЕН typewriter layouts placed punctuation efficiently after a century of ergonomic refinement. When Western computers arrived, someone "Russified" a Latin keyboard without understanding this tradition and put the comma — used far more often than the period — in the upper register (Shift-required). **"Достаточно было десяти минут труда случайного постороннего, чтобы неудобная, замедляющая набор раскладка стала тиражироваться"** — ten minutes of careless outside work produced a standard that degraded millions of users' comfort ever since. A caution about the outsized, lasting weight of small design decisions.

### Неформальная типографика (§ 135)

- Formal typography (newspapers, books) and informal (personal/online communication) split, but informal devices can enrich traditional media too. Strikethrough, originally an ad convention (crossing out old prices), migrated into blogs to imply subtext — works in headlines and body text alike.
- **"Смайлики незаслуженно считаются второсортным выразительным приемом"** — punctuation-based emoticons (`:-)`) are legitimate typography, as historically valid as Roman numerals; graphic image emoticons signal poor taste. Neither device substitutes for actual wit — both demand restraint.

### Написание «интернет» (§ 55)

- Write "интернет" lowercase and decline it normally through all six Russian cases — don't capitalize, quote, or leave it undeclined/Latin-alphabet. Don't defer to an "authoritative" source uncritically: Lebedev's request to the Russian Academy of Sciences' language institute came back with its own grammatical errors.

### Знак рубля, доллара, евро

- **Ruble** (§ 116, superseded by § 159): originally argued the abbreviation "руб."/"р." is the best "symbol" — no glyph needed, works in any font, readable to foreigners without training. **"Знак рубля всегда должен стоять через пробел после числа"** — the mark follows the number with a space. **Lebedev later reversed this** (§ 159, 2007): after a law mandated an official symbol, a studio coalition (his included) designed it deliberately rather than leaving it to chance. **"У нового знака нет автора, на его копирование и модификации не накладывается никаких ограничений."** **"Внедрение нового символа происходит, когда набирается критическая масса первопроходцев"** — adoption depends on bold designers and bold clients, not decree.
- **Currency placement generally** (§ 74): symbol follows the amount with a space — "100 $", not "$100" — matching Russian/French/German convention against a US-style prefix.
- **Euro** (§ 77): case study in bad symbol governance — the € sign (designed by Arthur Eisenmenger, never publicly credited) was released as a rigid frozen "logo" with mandated construction geometry instead of an adaptable typographic character to be redrawn per-typeface. The mandated "always before the number" placement ignored existing local convention (France, Germany, Russia place currency after the amount). Called "one of the ugliest signs," aggravated by a secretive selection process.

### Амперсанд (§ 112)

- The & is a graphic ligature of Latin *et*, invented by Cicero's secretary Tiro (Notæ Tironianæ, c. 63 BCE). In Russian it's unnecessary: **"союз и уже короткий на слух и на вид"** — "и" is already short. Using & in Russian branding manufactures false "иностранность"/"бизнесовость" — poor taste, like tacking on a hard sign for fake archaism.

### Разрядка (letter-spacing) (§ 79, § 142)

- **"Прописные буквы всегда разрежаются"** (capitals are always tracked out); **"строчные — никогда"** (lowercase never).
- For emphasis in running text, only semi-bold and italic remain legitimate. Forbidden for body-text emphasis: letter-spacing, underlining, color highlighting (typewriter-era holdovers). Bold = headlines/immediate attention; italic = subtler in-text emphasis, literary quotation. Bold-inside-bold → bold italic; italic-inside-italic → upright regular as contrast. Never set whole passages in italic.

### Склонение топонимов

- **On "-о" endings** (§ 146): Toponyms ending in "-о" (Домодедово, Шереметьево) decline like normal Russian nouns, not frozen in nominative. "После Домодедова еда в Шереметьеве показалась издевательством."
- **On contested toponyms** (§ 121, polemical/political): prescribes conservative spellings — Таллин (not Таллинн), Алма-Ата (not Алматы), Белоруссия (not Беларусь — "это трактор"), "поехать на Украину" (not "в Украину") — favors established Russian tradition over post-Soviet renaming.
- **On brand names** (§ 114): "от" is misused to dodge declining brand names ("костюм от Армани" instead of grammatically correct "костюм Армани") — "корпоративная трусость," corporate cowardice about inflecting trademarks like real Russian words.

### «Вы» с маленькой буквы (§ 165) — three rules

1. **Lowercase "вы"**: never capitalize; lowercase already conveys respect. "Все для Вас" reads as foolish, not respectful — "невыносима рекламно-подобострастная манера." Reserve capital "Вы" for maybe 3 people in a lifetime, genuinely extraordinary address.
2. **Use "свой"**: Russian's reflexive possessive has no English equivalent; don't default to "вашу/вашей" out of translation habit. "Маша вынула руки из карманов" needs no possessive at all.
3. **Drop unnecessary "вы"**: avoid Anglicized "здесь вы можете зарегистрироваться" — prefer "здесь можно зарегистрироваться" or just "Регистрация." Cutting surplus pronouns strengthens interface text and prose generally.

### Номера телефонов, адреса, даты

- **Phone numbers** (§ 91): local "123-45-67"; with city code "(123) 123-45-67"; mobile "+7 123 123-45-67." Group digits in pairs from the right for readability and error-reduction.
- **Postal addresses** (§ 163): reverse the traditional Russian order (large→small) to international standard (small→large): recipient → company → street/building/apt → settlement → district → region → postal code → country. Rationale is the postal worker's decoding speed at scale, not the recipient's convenience.
- **Dates** (§ 74): DD.MM.YYYY with periods, not slashes. Lowercase weekdays/months; avoid over-capitalized headlines. Time uses a colon — "15:45," not "15.45." Thousands use a (half-)space separator for 5+ digit numbers. Space between initials: "В. И. Пупкин," never "В.И.Пупкин."

---

## 3. Экранная типографика и вёрстка

### Resolution has no inherent meaning

- **Разрешение картинок** (§ 69): a digital image file has no inherent "resolution" — only devices (screen, printer) resolve dots per inch. **"Картинке в «Фотошопе» совершенно все равно, сколько ей задать точек на дюйм."** The 72 DPI convention traces to early Macintosh's screen-to-print WYSIWYG mapping. DPI metadata is ignored on-screen by browsers/monitors — it only matters for print sizing. **"Размер пикселя — это как размер ангела: точных данных ни у кого нет."**
- **Разрешение экранов** (§ 70): screens/GPUs don't actually know their own DPI. Apple picked 72 DPI (true WYSIWYG at the time); Microsoft picked 96 DPI (~1.3×), assuming 1024×768 should fit comfortably on a 14" display. Identical point-sized fonts render physically larger on Windows than Mac — a 12pt font is 72px tall on Mac vs 96px on PC.

### Pixel graphics and its limits

- **Смерть пиксельной графики** (§ 71): screen resolution behaves like map scale — more pixels means more detail shown smaller, not "more size." Setting type size in pixels is "технически просто, но дурным тоном" (technically easy but bad practice) — prefer resolution-independent (vector) units. As pixel density rises, individual pixels become imperceptible, so purely pixel-based UI chrome (icons, cursors, pixel fonts) is a dead end.
- **Печать пиктограмм и скриншотов** (§ 155): the "everything needs 300 DPI" dogma wrongly applied to pictograms/screenshots — inherently low-res graphics. **"Чтобы напечатать пиктограмму или скриншот на бумаге, достаточно их механически растянуть без каких-либо предварительных сглаживаний"** — scale mechanically, no smoothing. Interpolation is right for photos, wrong here — it blurs sharp pixel edges. The rough/angular enlarged look is correct, not a defect.
- **Limit of font scaling** (§ 134): metal type physically prevented distortion; DTP unleashed "столько образцов невообразимого уродства." **"Если шрифт хорош, его рисунок нельзя трогать — будет гарантированно хуже"** — if a typeface is good, don't touch its design. Tolerance ≈ 1–2% compression, imperceptible. Training method: distort your own photograph alongside the font; stop scaling type once facial distortion becomes visible in the photo.
- **GIF compression** (§ 8): GIF compresses row-by-row horizontally — a run of identical horizontal pixels compresses far better than the same run vertically; a 90°-rotated version of the same image can be 3–4× smaller. GIF fits flat graphics (text, lines, solid fills), not photographs.

### Theory of proximity, shared air, symmetry

- **Теория близости** (§ 136): **"Объекты, расположенные близко друг к другу, воспринимаются связанно"** — objects placed close together read as related. **"Рядом, потому что связано."** Rooted in Gestalt psychology. A header must sit closer to its own paragraph than to neighboring text — equal spacing above/below creates ambiguity. Illustration: a woman standing equidistant between two men reads as unaffiliated with either. Inverse principle: **"Трудно различать объекты с одинаковыми признаками"** — objects sharing identical traits are hard to tell apart; differentiate distinct elements via position, size, weight, or color.
- **Воздух общий** (§ 166): intrusive web ads are like the childhood prank of waving a hand in someone's face saying "the air is shared" — not technically a boundary violation, but it feels like one. **"У рекламы должно быть свое четко обозначенное место"** — advertising must have its own clearly bounded territory, no right to intrude beyond it without explicit user action. Only a deliberate click specifically to view the ad counts as consent, and even that trigger can't sit inside the main content's space.
- **Симметрию — на помойку** (§ 85): **"Симметрия помогает дизайнеру все испортить"** — symmetry actively enables designers to wreck meaning; never apply it for tidiness alone. Failure mode: reordering words purely to visually balance a sign ("Кино Полярный театр" for a theater actually named "Полярный") sacrifices correct reading order for symmetric shape — measured cost: real readers took 7–30 seconds to parse aloud, often misreading entirely. Symmetry must serve communication; if it breaks reading order or clarity, drop it.
- **Punctuation neutralization** (§ 143): text often looks unruly only because the designer skips neutralization techniques. Tracking: punctuation spacing stays tighter than letterspacing. Centering: center as if no punctuation existed, then place marks after — ellipses especially distort centering if measured in. Match punctuation weight/style to adjacent text (bold punctuation with bold words). Hyperlinks go before quotation marks to avoid underline clashing with marks. Footnote numbers go before punctuation, not after. Never mix Russian/English/French typographic conventions in one text. **"Признаком хорошей верстки является незаметность сложных моментов"** — good typesetting keeps its hard problems invisible.

### Цветовые модели (§ 40)

- Color models are chosen by application, not inherent superiority: **"CMYK — в полиграфии, RGB — на экране, LAB — для описания и хранения любого цвета"** — pick the model that fits the medium, not a personal favorite. CMY in theory yields black but in practice yields muddy brown, hence the added K plate — and "K" stands for "key color," not necessarily black, a common misconception to correct. You don't need to invent a new color model — a numeric pattern within an existing space is enough to produce a perceptibly harmonious palette even from a limited set of hues.

### Перспектива и вертикальные линии (§ 101)

- The human eye reads all vertical lines as vertical and parallel — any rendering that lets verticals lean or converge incorrectly reads as visually "wrong," regardless of style era. Check architectural/product renders and photography for accidental converging/leaning verticals — most rendering-software defaults get this wrong, and it's immediately perceptible even to non-experts.
- **"Хорошая иллюстрация всегда является дополнительным аргументом в пользу достоинств товара. Плохая иллюстрация констатирует печальную правду"** — a good illustration argues for the product's quality; a bad one states an unfortunate truth about the maker's care.

### Матрица эмоций — spatial direction reads as emotion (§ 137)

- The sum of "up" and "forward" vectors points to the upper-right corner — **"это самый «позитивный» угол"** — the most positive direction in a composition. Combining vertical (up/down) and directional (forward/back) axes yields 8 emotional zones: top-right maximally positive, bottom-left maximally negative, center calm/balanced.
- Case studies: YUKOS's descending diagonals plus a downward-pointing triangle read as collapse despite bold type; BP's symmetrical rays toward lowercase letters combine dynamism with stability, reading as positive.
- Caveat: applies only to *dynamic* compositional elements, not static objects, and not to multiple compositions sharing one surface — don't over-apply it literally.

### Цифровое и аналоговое (§ 118)

- **"Цифровое дискретизирует сознание и рождает роботизированность, аналоговое — гладкое, хотя и менее функциональное"** — the digital discretizes consciousness and breeds mechanicalness; the analog is smooth but less functional. Digital wins on precision but risks dehumanizing perception; analog preserves continuity at the cost of capability — weigh this when balancing technical function against human-centered experience.

---

## 4. Веб-конвенции

### Гипертекст — hypertext fundamentals

- History (§ 54): hypertext predates computing — Gilbert of Poitiers's 12th-century Psalter cross-referencing, Bush's "Memex" (1945), Nelson's "hypertext"/"Xanadu" (1965), Engelbart's first working system (1968), Atkinson's HyperCard. **"Со времен Возрождения, кроме скорости перемещения по ссылкам, мало что изменилось"** — since the Renaissance only the speed of following links has changed; a good hyperlink apparatus takes the same care it always did.
- **Секреты хорошего гипертекста** (§ 83): text must survive being detached from its links (e.g. printed out) and still make sense — **"Если текст в отрыве от браузера непонятен, то гипертекст плох."** Never link from vague words like "here"/"there" — link text itself must carry meaning. Don't over-link: **"Если каждое второе слово подчеркнуто, читатель перестает воспринимать текст."** Prefer clustering links at the end of a passage over mid-sentence scattering. Only link where it adds genuine value. Cross-reference prior related material for full context. Keep link text short (1–2 words), never used purely as a highlighting device.

### Правила оформления ссылок — link styling rules (§ 171)

- Links always underlined, even if ugly; never underline non-link text. Don't remove the underline on hover.
- Active links: blue (or black/dark gray); visited: purple. **"Ссылки других цветов гарантированно сбивают с толку читателя"** — other colors reliably confuse readers; reserve link colors exclusively for links.
- On hover: highlight red/orange or change background/border.
- Dotted underline = in-place toggle/tooltip/calculator; solid underline = actual page navigation.
- Ultimate test overriding all the above: **"Если зритель, не притрагиваясь к мыши, может угадать, где ссылка"** — a viewer should spot links without touching the mouse.
- Liberal linking (§ 42): **"Ссылки можно и нужно ставить на любую страницу в интернете. Спрашивать разрешения никогда не надо"** — link to any page freely; asking permission first is unnecessary and stifles the web's basic value mechanism. Warning signs: zero outbound links, a token "Links" page pointing at Microsoft, or 88×31 button link-farms ("один из самых идиотских форматов").
- No self-links (§ 75): **"ничто не должно содержать ссылку на само себя"** — nothing should link to itself, because "любая ссылка подразумевает перемещение" (a link implies going somewhere). The logo-as-home-link must be inactive on the homepage itself.

### New windows and forced navigation

- **Открывание новых окон** (§ 43): **"Открывать новые окна против желания пользователя — смертный грех"** — opening windows the user didn't request is a cardinal sin; the browser window is the user's control surface, not the site's. Only legitimate case: linking to unverified external content, and even then the site must say explicitly it's opening a new window. Unsolicited window-opening is spam.
- **Порноиндустрия anti-patterns** (§ 41), reject in any review: max two 468×60 banners per page; max six 88×31 buttons (use a real "Links" text section instead); never force links into new windows; never spawn a replacement window when the user closes one; no unsolicited pop-ups (trigger only via explicit action); never hide browser chrome or force fullscreen to block the back button. **"Дизайн должен быть эффективен без использования нечестных приемов."**

### URLs

- **Боремся за чистоту урлов** (§ 48): plan directory/file names deliberately; keep URLs short and self-explanatory. Prefer English for paths; Russian only for transliteration/already-naturalized loanwords — never mix languages within one path. **"Посетитель всегда должен получить осмысленное и предсказуемое содержимое, если он стер часть адреса до ближайшей косой черты"** — truncating a URL at any slash must land on a meaningful, predictable page.
- **Cyrillic domains** (§ 68): don't register/use them — mixing alphabets breaks navigation, Cyrillic percent-encodes into unreadable strings, mail can fail to deliver, transliterated fallback may be taken, glyph lookalikes enable spoofing (Cyrillic "ВМ" mimicking Latin "BM" in "IBM"), requires compatible keyboard/encoding. Analogy: license plates are Latin-only for global legibility.
- **Дублирующая навигация / breadcrumbs** (§ 49): exist to substitute for a URL's own legibility. **"Дублирующую навигацию следует использовать во всех случаях, когда присутствует логическая вложенность содержания, но отсутствует отдельное боковое меню"** — use breadcrumbs whenever content nests logically and there's no sidebar menu.

### Заставки — splash screens (§ 46, § 47)

- Splash screens solved a real problem once (pre-auto-detect Cyrillic encoding selection); once that problem vanished, most became pure friction. **"Если нет стопроцентной уверенности в необходимости заставки… заставку делать не надо"** — when in doubt, cut it. Never use a homepage screenshot as the splash — produces jarring double-navigation. News/timely sites lose credibility with a splash delay; splash pages belong only to rarely-changing content.
- If used at all, core job is to be an entry point — always provide a clear text link in. Flash splashes: always include "skip," never replay on repeat visits, auto-detect rather than ask. **"Поменьше загадок для новых гостей"** — minimize riddles; don't gate access behind timers, unclear icons, or unfinished animations.

### Статусная строка (§ 50)

- The status bar tells the user where a link leads and shows load progress — hiding/overwriting it removes expected information, like taping over a car's speedometer. **"Нельзя вмешиваться в привычный стандартный интерфейс и нельзя прятать его элементы в ситуациях, когда человек их ожидает."**

### Звуки на сайтах (§ 51)

- The web is a silent, book-like medium by default; users are unprepared for sound. **"В интернете нельзя использовать звуки и музыку в декоративных целях"** — never use sound/music decoratively. Acceptable only when explicitly opted in and carrying real semantic meaning.

### Mobile versions — the position, and its reversal

- **§ 177 (original)**: **"Самая большая глупость на свете — создание отдельных мобильных версий сайтов"** — creating separate mobile site versions is one of the world's greatest follies. **"Делать мобильные версии сайтов есть смысл только за деньги тех, кому некуда деньги девать"** — only worth doing with money from clients who have nowhere else to spend it. Modern smartphones render normal sites correctly; "mobile version" is largely agency sales rhetoric.
- **§ 182 (two years later, partial reversal)**: mobile sites are no longer automatically the worst option, since mobile devices now outnumber computers. **"Чем больше экран, тем лучше интерфейс"** — the bigger the screen, the better the interface (an enduring rule he still holds). **"Качество уходит на второй план"** at this stage of adoption, but **"ренессанс всегда наступает после темных веков"** — a renaissance always follows a dark age; treat the current mobile-quality compromise as temporary.

### Главное правило экранных интерфейсов

- **"Любые элементы управления не должны быть по площади меньше квадрата размером 16×16 пикселей"** (§ 168) — no control element should be smaller in area than a 16×16 px square — baseline for clickable-target usability.

### Два главных принципа построения интерфейсов (§ 76)

1. **Unity of form and content across all control surfaces for one function.** The same function (e.g. volume) must use the same physical control mechanism everywhere, or users never build motor memory: **"Это не просто неудобно. Это создает очень большие психологические сложности, так как у пользователя не вырабатывается моторная память."** **"Если мы меняем звук колесом, то регулировка звука везде должна производиться именно колесом."**
2. **Two-way communication/feedback.** Any remote control of state must feed the state back to all control surfaces in sync (Radiotehnika R-100 example: adjusting volume remotely must update the remote's own display too).

### Interface engineering needs domain experts, not just software polish (§ 90)

- BMW's original iDrive controller: digitizing controls just to look advanced backfired — underused 8-way pad, slow menu navigation for safety-critical functions (traction control buried in menus instead of a dedicated button), physically misplaced controls (CD-eject hit by a passenger's knee). Root cause: disconnect between software engineers and domain (automotive) engineers — a caution against centralizing physical controls into a menu system without domain-aware validation. Charging a premium for a "luxury" interface that is actually worse usability is unnecessary complexity marketed as sophistication — the opposite of quality.

### Пиктограммы и идеограммы (§ 78)

- Pictogram = literal depiction (a glass = a glass); ideogram = symbol standing for a broader concept (a glass = drinking culture, statistics) — ideograms are inherently ambiguous without context. Even "self-evident" pictograms often need text to disambiguate.
- **"Человек в состоянии моментально увидеть и распознать некоторое ограниченное количество объектов"** — humans instantly recognize only a limited number of distinct symbols; cram too many into one field (dense road-sign clusters) and none of them read. When a pictogram's meaning isn't instantly unambiguous, duplicate it with text.

### Подписи на фотографиях (§ 169)

- **"Не нужно превращать подпись на фотографии в рекламу"** — don't turn a photo credit into self-promotion (no frames, decorative fonts, prominent placement). **"Подпись должна быть видна только тогда, когда мы ее осознанно ищем"** — a caption should be visible only when consciously sought — low-opacity, discreet, present only if needed.

### Other web/interface conventions

- **"K"/kilo- ambiguity** (§ 84): binary 1024 (memory) vs. decimal 1000 (drives, bandwidth) — always check which base a spec means before quoting a number. Flag as a marketing trick: manufacturers exploit the gap to advertise larger-sounding capacities.
- **404 pages** (§ 93): state the error immediately, including in the tab title; no ads, no long copy, no decorative graphics (logo excepted); don't reuse normal site chrome; explain plainly what happened; preserve the erroneous URL in the address bar.
- **Data preservation** (§ 188): **"Все данные, которые ввел пользователь, — священны. Всегда, во всех ситуациях"** — all user-entered data is sacred, always. After a crash/restart/closed window, the user should reopen and continue exactly as if nothing happened — full state restoration, no re-entry. An ethical baseline, not a UX nicety.
- **Скиномания / customization** (§ 65): let users customize *how* content looks, never *what* content appears — editorial identity is non-negotiable: **"самое главное для издания — сохранить свое лицо и свой голос."** Editorial/news sites forbid customization; service sites (search, mail) may allow it.
- **News on non-news sites** (§ 129): **"Новости на морде — это самый дешевый способ показать посетителю, что сайт еще живой"** — a homepage news feed is the cheapest way to fake vitality. If updates come less than monthly, drop the word "news." **"Даты являются совершенно мусорным элементом, засоряющим пространство сайта"** — dates next to headlines are clutter; readers learn something's news by reading it. Archive stale items immediately.
- **Informational vs presentational sites** (§ 56): informational design (well-marked highway) vs. presentational/eclectic design (ornamental garden maze) — legitimate but opposite purposes. **"Сайт без картинок и теней — это тоже сайт"** — a site with no images/shadows is still a real site; staying usable at any window width is harder and more valuable than a fixed-width graphic showcase. Anything over 5–10 seconds to load loses to faster alternatives.
- **Placeholder content / рыба** (§ 66, § 67): placeholder should look like real content, not an obvious stand-in — repeated boilerplate ("Тут будет текст...") is one of the worst effects in a design review. Write custom, plausible placeholder copy instead. Check Lorem Ipsum for accidentally inappropriate corrupted content before shipping.

---

## 5. Текст и язык

### Короче — say it shorter (§ 141)

- **"Сообщение всегда должно учитывать условия его получения"** — a message must always account for the conditions under which it's received. Case: a roadside sign near Taganrog reminding drivers to buckle up fails via ALL CAPS (slows reading), uneven spacing, cramped line spacing, superfluous address ("Водитель!"), bureaucratic compound nouns. Fix: direct, imperative, minimal — "— Пристегнись! Включи фары!" Brevity here isn't style preference but a functional requirement given speed and limited attention.

### Корпоративный русский (§ 114)

- **"Компаниям должно быть стыдно, что они находят деньги на ремонт офиса раньше, чем берут в штат редактора"** — companies should be ashamed they fund office renovations before hiring an in-house editor. Corporate marketers mechanically transliterate English into Russian, producing unnatural phrasing ("Теперь одновременно" for "All Together Now"). Slogans increasingly function as pure graphic elements, unfit for speech: **"синтетика не предназначена для устного использования."** New logo trends place taglines below the mark in unnatural word order, violating Russian syntax.

### Штампы — clichés (§ 123)

- "Клише" and "стереотип" began as pure typographic terms (a printing plate; a cast plate from a matrix) before drifting into general synonyms for banality across Europe. Illustrates how technical vocabulary migrates into metaphor for mechanical repetition — worth knowing when flagging clichéd copy.

### Факты — facts (§ 125)

- Shared flaw of Russian designers and journalists: disregard for factual accuracy, source-checking, quote verification. **"Для дизайнера и журналиста любая работа — импровизация на тему заданных ключевых слов"** — for both, any assignment becomes improvisation on given keywords rather than fact-grounded work. **"Человек, которому есть что сказать самому, позволяет другим иметь свое мнение"** — someone with genuine content of their own lets others hold their own opinion; insecure people copy/misquote. Contrast: *Wired* employs dedicated fact-checkers, a standard largely absent in Russian publishing.

### Слоганы — slogans (§ 30, § 160)

- **"Попытка придумать рифму к торговой марке при полном отсутствии языкового чутья"** — forcing a rhyme onto a brand name with no ear for language; reject slogans that exist only to rhyme, with no linguistic sensitivity behind them.
- **Two widespread myths** (§ 160) responsible for more bad design/advertising than almost anything else: Myth 1 — **"Хороший логотип должен быть таким, чтобы любой человек мог его по памяти от руки изобразить"** — a good logo should be drawable from memory by anyone (false). Myth 2 — **"Это хорошо, если реклама не сразу понятна… человек… лучше запомнит такую рекламу"** — it's good if an ad isn't instantly clear because decoding effort aids memory (false). Clarity and genuine effectiveness beat forced simplicity or contrived obscurity.

### Robot-speak and automated text (§ 98)

- Mass-produced automated text (mail-merge greetings, generic "подробнее" links, auto-truncated ellipses) reads as robotic — avoid or hand-finish it. Russian is harder to automate correctly than English due to its rich inflection; don't port English-style templated copy into Russian without editorial review. Named failure: "Доброе время суток" as the emblem of machine-like phrasing.

### Честная маркировка (§ 127)

- Serious publications must clearly label superstitious content (horoscopes) as such, rather than presenting it as credible reporting — the same way ads are marked "на правах рекламы." Calls astrology forecasts "окончательная и бесповоротная херня" while granting entertainment value — insists on labels like "предрассудки" or "развлечения." (*Kommersant* actually discontinued horoscopes 12 January 2009.)

### Бумага стерпит — printed carelessness (§ 128)

- **"Бумага стерпит и во второй раз"** — paper's infinite tolerance gets exploited by publishers who show contempt for readers via careless printed content. Named failures: a translated design book that never converted imperial measurements to metric, forcing readers to calculate; a factory-director "interview" that reads like a raw spec sheet, suggesting no real dialogue occurred.

### E-mail culture — 10 commandments (§ 189)

1. Strip quoted headers ("On 18 Jan 2018, at 18:14, Vasya Pupkin wrote:") — "стопроцентный мусор."
2. Quote selectively — only the relevant portion, never the sender's signature block.
3. Separate your reply from quotes with blank lines; double-space between quoted sections.
4. **"Ответ должен быть длиннее цитаты"** — your reply must be longer than what you quoted.
5. Embed images directly in the message body — never send zipped image archives.
6. Keep messages under a couple of megabytes.
7. Don't bury text inside Word documents — the email body renders text fine.
8. Signatures: max 3–4 lines, no logos, no decorative icons.
9. Use your real full name or a clear identifiable nickname — not something generic like "Sasha."
10. Always fill the subject line, update it once the thread's topic shifts.

---

## 6. Работа с клиентом и профессия

### Клиент всегда неправ (§ 87)

- **"Клиент всегда неправ"** — the client is by default wrong on design questions, preoccupied with business concerns, not visual culture. The designer must hold a defensible position, not simply execute requests verbatim — closer to an "illusionist" delivering results that land with the real audience. **"Важно, чтобы поняли те, с кем клиенту приходится иметь дело. Те, ради кого, собственно, делается дизайн"** — design succeeds when it works for the client's audience, not when the client personally "gets" it.
- **Плохие дизайнеры и плохие заказчики** (§ 86): rejects the "client forced me" excuse — **"плохого дизайна не было бы, если бы не существовало плохих дизайнеров"** — bad design cannot exist without a bad designer executing it. The designer bears final responsibility: block a bad concept or elevate a mediocre client idea into something that works.
- **Хочу как у них** (§ 103): clients copy a competitor's visual identity without grasping the strategic logic behind it. A mark like BMW's is good only because it sits on good cars — copying surface design without the underlying product excellence is like **"съедание коленной чашечки чемпиона мира по бегу для победы в марафоне"** (eating the champion's kneecap to win the marathon). Design excellence is exemplary only in service of genuinely excellent products.
- **"А что если заказчик умнее тебя?"** (§ 140): a designer is easily paralyzed by this question, which exposes that designer confidence rests on an unexamined assumption of superiority. Critiques the belief that a designer's work is Art deriving worth from authorship alone, rather than from solving real problems.

### Авторство неотчуждаемо (§ 14, § 15)

- Authorship right arises at creation and is inalienable — **"неотчуждаемым"** — it cannot be bought, sold, or gifted away, even when usage rights are sold. Selling a work transfers usage rights, not authorship: a designer keeps the right to show a commissioned logo in their portfolio even after the client owns exclusive usage. Plagiarism means copying idea, look, or solution with minimal change; working in someone's manner without copying specific elements violates nothing.
- The five marks — © ® ℗ ™ ℠ — are reminders only: **"наличие любого из этих символов… не значит ровным счетом ничего, кроме напоминания."** Their absence doesn't remove legal protection; misapplied/decorative use of © is **"признаком невежества"** (a mark of ignorance). If proper glyphs are unavailable, (c)/(r)/(TM) text substitutes are poor form given modern typography — use the real character.

### Фокус-группы (§ 126)

- Marketing as **"многоступенчатая система по сниманию ответственности"** — a system for offloading accountability, focus groups its chief instrument. Paid participants (≈500 rub/hr) invent opinions to justify their presence; moderators suppress genuine expertise while amplifying buzzwords like "престиж"/"лояльность." **"Все, что можно узнать, спрашивая мнение людей, — это то, что они знают сегодня"** — polling only reveals what people already knew before your new product existed; it cannot predict genuine innovation. Segway and Apple bypassed focus groups entirely and still succeeded.
- **Related — research-as-dogma** (§ 130): eye-tracking studies showing users look at the upper-left aren't universal law — **"Люди смотрят туда, где им что-то показывают"** — attention follows content, not fixed zones. Reject the above-the-fold myth; scrolled-past content isn't forgotten. **"Цвет — явление идеологическое"** — color is contextual, not inherently symbolic; treating color meaning as fixed and universal is "шаманство хуже гороскопов," shamanism worse than horoscopes.
- **О маркетинге** (§ 115): entire thesis, unelaborated — **"Маркетинга не существует"** — Marketing does not exist.
- **Большая маркетологическая глупость** (§ 96): don't let "research says" claims or folk-wisdom market opinions override professional judgment without real evidence. Case: Intel's global one-word "Yes" campaign, forced by Russian regulation to add a footnote translating it to "Да" — the disclaimer semantically downgraded a confident statement into "yes, but maybe not." A mandated disclaimer can invert a design's core communicative intent — check what a required addition does to meaning, not just layout.

### Гайдлайны (§ 117)

- **Rule 1**: the guideline author must know exactly what to communicate and state it plainly — **"читатель не сможет догадаться, какие знания остались в голове составителя"** — spell out even the "obvious."
- **Rule 2**: guidelines need a competent interpreter who knows when rules can/should be broken and briefs the designer accordingly — not literal rule-following.
- **"Бездумное составление гайдлайнов и буквальное их прочтение — пустая трата времени."** Bad guidelines pad themselves with meaningless symbolism ("round logo = perfection, square = stability"); good guidelines (BBC's pixel-grid explanation) teach the designer something they didn't already know.

### Инструменты вместо фотостоков (§ 61)

- **"Использование готовых картинок из фотобанков является моветоном, если мы говорим о дизайнерской работе"** — stock photography is poor form for real design work. Under time/budget pressure, produce original material instead: scan or photograph real objects, hand-letter and scan text rather than using script fonts, stage real people/colleagues rather than generic stock models. Exception: stock is acceptable only for genuinely unobtainable imagery (space photography, archival footage) — and even then, prefer sourcing the primary material directly.

### Бланки: клиент боится пустоты (§ 102)

- A blank/letterhead is a simple, utilitarian object needing no special decoration: **"Бланк — очень простой, утилитарный и функциональный объект, не требующий специального украшения."** Clients mistake empty space for unfinished work — present blanks filled with sample correspondence, not empty, to preempt the "it's empty" objection. Functional constraints override decoration: no background images (fax transmission), generous left margin (hole-punching), absorbent non-glossy paper (stamps/signatures). Prefer restraint — a subtle "графическая рифма" over decorative excess.

### Э-коммерция не спасает офлайн (§ 60)

- **"Электронной коммерции не существует"** — rejects the term as marketing hype. A company must get its offline fundamentals right — delivery, service, logistics — before an online storefront can work; e-commerce doesn't fix broken commerce.

### Нейминг (§ 94)

- Four historical naming strategies, useful as a checklist: founder's name (Bosch, Chanel); geography (Nokia, Zhiguli); invented/unique letter combos (Kodak, ABBYY); abbreviations (IKEA, SAAB). Successful naming is largely circumstantial, not formulaic — **"nobody conducted focus groups"** for the brands that became iconic; be skeptical of naming decided by focus group or phonosemantic pseudo-science.
- Debunks the "25th frame" subliminal-message myth (Vicary's fabricated 1950s popcorn study; human perception can't resolve information at that speed) — a caution against basing design decisions on popular pseudoscience rather than professional judgment.

### Заявка на дизайн (§ 95)

- Reviewer's method: study failure, not success — **"Изучение «удачного» дизайна не дает никакой возможности понять, как в будущем не сделать ошибок."** Four-stage lifecycle, diagnostic lens: (1) a problem arises, (2) ordinary people notice/name it, (3) they improvise a DIY fix with available materials, (4) a professional solution finally replaces the improvisation. Scan the environment for visible DIY workarounds — each one is a live, undocumented design brief nobody has answered properly yet.

### Логотипы (§ 124, § 152, § 157)

- Word "логотип" drifted across three eras: 19th c. — synonym for a ligature (fused characters); late 19th c. — any reusable text plate (masthead needing no resetting); 20th c. — anything: lettering, mark, or combination. Illustrated with Paul Rand's IBM mark, Rob Janoff's Apple logo, Mercedes-Benz star.
- **Trademarks becoming everyday words** (§ 152): a healthy process, not a violation to resent. **"Хорошо, когда язык живет"** — good when a language is alive. Insisting on generic terms (копир instead of ксерокс, внедорожник instead of джип) is as absurd as calling cognac "brandy." ~80 former trademarks are now ordinary Russian words: адреналин, аспирин, джип, героин, ксерокс, линолеум, термос, эскалатор.
- **О стилизации** (§ 157): one line, unqualified — **"Любая стилизация — это ужасно"** — any stylization is terrible.

### Творческий кризис, зона комфорта, and working conditions

- **Творческий кризис** — see § 1 above (§ 162): crisis only arises from targeting originality as the goal; the original surfaces only while actually working the problem.
- **Зона комфорта** (§ 172): differences in urban quality of life stem from psychology, not national wealth. **"В России традиционно зона комфорта заканчивается у человека его входной дверью"** — in Russia the comfort zone traditionally ends at one's own front door. **"Начать расширять свою зону комфорта очень просто: нужно для начала разрешить в ней оказаться хотя бы еще кому-нибудь"** — expanding it starts by letting at least one more person in.
- **Напряг и свобода** (§ 179): managing creatives requires two independent controls, not one dial with opposite ends — **"Это два разных регулятора."** Too much of either pressure or freedom degrades output; balance is per-designer, per-project.
- **Эстетика контроля и запрета** (§ 180): restrictive rules don't have to breed resentment. **"Любой контроль или запрет можно настолько изящно преподнести, что никто не почувствует себя униженным."** **"Неприятное или неинтересное должно быть подано так, чтобы все этого хотели."** Examples: Russian passports (blunt) vs. US driver's licenses as ID (normalized); bollards vs. gates; landscaping vs. fences.
- **Идея на минус миллион** (§ 161): ideas have no legal protection and inventors habitually overvalue them. Every real idea needs serious capital to become anything — "минимум миллион" before any return. **"Любой изобретатель или дизайнер, рассказывающий о своей идее, должен честно говорить: 'У меня есть идея на минус миллион.'"**
- **Софтверизация** (§ 184): **"Все, что может быть софтверизовано, будет софтверизовано"** — everything strippable of its physical form will be turned into software (phone exchanges, water meters, books, posters, road markings, music's arc concerts→vinyl→streaming). Use this lens to judge which industries deserve investment and which are dissolving into software.
- **Со временем всё портится** (§ 151): craftsmanship perceptibly declines across generations even as technology advances — anatomical atlas illustrations degrade from masterful (1900) to flat (1992) to incompetent (2007, artist doesn't know anatomy). Self-aware paradox: **"Интересно, как поменяется восприятие, когда эта иллюстрация будет считаться образцом для подражания"** — today's ugly outputs may look like tomorrow's gold standard.
- **Мастерство важнее месседжа** (§ 154): tracing the pointing-finger recruitment poster (Kitchener's "Your Country Needs YOU," Moor's "Ты записался добровольцем?") — **"Моор был не просто превосходным художником, он еще мастерски владел плакатным словом"** — visual/rhetorical craft, not just the message, decides whether persuasive design actually works. A failed 1919 counter-version (formal "you," weak type) proves competence, not idea alone, decides effectiveness.
- **Бессмысленная презентация** (§ 145): **"Лучшая презентация та, которую не показали"** — the best presentation is the one never shown. Slide format forces oversimplification; audiences read text faster than a speaker can say it aloud; Russian business culture is oral/dialogic and resists PowerPoint — real decisions happen after the slideshow, among leadership.

---

## Lebedev's razor — 10 sharpest one-line tests

1. **Has the task actually been solved?** — the only valid design question (§ 149): "дизайн не надо обсуждать, он является решением поставленной задачи."
2. **Simple, but not primitive?** — did restraint keep the meaningful detail, or just remove consideration? (§ 147)
3. **Can it be cut in half?** — "любой интерфейс можно упростить в два раза" — find the redundant control/element before shipping. (§ 110)
4. **Would this survive detached from its medium?** — text off the browser, hypertext off its links, message off its channel — does it still make sense? (§ 83, § 141)
5. **Can a viewer spot it without touching the mouse?** — the link-visibility test, generalizable to any affordance. (§ 171)
6. **What's the worst possible version — and did you remember to flip it back?** — от обратного; the reversal, not just the imagining, is the design. (§ 150)
7. **Does this exist because it's cheaper than the alternative, or because it's actually needed?** — urns, bottlenecks, constraints: know the real economic/functional cause before redesigning. (§ 88, § 140)
8. **What does this do to the meaning, not just the layout?** — check what a mandated disclaimer, a client add-on, or a "safety" caveat does to the message's actual force. (§ 96)
9. **Would a security guard giving directions beat this signage system?** — "охрана дает справки": if the wayfinding needs a manual, it has already failed. (§ 131)
10. **Is this a law, or just a guideline that worked once?** — "в дизайне законов нет" — interrogate every rule, including these, against the specific constraints in front of you. (§ 99)

---

*Compiled from Ководство §§ 0–191 (published sections only). Sections skipped as pure historical trivia, humor, satire, or visual-only content with no extractable rule: § 27 (Коломнин reprint), § 39 (Chaif song tribute), § 80 (backdrop critique, polemic), § 100 (image-only), § 113 (satirical Declaration of Independence), § 122 (book spine convention, historical), § 138 (кофе gender, linguistic trivia — cf. § 152 on living language), § 144 (Leonardo quote, anecdotal), § 170 (Негры — historical/critical, no actionable rule), § 173–174 (Дед Мороз, Белый Кремль — culturally specific asides), § 183 (Chinese font trivia).*
