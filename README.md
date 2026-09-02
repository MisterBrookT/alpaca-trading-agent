# alpaca-trading-agent

Entry for the **Alpaca AI Trading Agents Hackathon** (lablab.ai, 28 Aug – 4 Sep 2026).

- Submission deadline: **Sep 4, 11:00 PM CST**
- Format: online, 7 days, $6,300 prize pool
- Required stack: Alpaca Trading API / Alpaca MCP server / Alpaca CLI (paper trading)
- Event page: https://lablab.ai/ai-hackathons/alpaca-ai-trading-agents-hackathon

## Status

Repo scaffolded. No implementation yet — design first.

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
