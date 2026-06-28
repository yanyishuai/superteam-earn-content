# Superteam Nepal Mini Hack — Project Proposal

**Bounty** — https://superteam.fun/earn/listing/superteam-nepal-mini-hack | **$850**

---

## Project: Solana Bounty Tracker Mini-App

**One-liner:** Mobile-friendly PWA that aggregates **your** open earn opportunities (Superteam + GitHub PRs + wallet balance) in one dashboard.

**Why this problem:** Builders in Nepal (and globally) miss deadlines because bounties live across Superteam, GitHub, and MergeWork — no single view.

---

## Stack

| Layer | Choice |
|-------|--------|
| Frontend | Next.js or Vite + React (mobile-first) |
| Wallet | Phantom adapter |
| Data | Public APIs only (Superteam listings, GitHub search) |
| Deploy | Vercel / Cloudflare Pages |

---

## MVP Features (48h build)

1. **Dashboard** — open bounties sorted by deadline + reward
2. **Wallet strip** — SOL/USDC balance via RPC (`Do4v7fo…` optional connect)
3. **GitHub PR tracker** — paste username → show open PRs with `/bounty` amounts
4. **Deadline alerts** — local notification 24h before due
5. **Submit checklist** — per-bounty notes + link field

---

## Solana Native Angle

- Read-only wallet connect (no custody)
- Optional: show recent bounty payout txs from `getSignaturesForAddress`
- Uses Solana JSON-RPC for balance — demonstrates ecosystem integration

---

## Deliverables

- [ ] Public repo: `yanyishuai/solana-earn-dashboard` (or similar)
- [ ] Live demo URL
- [ ] 2-min Loom walkthrough
- [ ] README with setup

---

## Wallet

`Do4v7foHJvRJLpRRoGaVPWX6DDEjX3yTK7J91gpwUQpE`

---

*Proposal doc — implement repo + demo for hack submission.*
