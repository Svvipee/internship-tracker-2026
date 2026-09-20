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
