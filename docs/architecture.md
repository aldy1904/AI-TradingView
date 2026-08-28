# Architecture — V0.2

## Purpose

V0.2 is a proof-of-concept for manual TradingView visualization, optimized for clean setup-level review on instruments such as XAUUSD. It adds a local setup canvas: trade levels, supply and demand zones, trendline, EMAs, and labels are rendered only around a configurable recent anchor rather than across the full chart.

## Components

- **Pine visualization:** accepts manual values and renders a local setup area.
- **Configuration schema:** reserves a non-operational contract for a future analysis result.
- **API placeholder:** documents the future boundary only.

## Future analysis-to-visualization mapping

V0.2 is intentionally manual. A future bridge would map an analysis result to the following Pine visualization fields:

| Future analysis parameter | V0.2 visualization target |
| --- | --- |
| symbol | The TradingView chart symbol where the indicator is applied |
| timeframe | The TradingView chart timeframe where the indicator is applied |
| direction | Direction input (Long or Short) |
| entry | Entry input and local entry line |
| stop_loss | Stop Loss input and local stop line |
| tp1 | Derived from exact risk × 1.5, then shown as the TP1 line |
| tp2 | Derived from exact risk × 2.0, then shown as the TP2 line |
| supply_zone | Supply top and Supply bottom inputs and supply box |
| demand_zone | Demand top and Demand bottom inputs and demand box |
| trendline_coordinates | Trendline start/end bar offsets and start/end price inputs |
| analysis_labels | Setup label input and setup label object |

The setup anchor and level length determine the local bar range used for trade lines and zones. A bridge must translate any timestamp-based setup coordinates into the chart's applicable bar positions.

## Explicit non-goals

- No AI analysis engine
- No external API bridge
- No broker connectivity
- No automated trading
- No order placement or execution

## Future bridge boundary

Pine Script does not directly receive arbitrary external HTTP responses. ChatGPT-to-TradingView communication requires a separately designed, secure transport and an ingestion pattern that TradingView supports. That work is intentionally out of scope for V0.2.
