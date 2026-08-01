---
name: maintain-ba-torment-wiki
description: Review pending BA Torment game-wiki feedback or refresh the beginner guide from human-verified analyzed videos. Use for weekly/manual wiki maintenance, feedback triage, 피드백 처리, 뉴비 영상 갱신, or beginner-video curation.
---

# Maintain BA Torment Wiki

Work only in `data-aggregator`, `ba-analyzer`, and `llmwiki-game`. Keep each
service on its own database: feedback comes from `data-aggregator`; verified
videos come from `ba-analyzer`.

Before editing wiki documents, read `llmwiki-game/AGENTS.md` and
`llmwiki-game/.agents/skills/author-ba-torment-wiki/SKILL.md`. Follow that
skill for prose, sources, frontmatter, and `bluearchive/log.md`.

## Default: review only

Unless the user explicitly asks to apply changes:

1. Collect candidates without changing the database or wiki.
2. Show accepted, rejected, uncertain, and duplicate candidates with concise
   reasons.
3. Ask only about uncertainties that could change the result.

Never branch, commit, push, open a PR, or change feedback status merely because
this skill was invoked.

## Feedback mode

List pending feedback from the owning service:

```text
cd data-aggregator
go run ./cmd/wiki-feedback -action list -status pending -limit 50
```

Then:

1. Group duplicates by domain, slug, and meaning.
2. Read the current target document and its index entry.
3. Cross-check each claim against structured game data, official material, or
   another authoritative source appropriate to the claim.
4. Accept only corrections supported by evidence. Reject false or
   out-of-scope reports. Keep unverifiable claims out of the wiki and mark them
   uncertain.
5. When asked to apply, edit only the supported claims and complete the wiki
   bookkeeping. Create a feature branch or PR only when the user asks.

Do not resolve feedback when a draft or PR merely exists. After the user
confirms the accepted wiki change is merged, or confirms a rejection, update
each pending row separately:

```text
go run ./cmd/wiki-feedback -action resolve -id <ID> -status resolved -resolution "<merged PR or concise evidence>"
go run ./cmd/wiki-feedback -action resolve -id <ID> -status rejected -resolution "<concise evidence>"
```

The CLI intentionally omits submitter IPs. Do not obtain or publish them by
another route.

## Newbie-video mode

List beginner-video candidates by title evidence. The result includes both
verified and review-pending videos:

```text
cd ba-analyzer
go run ./cmd/dump-video-analysis -mode newbie -limit 200
```

Read `llmwiki-game/bluearchive/guides/beginner.md`, then:

1. Resolve every Korean boss and content name through
   `llmwiki-game/bluearchive/glossary.md`; never transliterate a video title.
2. Exclude URLs already present, but process every other human-verified match;
   do not stop after the newest review-pending row.
3. Prefer titles explicitly containing `初心者` when ordering them.
4. Find every `{N}周年先生` title in the result, determine the largest current
   `N`, and prefer that generation. Never hardcode the anniversary number.
5. Use only videos whose difficulty is explicit in the title. Keep different
   armor, season, and difficulty routes; remove only true duplicate routes.
6. Prefer a clear, reproducible beginner route over a marginally higher score.
   Do not claim investment requirements that the verified analysis does not
   establish.
7. When asked to apply, update the links, explanation, source count/date,
   frontmatter `updated`, and `bluearchive/log.md`.
8. Put each video URL in its own paragraph so the wiki renderer embeds it.

Review-pending rows are the priority queue, not wiki sources. Every selected
link must remain backed by a human-verified analysis. Do not substitute merely
discovered, queued, or AI-only analysis rows.
