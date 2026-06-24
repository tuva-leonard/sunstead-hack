# Roast My Repo

**Paste a repo. Our AI roasts the code. $1. Do it for the lols.**

Challenge: *Tools for Builders on Tangled* (Sunstead Hack 2026).
Goal: price it so low it's an impulse — **hundreds of $1 roasts in 24 hours.**
Traction isn't 50 paying users; it's *how many* couldn't resist.

## The idea

One page. One input. One button.

1. Paste any Tangled (or GitHub) repo URL — yours, or a friend's.
2. Our AI reads the code and writes a savage — but lovingly accurate — roast.
3. See it blurred for free. **$1 reveals the full roast + a shareable card.**

That's the whole product. No login, no setup, no explaining. A dollar to laugh.

## The lols engine

The killer move: **roast someone else's repo.** Because Tangled's read API is open,
any public repo works. Pay $1, roast your friend's code, send them the card. They
laugh, they get offended, they roast you back. The fight *is* the marketing.

## Why it's idiotically simple to ship

Tangled's read API is **open, with no auth and no rate limits.** No sign-in, no
accounts, no PDS writes — we read the public repo and let Claude cook.

| Layer | How |
|---|---|
| Read code | Tangled read XRPC (`git.getDiff`, `git.getLog`) — no auth, no limits |
| Roast | Claude over the diff and commit history |
| Card | Auto-generated image, sized for Bluesky |
| Payment | Stripe Checkout — $1, one tap |

## Why it sells in 24 hours

At $1, there's nothing to decide. Every paid card gets posted to Bluesky and tags the
developer — friends see it, laugh, and roast each other back. **One roast starts a fight,
and the fight sells the next ten.** The AT Protocol *is* the distribution channel.

## Why it fits the challenge

- Leans entirely on Tangled's open primitives — reads public repos, posts to the
  social graph, reinvents nothing.
- Original and playful (the brief literally invites "playful" ideas).
- Optional upgrade: mint the roast as a record on the user's PDS so they own it.

---

*Team: William Störtebecker, Leonard Xander — Sunstead Hack, Levi, Finland.*
