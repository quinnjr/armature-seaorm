# Changelog — `armature-seaorm`

All notable changes to this crate will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this crate adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

Earlier changes are recorded in the workspace [`CHANGELOG.md`](../CHANGELOG.md).

## [Unreleased]

## [0.3.0] - 2026-09-15

### Changed

- **Breaking:** `sea-orm` (1.1 → 2.0) and `sea-query` (0.32 → 1.0) are re-exported and appear in `DatabaseConfig::to_connect_options`, so the upgrade is breaking and the minor moves.
- Dependencies bumped to their latest releases: `sea-orm` 1.1 → 2.0, `sea-query` 0.32 → 1.0.
- Migrate to sea-orm 2.0 and sea-query 1.0.

