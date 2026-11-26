# About

## License

MarkoWizard is released under the
[MIT License](https://github.com/GusFurtado/MarkoWizard/blob/main/LICENSE).

## Credits

The library is built on [NumPy](https://numpy.org), [pandas](https://pandas.pydata.org),
[SciPy](https://scipy.org) and [Plotly](https://plotly.com/python/), and downloads market data
with [yfinance](https://github.com/ranaroussi/yfinance), which is not affiliated with Yahoo.
The web app runs on [FastAPI](https://fastapi.tiangolo.com) and
[Uvicorn](https://www.uvicorn.org). The wordmark is set in
[Montserrat](https://github.com/JulietaUla/Montserrat) (SIL OFL), outlined.

## Contributing

The project uses [uv](https://docs.astral.sh/uv/).

```bash
git clone https://github.com/GusFurtado/MarkoWizard
cd MarkoWizard
uv sync
```

`uv sync` installs the library plus the `dev` dependency group (pytest, ruff). Before opening a
pull request, make sure the checks pass:

```bash
uv run pytest          # tests
uv run ruff check      # lint
uv run ruff format     # format
```

`markowizard/` is the installable library: keep it dependency-light and free of web or UI
concerns. The web app under `backend/` and `frontend/` is not part of the published package;
run it with:

```bash
uv run --with-requirements backend/requirements.txt uvicorn backend.main:app --port 8000
```

This site is built with [MkDocs Material](https://squidfunk.github.io/mkdocs-material/)
and [mkdocstrings](https://mkdocstrings.github.io/) (API pages are generated from the
library's docstrings). To preview it locally:

```bash
uv run --group docs mkdocs serve
```

It publishes to GitHub Pages on every push to `main` that touches `docs/`, `mkdocs.yml` or
`markowizard/`.

For pull requests: branch off `main` and keep changes focused, add or update tests for
behaviour changes, and describe what changed and why.

## History

MarkoWizard started as *Diversificador*, a portfolio-analysis web app built with
[Dash](https://dash.plotly.com/). That app is no longer maintained, but it is preserved on the
[`dash-deprecated`](https://github.com/GusFurtado/MarkoWizard/tree/dash-deprecated) branch.

The container images for v0.1.0 to v0.2.1 were published as
`ghcr.io/outliersanalytics/markowizard`. Since v0.3.0 the image is
`ghcr.io/gusfurtado/markowizard`.
