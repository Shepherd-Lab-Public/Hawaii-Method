# Changelog

Newest first. Each heading is a git tag.

## 2026-11-21b

- VS Code first: the recommended setup is every house in Claude Code inside VS Code. New "What you need" list at the top of the guide: Claude Pro or higher (the free plan does not include Claude Code), a GitHub account, VS Code, Git, the Claude Code, LaTeX Workshop, and PDF extensions, and Gmail, Google Calendar, and Google Drive connectors turned on at claude.ai, which Claude Code picks up from the same account.
- Setup: Node 4 now installs and signs in to these tools and clones the repository in VS Code, whose GitHub sign-in lets Claude push (the Claude GitHub App is needed only for app chats); a setup begun in a Claude chat moves into VS Code there. Node 7 runs every house in VS Code, Node 11 creates a command for each house, and Nodes 12 and 13 open and rotate houses with those commands. Sections 11, 12, 18, and 21 match.
- App chats stay as the fallback for a house that cannot run in VS Code.
- New lesson: a beginner fixed a broken website, moved it from WordPress to Jekyll, and then wrote a 42-chapter book with the method.
- Staying current: setup (Node 1) asks how the person got the guide and checks it against the latest version on GitHub, using the latest if theirs is older. HOUSEHOLD.md section 1 records the version followed, as the README already said. Once a week, at sync, the Head House checks for a newer version and tells the owner what changed; the owner decides what to adopt (section 19).

## 2026-11-21

- Writing projects: the book example (section 0) becomes one example for a grant, a journal manuscript, or a book: a Head House, one Writer who owns all the text, a Librarian, and a Guidelines Specialist who keeps the funder's, journal's, or publisher's guidelines and owns formatting and assembly. Splitting the text among several writer houses proved confusing and complicated.
- Start simple: setup (Node 6) proposes the fewest houses that will do, and the writing example starts with the Head House and the Writer, adding houses only when needed.
- New lesson, "One Writer per document". "Deliverables as fragments" no longer applies to a book's chapters, and builders own the text of a document rather than sections of it (section 7).
- Each house commits its own work, and only its own: stage files by name, never everything at once, and never commit another house's changes. Added to the CLAUDE.md template, the base rules (15.4), the checkpoint, and the git conventions (section 16), because houses sharing one local copy can otherwise sweep each other's unfinished work into a commit.
- End of day (section 14): checkpoint every house opened today, all at once, then sync in the Head House, then close the sessions. Sync now starts by listing which houses checkpointed today and any house folder with uncommitted changes.

## 2026-11-03

- No-warranty notice added to the top of the guide and the README, because the guide often travels without the LICENSE file. It points to section 5 of the license.
- Giving back: the guide now invites people to send improvements back and links to CONTRIBUTING.md, so someone who has only the guide file can find it.
- CONTRIBUTING.md: pull requests can edit `languages.md` as well as the guide.

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
