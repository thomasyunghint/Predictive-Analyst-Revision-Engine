# PARE — Predictive Analyst Revision Engine

**Cross-Lingual Assumption Stress-Testing for EV/Battery Supply Chains**

[**→ Live Demo**](https://thomasyunghint.github.io/Predictive-Analyst-Revision-Engine/)

---

## What It Does

Sell-side analysts covering U.S. EV and battery companies anchor to management guidance between earnings calls — even when external data contradicts their models. This is not an information access problem. It is a causal reasoning problem: most analyst frameworks lack the cross-supply-chain links to connect Chinese supplier economics to U.S. company line items.

PARE performs the causal reasoning that analysts skip:

1. **Decompose Consensus** — Extracts embedded assumptions from U.S. earnings call transcripts (e.g., "lithium costs stabilized" → COGS flat QoQ)
2. **Test Against Chinese Ground Truth** — Ingests Mandarin-language sources (CATL filings, MIIT/MOFCOM policy announcements, lithium spot indices) and extracts corresponding data points
3. **Identify the Breaking Assumption** — Traces the causal chain from Chinese supplier data to specific U.S. company line items and quantifies the gap vs. consensus
4. **Output** — Generates a falsifiable, traceable prediction: which assumption is breaking, the evidence source, the affected line item, and implied magnitude

## Demo Case: Tesla Q1 2025

The live demo walks through a fully traced historical case:

- **Apr 22** — Tesla CFO states lithium costs "stabilized" on earnings call
- **Apr 29** — CATL Q1 filing (Mandarin) reports lithium carbonate cost +12-15% QoQ
- **Apr 29** — PARE flags divergence: consensus COGS assumption is stale
- **May 14-22** — Sell-side analysts revise downward (Morgan Stanley, Goldman Sachs)
- **Result** — 23-day lead over consensus with correct direction, line item, and magnitude

## Why This Works

The system's edge is structural information asymmetry: source data is in Mandarin, affected analysts operate in English, and the causal chain (Chinese policy → supplier cost → OEM margin) is absent from most sell-side models.

## Tech Stack

Python, Claude API (structured extraction from English and Mandarin), requests/BeautifulSoup, pandas, FastAPI

## Author

**Thomas Tse** — Arizona State University, Mathematics (Statistics) & Computer Science  
Built for the Bridgewater Associates AI Innovation Hackathon 2026
