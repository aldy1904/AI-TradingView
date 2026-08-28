# AI TradingView Analyzer — V0.1

A proof-of-concept TradingView visualization project.

## Scope

V0.1 provides a manually configurable Pine Script v6 overlay for visualizing:

- entry, stop loss, TP1 (1:1.5), and TP2 (1:2)
- supply and demand zones
- a trendline
- EMA 50 and EMA 200
- optional labels

This release is intentionally visualization-only. It does **not** include automated trading, order execution, an AI analysis engine, or an external API bridge.

## Repository layout

- `pine/` — TradingView Pine Script visualization
- `api/` — reserved documentation for a future API boundary
- `config/` — the future analysis-result schema
- `docs/` — V0.1 architecture notes

## Usage

Open `pine/AI_Trading_Analyzer_V0_1.pine` in TradingView's Pine Editor, add it to a chart, and manually adjust the inputs to test the visualization canvas.

> Educational and visualization use only. This is not trading advice.
