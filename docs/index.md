<p align="center">
  <a href="assets/readme-banner.webp"><img src="assets/readme-banner.webp" alt="MarkoWizard" width="100%">
</p>

**A modern Python library for Markowitz portfolio optimization and analysis.**

MarkoWizard takes a list of assets, downloads their price history and finds the mix with the
best return for its risk: the efficient frontier, the maximum-Sharpe portfolio and the capital
allocation line, ready to plot. The math is plain NumPy and SciPy, and the frontier comes back as
a pandas DataFrame, so it fits into whatever analysis comes next.

The repository also ships a web app on top of the library: pick the assets and the history
window, and read the report in the browser. It runs from a small Docker image.

[![PyPI](https://img.shields.io/pypi/v/markowizard)](https://pypi.org/project/markowizard/)
[![Python versions](https://img.shields.io/pypi/pyversions/markowizard)](https://pypi.org/project/markowizard/)
[![Downloads](https://static.pepy.tech/badge/markowizard/month)](https://pepy.tech/projects/markowizard)
[![CI](https://github.com/GusFurtado/MarkoWizard/actions/workflows/ci.yml/badge.svg)](https://github.com/GusFurtado/MarkoWizard/actions/workflows/ci.yml)
[![License](https://img.shields.io/pypi/l/markowizard)](https://github.com/GusFurtado/MarkoWizard/blob/main/LICENSE)

## Features

- **Markowitz mean-variance optimization**: the efficient frontier and the maximum-Sharpe
  portfolio, computed with `scipy.optimize`.
- **Capital allocation line**: mix the risky portfolio with a risk-free asset.
- **Charts**: Plotly figures for the efficient frontier, the allocation, the CAL, correlations
  and prices.
- **Market data**: helpers to download prices with yfinance and turn them into monthly returns.
- **Web app**: a FastAPI backend with an interactive report, in six color themes, each light
  and dark.

<div class="shots">
  <a class="wide" href="assets/screenshot-overview.webp"><img src="assets/screenshot-overview.webp" alt="The web app: five assets, the report's headline numbers and the efficient frontier"></a>
  <a href="assets/screenshot-allocation.webp"><img src="assets/screenshot-allocation.webp" alt="The optimal allocation, with a donut chart and a slider to blend in cash"></a>
  <a href="assets/screenshot-correlation.webp"><img src="assets/screenshot-correlation.webp" alt="The correlation matrix in dark mode, with the least correlated pair"></a>
</div>

## Where to go next

- [Installation](installation.md): install the library or run the web app
- [Quick Start](quickstart.md): optimize a portfolio in a few lines of Python
- [Web Application](web-app.md): run the interactive report locally or with Docker
- [API Reference](reference/core.md): every public function and class
- [About](about.md): license, credits, contributing and the project's history

## Modules

| Module | Description |
|---|---|
| [`core`](reference/core.md) | `MarkowitzOptimizer`: efficient frontier optimization |
| [`allocation`](reference/allocation.md) | `CapitalAllocator`: risk-free asset allocation |
| [`visualization`](reference/visualization.md) | Plotly charts (efficient frontier, pie, CAL, correlation) |
| [`data`](reference/data.md) | Market-data fetching and monthly-return helpers (yfinance) |

The web app (`backend/`, `frontend/`) lives in the repository but is not part of the
installable package: see [Web Application](web-app.md).
