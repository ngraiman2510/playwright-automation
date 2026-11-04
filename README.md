# Cricbuzz Score Scraper

A small Python script that uses Playwright to open Cricbuzz, read the first
scorecard displayed in its match carousel, and print the text to the terminal.

## Requirements

- Python 3.9 or later
- An internet connection
- A graphical desktop session, because the browser runs in headed mode

## Set up

From this directory, create and activate a virtual environment:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

On Windows, activate it with:

```powershell
.venv\Scripts\Activate.ps1
```

Install Playwright and its Chromium browser:

```bash
python -m pip install playwright
python -m playwright install chromium
```

## Run

With the virtual environment activated:

```bash
python cricbuzz_score.py
```

The script opens a Chromium window, waits up to 15 seconds for the scorecard,
prints its text, and closes the browser.

## Notes

- The script reads only the first matching item in Cricbuzz's match carousel;
  it does not provide a complete live-score feed.
- Cricbuzz may change its page structure or restrict automated browsing. If the
  scorecard is not found, check the selector in `cricbuzz_score.py` and the
  page's availability.
- Keep Playwright installed in the active virtual environment when running
  the script.
