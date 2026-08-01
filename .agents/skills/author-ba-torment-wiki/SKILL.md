---
name: author-ba-torment-wiki
description: Write or revise Blue Archive boss guides, season raid reports, and student build notes in llmwiki-game. Use for 공략, 총력전·대결전 리포트, 스작·육성 문서.
---

# Wiki Authoring

Read `llmwiki-game/AGENTS.md` first.
It defines file placement, frontmatter, index, log, glossary, and history rules.
This skill defines writing quality.

## Workflow

1. Read the target, its index entry, and the related boss guide.
2. Gather only what the document needs from structured data, official skill
   text, and player interpretation.
3. Cross-check at least one important number. Prefer structured data when
   sources disagree; omit or mark anything still uncertain.
4. Decide the document's real complexity before choosing its length or shape.
5. Write conclusions a player can act on, using data as evidence rather than as
   the table of contents.
6. Finish the repository bookkeeping required by `AGENTS.md`.

When a user has verified a table or other structured block, treat its rows,
numbers, and claims as fixed. Improve its tone or the surrounding explanation;
do not replace the structure unless the user asks.

## Shared quality bar

- A general player should understand the document comfortably in 5–10 minutes.
- Extract the few mechanics or choices that matter. Do not dump databases.
- Explain what to do, why it works, and any important limitation.
- Include human-scale judgment: easy or restrictive, fixed or flexible,
  ownership pressure, ranking pressure, and the reason.
- Write an editorial report, not a neutral database summary. Lead with why
  players remember the season: expectations, surprise, frustration, relief, or
  a widely shared evaluation supported by the sources. Most seasons have no
  special story; default to a concise explanation and use narrative buildup
  only when expectation and outcome genuinely diverged.
- Use plain Korean. Avoid private shorthand, analyst jargon, and repeated
  conclusions.
- Put time-sensitive findings in `## 히스토리`; keep timeless mechanics in the
  guide.

## Boss guides

- Do not name students. Recommend roles or capabilities.
- Cover difficulty stats, part/armor structure, composition-defining mechanics,
  and useful student types.
- Reduce official boss skills to the mechanics that change party building.
- Recommend only actions a student can actually perform.

## Season reports

Add every covered raid ID to `raid_ids` frontmatter.

### Research gate

Do not rewrite from the existing report. Before changing one season, inspect:

1. the complete party dataset, including the highest-score party;
2. summary, party-count, essential/high-impact, and rank-band trends for every
   difficulty or armor variant;
3. the most common parties and how they differ from the highest-score party;
4. resolved skills for every student used to support a causal claim;
5. the boss guide and underlying boss numbers or official skill text.

Derive one explanation that accounts for all five. The report body, summary-tab
cards, and Arona comments must be different views of that same explanation and
must not contradict each other. If any dataset is unavailable, stop that report
instead of filling the gap from the old prose.

The party page already exposes sample size and summary cards. Do not introduce
a report by repeating them. Start with what kind of fight it was and what
happened in that season. Reuse a number only when it proves an interpretation.

Recover the core combat sequence, not just the final roster. Inspect high-score
videos frame by frame when available. State observed turning points such as
wave setup, retreat, groggy timing, or party handoff, but do not invent an exact
skill order or timing that the evidence cannot support.

Finish the evidence-backed draft before asking about missing micro-tactics or
community context. Collect only questions that could change the interpretation
and ask the user once after the draft; leave the affected claim pending without
blocking the rest of the report.

Do not infer that a low party count means the mechanic was simple. Check
whether players bypassed a lethal or restrictive mechanic with enough damage
and only the minimum reproducible movement.

Keep the competitive context visible, but never fill space with the generic
fact that faster clears score higher. Name a season-specific optimization only
when the evidence shows one; otherwise stop at the concrete tactic and result.

Take the difficulty scope and clear count from the current summary data, never
from the old report. Resolve same-name alternate IDs separately when their
stances or roles differ; a display name alone is not enough to identify a kit.

Name the denominator and assist treatment before quoting usage.
`essentialCharacters` excludes assists but counts appearances, while party
totals include assists and repeated uses. Deduplicate explicitly before calling
either one a percentage of users.

### Let the season choose the shape

- `notes/3s25_binah_meta.md` is the simple-season reference: one clear answer,
  short explanation, no manufactured conflict.
- `notes/s90_gregorius_meta.md` is the complex-season reference: difficulty
  metas diverge, so separate sections and numeric breakpoints are useful.
- `notes/s86_binah_meta.md` is the season-story reference: expectation and
  outcome diverge, and the report explains the community's experience before
  listing the party.
- These are two poles, not templates. Use only the sections the reader needs.
- If only the dealer changes by armor, say it once and stop.

### Explain picks

