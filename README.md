# logprune

Opinionated log housekeeping tool with dry-run support

Started as a weekend hack, grew on me.

## What it does

- Archive matched logs into a timestamped .tar.gz
- Filter by age (--older-than) or size (--larger-than)
- Scan directories for log files by glob pattern
- Dry-run mode shows what would happen, touches nothing
- Exit codes friendly for cron and CI

## Getting started

```bash
pip install -r requirements.txt
python -m logwash --help
```

## How to use

```bash
# show what would be cleaned, change nothing
logwash ./logs --older-than 30 --dry-run

# archive logs older than 30 days
logwash ./logs --older-than 30 --archive ./backup
```

## Project structure

```text
├── .github/
│   └── dependabot.yml
├── docs/
│   ├── configuration.md
│   ├── development.md
│   ├── roadmap.md
│   └── usage.md
├── examples/
│   └── quickstart.md
├── logwash/
│   ├── __init__.py
│   ├── __main__.py
│   ├── cli.py
│   ├── errors.py
│   └── utils.py
├── tests/
│   └── test_cli.py
├── .gitattributes
├── .gitignore
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── LICENSE
├── pyproject.toml
└── requirements.txt
```

## Development

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
python -m pytest -q
```

## License

MIT licensed, see LICENSE.
