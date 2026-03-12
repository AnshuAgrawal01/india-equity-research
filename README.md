# India Equity Research - Claude Code Skills

Claude Code skills for **institutional-grade equity research** on **Indian markets (NSE/BSE)**. Adapted from Anthropic's official [financial-services-plugins](https://github.com/anthropics/financial-services-plugins) for the Indian regulatory, accounting, and market ecosystem.

## What's Included

### Equity Research Skills (`/skills/`)

| Skill | Command | Description |
|-------|---------|-------------|
| **Initiating Coverage** | `/initiate` | 5-task workflow for comprehensive initiation reports |
| **Earnings Analysis** | `/earnings` | Post-earnings update reports (8-12 pages) |
| **Earnings Preview** | `/earnings-preview` | Pre-earnings scenario analysis |
| **Morning Note** | `/morning-note` | Daily research notes for morning meetings |
| **Model Update** | `/model-update` | Update financial models with new data |
| **Catalyst Calendar** | `/catalysts` | Track upcoming events across coverage universe |
| **Idea Generation** | `/screen` | Systematic stock screening and idea sourcing |
| **Sector Overview** | `/sector` | Industry landscape and competitive positioning |
| **Thesis Tracker** | `/thesis` | Maintain and update investment theses |

### Financial Analysis Skills (`/financial-analysis/skills/`)

| Skill | Command | Description |
|-------|---------|-------------|
| **3-Statement Model** | `/3-statement-model` | Populate integrated financial models |
| **DCF Model** | `/dcf` | Discounted Cash Flow valuation |
| **Comps Analysis** | `/comps` | Comparable company analysis |
| **LBO Model** | `/lbo` | Leveraged buyout modeling |
| **Competitive Analysis** | `/competitive-analysis` | Competitive landscape reports |
| **Check Deck** | `/check-deck` | QC presentations for errors |
| **Debug Model** | `/debug-model` | Audit spreadsheets for formula errors |
| **PPT Template** | `/ppt-template` | Create reusable PowerPoint skill |

## India-Specific Adaptations

This plugin has been comprehensively adapted from the US-focused original:

### Regulatory Framework
- **SEBI** (not SEC) as the primary regulator
- **BSE/NSE corporate filings** (not SEC EDGAR) for financial data
- **Annual Reports** and **Quarterly Results** (not 10-K/10-Q)
- **LODR Regulations** (Listing Obligations and Disclosure Requirements)
- **Companies Act 2013** for corporate governance

### Accounting Standards
- **IndAS** (Indian Accounting Standards, converged with IFRS) instead of US GAAP
- Indian-specific line items (promoter holding, related party transactions)

### Market Data & Indices
- **Nifty 50 / Sensex** as benchmark indices (not S&P 500)
- **NSE/BSE** as exchanges (not NYSE/NASDAQ)
- Indian data sources: **Screener.in, Trendlyne, Moneycontrol, Tijori Finance, CMIE Prowess**

### Valuation & Macro
- **India G-Sec yield** as risk-free rate (not US Treasury)
- **India Equity Risk Premium (7-8%)** including country risk premium
- **RBI MPC** meetings (not Fed/FOMC)
- Currency in **INR (₹)**, amounts in **crores/lakhs**

### Data Sources
| US Source | India Equivalent |
|-----------|-----------------|
| SEC EDGAR | BSE/NSE corporate filings, MCA |
| Yahoo Finance | Screener.in, Moneycontrol, Tickertape |
| Seeking Alpha | Trendlyne, Company IR sites |
| S&P Capital IQ | Ace Equity, CMIE Prowess |

## Installation

### As a Claude Code Plugin

```bash
# Clone the repo
git clone https://github.com/anshuagrawal/india-equity-research.git

# Install as a local plugin
claude plugin install ./india-equity-research
```

### From GitHub Marketplace

```bash
claude plugin marketplace add anshuagrawal/india-equity-research
claude plugin install india-equity-research@india-equity-research
```

## Usage

Once installed, use the slash commands in Claude Code:

```
/initiate          # Start an initiating coverage report for an Indian company
/earnings          # Analyze quarterly results
/dcf               # Build a DCF model with India-specific WACC
/comps             # Run comparable company analysis on NSE/BSE peers
/screen            # Screen for investment ideas on Indian markets
```

## Credits

Adapted from [anthropics/financial-services-plugins](https://github.com/anthropics/financial-services-plugins) by Anthropic FSI.

## Disclaimer

This is for **educational and research purposes only**. Not financial advice. Always conduct your own due diligence before making investment decisions.

## License

MIT
