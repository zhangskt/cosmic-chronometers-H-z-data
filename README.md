# Cosmic Chronometers H(z) Data (32 points)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

32 Hubble parameter measurements from cosmic chronometers.

| Property | Value |
|----------|-------|
| Total points | **32** |
| Redshift range | z = 0.07 – 1.965 |
| Uncorrelated | 17 |
| Correlated (Moresco) | 15 (covariance matrix available) |

## Files

| File | Description |
|------|-------------|
| `Hz_data_32points.csv` | Main data: z, Hz, sigma_Hz, Reference, Correlated |
| `covariance/` | Covariance matrix for 15 correlated points (from [Moresco GitLab](https://gitlab.com/mmoresco/CCcovariance)) |

## Quick Start

```python
import pandas as pd
df = pd.read_csv("Hz_data_32points.csv")
print(f"Loaded {len(df)} H(z) measurements")
# Correlated vs uncorrelated
corr = df[df['Correlated'] == 'Yes']    # 15 points (Moresco)
uncorr = df[df['Correlated'] == 'No']   # 17 points (others)
```

## Data Sources (8 papers)

| Authors | Year | Points | arXiv |
|---------|:----:|:------:|-------|
| Jimenez et al. | 2003 | 4 | [astro-ph/0302560](https://arxiv.org/abs/astro-ph/0302560) |
| Simon et al. | 2005 | 4 | [astro-ph/0412269](https://arxiv.org/abs/astro-ph/0412269) |
| Stern et al. | 2010 | 5 | [0907.3149](https://arxiv.org/abs/0907.3149) |
| Moresco et al. | 2012 | 8 | [1201.3609](https://arxiv.org/abs/1201.3609) |
| Moresco | 2015 | 2 | [1503.01116](https://arxiv.org/abs/1503.01116) |
| Moresco et al. | 2016 | 5 | [1601.01701](https://arxiv.org/abs/1601.01701) |
| Ratsimbazafy et al. | 2017 | 3 | [1702.00418](https://arxiv.org/abs/1702.00418) |
| Borghi et al. | 2022 | 1 | [2110.04304](https://arxiv.org/abs/2110.04304) |

Covariance matrix: [Moresco et al. 2020](https://arxiv.org/abs/2003.07362) ApJ, 898, 82 — [GitLab data](https://gitlab.com/mmoresco/CCcovariance)

## Version History

| Version | Points | Change |
|:-------:|:------:|--------|
| Moresco 2016 Table 4 | 30 | Original |
| + Ratsimbazafy 2017 | **31** | Added z=0.47 |
| + Borghi 2022 | **32** | Added z=0.75 (current) |

## License

MIT License — see [LICENSE](LICENSE) file.
