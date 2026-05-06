# hexa-cosmos v1.0.0 — Cosmos substrate (HEXA family)

**Release date**: 2026-05-06
**Closure verdict**: **SPEC_ONLY** (0/3 pillars wired; 3/3 ship as theoretical spec)
**Provenance**: extracted 2026-05-06 from `n6-architecture@c0f1f570`
(domains/physics/{cosmology, cosmology-particle, cosmic-observatory}).
Sister extraction of `hexa-bio` v1.0.0 (2026-05-04, registry L24).

This is the **initial standalone release** of `hexa-cosmos`, a 3-pillar
Cosmos substrate organized around the **n=6 invariant lattice**: COSMOLOGY /
PARTICLE / OBSERVATORY. All 3 pillars are theoretical specs; the n=6 ΛCDM
(LambdaCDM) 6-parameter closed-form mapping ships as a **candidate**, not a
measurement.

## Highlights

- **3-pillar architecture** — COSMOLOGY (cosmology spec), PARTICLE
  (particle-cosmology spec), OBSERVATORY (cosmic-observatory spec). All 3
  inherited verbatim (read-only) from `n6-architecture/domains/physics/`.
- **n=6 ΛCDM closed-form candidate** — `n=6` matches the count of
  independent ΛCDM parameters {Ω_b·h², Ω_c·h², 100θ_MC, τ_reion, n_s,
  ln(10¹⁰A_s)}. Closed-form mappings (e.g. Ω_m = φ/n = 1/3, Ω_Λ = (σ-τ)/σ
  = 2/3, T_CMB ≈ 2.725 K) are documented in `docs/lambda_cdm_vs_n6.md`
  as **candidate**, not measured.
- **n=6 invariant lattice** — `σ(6)=12, τ(6)=4, φ(6)=2, J₂=24`; master
  identity `σ·φ_E = n·τ = 24`. Verified via OEIS A000203/A000005/A001414
  cross-derivation only.
- **CLI placeholder** — 6 subcommands (`cosmology`, `particle`,
  `observatory`, `status`, `selftest`, `help`); subcmd dispatch + audit
  logging landed. Numerical wiring TBD (post-v1.0).
- **Selftest** — 3-pillar markdown presence sweep;
  `__HEXA_COSMOS_SELFTEST__ PASS` confirms all 3 spec files present
  (sentinel-only PASS does **not** validate empirical claims).
- **MIT license** — pure-text spec + placeholder CLI; no runtime deps.
- **GitHub-only distribution** — canonical at
  <https://github.com/need-singularity/hexa-cosmos>.

## Installation

```bash
# Via git clone (works today):
git clone https://github.com/need-singularity/hexa-cosmos.git ~/.hexa-cosmos
export HEXA_COSMOS_ROOT=~/.hexa-cosmos
export PATH="$HEXA_COSMOS_ROOT/cli:$PATH"
hexa run $HEXA_COSMOS_ROOT/cli/hexa-cosmos.hexa selftest
```

## Quickstart

```bash
hexa-cosmos selftest         # 3-pillar markdown presence sweep
hexa-cosmos status           # pillar status table + n=6 ΛCDM caveats
hexa-cosmos cosmology        # SPEC — print spec path
hexa-cosmos particle         # SPEC — print spec path
hexa-cosmos observatory      # SPEC — print spec path
```

## Honest C3 caveats (raw#10)

1. **0/3 pillars empirically wired.** All 3 ship as theoretical spec only.
   The `.hexa` CLI is a placeholder router; numerical wiring (CMB pipeline,
   BBN solver, N-body bridge, telescope orchestrator) is deferred post-v1.0.
2. **n=6 ΛCDM closed-form comparison is a CANDIDATE, not a measurement.**
   See `docs/lambda_cdm_vs_n6.md` for the side-by-side parameter table with
   honest sigma-bounds vs candidate n=6 derivation.
3. **n=6 invariant lattice** (σ=12, τ=4, φ=2, J₂=24) is verified via OEIS
   sequence cross-derivation only (A000203/A000005/A001414). Application
   to ΛCDM 6-parameter set is hypothesized, not demonstrated.
4. **No proprietary calibration.** All theoretical content lives in
   markdown specs imported verbatim from `n6-architecture@c0f1f570`.
5. **Cross-link cousins**: `need-singularity/hexa-space` (aerospace +
   astronomy + astrobiology, observation-side ops) and
   `need-singularity/hexa-millennium` (math substrate cousin).

## Distribution (GitHub canonical)

- canonical: <https://github.com/need-singularity/hexa-cosmos>

## License

MIT — see [LICENSE](LICENSE).
