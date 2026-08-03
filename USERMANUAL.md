---
title: "Information Provisions of the Geneva Conventions — Facilitator Manual"
document_ref: HCXAI-LA-001-M
version: 1.0
status: Released
owner: HCXAIResearch
applies_to: geneva-data-provisions-lesson.html v1.0
audience: Facilitators, trainers, self-directed learners
---

# Facilitator Manual

Everything needed to deliver, adapt or self-study the module. Section 1 covers delivery, section 2 the teaching notes, section 3 the verified answer key, section 4 customisation.

---

## Contents

1. [Getting started](#1-getting-started)
2. [Session plans](#2-session-plans)
3. [Teaching notes by section](#3-teaching-notes-by-section)
4. [Answer key](#4-answer-key)
5. [Scoring and interpretation](#5-scoring-and-interpretation)
6. [Customisation](#6-customisation)
7. [Capturing results](#7-capturing-results)
8. [Accessibility](#8-accessibility)
9. [Troubleshooting](#9-troubleshooting)

---

## 1. Getting started

Open `geneva-data-provisions-lesson.html` in a browser. There is nothing to install.

### The interface

| Element | Behaviour |
| --- | --- |
| Masthead | Navy band, HCXAI logomark, module title |
| Tally strip | Running count of questions answered and correct, with a progress bar. Updates on every submission |
| Tab strip | Nine sections, numbered `00`–`08`. Sticks to the top of the viewport when scrolling. Horizontally scrollable on narrow screens. A tick appears on a tab once all its questions are answered |
| Provision cards | Article citation and marginal descriptor in the left margin; the extract beside it. Operative phrases are highlighted |
| Translation panels | Navy blocks headed **For the AI deployer**. The governance reading of the provisions above |
| Questions | Four options each. Click to submit. Options lock, the correct answer is marked, the chosen wrong answer is struck through, and the reasoning appears |
| Scorecard | Tab `08`. Overall percentage, raw score, per-section breakdown, and **Start over** |

### Navigation

Click a tab, or focus the tab strip and use the left and right arrow keys. Selecting a tab returns the view to the top of the panel.

### Two things to know before you present

**Answers lock.** There is no undo on a submitted answer. Say this at the start of a session, or learners will guess on the first question and be annoyed.

**Nothing is stored.** A reload wipes all progress. Do not reload mid-session, and do not rely on the module to record results — see [section 7](#7-capturing-results).

---

## 2. Session plans

### 90 minutes — full delivery, recommended

| Time | Activity |
| --- | --- |
| 0:00–0:10 | Tab `00`. Frame the two structural findings. Do not skip this; the rest of the module depends on them |
| 0:10–0:20 | Tab `01` Minimisation. The clearest section — use it to establish the three-beat rhythm |
| 0:20–0:35 | Tab `02` Coercion. The hardest and most important. Budget the extra time |
| 0:35–0:45 | Tab `03` Exposure |
| 0:45–0:55 | Tab `04` Provenance |
| 0:55–1:05 | Tabs `05` Timeliness and `06` Interoperability, paired — both are about the record in motion |
| 1:05–1:15 | Tab `07` Vulnerability. Close on the ranking in `GC III Art. 17 ¶5`; it is the strongest note to end on |
| 1:15–1:30 | Tab `08` Assessment, then scorecard and discussion |

### 45 minutes — condensed

Tabs `00`, `01`, `02`, `07`, `08`. This keeps the two structural findings, the absolute prohibition, and the explicit ranking of protection above necessity. Set tabs `03`–`06` as follow-up reading.

### 25 minutes — briefing

Tab `00` and the eight-question assessment on tab `08`. Use wrong answers to decide which principle sections the audience needs.

### Self-directed

Work through in order. Budget two hours. Read each translation panel twice — once before the questions and once after, since the questions are written to expose the gap between recognising a provision and applying it.

---

## 3. Teaching notes by section

### 00 · Orientation

The whole module hangs on the second finding. Make the audience read the qualifying language themselves: *as soon as possible*, *in so far as available*, *if possible every week* — then note that the coercion prohibition has no qualifier at all. Once they see it, the hard-constraint / soft-constraint split becomes obvious rather than asserted.

**Anticipate:** someone will argue every obligation is negotiable in practice. Agree, and point out that this is exactly why the distinction matters.

### 01 · Minimisation

The teaching point most often missed is the two-sided drafting. `GC IV Art. 138` sets a **floor** ("at least") because the protective purpose requires a minimum. `GC III Art. 17` sets a **ceiling** ("only") on what may be compelled from the individual. Most corporate minimisation controls have only a deletion schedule, which is neither.

**Discussion prompt:** name one field your systems currently hold about an identifiable person, and state the protective purpose it serves. Fields that cannot survive the question are out of scope.

### 02 · Coercion

Slow down here. Three system classes sit directly under this prohibition, and it is worth naming each: compelled biometrics, affect and deception inference, and network inference about third parties.

`GC IV Art. 31`'s reach to third parties is the provision practitioners have never heard of and the one with the widest implication for graph and relationship models.

**Anticipate:** an operational-necessity argument. The answer is structural, not rhetorical — there is no exception clause, no balancing test and no consent gateway in either article. In a control framework this is a design failure, not a risk to be scored.

### 03 · Exposure

Open by separating two questions that practitioners routinely merge: *may we hold this?* and *may we show this?* Lawful holding does not license display.

`GC IV Art. 137 ¶2` is the most directly reusable piece of architecture in the module — a harm-based test on outbound sharing, paired with a channel to the neutral custodian that cannot be suppressed. Protecting the individual changes routing; it does not delete the record.

**Discussion prompt:** who can currently screenshot your operational dashboard, and where does that screenshot go?

### 04 · Provenance

Frame the signature-or-seal requirement as a 1949 non-repudiation control. It attributes a communication to an accountable author and makes alteration detectable — neither of which encryption or access control does.

The load-bearing point: where a model drafts, matches or de-duplicates a record, the authentication duty does **not** transfer to the model. A human signs, which means that human must be able to see and correct what the system produced. Automation that cannot be inspected cannot be attested.

**Line worth using:** an erroneous identification here is not a data-quality defect. It is a person unaccounted for.

### 05 · Timeliness

The distinction to drive home is event-driven versus periodic. Six named events trigger an immediate push — transfers, releases, repatriations, escapes, hospital admissions, deaths, and under `GC IV` also births. The weekly health report is the only real periodic duty. A nightly batch export satisfies neither.

`GC III Art. 120` is the one that surprises people: the duty extends to recording subsequent moves of bodies. The record has no terminal state, which constrains any automated archival or deletion policy.

### 06 · Interoperability

Present the identity-card provisions as what they are — a treaty-level interoperability standard, with uniform format and models exchanged *at the outbreak of hostilities*. The lesson is timing: the schema is agreed before it is needed.

The Central Agency is a working precedent for neutral custodianship. Where mutual trust is absent, structure does the work that no contractual assurance between belligerents could.

Do not skip `Arts. 124` and `141`, the free-postage provisions. They exist so that cost never becomes the reason information does not move. Read across: the transmission path must be funded as part of the obligation, not left as an unowned dependency.

### 07 · Vulnerability

Close the module on the last eight words of `GC III Art. 17 ¶5`: *subject to the provisions of the preceding paragraph*. "All possible means" is expressly subordinated to the coercion prohibition — and this is the most sympathetic possible case, a person who cannot state who they are.

Necessity is ranked below protection, on the face of the text. That is the single most transferable drafting move in the module, and it argues for placing constraint checks upstream of optimisation rather than in review afterwards.

`GC IV Art. 50` pairs the heaviest positive duty with an absolute limit in one article: identify actively, record parentage, never alter personal status. For any system that resolves or merges identity records, immutability of legal status is a hard requirement.

### 08 · Assessment

Eight mixed questions. Take the scorecard breakdown into discussion rather than the headline percentage — a low score in one section is a curriculum signal, not a learner problem.

---

## 4. Answer key

Verified against v1.0 of the module. Correct-answer positions are distributed, so do not look for a pattern.

### 00 · Orientation

| Q | Ans | Correct option |
| --- | --- | --- |
| 1 | **A** | Identifying, notifying, treating and accounting for people under a party's control |
| 2 | **C** | The prohibition on coercion to obtain information |

### 01 · Minimisation

| Q | Ans | Correct option |
| --- | --- | --- |
| 1 | **B** | Name, rank, date of birth and serial number, and nothing more |
| 2 | **D** | Sufficient to identify the person exactly and advise next of kin quickly |
| 3 | **A** | Purpose limitation — collection is bounded by the protective purpose, not by accuracy gains |

### 02 · Coercion

| Q | Ans | Correct option |
| --- | --- | --- |
| 1 | **C** | Nothing adverse — they may not be threatened, insulted or disadvantaged in any way |
| 2 | **B** | The protected person and any third parties |
| 3 | **D** | A latency target for transmitting hospital admissions to the Information Bureau |

### 03 · Exposure

| Q | Ans | Correct option |
| --- | --- | --- |
| 1 | **A** | Protection against insults and public curiosity |
| 2 | **C** | Transmission is withheld, but the information may still not be withheld from the Central Agency |
| 3 | **B** | At the disclosure boundary, so routing can differ by recipient while the record stays intact |

### 04 · Provenance

| Q | Ans | Correct option |
| --- | --- | --- |
| 1 | **D** | By a signature or a seal |
| 2 | **A** | Non-repudiation through signed, tamper-evident records |
| 3 | **C** | With the accountable human who reviews and signs the record |

### 05 · Timeliness

| Q | Ans | Correct option |
| --- | --- | --- |
| 1 | **B** | Regularly, every week if possible |
| 2 | **D** | Change of religious observance *(the "NOT" question — flag the stem aloud)* |
| 3 | **A** | It remains live — subsequent moves of the body must also be recorded |

### 06 · Interoperability

| Q | Ans | Correct option |
| --- | --- | --- |
| 1 | **C** | In a neutral country |
| 2 | **B** | At the outbreak of hostilities |
| 3 | **D** | To ensure cost or infrastructure never obstructs the flow of protective information |

### 07 · Vulnerability

| Q | Ans | Correct option |
| --- | --- | --- |
| 1 | **A** | Change their personal status |
| 2 | **C** | The prohibition on coercion in the preceding paragraph |
| 3 | **B** | An automated merge may alter a child's recorded personal status or parentage |

### 08 · Assessment

| Q | Ans | Correct option |
| --- | --- | --- |
| 1 | **D** | `GC III Art. 122 ¶8` → non-repudiation and signed audit trail |
| 2 | **A** | No — the coercion prohibition carries no exception clause |
| 3 | **C** | Obligations carry qualifiers such as "as soon as possible"; prohibitions carry none |
| 4 | **B** | `GC III Art. 13` — protection against insults and public curiosity |
| 5 | **D** | Protection changes who receives the information, not whether it is held |
| 6 | **A** | Notification of a transfer, escape or death |
| 7 | **C** | It places the custodian outside both parties, so exchange does not depend on trust between belligerents |
| 8 | **B** | The prohibitions, which are ranked above the protective objective |

---

## 5. Scoring and interpretation

Thirty-one questions. The scorecard reports percentage of **attempted** questions answered correctly, plus the raw count against the full thirty-one, plus a per-section breakdown.

Suggested reading of the result. These bands are guidance for a facilitator, not a certification threshold — the module carries no accreditation.

| Score | Reading |
| --- | --- |
| 90–100% | Working command of the provisions and their governance translation |
| 75–89% | Solid. Revisit whichever sections show a gap in the breakdown |
| 60–74% | Provisions recognised, application uncertain. Re-read the translation panels |
| Below 60% | Rerun tabs `00`–`02` before continuing. The structural findings have not landed |

Watch for one specific pattern: strong scores on the recall questions (`01 Q1`, `05 Q1`, `06 Q1–Q2`) alongside weak scores on the application questions (`01 Q3`, `03 Q3`, `04 Q3`, `07 Q3`). That combination means the text has been learned and the design implication has not — the more useful of the two to fix.

---

## 6. Customisation

All content sits in the `LESSON` array at the top of the `<script>` block. The renderer loops over it, so nothing else needs touching.

### Section shape

```js
{
  id: "minim",              // unique, used for element ids
  tabLabel: "Minimisation", // tab text
  kicker: "Principle 01",
  title: "Data minimisation and purpose limitation",
  standfirst: "…",
  blocks: [ /* see below */ ],
  quiz: [ /* see below */ ]
}
```

### Block types

| Type | Fields | Renders as |
| --- | --- | --- |
| `prov` | `cite`, `note`, `text` | Provision card. `cite` is the article reference, `note` the marginal descriptor. Wrap operative phrases in `<em>` to highlight them |
| `translate` | `h`, `ps` (array) | Navy translation panel |
| `note` | `h`, `p` | Bordered aside on the page stock |
| `html` | `html` | Raw markup, for prose sections with `<h3>` subheads |

### Question shape

```js
{
  stem: "…",
  opts: ["…", "…", "…", "…"],
  a: 2,          // zero-based index of the correct option
  why: "…"       // shown after submission, both when right and wrong
}
```

Vary `a` across `0`–`3` as you add questions. The `31` in the tally strip is hard-coded in the markup — search for `/ 31` and update it if you change the question count. Everything else recalculates.

### Rebranding

Change the tokens in `:root` and nothing else. The `--red` variable name is legacy from the first build and holds the deep teal value; rename it across the file if it bothers you, but nothing depends on the name.

To restore the source document's palette: `--navy` → `#141210`, `--red` → `#D7141A`, `--onDark` → `#D7141A`, `--leaf` → `#F6F3EF`, `--rule` → `#D9D3CB`, `--slate` → `#55504A`.

### Typography

Replace the Google Fonts `<link>` and the `--display`, `--body`, `--mono` tokens. For the HCXAI house pairing: Poppins for `--display`, Inter for `--body`, IBM Plex Mono unchanged.

---

## 7. Capturing results

The module holds no storage and emits no telemetry, deliberately. For a session where results must be recorded, in order of effort:

1. **Screenshot the scorecard.** Adequate for most training records. Capture tab `08` after the assessment.
2. **Facilitator tally.** Run the assessment as a group exercise and record answers on a sheet, using [section 4](#4-answer-key).
3. **Add an export.** In the browser console, `JSON.stringify(state)` returns the full attempt keyed by question id. Wiring that to a download button follows the pattern used across the HCXAI toolkit: build a `Blob`, create an object URL, trigger an anchor click. **Do not use `window.print()`** — it is blocked in sandboxed iframes, which is why every export in the toolkit is Blob-based.
4. **Snapshot to SharePoint.** Consistent with the versioning approach used elsewhere in the toolkit: attach the exported JSON to the training record. There is no backend to query.

---

## 8. Accessibility

| Feature | Implementation |
| --- | --- |
| Tab pattern | `role="tablist"` / `role="tab"` / `role="tabpanel"` with `aria-selected` and `aria-controls` |
| Keyboard | Left and right arrows move between sections when the tab strip has focus. All controls are native buttons and reachable by <kbd>Tab</kbd> |
| Focus visibility | 3 px teal outline with offset on tabs, options and buttons |
| Motion | `prefers-reduced-motion: reduce` disables all animation and transition |
| Colour | Correct and incorrect states carry a border-weight change and a strike-through in addition to colour, so the distinction does not depend on hue |
| Viewport | Responsive to 320 px. Below 760 px the provision margin column stacks above the extract |
| Zoom | Type is set in `px` against a fluid `clamp()` scale for headings; text reflows to 200% zoom without horizontal scrolling |

**Known limitation.** Answer submission is not announced to screen readers via a live region. If you are delivering to screen-reader users, add `aria-live="polite"` to the `.why` container.

---

## 9. Troubleshooting

| Symptom | Cause and fix |
| --- | --- |
| Type renders as Georgia and a default monospace | Google Fonts is blocked. Harmless — the fallbacks are declared. To remove the dependency, delete the `<link>` tags in `<head>` |
| Progress lost | Expected. State is in memory only; a reload clears it. Do not reload mid-session |
| Tabs run off the screen | Working as intended on narrow viewports. The strip scrolls horizontally, or use arrow keys |
| An answer cannot be changed | By design. Answers lock on submission. **Start over** on tab `08` resets everything |
| Scorecard shows 0% with answers submitted | The percentage is of attempted questions and updates on submission. If it is genuinely stuck, the browser has blocked scripts |
| Provision margin column collapsed on a wide screen | Browser window is under 760 px wide, or page zoom is high enough to cross the breakpoint |
| Editing the `LESSON` array broke the page | Almost always a missing comma or an unescaped `"` inside a string. Open the console for the parse error, or run `node --check` against the extracted script block |

---

*HCXAIResearch · Human-at-centre AI governance · `HCXAI-LA-001-M` v1.0*
