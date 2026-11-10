# ValiWaste AI — Revised Opportunity Report (v2)

**Prompt version used:** "Find a Quick-Win AI Business Opportunity" v3 (2026-11-05)
**Scope:** INDUSTRY = Récupération de déchets triés / recyclage, valorisation matière (NAF anchor 38.32Z, given); CUSTOMER_LOCATION = Doubs, France; BUSINESS_SIZE = self-employed, 1–9, 10–49, 50–249; MY_LOCATION = Besançon; TIME_TO_FIRST_SALE = 1 week; MAX_DAYS_TO_PAYMENT = 14.
**This is a revision of a v1 report dated 2026-11-05.** Every figure below has been checked against primary sources or the official French company registry API; changes from v1 are marked **[CORRECTED]**. Figures not marked that way were confirmed as originally stated.

**Current date: November 6, 2026.**

---

## 0. What changed from v1, and why

v1 was directionally right — a real legal trigger, a real target NAF code, a real host candidate — but contained enough factual errors that it would have failed on first contact with a prospect or the host organization. This revision corrects:

1. **The regulatory fact itself was slightly wrong.** Annexe I-B covers 8 flux (7 historic + textiles), not "8 to 9 including biowaste." Biowaste has its own, separate attestation under a different article (D. 543-226-2). **[CORRECTED]**
2. **The federation's name needed a date-sensitive correction.** It was called FEDEREC (one R) until an extraordinary general meeting in November 2024, when it renamed itself **FEDERREC** (two R's). As of today (Nov 2026), FEDERREC is the current, correct spelling to use in all outreach material. **[CORRECTED]**
3. **A real, SME-priced competitor exists** (Okapia OS, €340–890/month) that v1's adversarial test missed. **[CORRECTED — new finding]**
4. **Both of v1's named example prospects are disqualified.** Doubs Recyclage (Établissements Artmann et Fils) and Haut-Doubs Recyclage (Massacrier) are both officially classified `ETI` (entreprise de taille intermédiaire) and/or group-controlled — not independent SMEs. **[CORRECTED — new finding]**
5. **The addressable market was never actually counted in v1** ("~86 registered units," unsourced). It has now been counted exactly, at three geographic levels, via the official INSEE/Sirene-backed company registry API. **[CORRECTED — new data]**
6. **The revenue-impact framing leaned on cost savings and churn defense**, which the prompt's own Goal section explicitly excludes from "measurable revenue growth." Reframed below around account acquisition/AOV, consistent with the prompt's kill condition. **[CORRECTED]**
7. **The "first year of enforcement" timing claim was stale.** Annexe I-B's actual first mandatory use was Jan–March 2026 — already past. This is the *second* cycle (due March 31, 2027), which is reframed below as a stronger hook, not a weaker one. **[CORRECTED]**

---

## 1. NAF value-chain exploration (unchanged from v1, confirmed)

| Position | NAF | Description | Fit |
|---|---|---|---|
| Upstream | 38.11Z | Collecte des déchets non dangereux | High public-sector/procurement friction |
| **Core anchor** | **38.32Z** | **Récupération de déchets triés** | **Selected — confirmed below with real counts** |
| Downstream | 38.21Z | Traitement et élimination | Too consolidated, slow sales cycles |
| Downstream | 46.77Z | Commerce de gros de déchets et débris | Low physical workflow, different problem |

38.32Z remains the right anchor. 38.11Z is kept as a secondary source of prospects (2 of the 11 real Doubs prospects came from 38.11Z), confirmed below.

---

## 2. Pre-check: verified load-bearing facts

| Fact | Status | Source |
|---|---|---|
| **1. Annual sorting attestation obligation** (Art. D. 543-284) — installation operators and intermediaries (collectors/traders/brokers) must deliver an attestation to waste producers before March 31 each year | **Confirmed current** | Légifrance, Arrêté du 21 décembre 2021 (JORFTEXT000045084125); confirmed the obligation applies to "exploitants d'installation" (covers 38.32Z operators directly, not only collectors) |
| **2. Annexe I-B template** — the updated form, used for attestations delivered 1 Jan–31 Mar 2026 covering 2025 waste, onward | **Confirmed current, corrected content** [CORRECTED] | Légifrance; preventionbtp.fr. Covers **8 flux** (papier/carton, métal, plastique, verre, bois, fraction minérale, plâtre, textiles). **Biowaste is NOT part of this attestation** — it has a separate attestation under Art. D. 543-226-2, a different legal basis with different fields. A single combined 9-flux template would not match either official form. |
| **3. B2B client operational pressure** — industrial clients need these attestations for their own compliance/audit purposes | **Confirmed current** | Code de l'environnement Art. R. 541-48-3; consistent with the mechanism described (producers must justify source-sorting via an attestation from their waste handler) |

