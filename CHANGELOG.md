# Changelog

Newest first. Each heading is a git tag.

## 2026-11-02

- The method is now the Hawaii Method, and its parts have plain English names: house, Head House (still titled Lead by default), responsibility, and HOUSEHOLD.md. The guide is `hawaii-method.md` and the shared rules are `_house-base.md`.
- "Household" names the whole project; a project with several houses is a "full household", as opposed to a seed.
- Giving back: a suggested donation to one of three charities: the Hawaii H.O.M.E. Project, Waikiki Health, or Kuaʻāina Ulu ʻAuamo (KUA).

## 2026-10-29

- Working languages: a household can write and talk in any language its models handle well, while the guide stays in English. People can start setup in their own language; otherwise setup offers a menu of languages, each in its own name, first (Node 1) and switches at once, then confirms the agents' working language and variant (Node 9); HOUSEHOLD.md records it; the CLAUDE.md template and the base rules keep the structure (file names, headings, IDs, status words, ISO dates) in English and the content in the working language; section 13 notes that quality varies by model. New companion file `languages.md` with notes for Spanish, French, Portuguese, German, Mandarin, Japanese, Hindi, Arabic, and Bengali.

## 2026-10-24

- New section 17, Safeguards: what counts as sensitive; rules for the repository, agent sessions, and products; what to do when something leaks; a compliance advisor for regulated data. Setup (Node 9) asks about sensitive data and records data rules in HOUSEHOLD.md; the base rules, the CLAUDE.md template, and the git conventions point to section 17. Force-pushing is allowed only to remove leaked material. Sections 17-20 renumbered 18-21.
- Only the owner opens a house: no agent starts another house, or a second copy of itself, as a subagent or background session. Helpers that load no role file and write nothing are still allowed. Added to section 12, section 13, the CLAUDE.md template, the base rules, units, and the checklist, with an optional Claude Code hook to enforce it.
- The hybrid (section 3) narrowed: the Head House dispatches a house subagent only when the owner asks, in the foreground, for a house with no open session.
- Using other models (section 13): data handling differs by AI service, so check each against the data rules.
- Git conventions: prefer SQLite when a project needs a database; gitignore the database file and commit the schema and a rebuild script. One house owns the database and is its only writer; data that cannot be rebuilt gets a backup outside git; the live file stays off synced folders and network drives.
- Lessons learned: houses must not start houses; going public exposes the history; local databases can be recreated from the rebuild script.
- Names of specific projects, repositories, and houses removed from the guide; lessons keep the kind of project and the date.
- Consistency: "staff houses" replaces "employee"; every house, the Head House included, follows `_house-base.md`; the Head House's folder has its own STATE.md; one opening-line form; agents never send email (drafts only), matching section 18; launchers shown in the standalone layout; PRODUCTS.md added to the growth and build steps; a wrong cross-reference to the style rules fixed.
- New-project checklist items for data rules, the database, and the owner-opens-a-house rule.
- Licensed under CC BY 4.0 (was all rights reserved); LICENSE file added. CONTRIBUTING.md added: how to propose changes by pull request; maintainers decide what merges.

## 2026-10-09

- One layout everywhere: every household keeps all its house under `staff/`, with the Head House at `staff/lead/`, in standalone and control repositories alike.
- Shared base rules are named `_house-base.md` everywhere (was `_employee-base.md`).
- Adopting a repository: planning files (to-do lists, issue logs, lab books) move out of product repositories to their owning house; a new final step checks the live product by URL for working files.
- Lessons learned from a lab website: exclude lists fail open; deleting a published file is not instant behind a CDN cache.
- New-project checklist items for the `staff/` layout and the live-URL check.

## 2026-10-06

- Credit: the method is by John Shepherd and Sven Prevrhal.
- A household never shares a repository with anything that publishes. New control repository model: the household lives in its own private repository, and each product repository carries only a pointer CLAUDE.md. Replaces the "embedded" layout that excluded `staff/` from a website build.
- MASTER.md renamed HOUSEHOLD.md.
- PRODUCTS.md added: each house lists the work products the owner opens; the Head House compiles them at sync.
- Larger organizations: one `<org>-admin` control repository; a house may lead units, two levels at most.

## 2026-10-03

- Restructured into Part A, a guided setup for Claude with a decision tree, and Part B, the reference.
- New sections: examples to start from, the seed household, adopting an existing repository, and trying the method without committing.

## 2026-10-02

- First version under git, imported from an earlier draft.
