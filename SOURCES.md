# SOURCES — every factual claim → its source

Rule honored from the bounty spec: *every technical claim must trace to the public
repos or live endpoints; measured claims only.* Sources were fetched during package
assembly (2026-09-12) and **re-verified against live state on 2026-09-29** (right
before filing). Where a claim carries a number, the number is the exact value from
the named snapshot, with the snapshot's own timestamp quoted.

| # | Claim(s) supported | Source | Verified via |
|---|--------------------|--------|--------------|
| S1 | 80,035.16 RTC total paid; 4,977 transactions; 1,322 unique recipients; methodology (confirmed+pending from founder payout wallets, voids/internal pools excluded) | https://rustchain.org/payouts.json (payload updated_at 2026-09-29T09:07:01Z) | direct fetch 2026-09-29; raw snapshot **shipped in-repo** at `data/payouts-snapshot-20260929.json` |
| S2 | Tutorial series pays 5 RTC per episode (up to 25 RTC for a 5-episode series) | https://github.com/Scottcjn/bottube/issues/647 — title "[BOUNTY: 5 RTC/episode] Create a Tutorial Series (3+ episodes on any tech topic)"; body: "5 RTC per episode (up to 25 RTC for a 5-episode series)" | issue open, title + body re-read 2026-09-29. URL correction 2026-09-29: this bounty lives on the **bottube** repo — the assembly-time citation pointed at the rustchain-bounties mirror, where #647 has since been recycled by test issues |
| S3 | PPA explainer video pays 10 RTC | https://github.com/Scottcjn/bottube/issues/644 — title "[BOUNTY: 10 RTC] Create a "What is Proof of Physical AI?" Explainer Video" | issue open, title re-read 2026-09-29 (same URL correction as S2) |
| S4 | Payouts to self-custody wallets; RTC-format address required ("RTC… format — bare handles strand the balance"); address derived from own keypair | https://github.com/Scottcjn/rustchain-bounties/issues/509 (📌 FAQ — RTC Bounty Payouts, Wallets, and Off-Ramps) + claim instructions in #16601 body | issue open, re-verified 2026-09-29 |
| S5 | Over a hundred open bounty issues | https://github.com/Scottcjn/rustchain-bounties/issues (open issue list) | re-checked 2026-09-29 via search API: **981 open** (claim hedged as "over a hundred" by design) |
| S6 | Distribution round: Package A (YouTube full production kit) = 40 RTC, first 5 accepted, +20 traction bonus; package contents (script.md, voiceover/, visuals/, assembly.md, thumbnail+2, metadata.md, SOURCES.md); claim = public repo + comment with RTC address | https://github.com/Scottcjn/rustchain-bounties/issues/16601 — body re-read 2026-09-29: A=40 RTC / first 5 accepted / +20 traction all present | issue page re-fetched 2026-09-29 |
| S7 | Security reports (e.g. unauthenticated IDOR on wallet balance/history endpoints) target the HIGH tier — 25 RTC reward request | https://github.com/Scottcjn/rustchain-bounties/issues/16941 (SECURITY: IDOR — Unauthenticated Wallet Balance & Transaction History Disclosure) | issue open, re-verified 2026-09-29; framed as a reward REQUEST, not a confirmed payout |
| S8 | Micro-bounty example: 0.1 RTC for a written answer ("Why did you choose to work on an Elyan Labs repo?") | https://github.com/Scottcjn/rustchain-bounties/issues/16863 — "[MICRO-BOUNTY: 0.1 RTC] Why did you choose to work on an Elyan Labs repo?" | issue open, re-verified 2026-09-29 |
| S9 | Worked pipeline example: 5 tutorial episodes, 466 seconds total produced by this desk (102.9 + 83.0 + 80.6 + 91.8 + 107.7 s), uploaded via agent API, awaiting human review | Own production logs in `artifacts/botube-647/` (specs, build + upload response JSON); upload receipts from BoTTube agent API (agent id 1756) | local artifacts + API 201 responses, 2026-09-11 (first-party; status re-checked against the desk ledger 2026-09-29 — still awaiting review) |
| S10 | Payout ledger distinguishes queued / pending / confirmed states | https://github.com/Scottcjn/rustchain-bounties/issues/104 — "[LEDGER] Bounty Payout Ledger — Queued / Pending / Confirmed" | issue re-verified 2026-09-29 (now closed: the ledger practice it documented is standing policy) |

## Verification notes

- Numbers in narration were re-read from the live payloads **on the day of the
  latest verification (2026-09-29)** and are phrased with the exact values from
  the sources (no rounding beyond what the source itself prints, e.g. "80,035+"
  on the endpoint vs exact 80,035.16 in JSON). The raw JSON snapshot ships with
  this package at `data/payouts-snapshot-20260929.json` so every number is
  checkable offline.
- S7 is deliberately framed as "reports target the HIGH tier (25 RTC)" because the
  referenced issue is another researcher's reward request, not a confirmed payment.
- S9 is first-person, first-party evidence: our own uploads and logs, with statuses
  stated honestly ("awaiting review" at filing time).
- Anything not directly observable was either omitted or hedged ("over a hundred").
- History: the assembly-time snapshot (2026-09-11) read 76,658.61 / 4,394 / 1,219;
  the 2026-09-29 refresh supersedes it everywhere in this package (script, stats
  card, metadata, README). Older numbers appearing anywhere would be an error —
  please flag it.
