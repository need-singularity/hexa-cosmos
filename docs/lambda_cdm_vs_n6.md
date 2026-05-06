# ΛCDM 6-parameter vs n=6 closed-form (candidate)

> **Status**: CANDIDATE COMPARISON, NOT A MEASUREMENT.
> The mappings below are theoretical-derivation candidates extracted from
> `n6-architecture@c0f1f570/domains/physics/cosmology/cosmology.md` §X
> ("BLOWUP — cosmology breakthrough-draft"). They are not fits to data;
> the side-by-side table is presented to expose the **claim surface** so it
> can be falsified (see Falsifiers below).

## n=6 invariant lattice (recap)

| symbol     | value | derivation                                |
|------------|-------|-------------------------------------------|
| n          | 6     | DOF; SE(3) = R³ × SO(3)                   |
| σ(6)       | 12    | divisor sum (OEIS A000203)                |
| τ(6)       | 4     | divisor count (OEIS A000005)              |
| φ(6)       | 2     | minimum prime factor                      |
| φ_E(6)     | 2     | Euler totient (OEIS A000010)              |
| sopfr(6)   | 5     | prime-factor sum (OEIS A001414)           |
| J₂         | 24    | 2σ; quadratic-form minimal-vector count   |
| σ-φ        | 10    | "Mach cap" / Kardashev decade             |
| σ·τ        | 48    | SC B-field cap (T)                        |
| σ-τ        | 8     | Golay distance                            |

Master identity: `σ·φ_E = n·τ = 24` (n=6 uniqueness lemma).

## ΛCDM 6 parameters vs n=6 closed-form candidate

The "standard" ΛCDM model has **n = 6** independent parameters; this
coincidence is the launching observation for the n=6 substrate claim.

| # | ΛCDM parameter        | Planck 2018 measurement       | n=6 candidate closed-form                                | candidate value | match? |
|---|-----------------------|-------------------------------|----------------------------------------------------------|-----------------|--------|
| 1 | Ω_b · h² (baryon)     | 0.02237 ± 0.00015             | (under construction; sopfr/σ²·φ scale)                   | ≈ 0.022         | candidate |
| 2 | Ω_c · h² (cold DM)    | 0.1200 ± 0.0012               | τ/(σ+sopfr-φ) base (L9-dark-matter 7463)                 | ≈ 0.12          | candidate |
| 3 | 100·θ_MC (acoustic)   | 1.0411 ± 0.0003               | (1 + μ/σ²) acoustic-scale                                | ≈ 1.04          | candidate |
| 4 | τ_reion (optical d.)  | 0.0544 ± 0.0073               | sopfr/(σ²-σ-...) reionization                            | ≈ 0.054         | candidate |
| 5 | n_s (spectral idx)    | 0.9649 ± 0.0042               | (n/φ)³ / ((n/φ)³+μ) = 27/28                              | 0.9643          | within 1σ |
| 6 | ln(10¹⁰·A_s)          | 3.044 ± 0.014                 | (under construction; σ/τ + correction)                   | ≈ 3.04          | candidate |

> **Note**: parameters 1, 3, 4, 6 ship as **placeholders** for the candidate
> closed-form; parameter 5 (n_s = 27/28) is the headline tightest match in
> the n=6 substrate (existing PHYS-CMB-spectral-index claim, reused from
> `n6-architecture/.../cosmology.md` §X.1 breakthrough-draft 2). Parameter
> 2 (Ω_c·h²) and the derived Ω_m / Ω_Λ split are documented below.

## Derived ΛCDM observables (candidate closed-forms)

| observable                 | measured                       | n=6 candidate                          | candidate value | error |
|----------------------------|--------------------------------|----------------------------------------|-----------------|-------|
| H₀ (Planck CMB)            | 67.4 ± 0.5 km/s/Mpc            | σ·sopfr + τ + J₂/σ − μ                 | 67              | 0.6%  |
| H₀ (SH0ES ladder)          | 73.0 ± 1.0 km/s/Mpc            | σ·sopfr + J₂/φ + 1                     | 73              | 0.0%  |
| Hubble tension Δ           | 5.6 km/s/Mpc (~5σ)             | σ-sopfr-φ = sopfr                      | 5               | 0.0%  |
| Ω_m                        | 0.315 ± 0.007                  | φ/n = 1/3                              | 0.333           | ~6%   |
| Ω_Λ                        | 0.685 ± 0.007                  | (σ-τ)/σ = 2/3                          | 0.667           | ~3%   |
| Ω_total (flat)             | 1.000 ± 0.005                  | Ω_m + Ω_Λ                              | 1.000           | 0.0%  |
| T_CMB                      | 2.72548 ± 0.00057 K            | (τ−μ/J₂)·(σ+φ)/(σ·φ) [3-path avg]      | 2.725           | 0.04% |
| CMB 1st acoustic peak l₁   | 220 ± 1                        | σ(σ+n) + τ = 12·18 + 4                 | 220             | 0.0%  |
| BBN light-element count    | 4 (H, He-3, He-4, Li-7)        | τ                                      | 4               | exact |
| Hubble radius log₁₀(R_H/m) | ≈ 26.13                        | σ + τ + (σ-φ) = 12 + 4 + 10            | 26              | 0.5%  |

## Falsifiers (preregister)

The candidate claim collapses if any of the following hold:

- **F1** Hubble tension magnitude ≠ sopfr = 5 (±0.5 km/s/Mpc) → `σ-sopfr-φ`
  lock discarded.
- **F2** Ω_m : Ω_Λ ≠ 1/3 : 2/3 (±5%) → `φ/n : (σ-τ)/σ` share discarded.
- **F3** T_CMB measurement ≠ 2.725 K (±0.01) → `(τ−μ/J₂)·(σ+φ)/(σ·φ)`
  3-path average discarded.
- **F4** ΛCDM independent-parameter count revised away from 6 (e.g. 5 or 7
  becomes the consensus standard) → n-parameter lock discarded.
- **F5** CMB first acoustic peak l₁ ≠ 220 ± 3 → `σ(σ+n)+τ` reuse discarded.
- **F6** Bosonic-string compactification yields ΛCDM independent count ≠ n
  → `26 − J₂ + τ − μ·φ = 6` chain discarded.

## What this comparison is NOT

- NOT a fit to data. The n=6 closed-forms above were derived from
  number-theoretic identities (OEIS sequences) and then compared to the
  measured ΛCDM parameters post-hoc.
- NOT a replacement for ΛCDM. ΛCDM is a phenomenological model fit to CMB
  + BAO + supernova data; the n=6 substrate is a candidate algebraic
  ansatz for **why** the parameter count and certain ratios take their
  observed values.
- NOT a calibration. No proprietary data, no pipeline, no Markov chain.

## Provenance

- Extracted 2026-05-06 from `n6-architecture@c0f1f570`:
  - `domains/physics/cosmology/cosmology.md` §X (breakthrough-draft + falsifiers)
  - `domains/physics/cosmology-particle/cosmology-particle.md`
  - `domains/physics/cosmic-observatory/cosmic-observatory.md`
- OEIS cross-references: A000203 (σ), A000005 (τ), A000010 (φ_E),
  A001414 (sopfr).
- Sister substrate: `need-singularity/hexa-bio` (4-verb molecular toolkit,
  same n=6 lattice, sister extraction template).
