# Ozone and deaths in London, 2002–2006

A worked example for [Fieldwork](https://github.com/digital-twin-ph/fieldwork): a daily time series of deaths,
ozone and temperature in London, from a tutorial paper on time-series regression in environmental epidemiology
(Bhaskaran et al. 2013).

**Not built yet.** The data are here. The workflows wait for regression in Fieldwork (experiment 167), because the
paper's results are regression estimates.

## What the paper reports, to check against

Death rate ratio per 10 µg/m³ increase in ozone, quasi-Poisson regression:

| Model | Rate ratio (95% CI) |
| --- | --- |
| Unadjusted | 0.991 (0.987–0.994) |
| Adjusted for season and long-term trend (cubic B-spline of time, 35 df) | 1.007 (1.003–1.010) |
| Also adjusted for temperature (deciles) | 1.003 (0.999–1.006) |

The sequence shows confounding by season, then by temperature: ozone and deaths both follow the seasons in opposite
directions, so the unadjusted estimate points the wrong way.

## Files

| File | What it holds |
| --- | --- |
| `data/londondataset2002_2006.dta` | Stata file as the authors published it: 1,826 days, `date`, `ozone` (µg/m³), `temperature` (°C), `relative_humidity` (%), `numdeaths` |

Fieldwork reads Stata files directly. The file has no missing values.

## What this does not establish

- **Where the series came from.** The paper does not name the sources of the deaths, ozone or weather data.
- **Terms for the data.** The paper states none; see NOTICE.txt for the basis on which the file is shared here.

## Reference

Bhaskaran K, Gasparrini A, Hajat S, Smeeth L, Armstrong B. Time series regression studies in environmental
epidemiology. *International Journal of Epidemiology*. 2013;42(4):1187–1195.
[doi:10.1093/ije/dyt092](https://doi.org/10.1093/ije/dyt092). Open access, CC BY-NC 3.0.
