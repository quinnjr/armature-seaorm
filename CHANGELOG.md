# Changelog — `armature-seaorm`

All notable changes to this crate will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this crate adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

Earlier changes are recorded in the workspace [`CHANGELOG.md`](../CHANGELOG.md).

## [Unreleased]

## [0.4.0] - 2026-10-17

### Removed

- **Breaking:** The `runtime-tokio-native-tls` and `runtime-actix-native-tls` features are removed (they pulled in OpenSSL through sqlx; Armature is rustls-only). Use `runtime-tokio-rustls` (the default) or `runtime-actix-rustls`.

### Changed

- **Sibling requirements follow the security-hardening release train (breaking).**
  `armature-log` 0.2 → 0.3. Those releases change public APIs and secure-by-default behaviour
  (see each crate's CHANGELOG); this crate's minor moves with them so a
  downstream build can't mix it with the previous sibling releases. No code
  changes in this crate.

## [0.3.0] - 2026-09-15

### Changed

- **Breaking:** `sea-orm` (1.1 → 2.0) and `sea-query` (0.32 → 1.0) are re-exported and appear in `DatabaseConfig::to_connect_options`, so the upgrade is breaking and the minor moves.
- Dependencies bumped to their latest releases: `sea-orm` 1.1 → 2.0, `sea-query` 0.32 → 1.0.
- Migrate to sea-orm 2.0 and sea-query 1.0.

