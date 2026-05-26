# Versucture — SMC Trading Toolkit

> Smart Money Concepts (SMC) trading system with Pine Script indicators and Telegram-based real-time alerts.

This repository contains a **public demonstration** of the Versucture trading toolkit — a complete SMC trading system I designed and built starting in 2020, leading a 3-person development team. The full production code is proprietary, but the screenshots below show the indicator working on live charts.

---

## What it does

Versucture identifies high-probability trading setups using the **Smart Money Concepts (SMC)** methodology:

- **Market Structure** — detects Break of Structure (BOS) and Change of Character (CHoCH)
- **Order Blocks** — marks institutional supply/demand zones (Normal, SWS, SCOB Pattern, SOB)
- **Liquidity Sweeps** — identifies stop-hunt patterns and session sweeps (Tokyo, London, NY)
- **Point of Interest (POI)** — classifies high-probability entry zones (Structural, External, Live)
- **IDM Detection** — Inducement levels with Transfer Level (TRL) feature
- **Multi-timeframe validation** — analysis from HTF down to entry timeframe
- **Fair Value Gap (FVG)** — imbalance detection inside Order Blocks

---

## Live Examples

### 1. Market Structure Overview — BTC/USDT 1H

Full structural mapping with BOS, CHoCH, IDM levels, and Order Blocks across multiple weeks of price action.

![BTC 1H Overview](screenshots/01-overview-btc-1h.png)

### 2. Higher Timeframe Setup — BTC/USDT 5M

Order Block identified on the 5-minute chart, marked as the **H OB** (high-timeframe Order Block) — the zone where price is expected to react.

![BTC 5M Setup](screenshots/02-htf-setup-btc-5m.png)

### 3. Entry Execution — BTC/USDT 1M

After price entered the 5M Order Block, a refined entry was taken on the 1-minute timeframe using the inside Order Block + FVG, with confirmation candle. **Live P&L: 415.4, Risk/Reward: 11.18.**

![BTC 1M Entry](screenshots/03-entry-execution-btc-1m.png)

---

## Components

### 1. Pine Script Indicator (TradingView)

A custom indicator for TradingView that overlays SMC structures directly on price charts. Identifies all structural elements automatically across any symbol or timeframe.

### 2. Multi-Symbol Telegram Screener

A backend service that monitors multiple symbols across multiple timeframes simultaneously and sends real-time Telegram alerts when price interacts with key POIs.

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
- POI classification system (Structural, External, Live)
- Liquidity dynamics
- Entry confirmation logic (SCOB, FVG, IDM)

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
