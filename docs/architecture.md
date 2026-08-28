# Architecture — V0.1

## Purpose

V0.1 is a proof-of-concept for manual TradingView visualization. The Pine Script runs entirely in TradingView and renders configurable levels, zones, a trendline, moving averages, and labels.

## Components

- **Pine visualization:** accepts manual inputs and displays them on a chart.
- **Configuration schema:** reserves a small, non-operational contract for a future analysis result.
- **API placeholder:** documents the future boundary only.

## Explicit non-goals

- No AI analysis engine
- No external API bridge
- No broker connectivity
- No automated trading
- No order placement or execution

Any future implementation should preserve the separation between analysis, visualization, and execution.
