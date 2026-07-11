# UI Assessment Canon — Ilya Birman + Lebedev

Dense reference for judging any interface. Source: Ilya Birman's advice column (bureau.ru/soviet, with Artyom Gorbunov / Bureau Gorbunova), 698 soviets, plus his lecture «Навигация» and electronic textbook «Пользовательский интерфейс» (bureau.ru/books/ui); Lebedev's kovodstvo supplies affordance/forms/layout material Birman doesn't cover directly. Canonical Russian formulations are kept in «quotes» with an English gloss. Each bullet is one usable rule — apply it directly when reviewing a screen. Rules are grouped, not ranked; use the Diagnostic checklist at the end to prioritize.

---

## 1. Принципы (Foundations)

### Интерфейс как мир пользователя
- Raskin's definition, adopted as the baseline: an interface is «способ, которым вы выполняете какую-либо задачу с помощью какого-либо продукта» (the way you perform a task with a product) — the actions you take and what you get back.
- «Не бывает нематериальных интерфейсов» (no interface is immaterial) — every rule has a physical embodiment; the designer's job is to minimize the number of gestures and messages required to get the task done.
- Observe the real user, don't imagine them: before advising on a specialized interface (admin panel, dashboard), watch an actual person use it — «Сел бы за спиной у администратора и смотрел бы, как он администрирует» (sit behind the admin and watch them administer).
- Reading the finished artifact alone is not equivalent to watching it used — silent observation, then asking "что ты сейчас сделал? зачем?" (what did you just do, and why?), surfaces the repeated actions and points of friction a spec never shows.
- The interface stays passive toward the user, never the reverse: it waits for commands and executes unconditionally — a computer is a tool, not a conversation partner.
- Avoid dialog-style prompts ("Хотите продолжить?" — Do you want to continue?) — most can be cut without loss of meaning; a plain command button gives more «чувство контроля» (sense of control) with fewer actions than a question-and-answer exchange.
- Ask a system question only when the system genuinely needs the clarification to proceed (e.g. "Сохранить файл перед выходом?" before an unsafe close) — not as a reflexive confirmation ritual.
- Don't flirt with the user: smileys, "this'll only take a minute," apologies and persuasion in interface copy read as cartoonish and out of place.
- A registration form must not manipulate through forced politeness or guilt.
- Explain why you're asking for any given piece of data. If a field looks superfluous to the user, they either abandon the form or lie in it.
- State the concrete benefit of a requirement instead of asserting it ("Курьер позвонит за час" — the courier will call an hour ahead — beats "Обязательное поле").
- Registration/login is frequently unnecessary. If the actual goal is identifying a returning customer, a phone number plus an SMS code is often enough — no separate "registration" step.
- Design from the user's scenario, not from the system's internal architecture or database structure: «Когда интерфейс продиктован внутренней архитектурой и системными понятиями, он превращается в неподдающуюся пониманию китайскую головоломку» (an interface dictated by internal architecture becomes an incomprehensible puzzle).
- One free-text field with clarification afterward often beats a form assembled from the system's own fields.
- Reality, for design purposes, is whatever is useful to the user's task at hand — map layers, data fields, even geographic accuracy should be chosen by scenario, not by abstract completeness.
- The user's mental model has four parts: habits (below); attention fixed on the task, not the interface's internal state (§2, modality); their own vocabulary, not the developer's (§7, stop-words); their scenario, not the programmer's data model (§4, navigation).
- Convergent design across competing products (streaming players, cars, forms) usually reflects converging functional/ergonomic requirements, not laziness — deviating just to "look different" typically costs measurable quality.
- A functionally superior but visually unfamiliar pattern can carry a real marketing cost (new users can't parse it from a screenshot) — note this trade-off explicitly rather than assuming "better UX" wins adoption by default.
- A client's request for "several options to choose from" is usually a symptom of low trust that you understood the brief — don't argue them out of it; find out what you failed to convey.
- Producing full alternative concepts "to pick from" (as opposed to reference images to align aesthetic expectations) is a red flag, not a service.
- To beat a client's mediocre idea, don't debate it — out-design it: «Чтобы убедить клиента, что от его идеи лучше не становится, нужно придумать идею, от которой станет ещё лучше, чем клиент думал, что станет от его идеи».
- Reformulate an operational objection as a requirement/constraint instead of letting it kill a good design: «Старайтесь переформулировать любое возражение в терминах требования или ограничения, и тогда дизайнить станет интереснее».
- «Focus is saying no to things» — consciously deprioritize secondary fixes to ship on time, but record the plan to close them, don't just drop them silently.
- Don't design "impossible" layouts: the interface must never cover or obstruct the content it exists to serve.

### «Интерфейс — зло» — идеальность по Альтшуллеру
- Altshuller's ideality, applied to interfaces: the ideal object is the one that doesn't exist, but its function is still performed.
- An ideal admin panel is no admin panel — inline editing in place of a separate management screen is the concrete application.
- An ideal wayfinding sign is no sign, with the environment itself performing the orienting function: «Идеальный маршрутный указатель — это когда его нет, а функция выполняется».
- «Пусть потеет машина» — let the machine sweat, not the person: if the computer can compute or remember something, it must, instead of routing it through an extra control.
- Example: retail/wholesale pricing should compute automatically from quantity, not toggle by hand — a manual toggle the user forgets to flip feels like a trap, not a feature.
- Don't predict or forecast on the user's behalf: «Не предугадывать и не прогнозировать. Выводы делает человек» — algorithmic forecasts from indirect metrics provoke false alarms and erode trust.
- Show objective facts (a red highlight on real overdue/over-budget data) and let the person draw the conclusion, rather than building a prediction engine.
- Minimization of construction (Gorbunov's second law of design, extended by Birman to interfaces): useful physical means shrink over time while the function they perform grows.
- Three techniques for minimization: (1) strip everything unnecessary (УВЛ), (2) factor out the repeated, (3) transfer a function onto an existing element instead of adding a new node (an iMac instead of a tower plus monitor).
- Simplification must never lose the underlying useful function — not every reduction counts as an improvement.
- Don't build an interface out of controls where data alone would do the job — showing information and letting the system decide correctly beats making the user operate a control.
- Hiding a genuinely necessary technical setting from the user doesn't excuse shipping a worse underlying default — if you remove a manual control (a COM-port speed picker), the automatic replacement is obligated to actually be fast and correct, not just invisible.
- Run slow background/automatic operations (device auto-detection, connection setup) in parallel with something the user is already doing, so the wait is never perceived as a wait at all.
- Routine hardware/configuration setup is what Cooper calls «наглые налоги» (excise taxes) on the user — the program, not the person, is obligated to absorb that cost.

### Информация, а не элементы управления
- Definition: «Информативность — это доля полезного содержания в общей длине сообщения» (informativeness is the share of useful content in the total length of the message).
- Lever one — **УВЛ, убрать всё лишнее**: borderless windows, scrollbars that appear only when needed, no gratuitous textures or gleams.
- Applying УВЛ to content: show only data relevant to the recipient, so, e.g., «письма можно было открывать не читая» (emails can be opened without needing to read them).
- Lever two — **вынести за скобки повторяющееся**: a word repeated in every row of a list becomes a section heading instead of a per-row repetition.
- Combine functions in one existing element rather than introducing a new one: «Всегда стоит подумать, как наделить новой функцией существующий элемент, а не вводить новый».
- Example: a blue star that simultaneously means "VIP" and "unread"; a window's close-button dot that signals both unsaved changes and resistance to closing; a progress bar merged directly into the address bar.
- The recurring diagnostic sequence, applied in order: **"Можно ли убрать что-то без потери смысла?"** then **"Можно ли автоматизировать то, что сейчас поручено человеку?"**
- Insufficient detail is also a failure of informativeness: an "infographic" reduced to a single bare number isn't an infographic — define what follows from what, and what to do on deviation, before styling it.

### Последовательное волшебство
- «Мы понимаем и принимаем правила игры, если можем их себе объяснить, если видим в них последовательность и логику» (we accept an interface's rules if we can explain them to ourselves).
- Every state and every transition must be explainable inside the interface's own "magic world" — a link that vanishes without a trace on click destroys trust in the whole system.
- Design process: first invent the desired behavior for the important individual cases, then generalize a single law from which that behavior follows.
- A good interface reduces to one simple rule with no exceptions (iOS view transitions); a bad one is a pile of special cases that resist generalization.
- The test for consistency: does the same gesture always produce the same result, everywhere in the product?

### Привычки и конвенции
- Habit fuses a complex sequence of actions into a single indivisible action in the user's perception: «Только те, кто понимают роль привычек, знают, как на самом деле работает интерфейс».
- Habit is double-edged: it speeds work up, and it is also the source of errors, because a habituated user "learns to confirm anything without reading" — which is why confirmation dialogs stop protecting against mistakes over time.
- Never change the order of key, frequently-used controls — swapping them is as dangerous as swapping the gas and brake pedals.
- Follow platform look-and-feel conventions rather than inventing your own from scratch.
- Good design accommodates human nature instead of fighting it — prefer Undo over blocking confirmations.
- Concrete pattern: Gmail's "delete sent" window, or a short delay before a payment fires, giving seconds to reconsider even though there's no true technical "undo."
- Variable reward strengthens habit more than a guaranteed one (Skinner's pigeon effect) — the unpredictability of a like/message/post is why people check more often than a guaranteed reward would justify.
- Apply variable reward respectfully: it should reflect genuine product value the user doesn't want to miss, not a manufactured compulsion loop.
- Don't fight standard OS/browser navigation (e.g. the Back button) — design so it never breaks or silently mutates additional state; it is not an Undo button and shouldn't be treated as one.
- Established icon/pictogram conventions (auto-dashboard glyphs, save-disk icon) shouldn't be redesigned just because no single "correct" universal image exists — habit outweighs a marginal semantic improvement.
- A component/behavior that seems arbitrary today may just be this year's convention, expected to shift again later — don't over-invest in reverse-engineering a "true" rule behind a fashion-driven UI choice.
- Radical interface changes are safer piloted in a new, separate product; once the change earns recognition there, migrate it back into the established product, which reads as less disruptive.
- Don't turn a content site into a database-management console for its own visitors — check that a familiar e-commerce pattern (a cart, a filter panel) actually fits the scenario before adopting it by reflex.
- A tree-structured comment/discussion system is worth its complexity only when comment quality genuinely doesn't matter — a linear system is the safer default.
- Redundant, physically separate channels for the same critical information (a primary display plus a backup readout) are worth the duplication precisely because any single channel can fail or be missed.

---

## 2. Обратная связь и состояния (Feedback & states)

### Базовый принцип
- «Действия пользователя должны вызывать в интерфейсе адекватную и заметную реакцию — обратную связь» (user actions must produce an adequate, noticeable reaction).
- Without visible feedback (e.g. a ticket machine silently printing for two seconds), the user assumes nothing happened and repeats the action.
- Five qualities of good feedback, used as a checklist: **мгновенность** (instantaneity), **непрерывность** (continuity), **честность** (honesty), **нежность** (gentleness), **физичность** (physicality).
- A design can be simultaneously excessive and insufficient at once — check both axes, not just "is it too much." Example: a smooth animated fill for PIN entry can feel like excess motion while still failing to honestly convey the exact digit count entered (no discrete steps).
- Don't overdo the reaction: an aggressive error alert (Photoshop's beep on an invalid selection) reads as punishment.
- A soft cue beats a hard rejection: macOS's password-field "shake," or a subtle field highlight, instead of a blocking dialog.
- Don't escalate feedback for routine events: «Если каждое добавление в корзину сопровождать появлением диалогового окна, покупателю это быстро надоест» (a popup on every add-to-cart quickly tires the shopper) — a barely-noticeable signal (a field's gentle wobble) is often enough.
- Birman is skeptical of "баланс" as a polite synonym for compromise between conflicting requirements — push for one solution that satisfies brand, feedback quality, and delight simultaneously rather than trading them off.

### Предотвращение вместо реакции
- «Хороший интерфейс предотвращает бесполезные и ошибочные действия пользователя» — disable a button visually instead of letting the user click it and only then showing an error.
- Use input masks that physically exclude invalid input, instead of validating after submission.
- Validate file type/size client-side before upload — the error should appear immediately, in place of the upload, not after it.
- Never give false-positive success feedback. If an action might silently fail (weak network on a smartwatch), confirm receipt of the command instantly, but report a failure within a short window if it occurs.
- «Вопроса «Сохранить?» не может быть, ответ всегда «Да». Вопроса «Забыть?» не может быть, ответ всегда «Нет»» — user data is infinitely valuable; save automatically, delete only on explicit, reversible request.
- Whether a genuinely destructive control (submit button that's disabled until required fields are filled) should be disabled-until-ready or clickable-with-inline-errors depends on obviousness: disabling is defensible for self-evidently required fields (email + password), but harmful in less typical forms where the reason for disablement isn't obvious — there it costs conversions, so bias toward a clickable control that explains what's missing on attempted submit.
- Don't accept a listicle argument that disabled buttons are inherently bad ("hard to notice," "unclickable") without checking whether each "flaw" is actually the button's intended function (unclickable = correctly signals the form isn't done yet) — evaluate against the state-design framework, not a surface pro/con list.

### Мгновенность, непрерывность, физичность
- «Если по мере движения невозможно отображать результат точно, показывайте его приближённо сразу; заменяйте точным потом» — Google Maps zooms the cache instantly while detail tiles load in behind it.
- A slider beats a modal dialog for any parameter with a visible real-time effect: «Двигая слайдер, человек в реальном времени наблюдает изменяющийся результат.»
- Recalculate live wherever the inputs allow it — no "Calculate" button standing between input and result.
- Scroll and drag gestures must track the finger with zero perceptible lag — not merely fast, but literally synchronous, which is what creates the illusion of directly manipulating an object rather than issuing a command to a device.
- «Интерфейсная реакция на действия пользователя должна иметь наивысший приоритет» — artificial animation delays create a sluggish feel even when the underlying system is otherwise fast.
- Choose the loading indicator to fit context: a stylized in-world preloader can extend immersion in a game; a generic spinner is the right default elsewhere.
- A stalled progress bar (frozen at one position) needs its own subtle motion added to signal it's alive, not broken.
- Progress indicators «не обязаны быть честными» (don't have to be honest) — managing perceived speed is a legitimate design goal even when it doesn't literally track real progress.
- Don't let unresolved backend verification block the interface: «Разрешайте всё делать сразу, а сами операции до подтверждения документов ставьте в очередь или исполняйте „понарошку"» — occupy the user with genuinely useful parallel work instead of a spinner.

### Модальность — канонический разбор
- Definition: «Интерфейс называется модальным, если у него есть состояния, которые человек не осознаёт в момент жеста, но в которых этот жест интерпретируется по-разному». A **modal error** results from not realizing which state the interface is in.
- «Модальность — это признак плохого интерфейса, а не небрежности пользователя» — it is entirely natural that attention is on the task, not on the interface's state.
- Not all mode-switches are modal: a deliberate, self-aware choice (long-pressing a known corner of a known app) isn't modality; accidentally triggering behavior while attention was elsewhere is.
- The half-measure — making state visible (Photoshop's cursor changing per tool, icons vibrating in rearrange mode) — has a real cost: «Интерфейс кричит пользователю: „Смотри, в каком я состоянии!"», which distracts from the task and blocks the formation of automatic habit.
- **Cure 1 — Разделить жесты**: distinct controls for distinct functions instead of one multi-meaning control (separate camera-shutter and video-record buttons).
- **Cure 2 — Квазирежимы**: a mode physically felt only while held (Shift for caps, a held mouse button while dragging) — unlike Caps Lock, which silently latches and stays on without being felt.
- **Cure 3 — Изменить сценарий**: select the object first, then apply one unambiguous action (select an email, then hit delete) instead of toggling a "delete mode" and clicking through items.
- Two-finger pinch-to-zoom instead of overloading one scroll-wheel axis for both pan and zoom is the same cure applied to a physical gesture conflict.
- «Универсальный способ избавиться от модальности пока неизвестен» — no algorithm exists beyond these three cures plus the half-measure; every case still needs judgment.
- Modality is usually reached for because it's the path of least design effort («простое решение, не требующее вдумчивой работы»), not malice — resist defaulting to a mode when short on space or buttons.
- Modality is also sometimes used deliberately against the user's interest (forced cookie/legal modals, ad monetization) — recognize this and decide consciously how much user comfort is being traded away.
- When modality can't be eliminated, mitigate with reversibility: any destructive action reachable through a modal error must be instantly undoable (⌘Z).
- Canonical case: ⌘W closing the wrong window in macOS — «Это модальная ошибка по определению.»
- A checkbox that syntactically behaves like a radio button (single click flips a multi-select's meaning) is an unresolved modal conflict — it needs an explicit modifier/mode-switch, not a semantic hybrid crammed into one control.

### Состояния элементов
- State must be legible from appearance alone: **focus** — outline/glow; **disabled** — reduced contrast and saturation; **pressed** — a "recessed" effect.
- States aren't always mutually exclusive — a visited link can also be in a pressed state.
- A disabled element has no hover state.
- Transitions between states should be instant, except the return-to-neutral transition (0.2–0.4s).
- A pressed/toggle visual only fits a genuine binary on/off meaning — don't reuse it for an action that isn't really a toggle.
- If it isn't a clean toggle, reword the label to describe the state currently shown (e.g. "показывать офлайновых" instead of "показывать только онлайн"), so the pressed state visually matches what's on screen.
- «Нет универсальных законов» — judge each button's semantics individually rather than applying one toggle convention everywhere.
- On a state-indicating button, the icon itself must not change on press, or it becomes ambiguous whether it shows the current state or the future command ("state vs. command" collision) — reformulate the function so the pressed state matches the current state (e.g. "currently muted," not "will mute").
- A word/text status is often more reliable than an icon when no unambiguous icon exists — write "Stop" next to a running timer instead of gambling on a play/pause glyph.
- Resolve icon-level ambiguity (a lock icon, an eye icon for password visibility) by switching pattern — toggle, color-coding, two distinct icons — rather than debating one icon's "correct" reading.
- A password-visibility icon should reflect the current state (open eye = visible), not the action a click will perform.
- Where password managers reliably autofill a field, a manual show/hide toggle may simply be unneeded — check whether the threat the masking defends against still exists in practice before keeping the control.
- Changing a UI element just because the technology *can* change it (an on-screen keyboard's letter case shifting per Shift state) isn't automatically an improvement — apply dynamization only where it carries real functional benefit; a user who already knows lowercase letters by shape gains nothing from watching the glyphs literally change case.
- Swapping a working mechanical control for a touchscreen equivalent needs its own functional justification — «Технологии сами по себе бесполезны, они должны решать задачи» (technology isn't valuable by itself — it has to solve a problem); tactile feedback matters most where the result of an action isn't immediately visible, and is dispensable for a simple, instantly-visible toggle.

### Анимация
- Interface animation should work «скромно, быстро, почти незаметно» (modestly, quickly, almost invisibly) — subtle functional motion (focus moving between form fields) works; showy "wow" animation tires within a day.
- Animation is only justified when it is physically plausible or informative — inertial scrolling and rubber-band bounce work because they stay synchronized with the user's gesture in real time.
- Artificial slowdown for animation's sake (a link's hover-color transition dragged out longer than needed) reads as a slow interface, not a polished one.
- Good animation gives feedback and clarifies what's happening (loading, list-end, an object's position); use it for state signals only if the motion is flawless and never blocks input.
- If an animated effect can't be brought to perfection (stutters, lag), remove it — a broken animation is worse than no animation.
- Over-animating a UI reads as slow and intrusive: «делает интерфейс слишком медлительным и назойливым».

---

## 3. Элементы управления (Controls)

### Синтаксис элементов интерфейса
- «Интерфейс — язык, у которого есть синтаксис. Нарушение синтаксиса мешает однозначному пониманию интерфейса» — check labels the way you'd check grammar: verb aspect, case, mood.
- A mismatch (e.g. imperative "Вернитесь" instead of infinitive "Вернуться" on a button) creates ambiguity even when the surface meaning seems clear.
- **Форма = предложение**: the form's title is the **subject** (nominative-case noun: "Жалоба"), the submit button is the **predicate** (verb, base form: "Отправить").
- «Интерфейс находится в „пассивной позиции" по отношению к пользователю: интерфейс ждёт команд, а не командует пользователем» — like "Чай готов," not a command issued at the user.
- The filled-in form should read back as one coherent sentence — designing a form's syntax is a form of editing.
- Elements within one group must share the same syntactic role. Working example: "Отображать участников: компактно, с фотографиями, подробной таблицей" — every option answers "как?" (how), so the parallelism holds.
- Mixing different grammatical roles within one group (some options as nouns, some as adjectives) causes confusion even when each option is individually clear.

### Кнопки: три функции, три синтаксиса
- **Command button** = a perfective verb in base/infinitive form, answering "Что сделать?": «Отправить, Купить, Добавить, Настроить».
- A bare noun ("Новый документ") is worse than an explicit verb ("Создать документ") — the verb removes ambiguity.
- A verbal adjective ("Сохранять автоматически") reads as a checkbox label, not a command button.
- **Navigation button** (leads to an object/screen, not a command) = a noun in the nominative, answering "Что?": «Поиск, Настройка, Недавние документы».
- Don't prefix a navigation label with "Перейти к…"/"Открыть…" if the bare noun already suffices.
- Adverbs ("Дополнительно", "Ещё…") are the worst option for a navigation button label.
- **Status button** (not a command) = a nominal predicate — noun/adjective/participle/adverb, answering "Что это?": «Это спам», «Важное», «Готово», «5».
- A status label is more informative than a redundant command phrasing of the same fact.
- «Новый» reads as an implicit verb only in strongly conventionalized contexts — rely on that only when the object is clearly "duplicable" to the user.
- In ambiguous contexts (a bank: "Новый счёт"), an explicit verb reads more confidently: "Открыть счёт" beats "Новый счёт"; "Добавить пользователя" beats "Новый пользователь."
- A link, unlike a button, only ever navigates and only ever names the destination: «При переходе по ссылке открывается страница, о которой идёт речь в тексте ссылки».
- Meaningless links ("здесь", "подробнее") and command-phrased links ("Сохранить") are syntax errors — a command needs a button, not a link.
- A link's unique property versus any other navigation control is that it's tied to a real address: it can be copied, forwarded, or opened in a new tab.
- An in-app navigation control (tab, icon-button) lacking that URL-level behavior isn't really a link and shouldn't be styled to imply it is.
- **Ellipsis on a button is a warning, not decoration**: it signals the click won't act immediately — more input/clarification is needed ("Сохранить как…", "Подключиться к серверу…").
- On a navigation button that's already a bare noun (e.g. "Настройка"), the ellipsis is redundant and falsely implies a dialog will open.
- No fixed platform standard governs the ellipsis (Apple HIG doesn't define it precisely; Google dropped it on the web; Figma kept it) — but it remains functionally important before destructive/semi-destructive actions, as a warning ahead of an irreversible operation.
- Ellipsis never belongs in placeholder text — it doesn't fit the "instant action vs. needs more input" meaning it carries on buttons, and placeholders aren't buttons.
- **Placeholder text is a noun answering "what?"**, not an instruction — write "Эл. почта," not "Введите ваш email."
- If you're going to render bevels/gleams on a control at all, they must correspond to a real, consistent light source and material — an ungrounded highlight is worse than a flat control, and a dated skeuomorphic style can't be rescued by fixing individual details once its core visual language is obsolete.
- A clear, action-specific CTA label ("Add walls") beats a generic one ("Click," "Continue") — name the actual next action, not the gesture required to trigger it.
- Icons follow the same discipline as navigation buttons: name the icon simply, as a noun answering "What?", with no implied verb.
- Duplicate button-name signage on a physical control panel (name printed on the button itself, plus a separate adjacent label) and inconsistent icon-vs-text styling across sibling buttons within one panel are inconsistency red flags worth calling out directly.
- Before hunting for an icon at all, ask whether an icon is even the right move — sometimes restructuring the interface (show the full table) removes the need for the icon-as-crutch entirely.

### Формы — общие принципы
- A form is always an obstacle. If it can't be removed, minimize friction — and don't assume "nothing left to remove" means the form is good; check layout, button labels, and non-editable filler fields too.
- Careful layout alone can halve a form's perceived complexity, with zero fields removed.
- Grouping is the primary tool of order: merge adjacent fields tightly (a shared border instead of triple lines) when it reduces visual noise — deliberate, not sloppy (Excel does this).
- Automate instead of manually toggling wherever the value is computable from data already entered (retail/wholesale pricing from quantity) — a manual toggle the user forgets to flip feels like betrayal.
- A dropdown is not always the best control for 2–3 mutually exclusive options — radio buttons/segmented controls are faster because the choice is visible without an extra open-click.
- Opening a dropdown just to see the options, then clicking again to pick, is a "double loss" of efficiency versus a control whose options are always visible.
- Autofill a default value only when the guess is almost always right (country by geolocation); when the value space is unpredictable (car make, fruit variety) leave the field empty like an ordinary input.
- "Either field, or one of two" ambiguity should be resolved in the copy itself, not a workaround label: "Эл. почта или телефон для связи" (need exactly one) versus "Эл. почта / Телефон / Мы свяжемся, чтобы уточнить время доставки" (need any, with the reason stated).
- Use Russian abbreviations, not anglicisms, in a Russian-language interface: "эл. почта," not "email."
- Registration-form checklist: question whether the step is needed at all — «по моему опыту она не нужна почти никогда».
- Don't repeat the same word three times ("регистрация... регистрация... регистрация").
- Don't apologize in copy ("это просто" — it's easy).
- Don't lead with a dead technology (OpenID) as the first login option.
- No smileys in form copy.
- Don't substitute a field's label with the text of its error message.
- The primary button sits left-aligned in a form, not right, per this checklist's convention.
- Keep register/tone consistent throughout a form once chosen (capitalized "Вы" isn't a universal rule, but be consistent).
- Order-form simplification sequence, applied in order: (1) clean layout halves complexity immediately; (2) strip excess text/labels; (3) rename and logically group toggles; (4) hide irrelevant options when one choice predetermines another (don't show a payment-method choice if delivery already fixes it); (5) explain why email/phone are requested; (6) finally ask «А может, эта форма и вообще не нужна?»
- Dynamic show/hide fields need no special marker beyond distance-based grouping to show the relationship between trigger and revealed fields.
- Changes triggered by a form field must only ever affect fields **below** the trigger — never let a lower action insert fields into the middle of the form.
- Animating a dynamic field's appearance is desirable for clarity but not mandatory.
- No universal standard exists for Enter vs. Ctrl+Enter submit behavior — make the field's shape self-evident instead.
- A field that submits on Enter should stay visually single-line even with overflowing text (like `input type="text"`).
- A field where Enter inserts a newline should render at least two lines tall from the start, so its multi-line nature is visible before typing.
- A colon after a form label is redundant when the label-control link is obvious, the way a nameplate over an office door needs no further caption — omit it in a dense multi-field form.
- Keep the colon only where that link feels weak — e.g. a single standalone input rather than one of many fields in a form.
- Group ~10 flat fields into ~3 logical groups to reduce perceived complexity — grouping, not raw field count, controls how "big" a form feels.
- The last thing worth doing to compress a form is packing several fields onto one row — sequence the effort: first cut fields, then move labels to the left of inputs, then compact the overall composition, only then consider a shared row.
- A required action (what the user actually came to say) belongs first in the form — «человеку свойственно забывать, что он хотел сказать» (people tend to forget what they meant to say) if it's buried under secondary fields.
- Start any form review by putting its spacing/indentation in order first — a huge share of perceived "messiness" is just inconsistent margins, fixable before touching content.
- Push optional contact fields to the end of a form — the task-specific content belongs first, contact details are secondary.
- A placeholder used as the *only* label disappears the moment the user starts typing, taking the field's meaning with it — pair a placeholder with a persistent label for anything the user might need to re-check mid-entry, don't rely on placeholder-only labeling.
- Avoid tabs inside a form on any device — it's unclear whether data entered on a hidden tab will be preserved; commit to one strategy for the whole form, either fully linear or fully step-by-step, not a hybrid.
- For a professional/expert user's tool, their existing habit outranks a newcomer's first impression of clarity — find out what specifically obstructs the professional's workflow and fix only that, rather than redesigning for legibility a novice will never need.
- A required legal/compliance field belongs on the form only if the underlying regulation genuinely demands it — verify the actual requirement before adding friction in its name; pre-fill everything already known, and design as if you're «по одну сторону баррикад» with the user (on the same side of the barricade), not the institution's.
- Don't route all product access through an unconfirmed-email gate — issue a working session/cookie immediately, and restrict only the specific, genuinely risky actions (e.g. spending money) until confirmation completes.

### Специфические паттерны форм
- Phone-number input: allow free-format entry ("+7 495 646-84-89" or "(495) 6468489"); a leading prefix, not a rigid mask, is what signals the number should be entered in full — parse the format on the backend, not by frontend restriction.
- Address input: field order is a postal convention, not a language question — keep the same field order in translated versions as in the original.
- A building-letter suffix (e.g. "112М") should be capitalized and joined with no space, so it can't be mistaken for another character.
- Combobox (text input + dropdown list) is the right control when the user must both pick from a list and enter a new value on the fly; remember the new value for next time.
- For "select nothing" in a combobox, simple text-clearing is often enough; if an explicit "not required" state is needed, give it its own list item or move it outside the control entirely (e.g. a checkbox).
- If creating a new entity via a combobox is a significant action, ask for explicit confirmation rather than creating it silently on text entry.
- One field that parses several input formats itself (including plain-text alternatives for special characters) beats several separate fields, each demanding one rigid format.
- Flexible parsing needs live feedback: show, as the user types, how the text will be interpreted — otherwise they can't be sure they were understood correctly.
- Remove an unnecessary confirmation step wherever the result can instead be shown immediately and updated live as input changes.
- Date/time selection: a calendar view is preferable when the full range of options should be visible at once and only one click is needed to choose — pair it with a sensible default, labeled weekdays, and weekend highlighting.
- Interlinked numeric fields (loan amount / term) should recompute each other live — editing either field updates the other, instead of a static one-way calculation.
- Collapse completed steps/checks under a link, leaving only the current, unfinished item visible.
- For "sign up" flows that also serve as sign-in, auto-log the user in immediately after registration: «просто залогиньте меня, чтобы я даже не заметил, что ввёл всё не в ту форму».
- Radical alternative to password-based signup: passwordless entry via a one-time link sent to email/phone.
- On any list with a multi-select control, don't auto-select all child items just because the parent container was selected without checking the real scenario first — verify actual intent before wiring bulk selection.
- A search-first, filter-second sequence pays off in booking/matching forms too: show what already exists before demanding the user fully specify a query — people find it easier to refine something visible than to formulate a need from a blank form.
- Before designing a settings control at all, ask whether the setting should exist — prefer removing the need to configure (e.g. push for always-live updates) over polishing a refresh-interval knob nobody should have to think about.
- Replace an ambiguous text status ("Charge: 76% remaining" — remaining, or yet to charge?) with an icon or clearer phrasing only when the new form actually removes the ambiguity, not merely to save space.
- For a small, discrete-choice setting, an explicit control with real named presets (.25s / .5s / 1s / 2s / 5s, "Less often" / "More often") beats a minimal-looking "−/+" text stepper that doesn't read as interactive.
- A column of always-visible per-row action buttons ("батарея") gets visually noisy at scale — «рябит в глазах».
- Hide-on-hover for row actions breaks precision: «то, во что кликает пользователь, изменяется, пока он целится» — never let the hit target shift under a cursor that's still aiming.
- Prefer disabled-but-still-visible row actions, or flyout controls that pop out sideways from a hover zone (hard to trigger by accident), over a hide/reveal "battery" — choice depends on how the list is actually used.
- When two synced media tracks are being compared side by side, don't expose an "unlock sync" toggle if there's never a legitimate reason to view them unsynced — default to always-synced, and hide any independent-scrub complexity behind an explicit, deliberate per-clip trim control instead.
- For time-anchored annotations on a moving timeline (a mark that becomes stale as playback continues), design multiple explicit modes rather than one generic "add annotation": fade-in/out around the marked moment, freeze-frame-while-annotating, or drag-with-the-timeline for markers that must track motion — pick per case instead of forcing one mechanism to do everything.
- A "draw a line to match pairs" interaction doesn't require literal line-drawing — sequential tap-to-pair (dims on match) or letting the user re-sort a second list to align with the first are lighter alternatives; choose based on whether the user must commit every match before checking, or can check incrementally.
- If matching lines must be drawn, curve them so crossings don't obscure legibility, rather than using straight lines that stack on top of each other visually.
- Don't assume mobile forces single-column layout by default — two columns can still work on narrow screens with wrapping, as many marketplace apps demonstrate with two items per row.

### Чекбоксы и радиокнопки
- Checkbox syntax: avoid negative/concessive phrasing ("не печатать", "скрывать", "несмотря на") — use direct positive phrasing with an appropriate default state instead.
- Never label a checkbox "да"/"вкл." — it breaks checkbox syntax and carries zero information on its own, since the meaning lives entirely in external text.
- Use a checkbox only when the off-state's meaning is self-evident (on/off, shown/hidden).
- If the off-state is ambiguous, use radio buttons/segmented control/dropdown with explicitly named options instead — don't use a lone "включить сейчас" checkbox when the real choice is "сейчас" vs. "позже."
- Make the entire label clickable, not just the glyph (Fitts's law) — never put a link inside checkbox/radio label text, since it breaks the click target.
- Parent/child checkbox trees need a third **indeterminate** state (dot/dash) when only some children are checked.
- Restore prior child states when cycling back through the indeterminate state — don't lose data across toggles.
- Radio labels must be syntactically parallel coordinate clauses.
- Never use "да"/"нет"/"вкл."/"выкл." as radio option text — use a checkbox instead if the choice really is binary.
- Radio buttons in one group must stack **vertically**, never in a row — horizontal placement separates each control from its own label and breaks the proximity cue.
- Use segmented controls or a dropdown instead of radios for a genuinely single-row layout.
- Default rule: put the recommended option first, unless the options form a natural sequence (size: small/medium/large) — then preserve the sequence order and default-select the recommended option wherever it falls.
- When no default is safe or desirable (a survey, a test, a gender field where defaulting violates neutrality), don't leave the group unselected — add an explicit degenerate option ("не указан" / "без ответа") and default to that.
- For exactly two options with a required choice, prefer radio buttons over checkboxes — checkboxes don't visually communicate that a choice is mandatory.
- For more than two options, checkboxes are fine.
- Never disable the last remaining checked checkbox in a group — auto-select a different option instead when the user tries to uncheck the last one.
- When two multi-select filter states ("nothing selected" and "everything selected") end up meaning the same practical thing, that collapse is fine for options that are mutually exclusive by nature at point of use.
- When filter options are genuinely independent (each freely on/off), the empty state is ambiguous between "don't care" and "must not have this" — design a real three-way control (want / don't want / don't care), don't reuse the two-state collapse.
- Switch/toggle vs. checkbox: syntactically equivalent, but semantically a toggle usually implies a heavier, possibly asynchronous consequence.
- Choose by weight of consequence: an instant, visible side effect (Wi-Fi toggle) → switch; a more serious system action → a full button, not a toggle or checkbox.
- Never put "Включить" (Turn on) next to a toggle switch — the control already implies on/off.
- Use the object's name alone ("Комментарии") or an imperfective verb describing ongoing behavior ("Загружать изображения") next to a toggle, not a perfective command verb.

### Выпадающие меню и переключатели
- Segmented control is syntactically and behaviorally identical to a radio group — same rules apply.
- Prefer a segmented control over stacked radios when the options fit compactly in one row; move detail text to a caption below to gain room.
- With only two options in a segmented control, the selected state must be unambiguous — never let both segments look "selected, just differently."
- Instant-action segmented controls must not react to hover.
- Instant-action segmented controls must never reorder their options on selection — reordering breaks honest feedback.
- Grouping options inside one shared container visually signals mutual exclusivity — don't separate them visually even if the meaning is technically inferable from context.
- Dropdown rule: never use it for navigation, where selecting an item jumps to a different page/screen.
- The open dropdown list must be at least as wide as the closed field — may be wider, never narrower.
- Required dropdown keyboard support: arrow-key cycling, type-ahead search, Escape to close.
- Don't flip the dropdown arrow's direction on open to "hint" it will close — it draws unwanted attention, and with several adjacent dropdowns the arrows visually "point at each other."
- An empty/unset dropdown state is valid (a blank default option), but never fill the blank placeholder with an instruction like "Выберите страну" — treat it as an ordinary unfilled field.
- "Дропдаун — лучше всего никогда" on marketing/content sites: no consistent visual standard, conflicts with click behavior, and fails on touch — avoid where a simpler pattern will do.
- Tabs vs. radio buttons can look identical but differ in function, not appearance: a tab switches a *screen region's content*; a radio group switches a *value*.
- Classify a control by its semantic role, not by its rendering style — visual similarity across platforms is coincidental fashion; meaning stays constant.

### Ссылки
- A link names the object it leads to — never leave a link's destination unstated ("здесь", "подробнее").
- Underline links by convention; don't underline trailing punctuation that isn't part of the link text.
- Underlining is the convention that survives without hover — «Даже на десктопе полагаться на один только ховер — дурной тон. Интерфейс должен быть понятен на вид.»
- Hover color-change is useful *confirmation* feedback before a click, but it is not sufficient on its own and doesn't reach touch devices at all.
- Open a link in a new window/tab only when: the user explicitly asked (⌘/⇧-click), the user configured it that way, adjacent text explicitly says it opens in a new window, or the source page is a persistently-open web app.
- «Ссылка не должна открываться в новом окне просто потому, что вам жалко отпускать пользователя.»
- Visited-link styling applies by default; drop it only where it's clearly unhelpful (a single "читайте далее" link, or a frequently-revisited main menu).
- Whatever visited-link rule you choose must be applied uniformly within one row of links, never mixed.
- A "fake" link styled and behaving as a button is not a defect — what matters to the user is the syntax matching the function, not the underlying markup.
- Prefer a link over a button for a lightweight, low-consequence action like logout: «кнопка — весьма тяжеловесный элемент» (a button is a fairly heavyweight element).

---

## 4. Навигация и структура (Navigation & structure)

### Меню
- Unavailable/disabled menu items should be shown pale/grayed but kept in their usual position — removing them breaks positional habit/muscle memory even though they're temporarily irrelevant. Applies to any menu, not just desktop app menus.
- Context-menu placement: anchor the top-left corner to the source object (for LTR writing), falling back to bottom-left/top-right/bottom-right when space runs out.
- Proximity of a context menu to its source both signals relatedness and shortens Fitts's-law travel distance.
- Site-nav menu has three states, not two: the **current page's** item should look *more* prominent, not pale/disabled, and stay clickable.
- Styling the current-page item as disabled is an explicit error — it's selected, not unavailable.
- A **parent-section** item (in-section, but not on the section's own landing page) should look both selected and remain clickable, leading to that section's main page.
- Never put "Главная" (Home) as a menu item — the logo already performs that function.
- There is nothing "obligatory" about a menu's contents beyond real informativeness — replace generic "Товары"/"Услуги" with the actual concrete list of what's offered.
- Simply mirroring the main menu in the footer is a cheap retention gesture — offering topic-relevant material or an explicit call to action there is more useful.
- «Правило семи элементов» (Miller's magic number) is commonly misapplied to justify hiding menu items behind "Дополнительно" — the actual fix for an overloaded menu is grouping by meaning and revisiting real scenarios, not concealment.
- Counting hidden menu items ("+5 more") is low-value — showing the items themselves (even abbreviated) beats a bare count: «Сокращённые названия на виду в любом случае информативнее полных, но спрятанных.»

### Хлебные крошки, поиск, ошибки, редиректы
- Breadcrumbs frequently duplicate the main menu — check for redundancy before shipping them.
- Navigation should answer the user's scenarios, not mirror the underlying data structure — a filesystem tree is not the only way to find things in it.
- Offer several parallel paths (search, back/forward, breadcrumbs, tags) rather than forcing a single hierarchy.
- A 404/dead-end screen is effectively an error message: it should help solve the problem (offer search, similar items), not just state it.
- **Never auto-redirect a 404 to the homepage.**
- A distinct error-page treatment reassures the user they haven't broken something, rather than blending in as if nothing went wrong.
- A "На главную" (Home) fallback button is fine while normally browsing (e.g. an empty folder) — content shouldn't dictate unrelated navigation options in that case.
- If the user followed a now-dead link, a good error screen offers search or similar items, not just a passive way out.
- The HTTP 404 status itself is «единственный способ передать мысль „страница не найдена" в трёх символах» (the only way to convey "page not found" in three characters) — preserve the real status code even while designing a friendlier page around it.
- QR codes are, in Birman's assessment, an evolutionary dead end for wayfinding — don't build a navigation system that assumes every visitor is willing and able to scan one with a personal smartphone in the moment.
- A canonical URL should exist for every page; redirect the non-canonical variant to it (trailing slash or not — pick one and stick to it site-wide).
- Never make the user remember or guess the site's own address format.
- On genuine intent, use a 301 redirect, never a 302; when the target is ambiguous, show a disambiguation page instead of guessing.
- Only drop an explicit "search" button if search-as-you-type is active *and visually obvious*; otherwise keep an explicit control — a compact "↵" glyph can hint at Enter while staying clickable, as a middle ground.
- Don't hide a search field behind an icon — show it directly on the page rather than gating it behind a click.

### Sticky, пагинация, wizard, фильтры
- «Как правило, залипающие меню использовать не стоит» — the main exception is long documents, where a shrunk sticky header (reduced from its full height) helps.
- Mechanical equal-division pagination is weak: page "7" is meaningless out of context, and numbering "sprawls" as new records are added.
- Pagination must match the current sort order — paginate by date if sorted by date.
- Pagination can often be removed entirely in favor of infinite scroll.
- Prefer "Ранее"/"Позднее" over raw page numbers, or better, replace the count with real information ("Нашлось 2700 вафельниц" instead of a page index).
- On very large tables, separate the two real user tasks — **поиск** (find one specific value) and **сравнение** (compare several values side by side) — and solve each with a dedicated tool rather than a universal paginator.
- A pragmatic compromise without a full rebuild: fixed pages of ~100 rows, or infinite scroll.
- A page-jump/pagination control that trades literal clarity for a bigger Fitts's-law target (fewer, larger click zones) can be a deliberate, defensible compromise if the control is barely used anyway.
- Wizards: one question, or one tightly related field set, per step.
- Provide a navigator showing total step count/names and current position.
- Never lose data entered on other steps when the user goes back.
- Desktop: Back/Next are equal-weight; mobile: Next is primary, Back secondary.
- Wizards suit high-volume routine intake but constrain freedom — avoid them in professional/power-user interfaces.
- Filters are needed when the user has clear criteria and the catalog is huge — «когда на сайте тысячи вариантов, показывать их сплошным списком бессмысленно».
- Filters are harmful when the product's value is serendipitous browsing — a hard filter can shrink results to five irrelevant items and hide the finds that make browsing worthwhile.
- Decide on filters by actual user/business benefit, not feature fashion; they can be introduced incrementally as a catalog grows.
- «Сначала данные, потом фильтры» is about interaction sequence, not screen position: show *some* answer before the query is fully specified.
- The anti-pattern is forcing a full form before any result appears at all (typical of real-estate/car search sites).
- Filters split into **instant** (applied live, needs an undo/revert path) and **deferred** (an explicit "Show"/"Apply" button) — decide which mode fits the cost of a wrong guess.
- Filters exist to cut a list down sharply, and belong positioned after the data, not before it.
- A filter that defaults to zero visible results actively hurts conversion — default to an inclusive/unfiltered state.
- Never leave a filter state with no visible way back — every active/toggled filter needs a clear affordance to reset it.
- Mutually exclusive numeric bands (e.g. price ranges) shouldn't be offered as independent checkboxes that can be combined into a meaningless selection — use a range control instead.
- Don't ship a filter whose internal logic isn't guessable from experience (a menu that won't close, a click that silently toggles selection off) — «ни опыт, ни логика не помогут пользователю понять, как это работает» if the behavior is unpredictable.

### Прокрутка и листание
- «Прокрутка и удобнее, и универсальнее листания» by default — switch to discrete paging only when content is naturally discrete (cards, articles, photos), where a "page" earns its own identity.
- When paging is used, preserve the scroll gesture and its continuous feedback rather than replacing it with a dead, feedback-free jump.
- Keep position stable and shareable (URL/bookmark on a scroll position) wherever feasible — useful in both scroll and paged modes.
- For effectively-infinite or dynamically-loading documents (long chat history, infinite catalogs), don't model true document length with a literal proportional scrollbar thumb — treat it as explicitly unbounded, the way map apps drop scrollbars entirely in favor of pan/zoom/search.
- For a long-but-bounded history (a chat with a known start), use non-linear (e.g. logarithmic) scroll mapping, so dragging near "now" gives fine control and dragging further back covers more ground per pixel — show tick marks/labels as soon as dragging starts, and shrink the thumb toward the sparse end to signal reduced precision.
- When new content loads and shifts total length mid-scroll, recompute scroll math so the currently-viewed point stays anchored to the same document position — don't recompute as a fresh proportion each time, which causes visible jumps.
- Scrollbar informativeness can go well beyond a bare thumb: highlight risky/found fragments directly on the track, pop up a page-number readout while dragging, swap the proportional scale for an alphabet strip where proportionality doesn't matter, or show a thumbnail "infoscroller" of the whole document (headings/images visible in miniature).
- Pull-to-refresh and other nonstandard scroll gestures live or die on continuous feedback — intercepting the scroll gesture and replacing it with discrete paging that drops feedback is «страшное преступление» (a grave sin) against physicality.
- Time-zone handling belongs in the system, not the UI: the browser knows the user's zone, the server stores UTC and converts through a DST-transition table — don't invent an interface trick to route around this. Where relevant, show the explicit equivalent time at the other party's location, named by city, with a warning if a DST change is imminent.

### Физическая навигация и таблички (wayfinding & signage)
- Wayfinding signage needs at minimum: current location shown, transfer/route options labeled, and direction arrows that map to actual physical orientation — a wrong-pointing arrow is worse than none.
- Test signage design in its real installation location — «Такой дизайн вообще нельзя обсуждать на сферическом макете в вакууме» (this kind of design can't be discussed on an abstract mockup in a vacuum).
- On a pedestrian call-button light, put the indication that a button exists where the person is already looking (in the light itself), not only on a separate remote sign.
- Prefer subway/hallway signs that state the destination in words directly over number+legend systems — the reader shouldn't have to memorize a number and cross-reference a key.
- Reserve number+legend schemes for genuinely constrained space/typesetting; treat it as a compromise, not a default.
- Room/locker numbering should leave gaps at group boundaries (e.g. 11,12,13; 21,22,23,24) so future additions append cleanly without renumbering everything else.
- When numbering rooms around a loop corridor, choose the direction so that, walking with a target number in mind, the numbers approach consistently rather than requiring backtracking.
- Keep numbering continuous within one corridor loop; don't restart or skip arbitrarily.
- A purely decorative/gamified label must not replace a functional identifier (a locker number) — layer personality on top of the working system, don't substitute it.
- Signage/wayfinding text works on three layered levels, in this order: **ясность** (clarity), **вежливость** (politeness), **юмор** (humor) — reversing the order (joke first, safety instruction last) buries the message and can read as mockery, especially in safety-relevant signage.
- Subway/floor indicators: give the current facility's directory real content (which departments/floors are where), not just a bare number list.
- Uneven line spacing within one wayfinding label versus between adjacent labels defeats the proximity grouping the label needs to read correctly — space within a label tighter than space between labels.
- Podium/directory materials and mounting shouldn't be cheapened at the cost of durability or correct height (avoid a low overhang that people can hit their heads on).
- Suspended/overhead signs are more visible along a walking path (optimal height ~3m); wall-mounted signs suit decision points — forks, dead ends, elevator lobbies — since a wall sign along a straight path is easy to miss.
- On a floor/wall with existing numbered doors, don't remove an old, functioning number plate just for uniformity when a new one is added — coexistence often looks better than the scars left by removal.
- A numbering/way-finding scheme should be designed to survive future change (units added, removed, split, merged) by leaving numbering slack, not by a rigid, exhaustive sequence.
- Give every "impossible to reach without navigation" area an alternative: search, a staffed help point, or a phone-based fallback, since no purely graphic system covers every real edge case.
- Sensitive/legally-required content (privacy blur, restricted-area masking) doesn't have to look ugly to satisfy the constraint — a treatment that doesn't visually draw extra attention to what's hidden beats an obvious blur.

---

## 5. Законы восприятия (Perception laws)

### Закон Фиттса
- «Чем дальше объект, тем больше время прицеливания; чем больше объект, тем меньше время прицеливания» — the relationship is logarithmic, so past a point, enlarging an element further barely helps.
- Enlarge the **hit area**, not just the visual element — a menu item is clickable across its full row; a checkbox's entire label is clickable, not just the glyph.
- Separate "mutually dangerous" adjacent controls (destructive next to routine) physically, to cut accidental clicks.
- Give visual feedback (highlight) before a click actually registers, to aid aiming — «обратная связь помогает прицеливанию».
- The fastest possible target is the point already under the cursor (a Windows context menu's first item appears right there).
- Screen **corners** have near-infinite effective size — put frequent actions there (hot corners).
- Screen **edges** are infinite along one axis — use them for pinned toolbars/menus flush to the edge.
- «Человек не меняет принятое решение о клике по пути» — don't let hover-triggered elements appear and obscure a target the cursor is already travelling toward.
- A submenu shouldn't close early just because the cursor's path moves diagonally across it en route to a deeper item.
- When different clicks on parts of one perceived object should mean different things, the interface becomes hard to use — treat a perceived single unit as one uninterrupted, hole-free click target.
- No gap should exist between lines of a multi-line link, or between an image and its caption, when both are meant to be one clickable object.
- Small width differences between adjacent buttons read as sloppy ("не подружились" — they don't get along) — align widths, or make the difference large enough to read as intentional.
- On mobile, place frequent, useful actions within comfortable thumb reach; reserve the top of the screen for rare/administrative actions ("Назад," "Done") — this needs no formal study, just common sense plus Fitts's law.
- Prefer controls that let the user modulate a continuous *rate* (like a steering wheel) over ones that only set a target state, wherever precision over time matters more than a single endpoint.

### Теория близости
- «Объекты, расположенные рядом, кажутся нам связанными» — proximity outranks almost every other visual cue, including arrows.
- If an element ends up closer to the wrong neighbor by accident, fix it by increasing distance and deliberately breaking alignment — severing the false link, not adding an explanatory label.
- Group semantically related fields close together in forms (first+last name, card number+expiry) rather than spacing everything evenly regardless of relationship.
- Keep "зоны безопасности" (safety margins) around lines/objects on schematics free of unrelated labels — labels crossing into a "foreign" zone are a leading cause of misreading.
- If a label must cross a foreign line, pull the start of the word out of that line's safety zone to reduce interference during fast scanning.
- Diagram/chart elements read better when placed closer together — proximity aids comprehension even in pure data visualization, not just navigation.

### Оптическое выравнивание
- Metric (pixel-exact) alignment isn't the same as *felt* alignment — check optical balance separately from measured symmetry.
- Reading direction (left-to-right) makes left-side margins register more strongly than right-side ones of the same measured size.
- Anything vertically centered against surrounding elements typically needs a slight upward nudge to *read* as centered (this applies to button-label optics specifically).
- Apply the same optical-correction policy across every button in a set, not ad hoc per instance.
- Center alignment on data/label columns is a decorative flourish, not a default — left-align (or right-align by digit rank for numbers) whenever the column supports scanning or comparison.
- Center only when a single item clearly outranks the rest in importance.
- A standard hyphen is calibrated for lowercase letters and old-style figures — with lining/tabular digits it often needs manual vertical repositioning, or a minus sign should replace it for clearer digit-group segmentation.

### Аффорданс
- Uniform flatness kills affordance — if every element looks the same, users can't tell what's tappable.
- Teach a non-obvious interaction on the element itself, in the moment ("Slide to unlock"), with a hint animation that disappears once the real gesture starts.
- Three ways to signal clickability, by reliability: (1) interface habit/convention (button shape, blue+underline+pointer cursor for links); (2) skeuomorphism — borrowed expectations from the physical world; (3) an explicit text instruction for a genuinely unfamiliar control.
- Skeuomorphic detail earns its place only when it carries real function (raised bumps on F/J keys aid touch-typing home-row orientation) — decorative realism without function is a liability.
- A physical door's opening direction should be encoded in the hardware itself (handle vs. flat plate), not a printed "push"/"pull" label — the same logic favors a shape/behavior that makes a digital affordance self-evident over an instructional label bolted on top.
- A cropped or overflowing element can intentionally *signal* more content exists (a title running off-screen as a scroll cue) — but only when it's a deliberate design decision, not an accidental layout bug.
- Watch for semantic collisions when reusing a generic system-dialog convention (e.g. confirm = green, cancel = red) on an action whose real-world meaning calls for the opposite mapping (a destructive "Delete" shouldn't inherit a reassuring green) — check the action's actual stakes before applying a color convention by reflex.
- A legally-mandated but low-priority text block (fine print, credits) can be deliberately set dense and visually "textured" rather than inviting — this satisfies the requirement to display it without competing for attention the content doesn't need.

---

## 6. Таблицы, списки, схемы и графики (Tables, lists, diagrams, transit-scheme notation)

### Таблицы
- «Бирман поменял подлежащие со сказуемым местами, и таблица сократилась в два раза» — swapping what's compared for how it's compared (rows ↔ columns) can shrink a table dramatically without losing data.
- Classic case: put room-count on the horizontal axis, not vertical, so price-per-m² is comparable both by room count and by district at once.
- No table without comparison: if the data isn't actually compared along a shared axis, it belongs in plain connected text, not a table.
- Factor the general case into the header/caption instead of repeating it in every row (don't write "замена" in every cell — make it the column head).
- Always align numbers by digit place (right-align integers, align on the decimal point/comma) — never left/ragged.
- Normalize decimal precision across a compared column (e.g. "16" → "16,0") so differing precision doesn't create a false visual impression of magnitude.
- Explicit units belong in the header, not repeated per cell.
- A monospace/tabular figure style helps comparison and typo-checking — reserve monospace for fields prone to typos (account numbers, phone numbers), not for aesthetics broadly.
- «Хорошо свёрстанная таблица занимает минимальную возможную для себя ширину» — don't stretch a table wider than its data needs.
- A forced full-bleed table creates gaps between columns that make rows harder to track — stretching for surrounding-layout consistency is a conscious trade, not a default.
- Kill ruling lines and zebra-striping by default: «Добавление любого графического элемента приводит к возникновению элементов, которых вы не рисовали» (any added graphic element creates elements you didn't intend to draw).
- If a table looks like it "falls apart" without zebra-striping, the fix is better layout, not a decorative crutch.
- One rule between header and first row is usually enough to read a table as a whole; question the need for any further rules or bands.
- Align cell content to the top-left, not centered — top-alignment specifically matters when rows have uneven content height.
- Split a long table into two when it genuinely helps legibility, but check whether the actual problem is typographic/structural before restructuring.
- Transposing (long text per row → dense single column per object) often solves what looks like a "too wide" table problem.
- A table mixing fundamentally different data types in one column (user-counts among dollar amounts) signals a need to reorganize by meaning, not just reformat.
- Different orders of magnitude coexisting in one column is normal, not a defect — the resulting digit-shape difference actually speeds visual comparison.
- Remove meaningless whitespace and repeated per-row units; align by digit rank instead.
- Dynamic (on-screen, interactive) and print versions of the same table serve different jobs — they aren't obligated to share the same structure.
- Bold table headers signal "what is this?" even when the content itself carries more meaning — skip the emphasis when the data is self-evident without a header.
- A running-balance/ledger table should read as a transaction log (concrete dates, operations, running balance), the way most financial institutions present it — not an opaque single running number.
- Don't economize screen space in a way that removes plain-language explanations of individual charges or adjustments in a billing table.
- Follow the local decimal/thousands convention (Russian: comma for decimal separator) rather than an institutional standard that contradicts it.
- Always begin a table or calendar-style layout by asking whether you can avoid borders and separator lines entirely — start from the variant that needs none, then add rules only where genuinely necessary for legibility.
- Don't collapse or hide empty periods/rows in a schedule-style table just to look tidier — the gap itself may be meaningful information (nothing scheduled), and hiding it can mislead.
- Match a data-table's format to its actual audience's fluency, not to an abstract "best practice" — a spreadsheet-literate internal audience tolerates density a public-facing table shouldn't.
- In a financial/ledger table, center the single most important figure and align the surrounding text to its outer edge — this reads as both more legible and more orderly than uniform left- or right-alignment (proximity theory applied to a summary row).
- A "деструктивная разметка" test for a diagram/table legend: either name every element directly, or explain every abbreviation — never leave the reader guessing which elements were considered self-explanatory and which weren't.

### Списки
- Colored-row highlighting conventionally means "current/focused item," not "selected" — don't overload the same visual signal for both.
- When both selection and focus states are needed: checkboxes for selection (explicit, self-documenting), background color reserved for the focused row.
- Don't bind a separate double-click action to rows that also support single-click selection — the ambiguity between "select" and "activate" causes accidental triggers.
- List punctuation depends on the list's role: as running text (short items, no internal punctuation), use ordinary comma-based punctuation; as a standalone design element (poster, catalog), punctuation can be replaced by layout, color, type, or rules.
- An undifferentiated long flat list "will look like a mass grave no matter how you style it" — carve out thematic slices (popular, editor's pick, new) instead of decorating one continuous list.
- Sort order and display order don't have to match: sorting by surname while displaying "first last" is fine — pair it with in-page search so visual "non-alphabetical" scanning isn't the only way to find an entry.
- Don't overload a list item with more metadata than content — a comment row with more badges/ratings than actual text «выглядит удивительно громоздко и неопрятно» (looks strangely bulky and untidy).
- Never hide part of a list silently — if only 5 of 15 comments are shown, say so explicitly, or the user assumes they're seeing everything.
- An in-list "report/flag" action should be a button, not a text link — it's a command, not a navigation destination.
- If a form already separates labels and values into distinct columns, that layout alone already provides visual distinction — additional font-weight or contrast tricks to highlight "what the user entered" are purely stylistic, not functionally necessary.

### Иконки и пиктограммы
- For near-duplicate actions, base similar icons on unrelated associations (payment cadence: calendar vs. a stack of cash) rather than literal variations of the same object, and strip elements the surrounding context already implies.
- Good interface pictograms don't try to depict the object literally — recognition comes from position, color, and shape more than literal resemblance.
- Develop a pictogram set together, in-context, not individually on a blank canvas — the "squint test": you should still find the right button with eyes half-closed.
- Icons within one set need shared visual DNA while remaining distinguishable — they should "get along," not compete.
- For abstract referents with no natural visual association (cement, gypsum), a pictogram is often simply impossible — words alone may be the only honest solution.
- Combining meaning from primitive icon components by a "language of icons" risks becoming a rebus — a puzzle to solve, not a shortcut to recognition.
- A universal, unambiguous pictogram is rare — history shows even seemingly obvious referents (an elevator) resist good iconification; draw the *scenario* rather than the object, or fall back to a word.
- Keep an icon's core, recognizable shell fixed even when part of its content updates live (a clock/calendar icon showing real time/date) — full-content variability destroys the recognizability habit depends on.
- A telephone number is better shown as text than as a phone icon on mobile — an icon can go unnoticed while scanning for contact info, even if most users would eventually guess its meaning.
- Test a claim like "people don't tap on text" empirically rather than by intuition — «Статистики нет. Соберите сами» (there's no data — go collect it yourself).

### Транспортные схемы (notation doctrine)
- **Графема**: the overall shape recognizable before any label or individual line is read — a strong graphema (a ring, a distinctive silhouette) lets people recognize a scheme even without color or a grid.
- Where no natural landmark exists, the designer must add one (ring lines, parks, monuments) — avoid accidental "parasitic" shapes emerging by coincidence.
- Find an appealing overall image before polishing detail — detail work done before the form is fixed is wasted effort.
- Where a scheme "resists" the format (long station names, awkward stretches), compactness of form outranks literal fidelity to every name.
- Angle systems — pick deliberately from: 45° (classic, most predictable), other fixed-angle multiples (18°, 30°), free-curve/geographic, or quasi-geographic (distorted for the format but still recognizable) — and commit to one system throughout.
- Mixing straight and arbitrarily-curved segments on the same scheme reads as inconsistency, not style.
- A uniform grid of only-vertical/only-horizontal crossings gives the eye nothing to "grab onto" — a unique curve shape per line becomes its own orientation landmark.
- Z-order at intersections: a turning/curving line should render **above** a straight one — the bend needs visibility more than the straight run does.
- After re-sorting lines at a junction, no "holes" should remain in the bundle.
- All branches leaving a shared bundle should exit from one side of it, not the middle, to avoid leaving holes after separation.
- **Interchange stations**: use one circle per line converging there, not a single fused circle, when platforms/transfers must be individually labeled — a diamond ("ромбиком") layout resolves this when several platforms need distinct labels.
- A double/fused circle "hinders reading" — one station with several lines gets one circle (filled with each line's color in segments), not several glued circles.
- Circles beat "pegs" (пеньки) for interchanges — a peg graphically belongs to one line, but an interchange belongs to several, and circles are symmetric enough to carry multiple lines at any angle.
- For ordinary (non-interchange) stops, small marks/pegs beat circles — quieter, and they point at their own station rather than merely sitting near it.
- A line simply broken (gapped) to mark a stop doesn't work — the eye still perceives the resulting white notch as an object even though nothing was drawn there.
- Color rule, the **"one word" test**: every color in the palette should be nameable by one unambiguous word.
- Avoid black for a line color — it prints poorly and reads oddly on dark backgrounds.
- Always check the palette against colorblindness (protanopia/deuteranopia confuse red/green) via software simulation and real colorblind testers.
- Never color station names by their line's color — «выглядит грязно и недоступно людям с проблемами цветовосприятия» — keep station-name text a neutral color.
- Line thickness is a balance, not a maximum: «чем меньше, тем непрактичнее; чем больше, тем неэлегантнее» — tune it against the whole scheme, never in isolation.
- Match label size to line thickness — thicker lines demand larger type, or the pairing looks miscalibrated.
- When color and thickness alone can't distinguish enough line types, add pattern/hatching (dashed for tram, hatched for planned) — but respect the complexity ceiling: «Чем сложнее система обозначений, тем больше объяснений нужно и тем сложнее пользоваться».
- Don't leave unexplained graphic elements (odd marks on circles, nonstandard colors) — either add a legend entry or remove the element.
- A legend is often a symptom, not a feature — label lines/objects directly at their endpoints wherever there's room: «легенда низачем не нужна», if the information is already integrated into the scheme.
- Fill communicates mass; bare outline doesn't — for floor plans and similar diagrams, restore fills to walls/furniture, and separate functional layers (seating vs. structure) by color.
- Don't fake subscript/superscript numerals by simply shrinking full-size digits — use a font's real subscript glyphs, or switch fonts.
- Test signage/scheme legibility in the worst realistic viewing conditions (bad lighting, glare, faded print) — real systems accept some graphic imperfection in exchange for robustness under those conditions.
- Test a redesigned scheme on an eye-tracker or a cheap proxy for one: mark "safety zones" directly on the layout in your vector tool and visually check that no foreign label enters them.
- The main value of eye-tracking data is finding station/label mismatches — fix specific problem labels point by point rather than redesigning the whole scheme from aggregate heat-map data.
- Don't chase literal eye-tracking-line straightness as a proxy metric — optimize for tidy layout and real conversion/comprehension instead.
- Route-direction ("bullet") arrows must unambiguously encode direction in both plains (with and against travel) — ambiguity here provokes constant clarifying questions.
- When a whole bundle of routes only travels one-directionally past a stop, mark the stop itself as one-directional rather than inventing a special notation per route.
- If borrowing another city's or system's *functional*, lean notation, copy it faithfully rather than half-adopting it — a system's brand-defining signature flourishes, however, should not be copied, or the new scheme reads as an imitation instead of having its own identity.
- A scheme too strongly borrowed from a famous system (London Underground-style) risks "continuing to work for [the original city], not for its own" — don't import a foreign visual brand wholesale.
- A locally distinctive graphic identity matters as much as legibility logic — a transit system's scheme is a visible piece of brand design in a major city, not merely a technical diagram.
- As a minimalism stress-test, try removing elements from a finished scheme one at a time until meaning starts to break — anything removable before that point was decorative, not functional.
- Numbering interchange/exit points: apply a fixed standard for typical stations, and accept bespoke local solutions for atypical ones — one rule doesn't have to cover every case.
- Visual weight on any schematic must match informational significance — a secondary decorative layer (water, background texture) that visually "wins" over the primary content (route lines) is a hierarchy failure, independent of how attractive either layer looks alone.
- Information density across one scheme should stay roughly even — an area that's suspiciously empty relative to the rest reads as a mistake unless it's backed by real content (a park, a river) that explains the gap.
- A single consistent typeface across an entire scheme is a baseline requirement — mixing faces between the title and the line-end labels reads as an unintentional error, not a stylistic choice.

### Редактируемость и рукописный ввод
- A dotted/pecked underline is the established convention for "this value is editable" — reserve it for genuinely editable fields, and don't apply a decorative dotted style anywhere it could be mistaken for that affordance.
- Don't show visibly empty data cells just to preserve a table's rectangular completeness — an empty cell with nothing to say is better omitted or merged than dressed up to look "full."
- On a printed form meant for handwriting, leave dedicated blank space sized for real handwriting, not a font-sized line calibrated for typed text.

### Карты и географические схемы
- Any map is a convention: every projection sacrifices something (lengths, angles, areas, shape) — the acceptable sacrifice depends on scale and task, not on an abstract notion of "accurate."
- Geographic distortion on a wayfinding scheme is acceptable only if the passenger understands and accepts the scheme's own "rules of the game" — if a rider looks for a place they know from the real city and can't find it, the scheme has failed regardless of how elegant it looks.
- A hybrid ("looks geographic but contains all sorts of distortions to make everything fit") is a working compromise — keep recognizable real-world landmarks (rivers, streets, districts) even while simplifying.
- Choose which map layers to show (relief, borders, routes) by the user's actual task in the moment, not by a notion of cartographic completeness.
- For area-filled data on a map (e.g. a choropleth), remember the modifiable-areal-unit problem: encoding an absolute count (5 deaths in a 5-person house vs. 5 in a 50-person house) rather than a rate produces the same color for very different realities.
- Lower the contrast of filled/area map objects (land, water, background regions) as much as possible; raise the contrast of point, line, and text objects — area fills should recede, point/line/text data should pop.
- When a map mixes many inconsistent styles (some labels italic, some boxed, some circled, some bare, some colored, some black), first collapse everything into a small number of deliberate visual "layers," decided on pure aesthetic grounds, then assign meaning to that palette — don't style ad hoc per label.
- A required "ugly" constraint on a map (must obscure a sensitive location) doesn't have to look like an obvious blur — a plausible generative texture that doesn't itself attract attention satisfies the constraint more gracefully.
- Rivers/water bodies: a simple light-blue line freed from the scheme's angle grid reads well; a stronger technique borrowed from cartography is shading that darkens near the shoreline, which reads better than parallel lines or wave patterns.
- The map's background represents land; its *absence* represents water — a water body doesn't have to be filled blue to read as water.
- Parks/green space: a flat green fill or "no street grid" is enough by default; detailed tree-crown icons are appropriate only for a task that specifically calls for them.
- Rotating a navigational/street map away from the conventional north-up orientation is acceptable (a majority of users prefer direction-of-travel orientation) only if the user is already comfortable with the place's standard orientation — otherwise rotation disorients rather than helps.
- Color-coding by district/zone only pays off with sustained, repeated exposure (like metro lines) — a one-off or rarely-seen color code in an unfamiliar environment carries no real information.

### Графики
- No chart without a genuine pattern/relationship in the data — a chart of already-sorted-descending data shows only that it's sorted, a null insight; use a table or plain text instead.
- Always label units and cite source/method/authors — a chart is worthless if the reader can't tell what's being measured or why to trust it.
- Combine multiple curves on one shared coordinate system only when their axes genuinely coincide (same unit of measurement); otherwise normalize to relative values or stack the charts vertically sharing only the X-axis.
- Merging curves with mismatched axes onto one shared scale produces misleading "pseudo-curves."
- Use "small multiples" (repeated, identical small charts, legibly ordered) rather than one overloaded combined chart when comparing many categories.
- Fold the legend into one of the charts itself rather than a separate color key, freeing color to carry information instead of merely labeling it.
- Enrich a metric with context/causality rather than showing a bare value or category zone — pair a spike with the event that caused it, rather than an isolated abstract measurement.
- A chart works best wider than tall — a roughly 45° slope for the steepest features reads most naturally.
- Don't visualize the obviously self-evident (a spec that's just a bare number, restated as a shape) — it adds a form without adding insight.
- Don't map a non-cyclical quantity (a day's schedule) onto a circular chart just because a clock face is a familiar shape — a circle implies cyclical/periodic meaning and misleads when the underlying data is linear.
- Replace an opaque summary counter ("выбрано 5") with the actual selected values ("Москва, Казань (+3)") wherever there's room — this raises informativeness without changing the control's structure.
- When options differ along several independent dimensions (module × content type × format, for a set of pricing tiers), visualize as a matrix rather than as parallel single-axis cards — parallel cards make cross-dimension comparison much harder to see at a glance.
- Set prices and other emphasized numerals in true lining figures, not minuscule/old-style figures, and space digit groups consistently across every price shown on a screen — inconsistent number styling within one price list undermines trust more than its size suggests.

---

## 7. Текст в интерфейсе (Interface copy)

### Стоп-слова
- Definition (Ilyakhov's, adopted by Birman): words that are «предсказуемо удаляются из текста без потери смысла» (predictably removable without losing meaning).
- **Evaluative adjectives** ("основной," "важный," "полезный"): naming something "useful" implies the rest isn't — state the concrete benefit instead of the label.
- **Modal/obligation words** ("необходимо," "обязательно," "должен," "пожалуйста"): replace "Обязательное поле" with the actual payoff ("Курьер позвонит за час").
- **Generic descriptive terms** ("форма," "список," "архив," "справочный"): name the thing itself — "Покупка Айфона," not "Форма заказа"; "Обои," not "Каталог обоев."
- **Technical/IT jargon** ("транзакция," "авторизация," "сессия"): translate into plain language — "вход," not "авторизация."
- **Empty verbs** ("перейти," "запустить"): name the object directly — "Словарь," "Почта," not "Перейти в Словарь."
- Application rule: if you understand *why* a word is formally "bad" but are certain it belongs here anyway, keep it — it's a heuristic, not a dogma.
- Universal test: if a word can be deleted without loss of meaning, delete it.
- "Расширенный/дополнительно" is usually «свалка всего, чему проектировщик не нашёл места» (a dumping ground for whatever the designer found no proper place for) — a red flag worth interrogating, not just a neutral label.

### Регистр, вежливость, жаргон
- No politeness is owed by a machine: «Никакой невежливости в отсутствии слов «спасибо» и «пожалуйста» нет» — you don't expect politeness from an elevator either.
- Reserve "спасибо"/"пожалуйста" for text explicitly voiced by a named human, first person ("мы получили ваше обращение"), never for system-voiced copy.
- Avoid emoji/smileys in an organization's formal voice — «улыбаться должно физическое лицо, а не организация».
- If smileys fit the product's tone, standardize their use as part of the editorial toolkit rather than leaving it to individual authors.
- Replace IT/system terminology with the user's own words: "авторизация/аутентификация" → "вход."
- Never write jargon acronyms without spelling them out for the audience — don't assume domain fluency.
- Machine-generated, template-driven copy reads as inhuman ("Нет новых писем") — write each message deliberately for its specific case, not from a shared template.
- Common sources of inhuman copy: universal templates applied without understanding meaning, developers avoiding grammatical declension, showing empty/unhandled states instead of hiding them, unreviewed system dialogs leaking through, and the underlying state graph "leaking" into the interface's language.
- Name a control by its user scenario, not its technical action — before naming a "Duplicate"/"Copy" button, ask why users actually want a copy, and name the button for the outcome.
- «Изменить» is an acceptable, shorter Russian translation for "Edit" over the more cumbersome «Редактировать» — or sidestep translation with a pencil icon.
- A form's title must describe its actual, specific content, not the general service category — and the button's verb must agree syntactically with that specific noun (e.g. "запись" pairs with "назначить," not with a generic "заказать").
- An email/message signature should carry "a semantic period" appropriate to the relationship ("С уважением" / "Твой сын" / a job title) — not a fixed template regardless of context; skip it in active back-and-forth threads.

### Числа, единицы, форматирование
- Explicit units are often unnecessary where context already disambiguates plausible magnitude (weather forecasts don't need °C stated) — add explicit units only where the reader has no intuitive reference (a device's operating-temperature spec).
- Degree-sign typography: no space before a bare degree ("+15°"); a normal space before a unit letter ("+15 °C"); keep the unit letter at full cap-height, never shrunk into a fake superscript.
- Thousand-separator spacing must be visually distinct from a normal word space, or numbers of four-plus digits "fall apart" into what reads as several numbers.
- There's no fixed universal separator width — tune it per typeface and context, down to a "third-space" if needed.
- Follow the language's actual numeral convention rather than an institutional standard that contradicts it — Russian: comma for decimal, space for thousands.
- Convert raw units into the format people actually think in (3:55 instead of 235 raw minutes) — an unfamiliar large absolute number isn't intuitively legible.
- «Лучше сказать примерно, но понятно, чем точно, но непонятно — это человечность» (better approximate-but-clear than exact-but-confusing).
- State a negative temperature interval from low to high by default ("−35…−30 °С"); the reverse order (high to low) is acceptable only to convey escalating intensity, and should be labeled explicitly ("холода," not "температура") when used that way.
- Prefer the language's regionally standard separator for large numbers over an official classifier that contradicts normal orthography — trust the typographic tradition over the bureaucratic standard when they conflict.

### Ссылки, сноски, ирония, транслитерация
- A link is itself a visual emphasis — «Ссылка — это выделение, так уж вышло» — choose surrounding words and sentence order knowing the link will visually dominate.
- Footnotes/asterisks read as "the bitter truth" and provoke distrust — state data and its source openly in the running text rather than tucking it behind a footnote marker.
- Citing a source openly is a mark of respect for the reader, not a defensive move.
- Strikethrough for irony is risky: it can be silently lost when text is copied to plain text, reversing the meaning — the more consequential the context, the more caution around a joke delivered this way («не уверен — не шути»).
- With widely-known foreign names, transliteration causes no confusion; with unfamiliar names, disambiguate through context, quotation marks, or a brief category gloss.
- Russian transliteration of an unfamiliar foreign name is often clearer than the Latin original, since Latin letters (ch, v, e) read ambiguously across languages to a Russian-only reader.
- A spoken/voice channel is a low-resolution substitute for a scannable table — don't replace a data table a user needs to compare values in with an audio readout of the same numbers.
- An offline-printed domain name reads best bare, lowercase, without protocol or "www" — reserving capitalization inside a domain for cases where it's genuinely needed to disambiguate an otherwise hard-to-parse name.
- A nested-quotation convention exists for a reason: inside a «guillemet»-quoted passage, switch to „low-high" quotes for the embedded quotation rather than repeating the same quote glyph at both levels.
- Distinguish technical, case-sensitive machine-facing tokens (real file extensions: MP3, PDF) — keep those Latin — from the same terms used as ordinary words in Russian prose, which should be transliterated and capitalized like any acronym (МП3, ПДФ), without quotation marks.
- A period can close a bureaucratic/postal address when it's read as a complete statement — it gives the block a more finished, stable feel.
- A space always separates words, even abbreviated ones ("ул. Ленина"); with very dense abbreviation runs the individual space may shrink, but do it consistently, not ad hoc.

---

## 8. Вёрстка экрана (Screen layout & density)

- **УВЛ (убрать всё лишнее)** is the default reflex on any pass: try removing an element before adding an explanation to it.
- Don't draw decorative shadows/gleams/bevels without a physically coherent light model — an ungrounded highlight looks arbitrary and dated even after every other detail is fixed: «даже если всё поправить, кнопка не станет крутой, стиль устарел».
- All-caps type without letter-tracking is a typesetting mistake, not a stylistic choice, and reads as harder to scan generally.
- Strip nested boxes-within-boxes and redundant borders/frames first when cleaning up a cluttered screen — «графический мусор в виде вложенных друг в друга плашек и рамок» — this alone often does more than any single content fix.
- Remove decorative color and background fills that carry no meaning; a color must encode information, or it's noise — «убрать зелёность, потому что она ничего не значит.»
- A colored plate/background under a submit button and its fields is functional, not decorative: it makes the form's endpoint and dominant action visible regardless of the form's length or complexity.
- An associated required checkbox belongs on that same plate, visually subordinated to the button it governs.
- «Использовать всё пространство стоит всегда, на то это пространство и дано» (space should always be put to use), but that doesn't obligate filling it with *content* — empty space can itself be a deliberate compositional choice.
- Full-bleed background fills on every section of a page flatten hierarchy and read as "the author didn't care" — reserve edge-to-edge treatment for the first/last block or for photography, to preserve a sense of priority.
- Responsive design's core rule: the page must not lose recognizability across breakpoints — element order and general appearance should stay close enough that the user never consciously registers "this is the mobile version."
- Design responsiveness per element (menu, images, marginal notes, tables), each with its own predictable adaptation, rather than redesigning the whole page per breakpoint.
- Make the semantic relationship between elements explicit before adapting layout (does this image illustrate the whole text or one paragraph? does this note apply to the whole piece or one paragraph?) — that relationship should drive how it reflows.
- Don't design for a single target resolution — think simultaneously about placement and behavior under resize, not one fixed breakpoint.
- "Резиновая" (fluid) layout respects that the user controls their own browser, but fluid doesn't mean infinitely stretching everything.
- The actual design task under fluid layout is choosing which elements stretch, within what limits, by what rule — e.g. capping a text column's width for readability regardless of viewport.
- On dark UI backgrounds, weight/contrast changes (bold text, subtle highlight) read far more weakly than on light backgrounds — pair a weight change with a brightness change to make it register on dark surfaces.
- Test any layout in its real physical/viewing context before calling it final — floor-mounted, kiosk, and poster graphics read differently in situ than on a flat monitor mockup.
- Don't stop at "not visually broken" without JavaScript — a page should degrade gracefully, not collapse entirely, even where full no-JS parity isn't worth engineering.
- Font smoothing has no medium-specific exception — apply it consistently across the whole screen design, not selectively.
- A vector-heavy layout benefits from a divisible base unit (e.g. 12, divisible by 2 and 3) for derived stroke widths — pick type sizes by eye against the resulting linework, not by formula.
- When redesigning an unclear existing artifact and you don't know where to start, ask the original authors what they meant to communicate, then communicate that clearly — don't guess purely from the artifact.
- Don't remove a working, well-liked graphic element (a distinctive scheme feature, an old signage element) purely for internal consistency if doing so measurably degrades what's actually there — coexistence of old and new can look better than a forced, lowest-common-denominator unification.
- Mass unification/standardization "from above," pursued purely for consistency, risks a race to the bottom in unit cost and quality — prefer adding what's missing point by point over wholesale replacement of things that already work.
- Don't algorithmically randomize a "casual-looking" layout (scattered photo grid, organic arrangement) at runtime — design a small set of genuinely good fixed arrangements and cycle through them; «высший пилотаж — дизайн, который выглядит круто, но прост в реализации» (the real mastery is a design that looks impressive but is simple to implement).
- Prefer vector construction over hand-placed pixels wherever a shape can be built from real geometry — curves, offsets, and boolean operations reproduce cleanly at any size; a hand-nudged pixel doesn't.
- Excess decoration that forces a shrink in the primary content's type size has lost the actual trade-off — if ornamentation is squeezing out legibility, remove the ornamentation, not the type.
- Too many simultaneous emphasis devices stacked on one piece of text (bold and color and italic and a larger kegel at once) reads as noise, not emphasis — pick one dominant device per distinction and stay with it.
- Agree on a shared measurement convention within the team (which baseline you measure spacing from, em vs. pixel units when briefing a developer) rather than searching for the objectively "correct" method — consistency inside the team matters more than the reference point chosen.

---

## Diagnostic checklist

Fifteen highest-yield checks, in priority order — run them in sequence when reviewing any interface.

1. **Syntax of every label.** Read each button/link aloud: is it a command (perfective verb), a navigation object (noun), or a status (nominal predicate)? Does the syntax match the actual function? Does a form's title read as the subject and its button as the predicate of one sentence?
2. **Removable without loss?** For every element, word, and step: can it be deleted without losing meaning (УВЛ)? Can what's currently manual be computed/automated instead ("пусть потеет машина")?
3. **Hidden modes.** Does one gesture ever mean two different things depending on a state the user isn't tracking? If modality exists, is it cured (separate gestures / quasimode / changed scenario) rather than just made "visible" (a half-measure with its own attention cost)?
4. **Feedback loop.** Does every user action produce an instant, honest, continuous, gentle, physically-plausible reaction? Is anything reported as succeeded before it actually has?
5. **Error prevention over error messaging.** Are invalid actions disabled/masked away before submission, or only caught and explained afterward? Is there Undo for anything destructive, rather than (or in addition to) a confirmation dialog?
6. **Newcomer's eyes.** Does every individual screen — including empty, loading, and error states — make sense on its own, with no memory of prior screens or hidden context?
7. **Fitts's law.** Are hit areas at least as big as (ideally bigger than) their visual glyphs? Are dangerous/adjacent controls separated? Are frequent actions placed where aiming is cheap (edges, corners, under the cursor)?
8. **Proximity.** Does spatial closeness correctly signal every real relationship, and correctly avoid signaling false ones? Any element sitting closer to the wrong neighbor than the right one?
9. **Checkbox/radio/dropdown fit.** Is the control type matched to the actual decision (binary self-evident → checkbox; mutually exclusive with visible options → radio, vertically stacked; compact single-row choice → segmented control; long/rarely-glanced list → dropdown)? Is the whole label clickable? Is there always a safe default or an explicit "not specified" option?
10. **Table integrity.** Is there an actual comparison being made? Are numbers aligned by digit rank? Is anything stretched beyond its data's natural width, ruled, or zebra-striped without solving a real problem?
11. **Vocabulary.** Any stop-words (основной/обязательно/форма/авторизация/пожалуйста) that could become concrete benefit or plain language? Any unexplained jargon/acronym?
12. **Navigation matches scenario, not data structure.** Does the menu/hierarchy reflect what the user is trying to do, or how the backend/database happens to be organized? Are dead ends (404, empty states) helpful rather than a wall?
13. **Consistency as a law, not a pile of cases.** Can the interface's behavior be stated as one general rule with no exceptions? Does the same element always look/behave the same way across the product?
14. **Density and decoration.** Any nested boxes-within-boxes, unmotivated shadows/gradients/borders, or color that carries no meaning? Would removing them lose any real function?
15. **Responsive recognizability.** Does the layout stay recognizable — same relative order, same feel — across breakpoints, or does it visibly "become a different product" on mobile?

Run 1–6 first on any flow with real user consequences (forms, checkout, destructive actions); run 10–15 first on data-dense or read-only screens (dashboards, tables, schemes, signage).
