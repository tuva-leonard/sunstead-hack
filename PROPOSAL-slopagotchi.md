# Slopagotchi

**A Tamagotchi for your code quality. Ship clean code and your Slopagotchi thrives;
ship slop and it gets sick — and your whole team is watching.**

Challenge: *Tools for Builders on Tangled* (Sunstead Hack 2026).
The anti-slop layer the AT Protocol has been missing.

## The idea

Every developer gets a **Slopagotchi**. Its health is your **anti-slop score**, computed
from your real activity on Tangled. Write thoughtful, tested, reviewed code and your
Slopagotchi grows happy and evolves. Ship lazy AI slop — or stop shipping — and it gets sick.

A whole org lives in one **zoo**: every coworker's Slopagotchi, with their name above it and
their score on display. Pride and gentle shame do the rest. Teams get their own workspace.

## How it's a Tangled / AT Protocol integration

This is the part that matters: the pet *eats real data from the network.*

- **Fed by Tangled.** We listen to the firehose (`sh.tangled.git.refUpdate`,
  `sh.tangled.repo.pull`) and read diffs (`git.getDiff`) — open API, no auth, no limits.
- **Scored by AI.** Claude rates each diff for slop: missing tests, giant unreviewed
  dumps, copy-paste, hollow commit messages, low-effort AI output. Score → Slopagotchi health.
- **Identity is atproto.** Each Slopagotchi and score is a record the developer **owns on their
  own PDS**; the zoo is a view over the org's AT Protocol identities. Portable, verifiable.
- **It is the web of trust.** Tangled wants to fight LLM spam with trust. A visible,
  earned quality score *is* that signal — made fun instead of punitive.

## The engagement loop (Tamagotchi mechanics)

- **Decay:** Slopagotchis need care. Go quiet or ship slop and health drops daily → people come back.
- **Growth:** sustained quality makes them evolve into rarer forms.
- **Zoo pressure:** seeing a coworker's healthy Slopagotchi next to your sick one is the nudge.

## Monetization

- **Individual Slopagotchis are free** — shareable cards pull new teams in (the viral hook).
- **Teams pay per seat** for their private zoo, workspace and history.
- Honest note: team seats convert slower than $1 impulse buys, so the free viral Slopagotchi
  is what feeds the paid zoo.

## What we build (24h MVP)

| Layer | How |
|---|---|
| Auth | atproto OAuth → DID |
| Ingest | Tangled firehose + `git.getDiff` for connected repos |
| Slop score | Claude rates each diff → rolling Slopagotchi health |
| Slopagotchi | Pixel-art creature with health/evolution states |
| Zoo | Org workspace: every member's Slopagotchi, name and score |
| Storage | DB for MVP; Slopagotchi/score as PDS records as the atproto stretch |

---

*Team: William Störtebecker, Leonard Xander — Sunstead Hack, Levi, Finland.*