- Identify the damage axis from the highest-scoring party, not usage rank.
- Describe the actual composition order and hierarchy: who anchors party 1,
  who appears from party 2 onward, which effects stack, and what can be
  replaced. Do not substitute a theoretically useful student for an observed
  core pick.
- Do not trust `TacticRole` alone. Read resolved skill effects and preserve
  multi-role picks.
- Connect `kit trait → boss mechanic or part → practical reason for selection`.
- A generic skill description has no report value. For each pick, answer why
  this student occupied this slot in this fight.
- Mention only the subset of a student's kit whose activation conditions and
  effects mattered in this boss, difficulty, party, and tactic. Omit otherwise
  strong traits that did not contribute here.
- Evaluate movement skills by the resulting formation, not only the selected
  unit's destination. Unit collision and spacing can reposition nearby allies
  and may be the real reason for the pick.
- Do not credit a debuff merely because it exists in the kit. Confirm that the
  boss stat made it relevant and that the tactic actually used it.
- Preserve damage hierarchy accurately. A second festival-grade dealer is a
  co-damage axis even when it also helps another dealer's accumulation mechanic.
- Describe strong synergy as `especially compatible` unless the data proves
  exclusivity; a generally useful attribute buffer may appear in many parties.
- Explain filler picks when they solve a specific mechanic.
- Distinguish highest-score and popular parties only when the difference
  reveals player behavior or a difficulty mechanic.
- Check release timing before interpreting low cumulative usage. A new
  student's short history is not evidence that the pick was niche, forgotten,
  or revived.
- Read the season terrain and each competing dealer's terrain affinity. Treat
  affinity as one reason a dealer won that season, never as an absolute ranking:
  a large kit or damage gap can outweigh poor terrain.
- Treat small samples as noisy. Filter memorial tails, but never use them to
  judge player skill.

### Arona comments

Place `## 아로나 코멘트` immediately before `## 히스토리`.

- Format: `- 카드라벨(선택적 난이도 또는 대결전 장갑): 해요체 한두 문장`
- Labels: `시즌 한 줄`, `플래티넘 컷`, `핵심 캐릭터`, `Top 5 파티`,
  `파티 비율`, `특수 클리어`, `상세 분석`
- Scope: `토먼트`, `루나틱`, `경장갑`, `중장갑`, `특수장갑`, `탄력장갑`.
  장갑명은 카드 라벨이 아니며 `Top 5 파티(특수장갑)`처럼 범위로만 씁니다.
- Sound like a familiar guide with an opinion, not a formal analyst. A light
  aside or rhetorical question is welcome when it fits the season.
- Write retrospectively about what happened that season. Do not turn every
  comment into a generic instruction ending in “챙겨 주세요” or “하면 돼요.”
- Lead with a friendly interpretation or an observation that only becomes
  visible after analyzing the season. Never paraphrase a summary card merely
  to fill the comment. One decisive number may be repeated only when it is the
  punchline that makes the season understandable.
- Make `Top 5 파티` name the top composition's concrete division of labor or
  optimization. Do not replace it with a generic remark about strong players,
  role coverage, or synergy.
- Scope difficulty-specific claims. Omit comments with no added value.

### Prose

- Write the entire season report in Arona's friendly `해요체`. Avoid formal
  report endings such as `입니다`, `했습니다`, and `됩니다`. An occasional
  natural `답니다` is fine when it sounds like Arona rather than a report.
- Open with the observed fight and player response. Do not compress the whole
  season into a dramatic thesis such as `X was the real wall` or `players were
  stopped at Y`; let the judgment emerge from the concrete sequence.
- State the relevant cause with concrete subjects and actions. Avoid reveal-style
  negation (`X was not merely Y`) and balanced abstractions (`leave only A and
  spend the rest on B`); they sound written rather than spoken.
- Do not manufacture editorial copy in headings. Use only the minimum
  structural labels the subject requires; never add slogan-like subtitles such
  as `— A가 열고 B가 끝냈다`.

## Build and training notes

- Give every genuine low-invest student a separate row and four-slot spec.
- Explain the reason from resolved skills when supported; otherwise mark it
  uncertain without deleting the observation.
- Separate skippable skills from unfinished rookie accounts and check
  base/alternate-name collisions.
- Check raw SchaleDB `WeaponPassive`. Buff/debuff-duration passives can reverse
  a low-invest recommendation at higher weapon tiers, so state the exception.
- Normalize EX level 5 to `M`; ignore gear, weapon, potential, and bond tokens.
- Warn that high-score uploads favor max investment and missing notation limits
  conclusions.

## Final pass

- Remove sections that merely restate another table or paragraph.
- Check every proper noun and causal claim against a source.
- Confirm frontmatter, links, index, log, glossary, and history.
- Improve this skill only when a reusable rule emerges. Replace obsolete rules;
  never append a postmortem or one-off anecdote.
