# Contributing

Thanks for your interest in MarkoWizard.

## Setup

The project uses [uv](https://docs.astral.sh/uv/).

```bash
git clone https://github.com/GusFurtado/MarkoWizard
cd MarkoWizard
uv sync
```

`uv sync` installs the library plus the `dev` dependency group (pytest, ruff).

## Checks

```bash
uv run pytest          # tests
uv run ruff check      # lint
uv run ruff format     # format
```

Please make sure both pass before opening a pull request.

## Scope

`markowizard/` is the installable library — keep it dependency-light and free of
web/UI concerns. The web application under `backend/` and `frontend/` is not part
of the published package; run it with:

```bash
uv run --with-requirements backend/requirements.txt uvicorn backend.main:app --port 8000
```

## Building the docs

The docs site (https://www.gustavofurtado.com/MarkoWizard/) is built with
[MkDocs Material](https://squidfunk.github.io/mkdocs-material/) and
[mkdocstrings](https://mkdocstrings.github.io/) from `docs/` + docstrings in
`markowizard/`. Preview locally with:

```bash
uv run --group docs mkdocs serve
```

It deploys automatically on every push to `main` (see `.github/workflows/docs.yml`).

## Pull requests

- Branch off `main`, keep changes focused.
- Add or update tests for behaviour changes.
- Describe what changed and why.
