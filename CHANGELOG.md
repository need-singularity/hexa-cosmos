# Changelog

All notable changes to **hexa-cosmos** are documented here. Format follows
[Keep a Changelog](https://keepachangelog.com/en/1.1.0/) and SemVer.

## [1.0.0] - 2026-05-06

### Added
- Initial standalone extraction from `n6-architecture@c0f1f570`.
- 3-pillar architecture:
  - `cosmology/`    ← `n6-architecture/domains/physics/cosmology/`
  - `particle/`     ← `n6-architecture/domains/physics/cosmology-particle/`
  - `observatory/`  ← `n6-architecture/domains/physics/cosmic-observatory/`
- `hexa.toml` package manifest (MIT, name `hexa-cosmos`).
- `install.hexa` `hx` build hook (sister-borrowed from hexa-bio).
- `cli/hexa-cosmos.hexa` placeholder CLI router (subcmd dispatch landed;
  numerical wiring TBD).
- `tests/test_selftest.hexa` 3-pillar markdown presence sweep harness.
- `docs/lambda_cdm_vs_n6.md` ΛCDM 6-parameter (Ω_b·h², Ω_c·h², 100θ_MC,
  τ_reion, n_s, ln(10¹⁰A_s)) vs n=6 closed-form candidate comparison table.
- `LICENSE` MIT.
- `RELEASE_NOTES_v1.0.0.md`.

### Honest C3 caveats (raw#10)
- 0/3 pillars empirically wired. All 3 ship as theoretical spec only.
- n=6 ΛCDM closed-form comparison is a **candidate**, not a measurement.
- n=6 invariant lattice verified via OEIS cross-derivation only.
- Numerical pipelines (CMB, BBN, N-body, telescope) deferred post-v1.0.

### Cross-links
- need-singularity/hexa-space (observation-side ops sister)
- need-singularity/hexa-millennium (math substrate cousin)
- need-singularity/hexa-bio (sister extraction template)
