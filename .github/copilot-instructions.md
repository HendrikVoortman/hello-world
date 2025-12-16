# GitHub Copilot instructions — hello-world ✅

This repository is a small Python test/example project. The goal of AI agents working here is to make minimal, well-tested, and documented improvements while preserving the simple behavior.

## Quick facts 🔧
- Language: **Python 3**
- Main module: `perftest.py` — contains `multiply(a, b)` and a `if __name__ == '__main__'` runner that prints `hello world`.
- No CI, no tests, no packaging in the current repo snapshot.

## Quick start (what to run) ▶️
- Run the script: `python3 perftest.py` (expects stdout: `hello world`).
- Add tests and run them locally with pytest:
  - `python3 -m pip install pytest`
  - `pytest`

## Editing and contribution guidance ✍️
- Keep the top-level script behavior behind `if __name__ == '__main__'` so functions remain importable and testable.
- When adding/changing functionality, export small, pure functions at module level (easier to unit test).
- Add tests under `tests/` with names like `tests/test_perftest.py`.

Example unit test for an existing function:

```py
# tests/test_perftest.py
from perftest import multiply

def test_multiply_basic():
    assert multiply(2, 3) == 6
```

- If you change printed output or CLI behavior, update `README.md` and add a test that covers the change.

## Project patterns & conventions 📌
- This is intentionally minimal: prefer minimal, clear, and well-scoped changes rather than broad refactors.
- Use explicit `python3` commands in docs and CI scripts when specifying how to run things.
- If you add third-party dependencies: add a `requirements.txt` at the repo root and document install/run steps in `README.md`.

## Testing & debugging advice 🐞
- Because there is no CI, run tests locally (`pytest`) and run the script directly for quick sanity checks (`python3 perftest.py`).
- For isolated testing, prefer small unit tests that import and exercise individual functions.

## PR & commit guidance ✅
- Keep commits small and focused (one logical change per commit).
- Use imperative commit messages (e.g., `Add multiply edge-case tests`).
- PR description should summarize the change and list the commands to verify it locally.

## Files to inspect first 🔎
- `perftest.py` — primary source file; editing here is the main activity.
- `README.md` — update for usage changes.

> Note: This file documents the repository *as it currently exists* (tiny example/test). If you add tests, CI, packaging, or other infra, update this guidance to reflect those changes.

If anything above is unclear or you'd like the file to include more specifics (e.g., preferred test frameworks, style rules, or a suggested CI config), tell me which areas to expand. 👇