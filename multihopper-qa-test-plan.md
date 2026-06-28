# MultiHopper Agentic Flow — QA Test Plan

**Superteam bounty** — https://superteam.fun/earn/listing/break-it-before-users-do-multihopper-agentic-flow-bugs-and-fixes

**Prize pool:** 1,000 USDC (4 × 250 USDC for top findings)

---

## Scope

Responsible security/QA testing of **MultiHopper API** in **agentic workflows** — multi-hop token routing on Solana for AI agent integrators.

---

## Test Environment Setup

1. Obtain MultiHopper API access / docs from listing POC
2. Solana devnet or mainnet-fork wallet with small SOL + test tokens
3. Agent harness (Python/TS) that can:
   - Call route creation endpoints
   - Simulate agent retry loops
   - Log request/response + tx signatures

---

## Test Matrix

| # | Category | Test case | Expected |
|---|----------|-----------|----------|
| 1 | Input validation | Empty hop path | 400 + clear error, no partial route |
| 2 | Input validation | Invalid mint addresses | Reject before on-chain attempt |
| 3 | Input validation | Zero/negative amounts | Reject |
| 4 | Slippage | Max slippage exceeded mid-route | Fail cleanly; no stuck funds |
| 5 | Agent loop | Same failed request retried 50× | Rate limit or idempotency key |
| 6 | Agent loop | Concurrent duplicate routes from one agent | Dedupe or reject duplicates |
| 7 | Partial fill | Hop 2 fails after hop 1 succeeds | Document recovery / rollback path |
| 8 | RPC failure | 503 from RPC during simulation | Retry with backoff; no double-spend |
| 9 | Timeout | Agent cancels mid-flight | State query shows accurate status |
| 10 | Auth | Missing/invalid API key | 401, no route leakage |
| 11 | Auth | Expired session token | 401 with refresh hint |
| 12 | Response shape | Malformed JSON / HTML error page | Parser error, not silent success |
| 13 | Logging | PII / private keys in error responses | Must not appear |
| 14 | Edge | Single-hop degenerate path | Works or explicit unsupported |
| 15 | Edge | Max hops exceeded | Reject with limit in message |

---

## Agentic Workflow Scenarios

### Scenario A — Tool-calling agent
Agent receives user intent "swap A→B→C via MultiHopper". Verify:
- Tool schema matches API
- Failed tool call doesn't hallucinate success
- Agent can query route status after submit

### Scenario B — Autonomous retry bot
Simulate buggy agent that retries on any error. Verify:
- No runaway tx spam
- Cost bounds / circuit breaker

### Scenario C — Parallel agents
Two agents same wallet, same route. Verify:
- No nonce collision / duplicate execution

---

## Report Template (per finding)

```markdown
## Finding: [title]
**Severity:** Critical / High / Medium / Low
**Steps:** 1…n
**Expected:** …
**Actual:** …
**Evidence:** logs, tx sig, screenshot
**Suggested fix:** …
```

---

## Submission

- File issues or consolidated report per bounty rules
- Wallet: `Do4v7foHJvRJLpRRoGaVPWX6DDEjX3yTK7J91gpwUQpE`
- **Dev/QA bounty** — run tests against live/staging API

---

*Prepared as submission scaffold — execute tests against MultiHopper API for ranked prizes.*
