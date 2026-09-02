# alpaca-trading-agent

Entry for the **Alpaca AI Trading Agents Hackathon** (lablab.ai, 28 Aug – 4 Sep 2026).

- Submission deadline: **Sep 4, 11:00 PM CST**
- Format: online, 7 days, $6,300 prize pool
- Required stack: Alpaca Trading API / Alpaca MCP server / Alpaca CLI (paper trading)
- Event page: https://lablab.ai/ai-hackathons/alpaca-ai-trading-agents-hackathon

## Status

Screening form submitted (Sep 2). Awaiting approval email from lablab.ai.
Repo scaffolded. No implementation yet — design first.

## Hard requirements (from the event page)

- Autonomous AI trading agent on Alpaca's **Trading API**
- MUST use Alpaca's **MCP server or CLI**
- MUST incorporate **options trading**
- Final submission MUST run on a **brand-new** paper account, starting balance **$100,000**
  (reused accounts are ineligible for judging)
- One-page write-up: AI logic, risk gates, Alpaca infrastructure
- Register on the lablab.ai **Discord** too
- Optional: up to 5 social posts (X/LinkedIn, tag @lablabai + @AlpacaHQ) → 2 × $500 social prize

## How it's judged

Not a backtest — **live paper-trading P&L on the fresh account**, identified by the
Alpaca paper account ID submitted with the project. Criteria:

1. **P&L performance** — real trading activity during the event window
2. **Technology implementation** — Trading API + MCP/CLI usage
3. **Creativity & originality** — strategy and agent behaviour
4. **Presentation & execution** — demo clarity, stated reasoning
5. **Social engagement** — quality + reach of the ≤5 posts

Submission package: title, short + long description, tags, cover image, video
presentation, slides, public GitHub repo, demo URL, **Alpaca paper account ID**,
≤5 social links. Teams 1–6 people.

Timing constraint: deadline Sep 4, 23:00 China time ≈ 11:00 UTC, i.e. **before the
US cash session opens on Sep 4**. Only the **Sep 3 session** (plus overnight/crypto)
is realistically available for live P&L.

## Direction (draft)

LLM agent over the Alpaca MCP server with a **deterministic risk gate** between signal
and execution: the model proposes orders, hard-coded rules (position size, max notional,
daily loss cap, symbol allowlist) accept or reject, every decision is audit-logged.
Paper account only.

## Notes

- Existing submissions already cluster on "LLM + indicators + risk gate" (Sentinel,
  SentinelTrade, Autonomous Options Desk). Differentiation must come from the
  verifiable-execution/audit angle or a genuinely different signal source, not from
  another RSI wrapper.
