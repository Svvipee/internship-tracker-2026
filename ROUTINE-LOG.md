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

---

## 2026-09-21 ~01:00 UTC

### Sync
`git fetch origin master` confirmed local (detached HEAD at `030fc5b`) matched `origin/master` exactly. Reset local `master` to track `origin/master`. No push-access issues at sync time.

### What was searched
Delegated to a research agent with the strict-verification instructions. Two priorities:
1. **Follow-ups from the last run's "worth re-checking" list**: Insulet NGP Systems Engineering Co-op (REQ-2026-18071, still needed a working URL), GD Electric Boat req 601496955 (5th consecutive Cloudflare block attempt), Textron Systems Materials Quality Engineer intern (req 1539632, season still unstated), GE Aerospace (any new Lynn/Spring 2027 reqs), Analog Devices/Caterpillar/Lam Research, HII/Newport News Shipbuilding, Draper JR002688/JR002717, MIT Lincoln Laboratory (any new reqs).
2. **Fresh sweep**: Beta Technologies, Archer Aviation, Wisk Aero, Mercury Systems, Cognex, Abiomed, Haemonetics, Vertex Pharmaceuticals, Moderna, American Superconductor, Machina Labs, Hadrian, ICON, Divergent3D, Leonardo DRS, Elbit Systems, Saab, Mercury Marine, Illumina, 10x Genomics, and others.

Note: the agent's exclude-list briefing accidentally omitted Formlabs (already fully tracked from a prior run) — the agent independently flagged it as unfamiliar rather than blindly re-adding it; verified against `build.mjs` and confirmed it's a pre-existing duplicate, no action taken.

