# On/Offramp Solutions for Ukrainian Users & Founders

**Superteam Ukraine bounty** — https://superteam.fun/earn/listing/onofframp-solutions-for-ukrainian-users

**Deliverable:** Research spreadsheet + summary. Upload the companion CSV/XLSX to Google Sheets and link in submission form.

---

## Executive Summary

Ukrainian users face three recurring friction points when moving between UAH ↔ crypto ↔ USD/EUR:

1. **Banking & sanctions context** — international card rails are uneven; P2P and regional fintech bridges often beat direct US/EU on-ramps.
2. **KYC geography** — many global exchanges restrict or tier Ukrainian passports; local/regional providers (WhiteBIT, Kuna legacy paths, P2P) remain common.
3. **Solana-specific** — on-ramp is rarely chain-specific; off-ramp to UAH usually happens via CEX → bank/P2P, then users bridge to Solana via Jupiter/Allbridge.

---

## Spreadsheet Columns (use in XLSX)

| Column | Description |
|--------|-------------|
| Provider | Name |
| Type | CEX / P2P / Card / Ramp / OTC |
| On-ramp UAH | Yes/Partial/No |
| Off-ramp UAH | Yes/Partial/No |
| KYC level | None / Basic / Enhanced |
| UA passport accepted | Yes / Restricted / No (verify live) |
| Fees (typical) | % + fixed |
| Limits | Daily/monthly |
| Settlement speed | Instant / 1–3d |
| Solana support | Native / via swap |
| Notes | Risk, UX, founder use-case |

---

## Provider Matrix (March 2026 — verify before submit)

### Tier A — Most used by UA crypto natives

| Provider | On UAH | Off UAH | KYC | Solana | Notes |
|----------|--------|---------|-----|--------|-------|
| **WhiteBIT** | P2P + card (varies) | P2P → bank/card | Required | Deposit SOL, trade USDT | UA-founded exchange; strong local P2P liquidity |
| **Binance P2P** | USDT via P2P (UAH) | USDT → UAH P2P | Required | SOL withdraw | Availability changes; check TOS for UA |
| **Bybit P2P** | Similar to Binance | P2P off-ramp | Required | SOL supported | Compare P2P spreads vs WhiteBIT |
| **OKX P2P** | UAH pairs episodic | P2P | Required | SOL | Check regional app version |

### Tier B — Global ramps (founders receiving USD/EUR)

| Provider | On-ramp | Off-ramp | UA access | Solana |
|----------|---------|----------|-----------|--------|
| **MoonPay** | Card/Apple Pay | Limited sell | Region-dependent | Via partner wallets |
| **Transak** | Card/bank | Sell in supported regions | Check live | Phantom integration |
| **Banxa** | Card | Sell | Check live | Wallet partners |
| **Ramp Network** | Card | Sell EU/US | Often restricted for UA | Via embedded widgets |
| **Stripe (fiat)** | N/A for crypto | N/A | Business entity location matters | N/A |

### Tier C — Solana-native / DeFi path

| Path | Flow | Best for |
|------|------|----------|
| **CEX → Phantom** | UAH P2P → USDT on CEX → withdraw SOL/USDC to Phantom | Traders, bounty earners |
| **Jupiter + CEX** | Same, swap on-chain after deposit | DeFi users |
| **OTC / founder networks** | USDC wire → multisig | Startups raising abroad |
| **Payroll (Remote, Deel)** | Fiat salary → self-custody | Remote devs |

---

## Founder Playbook (UA → Solana startup)

1. **Incorporate / invoice entity** — EU/US entity often unlocks Stripe + Ramp; personal UA passport alone may block.
2. **Treasury** — USDC on Solana (Squads multisig) + small CEX hot wallet for UAH ops.
3. **Team payouts** — USDC on-chain beats repeated P2P for distributed teams.
4. **Compliance** — keep P2P receipts; avoid mixing personal/business P2P accounts.

---

## Risks & Disclaimers

- Provider policies change weekly; **verify KYC acceptance before listing as "Yes"**.
- P2P counterparty risk — use escrow, high-reputation merchants only.
- This document is research, not financial/legal advice.

---

## Submission checklist

- [ ] Convert table to **Google Sheets / XLSX** with all required columns from bounty scope
- [ ] Add 2–3 sentence intro for founders vs retail users
- [ ] Link sheet + this summary in Superteam form
- [ ] Wallet: `Do4v7foHJvRJLpRRoGaVPWX6DDEjX3yTK7J91gpwUQpE`
