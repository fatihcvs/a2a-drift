# Changelog

All notable changes to this project will be documented in this file.

## [Unreleased]

### Added

- `validate_url()` helper plus `--deny-internal` / `--allow-internal` CLI flags to
  refuse internal, loopback, link-local and reserved addresses (CWE-918).
- `--spec-version` is now honored: the target version is threaded through to
  `AgentCardChecker` and reported as `target_spec_version` in JSON output.
- `ValidationResult.spec_version_target` records the version drift was measured against.
- `to_sarif()` in `a2a_drift/cli.py`; `check`, `probe` and `batch` accept `--format sarif`.
- `--output` is now honored by the `probe` subcommand.

### Changed

- Non-positive `--retries` values are rejected by argparse (exit 2) instead of
  crashing with `UnboundLocalError`; the library constructors clamp to 1 attempt.
- `batch` isolates per-URL failures, reports every entry, and treats an empty
  URL file as an error rather than a vacuous success.

### Fixed

- A JSON array, `null`, string or number agent card is reported as a
  `schema-violation` finding instead of raising `AttributeError`/`TypeError`.
- `--format sarif` emits a real SARIF 2.1.0 document; it previously accepted the
  flag and printed the human-readable text report.
- A missing `--file` for `batch` reports a clean error instead of a traceback.

## [Initial Release]

- Initial project release
