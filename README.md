<p align="center">
  <a href="https://www.gustavofurtado.com/MarkoWizard/"><img src="https://www.gustavofurtado.com/assets/img/projects/markowizard.png" alt="MarkoWizard" width="640"></a>
</p>

<p align="center">
  <b>A modern Python library for Markowitz portfolio optimization and analysis.</b>
</p>

<p align="center">
  <a href="https://pypi.org/project/markowizard/"><img src="https://img.shields.io/pypi/v/markowizard" alt="PyPI"></a>
  <a href="https://pypi.org/project/markowizard/"><img src="https://img.shields.io/pypi/pyversions/markowizard" alt="Python versions"></a>
  <a href="https://pepy.tech/projects/markowizard"><img src="https://static.pepy.tech/badge/markowizard/month" alt="Downloads"></a>
  <a href="https://github.com/GusFurtado/MarkoWizard/actions/workflows/ci.yml"><img src="https://github.com/GusFurtado/MarkoWizard/actions/workflows/ci.yml/badge.svg" alt="CI"></a>
  <a href="https://github.com/GusFurtado/MarkoWizard/blob/main/LICENSE"><img src="https://img.shields.io/pypi/l/markowizard" alt="License"></a>
</p>

<p align="center">
  <b><a href="https://www.gustavofurtado.com/MarkoWizard/">Documentation</a></b>
</p>

Efficient frontier, capital allocation line and interactive charts, from market data to the
best portfolio in a few lines. Previously known as _Diversificador_.

## Installation

```sh
pip install markowizard
```

## What's inside

- **`MarkowitzOptimizer`**: mean-variance optimization over the efficient frontier, with Sharpe ratios and the max-Sharpe portfolio.
- **`CapitalAllocator`**: the capital allocation line, mixing a risky portfolio with a risk-free asset.
- **`markowizard.visualization`**: Plotly charts for the frontier, allocation, CAL, correlations and prices.
- **`markowizard.data`**: helpers to download prices with yfinance and compute returns.
- **Web app**: a FastAPI backend with an interactive frontend, available as a Docker image ([docs](https://www.gustavofurtado.com/MarkoWizard/web-app/)).

See the [quick start](https://www.gustavofurtado.com/MarkoWizard/quickstart/) and the
[API reference](https://www.gustavofurtado.com/MarkoWizard/reference/core/).
