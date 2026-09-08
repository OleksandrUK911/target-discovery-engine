# Target Discovery / Prioritization Engine

Ranks candidate biological targets (genes/proteins) for a given disease or
condition, using public biological data (Open Targets, STRING, DisGeNET,
Reactome).

## Status
🔴 In planning — implementation not started yet.

## Stack
- **Data/ML:** Python, public bio-data APIs, network analysis (NetworkX)
- **Backend:** FastAPI, PostgreSQL (cache)
- **Frontend:** React, interactive PPI network graph
- **Infra:** Docker, GitHub Actions

## How it works
```
Disease/condition → evidence aggregation → scoring → ranked target list
```

## Disclaimer
Research/educational project based entirely on public data. Scores are
evidence-based rankings, not clinical or regulatory recommendations.

## License
TBD
