# Roast My Repo

**Paste your repo. Our AI roasts your code. Flex the card on Bluesky.**

Challenge: *Tools for Builders on Tangled* (Sunstead Hack 2026).
Goal: the simplest thing we can possibly sell — **50 × $20 within 24 hours.**

## The idea

One page. One input. One button.

1. Paste a Tangled (or GitHub) repo URL.
2. Our AI reads the code and writes a savage — but lovingly accurate — roast.
3. See it blurred for free. **$20 reveals the full roast + a shareable card.**

That's the whole product. No login, no setup, no explaining.

## Why it's idiotically simple to ship

Tangled's read API is **open, with no auth and no rate limits.** We don't need
sign-in, accounts, or PDS writes — we just read the public repo and let Claude cook.

| Layer | How |
|---|---|
| Read code | Tangled read XRPC (`git.getDiff`, `git.getLog`) — no auth, no limits |
| Roast | Claude over the diff and commit history |
| Card | Auto-generated image, sized for Bluesky |
| Payment | Stripe Checkout to reveal |

## Why it sells in 24 hours

Roasts are made to be shared. Every paid card gets posted to Bluesky and tags the
developer — their friends see it, laugh, and want theirs. **One roast brings the next.**
The AT Protocol *is* the distribution channel.

## Why it fits the challenge

- Leans entirely on Tangled's open primitives — reads public repos, posts to the
  social graph, reinvents nothing.
- Original and playful (the brief literally invites "playful" ideas).
- Optional upgrade: mint the roast as a record on the user's PDS so they own it.

---

*Team: William Störtebecker, Leonard Xander — Sunstead Hack, Levi, Finland.*
