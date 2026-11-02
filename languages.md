# Working in other languages

A companion to the Hawaii Method guide ([hawaii-method.md](hawaii-method.md)). Read it when setting up a household whose agents will write and talk in a language other than English.

## The rule

The guide stays in English: it is the instruction set, and one authoritative version keeps every household built the same way. Each household chooses a **working language**, recorded in HOUSEHOLD.md, and its agents write and talk in it.

| Stays in English | Written in the working language |
|---|---|
| File and folder names (`STATE.md`, `DIRECTIVES.md`, `staff/lead/`) | Logs, notes, and drafts |
| Template headings ("For the Head House", "Waiting on people") | Directive goals, tasks, and outcomes |
| Directive and task IDs (`SCI-004.2`) and commit prefixes | STATE.md content under the English headings |
| Status words (active, blocked, done; living, draft, final, sent) | Products, and everything said to the owner |
| Dates, as `YYYY-MM-DD` | Chat with the owner |

The structure stays in English so every household has the same layout and the routines can find what they look for. Everything people read is in the working language.

- **Routine words work in both languages.** Agents accept "checkpoint", "sync", and "start" in English or in the working language (for example, "punto de control", "sincronizar", "inicio").
- **Save every file as UTF-8.** Most tools do this already; some Windows tools default to other encodings and garble non-Latin text.
- **In Claude Code, set the response language too.** Add `"language": "<language>"` (for example, `"language": "spanish"`) to the household's `.claude/settings.json`, so every session responds in the working language. Other tools have their own settings; the rule in CLAUDE.md works everywhere.

## Before you rely on a language

- **Pilot it.** Run one house in the working language for a week or two and read what it writes. Quality varies by language and by model, especially for specialized vocabulary.
- **Expect some scripts to fill the context window faster.** Text in Devanagari, Bengali, Arabic, Chinese, or Japanese script often uses more of a model's context for the same content than English does. Keep STATE.md short and rotate chats a little sooner.
- **Record the variant and register in HOUSEHOLD.md**, so every house writes the same way.

## Notes by language

| Language | Choose and record | Notes |
|---|---|---|
| Spanish | Latin American or European; formal (usted) or informal (tú) | Generally strong in current models. |
| French | Region if it matters (France, Canada); formal (vous) by default | Generally strong. |
| Portuguese | Brazilian or European | Generally strong; the variants differ in spelling and vocabulary. |
| German | Region if it matters (Germany, Austria, Switzerland, where ß is written ss); formal (Sie) or informal (du) | Generally strong. Long compound words are normal; agree on technical terms once, in HOUSEHOLD.md, so houses don't mix German and English names for the same thing. |
| Mandarin Chinese | Simplified or Traditional characters | Generally strong. Uses more context than English. |
| Japanese | Register: polite (です/ます) or plain (だ/である) | Generally strong. Uses more context than English. |
| Hindi | Devanagari script; how much English technical vocabulary to keep | Good, but less consistent; pilot carefully. Keep Western digits in IDs and dates. |
| Arabic | Modern Standard Arabic or a regional dialect | Good, but less consistent. Written right to left: keep IDs in code formatting (`SCI-004`) and English headings on their own lines so editors display them cleanly. Keep Western digits in IDs and dates. |
| Bengali | Bengali script; how much English technical vocabulary to keep | Good, but less consistent; pilot carefully. Keep Western digits in IDs and dates. |

These notes are general guidance, not test results. Models change quickly; your pilot is what counts. For published figures, see your model provider's documentation (for Claude: [Multilingual support](https://platform.claude.com/docs/en/build-with-claude/multilingual-support)).

## Teams that speak different languages

One working language for the whole household is simplest. If a house's human counterpart needs a different language, record that house's language in the ownership table in HOUSEHOLD.md. The Head House can read every house whatever its language, but the owner may not; say in HOUSEHOLD.md which language the Head House's reports to the owner use.
