# DAO Stablecoin Revenue Research

This repository contains the complete research codebase for the DAO Stablecoin Revenue Research project, conducted by Lampros DAO as part of an ArbitrumDAO grant. The research analyzes Arbitrum's stablecoin-driven sequencer fee revenue across two tracks.

---

## Research Overview

| Phase | Title | Description |
|---|---|---|
| Phase 2 | Sequencer Fee Attribution Model | Measures how much of Arbitrum's sequencer revenue comes from stablecoin activity, how that relationship has evolved over time, and how much revenue the DAO could lose under different stress scenarios |
| Phase 3 | Non-USD Stablecoin Benchmarking & Revenue Modeling | Analyzes 16 non-USD stablecoins across 8 blockchains, projects the revenue opportunity if non-USD stablecoins deployed meaningfully on Arbitrum, and models an equity-in-issuer revenue path |

---

## Repository Structure

```
dao-stablecoin-revenue-research/
│
├── requirements.txt                           # Python dependencies
├── .gitignore                                  
│
├── Phase 2/
│   ├── Data/                                  # Input datasets used for Phase 2 analysis
│   ├── Results/                               # Output CSV files containing analysis results
│   └── Sequencer_Fee_Attribution_Model.ipynb  # Full Phase 2 analysis notebook
│
└── Phase 3/
    ├── Data/                                  # Input datasets used for Phase 3 analysis
    └── Non_USD_Stablecoin_Benchmarking.ipynb  # Full Phase 3 analysis notebook
```

---

## Setup and Installation

**Prerequisites:** Python 3.8 or higher

**Install dependencies:**
```bash
pip install -r requirements.txt
```

**Run notebooks:**
```bash
jupyter notebook
```
Navigate to the relevant phase folder and open the notebook.

---

## Data Sources

| Source | Used For |
|---|---|
| Dune Analytics | Arbitrum L2 sequencer fees, stablecoin activity, transfer data |
| DefiLlama | Non-USD stablecoin global supply across all chains |
| ECB, BCB, MAS, Bank of Canada | Central bank interest rates for equity-in-issuer analysis |

---

## Key Findings

**Phase 2**
- Stablecoins contribute nearly 50% of all Arbitrum sequencer fees - the single largest revenue category on the network
- USDC and USDT together account for 98.5% of stablecoin-generated fees
- Stablecoin supply has almost no direct relationship with total sequencer fees (Pearson r = 0.07) - activity and velocity drive revenue, not supply
- A moderate stress event (40% stablecoin activity contraction) would cost the DAO approximately $1.90M annually under a realistic dual-contraction scenario

**Phase 3**
- 10 of 16 non-USD stablecoins analyzed have no Arbitrum presence - combined global supply of ~$4.26 billion generating fees elsewhere
- Non-USD stablecoin revenue upside: $2.2M–$11.1M annually at base case adoption (supply-based model)
- EUR stablecoins with proper DeFi integrations are 2.4x more fee-efficient than the USD stablecoin baseline on Arbitrum
- A 10% equity stake in Transfero (BRZ issuer) would generate $6.4M annually from reserve yield alone - independent of Arbitrum deployment

---

## Analysis Window

All performance metrics in both Phase 2 and Phase 3 are calculated using the same trailing 12-week window: January 26, 2026 to April 19, 2026. Using identical windows across both phases ensures the findings are directly comparable.

This window was chosen for three reasons: it reflects the most current market conditions, averaging across 12 weeks removes short-term distortions from one-off weekly events, and it produces stable baseline figures for projection and stress testing purposes.

---

## About Lampros DAO

Lampros DAO is a contributor organization in the Arbitrum ecosystem with over 2.5 years of ecosystem contributions. This research was conducted as part of an ArbitrumDAO grant focused on stablecoin revenue analysis and ecosystem strategy.

---

## License

MIT License - open for use, reproduction, and building upon with attribution.
