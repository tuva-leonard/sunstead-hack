# Builder Score

**A portable, verifiable developer reputation — built from your real code on the AT Protocol.**

Challenge: *Tools for Builders on Tangled* (Sunstead Hack 2026).
Goal: not just a demo — **prove real demand by selling 50 × $20 plans within 24 hours.**

## The idea

On GitHub, your contribution history is locked inside GitHub — you don't own it and
no one can build on top of it. On the AT Protocol, your repos, pull requests and commits
are **public records that you own**, spread across the whole network.

Builder Score turns that into a product. An AI agent reads your real code on Tangled
(no API keys, no rate limits), scores it, and writes the result back as a record **you own
on your own PDS** — a reputation you can take anywhere.

## How it works

1. **Sign in** with your AT Protocol / Bluesky identity (OAuth).
2. **The agent reads your code** via Tangled's read APIs (`listRepos`, `git.getLog`,
   `git.getDiff`, `git.getTree`) and analyses it with Claude.
3. **Free:** your Builder Score + one teaser line about your coding style.
4. **$20 unlocks:** a full AI code review, a shareable score card, an auto-posted
   Bluesky thread, and a **verifiable reputation record** minted to your own PDS.

## Why it sells in 24 hours

The product markets itself. Every paid score card is posted to Bluesky and tags the
developer — their network sees it and wants their own. Free score in, paid card out:
**one sale brings the next.** The AT Protocol *is* the distribution channel.

## Why it fits the challenge

- **Only possible on atproto:** portable public records + identity + social graph.
- **Leans on the primitives** instead of rebuilding infrastructure.
- **Agents as first-class citizens** — the agent reads, judges, and writes records.
- Original and inspiring: *own your developer reputation.*

## What we build

| Layer | How |
|---|---|
| Auth | atproto OAuth → DID |
| Read code | Tangled read XRPC (no rate limits) |
| Score + review | Claude over diffs and commit history |
| Owned reputation | `com.atproto.repo.createRecord` on the user's PDS |
| Distribution | Auto-posted Bluesky card |
| Payment | Stripe Checkout in front of the unlock |

---

*Team: William Störtebecker, Leonard Xander — Sunstead Hack, Levi, Finland.*
