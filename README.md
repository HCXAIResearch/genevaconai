| Field | Value |
|---|---|
| Title | Information Provisions of the Geneva Conventions — Learning Aid |
| Document Reference | HCXAI-LA-001 |
| Version | 1.0 |
| Status | Released |
| Owner | HCXAIResearch |
| Audience | AI governance practitioners, compliance leads, training facilitators |
| Standards Reference | Geneva Conventions of 12 August 1949 (GC I–IV); ISO/IEC 42001:2023; ISO/IEC 42005:2025; NIST AI RMF 1.0; OECD AI Principles |
| License | See LICENSE |

# Information Provisions of the Geneva Conventions

A single-file, browser-based teaching module that draws seven data-governance principles out of the text of the four Geneva Conventions of 12 August 1949 and translates each one into terms an organisation **deploying** AI in or around armed conflict can act on.

Nine tabbed sections, thirty-one checked questions, a live scorecard. No backend, no build step, no telemetry.

---

## Why this exists

The 1949 Conventions were drafted for index cards, sealed packets and the postal service. They nonetheless contain the most tested body of rules anywhere on handling data about people who cannot protect themselves — which is precisely the problem an AI deployer faces in conflict-adjacent work.

This module extracts the information provisions specifically, separates them from the targeting and weapons-review provisions that dominate the AI-and-warfare literature, and presents them as a set of design constraints.

Two structural findings run through the whole module and are taught explicitly:

| Finding | Consequence for system design |
| --- | --- |
| Identification in these Conventions is a **protective** act, never a targeting one | A capability that identifies people for protection is authorised by this text; the same capability pointed at targeting is not |
| The **prohibitions are absolute; the obligations are best-efforts** | Gives a clean hard-constraint / soft-constraint split. Operational pressure may compress an obligation; it never touches a prohibition |

---

## What is in it

| # | Section | Provisions covered | Questions |
| --- | --- | --- | --- |
| 00 | Orientation | The two structural findings; how the module runs | 2 |
| 01 | Minimisation | `GC III Art. 17 ¶1`, `GC III Art. 122 ¶4`, `GC IV Art. 138` | 3 |
| 02 | Coercion | `GC III Art. 17 ¶4`, `GC IV Art. 31`, `GC III Art. 99 ¶2` | 3 |
| 03 | Exposure | `GC III Art. 13 ¶2`, `GC IV Art. 27`, `GC IV Art. 137 ¶2` | 3 |
| 04 | Provenance | `GC I Art. 16`, `GC III Art. 122 ¶8`, `GC IV Art. 137 ¶4`, `GC III Arts. 96 & 105` | 3 |
| 05 | Timeliness | `GC III Art. 122 ¶5–6`, `GC IV Art. 136 ¶2`, `GC III Art. 120` | 3 |
| 06 | Interoperability | `GC I Art. 40`, `GC II Art. 42`, `GC III Arts. 123–124`, `GC IV Arts. 140–141` | 3 |
| 07 | Vulnerability | `GC IV Art. 50`, `GC IV Arts. 25–26`, `GC III Art. 17 ¶5` | 3 |
| 08 | Assessment | Mixed, drawing across all seven principles, plus scorecard | 8 |

Every principle section follows the same three-beat structure: **article extracts → "For the AI deployer" translation → checked questions.**

---

## Running it

Open `index.html` in any modern browser. That is the whole installation procedure.

To host it, drop the file anywhere that serves static content — SharePoint document library, internal wiki, S3 bucket, GitHub Pages. It has no server dependency and no same-origin requirement.

The only external requests are Google Fonts. If your environment blocks them, the module degrades to the declared fallbacks (Georgia, system monospace) with no loss of function. To make it fully self-contained, remove the two `<link rel="preconnect">` tags and the stylesheet `<link>` in `<head>`.

---

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The module. Self-contained: markup, CSS, content and logic in one file |
| `README.md` | This document |
| `USER_MANUAL.md` | Facilitator guide, session plans, verified answer key, customisation instructions |

---

## Design and branding

Branded to the HCXAIResearch identity. Tokens are declared once in `:root` and nothing downstream hard-codes a colour.

