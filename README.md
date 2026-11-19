# coinsnipe-status

When the CoinSnipe nightly job last ran, and whether it finished. **Run times only: no data, no code, no secrets.**

- `last-run.json`: written by the nightly server after every run (00:30 UTC): the date, start and finish times, and `ok`, `failed` or `skipped`, plus the last 14 nights.
- `setup.json`: written once by the server when its set-up finishes.
- **The morning check** (`.github/workflows/morning-check.yml`) runs at 01:30 UTC. If last night's run is missing, skipped or failed, it fails and GitHub emails the owner. GitHub sometimes starts scheduled checks late.
- The Daily run page in the CoinSnipe Hub reads `last-run.json` from here.

The server's key for this project can write here and nowhere else. The code lives in the private project `coinsnipe-data` (step P0.1b).