### Added to `rows` (3 new entries, all Partial)
- **Leonardo DRS** — Mechanical Engineer Co-Op (Spring 2027), Bridgeton, MO — **Partial** (LinkedIn + Workopia mirror only; Leonardo DRS's own careers site not independently opened for this req). New company, first Leonardo DRS posting tracked.
- **Insulet** — Co-op, Next Gen Platforms (NGP) Systems Engineering (Onsite), REQ-2026-18071, Acton MA — **Partial** (two aggregator mirrors, Workopia and Zapply, now corroborate the exact canonical Workday URL; official Workday page still returns empty on direct fetch after 3 runs). Resolves the "no verifiable URL" blocker flagged in the last 2 runs — moved out of `checked` into `rows`.
- **Moderna** — Co-Op, Applied Technologies (Spring 2027), Norwood MA (~14 mi, Boston metro) — **Partial** (full content confirmed directly via a biospace.com job-board mirror; Moderna's own Workday page returned empty). Discipline caveat noted (automation/bioprocess engineering, not classic mechanical) — same treatment as the existing Sanofi/Genzyme row.

### Not added — discipline mismatch or already tracked (important correction)
The research agent initially reported "Draper — Sensor Electrical Engineering Co-op (JR002885)" and "Draper — Optics-Physics Sensor Engineering Co-op (JR002884)" as new verified findings, and "Insulet — Co-op, Systems Engineering (REQ-2026-18061)" as new. **Cross-checked against `build.mjs` before editing: all three were already accounted for** — the two Draper reqs have been correctly excluded for discipline mismatch (electrical/optics, not on Hamza's list) across 3 prior runs, and REQ-2026-18061 was already added to `rows` as Yes in the 2026-09-20 ~19:00 UTC run. None were re-added or duplicated. Also not added: Draper Systems Engineering Co-Op (JR002882) and Electro-Mechanical Instrument Co-op (JR002883-1) — the agent reported these as still-Partial (couldn't re-fetch the Workday page this run), but both were already upgraded to fully-verified "Yes" in the 2026-09-20 ~19:00 UTC run via a successful direct fetch; that earlier direct confirmation stands and they were left unchanged at Yes.

### Updated in `checked`
- **Textron Systems req 1539632** ("2027 Intern - Materials Quality Engineer (Weapons)") — **RESOLVED**: a proxy fetch this run finally returned the full posting body, which explicitly states "Paid, full-time 10-week summer internship," deadline Oct 31 2026. Confirmed Summer 2027 (wrong season) — reason text updated to reflect this, supersedes the prior "season never stated" notes across 3 runs.
- Removed the old Insulet REQ-2026-18071 `checked` exclusion entry (superseded — now in `rows` as Partial, see above).

### Added to `checked` (19 new entries)
GE Aerospace Lynn trade/software reqs (discipline mismatch), MIT Lincoln Lab Cyber Security Co-op (discipline mismatch), Moderna CMC Development (aggregator-only, unconfirmed canonical URL — weaker discipline fit than the Applied Technologies req that WAS added), and a fresh-sweep batch with nothing qualifying found: Beta Technologies, Archer Aviation, Wisk Aero, Mercury Systems, Cognex, Abiomed, Haemonetics, Vertex Pharmaceuticals, Elbit Systems of America, Saab Inc, Divergent3D, Emerson/National Instruments, Mercury Marine, Illumina, 10x Genomics, American Superconductor, and a 9-company "nothing found" group (Hadrian, Machina Labs, ICON, Boston Engineering, Bruker, Zeiss Industrial Metrology, Nikon Metrology, Overair, Form Energy).

### Priority re-check outcomes (no `rows`/`checked` change needed)
- **GD Electric Boat req 601496955** — still Cloudflare-blocked on the 5th consecutive run (direct fetch, proxy, and search-cache methods all failed). Status unchanged at Partial in `rows`.
- **Analog Devices, Caterpillar, Lam Research** — still nothing posted for the Winter2026/Spring2027 cycle; Caterpillar's engineering internship program confirmed Summer-only by design.
- **HII/Newport News Shipbuilding** — company states Spring postings go up "September through October" (i.e. now) but nothing indexed/live yet — likely not posted yet, re-check in 1-2 weeks.
- **Draper JR002688/JR002717** — still no season stated; deprioritizing further checks now that the company's actively-dated Spring 2027 reqs (JR002882-JR002885) are all tracked.

### Staged applications
None created this run — all 3 new postings are Partial, not fully verified, so per the routine's rule none were staged.

### Spreadsheet regenerated
`npm install xlsx --no-save && node build.mjs` → printed `done`; `.xlsx` file changed (114.2KB → 124.5KB, confirmed via `git diff --stat`). Current totals: 63 rows in "Winter26-Spring27 Internships", 127 rows in "Checked - Not Included".

### Worth re-checking next time
- **GD Electric Boat req 601496955** — 5 consecutive Cloudflare blocks; consider trying a Wayback Machine/archive.org snapshot next run instead of live fetch.
- **Insulet REQ-2026-18071 and the Leonardo DRS/Moderna Partial entries** — all three new Partial rows this run were verified only via aggregator/third-party mirrors, not the employer's own page directly rendering; worth a follow-up direct-fetch attempt each to upgrade to Yes.
- **Saab "Systems Engineering Co-Op (Spring - Summer 2027)"** (East Syracuse, NY) — near-miss on season clarity, worth a direct fetch attempt to pin down the exact start date.
- **Beta Technologies** — "2026-2027" program season labeling is ambiguous; worth checking specific team/track postings for a dated Spring 2027 version.
- **Moderna CMC Development co-op** — aggregator-only, unconfirmed canonical URL; worth a direct fetch retry.
- **HII/Newport News Shipbuilding** — re-check in 1-2 weeks per their own stated posting cadence.
- **Analog Devices, Lam Research** — cycles still not open, recurring note across many runs now.

---

## 2026-09-21 ~07:00 UTC

### Sync
`git status` initially showed a detached HEAD; `git fetch origin master` confirmed local matched `origin/master` exactly at `cd10a56` (7 commits ahead of the stale local `master` branch pointer). Checked out and fast-forwarded `master` cleanly. No push-access issues at sync time.

### What was searched
Delegated to a research agent with the strict-verification instructions. Two priorities:
1. **Follow-ups from the last run's "worth re-checking" list**: GD Electric Boat req 601496955 (Cloudflare-blocked 5 runs straight — tried Wayback Machine this time), the three Partial entries added last run (Leonardo DRS, Insulet REQ-2026-18071, Moderna Applied Technologies Co-Op) — attempted direct-fetch upgrades on the employer's own page, Saab Systems Engineering Co-Op season wording, HII/Newport News Shipbuilding, Analog Devices/Lam Research/Caterpillar, GE Aerospace (any new Lynn, MA reqs).
2. **Fresh sweep**: Vicor, Nuvation, BAE Systems (Merrimack NH), Textron Systems, Sig Sauer, Smith & Wesson, iRobot (re-check), Desktop Metal, MathWorks, Waters Corp, Analogic, Charles River Labs, Vertex Pharmaceuticals, National Grid/Eversource, MassDOT, Raytheon BBN, plus re-checks of Blue Origin/SpaceX/Anduril for additional reqs and Joby/Archer/Firefly/Virgin Galactic for a dated Spring 2027 posting.

### Upgraded from Partial to Yes (3 entries)
- **Leonardo DRS — Mechanical Engineer Co-Op (Spring 2027)**, Bridgeton MO — now confirmed via direct fetch of Leonardo DRS's own careers.leonardodrs.com ATS (job ID 115172), replacing the prior LinkedIn/Workopia-mirror basis.
- **Insulet — Co-op, NGP Systems Engineering (Onsite)** (REQ-2026-18071), Acton MA — now confirmed via direct fetch of Insulet's own Workday CXS job API, replacing the prior aggregator-mirror basis. Pay ($25–34/hr) and deadline (2026-12-31) added.
- **Moderna — Co-Op, Applied Technologies (Spring 2027)**, Norwood MA — now confirmed via direct fetch of Moderna's own Workday CXS job API under req R19735, replacing the prior biospace.com-mirror basis. Note: R19735 is a different req number than the mirror's job ID (3072468); judged very likely the same underlying posting referenced by two different sites, not a separate role — flagged for a quick sanity check next run rather than treated as certain.

### Added to `checked` (8 entries)
BAE Systems (Merrimack, NH — no matching mechanical/systems co-op, the only Spring/Summer 2027 co-op found is in Cedar Rapids IA), Sig Sauer (only an EE/CE-discipline Spring 2027 posting, no mechanical match), Textron Systems Wilmington MA fresh sweep (the only "2027 Intern - Mechanical Engineer" found is at Howe & Howe/Waterboro ME, a different site/subsidiary — not a Wilmington match), Raytheon BBN (no mechanical/systems co-op, BBN skews AI/computing), Eversource (season reads as Summer despite "2027" branding), National Grid (nothing found), MassDOT (co-op/internship programs run Fall/Summer only by design, also civil-engineering-focused), GE Aerospace Applied AI Engineer Co-op — Lynn MA area (discipline mismatch, software/AI not mechanical).

### Flagged but NOT added (judgment call, not excluded outright)
- **Saab Inc — Systems Engineering Co-Op**, East Syracuse NY — exact wording pinned down via direct fetch as **"Spring - Summer 2027"** (a single combined term, not a clean Winter/Spring-only co-op). Judged closer to the common Summer 2027 wave than to a genuine Fall-through-Spring term, so it was logged to `checked` with the exact wording rather than added to `rows` — Hamza may want to reconsider this call himself since it's a genuinely borderline case.

### Priority re-check outcomes (no `rows`/`checked` change)
- **GD Electric Boat req 601496955** — Wayback Machine has **no archived snapshot** of the URL; direct fetch, proxy, and search-cache all still Cloudflare-blocked. 6th consecutive run unresolved — status unchanged at Partial in `rows`. Recommend deprioritizing further automated attempts; this needs a human in-browser check.
- **HII/Newport News Shipbuilding, Analog Devices, Lam Research, Caterpillar** — no change, still not posted for the Winter 2026/Spring 2027 cycle.
- **iRobot** — re-confirmed no current postings (live careers search returns 0 results for "mechanical intern"); no change to existing `checked` entry.
- **Joby Aviation, Archer Aviation, Firefly Aerospace, Virgin Galactic** — re-checked, no new findings; these were already covered by existing `checked` entries from prior runs, so no new entries were added (avoiding duplication).

### Not added — unresolved, worth a follow-up (not in `checked`, since not conclusively ruled out)
- **Vertex Pharmaceuticals** — company confirms it runs summer and winter co-op programs generally, but the intern-specific Workday portal (`vrtx.wd5.myworkdayjobs.com/vertex_intern`) returned HTTP 500 on direct fetch; no specific dated req could be found or ruled out this pass.
- **Anduril Industries — "Manufacturing Co-Op" / "Winter 2027 Manufacturing Engineer Co-op"** (Quincy/Lexington, MA) — appears to exist and be in-discipline/in-season per search snippets, but not independently direct-fetched from the live Greenhouse page this pass — worth a follow-up direct fetch before adding.

### Staged applications created (3 files, `staged-applications/`)
One per newly fully-verified ("Yes") posting this run: `leonardo-drs-mechanical-engineer-coop.md`, `insulet-ngp-systems-engineering-coop.md`, `moderna-applied-technologies-coop.md`.

### Spreadsheet regenerated
`npm install xlsx --no-save && node build.mjs` → printed `done`; `.xlsx` file changed (124.5KB → 128.2KB, confirmed via `git diff --stat`).

### Worth re-checking next time
- **GD Electric Boat req 601496955** — 6 consecutive automated-verification failures (direct fetch, proxy, search-cache, Wayback Machine); recommend a human in-browser check rather than further automated attempts.
- **Vertex Pharmaceuticals** — retry the intern Workday portal (500 error this pass) or find an alternate canonical URL.
- **Anduril "Manufacturing Co-Op" (Quincy/Lexington, MA)** — worth a direct-fetch follow-up to confirm season/discipline fit before adding to `rows`.
- **Moderna req R19735 vs. biospace mirror job 3072468** — confirm these are the same posting (very likely) rather than two separate reqs, next time either source is touched.
- **Saab "Spring - Summer 2027" Systems Engineering Co-Op** — Hamza's own call on whether this borderline combined-term posting should count.
- **HII/Newport News Shipbuilding** — re-check per their own stated "September-October" posting cadence.
- **Analog Devices, Lam Research, Caterpillar** — still not posted, recurring note across many runs now.

---

## 2026-09-21 ~13:00 UTC

### Sync
Session started with a detached HEAD; `git fetch origin master` confirmed local matched `origin/master` exactly at `d6e02f2`. Checked out and reset local `master` to track it cleanly. No push-access issues at sync time.

### What was searched
Delegated to a research agent with the strict-verification instructions. Two priorities:
1. **Follow-ups from the last run's "worth re-checking" list**: GD Electric Boat req 601496955 (Cloudflare-blocked 6 runs straight), Vertex Pharmaceuticals (Workday 500 error), Anduril "Manufacturing Co-Op" (Quincy/Lexington MA, found in snippets but not direct-fetched), HII/Newport News Shipbuilding (their own Sept-Oct posting-window claim), Moderna req R19735 vs. biospace mirror job 3072468 sanity check (low priority, deprioritized this run).
2. **Fresh sweep**: Blue Origin, Textron (Bell Helicopter/Textron Aviation), other GD divisions (GD Mission Systems, GD Ordnance & Tactical Systems), L3Harris, Sikorsky/Lockheed Martin, Honeywell Aerospace, Hexcel, Textron Specialized Vehicles, Chart Industries, Nuvation, Vicor, MathWorks, Desktop Metal, Waters Corp, Analogic, Charles River Labs, Formlabs (new reqs), Markforged, PTC, Hologic, Teradyne, Analog Devices (re-check), Wistron/Jabil/Flex/Sanmina, Firefly Space, Relativity Space, ABB Robotics, KUKA, Fanuc, Universal Robots, Vecna Robotics, Locus Robotics, GreenPower Motor, Proterra, Commonwealth Fusion Systems, Form Energy (re-check), Sublime Systems.

### Added to `rows` (2 new entries)
- **Anduril Industries — Winter 2027 Manufacturing Engineer Co-op**, Lexington MA / Quincy MA — **Yes**, confirmed live on Greenhouse (job 5236589007), $32–$45/hr. This is the req the prior run flagged as "found in snippets but not direct-fetched" — now confirmed. Same cohort/site family as the already-tracked Mechanical/Systems Engineer Co-ops.
- **General Dynamics Mission Systems — Mechanical Engineering Co-Op (January – May 2027)**, McLeansville, NC — **Partial** (corroborated across multiple independent aggregator/mirror sources with consistent title/pay/dates/location, but the icims URL redirected to a generic careers landing page and the gd.com mirror returned HTTP 403 — could not independently render the job page or confirm open status). Not Boston-area. Different req/season from the already-tracked GDMS Infrastructure Engineer Co-op (Pittsfield, MA, Fall 2026 or Spring 2027).

### Added to `checked` (9 new entries)
Textron (Bell Helicopter/Textron Aviation — Summer 2027 only, posting window Sept 1–Oct 31 2026), Honeywell Aerospace (26 reqs found, all Summer 2027, posted Aug 25–27 2026), Hexcel (no Spring 2027 posting), MathWorks (re-checked and confirmed Software Engineer role — discipline mismatch, supersedes prior "unconfirmed season" note), Waters Corporation (only an EE co-op + non-engineering roles, no ME co-op), Chart Industries (no postings at all), GreenPower Motor/Proterra (no current 2027 postings, only stale 2022 listings), Universal Robots/ABB Robotics (no Spring 2027 postings), Lockheed Martin/Sikorsky (confirmed further site migration — legacy search-jobs URL now hard-redirects to a 404).

### Priority re-check outcomes (no further `rows`/`checked` change beyond the above)
- **GD Electric Boat req 601496955** — still Cloudflare-blocked; tried direct fetch and an r.jina.ai proxy workaround, both failed. 7th+ consecutive failed attempt across runs. Recommend deprioritizing further automated tries — needs an actual in-browser check.
- **Vertex Pharmaceuticals** — Workday portal returned HTTP 500 again (2nd consecutive), and the co-ops page directly returned HTTP 403. No Spring 2027-specific req found via search either. Still unresolved.
- **Anduril "Manufacturing Co-Op" Winter 2027** — CONFIRMED, see new `rows` entry above.
- **HII/Newport News Shipbuilding** — re-checked directly; still nothing live for Spring 2027 (only Fall 2026 co-op and Summer 2027 internships exist). Their Sept–Oct posting-window claim hasn't materialized yet as of today. Worth another pass in 1–2 weeks.
- **Moderna req R19735 vs. biospace mirror job 3072468** — not re-verified this run (explicitly deprioritized); prior run's conclusion (very likely the same posting) stands unchanged.

### Fresh sweep — nothing qualifying found
Sublime Systems (third-party mirror confirms closed — corroborates the existing Lever-board "checked" entry, no new entry needed), plus the 9 new `checked` entries above. No qualifying new postings found at L3Harris, Nuvation, Vicor, Desktop Metal, Analogic, Charles River Labs, Formlabs (no new reqs beyond existing), Markforged, Hologic, Teradyne, Analog Devices, Firefly Space, Relativity Space, KUKA, Fanuc, Locus Robotics, Commonwealth Fusion Systems, or Form Energy this pass (agent did not report explicit findings for every company in the sweep list — treat any not mentioned above as "no notable finding," not as independently ruled out).

### Staged applications created (1 file, `staged-applications/`)
`anduril-industries-manufacturing-engineer-coop.md` — the one new fully-verified ("Yes") posting this run. The GD Mission Systems row is Partial, so per the routine's rule it was not staged.

### Spreadsheet regenerated
`npm install xlsx --no-save && node build.mjs` → printed `done`; `.xlsx` file changed (128.2KB → 133.3KB, confirmed via `git diff --stat`).

### Worth re-checking next time
- **GD Electric Boat req 601496955** — 7+ consecutive automated-verification failures; needs a human in-browser check rather than further automated attempts.
- **Vertex Pharmaceuticals** — retry the Workday portal (2 consecutive 500s) or find an alternate canonical URL; also try the co-ops page again (403 this run).
- **GD Mission Systems Mechanical Eng Co-op (McLeansville, NC)** — needs a working direct-fetch method (icims redirects to a landing page, gd.com 403s) to move from Partial to Yes.
- **Lockheed Martin/Sikorsky** — try the current `careers.lockheedmartin.com` host structure fresh next run instead of the now-dead legacy `lockheedmartinjobs.com`/search-jobs paths.
- **HII/Newport News Shipbuilding** — re-check per their own stated "September-October" posting cadence.
- **Analog Devices, Lam Research, Caterpillar** — still not posted, recurring note across many runs now.
- **Moderna req R19735 vs. biospace mirror job 3072468** — confirm same posting next time either source is touched.
- **Saab "Spring - Summer 2027" Systems Engineering Co-Op** — still Hamza's own judgment call on the borderline combined-term posting.

---

## 2026-09-21 ~19:00 UTC

### Sync
`git fetch origin master` confirmed local (detached HEAD) matched `origin/master` exactly at `d2303ca`. Checked out and fast-forwarded local `master` cleanly. No push-access issues at sync time.

### What was searched
Delegated to a research agent with the strict-verification instructions. Two priorities:
1. **Follow-ups from the last run's "worth re-checking" list**: GD Electric Boat req 601496955 (Cloudflare-blocked 7+ runs straight), Vertex Pharmaceuticals (Workday 500 errors), GD Mission Systems McLeansville NC Mechanical Eng Co-op (Partial in `rows`, needs a working direct-fetch method), Lockheed Martin/Sikorsky (site migration, try current host structure), HII/Newport News Shipbuilding (Sept-Oct posting cadence), Analog Devices/Lam Research/Caterpillar (recurring not-yet-posted note), Draper Laboratory and MIT Lincoln Laboratory (any new in-discipline Spring 2027 req), GE Aerospace (any new Lynn, MA reqs).
2. **Fresh sweep**: Northrop Grumman, Boeing, Spirit AeroSystems, Collins Aerospace direct, Moog, Woodward, PerkinElmer/Revvity, Boston Scientific, Medtronic, Becton Dickinson, GD Bath Iron Works, GD Ordnance & Tactical Systems, Blue Origin (new reqs), SpaceX (new reqs), Joby Aviation, Natel Energy, Sanergy, Vicor, Nuvation, PTC, Instron.

### Result: no new entries added to `rows`
Every "new" finding the research agent surfaced turned out, on cross-check against the current `build.mjs`, to already be tracked verbatim (SpaceX Spring 2027 Engineering Internship/Co-op, RTX Collins Aerospace Cedar Rapids IA Mechanical Eng Co-op req 01869080, Northrop Grumman Chandler AZ 2027 Spring Mechanical Engineering Co-op, Draper Electro-Mechanical Instrument Co-op JR002883-1, and GD Mission Systems McLeansville req 74530 with the exact same job ID/pay already on file). No genuinely new qualifying posting was found this run. One candidate (Blue Origin Spring 2027 Manufacturing Engineering Internship – Undergraduate, Space Coast FL, req R66348) was found via an aggregator mirror only; the same mirror states the application window closed July-Aug 2026 (already past as of today), so it was excluded rather than added as Partial — see `checked` below.

### Added to `checked` (12 new entries)
Lockheed Martin/Sikorsky (current portal is lockheedmartin.eightfold.ai/careers, replacing the dead legacy site — still JS-blocked, no Spring 2027 co-op located), GD Mission Systems McLeansville re-verify attempt (same blocking pattern, status unchanged), GD Electric Boat req 601496955 (8th+ consecutive Cloudflare block), HII/Newport News Shipbuilding (still nothing for Spring 2027), Analog Devices/Lam Research (re-check, no change), MIT Lincoln Laboratory (re-check, no new in-discipline req), GE Aerospace (re-check, no new Lynn MA req), Caterpillar (new "2027 Engineering Corporate Parallel Co-op Program" req IDs found and opened directly, but ambiguous continuous-rotation format still fails the discrete Winter/Spring-term bar, no MA location), Blue Origin req R66348 (aggregator-only, application window likely already closed), a 10-company fresh-sweep "nothing found" group (Spirit AeroSystems, Medtronic, Becton Dickinson, Moog, Woodward, PerkinElmer/Revvity, PTC, Natel Energy, Sanergy, Nuvation Engineering), GD Bath Iron Works (trades apprenticeship, discipline mismatch), and GD Ordnance & Tactical Systems / Northrop Grumman Boston-area presence (nothing found).

### Staged applications
None created this run — no new fully-verified postings.

### Spreadsheet regenerated
`npm install xlsx --no-save && node build.mjs` → printed `done`; `.xlsx` file changed (133.3KB → 139.4KB, confirmed via `git diff --stat`).

### Worth re-checking next time
- **GD Electric Boat req 601496955** — 8+ consecutive automated-verification failures; still needs a human in-browser check.
- **Vertex Pharmaceuticals** — not re-attempted this run (deprioritized); Workday portal has returned HTTP 500 on prior attempts.
- **GD Mission Systems McLeansville NC Mechanical Eng Co-op (req 74530)** — still Partial; icims/gd.com both still block direct rendering after 2 runs of trying.
- **Draper JR002688/JR002717** (Acoustic and Vibration Technologies Co-op, Metrology Co-op) — still open/rolling but no stated season/year; not re-attempted this run.
- **HII/Newport News Shipbuilding** — re-check again per their own stated "September-October" posting cadence; still nothing live as of this run.
- **Analog Devices, Lam Research** — still not posted, recurring note across many runs now.
- **Moderna req R19735 vs. biospace mirror job 3072468** — not re-touched this run; prior conclusion (very likely same posting) stands.
- **Saab "Spring - Summer 2027" Systems Engineering Co-Op** — still Hamza's own judgment call on the borderline combined-term posting.
- **Caterpillar "2027 Engineering Corporate Parallel Co-op Program"** — confirmed live/open this run but excluded on ambiguous-term grounds; worth Hamza's own judgment call if he's open to a continuous parallel co-op structure rather than a discrete Winter/Spring-only term.

## 2026-09-22 ~01:00 UTC

### Sync
`git status` initially showed a detached HEAD; `git fetch origin master` confirmed local matched `origin/master` exactly at `3507a61`. Checked out and reset local `master` to track it cleanly. No push-access issues at sync time.

### What was searched
Delegated to a research agent with the strict-verification instructions. Two priorities:
1. **Follow-ups from the last run's "worth re-checking" list**: GD Electric Boat req 601496955 (Cloudflare-blocked 8+ runs straight), Vertex Pharmaceuticals (Workday 500/blank errors), GD Mission Systems McLeansville NC Mechanical Eng Co-op req 74530 (Partial, icims/gd.com block direct rendering), HII/Newport News Shipbuilding (Sept-Oct posting cadence), Draper Laboratory and MIT Lincoln Laboratory (any new in-discipline Spring 2027 req), GE Aerospace (any new Lynn, MA reqs).
2. **Fresh sweep**: Boston Scientific, Vicarious Surgical, Desktop Metal, Markforged, PTC, Bose, Philips (Andover/Cambridge MA), Toyota Research Institute, Vicor, Nuvation Engineering, Instron, Analogic, Charles River Laboratories, Symbotic, Boston Metal, Alloy Enterprises, Commonwealth Fusion Systems (re-check), Sonos, Duracell, Hasbro, Curtiss-Wright, Textron Systems (re-check), Aurora Flight Sciences, Sierra Space, Redwire Space, Karman Space & Defense, L3Harris, Leidos, Astranis, Relativity Space, Firefly Aerospace, Joby Aviation, Honeywell Aerospace (re-check), Moog, Woodward.

### Added to `rows` (3 new entries)
- **Applied Materials — 2027 Spring Mechanical Engineer Co-op (Gloucester, MA)** (R2628290 / 100424621952) — **Yes**, confirmed live via direct fetch of Applied Materials' own careers site, posted 2026-09-10, $31–$33/hr. Boston metro (~35 mi). New req/location distinct from other Applied Materials postings already tracked.
- **Vertex Pharmaceuticals — Vertex Spring Co-Op 2027, Mechanical Automation** (REQ-30500-1), Boston, MA — **Partial** (independent aggregator mirror shows full details and a fresh 2026-09-21 post date; Vertex's own Workday page returned blank/JS-rendered on both wd5 and wd501 subdomains, consistent with a recurring known access issue). Deadline Nov 15, 2026. Distinct from the excluded biotech/process Vertex reqs — see `checked`.
- **Astranis Space Technologies — Mechanical Engineer Intern (Spring 2027)**, San Francisco, CA — **Yes**, confirmed live via direct fetch on Greenhouse. ITAR-restricted (US citizen/LPR/protected individual only). Not Boston-area but included per Hamza's nationwide preference. A separate Summer 2027 req exists at the same company — do not conflate.

### Added to `checked` (10 new entries)
Sonos (Fall 2026 only, wrong season), Vertex Pharmaceuticals' Process Development Upstream / CGT Process Development Spring Co-Op 2027 reqs (discipline mismatch — biotech/process, not mechanical), Karman Space & Defense (Summer-only program by design), Symbotic req R6576 (404, appears filled/removed), Commonwealth Fusion Systems (re-check, only Fall 2026 co-op posted, no change), HII/Newport News Shipbuilding (re-check, still nothing for Spring 2027 despite stated cadence), MIT Lincoln Laboratory (re-check, only Cyber Security discipline-mismatch and Fall-2026 Rapid Prototyping found), Draper Laboratory (re-check, no new reqs), GE Aerospace (re-check, no new Lynn MA reqs), and a 10-company fresh-sweep "nothing found" batch (Boston Scientific, PTC, Desktop Metal, Markforged, Vicor, Nuvation Engineering, Instron, Analogic, Boston Metal, Alloy Enterprises).

### Not added — unresolved, flagged for follow-up (not in `checked`, not conclusively ruled out)
- **Philips — Co-op, Robotics Mechatronics, Surgical Robotics (Cambridge, MA)**: in-discipline and pay-attractive ($29-32/hr), but season is contradictory across sources — the authoritative Workday req (589905, posted Aug 26) is titled "Fall 2026" while aggregator mirrors label the same-looking role "January 2027." Employer's own page is JS-blocked. Not added due to unresolved season conflict.
- **RTX — Mechanical/Industrial Engineering Co-op, req 01872434, Melbourne FL**: confirmed live via aggregator mirror (posted Sept 17), but season labeled ambiguous "Spring/Summer 2027" rather than a clean Spring-only term. Not added; worth checking jobs.rtx.com directly for clearer season language.

### Priority re-check outcomes (no `rows`/`checked` change)
- **GD Electric Boat req 601496955** — still Cloudflare-blocked (buildsubmarines.com mirror 403, guessed icims URL now 410). 9+ consecutive failed independent-verification attempts. Recommend treating as Partial-only going forward and deprioritizing further per-run automated effort — needs a human in-browser check.
- **GD Mission Systems req 74530 (McLeansville, NC)** — got the corrected exact iCIMS URL this run via a dreamworkhq mirror, but direct fetch of that exact URL still resolves to a generic careers landing page, not the job itself. Status unchanged at Partial.

### Staged applications created (2 files, `staged-applications/`)
`applied-materials-mechanical-engineer-coop-gloucester.md`, `astranis-mechanical-engineer-intern-spring2027.md` — the two fully-verified ("Yes") new postings this run. The Vertex Mechanical Automation row is Partial, so per the routine's rule it was not staged.

### Spreadsheet regenerated
`npm install xlsx --no-save && node build.mjs` → printed `done`; `.xlsx` file changed (139.4KB → 143.5KB, confirmed via `git diff --stat`).

### Worth re-checking next time
- **GD Electric Boat req 601496955** — 9+ consecutive automated-verification failures; needs a human in-browser check rather than further automated attempts.
- **GD Mission Systems req 74530 (McLeansville, NC)** — still Partial; try a different access method (referer/query string) next time.
- **Philips Co-op, Robotics Mechatronics, Surgical Robotics (Cambridge, MA)** — season conflict (Fall 2026 vs January 2027) unresolved; worth a fresh direct-fetch attempt to pin down which label is current.
- **RTX req 01872434 (Melbourne, FL)** — "Spring/Summer 2027" ambiguous wording; worth checking jobs.rtx.com directly for a clean season statement.
- **Vertex Pharmaceuticals Mechanical Automation Spring Co-Op (REQ-30500-1)** — still Partial; worth a direct-fetch retry on Vertex's own Workday page to upgrade to Yes.
- **HII/Newport News Shipbuilding** — re-check again per their own stated "September-October" posting cadence, still nothing live as of this run.
- **Analog Devices, Lam Research** — still not posted, recurring note across many runs now.
- **Saab "Spring - Summer 2027" Systems Engineering Co-Op** — still Hamza's own judgment call on the borderline combined-term posting.
- **Caterpillar "2027 Engineering Corporate Parallel Co-op Program"** — still Hamza's own judgment call on the ambiguous continuous-rotation structure.
- **Moderna req R19735 vs. biospace mirror job 3072468** — prior conclusion (very likely same posting) stands, not re-touched this run.