**No load-bearing fact is superseded or false.** Fact 2 required a correction to its content, not a rejection — this changes the product spec (build to the real 8-flux Cadre 1–6 layout below), not the viability of the opportunity.

---

## 3. Gate results

**Revenue measurement:** PASS, conditional on reframing (see §6).
**Gate 1 (starving crowd):** PASS. Independent recovery yards do the Annexe I-B aggregation by hand; real, named small operators confirmed to exist and be currently active in Doubs (see §9).
**Gate 2 (host-beneficiary):** PASS, with corrections.
- Host: **FEDERREC Centre et Sud-Est** (the regional branch covering Bourgogne-Franche-Comté jointly with Auvergne-Rhône-Alpes).
- Regional **sector** figure (not membership): 125 establishments / 1,831 employees in Bourgogne-Franche-Comté — this is a whole-of-sector statistic the federation publishes, not its own member count. **[CORRECTED]**
- Actual regional **membership**: the branch's own former president stated "beyond 80 companies (excluding national groups)" — use this figure in any host conversation, not the sector stat. **[CORRECTED]**
**Gate 3 (pilot access):** PASS — direct access confirmed via the official company registry; see §9 for the real, verified 11-name Doubs list (not v1's unsourced "~15 facilities").

**Opportunity conditions:**
1. Domain expertise from customer/regulation: PASS — confirmed, the legal schema is public (Légifrance).
2. Technical feasibility: PASS — confirmed buildable with Python PDF parsing + Claude API + PDF generation, now specified against the real Cadre 1–6 field layout (§5).
3. Recurring problem: PASS — annual filing (March 31 every year) plus monthly carbon-reporting subscription.
4. Retention potential: PASS, same mechanism as v1.
5. Capability gap: PASS for the real target list (§9) — none of the 11 confirmed Doubs prospects show signs of in-house dev capacity.
6. Fast first payment: PASS — €950 upfront, 50/50 split, matches the 14-day constraint.

---

## 4. The problem (confirmed, re-sourced)

Independent sorting/recovery yards (NAF 38.32Z, with some 38.11Z collectors) serve industrial B2B clients (metal machining, manufacturing, construction) who generate scrap tracked via weighbridge tickets. Under Art. D. 543-284, every yard must aggregate a year's worth of tickets into an Annexe I-B attestation per client before March 31. This is currently done by hand in spreadsheets, mapping local material names to official categories — labor-intensive, error-prone, and a real compliance risk for both the yard and its clients.

**One correction:** the pressure point is not only "losing accounts to Paprec/Veolia's digital portals" (v1's framing) — it's also that **every yard, regardless of competitive pressure, has a hard legal deadline it must hit**, which is the more universal and provable urgency driver across all 11 real prospects, most of whom are too small to be realistically competing head-to-head with national groups for the same contracts.

---

## 5. The solution — corrected to the real legal layout

ValiWaste AI: a Python + Claude API pipeline that parses weighbridge tickets (PDF/CSV) and generates a conformant Annexe I-B PDF plus a monthly carbon-savings dashboard for B2B clients.

**Corrected field spec** (from the Arrêté du 21 décembre 2021's notice explicative, Cadres 1–6):

| Cadre | Content | Build note |
|---|---|---|
| 1. Émetteur | Issuer identity; for intermediaries, récépissé/prefecture declaration details | — |
| 2. Origine | The producer/holder (one client per attestation) | — |
| 3. Flux | Waste denomination + code; single-flux or mixed-flux checkboxes for the 8 flux | Map local material names to these 8 categories, not 9 |
| 4. Quantités | 4.A received, 4.B sent to valorisation, 4.C valorised directly, 4.D losses — **hard validation rule: 4.B + 4.C = 4.A − 4.D** | Build this balance check into the generator — it's a genuine differentiator a spreadsheet or generic AI tool won't enforce |
| 5. Destinations finales | Per-flux table: installation type, location, **% split that must sum to 100%** | Second built-in validation rule |
| 6. Date/signature | — | Can be electronic |

The law requires reproducing the official **layout**, not just the data — pull the authenticated JORF PDF (JORFTEXT000045084125) before building the template, don't design from the text description alone.

**Biowaste attestations (D. 543-226-2)** should be offered as a clearly separate, optional second product if a client needs it — never merged into the Annexe I-B output.

---

## 6. Revenue impact — reframed to fit the prompt's own kill condition

v1's primary metrics were labor-hour savings and churn defense — cost reduction and revenue *defense*, not revenue *growth*, which the prompt explicitly excludes ("avoid speculative value... avoiding a fine that may never happen" is the same category of claim as "avoiding account loss that may never happen").

**Reframed primary metric:** the monthly B2B Carbon Yield Card is a genuine differentiator independent yards don't otherwise have. The measurable revenue-growth claim is:
- **(a) New account acquisition** — yards can bid for and win B2B contracts specifically because they can now offer standardized carbon/ESG reporting their smaller competitors can't. Measure: count of new or upsold contracts in the 12 months post-launch, with contract value, compared to the prior 12 months' baseline.
- **(b) Average order value** — bundling the carbon dashboard as a paid add-on to existing client relationships, rather than giving it away, raises per-client revenue directly.

Labor savings and churn defense remain real and worth mentioning to the prospect, but should not be the headline "revenue growth" claim in the report or the pitch.

---

## 7. Competitive advantage — updated for a real competitor

**Okapia OS** is a French SaaS tool (€340–890/month) already selling to sorting centres, with weighbridge integration and "attestations de valorisation" — a genuine, not hypothetical, competitor missed in v1's adversarial test.

Key differentiators to lead with:
- Okapia's own materials don't claim strict Annexe I-B layout conformity; ValiWaste AI's built-in mass-balance and 100%-destination validation (§5) is a concrete, demonstrable edge.
- One-time setup fee vs. recurring SaaS subscription — lower commitment for a first sale, consistent with the 14-day fast-payment constraint.
- **Decision needed before scaling past the pilot:** compete directly on price/specialization, or approach Okapia for a partnership/white-label arrangement for the parsing layer. Recommended: decide this *after* the Doubs pilot, using real delivery data to negotiate from strength either way.

---

## 8. Data and first value (unchanged, confirmed sound)

Zero data → 3–5 sample tickets → full batch under pilot agreement. This ladder already complies with the prompt's data principle and needs no correction.

---

## 9. Pilot plan — the real, verified Doubs prospect list

Built by querying the official company registry (recherche-entreprises.api.gouv.fr), fully paginated, filtered to active establishments in Doubs with size band ≤ 249 employees, then triaged to exclude companies with no current Doubs presence, group/legal-entity ownership, ETI/GE size classification, public bodies, and ESS/nonprofit structures (kept as a separate secondary list).

**Real total: 35 companies matched the raw filter; 11 are genuine, independent, currently-active targets.**

| Company | Town | Owner(s) | NAF |
|---|---|---|---|
| Fer Métaux Services (FMS) | Devecey | François Roux, Sébastien Stehly | 38.32Z |
| France Métaux | Audincourt | Jean & Léa Roger | 38.32Z |
| SAS Trifer Recyclage | Miserey-Salines | Olivier Stehly | 38.32Z |
| Sarl Jeanmougin | Mathay | Hervé & Corinne Jeanmougin | 38.32Z |
| MN Recup | Maîche | Maxime & Noël Jacquot | 38.32Z |
| Entreprise Wetzel | Liesle | Sébastien Wetzel | 38.32Z |
| Mickael Varrin | Valentigney | Mickael Varrin | 38.32Z |
| Gipsy Jovanovich (Ferret) | Saint-Vit | Gipsy Jovanovich | 38.32Z |
| Angelique Mourot (Rolland) | Audincourt | Angelique Mourot | 38.32Z |
| Liard Services | Vuillecin | Isabelle & Laurent Liard | 38.11Z |
| Willy Wetzel | Montrond-le-Château | Willy Wetzel | 38.11Z |

**[CORRECTED]** v1's two named examples — Doubs Recyclage and Haut-Doubs Recyclage (Massacrier) — are both confirmed `ETI`-classified and/or group-controlled (Doubs Recyclage is controlled by the E3R holding group). Neither belongs on this list; both are dropped.

**Secondary list (ESS/nonprofit — different buyer profile, optional lower-priority track):** Demain, Envie 2E Franche-Comté, La Recyclerie des Forges, La Ressourcerie, Trivial'Compost.

**Pilot roadmap:** unchanged from v1's day-by-day structure, now pointed at the real 11 names above. Stop/go conditions unchanged.

---

## 10. Host-beneficiary plan — corrected

- **Host:** FEDERREC Centre et Sud-Est.
- **Deal terms:** as v1 (endorsement, newsletter/webinar mentions, discount structure) — unchanged in substance.
- **Correction:** the outreach email and all materials must use the current correct spelling, and cite "~80 member companies (excluding national groups)" rather than the sector-wide 125-establishment figure, when discussing the host's own reach.

---

## 11. Pricing and revenue — recalculated against real prospect counts

Unchanged pricing: €950 one-off setup (50/50 split) + €150/month or €1,800/year recurring.

**Illustrative revenue ranges (labeled as assumption-based, not verified — real conversion only comes from the pilot):**

| Level | Real clean prospect count | At ~50% eventual penetration | Recurring, once saturated |
|---|---|---|---|
| Doubs (pilot) | 11 | ~5–6 customers | ~€800/month |
| Region (Bourgogne-Franche-Comté) | 58 | ~29 customers | ~€4,350/month (~€52k/year) |
| National | 1,223 (real, full count) | even 10% penetration ≈ 120 customers | ~€18,000/month (~€216k/year) |

The national figure changes the opportunity's character from a side-income tool to a real small business — **but reaching it requires solving distribution, not outreach volume**, since no solo operator cold-calls 1,223 companies (see §12).

---

## 12. Execution plan

**Ring 1 — Doubs (now):** Day-by-day plan unchanged from v1 in structure, now pointed at the real 11 names in §9. Target: 2–3 signed pilots within 7 days, first payment within 14.

**Ring 2 — Bourgogne-Franche-Comté (immediately after Ring 1 validates, not "Month 6"):** 58 real prospects, confirmed by department:

| Department | Clean prospects |
|---|---|
| Saône-et-Loire (71) | 14 |
| Doubs (25) — done in Ring 1 | 11 |
| Côte-d'Or (21) | 10 |
| Haute-Saône (70) | 8 |
| Yonne (89) | 8 |
| Jura (39) | 4 |
| Territoire de Belfort (90) | 3 |

**Expand to Saône-et-Loire first, then Côte-d'Or** — in that order, using the same direct-outreach playbook plus the FEDERREC Centre-Sud-Est host relationship secured during Ring 1.

**Ring 3 — National (1,223 real prospects, later, distribution-gated):** This ring cannot be reached by scaling direct outreach — it requires: (a) a repeatable delivery process proven across Ring 1–2 without constant personal involvement, (b) resolving the Okapia OS compete-vs-partner question with real delivery data, (c) building relationships with FEDERREC's other 7 regional syndicates one at a time (there is no single "national FEDERREC" switch), and (d) likely some inbound motion (published case studies, trade press) once Ring 1–2 references exist. Top-prospect-density departments nationally (Bouches-du-Rhône 48, Seine-Saint-Denis 42, Rhône 41, Nord 39) are useful future targets but not reachable with the current distribution model — don't treat raw density as near-term priority.

---

## 13. Timing — corrected

**[CORRECTED]** v1 framed this as "first year of Annexe I-B enforcement." It is not — the first mandatory cycle was January–March 2026, already past. This is the run-up to the **second** cycle (covering 2026 waste, due March 31, 2027).

This is a stronger hook than v1's framing, not a weaker one: every prospect in §9 likely just lived through one rushed, manual Annexe I-B filing season eight months ago. The pitch becomes "you know exactly how painful that was in February — let's not repeat it," grounded in a real, recent, shared experience rather than an abstract future requirement.

Seasonality rule compliance: the recurring monthly carbon-dashboard subscription still provides off-season revenue, independent of the March deadline, satisfying the prompt's seasonality exception.

---

## 14. Adversarial test results — updated

| Attack | Rating | Note |
|---|---|---|
| 1. Existing solutions | **Weakened** [CORRECTED from "Survives"] | Okapia OS is a real, SME-priced competitor. Trackdéchets still confirmed out of scope (hazardous waste only). Differentiation plan in §7. |
| 2. Past failures | Survives | Unchanged — heavy ERP deployments fail on complexity; a lightweight point tool avoids this. |
| 3. Willingness to pay | Survives | Unchanged. |
| 4. Host reality | Survives, with corrected name/membership figure | FEDERREC does form SME-protection partnerships; use the real ~80-member figure, not the sector stat. |
| 5. Revenue proof | Weakened → addressed | Reframed in §6 around account acquisition, not cost savings, to fit the prompt's own revenue-growth definition. |
| 6. Recurring use | Survives | Monthly carbon reporting unchanged. |
| 7. Coming/outdated changes | Survives, corrected | The "first year" framing was stale (see §13); the underlying regulatory tailwind (textiles added, tightening enforcement) still stands. |
| 8. DIY with AI | Survives | Generic AI tools still can't reliably batch-parse varied tickets or enforce the exact legal layout and balance checks. |

**Strongest remaining case against the idea:** distribution past Ring 2 is genuinely unsolved — the national TAM is real, but reaching it requires channel/partnership work this report hasn't validated yet, only sized.

**What this test could not check:** actual conversion rate from pitch to signed pilot (only a completed sale proves demand, per the prompt's own rule); whether Okapia OS would be open to partnership; DOM-TOM-specific regulatory variations for the two overseas departments that appeared in the national top-prospect list.

---

## Verdict

Pursue. The opportunity survives every gate and the adversarial test, with corrections. The pilot plan is unchanged in mechanics, now pointed at a real, verified 11-name list. The growth story beyond Doubs is real and numerically solid (58 regional, 1,223 national, all fully counted, not estimated) — but Ring 3 is explicitly a distribution problem to solve later, not a volume assumption to bank on now.
