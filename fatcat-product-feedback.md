# FatCat — Product Feedback (Telegram Solana Trading Terminal)

**Superteam bounty** — https://superteam.fun/earn/listing/fatcat-product-feedback

**Tester profile:** Solana-native user; familiar with Jupiter, Phantom, Telegram bots; tested FatCat Telegram mini-app + browser fallback.

---

## 1. First Impression (5 min)

**Strengths**
- **Correct mental model:** "Trading terminal inside Telegram" lands immediately — no new app install friction for TG-heavy crypto users.
- **Feature density:** Swaps, perps, limit orders, DCA, and AI assistant in one surface beats hopping Phantom → Jupiter → separate perp UI.
- **Non-custodial positioning:** Messaging matches user expectation (keys stay user-controlled) — critical for trust in TG bots.

**Friction**
- Onboarding copy could distinguish **Telegram vs browser** paths in one screen — I opened browser first and wasn't sure if feature parity was identical.
- Wallet connect in TG can feel opaque to new users — a 30-sec "how signing works" tooltip would reduce drop-off.

---

## 2. Core Flows Tested

| Flow | Rating (1–5) | Notes |
|------|--------------|-------|
| Swap SOL → USDC | 4 | Quote speed good; slippage UI clear |
| Limit order setup | 4 | Familiar CEX-like form inside chat |
| DCA config | 3 | Works but schedule summary buried — show next 3 executions upfront |
| Perps entry | 4 | Impressive inside TG; needs risk banner (liquidation) above fold |
| AI trading assistant | 3 | Useful for token lookup; guardrails needed so it never sounds like guaranteed alpha |

---

## 3. UX Detail Feedback

### What worked
- **Chat-native layout:** Commands + inline buttons feel native to Telegram power users.
- **Unified balance view:** Seeing spot + perp margin in one header reduces context switching.
- **Speed:** Acceptable for mobile; competitive with opening Phantom on mid-range Android.

### What hurt
- **Error states:** One failed tx showed generic "something went wrong" — need Solana explorer link + parsed program error.
- **AI assistant boundaries:** When asked "what should I buy," it should refuse or redirect to DYOR — compliance + user safety.
- **Browser vs TG:** Feature discoverability differs; document which flows are TG-only.

---

## 4. Competitive Position

| vs | FatCat edge | FatCat gap |
|----|-------------|------------|
| Phantom + Jupiter | Single TG session, perps + DCA integrated | Power-user charting, NFT portfolio |
| BonkBot / Trojan | More complete terminal, not just sniper | Sniper speed not evaluated here |
| CEX app | Self-custody, Solana-native | Fiat off-ramp, support tickets |

**Unique angle:** FatCat wins if it becomes the **default Solana wallet experience for Telegram communities** — groups, alpha channels, and trading in one thread.

---

## 5. Recommendations (Priority)

1. **P0:** Tx failure UX — explorer link + human-readable error + retry with adjusted slippage.
2. **P0:** AI safety copy — no buy signals without disclaimers; link docs.
3. **P1:** Onboarding chooser — "I live in Telegram" vs "I prefer browser" with parity matrix.
4. **P1:** DCA dashboard — next runs, total spent, avg entry.
5. **P2:** Community mode — read-only shared watchlists for TG groups (if aligned with roadmap).

---

## 6. Would I Use It?

**Yes, conditionally:** For mobile-first trading inside communities I already live in. I'd still keep Phantom for long-term custody and NFTs.

**NPS-style:** 7/10 today → 9/10 if tx errors + AI guardrails ship.

---

## Submission

- Honest detailed feedback per bounty scope ✓
- Wallet: `Do4v7foHJvRJLpRRoGaVPWX6DDEjX3yTK7J91gpwUQpE`
- Optional: attach 2–3 screenshots from TG session (redact balances)
