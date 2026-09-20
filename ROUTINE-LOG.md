# Routine Log — Winter 2026 / Spring 2027 Internship Tracker

Running log of every automated routine run. Each run reads this log first to avoid re-verifying known-dead links, then does fresh research, updates `build.mjs`, regenerates the spreadsheet, stages application drafts for new fully-verified postings, and commits/pushes.

---

## 2026-09-19 ~19:15 UTC (first logged run)

No prior ROUTINE-LOG.md existed — `build.mjs` already contained a seeded `rows`/`checked` dataset from earlier (unlogged) work, so this run treated that as the baseline and did NOT re-verify any of its existing entries; it began fresh research from that baseline forward.

### What was searched
Three parallel research passes:
1. **Priority re-checks** (per task instructions): GE Aerospace (Lynn, MA) Spring 2027 co-ops, Draper Laboratory (Cambridge, MA), MIT Lincoln Laboratory (Lexington, MA), plus Symbotic and Amazon Robotics re-checks.
2. **Aerospace/defense majors**: RTX/Raytheon/Collins Aerospace/Pratt & Whitney, Lockheed Martin/Sikorsky, Textron/Textron Aviation, GD Electric Boat, Boeing, Northrop Grumman, L3Harris, Leidos, BAE Systems.
3. **Broader manufacturing/robotics/automotive/space sweep**: Boston-area robotics/hardware companies (iRobot, Vicarious Surgical, Desktop Metal/Markforged, Vecna Robotics, Locus Robotics, Boston Dynamics, Berkshire Grey, PTC, Analog Devices), general manufacturing majors (Caterpillar, John Deere, Honeywell, 3M, Rockwell, Parker Hannifin, Eaton, Danaher, Cummins, Stanley Black & Decker), automotive/EV (Rivian, GM, Ford, Stellantis, Lucid), and space/launch (SpaceX, Rocket Lab, Firefly, Sierra Space, Relativity, Anduril).

All candidates were checked against the actual posting URL (company career site/ATS), not aggregator summaries, per the verification bar. Where a site was JS-rendered/bot-protected and couldn't be independently confirmed, entries were added as "Partial —" with an explicit note of what could/couldn't be verified, never silently dropped or silently upgraded.

