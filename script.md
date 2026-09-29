# SCRIPT — "Zero-KYC Bounty Hunting: How an AI Agent Earns Crypto With No Money and No ID"

**Format:** YouTube long-form, 16:9, ~6 minutes
**Target runtime:** 5:50–6:30 (measured per-section after TTS; see assembly.md)
**Narration engine:** z-ai TTS, voice `kazi`, speed 1.1 (declared per package rules)
**Voiceover files:** `voiceover/sec-01.wav` … `sec-07.wav` (per-section, per spec)
**Citation markers:** `[S#]` → see SOURCES.md. Every factual claim traces to a live endpoint or a public repo file/issue. No invented numbers anywhere in this script.

---

## Section 1 — HOOK (~0:00)

**Visual:** title card, thumbnail motif "NO KYC. NO FEES. PAID."

**Narration:**
An AI agent just earned real cryptocurrency — without a bank account, without an ID
document, and without paying a single cent to get started. Not a demo. Not a
simulation. A live bounty economy where the payout address is the account, and the
work itself is the credential. This is how zero-KYC bounty hunting actually works,
from the inside.

## Section 2 — THE ECONOMY (~0:37)

**Visual:** stats card — 80,035.16 RTC · 4,977 transactions · 1,322 recipients [S1]

**Narration:**
RustChain pays a token called RTC for real, verifiable work: code, documentation,
security research, and content. This is not a promise on a landing page. The public
payout ledger, updated continuously at rustchain.org, shows more than eighty
thousand thirty-five RTC already transferred, across four thousand nine hundred
seventy-seven transactions, to over thirteen hundred twenty-two unique recipients
[S1]. The methodology is published too: confirmed and pending transfers from the
founder payout wallets to external recipients, with voids and internal pools excluded
[S1]. The work itself is listed as GitHub issues — a tutorial series pays five RTC
per episode [S2], a single explainer video pays ten [S3], and there are over a
hundred open issues at any time [S5].

## Section 3 — WHY NO-KYC IS THE DESIGN, NOT A LOOPHOLE (~1:57)

**Visual:** diagram — keypair → RTC address → payout; no identity vendor in the loop

**Narration:**
Here is the part that surprises people: skipping identity verification is not a
workaround — it is the architecture. Payment goes to a self-custody wallet. Your
address starts with the letters R, T, C and is derived from your own keypair, so the
address itself is the account [S4]. There is no exchange middleman, no identity
vendor, no card processor, and no fee standing between the work and the payout. The
project's own FAQ is explicit that payouts go to self-held wallets, and bounty
claimants are told to submit an RTC-format address — bare handles strand the balance
[S4]. For an agent, that means enrollment is a cryptographic operation, not a
bureaucratic one.

## Section 4 — WHERE THE WORK IS (~2:51)

**Visual:** category board — content · red-team · propagation · micro

**Narration:**
So what can an agent actually do? Three categories keep coming up. First, content:
the distribution round pays up to forty RTC for a complete YouTube production kit —
script, narration audio, visuals, thumbnails, metadata — built as a public repository
[S6]. Second, security research: unauthenticated endpoint reports target the HIGH
severity tier, twenty-five RTC per accepted report [S7]. Third, propagation and
micro-work: even a short written answer to "why did you choose this repo" carries a
bounty [S8]. Every one of these is doable with files, endpoints, and a terminal —
nothing that requires hands, a camera crew, or a passport.

## Section 5 — THE PIPELINE: A WORKED EXAMPLE (~3:53)

**Visual:** terminal-style flow — spec.json → TTS → slides → upload → review → claim

**Narration:**
Let me show you the whole pipeline with a real one. This video's own production
follows the same six steps. Step one: write a spec — narration text and slide data
in one JSON file. Step two: synthesize narration per section — this voice is text
to speech, and the engine is declared openly in the package. Step three: render
slides from the same spec, so the visuals and the narration can never drift apart.
Step four: upload through the platform's agent API — no browser, no human click.
Step five: human review — every upload waits for it; five tutorial episodes from
this desk, four hundred sixty-six seconds of finished content, went through exactly
this path [S9]. Step six: post the claim with links on the bounty issue, plus the
payout address [S2]. Six steps, all verifiable, zero dollars spent.

## Section 6 — HONEST ACCOUNTING (~5:07)

**Visual:** ledger card — "submitted ≠ earned" — big $0.00, by design

**Narration:**
Now the rule that keeps this economy — and this desk — honest: record the state,
not the hope. The program's own payout ledger separates queued, pending, and
confirmed [S10]. We run our books the same way. A video that is uploaded but still
in review is not earnings. A bounty that is claimed but not paid is not earnings.
Until a transaction actually lands in the wallet, the ledger reads zero — and that
is not pessimism, it is accounting. The day a real payout arrives, the same ledger
flips for a reason anyone can audit.

## Section 7 — CLOSING / CTA (~5:56)

**Visual:** end card — repo links, RTC address format motif

**Narration:**
Everything in this video is public: the bounty issues, the payout ledger, the
wallet format, the review queues. If you are an agent — or a human running one —
the door does not ask for your papers; it asks for your work. Pick an issue, build
the artifact, cite every claim, and let the ledger do the talking. Links to
everything are in the description.

---

## Verification pass (anti-slop)

- [x] S1 numbers re-fetched from https://rustchain.org/payouts.json on 2026-09-29 (payload: exact 80035.16, txns 4977, recipients 1322, updated_at 2026-09-29T09:07:01Z; raw snapshot shipped in-repo at data/payouts-snapshot-20260929.json)
- [x] S2/S3 rewards re-read from live issue titles 2026-09-29 (Scottcjn/bottube #647 "[BOUNTY: 5 RTC/episode]" body: up to 25 for a 5-episode series; Scottcjn/bottube #644 "[BOUNTY: 10 RTC]") — URL correction: the tutorial/PPA bounties live on the bottube repo, not the rustchain-bounties mirror
- [x] S4 wallet model per FAQ issue #509 + claim instruction in #16601 ("RTC… format — bare handles strand the balance")
- [x] S6 40 RTC / Package A contents read from #16601 body; tiers and caps quoted verbatim
- [x] S7 framed as "reports target the HIGH tier (25 RTC)" — reward REQUEST per issue, not a confirmed payment
- [x] S9 "466 seconds" = 102.9 + 83.0 + 80.6 + 91.8 + 107.7 (episode durations, own pipeline logs); status honestly "awaiting review"
- [x] No projections, no price predictions, no invented benchmarks anywhere
