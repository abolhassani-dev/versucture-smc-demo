# Versucture — SMC Trading Toolkit (Demo)

> Smart Money Concepts (SMC) trading system with Pine Script indicators and Telegram-based real-time alerts.

This repository contains a **public demonstration** of the Versucture trading toolkit — a complete SMC trading system I designed and built starting in 2020, leading a 3-person development team. The full production version is proprietary, but this demo showcases the core ideas and the indicator's visual output.

---

## What it does

Versucture identifies high-probability trading setups using the **Smart Money Concepts (SMC)** methodology:

- **Market Structure** — detects Break of Structure (BOS) and Change of Character (CHoCH)
- **Order Blocks** — marks institutional supply/demand zones - 4 Diffrent Type of OBs . 
- **Liquidity Sweeps** — identifies stop-hunt patterns
- **Point of Interest (POI)** — classifies high-probability entry zones
- **Entry Confirmations** — multi-timeframe validation logic
- **Many More Options ** — Custome ZigZag - Fibo Levels For Confirm The High/Lows - Sessions - Reply for Backtesting and many more . 

---

## Components

### 1. Pine Script Indicator (TradingView)

A custom indicator for TradingView that overlays SMC structures directly on price charts. This demo version implements **Order Block detection** as a representative sample of the methodology.

See: `order-block-demo.pine`

### 2. Multi-Symbol Telegram Screener

A backend service that monitors multiple symbols across multiple timeframes simultaneously and sends real-time Telegram alerts when price interacts with key POIs.

> **Note:** The screener source is proprietary, but the architecture is shown below.

**Architecture:**
TradingView Webhook → Alert Router → Symbol/Timeframe Filter
→ POI Validation
→ Telegram Bot API → User

**Example alert (Telegram):**
🎯 POI TOUCH — XAUUSD 5m
Type: Bullish Order Block
Zone: 2,348.40 – 2,351.20
Status: Awaiting confirmation
Time: 14:32 UTC

### 3. SMC Methodology Documentation

I authored the complete methodology covering:
- Market structure rules (BOS, CHoCH definitions)
- POI classification system
- Liquidity dynamics
- Entry confirmation logic

---

## Why this exists

Most retail traders fail because they react to price without understanding **why** institutions move markets. SMC frames trading as following institutional liquidity hunts rather than chasing patterns. Versucture operationalizes that framework into a repeatable, monitorable system.

---

## Tech stack

| Layer | Tool |
|-------|------|
| Indicator | Pine Script v6 (TradingView) |
| Screener | Custom backend (proprietary) |
| Delivery | Telegram Bot API |
| Hosting | Linux VPS |

---

## Status

- Live & operational since 2020
- Production-grade with multi-user delivery
- 3-person development team led

---

## Author

**Hamidreza Abolhassani** — Founder, Strategy Owner, Technical Lead
Email: hr.dev.abolhassani@gmail.com
