---
name: author-ba-torment-wiki
description: Write or revise Blue Archive boss guides, season raid reports, and student build notes in llmwiki-game. Use for 공략, 총력전·대결전 리포트, 스작·육성 문서.
---

# Wiki Authoring

`AGENTS.md` sets placement, frontmatter, index, log, glossary, history and
style. This skill sets what a good Blue Archive document contains.

## Workflow

1. Read the target, its index line and the related boss guide.
2. Gather only what the document needs from structured data, official skill
   text and player interpretation. Cross-check at least one important number;
   prefer structured data when sources disagree; omit what stays uncertain.
3. Size the document to the subject's real complexity, then write conclusions
   a player can act on, with data as evidence rather than as the outline.
4. A table or block the user verified is fixed: improve the prose around it,
   never its rows, unless asked.

## Quality bar

- A general player reads it in 5–10 minutes. Pick the few mechanics or choices
  that matter; no database dumps.
- Say what to do, why it works and its limits, with human-scale judgment
  (restrictive or flexible, ownership pressure, ranking pressure) and the reason.
- Season reports are editorial: lead with why players remember the season when
  the sources support it. Most seasons have no story; then stay short.
- Time-sensitive findings go in `## 히스토리`; timeless mechanics in the guide.

## Boss guides

- Name roles or capabilities, never students.
- Cover difficulty stats, part/armor structure, the mechanics that shape the
  party, and useful student types. Reduce official skills to those mechanics.
- Recommend only actions a student can perform.

## Season reports

Add every covered raid ID to `raid_ids`.

### Research gate

Do not rewrite from the existing report. Before changing a season, inspect:

1. the complete party dataset, including the highest-score party;
2. summary, party-count, essential/high-impact and rank-band trends for every
   difficulty or armor;
3. the most common parties and how they differ from the highest-score party;
4. resolved skills of every student behind a causal claim;
5. the boss guide and its numbers or official skill text.

Derive one explanation that accounts for all five; the body, summary-tab cards
and Arona comments are views of it and never contradict. If a dataset is
missing, stop that report rather than reuse old prose.

- The party page already shows sample size and summary cards. Open with what
  kind of fight it was; reuse a number only when it proves a point.
- Recover the combat sequence, not just the roster: watch high-score videos
  frame by frame when available, state observed turning points (wave setup,
  retreat, groggy timing, handoff), never an exact order the evidence lacks.
- Finish the evidence-backed draft first, then ask the user once only what
  could change the interpretation, leaving that claim pending.
- A low party count does not mean a simple mechanic: check whether players
  bypassed a lethal mechanic with damage and minimal movement.
- Never fill space with "faster clears score higher"; name a season-specific
  optimization only when the evidence shows one.
- Difficulty scope and clear count come from current summary data. Resolve
  same-name alternate IDs separately; a display name does not identify a kit.
- Name the denominator and assist treatment before quoting usage:
  `essentialCharacters` excludes assists but counts appearances; party totals
  include assists and repeats. Deduplicate before calling either a share of users.

### Shape

- `notes/3s25_binah_meta.md`: simple season, one clear answer, short.
- `notes/s90_gregorius_meta.md`: complex season, difficulty metas diverge, so
  separate sections and numeric breakpoints.
- `notes/s86_binah_meta.md`: expectation and outcome diverge; the community's
  experience comes before the party.
- These are poles, not templates. If only the dealer changes by armor, say it once.

### Explaining picks

- Find the main dealer from the highest-scoring party, not usage rank. Describe
  the real hierarchy: who anchors party 1, who appears from party 2, what
  stacks, what can be replaced. Never swap in a theoretically useful student
  for an observed pick.
- Read resolved skill effects, not `TacticRole` alone, and keep multi-role picks.
- For each pick, answer why this student held this slot in this fight:
  `kit trait → boss mechanic or part → reason`. Mention only the part of the kit
  that mattered here.
- Movement skills: judge by the resulting formation; collision and spacing can
  move nearby allies and be the real reason.
- Credit a debuff only when the boss stat made it relevant and the tactic used it.
- A second festival-grade dealer is a co-dealer even when it also feeds another
  dealer's mechanic.
- Call strong synergy "especially compatible" unless data proves exclusivity.
- Explain filler picks that solve a specific mechanic. Contrast top and popular
  parties only when the difference shows player behaviour or a mechanic.
- Check release timing before reading low cumulative usage.
- Terrain affinity is one reason a dealer won, never a ranking; a kit or damage
  gap can outweigh it.
- Small samples are noisy. Filter memorial tails, never judge skill by them.

### Arona comments

`## 아로나 코멘트` sits right before `## 히스토리`.

- Format: `- 카드라벨(선택적 난이도 또는 대결전 장갑): 해요체 한두 문장`
- Labels: `시즌 한 줄`, `플래티넘 컷`, `핵심 캐릭터`, `Top 5 파티`, `파티 비율`,
  `특수 클리어`, `상세 분석`. Scope: `토먼트`, `루나틱`, `경장갑`, `중장갑`,
  `특수장갑`, `탄력장갑`, only as a scope, e.g. `Top 5 파티(특수장갑)`.
- A familiar guide with an opinion, looking back on the season. No generic
  instructions ending in "챙겨 주세요" or "하면 돼요".
- Lead with an observation only the analysis reveals; never paraphrase a card.
  One decisive number may repeat when it is the punchline.
- `Top 5 파티` names the top party's division of labour or optimization.
- Scope difficulty-specific claims; drop comments that add nothing.

### Prose

- Arona's `해요체` throughout; no `입니다`, `했습니다`, `됩니다` (an occasional
  natural `답니다` is fine).
- Open with the observed fight and the players' response; let the judgment come
  from the sequence, not a dramatic thesis ("X was the real wall").
- Concrete subjects and actions. No reveal-style negation or balanced
  abstractions, no slogan subtitles in headings.

## Build and training notes

- Every genuine low-invest student gets its own row and four-slot spec, with
  the reason from resolved skills, or marked uncertain without deleting it.
- Separate skippable skills from unfinished rookie accounts; check
  base/alternate-name collisions.
- Check raw SchaleDB `WeaponPassive`: duration passives can reverse a
  low-invest pick at higher weapon tiers; state the exception.
- Normalize EX level 5 to `M`; ignore gear, weapon, potential and bond tokens.
- Warn that high-score uploads favour max investment and missing notation
  limits conclusions.

## Final pass

- Check every proper noun and causal claim against a source.
- Confirm frontmatter, links, index, log, glossary and history.
- Change this skill only for a reusable rule: replace the obsolete rule, never
  append an anecdote.
