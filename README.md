# sample-package

Minimal Python package scaffold demonstrating a packaging manifest
(`MANIFEST.in`) setup with `setuptools` and `pyproject.toml`.

## Layout

```
.
├── pyproject.toml       # build system + project metadata
├── MANIFEST.in           # extra files to include in the sdist
├── src/
│   └── sample_package/
│       ├── __init__.py
│       ├── py.typed
│       └── data/
│           └── defaults.json
└── tests/
    └── test_package.py
```

## Install (editable, for development)

```bash
python -m pip install -e ".[dev]"
```

## Run tests

```bash
pytest
```

## Build distributions

```bash
python -m pip install build
python -m build
```

This produces a wheel and an sdist in `dist/`. `MANIFEST.in` controls
which extra (non-Python) files, such as `data/defaults.json`, get
bundled into the sdist.