| Token | Value | Role |
| --- | --- | --- |
| `--navy` | `#1B2A4A` | Masthead, dark panels, body ink |
| `--red` | `#0E7C7B` | Primary accent on light surfaces — citations, tab rule, kickers |
| `--onDark` | `#2FB6B2` | Accent on navy — progress bar, translation-panel headings |
| `--alert` | `#B4232A` | Semantic error state only; deliberately outside the brand palette |
| `--green` | `#0E7C7B` | Correct-answer state |
| `--leaf` | `#F3F6F8` | Page stock |
| `--rule` | `#D4DCE4` | Hairlines and card borders |
| `--slate` | `#5A6779` | Secondary text, marginal notes |

The `--red` token name is a legacy of the first build and is retained so that existing selectors stay untouched. It carries the deep teal value. Rename it if you fork.

**Typography.** Zilla Slab (display), Source Serif 4 (body and article extracts), IBM Plex Mono (provision codes and utility labels). This departs from the HCXAI house pairing of Poppins and Inter: treaty text reads correctly in a serif, and the slab display face carries the institutional register the subject needs. Swap it if house consistency matters more than register.

**Signature device.** Each provision is set as a booklet spread — article citation and a marginal descriptor (*Questioning of prisoners*, *Central Agency*) in a right-aligned left margin, extract beside them under a teal rule. This reproduces the marginal-note pattern of the printed Conventions. On narrow viewports the margin column collapses above the extract.

**Emblem.** The HCXAI bracket-and-figure logomark, inline SVG. The red cross emblem used in the first build was removed deliberately: recolouring a protective emblem to a brand palette is inappropriate on a document about the Conventions.

---

## Technical notes

- Vanilla JavaScript, no framework, no bundler. Content lives in a single `LESSON` array near the top of the `<script>` block; rendering is a loop over it.
- **No browser storage.** State is held in a plain in-memory object. Scores do not survive a page reload, by design — the module is intended for a facilitated session, not longitudinal tracking. If you need results captured, see *Capturing results* in the manual.
- Answers lock on submission and cannot be changed. Feedback appears immediately with the reasoning tied back to the article.
- Correct-answer positions are distributed across A/B/C/D rather than clustering, so the module cannot be passed by test technique alone.
- Accessibility floor: ARIA tab pattern, arrow-key navigation between sections, visible focus rings, `prefers-reduced-motion` respected, responsive to 320 px.

---

## Scope limits

Read these before putting the module in front of an external audience.

1. **1949 Conventions only.** Additional Protocol I is not covered. In particular `AP I Art. 36` (review of new weapons, means and **methods** of warfare) and `AP I Art. 57` (precautions in attack) carry the review and human-judgment obligations most often invoked for autonomous systems. Their absence is stated in the module footer, but a facilitator should name it aloud.
2. **Extracts are abridged for teaching.** Ellipses and emphasis have been applied. Nothing in this module is a substitute for the authoritative text.
3. **Not legal advice.** The "For the AI deployer" panels are a governance reading, not an interpretation of treaty obligations. Where a real deployment decision turns on any of these provisions, take qualified IHL advice.
4. **Deployer perspective throughout.** The module addresses what a deploying organisation can document, assess and control. It does not address obligations that fall on states or on frontier model developers.

---

## Roadmap

| Item | Note |
| --- | --- |
| AP I module | `Art. 36` review duty and `Art. 57` precautions, as sections 09–10 |
| Control mapping | Provision → AI governance control → `ISO/IEC 42001` Annex A control, as an exportable table |
| Results export | JSON snapshot of a completed attempt, consistent with the SharePoint versioning pattern used across the HCXAI toolkit |
| Optional full-text toggle | Disclosure control revealing the unabridged article beside each extract |

---

## Changelog

| Version | Change |
| --- | --- |
| 1.0 | Initial release. Nine sections, thirty-one questions, HCXAIResearch palette, answer positions rebalanced, question total corrected |
| 0.2 | Rebranded from ICRC red/black to HCXAI navy/teal; emblem replaced with the bracket-and-figure logomark |
| 0.1 | First build in the source document's palette |

---

*HCXAIResearch · Human Centered Explainable AI (Governance) · `HCXAI-LA-001` v1.0*
