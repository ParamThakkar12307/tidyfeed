# tidyfeed

Reusable ETL skeleton for the CSVs I get at work

## Highlights

- Writes a cleaning report next to the output
- Drops duplicates, trims strings, normalizes dates
- Chunked reading for files that do not fit in memory
- Config-driven column renames and type casts

## Install

```bash
pip install -r requirements.txt
```

## Usage

```bash
python pipeline.py raw.csv --config config.yaml --out clean.csv
```

## Project structure

```text
├── .github/
│   ├── dependabot.yml
│   └── pull_request_template.md
├── docs/
│   ├── configuration.md
│   ├── development.md
│   ├── roadmap.md
│   └── usage.md
├── examples/
│   └── quickstart.md
├── tests/
│   └── test_smoke.py
├── .editorconfig
├── .gitattributes
├── .gitignore
├── CHANGELOG.md
├── CONTRIBUTING.md
├── SECURITY.md
├── config.yaml
├── pipeline.py
└── requirements.txt
```

## Development

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
python -m pytest -q
```

## License

MIT - see [LICENSE](LICENSE).