### Added to `rows` (21 new entries)
- **MIT Lincoln Laboratory** — Microfabrication Industrial Eng Co-Op, Lexington MA — **Yes**, Jan–Aug 2027.
- **Draper Laboratory** (Cambridge, MA) — Systems Engineering Co-Op and Electro-Mechanical Instrument Co-op, Spring 2027 — **Partial** (Workday req pages blocked, confirmed via Draper's own listings page).
- **Amazon Robotics** — Industrial Development Engineer Intern/Co-op 2027, Westborough MA — **Yes** but flagged: shared pipeline for summer/spring/fall, Spring 2027 placement not guaranteed.
- **Anduril Industries** — Winter 2027 Mechanical Engineer Co-op and Winter 2027 Systems Engineer Co-op, **Quincy, MA (Boston metro!)** — **Yes**, confirmed live on Greenhouse.
- **Rivian** — Manufacturing Engineering (Normal, IL) and Design for Reliability (Irvine, CA), both Spring 2027 Co-Op — **Yes**.
- **SpaceX** — Spring 2027 Engineering Internship/Co-op, multiple sites — **Yes**.
- **Rocket Lab** — Mechanical Engineering Intern and Systems Engineering Intern, both Spring 2027, Long Beach CA — **Yes**.
- **Collins Aerospace / Pratt & Whitney / RTX (Collins)** — 5 Winter/Spring 2027 co-ops (Windsor Locks CT, Middletown CT, Winston-Salem NC, Cedar Rapids IA, Jamestown ND) — **Partial** (Workday blocked, confirmed via aggregator mirrors with req IDs and Sept 13–16 2026 posting dates).
- **Northrop Grumman** — 2027 Spring Mechanical Engineering Co-op, Chandler AZ — **Partial**.
- **Boston Dynamics** — Mechanical Engineering Co-Op, Waltham MA — **Partial**.
- **Berkshire Grey** — Spring 2027 Hardware Quality Co-op, Bedford MA — **Partial**.
- **Emerson** — R&D Engineering Co-Op and Project Engineering Co-op, both Spring 2027, PA/MI — **Partial**.

### Added/updated in `checked` (26 entries touched)
- **Corrected two stale exclusions**: Anduril (previously "Summer 2027 only" — a separate Winter 2027 Quincy MA cohort has since opened) and the Tesla/SpaceX/Apple/... group (SpaceX now has a genuine Spring 2027 posting, split out).
- **GE Aerospace (Lynn, MA)**: all previously-known reqs now return "no longer posted" or HTTP 410 — worse than before, no live Spring 2027 Lynn req found.
- **Draper Laboratory**: Sensor Electrical Engineering Co-op and Optics-Physics Sensor Engineering Co-op confirmed live but excluded — discipline mismatch (electrical/optics, not on Hamza's list).
- **Symbotic**: re-confirmed zero internship/co-op postings.
- **Amazon Robotics**: old req 3088739 confirmed dead (404), superseded by new req added to `rows`.
- New exclusions this run: BAE Systems (Nashua NH — Summer 2027 only), Textron Aviation (still can't confirm year), GD Electric Boat (new Spring 2027 cycle likely exists but no verifiable link found), Lockheed Martin/Sikorsky (site migrated, nothing found), L3Harris & Leidos (discipline mismatch — software/EE only), MIT Lincoln Lab's Rapid Prototyping co-op (Fall 2026 only, wrong season), Boston Dynamics' second req (season unstated), Eaton (broken link), Cummins (re-confirmed empty board), and a large batch of manufacturing/robotics/auto companies with no qualifying postings (iRobot, Vicarious Surgical, Desktop Metal/Markforged, Vecna, Locus, PTC, Analog Devices, Caterpillar, John Deere, Honeywell, 3M, GM, Ford, Stellantis, Lucid, Stanley Black & Decker, Rockwell, Parker Hannifin, Danaher (Canada-located), Firefly, Sierra Space, MathWorks, CIRTEC Medical, Relativity Space).

### Staged applications created (9 files, `staged-applications/`)
One per fully-verified ("Yes", not "Partial") new posting: MIT Lincoln Laboratory, Anduril (Mechanical + Systems), Rivian (Manufacturing Eng + Design for Reliability), SpaceX, Rocket Lab (Mechanical + Systems), and Amazon Robotics. Each contains the posting URL, known eligibility notes (citizenship/ITAR where relevant, GPA/enrollment where known), and a checklist of what to verify/prepare — draft only, nothing submitted.

### Spreadsheet regenerated
`npm install xlsx --no-save && node build.mjs` → printed `done`; `.xlsx` file changed (38KB → 65KB, confirmed via `git diff --stat`).

### Worth re-checking next time
- **GD Electric Boat** (Groton, CT) — a new Spring 2027 cycle appears to exist per aggregator evidence, but the official portals (ebcareers.com, careers-gdeb.icims.com) blocked automated fetch — check directly in-browser.
- **Textron Aviation** — "Spring Co-Op – Electronics Modules Engineer" still can't be dated; careers.textron.com remains JS-blocked.
- **Eaton** — Spring 2027 co-op wave exists generally but the specific link died; look for a fresh one.
- **RTX Massachusetts sites** (Andover/Tewksbury/Woburn) — RTX clearly has an active Winter/Spring 2027 co-op wave (5 reqs found this run, none in MA); their own MA-specific search page is JS-rendered and returned nothing — worth trying again.
- **Analog Devices, Sierra Space, Danaher (US site), Caterpillar (next cycle)** — cycles not yet posted per this run's findings; likely to open in the next 4–8 weeks.
- **Amazon Robotics req 10536817** — re-check periodically whether the posting narrows to a specific term, since it's currently a shared summer/spring/fall pipeline.

### ⚠️ Push failure
`git push -u origin master` failed with a 403: **"Claude doesn't have GitHub access to Svvipee/internship-tracker-2026 for your organization."** All of this run's work (build.mjs, the regenerated .xlsx, this log, and 9 staged-application files) is committed locally on `master` (commit `a3018f9`) but has NOT reached GitHub. An org admin needs to install the Claude GitHub App (https://github.com/apps/claude/installations/select_target) or reconnect GitHub from claude.ai settings before the next run's push — and before this run's commit — can land. **The next run should attempt to push this pending local commit before doing new work**, so nothing is lost or duplicated.

---

## 2026-09-20 ~00:49 UTC

### GitHub access resolved
On starting this run, `git status` showed a detached HEAD at commit `82ba943` (the previous run's two commits), while the local `master` branch pointer was still stale at the initial commit. `git fetch origin master` confirmed **origin/master is already at `82ba943`** — the prior run's "push failure" had actually been resolved/superseded and the commits did reach GitHub. Reset local `master` to track `origin/master` and continued from there. No action needed from an admin at this time.

### What was searched
Delegated to a research agent with strict-verification instructions (open the actual posting URL directly, no aggregator-only claims). Two priorities:
1. **Priority re-checks** from the last run's "worth re-checking" list: GD Electric Boat, Textron Aviation, Eaton, RTX Massachusetts sites (Andover/Tewksbury), Analog Devices/Sierra Space/Danaher(US)/Caterpillar next-cycle check, and Amazon Robotics req 10536817's term ambiguity.
2. **Fresh sweep**: additional Boston-area hardware/robotics/aerospace companies not yet checked (Vicor, Teradyne, iRobot, Commonwealth Fusion Systems, Olympus, Alloy Enterprises, Hologic, Vicarious Surgical), plus a broader re-check of GE Aerospace, Draper, MIT Lincoln Lab for any new reqs, and humanoid-robotics companies (Apptronik, Figure AI, Agility Robotics).

### Added to `rows` (5 new entries)
- **Formlabs** — Mechanical Engineering Intern (Winter/Spring 2027), Somerville MA — **Yes**, additional MA req beyond the one already tracked.
- **Formlabs** — Hardware Systems Integration Intern (Winter/Spring 2027), Somerville MA — **Yes**.
- **Eaton** — ETO Engineering Co-op, Syracuse NY, Fall 2026/Spring 2027 — **Yes** (verified via Eaton's own public Eightfold job API directly, since the rendered page is JS-heavy). This resolves last run's "Eaton link died" re-check note with a fresh, different req.
- **Reframe Systems** (new company — modular-construction/robotics-manufacturing startup) — Mechanical Engineer, Spring 2027 Co-op, Andover/Billerica MA — **Yes** (verified via Ashby's own public job-board API directly). Strong Boston-area fit.
- **General Dynamics Electric Boat** — 2027 Spring Engineering CO-OP Trainee, Groton CT — **Partial** (found via GD's own dedicated recruiting site with a specific req ID, but the page itself is behind a Cloudflare bot-check wall that blocked every fetch method tried).

### Updated in `rows`
- **Amazon Robotics** (req 10536817) — posting text now explicitly reads "...summer intern, spring co-op, and fall co-op roles," confirming Spring 2027 co-op is one of the covered terms (previously flagged as an ambiguous shared pipeline). Noted in the row's "Link Verified" field rather than re-added.

### Added to `checked` (13 entries)
Textron Aviation (no change, still unverifiable — SPA confirmed, aggregator mirror is stale 2024 data), RTX Massachusetts sites (no qualifying co-op, only Summer 2027 internship and full-time roles), Analog Devices/Sierra Space/Danaher(US)/Caterpillar (no change, next cycle not open yet), Olympus (2026 cohort closed, 2027 unverifiable), Alloy Enterprises (only Fall/Spring 2026), Commonwealth Fusion Systems (zero co-op postings on live board), GE Aerospace (two more specific reqs re-confirmed dead), Teradyne (only Spring 2026), Vicor (no co-ops at all), Hologic (only Spring 2026, one page 503'd), iRobot (nothing current), Vicarious Surgical (nothing current), Apptronik/Figure AI/Agility Robotics (no qualifying postings; one apparent Figure AI lead turned out to be Summer 2026 and closed).

### Staged applications created (4 files, `staged-applications/`)
One per fully-verified ("Yes", not "Partial") new posting: Formlabs (Mechanical Engineering Intern), Formlabs (Hardware Systems Integration Intern), Eaton (ETO Engineering Co-op), Reframe Systems (Mechanical Engineer Co-op). GD Electric Boat was NOT staged since it's Partial only.

### Spreadsheet regenerated
`npm install xlsx --no-save && node build.mjs` → printed `done`; `.xlsx` file changed (65KB → 74.5KB, confirmed via `git diff --stat`).

### Worth re-checking next time
- **GD Electric Boat req 601496955** — now have a specific req ID and it's on GD's own recruiting domain, but Cloudflare bot-check blocks every automated verification method. Worth trying to open directly in-browser to confirm live/open status and full discipline breakdown.
- **Textron Aviation** — still fully unverifiable (JS SPA); the aggregator mirror found is stale (2024). Probably not worth further automated attempts unless a first-party listings page (not the SPA search) can be found.
- **RTX Massachusetts sites (Andover/Tewksbury/Woburn)** — still nothing MA-specific found across two runs; likely deprioritize unless a new req appears.
- **Olympus (Westborough, MA)** — a "Jan–June 2027" Manufacturing Engineering Co-Op may exist per aggregator text but couldn't be independently confirmed; worth a direct in-browser check.
- **MIT Lincoln Laboratory** — confirmed the already-tracked Microfabrication Industrial Eng Co-Op has what looks like a sibling/refreshed req (careers.ll.mit.edu/job/Lexington-Group-08-35-Microfabrication-Engineering-Co-Op-Microelectronics-Laboratory-Jan-Aug-2027-MA-02420/1368363000/) — likely the same underlying role, not re-added to avoid duplication, but worth a look if the original req URL ever goes dead.
- **Analog Devices, Sierra Space, Danaher (US), Caterpillar** — still expected to open their Spring 2027 cycles in the coming weeks; keep checking periodically.

---

## 2026-09-20 ~06:57 UTC

### Sync
`git fetch`/`git pull origin master` confirmed local was 3 commits behind (still on the initial-commit `master` pointer while `origin/master` had advanced through the two prior routine commits). Fast-forwarded cleanly, no conflicts. No push-access issues this run.

### What was searched
Delegated to a research agent with the strict-verification instructions. Priorities:
1. Follow-ups from the last run's "worth re-checking" list: GD Electric Boat (req 601496955, still Cloudflare-blocked), Analog Devices, Caterpillar, Olympus (Jan–June 2027 claim), GE Aerospace (any new req), Draper Laboratory and MIT Lincoln Laboratory (any new reqs beyond what's tracked).
2. Fresh sweep of additional aerospace/mechanical/robotics employers not yet checked: Zipline, Astranis, Curtiss-Wright, Sierra Nevada Corporation, Redwire Space, Karman Space, Joby Aviation, Honeywell Aerospace, Moog, Woodward, Firefly Aerospace, Impulse Space, Virgin Galactic, Vecna Robotics, Desktop Metal/Markforged, Boston Dynamics AI Institute, plus re-checks of Boston Dynamics, Commonwealth Fusion Systems, Relativity Space, and L3Harris.

### Added to `rows` (1 new entry)
- **Zipline** — Mechanical Engineer Intern, Spring 2027, South San Francisco CA (or Dallas TX) — **Partial**: exact title and "Spring 2027" wording confirmed via direct fetch of the actual zipline.com posting, but the page is JS-rendered so the Apply button/open status couldn't be independently confirmed from the fetch alone; corroborated as currently listed by two other independent sources. Not staged as an application draft since it's Partial, not fully verified, per the routine's rule (staging is for fully-verified postings only).

### Added to `checked` (18 entries)
GE Aerospace (all 4 known reqs re-confirmed dead — 410/"no longer posted"/EXPIRED), Analog Devices (still not posted), Caterpillar (Summer 2027 reqs only), Olympus (Jan–June 2026 cohort confirmed closed; no real "Jan–June 2027" URL exists — a prior aggregator claim of one looks like a synthesis artifact, not a real posting), Draper Laboratory (5 additional reqs checked: 2 wrong-discipline, 1 Summer, 2 with no stated season), MIT Lincoln Laboratory (3 more cycles checked, all past/wrong-season, nothing new in the Spring 2027 window), Boston Dynamics (a possibly-distinct req R2495 couldn't be verified — Workday returned empty content twice), Commonwealth Fusion Systems (Fall 2026 co-op posting now 404s), Relativity Space (Boston, MA listing appears part of the Summer 2027 wave, not confirmed otherwise), Astranis (near miss — verified live/open but season is literally "Winter 2027", outside the Winter 2026/Spring 2027 target), L3Harris (2 mechanical co-op reqs both dead), Curtiss-Wright (new company — no year stated, fetch blocked 403), Sierra Nevada Corporation (Summer 2027 only), Redwire Space/Karman Space (season unverifiable — rate-limited/no content), a 10-company batch with nothing found (Joby Aviation, Honeywell Aerospace, Moog, Woodward, Firefly Aerospace, Impulse Space, Virgin Galactic, Vecna Robotics, Desktop Metal/Markforged, Boston Dynamics AI Institute), and GD Electric Boat (still Cloudflare-blocked even via a text-proxy workaround — status in `rows` unchanged at Partial).

### Spreadsheet regenerated
`npm install xlsx --no-save && node build.mjs` → printed `done`; `.xlsx` file changed (74.5KB → 82.8KB, confirmed via `git diff --stat`).

### Staged applications
None created this run — the only new posting (Zipline) is Partial, not fully verified, so per the routine's rule it wasn't staged.

### Worth re-checking next time
- **GD Electric Boat req 601496955** — three runs in a row now blocked by Cloudflare on jobs.buildsubmarines.com; automated methods (direct fetch, text-proxy) have been exhausted — probably needs an actual in-browser check to resolve from Partial to Yes or confirm dead.
- **Boston Dynamics req R2495** — search snippet suggests a possibly-distinct Spring 2027 Mechanical Engineering Intern (Atlas program) beyond the already-tracked R2476, but Workday fetch returned empty content twice. Worth a direct in-browser check.
- **Relativity Space (Boston, MA listing)** — part of a likely-Summer-2027 wave overall, but the specific Boston, MA req wasn't individually fetched — worth a closer direct check.
- **Curtiss-Wright JR1907** — "Co-op (Spring Term)" with no year stated; fetch blocked 403 — worth a retry.
- **Redwire Space / Karman Space** — candidate mechanical/aerospace intern roles exist but season unverified due to rate-limiting/fetch issues — worth another attempt.
- **Draper Laboratory JR002688 (Acoustic and Vibration Technologies Co-op) and JR002717 (Metrology Co-op)** — both open/rolling with no season stated; check periodically for a dated Spring 2027 version.
- **Astranis** — confirmed live "Winter 2027" (not Winter 2026/Spring 2027) Mechanical Engineer Intern; flagged as a near-miss in case Hamza wants to reconsider the season window, not re-checked otherwise.
- **Analog Devices, Caterpillar** — still expected to open Winter 2026/Spring 2027 cycles in the coming weeks (Analog Devices' next wave reportedly ~Oct/Nov 2026); keep checking periodically.

---

## 2026-09-20 ~13:00 UTC

### Sync
`git fetch origin master` confirmed local (detached HEAD at `f4a1a04`) matches `origin/master` exactly — no divergence, no pull needed. No push-access issues this run.

### What was searched
Delegated to a research agent with the strict-verification instructions. Two priorities:
1. **Follow-ups from the last run's "worth re-checking" list**: GD Electric Boat (req 601496955, still Cloudflare-blocked), Boston Dynamics req R2495, Relativity Space's Boston MA listing, Curtiss-Wright JR1907, Redwire Space/Karman Space, Draper JR002688/JR002717, Analog Devices, Caterpillar.
2. **Fresh sweep**: Toyota Research Institute, Textron Systems (Wilmington MA — distinct from Textron Aviation), Thermo Fisher Scientific, Waters Corporation, Bose, Instron, Analogic, Form Energy, Boston Metal, Sublime Systems, Sanofi/Genzyme, Charles River Labs, Applied Materials, KLA, Lam Research, Intuitive Machines, Hexagon Manufacturing Intelligence, GE HealthCare, Philips, Waymo, Aurora Flight Sciences, Terex, Oshkosh, Polaris.

### Added to `rows` (2 new entries)
- **Applied Materials** — 2027 Spring Mechanical Engineer Co-op, **Gloucester, MA (Boston metro!)**, req R2628290 — **Partial** (Workday blocked, confirmed via a dreamworkhq aggregator mirror quoting exact title/season/location/pay/req ID).
- **Sanofi (Genzyme)** — 2027 Spring Co-Op Opportunities, **Framingham, MA (Boston metro!)** — **Yes**, fetched directly, live, closes Nov 14, 2026. Biopharma manufacturing/process engineering (MSAT) umbrella posting, not classic mechanical — flagged as a discipline caveat in the row's Discipline field.

### Not added — deduped
- An RTX Cedar Rapids IA "Mechanical Engineering Co-op (Winter/Spring 2027)" req (01869080) surfaced in the fresh sweep but is identical to the RTX Cedar Rapids IA row already tracked from a prior run — logged in `checked` as a dedupe note, not double-counted.

### Added/updated in `checked` (21 entries)
Resolved/updated priority threads: GD Electric Boat (4th consecutive Cloudflare block, deprioritizing further automated attempts), Boston Dynamics R2495 (season still unconfirmed; also ruled out an unrelated same-titled Summer 2026 posting as a naming collision), Relativity Space (Boston MA listing no longer live), Curtiss-Wright JR1907 (posting still doesn't state a year — inference isn't enough to pass the verification bar), Redwire Space (Summer-only), Karman Space & Defense (Summer-only by program design), Draper JR002688/JR002717 (still no season stated, no change), Analog Devices (no change), Caterpillar (prior req dead, new "Parallel Co-op Program" doesn't cleanly fit a discrete term and has no MA location).
New exclusions from the fresh sweep: Toyota Research Institute (ML/AI roles, wrong location/discipline), a 5-company "nothing found" batch (Waters Corporation, Instron, Analogic, Boston Metal, Charles River Labs), Bose (only stale/dead links), Thermo Fisher Scientific (Summer 2027 season / wrong location), Philips (only 2025 postings), a 5-company Summer-only batch (Hexagon Manufacturing Intelligence, Oshkosh, Terex, Polaris, Waymo), Sublime Systems (zero open roles, confirmed via direct fetch), Lam Research (2027 cycle not yet posted).
Left unresolved (not excluded outright, flagged for follow-up): Textron Systems Wilmington MA (Taleo page wouldn't render real content), Aurora Flight Sciences (no dated listing found, only a generic description), GE HealthCare (zapply snippet couldn't be corroborated with real page content).

### Staged applications created (1 file, `staged-applications/`)
`sanofi-genzyme-spring-2027-coop.md` — the only fully-verified ("Yes") new posting this run. Applied Materials was NOT staged since it's Partial only.

### Spreadsheet regenerated
`npm install xlsx --no-save && node build.mjs` → printed `done`; `.xlsx` file changed (82.8KB → 94.6KB, confirmed via `git diff --stat`).

### Worth re-checking next time
- **Textron Systems (Wilmington, MA)** — "2027 Intern - Materials Quality Engineer (Weapons)" title exists but the Taleo posting page returns only template placeholders; needs a direct in-browser check to get season/pay/status.
- **Aurora Flight Sciences (Boeing subsidiary)** — company materials mention MA-based mechanical/autonomy engineering work generally; no specific dated 2027 co-op req found yet — worth checking careers.aurora.aero directly.
- **GE HealthCare** — "LSS Mechanical Engineering Co-op" title surfaced via zapply but the actual page returned unrelated content twice; try a direct careers.gehealthcare.com search instead.
- **Lam Research** — 2027 mechanical engineering intern cycle not yet posted as of this run; likely opens in the coming weeks.
- **GD Electric Boat req 601496955** — now blocked by Cloudflare on 4 consecutive runs; deprioritizing further automated fetch attempts — would need an actual in-browser check.
- **Boston Dynamics req R2495** — season still unconfirmed after 3 attempts; worth one more try with a different fetch approach, or otherwise treat as a dead end.
- **GE Aerospace, Analog Devices, Caterpillar** — all still expected to open new Winter 2026/Spring 2027 cycles in the coming weeks; keep checking periodically.

---

## 2026-09-20 ~19:00 UTC

### Sync
`git fetch origin master` confirmed local matched `origin/master` exactly at `e2131cd` (no divergence). Created/reset local `master` branch tracking `origin/master`. No push-access issues at sync time.

### What was searched
Delegated to a research agent with the strict-verification instructions. Two priorities:
1. **Follow-ups from the last run's "worth re-checking" list**: GD Electric Boat (req 601496955, Cloudflare-blocked for 4 straight runs), Boston Dynamics req R2495, Textron Systems Materials Quality Engineer intern, Aurora Flight Sciences, GE HealthCare LSS Mechanical Eng Co-op, Lam Research/Analog Devices/Caterpillar, GE Aerospace (any new Spring 2027 req), Draper JR002688/JR002717, MIT Lincoln Laboratory (any new reqs).
2. **Fresh sweep**: nuclear/energy/industrial (Westinghouse, GE Vernova, NuScale, Commonwealth Fusion re-check), medical device/robotics (Intuitive Surgical, Stryker, Insulet), defense/aerospace (Kratos, HII/Newport News, Parsons), Boston-area robotics not yet checked (Realtime Robotics, Piaggio Fast Forward, Diligent Robotics, Veo Robotics), semiconductor/precision manufacturing (MKS Instruments, Coherent/II-VI), automotive/EV distressed companies (Fisker, Canoo, Nikola, VinFast, Karma).

### Major finding — Boston Dynamics R2476 confirmed dead
Queried Boston Dynamics' live Workday CXS jobs API directly for all open reqs: all 37 current postings are `workerSubType: "Regular"` — **zero Intern/Co-Op postings exist company-wide right now.** The previously-tracked "Mechanical Engineering Co-Op" (req R2476) is no longer live. **Moved from `rows` to `checked`.**

### Upgraded from Partial to Yes
- **Draper Laboratory — Systems Engineering Co-Op (Spring 2027, JR002882)** and **Electro-Mechanical Instrument Co-op (Spring 2027, JR002883-1)** — both previously tracked as Partial (Workday page blocked). This run's agent successfully fetched both directly via Draper's Workday CXS job API (title, description, pay range all confirmed) — upgraded to fully verified.

### Added to `rows` (13 new entries)
- **GE Aerospace — Engines Engineering Co-op – US – Spring 2027** (R5029617-1), Lynn, MA or Evendale, OH — **Yes**. First live GE Aerospace Spring 2027 req found after 4 prior runs found only dead/expired reqs; Lynn, MA option is a Boston-metro fit.
- **GE Aerospace — Structures Intern/Co-op – ACSC – Spring 2027** (R5039588-1), Cincinnati, OH — **Yes**.
- **Insulet — Co-op, R&D Mechanical Engineering** (REQ-2026-18007), Acton, MA — **Yes**. Strong Boston-metro fit (medical device manufacturer, ~25 mi).
- **Insulet — Co-op, Manufacturing Engineering** (REQ-2026-18078), Acton, MA — **Yes**.
- **Insulet — Co-op, Systems Engineering** (REQ-2026-18061), Acton, MA — **Yes**.
- **Insulet — Co-op, Mechanical Lifecycle** (REQ-2026-18155), Acton, MA — **Partial** (confirmed live via Insulet's own Workday jobs-search API call, full description not individually opened).
- **Insulet — Co-op, R&D Manufacturing** (REQ-2026-18069), Acton, MA — **Partial** (same basis).
- **Insulet — Graduate Co-op, Manufacturing Engineering** (REQ-2026-18086), Acton, MA — **Partial** (same basis; confirm undergrad eligibility).
- **Insulet — Co-op, Supplier Development Engineering - Mechanical** (REQ-2026-18209), Acton, MA — **Partial** (URL sourced from a Dreamwork aggregator mirror quoting Insulet's own Workday link directly, since the live Workday page returned blank to direct fetch).
- **Insulet — Co-op, Systems Engineering - Design Verification** (REQ-2026-18144-1), Acton, MA — **Partial** (same aggregator-sourced-URL basis).
- **Insulet — Co-op, Life Cycle Engineering - Systems** (REQ-2026-18149), Acton, MA — **Partial** (same aggregator-sourced-URL basis).
- **GE HealthCare — Infant Care V&V Engineering Co-op - Spring 2027** (R4046324-1), Waukesha, WI — **Yes**. Accepts Mechanical/Electrical/Computer/Biomedical majors; V&V/test focus, not Boston-area.
- **GE Vernova — Nuclear Engineering Co-Op/Intern - Spring 2027** (R5048552), Wilmington, NC — **Yes**. Nuclear/Industrial Engineering, not Boston-area.

A 4th Insulet req found by the research agent — "Co-op, Next Gen Platforms (NGP) Systems Engineering" (REQ-2026-18071) — was investigated but **not added**: no source yielded a verifiable canonical Insulet Workday deep-link URL (unlike its siblings above), so per the no-fabricated-URLs rule it was logged to `checked` instead rather than including a guessed link.

### Added to `checked` (22 entries)
Boston Dynamics R2476 (moved from `rows`, confirmed dead — see above), Insulet NGP Systems Engineering (title/season/pay corroborated by two aggregators but no verifiable URL found), Draper Sensor Electrical Eng Co-op JR002885 (re-confirmed live but discipline mismatch, no change), Textron Systems Materials Quality Engineer intern (Taleo page now loads real content — Wilmington MA, Full-time Internship/Co-Op, posted 09/01/2026, requires US Citizenship for classified access — but still never states a season, so still excluded), Aurora Flight Sciences (still unverifiable, client-rendered Taleo board), GE HealthCare LSS Mechanical Eng Co-op R4046267-1 Madison WI (zero season language, wrong location, excluded — distinct from the Waukesha WI req that WAS added), MKS Instruments Andover MA (zero matching Workday reqs — "Spring 2027" reference was a stale aggregator artifact), Lam Research (2027 cycle still not posted), Analog Devices/Caterpillar/Commonwealth Fusion Systems (consolidated no-change re-check), and a 13-company fresh-sweep batch with nothing found (Westinghouse Electric, NuScale Power, Intuitive Surgical, Stryker, Kratos Defense, HII/Newport News Shipbuilding, Parsons Corporation, Realtime Robotics, Piaggio Fast Forward, Diligent Robotics, Veo Robotics, Coherent/II-VI, and a Fisker/Canoo/Nikola/VinFast/Karma Automotive group excluded partly due to several companies' financial distress).

### Staged applications created (9 files, `staged-applications/`)
One per fully-verified ("Yes") new/upgraded posting: Draper Systems Engineering Co-Op, Draper Electro-Mechanical Instrument Co-op (both upgraded from Partial this run), GE Aerospace Engines Engineering Co-op, GE Aerospace Structures Intern/Co-op, Insulet R&D Mechanical Engineering, Insulet Manufacturing Engineering, Insulet Systems Engineering, GE HealthCare Infant Care V&V Engineering Co-op, GE Vernova Nuclear Engineering Co-Op/Intern. The 7 Partial-verified Insulet sibling reqs were NOT staged, consistent with the routine's rule.

### Spreadsheet regenerated
`npm install xlsx --no-save && node build.mjs` → printed `done`; `.xlsx` file changed (94.6KB → 114.2KB, confirmed via `git diff --stat`). Sheet row counts: 60 in "Winter26-Spring27 Internships", 108 in "Checked - Not Included".

### Worth re-checking next time
- **Insulet — NGP Systems Engineering Co-op** (REQ-2026-18071, Jan-June 2027) — title/season/pay confirmed by two aggregators, but no source gave a working canonical URL. Also note a *separate* Insulet req exists for "NGP Systems Engineering Co-op (July-Dec 2026)" — different season, don't conflate the two. Worth a direct in-browser check to get the Jan-June 2027 req's real link.
- **GD Electric Boat req 601496955** — not re-attempted this run (previously deprioritized after 4 straight Cloudflare blocks); still Partial in `rows`, still needs an in-browser check to resolve.
- **Textron Systems Materials Quality Engineer intern** (req 1539632) — page finally loads real content, but the season is genuinely never stated on the posting itself; may need a recruiter/portal follow-up rather than another fetch attempt.
- **GE Aerospace** — first live Spring 2027 req found in 5 runs (Engines Eng Co-op, Lynn/Evendale); worth checking careers.geaerospace.com again soon in case more reqs open in this same wave, especially Lynn, MA-specific ones.
- **Analog Devices, Caterpillar, Lam Research** — still not posted; keep checking periodically (recurring note across multiple runs now).
- **HII/Newport News Shipbuilding** — per their own stated cadence, Spring co-op postings open "September through October" — check again in ~2-4 weeks.
