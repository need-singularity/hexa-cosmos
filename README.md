# 🌌 hexa-cosmos — Cosmos substrate (HEXA family)

> **Cosmos substrate — cosmology + particle-cosmology + cosmic observatory.
> n=6 ΛCDM (LambdaCDM) closed-form comparison candidate.**
>
> 3-pillar Cosmos substrate organized around the **n=6 invariant lattice**:
> COSMOLOGY / PARTICLE / OBSERVATORY. All 3 pillars ship as theoretical
> spec at v1.0.0; the n=6 ΛCDM 6-parameter mapping is a **candidate**, not
> a measurement.

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.20102602.svg)](https://doi.org/10.5281/zenodo.20102602)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-1.0.0-informational.svg)](CHANGELOG.md)
[![Pillars: 0/3 wired](https://img.shields.io/badge/pillars-0%2F3_wired_(spec_only)-orange.svg)](#3-pillar-status-table)
[![n=6 lattice](https://img.shields.io/badge/n%3D6-σ%3D12_τ%3D4_φ%3D2_J₂%3D24-purple.svg)](#n6-invariant-lattice)
[![ΛCDM](https://img.shields.io/badge/ΛCDM-6_param_candidate-blue.svg)](docs/lambda_cdm_vs_n6.md)

> **Status (2026-05-06)**: 이론 + 후보 spec. 작동 `.hexa` CLI TBD.
> ΛCDM (LambdaCDM) baseline에 대한 n=6 closed-form 비교 후보 (candidate, not
> measurement).

> **Distribution**: GitHub canonical at <https://github.com/dancinlab/hexa-cosmos>.

---

## §Why — n=6 우주론 substrate

`hexa-cosmos`는 **3-pillar Cosmos substrate**로, write-side 우주론 spec을
공개한다. ΛCDM의 핵심 좌표 — **6개 독립 파라미터**, **Ω_m : Ω_Λ ≈ 1/3 : 2/3**,
**T_CMB ≈ 2.725 K**, **CMB 1st peak l₁ = 220** — 가 모두 `n = 6` substrate의
number-theoretic identity로 closed-form 후보 표현을 가진다는 가설을 검증가능한
형태로 노출하는 것이 v1.0.0의 목적이다.

3개 pillar는 **tetrahedron이 아닌 triangle**로 구성된다 (자매 substrate
`hexa-bio`는 4-verb tetrahedron):

```
                ┌──────────────┐
                │  COSMOLOGY   │
                │  (ΛCDM 6-par)│
                └──────┬───────┘
                       │
               ┌───────┴───────┐
               │               │
        ┌──────▼─────┐  ┌──────▼──────┐
        │  PARTICLE  │  │ OBSERVATORY │
        │ (BBN/CMB)  │  │  (telescope)│
        └────────────┘  └─────────────┘
           [SPEC]            [SPEC]
```

n=6 invariant lattice가 ΛCDM와 만나는 지점 — **n_s = 27/28 = (n/φ)³/((n/φ)³+μ)**
(0.9643 vs 측정 0.9649 ± 0.0042) — 이 substrate의 가장 tight한 후보 매치이다.
전체 비교표는 [`docs/lambda_cdm_vs_n6.md`](docs/lambda_cdm_vs_n6.md) 참고.

---

## §Verbs — 3-pillar architecture

| pillar       | source (`canon@c0f1f570`)               | status         |
|--------------|---------------------------------------------------|----------------|
| `cosmology`  | `domains/physics/cosmology/`                      | SPEC v1.0.0    |
| `particle`   | `domains/physics/cosmology-particle/`             | SPEC v1.0.0    |
| `observatory`| `domains/physics/cosmic-observatory/`             | SPEC v1.0.0    |

### 3-pillar status table

```
  pillar        status              n=6 ΛCDM mapping         empirical sandbox
  ------------- ------------------- ------------------------ --------------------------
  cosmology     SPEC v1.0.0         candidate closed-form    deferred (post-v1.0)
  particle      SPEC v1.0.0         candidate closed-form    deferred (post-v1.0)
  observatory   SPEC v1.0.0         candidate closed-form    deferred (post-v1.0)
```

### n=6 invariant lattice

| symbol     | value | derivation                                |
|------------|-------|-------------------------------------------|
| n          | 6     | DOF; SE(3) = R³ × SO(3)                   |
| σ(6)       | 12    | divisor sum (OEIS A000203)                |
| τ(6)       | 4     | divisor count (OEIS A000005)              |
| φ(6)       | 2     | minimum prime factor                      |
| J₂         | 24    | 2σ; quadratic-form minimal-vector count   |

Master identity: `σ·φ_E = n·τ = 24` (n=6 uniqueness lemma).

---

## §Status

**이론 + 후보 spec. 작동 `.hexa` CLI TBD. ΛCDM (LambdaCDM) baseline에 대한
n=6 closed-form 비교 후보 (candidate, not measurement).**

- **0/3 pillars empirically wired.** All 3 ship as theoretical spec only.
  The `.hexa` CLI is a placeholder router (subcmd dispatch + audit logging
  landed; numerical wiring TBD).
- **n=6 ΛCDM closed-form comparison is a CANDIDATE, not a measurement.**
  See [`docs/lambda_cdm_vs_n6.md`](docs/lambda_cdm_vs_n6.md) for the
  side-by-side parameter table with honest σ-bounds vs candidate n=6
  derivation, plus 6 falsifiers (F1~F6).
- **n=6 invariant lattice** verified via OEIS A000203 / A000005 / A000010 /
  A001414 cross-derivation only.
- **Numerical pipelines** (CMB, BBN, N-body, telescope) deferred post-v1.0.

### Honest C3 caveats (raw#10)

1. 0/3 pillars empirically wired. All 3 ship as theoretical spec only.
2. n=6 ΛCDM closed-form comparison is a CANDIDATE, not a measurement.
3. n=6 invariant lattice (σ=12, τ=4, φ=2, J₂=24) is verified via OEIS
   sequence cross-derivation only.
4. Numerical pipelines (CMB, BBN, N-body, telescope) are out of scope for
   v1.0.0 — empirical wiring deferred to post-v1.0 cycles.
5. Cross-link cousins (see §Cross-link below) ship independently.

---

## §Install

### Via git clone (works today)

```bash
git clone https://github.com/dancinlab/hexa-cosmos.git ~/.hexa-cosmos
export HEXA_COSMOS_ROOT=~/.hexa-cosmos
export PATH="$HEXA_COSMOS_ROOT/cli:$PATH"

# Run any subcommand:
hexa run $HEXA_COSMOS_ROOT/cli/hexa-cosmos.hexa selftest
```

### Via `hx` (registry registration TBD)

```bash
hx install hexa-cosmos          # global, pulls latest from registry
hx install hexa-cosmos@1.0.0    # pin specific version
hexa-cosmos --version           # → 1.0.0
```

### Quickstart

```bash
hexa-cosmos selftest         # 3-pillar markdown presence sweep
hexa-cosmos status           # pillar status table + n=6 ΛCDM caveats
hexa-cosmos cosmology        # SPEC — print spec path
hexa-cosmos particle         # SPEC — print spec path
hexa-cosmos observatory      # SPEC — print spec path
```

---

## §Cross-link

Sister substrates (each independent, MIT/Apache-2.0 standalone):

- **[`dancinlab/hexa-space`](https://github.com/dancinlab/hexa-space)**
  — observation-side ops (aerospace + astronomy + astrobiology).
  hexa-cosmos provides the theoretical Cosmos substrate; hexa-space provides
  the observational ops that ground it.
- **[`dancinlab/hexa-millennium`](https://github.com/dancinlab/hexa-millennium)**
  — math substrate cousin. n=6 invariant lattice provenance lives here.
- **[`dancinlab/hexa-bio`](https://github.com/dancinlab/hexa-bio)**
  — sister extraction template (4-verb molecular toolkit, same n=6 lattice).

### Provenance

Extracted 2026-05-06 from `canon@c0f1f570`:

- `cosmology/`    ← `domains/physics/cosmology/`
- `particle/`     ← `domains/physics/cosmology-particle/`
- `observatory/`  ← `domains/physics/cosmic-observatory/`

The originating spec lives at `canon@c0f1f570` (read-only); this
repo is a thin standalone wrapper that exposes the 3 pillars + a placeholder
`.hexa` CLI router + the ΛCDM-vs-n=6 candidate comparison table.

---

## §License

MIT — see [LICENSE](LICENSE).

Copyright (c) 2026 박민우 <nerve011235@gmail.com>.
