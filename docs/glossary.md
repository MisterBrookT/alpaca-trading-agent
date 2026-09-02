# Glossary / 术语表

Bilingual running glossary for this project. Term stays English; meaning in plain Chinese.

| Term | 中文 | Plain meaning | Where it showed up |
| --- | --- | --- | --- |
| underlying | 标的物 | The asset an option is written on (SPY, IBIT, MSTR…) | choosing what to trade |
| exposure | 敞口 | How much your P&L moves when some risk factor moves; what you are "on the hook for" | IBIT gives Bitcoin exposure |
| proxy | 代理标的 | A tradable instrument used to get exposure to something you can't trade directly | MSTR as a levered BTC proxy |
| notional | 名义金额 | Full market value the position controls, not the cash you put up | 1 IBIT contract ≈ $4,378 notional |
| variance risk premium | 方差风险溢价 | The habitual gap between implied and later-realized vol; the seller's structural edge | MSTR +26.6 pts, IBIT +4.0 |
| iron fly | 铁蝶式 | Short straddle plus protective wings; credit smaller, loss capped | our chosen structure |
| wing | 保护腿 | The far OTM option bought purely to bound the tail | 135 call / 115 put |
| reward:risk | 盈亏比 | Credit collected divided by worst-case loss | ±$10 wing = 1.35 |
| gap risk | 跳空风险 | Price jumping while the market is closed, past any hedge | Wed night BTC move on MSTR |
| shortable / easy to borrow | 可做空 / 易借券 | Whether you can sell shares you don't own, cheaply | required for two-way delta hedge |
| leveraged proxy | 杠杆代理标的 | Instrument that amplifies another asset's moves | MSTR borrows to hold BTC |
| ETF (exchange-traded fund) | 交易所交易基金 | One ticker that holds a basket of assets | SPY = S&P 500 basket |
| call / put | 认购 / 认沽 | Right to buy / right to sell at the strike | `SPY260904C00762000` = C for call |
| strike price | 行权价 | The price the option lets you transact at | 762 in the code above |
| expiration date | 到期日 | The day the right disappears | 2026-09-04, our judging window |
| contract multiplier | 合约乘数 | 1 US equity option = 100 shares | $3.90 quote → $390 paid |
| premium | 权利金 | The option's price; buyer pays, seller collects | ATM SPY call premium $3.90 |
| bid / ask / spread | 买价 / 卖价 / 价差 | Best buy, best sell, and the gap you pay to cross | SPY $0.01 vs COIN $0.22 |
| ATM / OTM / ITM | 平值 / 虚值 / 实值 | Strike at / away from / inside the current price | ATM = strike ≈ spot |
| implied volatility (IV) | 隐含波动率 | The movement the market has *priced in*, annualised | SPY 17.5%, MSTR 97.9% |
| realized volatility | 已实现波动率 | The movement that actually happened | the bet: realized vs implied |
| delta | Delta | P&L sensitivity to a $1 move in the underlying | ATM call delta ≈ 0.50 |
| gamma | Gamma | How fast delta itself changes | SPY 0.040; forces re-hedging |
| theta | Theta | Value lost per day just from time passing | SPY ATM −$1.02/day |
| vega | Vega | P&L per 1 percentage-point change in IV | SPY ATM 0.225 |
| delta-neutral | Delta 中性 | Position hedged so direction stops mattering | strategy C |
| credit spread | 信用价差 | Sell one option, buy a cheaper protective one; loss capped | strategy A |
| straddle | 跨式 | Long/short both call and put at the same strike | strategy C sells it |
| 0DTE (zero days to expiry) | 零日到期 | Options expiring the same trading day | strategy B |
| paper trading | 模拟交易 | Simulated money, real market data | account PA3ZLVWUMG55 |
| buying power | 购买力 | Capital available to open positions | $400k on $100k equity (margin) |
| P&L (profit and loss) | 盈亏 | What you made or lost | judging criterion #1 |
| mark to market | 按市价计价 | Valuing an open position at current prices | how judges see Thursday's close |
| risk gate | 风控闸门 | Deterministic rules that veto the model's orders | our design's core idea |
| slippage | 滑点 | Extra cost from crossing the spread / moving price | 1¢/share in the simulator |
| vol crush | 波动率压缩 | IV collapsing after an event passes | why high-IV names are seductive |
| skew | 偏斜 | IV differing across strikes (puts usually richer) | limitation of our flat-IV model |
