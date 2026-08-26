# Quickstart

Fresh machine, five minutes.

```bash
pip install -r requirements.txt
python -m logwash --help
```

Then:

```bash
# show what would be cleaned, change nothing
logwash ./logs --older-than 30 --dry-run

# archive logs older than 30 days
logwash ./logs --older-than 30 --archive ./backup
```

If nothing happens, check docs/usage.md first.
