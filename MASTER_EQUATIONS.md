# Theorema Aureum 143 — Master Equation List

**Volume I · Morning Star Project · Certificate Ledger**

> Generated 2026-06-15. Source of truth: `scripts/check-towers.sh` BRICKS array.
> All Clay surfaces **OPEN**. Axiom footprint: `{propext, Classical.choice, Quot.sound}`.
> sorry = 0 in all registered bricks (1 documented in KP.Basic.CERT_Arb only).
> YM Surface #1 **OPEN** — no mass-gap / μ > 0 claim.

---

## Summary

| Tower | Bricks |
|-------|--------|
| `KP.Basic` | 4 |
| `KP.Main` | 2 |
| `Towers.NS` | 80 |
| `Towers.RH` | 2 |
| `Towers.Spectral` | 55 |
| `Towers.YM` | 521 |
| **TOTAL** | **664** |

---

## KP — Kotecký–Preiss Cluster Expansion (Basic)

*Single-site weight enclosures and polynomial brackets for the KP convergence criterion at β = 0.86. Necessary-not-sufficient for Surface #1; YM mass gap stays **OPEN**.*

### Module: `KP.Basic.CERT_Arb`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `exp_neg_086_lower` | Lower bound: e^{-0.86} ≥ r for a certified rational r (enclosure via Taylor series). |
| 2 | `tail_negligible` | The tail ∑_{k≥K} (activity)^k is bounded by a negligible ε term at β = 0.86. |
| 3 | `w1_poly_rat_086` | Rational polynomial bracket for w₁ at β = 0.86: certifies a ℚ enclosure of the single-site weight integral. |

### Module: `KP.Basic.D4`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `w1_0p86_gt_seventh` | Numerical certificate: w₁(β=0.86) > 1/7 — the KP summability threshold (single-site SU(3) weight exceeds 1/7 at β₀). |

## KP — Kotecký–Preiss Cluster Expansion (Main)

*Cluster-expansion moment formula and β₀ bracket certificate. Conditional: discharges no Clay surface.*

### Module: `KP.Main`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `kp_beta0_bracket` | β₀ bracket certificate: the critical inverse coupling β₀ lies in the certified interval [0.85, 0.87]. |
| 2 | `kp_moments_exact` | Exact KP cluster-expansion moment formula: E[f(Φ)] = ∑_γ ρ(γ)·f(γ) for the truncated activity measure. |

## NS — Navier–Stokes Tower (frozen at Clay boundary)

*Placeholder H¹-norm and finite-energy schema; symmetry combinators (translation, rotation, Galilean boost, parity, Euclidean motion). NS Surfaces #1/#2 stay **OPEN**. Tower frozen at milestone `NS-540-phase6-clay-boundary`.*

### Module: `Towers.NS.EnergyIneq`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `EnergyMonotone` | Named combinator: EnergyMonotone u u₀ ↔ ∃ M, ∀ t x, ‖u t x‖ ≤ M (placeholder energy-monotone). |
| 2 | `EnergyMonotone_of_h1norm_const` | If H1Norm is constant, EnergyMonotone holds (schematic combinator). |
| 3 | `EnergyMonotone_zero` | Zero velocity field satisfies EnergyMonotone (trivial witness M = 0). |
| 4 | `H1Norm_eq_norm_apply_zero` | Named unfolder: H1Norm u t = ‖u 0 0‖ (placeholder evaluation at (t,x)=(0,0)). |
| 5 | `H1Norm_nonneg` | The placeholder H¹-norm is non-negative: 0 ≤ ‖u‖_{H¹}. |
| 6 | `H1Norm_zero` | H¹-placeholder norm of the zero velocity field is 0: ‖0‖_{H¹} = 0. |
| 7 | `HasFiniteEnergy_add` | Finite-energy is closed under pointwise sum: M₁+M₂ via triangle inequality. |
| 8 | `HasFiniteEnergy_const` | Every constant spacetime field fun _ _ => c has finite placeholder energy (M = ‖c‖). |
| 9 | `HasFiniteEnergy_euclidean_motion` | Full Euclidean motion E(3): HasFiniteEnergy u₀ → HasFiniteEnergy (u₀ ·(R·+a)). |
| 10 | `HasFiniteEnergy_galilean_boost` | Galilean boost: HasFiniteEnergy u₀ → HasFiniteEnergy (u₀ ·(·+v·t)). |
| 11 | `HasFiniteEnergy_galilean_group` | Full Galilean group invariance of the placeholder finite-energy predicate. |
| 12 | `HasFiniteEnergy_of_bounded_zero` | ∀ x, ‖u₀ 0 x‖ ≤ M → HasFiniteEnergy u₀ (first-slot uniform bound). |
| 13 | `HasFiniteEnergy_of_smul_bounded` | |f(x)| ≤ 1, |·| ≤ M → HasFiniteEnergy (f • c). |
| 14 | `HasFiniteEnergy_parity` | Parity (spatial reflection) invariance: HasFiniteEnergy u₀ → HasFiniteEnergy (u₀ ·(-·)). |
| 15 | `HasFiniteEnergy_rotate` | Rotational invariance: HasFiniteEnergy u₀ → HasFiniteEnergy (u₀ ·(R ·)) for isometry R. |
| 16 | `HasFiniteEnergy_rotating_frame` | NS energy / regularity lemma: HasFiniteEnergy rotating frame. |
| 17 | `HasFiniteEnergy_spacetime_rigid_motion` | NS energy / regularity lemma: HasFiniteEnergy spacetime rigid motion. |
| 18 | `HasFiniteEnergy_time_reverse` | NS energy / regularity lemma: HasFiniteEnergy time reverse. |
| 19 | `HasFiniteEnergy_time_reverse_signed` | NS energy / regularity lemma: HasFiniteEnergy time reverse signed. |
| 20 | `HasFiniteEnergy_time_translate` | Time-translation: ∀ x, ‖u₀ s x‖ ≤ M → HasFiniteEnergy (fun t => u₀ (t+s)). |
| 21 | `HasFiniteEnergy_translate` | Spatial translation invariance: HasFiniteEnergy u₀ → HasFiniteEnergy (u₀ ·(·+a)). |
| 22 | `HasFiniteEnergy_zero` | The zero velocity field has finite placeholder energy (witness M = 0). |

### Module: `Towers.NS.Energy`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `energy_decomposition` | NS energy / regularity lemma: energy decomposition. |
| 2 | `energy_nonincreasing_flow` | NS energy / regularity lemma: energy nonincreasing flow. |
| 3 | `finite_energy_persistent` | NS energy / regularity lemma: finite energy persistent. |
| 4 | `kinetic_energy_def` | NS energy / regularity lemma: kinetic energy def. |
| 5 | `potential_energy_def` | NS energy / regularity lemma: potential energy def. |

### Module: `Towers.NS.EnergyV2`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `BKM_implies_strong_L3_bound` | Beale–Kato–Majda blow-up criterion schema: BKM implies strong L3 bound. |
| 2 | `BealeKatoMajda_bootstrap` | Beale–Kato–Majda blow-up criterion schema: BealeKatoMajda bootstrap. |
| 3 | `BealeKatoMajda_criterion` | Beale–Kato–Majda blow-up criterion schema: BealeKatoMajda criterion. |
| 4 | `BealeKatoMajda_criterion_schema` | Named-Prop schema for the NS surface: BealeKatoMajda criterion schema. |
| 5 | `BealeKatoMajda_implies_global` | Beale–Kato–Majda blow-up criterion schema: BealeKatoMajda implies global. |
| 6 | `Blowup_exclusion_small_target` | NS energy / regularity lemma: Blowup exclusion small target. |
| 7 | `Conditional_regularity_theorem` | NS energy / regularity lemma: Conditional regularity theorem. |
| 8 | `Dissipation` | NS energy / regularity lemma: Dissipation. |
| 9 | `Dissipation_nonneg` | NS energy / regularity lemma: Dissipation nonneg. |
| 10 | `Dissipation_positive_ae` | NS energy / regularity lemma: Dissipation positive ae. |
| 11 | `Dissipation_real` | NS energy / regularity lemma: Dissipation real. |
| 12 | `EnergyDecayBound` | NS energy / regularity lemma: EnergyDecayBound. |
| 13 | `EnergyDissipationIntegral` | NS energy / regularity lemma: EnergyDissipationIntegral. |
| 14 | `EnergyEnstrophy_interpolation` | Enstrophy (‖ω‖²_L²) lemma: EnergyEnstrophy interpolation. |
| 15 | `Energy_decay_exponential` | NS energy / regularity lemma: Energy decay exponential. |
| 16 | `Energy_decay_optimal` | NS energy / regularity lemma: Energy decay optimal. |
| 17 | `Enstrophy` | Enstrophy (‖ω‖²_L²) lemma: Enstrophy. |
| 18 | `EnstrophyBalance` | Enstrophy (‖ω‖²_L²) lemma: EnstrophyBalance. |
| 19 | `Enstrophy_bound_from_small_data` | Enstrophy (‖ω‖²_L²) lemma: Enstrophy bound from small data. |
| 20 | `Enstrophy_bound_global` | Enstrophy (‖ω‖²_L²) lemma: Enstrophy bound global. |
| 21 | `Enstrophy_bound_unconditional` | Enstrophy (‖ω‖²_L²) lemma: Enstrophy bound unconditional. |
| 22 | `Enstrophy_critical_bound` | Enstrophy (‖ω‖²_L²) lemma: Enstrophy critical bound. |
| 23 | `Global_regularity_proven` | NS energy / regularity lemma: Global regularity proven. |
| 24 | `Global_scheme_for_all_data` | NS energy / regularity lemma: Global scheme for all data. |
| 25 | `H1Norm_real` | NS energy / regularity lemma: H1Norm real. |
| 26 | `H1Norm_v2` | NS energy / regularity lemma: H1Norm v2. |
| 27 | `L3_critical_bound_bootstrap` | NS energy / regularity lemma: L3 critical bound bootstrap. |
| 28 | `Ladyzhenskaya_4D_sharp` | NS energy / regularity lemma: Ladyzhenskaya 4D sharp. |
| 29 | `Ladyzhenskaya_bound_refined_4D` | NS energy / regularity lemma: Ladyzhenskaya bound refined 4D. |
| 30 | `Ladyzhenskaya_inequality` | NS energy / regularity lemma: Ladyzhenskaya inequality. |
| 31 | `LerayEnergyIneq_real` | Leray–Hopf energy inequality schema: LerayEnergyIneq real. |
| 32 | `LerayHopf_unique` | Leray–Hopf energy inequality schema: LerayHopf unique. |
| 33 | `LerayHopf_weak_solution_exists` | Leray–Hopf energy inequality schema: LerayHopf weak solution exists. |
| 34 | `NavierStokes_global_regular` | NS energy / regularity lemma: NavierStokes global regular. |
| 35 | `NavierStokes_global_regular_promotion` | NS energy / regularity lemma: NavierStokes global regular promotion. |
| 36 | `NavierStokes_global_regular_promotion_v2` | NS energy / regularity lemma: NavierStokes global regular promotion v2. |
| 37 | `Serrin_criterion_L3` | NS energy / regularity lemma: Serrin criterion L3. |
| 38 | `SmallDataGlobal_nonzero` | Small-data global existence: SmallDataGlobal nonzero. |
| 39 | `SmallDataGlobal_proven` | Small-data global existence: SmallDataGlobal proven. |
| 40 | `SmallDataGlobal_schema` | Named-Prop schema for the NS surface: SmallDataGlobal schema. |
| 41 | `ViscosityScaling` | NS energy / regularity lemma: ViscosityScaling. |
| 42 | `blowup_excluded` | NS energy / regularity lemma: blowup excluded. |
| 43 | `enstrophy_bootstrap_lemma` | NS energy / regularity lemma: enstrophy bootstrap lemma. |
| 44 | `enstrophy_bootstrap_strong` | NS energy / regularity lemma: enstrophy bootstrap strong. |
| 45 | `enstrophy_bound_from_Ladyzhenskaya` | NS energy / regularity lemma: enstrophy bound from Ladyzhenskaya. |
| 46 | `enstrophy_bound_global` | NS energy / regularity lemma: enstrophy bound global. |
| 47 | `enstrophy_differential_inequality` | NS energy / regularity lemma: enstrophy differential inequality. |
| 48 | `enstrophy_differential_inequality_conditional` | NS energy / regularity lemma: enstrophy differential inequality conditional. |
| 49 | `vorticity_L2_energy_identity` | NS energy / regularity lemma: vorticity L2 energy identity. |
| 50 | `vorticity_equation_L2_energy_bound` | NS energy / regularity lemma: vorticity equation L2 energy bound. |

### Module: `Towers.NS.RealH1Norm`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `H1NormReal_nonneg` | Navier–Stokes lemma: H1NormReal nonneg. |
| 2 | `H1NormReal_zero_eq_zero` | Navier–Stokes lemma: H1NormReal zero eq zero. |
| 3 | `frobNormSq_nonneg` | Navier–Stokes lemma: frobNormSq nonneg. |

## RH — Riemann Hypothesis Tower

*Zero-density monotonicity and Bost–Connes threshold certificate. RH stays **OPEN**; these are necessary scaffolding lemmas, not a proof of RH.*

### Module: `Towers.RH.Chain.C06_ZetaControl`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `bost_connes_threshold` | Bost–Connes threshold: the KMS phase-transition inverse temperature β_c lies in the certified rational interval. |

### Module: `Towers.RH.ZeroDensity`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `N_monotone_in_sigma` | The zero-density counting function N(σ,T) = #{ρ : Re(ρ) ≥ σ, |Im(ρ)| ≤ T} is monotone non-increasing in σ. |

## Spectral — Operator / Spectral Theory Tower

*Mass-gap schema, OS axiom framework, spectral combinators. All schema Prop-level; YM mass gap stays **OPEN**.*

### Module: `Towers.Spectral.Operator`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `Hamiltonian_operator_def` | Spectral schema or combinator: Hamiltonian operator def. |
| 2 | `MassGap_def` | Spectral schema or combinator: MassGap def. |
| 3 | `mass_gap_pos_means_spectrum_gap` | Spectral schema or combinator: mass gap pos means spectrum gap. |
| 4 | `vacuum_is_eigenstate` | Spectral schema or combinator: vacuum is eigenstate. |
| 5 | `vacuum_state_def` | Spectral schema or combinator: vacuum state def. |

### Module: `Towers.Spectral.OperatorV2`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `Hamiltonian_IR_gap_uniform` | Spectral schema or combinator: Hamiltonian IR gap uniform. |
| 2 | `Hamiltonian_IR_regularized` | Spectral schema or combinator: Hamiltonian IR regularized. |
| 3 | `Hamiltonian_compact_resolvent_schema` | Named-Prop schema: (H+λ)⁻¹ is compact — prerequisite for discrete spectrum. |
| 4 | `Hamiltonian_compact_resolvent_toy` | (H₀+λ)⁻¹ is compact on EuclideanSpace ℝ (Fin n) with N = 0. |
| 5 | `Hamiltonian_discrete_spectrum_from_compact_resolvent` | Combinator: compact resolvent + empty essential spectrum → discrete spectrum. |
| 6 | `Hamiltonian_mass_gap_toy` | Toy mass gap: ∃ Δ > 0, MassGap (H₀) Δ on the one-point space (Fin 0). |
| 7 | `Hamiltonian_operator_v2` | Spectral schema or combinator: Hamiltonian operator v2. |
| 8 | `Hamiltonian_psd` | The placeholder YM Hamiltonian is positive semi-definite: ⟨ψ, Hψ⟩ ≥ 0 for all ψ. |
| 9 | `Hamiltonian_spectrum_toy` | Toy-model spectrum: σ(H₀) on EuclideanSpace ℝ (Fin 0) is the singleton {0}. |
| 10 | `Hamiltonian_symmetric` | The placeholder YM Hamiltonian operator is symmetric on EuclideanSpace ℂ (Fin 3). |
| 11 | `IR_cutoff_gap_estimate` | Spectral schema or combinator: IR cutoff gap estimate. |
| 12 | `IR_cutoff_gap_estimate_v2` | Spectral schema or combinator: IR cutoff gap estimate v2. |
| 13 | `IR_gap_lower_bound_explicit` | Spectral schema or combinator: IR gap lower bound explicit. |
| 14 | `IR_removal_limit_schema` | Spectral schema or combinator: IR removal limit schema. |
| 15 | `InfraredCutoff_Λ` | Spectral schema or combinator: InfraredCutoff Λ. |
| 16 | `MassGap_IR` | Spectral schema or combinator: MassGap IR. |
| 17 | `MassGap_YM_operator` | Spectral schema or combinator: MassGap YM operator. |
| 18 | `MassGap_YM_operator_promotion` | Spectral schema or combinator: MassGap YM operator promotion. |
| 19 | `MassGap_YM_operator_promotion_v2` | Spectral schema or combinator: MassGap YM operator promotion v2. |
| 20 | `MassGap_continuum` | Spectral schema or combinator: MassGap continuum. |
| 21 | `MassGap_exists_diagonal` | On a diagonal Hamiltonian schema, ∃ Δ > 0, MassGap H Δ is witnessed explicitly. |
| 22 | `MassGap_from_discrete_spectrum` | If σ_ess(H) = ∅ and (H+λ)⁻¹ compact, then ∃ Δ > 0, MassGap H Δ (combinator). |
| 23 | `MassGap_persists_under_limit_schema` | Spectral schema or combinator: MassGap persists under limit schema. |
| 24 | `MassGap_toy_exists` | ∃ H, ∃ μ > 0, MassGap H μ — existential mass-gap on Fin 0. |
| 25 | `MassGap_toy_proven` | ∃ μ > 0, MassGap (Hamiltonian_operator 0) μ — first fully-∃ mass-gap witness (vacuous on Fin 0). |
| 26 | `Neumann_eigenvalue_bound_Λ` | Spectral schema or combinator: Neumann eigenvalue bound Λ. |
| 27 | `Neumann_eigenvalue_lower_bound_Λ` | Spectral schema or combinator: Neumann eigenvalue lower bound Λ. |
| 28 | `Poincare_inequality_IR_lattice` | Spectral schema or combinator: Poincare inequality IR lattice. |
| 29 | `Poincare_inequality_IR_lattice_v2` | Spectral schema or combinator: Poincare inequality IR lattice v2. |
| 30 | `continuum_limit_exists` | Spectral schema or combinator: continuum limit exists. |
| 31 | `essential_spectrum_empty_schema` | Named-Prop schema: σ_ess(H) = ∅ (requires compact resolvent to discharge). |
| 32 | `essential_spectrum_empty_toy` | σ_ess(H₀) = ∅ on Fin 0 (vacuous via Subsingleton.elim; fails on Fin(n+1)). |
| 33 | `first_excitation_continuum` | Spectral schema or combinator: first excitation continuum. |
| 34 | `first_excitation_explicit` | Noncomputable standard basis vector e₀ on Fin(n+1) as first-excitation candidate. |
| 35 | `first_excitation_lower_bound` | The first excitation energy satisfies μ₁ ≥ Δ where Δ is the mass gap witness. |
| 36 | `first_excited_state_exists` | A non-vacuum unit vector orthogonal to the vacuum exists (combinator; FALSE on Fin 0). |
| 37 | `gap_equals_μ` | MassGap H Δ ↔ (0 < Δ ∧ ∀ A ≠ vacuum, Δ ≤ |H A − H vacuum|) — definitional Iff. |
| 38 | `gap_stability_under_limit` | Spectral schema or combinator: gap stability under limit. |
| 39 | `gap_uniform_in_Lambda` | Spectral schema or combinator: gap uniform in Lambda. |
| 40 | `gap_uniform_in_Lambda_v2` | Spectral schema or combinator: gap uniform in Lambda v2. |
| 41 | `lower_bound_from_psd` | A PSD lower bound on H gives a lower bound on the spectral gap via min-max. |
| 42 | `mass_gap_from_lower_bound` | If inf σ(H) ≥ Δ > 0, then H has a mass gap of at least Δ (combinator). |
| 43 | `minimax_characterization_μ` | Minimax characterization: μ = inf{⟨ψ,Hψ⟩ : ψ ⊥ vacuum, ‖ψ‖=1}. |
| 44 | `minimax_μ_equals_gap` | The minimax value μ equals the mass gap Δ: projection of the MassGap conjunction. |
| 45 | `spectrum_above_gap_continuous` | Spectral schema or combinator: spectrum above gap continuous. |
| 46 | `spectrum_discrete_below_2Δ` | Spectral schema or combinator: spectrum discrete below 2Δ. |
| 47 | `strong_resolvent_convergence` | Spectral schema or combinator: strong resolvent convergence. |
| 48 | `vacuum_is_ground_state` | The vacuum connection is the ground state: H(vacuum) ≤ H(A) for all A. |
| 49 | `vacuum_spectral_gap_corollary` | Corollary of MassGap_toy_proven: vacuum has a spectral gap in the toy model. |
| 50 | `vacuum_unique_of_kernel_one_dim` | If ker(H) is one-dimensional, the vacuum state is unique up to phase. |

## YM — Yang–Mills Tower

*SU(3) gauge field structure, Lie algebra, Wilson action, heat kernel, BDP phase reversal, Varadhan envelope, KP transfer. YM Surface #1 stays **OPEN**.*

### Module: `Towers.YM.AnalyticContinuationCore`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `exp_neg_continues` | Yang–Mills lemma: exp neg continues. |

### Module: `Towers.YM.BDP_PhaseReversal`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `Cert_fails_at_291` | Bridge test fails at threshold 291 — certifies the BDP boundary arithmetic. |
| 2 | `Cert_lemma2` | BDP arithmetic lemma 2: digit-extraction bound on κ^m mod πℤ. |
| 3 | `Cert_llm_trunc` | Certification of the LLM truncation error at 30-digit Machin π bounds. |
| 4 | `Cert_m_boundary` | Boundary mass certificate: the BDP m-boundary for the P5 prime family. |
| 5 | `Cert_phase_reversal` | Phase reversal at P5: χ(1/p₅)=13 < χ(fracDist p₅)=14 (requires 30-digit π). |

### Module: `Towers.YM.BrydgesFederbush_D1D3`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `geometric_activity_bound` | Yang–Mills lemma: geometric activity bound. |
| 2 | `kp_summable` | Yang–Mills lemma: kp summable. |
| 3 | `peierls_branching_bound` | Yang–Mills lemma: peierls branching bound. |

### Module: `Towers.YM.BrydgesFederbush_D5`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `d5a_closed` | Yang–Mills lemma: d5a closed. |
| 2 | `w1_seven_pos_Surface` | Yang–Mills lemma: w1 seven pos Surface. |

### Module: `Towers.YM.Casimir`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `Casimir_SU3_explicit_real_ge_quadratic` | Yang–Mills lemma: Casimir SU3 explicit real ge quadratic. |

### Module: `Towers.YM.CloverF`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `cloverF_antisymmetric` | Yang–Mills lemma: cloverF antisymmetric. |
| 2 | `cloverF_diagonal_zero` | Yang–Mills lemma: cloverF diagonal zero. |
| 3 | `cloverF_trivial_eq_zero` | Yang–Mills lemma: cloverF trivial eq zero. |

### Module: `Towers.YM.ClusterExpansion`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `Base_case_K_one` | Transfer-operator / polymer-activity lemma: Base case K one. |
| 2 | `Base_case_discharge` | Transfer-operator / polymer-activity lemma: Base case discharge. |
| 3 | `Brydges_Federbush_lemma` | Transfer-operator / polymer-activity lemma: Brydges Federbush lemma. |
| 4 | `Brydges_Federbush_lemma_exp` | Transfer-operator / polymer-activity lemma: Brydges Federbush lemma exp. |
| 5 | `Casimir_SU3_eq_three` | Transfer-operator / polymer-activity lemma: Casimir SU3 eq three. |
| 6 | `Casimir_SU3_explicit_at_fundamental` | Transfer-operator / polymer-activity lemma: Casimir SU3 explicit at fundamental. |
| 7 | `Casimir_SU3_explicit_at_zero` | Transfer-operator / polymer-activity lemma: Casimir SU3 explicit at zero. |
| 8 | `Casimir_SU3_explicit_nonneg` | Transfer-operator / polymer-activity lemma: Casimir SU3 explicit nonneg. |
| 9 | `Casimir_SU3_pos` | Transfer-operator / polymer-activity lemma: Casimir SU3 pos. |
| 10 | `Casimir_eigenvalue_SU3` | Transfer-operator / polymer-activity lemma: Casimir eigenvalue SU3. |
| 11 | `Casimir_eigenvalue_nonneg` | Transfer-operator / polymer-activity lemma: Casimir eigenvalue nonneg. |
| 12 | `Character_def_zero` | Transfer-operator / polymer-activity lemma: Character def zero. |
| 13 | `Character_orthogonality` | Transfer-operator / polymer-activity lemma: Character orthogonality. |
| 14 | `Cluster_convergence_radius` | Transfer-operator / polymer-activity lemma: Cluster convergence radius. |
| 15 | `Cluster_estimate_base` | Transfer-operator / polymer-activity lemma: Cluster estimate base. |
| 16 | `Cluster_expansion_step_eq_Wilson` | Transfer-operator / polymer-activity lemma: Cluster expansion step eq Wilson. |
| 17 | `Cluster_expansion_step_zero` | Transfer-operator / polymer-activity lemma: Cluster expansion step zero. |
| 18 | `Combinatorial_constant_e` | Transfer-operator / polymer-activity lemma: Combinatorial constant e. |
| 19 | `Combinatorial_constant_e_one_le` | Transfer-operator / polymer-activity lemma: Combinatorial constant e one le. |
| 20 | `Combinatorial_constant_e_pos` | Transfer-operator / polymer-activity lemma: Combinatorial constant e pos. |
| 21 | `Combinatorial_constant_e_real` | Transfer-operator / polymer-activity lemma: Combinatorial constant e real. |
| 22 | `Combinatorial_constant_e_real_def` | Transfer-operator / polymer-activity lemma: Combinatorial constant e real def. |
| 23 | `Combinatorial_constant_e_real_eq_e` | Transfer-operator / polymer-activity lemma: Combinatorial constant e real eq e. |
| 24 | `Combinatorial_constant_e_real_one_le` | Transfer-operator / polymer-activity lemma: Combinatorial constant e real one le. |
| 25 | `Combinatorial_constant_e_real_pos` | Transfer-operator / polymer-activity lemma: Combinatorial constant e real pos. |
| 26 | `Correlation_decay_from_CE` | Transfer-operator / polymer-activity lemma: Correlation decay from CE. |
| 27 | `Decay_constant_eq_one` | Transfer-operator / polymer-activity lemma: Decay constant eq one. |
| 28 | `Decay_constant_from_KP` | Transfer-operator / polymer-activity lemma: Decay constant from KP. |
| 29 | `Decay_constant_pos` | Transfer-operator / polymer-activity lemma: Decay constant pos. |
| 30 | `Decay_constant_real` | Transfer-operator / polymer-activity lemma: Decay constant real. |
| 31 | `Decay_constant_real_eq_one` | Transfer-operator / polymer-activity lemma: Decay constant real eq one. |
| 32 | `Decay_constant_real_pos` | Transfer-operator / polymer-activity lemma: Decay constant real pos. |
| 33 | `Dimension_formula_SU3` | Transfer-operator / polymer-activity lemma: Dimension formula SU3. |
| 34 | `Exp_moment_bound` | Transfer-operator / polymer-activity lemma: Exp moment bound. |
| 35 | `Exp_moment_bound_nonneg` | Transfer-operator / polymer-activity lemma: Exp moment bound nonneg. |
| 36 | `Gaussian_measure_mean_eq_zero` | Transfer-operator / polymer-activity lemma: Gaussian measure mean eq zero. |
| 37 | `Gaussian_measure_variance_eq_one` | Transfer-operator / polymer-activity lemma: Gaussian measure variance eq one. |
| 38 | `Gaussian_measure_variance_nonneg` | Transfer-operator / polymer-activity lemma: Gaussian measure variance nonneg. |
| 39 | `Gaussian_measure_variance_pos` | Transfer-operator / polymer-activity lemma: Gaussian measure variance pos. |
| 40 | `Heat_kernel_asymptotics` | Transfer-operator / polymer-activity lemma: Heat kernel asymptotics. |
| 41 | `Heat_kernel_asymptotics_real` | Transfer-operator / polymer-activity lemma: Heat kernel asymptotics real. |
| 42 | `Heat_kernel_at_identity_nonneg` | Transfer-operator / polymer-activity lemma: Heat kernel at identity nonneg. |
| 43 | `Heat_kernel_def_pos` | Transfer-operator / polymer-activity lemma: Heat kernel def pos. |
| 44 | `Heat_kernel_def_real_at_zero` | Transfer-operator / polymer-activity lemma: Heat kernel def real at zero. |
| 45 | `Heat_kernel_def_real_nonneg` | Transfer-operator / polymer-activity lemma: Heat kernel def real nonneg. |
| 46 | `Heat_kernel_def_real_pos_of_pos` | Transfer-operator / polymer-activity lemma: Heat kernel def real pos of pos. |
| 47 | `Heat_kernel_tail_estimate` | Transfer-operator / polymer-activity lemma: Heat kernel tail estimate. |
| 48 | `High_temp_bound_base` | Transfer-operator / polymer-activity lemma: High temp bound base. |
| 49 | `High_temp_bound_base_nonneg` | Transfer-operator / polymer-activity lemma: High temp bound base nonneg. |
| 50 | `High_temp_expansion` | Transfer-operator / polymer-activity lemma: High temp expansion. |
| 51 | `Kotecky_Preiss_criterion` | Transfer-operator / polymer-activity lemma: Kotecky Preiss criterion. |
| 52 | `Kotecky_Preiss_full` | Transfer-operator / polymer-activity lemma: Kotecky Preiss full. |
| 53 | `Kotecky_Preiss_real` | Transfer-operator / polymer-activity lemma: Kotecky Preiss real. |
| 54 | `Kotecky_Preiss_slack` | Transfer-operator / polymer-activity lemma: Kotecky Preiss slack. |
| 55 | `Kotecky_Preiss_strict` | Transfer-operator / polymer-activity lemma: Kotecky Preiss strict. |
| 56 | `Kotecky_Preiss_strict_real` | Transfer-operator / polymer-activity lemma: Kotecky Preiss strict real. |
| 57 | `Kotecky_Preiss_strict_slack` | Transfer-operator / polymer-activity lemma: Kotecky Preiss strict slack. |
| 58 | `MassGap_YM4_Clay_from_strict` | Transfer-operator / polymer-activity lemma: MassGap YM4 Clay from strict. |
| 59 | `MassGap_YM4_from_KP` | Transfer-operator / polymer-activity lemma: MassGap YM4 from KP. |
| 60 | `MassGap_from_spectral_radius` | Transfer-operator / polymer-activity lemma: MassGap from spectral radius. |
| 61 | `Mayer_expansion_def` | Transfer-operator / polymer-activity lemma: Mayer expansion def. |
| 62 | `Mayer_graph_expansion` | Transfer-operator / polymer-activity lemma: Mayer graph expansion. |
| 63 | `Mayer_overlap_symm` | Transfer-operator / polymer-activity lemma: Mayer overlap symm. |
| 64 | `Peter_Weyl_partial` | Transfer-operator / polymer-activity lemma: Peter Weyl partial. |
| 65 | `Plaquette_action_def_zero` | Transfer-operator / polymer-activity lemma: Plaquette action def zero. |
| 66 | `Plaquette_action_nonneg` | Transfer-operator / polymer-activity lemma: Plaquette action nonneg. |
| 67 | `Polymer_activity_bound` | Transfer-operator / polymer-activity lemma: Polymer activity bound. |
| 68 | `Polymer_activity_bound_real` | Transfer-operator / polymer-activity lemma: Polymer activity bound real. |
| 69 | `Polymer_activity_bound_real_exp` | Transfer-operator / polymer-activity lemma: Polymer activity bound real exp. |
| 70 | `Polymer_activity_bound_simple` | Transfer-operator / polymer-activity lemma: Polymer activity bound simple. |
| 71 | `Polymer_activity_def_zero` | Transfer-operator / polymer-activity lemma: Polymer activity def zero. |
| 72 | `Polymer_measure_def` | Transfer-operator / polymer-activity lemma: Polymer measure def. |
| 73 | `Polymer_measure_pos` | Transfer-operator / polymer-activity lemma: Polymer measure pos. |
| 74 | `Polymer_partition_function` | Transfer-operator / polymer-activity lemma: Polymer partition function. |
| 75 | `Polymer_support_def_id` | Transfer-operator / polymer-activity lemma: Polymer support def id. |
| 76 | `SU3_dimension_eq_eight` | Transfer-operator / polymer-activity lemma: SU3 dimension eq eight. |
| 77 | `SU3_dimension_pos` | Transfer-operator / polymer-activity lemma: SU3 dimension pos. |
| 78 | `Single_plaquette_handle` | Transfer-operator / polymer-activity lemma: Single plaquette handle. |
| 79 | `Small_beta_regime_def_unfold` | Transfer-operator / polymer-activity lemma: Small beta regime def unfold. |
| 80 | `Small_beta_regime_of_lt_zero` | Transfer-operator / polymer-activity lemma: Small beta regime of lt zero. |
| 81 | `Small_beta_threshold_eq_one` | Transfer-operator / polymer-activity lemma: Small beta threshold eq one. |
| 82 | `Small_beta_threshold_pos` | Transfer-operator / polymer-activity lemma: Small beta threshold pos. |
| 83 | `Small_coupling_KP_slack` | Transfer-operator / polymer-activity lemma: Small coupling KP slack. |
| 84 | `Small_coupling_from_KP` | Transfer-operator / polymer-activity lemma: Small coupling from KP. |
| 85 | `Small_g_regime_def` | Transfer-operator / polymer-activity lemma: Small g regime def. |
| 86 | `Small_g_regime_pos` | Transfer-operator / polymer-activity lemma: Small g regime pos. |
| 87 | `Small_t_dominance` | Transfer-operator / polymer-activity lemma: Small t dominance. |
| 88 | `Small_t_dominance_real` | Transfer-operator / polymer-activity lemma: Small t dominance real. |
| 89 | `Spectral_radius_lt_one` | Transfer-operator / polymer-activity lemma: Spectral radius lt one. |
| 90 | `Spectral_radius_lt_one_real` | Transfer-operator / polymer-activity lemma: Spectral radius lt one real. |
| 91 | `Spectral_radius_lt_one_strict_real_handle` | Transfer-operator / polymer-activity lemma: Spectral radius lt one strict real handle. |
| 92 | `Stationary_phase_bound` | Transfer-operator / polymer-activity lemma: Stationary phase bound. |
| 93 | `Strict_contraction_CE` | Transfer-operator / polymer-activity lemma: Strict contraction CE. |
| 94 | `Strict_contraction_CE_le_one` | Transfer-operator / polymer-activity lemma: Strict contraction CE le one. |
| 95 | `Strict_contraction_real` | Transfer-operator / polymer-activity lemma: Strict contraction real. |
| 96 | `Strict_contraction_real_le_one` | Transfer-operator / polymer-activity lemma: Strict contraction real le one. |
| 97 | `Strict_contraction_real_strict_handle` | Transfer-operator / polymer-activity lemma: Strict contraction real strict handle. |
| 98 | `Transfer_bound_from_CE` | Transfer-operator / polymer-activity lemma: Transfer bound from CE. |
| 99 | `Transfer_contraction_from_CE` | Transfer-operator / polymer-activity lemma: Transfer contraction from CE. |
| 100 | `Transfer_from_measure` | Transfer-operator / polymer-activity lemma: Transfer from measure. |
| 101 | `Tree_graph_counting` | Transfer-operator / polymer-activity lemma: Tree graph counting. |
| 102 | `Tree_graph_counting_one` | Transfer-operator / polymer-activity lemma: Tree graph counting one. |
| 103 | `Tree_graph_counting_three` | Transfer-operator / polymer-activity lemma: Tree graph counting three. |
| 104 | `Tree_graph_counting_two` | Transfer-operator / polymer-activity lemma: Tree graph counting two. |
| 105 | `Truncation_error_bound` | Transfer-operator / polymer-activity lemma: Truncation error bound. |
| 106 | `Truncation_error_bound_value_nonneg` | Transfer-operator / polymer-activity lemma: Truncation error bound value nonneg. |
| 107 | `Ursell_bound_real` | Transfer-operator / polymer-activity lemma: Ursell bound real. |
| 108 | `Ursell_functions` | Transfer-operator / polymer-activity lemma: Ursell functions. |
| 109 | `Ursell_functions_bound` | Transfer-operator / polymer-activity lemma: Ursell functions bound. |
| 110 | `Ursell_tree_bound` | Transfer-operator / polymer-activity lemma: Ursell tree bound. |
| 111 | `Ursell_tree_bound_exp_real` | Transfer-operator / polymer-activity lemma: Ursell tree bound exp real. |
| 112 | `Ursell_tree_bound_real` | Transfer-operator / polymer-activity lemma: Ursell tree bound real. |
| 113 | `Ursell_tree_bound_simple` | Transfer-operator / polymer-activity lemma: Ursell tree bound simple. |
| 114 | `Weyl_character_formula_SU3` | Transfer-operator / polymer-activity lemma: Weyl character formula SU3. |
| 115 | `Weyl_dim_SU3_explicit_at_fundamental` | Transfer-operator / polymer-activity lemma: Weyl dim SU3 explicit at fundamental. |
| 116 | `Weyl_dim_SU3_explicit_at_zero` | Transfer-operator / polymer-activity lemma: Weyl dim SU3 explicit at zero. |
| 117 | `Weyl_dim_SU3_explicit_pos` | Transfer-operator / polymer-activity lemma: Weyl dim SU3 explicit pos. |
| 118 | `Weyl_dim_def_pos` | Transfer-operator / polymer-activity lemma: Weyl dim def pos. |
| 119 | `Weyl_sum_bounded_by_heat` | Transfer-operator / polymer-activity lemma: Weyl sum bounded by heat. |
| 120 | `Weyl_sum_explicit_SU3_nonneg` | Transfer-operator / polymer-activity lemma: Weyl sum explicit SU3 nonneg. |
| 121 | `Weyl_sum_explicit_SU3_real_at_zero` | Transfer-operator / polymer-activity lemma: Weyl sum explicit SU3 real at zero. |
| 122 | `Weyl_sum_explicit_SU3_real_nonneg` | Transfer-operator / polymer-activity lemma: Weyl sum explicit SU3 real nonneg. |
| 123 | `Weyl_sum_monotone_N` | Transfer-operator / polymer-activity lemma: Weyl sum monotone N. |
| 124 | `Wick_pairing_constant_eq_one` | Transfer-operator / polymer-activity lemma: Wick pairing constant eq one. |
| 125 | `Wick_pairing_constant_pos` | Transfer-operator / polymer-activity lemma: Wick pairing constant pos. |
| 126 | `Wick_theorem_plaquette` | Transfer-operator / polymer-activity lemma: Wick theorem plaquette. |
| 127 | `Wilson_action_decomposition_zero` | Transfer-operator / polymer-activity lemma: Wilson action decomposition zero. |
| 128 | `Wilson_measure_def` | Transfer-operator / polymer-activity lemma: Wilson measure def. |
| 129 | `cluster_exp_bound` | Transfer-operator / polymer-activity lemma: cluster exp bound. |
| 130 | `cluster_exp_bound_pos` | Transfer-operator / polymer-activity lemma: cluster exp bound pos. |
| 131 | `heat_amplitude_constant_pos` | Transfer-operator / polymer-activity lemma: heat amplitude constant pos. |
| 132 | `heat_decay_constant_pos` | Transfer-operator / polymer-activity lemma: heat decay constant pos. |
| 133 | `mayer_Delta_constant` | Transfer-operator / polymer-activity lemma: mayer Delta constant. |
| 134 | `mayer_K_constant` | Transfer-operator / polymer-activity lemma: mayer K constant. |
| 135 | `mayer_K_pos` | Transfer-operator / polymer-activity lemma: mayer K pos. |
| 136 | `plaquette_activity_pw_ge_one` | Transfer-operator / polymer-activity lemma: plaquette activity pw ge one. |
| 137 | `plaquette_activity_pw_nonneg` | Transfer-operator / polymer-activity lemma: plaquette activity pw nonneg. |
| 138 | `plaquette_activity_pw_pos` | Transfer-operator / polymer-activity lemma: plaquette activity pw pos. |
| 139 | `polymer_activity_bound_real` | Transfer-operator / polymer-activity lemma: polymer activity bound real. |
| 140 | `polymer_activity_bound_real_pw` | Transfer-operator / polymer-activity lemma: polymer activity bound real pw. |

### Module: `Towers.YM.ContinuumHookup`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `continuum_heat_envelope_bound` | Yang–Mills lemma: continuum heat envelope bound. |
| 2 | `continuum_heat_envelope_bound_target_default` | Yang–Mills lemma: continuum heat envelope bound target default. |
| 3 | `continuum_heat_envelope_bound_widened_upper` | Yang–Mills lemma: continuum heat envelope bound widened upper. |
| 4 | `continuum_heat_envelope_pos_widened` | Yang–Mills lemma: continuum heat envelope pos widened. |

### Module: `Towers.YM.Continuum`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `AsymptoticFreedom` | Yang–Mills lemma: AsymptoticFreedom. |
| 2 | `IsMassGap` | Yang–Mills lemma: IsMassGap. |
| 3 | `YM4_Continuum` | Yang–Mills lemma: YM4 Continuum. |
| 4 | `lattice_to_continuum` | Yang–Mills lemma: lattice to continuum. |

### Module: `Towers.YM.EntropyBound`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `polymer_entropy_bound` | YM wall lemma: polymer entropy bound. |

### Module: `Towers.YM.EuclideanInvarianceCore`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `translateAction_zero` | Yang–Mills lemma: translateAction zero. |

### Module: `Towers.YM.GaugeField`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `GaugeField_zero_apply` | Yang–Mills lemma: GaugeField zero apply. |
| 2 | `YMHamiltonian_eq_norm_sq` | Yang–Mills lemma: YMHamiltonian eq norm sq. |
| 3 | `YMHamiltonian_nonneg` | Yang–Mills lemma: YMHamiltonian nonneg. |
| 4 | `YMHamiltonian_zero` | Yang–Mills lemma: YMHamiltonian zero. |
| 5 | `curvature_add` | Yang–Mills lemma: curvature add. |
| 6 | `curvature_zero` | Yang–Mills lemma: curvature zero. |

### Module: `Towers.YM.Geometry`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `curvature_4d_def` | Yang–Mills lemma: curvature 4d def. |
| 2 | `f_abc_antisymm` | Yang–Mills lemma: f abc antisymm. |
| 3 | `f_abc_jacobi` | Yang–Mills lemma: f abc jacobi. |
| 4 | `lattice_spacetime_4d_def` | Yang–Mills lemma: lattice spacetime 4d def. |
| 5 | `structure_constants_su3_full_def` | Yang–Mills lemma: structure constants su3 full def. |

### Module: `Towers.YM.GibbsMeasure`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `partitionFn_zero_beta_eq_one` | Measure / positivity lemma on SU(3): partitionFn zero beta eq one. |

### Module: `Towers.YM.KoteckyPreissReal`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `kotecky_preiss_real` | Yang–Mills lemma: kotecky preiss real. |

### Module: `Towers.YM.KoteckyPreiss`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `kotecky_preiss` | Yang–Mills lemma: kotecky preiss. |

### Module: `Towers.YM.KP_Closure`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `W1_KP_Surface_proved` | KP cluster-expansion lemma: W1 KP Surface proved. |
| 2 | `W1_one_seventh_proved` | KP cluster-expansion lemma: W1 one seventh proved. |
| 3 | `c_worst_fuss_catalan_lt_one` | KP cluster-expansion lemma: c worst fuss catalan lt one. |
| 4 | `gap_kp_star_gt_two` | KP cluster-expansion lemma: gap kp star gt two. |
| 5 | `log_two_gt_two_thirds` | KP cluster-expansion lemma: log two gt two thirds. |
| 6 | `z_kp_star_lt_seventh` | KP cluster-expansion lemma: z kp star lt seventh. |

### Module: `Towers.YM.KP_W1_Proof`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `w1_kp_lt` | SU(3) heat-trace / Tauberian lemma: w1 kp lt. |

### Module: `Towers.YM.LatticeGauge`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `G_eq_SU3` | Yang–Mills lemma: G eq SU3. |
| 2 | `GaugeConfig_eq_parametric` | Yang–Mills lemma: GaugeConfig eq parametric. |
| 3 | `Lattice_def` | Yang–Mills lemma: Lattice def. |

### Module: `Towers.YM.MassGapEnvelope`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `IsMassGap_mass_gap_envelope_default` | Yang–Mills lemma: IsMassGap mass gap envelope default. |
| 2 | `mass_gap_envelope_constant_pos` | Yang–Mills lemma: mass gap envelope constant pos. |
| 3 | `mass_gap_envelope_constant_widened_pos` | Yang–Mills lemma: mass gap envelope constant widened pos. |

### Module: `Towers.YM.MassGap`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `HilbertSpace_not_finiteDimensional` | Yang–Mills lemma: HilbertSpace not finiteDimensional. |
| 2 | `IsEigenstate_of_forall_zero` | Eigenstates of scaling-form predicate with coefficient 0 are trivial. |
| 3 | `IsEigenstate_zero_const` | ¬ IsEigenstate YMHamiltonian (fun _ => c) for constant c: no constant eigenstate. |
| 4 | `IsEigenstate_zero_zero` | ¬ IsEigenstate YMHamiltonian 0: zero is not an eigenstate of the placeholder Hamiltonian. |
| 5 | `MassGap` | Yang–Mills lemma: MassGap. |
| 6 | `MassGap_iff_pos` | Yang–Mills lemma: MassGap iff pos. |
| 7 | `MassGap_le_twelve_of_witness` | Yang–Mills lemma: MassGap le twelve of witness. |
| 8 | `MassGap_pos` | Yang–Mills lemma: MassGap pos. |
| 9 | `SU3Connection_component_det_one` | Each component has determinant 1: det(A i) = 1 (SU(3) membership). |
| 10 | `SU3Connection_component_mul_det_one` | det((A·B)(i)) = 1 (product stays in SU(3)). |
| 11 | `SU3Connection_component_mul_unitary` | (A·B)(i) is unitary: (A i)·(B i) ∈ U(3). |
| 12 | `SU3Connection_component_star_det_one` | det((A i)†) = 1 — conjugate-transpose is also in SU(3). |
| 13 | `SU3Connection_component_star_mul_self` | (A i)†·(A i) = I — full two-sided unitary law via star. |
| 14 | `SU3Connection_component_unitary` | Each component A(i) is a unitary matrix: (A i)†·(A i) = I. |
| 15 | `SU3Connection_mul_assoc` | SU(3) connection: (A·B)·C = A·(B·C) (associativity of gauge composition). |
| 16 | `SU3Connection_mul_one` | SU(3) connection: A·1 = A (right unit law). |
| 17 | `SU3Connection_one_mul` | SU(3) connection: 1·A = A (left unit law for the lattice gauge field). |
| 18 | `SU3Connection_one_one` | SU(3) connection at identity: (1)·(1) = 1. |
| 19 | `YMHamiltonianReal_vacuum_eq_zero` | Yang–Mills lemma: YMHamiltonianReal vacuum eq zero. |
| 20 | `YMHamiltonian_abs_le_twelve` | Yang–Mills lemma: YMHamiltonian abs le twelve. |
| 21 | `YMHamiltonian_abs_le_twelve_tight` | Yang–Mills lemma: YMHamiltonian abs le twelve tight. |
| 22 | `YMHamiltonian_diagNegOneOne_eq_neg_four` | Yang–Mills lemma: YMHamiltonian diagNegOneOne eq neg four. |
| 23 | `YMHamiltonian_no_eigenstate` | Yang–Mills lemma: YMHamiltonian no eigenstate. |
| 24 | `YMHamiltonian_no_nonzero_eigenstate` | Yang–Mills lemma: YMHamiltonian no nonzero eigenstate. |
| 25 | `YMHamiltonian_not_isEigenstate_zero` | The zero vector is not an eigenstate: YMHamiltonian ∧ ¬IsEigenstate ψ=0. |
| 26 | `YMHamiltonian_one_eq_twelve` | YMHamiltonian(fun _ => 1) = 12 — first numerical output of the schema. |
| 27 | `diagNegOneOneMat` | Yang–Mills lemma: diagNegOneOneMat. |
| 28 | `hilbertCanonicalFamily` | Yang–Mills lemma: hilbertCanonicalFamily. |
| 29 | `hilbertCanonicalFamily_orthonormal` | Yang–Mills lemma: hilbertCanonicalFamily orthonormal. |

### Module: `Towers.YM.NontrivialGap`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `nontrivial_gap` | Yang–Mills lemma: nontrivial gap. |

### Module: `Towers.YM.OSReconstruction`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `OSInnerProduct` | Osterwalder–Schrader axiom: OSInnerProduct. |
| 2 | `OSInnerProduct_symm` | Osterwalder–Schrader axiom: OSInnerProduct symm. |
| 3 | `OSNullSpace` | Osterwalder–Schrader axiom: OSNullSpace. |
| 4 | `OSSeminorm` | Osterwalder–Schrader axiom: OSSeminorm. |
| 5 | `OSSeminorm_nonneg` | Osterwalder–Schrader axiom: OSSeminorm nonneg. |
| 6 | `OS_Hilbert_complete` | Osterwalder–Schrader axiom: OS Hilbert complete. |
| 7 | `OS_Hilbert_quotient` | Osterwalder–Schrader axiom: OS Hilbert quotient. |
| 8 | `OS_Hilbert_separable` | Osterwalder–Schrader axiom: OS Hilbert separable. |
| 9 | `TimeZeroAlgebra_action` | Measure / positivity lemma on SU(3): TimeZeroAlgebra action. |
| 10 | `Transfer_contraction` | Measure / positivity lemma on SU(3): Transfer contraction. |
| 11 | `Transfer_operator_def` | Measure / positivity lemma on SU(3): Transfer operator def. |
| 12 | `Transfer_selfadjoint` | Measure / positivity lemma on SU(3): Transfer selfadjoint. |
| 13 | `Transfer_well_defined` | Measure / positivity lemma on SU(3): Transfer well defined. |
| 14 | `Vacuum_invariant` | Measure / positivity lemma on SU(3): Vacuum invariant. |
| 15 | `Vacuum_vector_norm_one` | Measure / positivity lemma on SU(3): Vacuum vector norm one. |
| 16 | `pullback_pullback` | Measure / positivity lemma on SU(3): pullback pullback. |
| 17 | `pullback_vacuum` | Measure / positivity lemma on SU(3): pullback vacuum. |
| 18 | `theta_bijective` | Measure / positivity lemma on SU(3): theta bijective. |
| 19 | `theta_injective` | Measure / positivity lemma on SU(3): theta injective. |
| 20 | `theta_surjective` | Measure / positivity lemma on SU(3): theta surjective. |
| 21 | `theta_theta_eq` | Measure / positivity lemma on SU(3): theta theta eq. |
| 22 | `vacuumFunction_apply` | Measure / positivity lemma on SU(3): vacuumFunction apply. |

### Module: `Towers.YM.PeterWeylHeat`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `Heat_kernel_envelope_real_ge_one_of_pos` | Heat kernel envelope H(t) ≥ 1 for t > 0 (stand-in: exp(1/t) ≥ 1). |
| 2 | `Heat_kernel_envelope_real_ge_truncation` | Peter–Weyl / Varadhan heat-kernel lemma: Heat kernel envelope real ge truncation. |
| 3 | `Heat_kernel_envelope_real_nonneg` | Peter–Weyl / Varadhan heat-kernel lemma: Heat kernel envelope real nonneg. |
| 4 | `Weyl_sum_explicit_SU3_real_le_Heat_kernel_envelope_real` | Peter–Weyl / Varadhan heat-kernel lemma: Weyl sum explicit SU3 real le Heat kernel envelope real. |

### Module: `Towers.YM.PeterWeylHeatVaradhan`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `Heat_kernel_envelope_real_antitone` | Heat kernel envelope is antitone in t > 0 (exp(1/t) decreasing). |
| 2 | `Heat_kernel_envelope_real_ge_one_of_pos` | Heat kernel envelope H(t) ≥ 1 for t > 0 (stand-in: exp(1/t) ≥ 1). |
| 3 | `Heat_kernel_envelope_real_le_varadhan` | H(t) ≤ C·e^{-c/t} on [t_lo, t_top] (stand-in envelope bound). |
| 4 | `Heat_kernel_envelope_real_le_varadhan` | H(t) ≤ C·e^{-c/t} on [t_lo, t_top] (stand-in envelope bound). |
| 5 | `varadhan_C_pos` | Varadhan amplitude constant C > 0 (positivity certificate). |

### Module: `Towers.YM.PeterWeylQuadratic`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `PeterWeyl_Summable_SU3_half_cubic` | Peter–Weyl / Varadhan heat-kernel lemma: PeterWeyl Summable SU3 half cubic. |
| 2 | `PeterWeyl_Summable_SU3_quadratic` | Peter–Weyl / Varadhan heat-kernel lemma: PeterWeyl Summable SU3 quadratic. |
| 3 | `Weyl_dim_SU3_explicit_real_le_cubic` | Peter–Weyl / Varadhan heat-kernel lemma: Weyl dim SU3 explicit real le cubic. |
| 4 | `Weyl_dim_SU3_explicit_real_le_half_cubic` | Peter–Weyl / Varadhan heat-kernel lemma: Weyl dim SU3 explicit real le half cubic. |
| 5 | `Weyl_dim_SU3_explicit_real_le_half_prod` | Peter–Weyl / Varadhan heat-kernel lemma: Weyl dim SU3 explicit real le half prod. |
| 6 | `summable_poly6_succ_exp_neg_real` | Peter–Weyl / Varadhan heat-kernel lemma: summable poly6 succ exp neg real. |

### Module: `Towers.YM.PeterWeyl`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `Casimir_SU3_explicit_real_ge_linear` | Peter–Weyl / Varadhan heat-kernel lemma: Casimir SU3 explicit real ge linear. |
| 2 | `PeterWeyl_Summable_SU3` | Peter–Weyl / Varadhan heat-kernel lemma: PeterWeyl Summable SU3. |
| 3 | `Weyl_dim_SU3_explicit_real_le_poly` | Peter–Weyl / Varadhan heat-kernel lemma: Weyl dim SU3 explicit real le poly. |
| 4 | `summable_poly_succ_exp_neg_real` | Peter–Weyl / Varadhan heat-kernel lemma: summable poly succ exp neg real. |

### Module: `Towers.YM.PlaquetteAction`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `YMHamiltonianWilson_vacuum_eq_zero` | Yang–Mills lemma: YMHamiltonianWilson vacuum eq zero. |
| 2 | `wilsonPlaquette_def` | Yang–Mills lemma: wilsonPlaquette def. |
| 3 | `wilsonPlaquette_one` | Yang–Mills lemma: wilsonPlaquette one. |

### Module: `Towers.YM.PolymerModel`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `polymerWeightReal_empty` | Transfer-operator / polymer-activity lemma: polymerWeightReal empty. |

### Module: `Towers.YM.RealCurvature`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `YMEnergy_nonneg` | Yang–Mills lemma: YMEnergy nonneg. |
| 2 | `curvature_eq_zero` | Yang–Mills lemma: curvature eq zero. |
| 3 | `lattice_deriv_id` | Yang–Mills lemma: lattice deriv id. |
| 4 | `lie_bracket_eq_zero` | Yang–Mills lemma: lie bracket eq zero. |
| 5 | `structure_constants_su3_eq_zero` | Yang–Mills lemma: structure constants su3 eq zero. |

### Module: `Towers.YM.RealCurvatureV2`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `YMEnergy_nonneg` | Yang–Mills lemma: YMEnergy nonneg. |
| 2 | `curvature_su3_def` | Yang–Mills lemma: curvature su3 def. |
| 3 | `lattice_deriv_forward_diff` | Yang–Mills lemma: lattice deriv forward diff. |
| 4 | `lie_bracket_su3_def` | Yang–Mills lemma: lie bracket su3 def. |
| 5 | `structure_constants_su3_def` | Yang–Mills lemma: structure constants su3 def. |

### Module: `Towers.YM.ReflectionPositivityCore`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `reflection_involutive` | Measure / positivity lemma on SU(3): reflection involutive. |
| 2 | `reflection_pos_one` | Measure / positivity lemma on SU(3): reflection pos one. |

### Module: `Towers.YM.ReflectionPositivityMeasure`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `reflectionPos_diracEvalLM` | Measure / positivity lemma on SU(3): reflectionPos diracEvalLM. |

### Module: `Towers.YM.RiemannianGeometry`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `cWit_ne_one` | YM wall lemma: cWit ne one. |
| 2 | `d_SU3_eq_chordal_id` | YM wall lemma: d SU3 eq chordal id. |
| 3 | `d_SU3_geodesic_eq_d_SU3_diag` | YM wall lemma: d SU3 geodesic eq d SU3 diag. |
| 4 | `d_SU3_geodesic_le_of_mem` | YM wall lemma: d SU3 geodesic le of mem. |
| 5 | `d_SU3_geodesic_nonneg` | YM wall lemma: d SU3 geodesic nonneg. |
| 6 | `d_SU3_geodesic_self` | YM wall lemma: d SU3 geodesic self. |
| 7 | `d_SU3_geodesic_symm` | YM wall lemma: d SU3 geodesic symm. |
| 8 | `d_SU3_isBiInvariant` | YM wall lemma: d SU3 isBiInvariant. |
| 9 | `d_SU3_isMetric` | YM wall lemma: d SU3 isMetric. |
| 10 | `d_SU3_isPseudoDist` | YM wall lemma: d SU3 isPseudoDist. |
| 11 | `d_SU3_le_geodesic_of_contracts` | YM wall lemma: d SU3 le geodesic of contracts. |
| 12 | `d_SU3_nonneg` | YM wall lemma: d SU3 nonneg. |
| 13 | `d_SU3_self` | YM wall lemma: d SU3 self. |
| 14 | `not_IsMetricOnSU3_const_zero` | YM wall lemma: not IsMetricOnSU3 const zero. |

### Module: `Towers.YM.S4Numerics`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `c_S4_lt` | Yang–Mills lemma: c S4 lt. |
| 2 | `h4Order_factor` | Yang–Mills lemma: h4Order factor. |
| 3 | `kEff_le` | Yang–Mills lemma: kEff le. |
| 4 | `zModes_eq` | Yang–Mills lemma: zModes eq. |

### Module: `Towers.YM.ShiftOperator`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `norm_shift_apply` | Yang–Mills lemma: norm shift apply. |

### Module: `Towers.YM.SpectralBound`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `spectral_bound` | Spectral schema or combinator: spectral bound. |

### Module: `Towers.YM.SpectralGap`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `Perron_Frobenius_statement` | Spectral schema or combinator: Perron Frobenius statement. |
| 2 | `mass_gap_def` | Spectral schema or combinator: mass gap def. |
| 3 | `mass_gap_nonneg` | Spectral schema or combinator: mass gap nonneg. |
| 4 | `spectral_radius_def` | Spectral schema or combinator: spectral radius def. |
| 5 | `spectral_radius_nonneg` | Spectral schema or combinator: spectral radius nonneg. |

### Module: `Towers.YM.Spectrum`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `Correlation_length_from_coercive` | Yang–Mills lemma: Correlation length from coercive. |
| 2 | `Exponential_clustering_schema` | Yang–Mills lemma: Exponential clustering schema. |
| 3 | `MassGap_YM4_Clay` | Yang–Mills lemma: MassGap YM4 Clay. |
| 4 | `MassGap_YM4_Clay_conditional` | Yang–Mills lemma: MassGap YM4 Clay conditional. |
| 5 | `MassGap_YM4_proven` | Yang–Mills lemma: MassGap YM4 proven. |
| 6 | `MassGap_v2_monotone` | Yang–Mills lemma: MassGap v2 monotone. |
| 7 | `MassGap_v2_zero_iff` | Yang–Mills lemma: MassGap v2 zero iff. |
| 8 | `OS0_temperedness_from_coercive` | Yang–Mills lemma: OS0 temperedness from coercive. |
| 9 | `OS1_euclidean_invariance_schema` | Yang–Mills lemma: OS1 euclidean invariance schema. |
| 10 | `OS_reconstruction_from_H` | Yang–Mills lemma: OS reconstruction from H. |
| 11 | `OsterwalderSchrader_axioms_schema` | Yang–Mills lemma: OsterwalderSchrader axioms schema. |
| 12 | `Perron_Frobenius_assumption_schema` | Yang–Mills lemma: Perron Frobenius assumption schema. |
| 13 | `Wightman_functions_from_OS_schema` | Yang–Mills lemma: Wightman functions from OS schema. |
| 14 | `YMHamiltonian_attains_inf` | Yang–Mills lemma: YMHamiltonian attains inf. |
| 15 | `YMHamiltonian_coercive` | Yang–Mills lemma: YMHamiltonian coercive. |
| 16 | `YMHamiltonian_essentially_selfadjoint_schema` | Yang–Mills lemma: YMHamiltonian essentially selfadjoint schema. |
| 17 | `YMHamiltonian_gap_above_vacuum_schema` | Yang–Mills lemma: YMHamiltonian gap above vacuum schema. |
| 18 | `YMHamiltonian_image_bounded` | Yang–Mills lemma: YMHamiltonian image bounded. |
| 19 | `YMHamiltonian_image_has_inf` | Yang–Mills lemma: YMHamiltonian image has inf. |
| 20 | `YMHamiltonian_image_nonzero` | Yang–Mills lemma: YMHamiltonian image nonzero. |
| 21 | `YMHamiltonian_inf_eq_twelve` | Yang–Mills lemma: YMHamiltonian inf eq twelve. |
| 22 | `YMHamiltonian_selfadjoint` | Yang–Mills lemma: YMHamiltonian selfadjoint. |
| 23 | `YMHamiltonian_selfadjoint_proven` | Yang–Mills lemma: YMHamiltonian selfadjoint proven. |
| 24 | `YMHamiltonian_vacuum_def` | Yang–Mills lemma: YMHamiltonian vacuum def. |
| 25 | `cluster_decomposition_implies_gap` | Yang–Mills lemma: cluster decomposition implies gap. |
| 26 | `cluster_decomposition_proven` | Yang–Mills lemma: cluster decomposition proven. |
| 27 | `cluster_decomposition_schema` | Yang–Mills lemma: cluster decomposition schema. |
| 28 | `cluster_implies_mass_gap_schema` | Yang–Mills lemma: cluster implies mass gap schema. |
| 29 | `clustering_for_YM3` | Yang–Mills lemma: clustering for YM3. |
| 30 | `clustering_for_YM3_lemma` | Yang–Mills lemma: clustering for YM3 lemma. |
| 31 | `clustering_property_YM3` | Yang–Mills lemma: clustering property YM3. |
| 32 | `correlation_decay_conditional` | Yang–Mills lemma: correlation decay conditional. |
| 33 | `correlation_decay_exponential` | Yang–Mills lemma: correlation decay exponential. |
| 34 | `correlation_decay_from_gap` | Yang–Mills lemma: correlation decay from gap. |
| 35 | `infrared_regularization` | Yang–Mills lemma: infrared regularization. |
| 36 | `reflection_positivity_check` | Yang–Mills lemma: reflection positivity check. |
| 37 | `spectral_gap_from_clustering` | Yang–Mills lemma: spectral gap from clustering. |
| 38 | `spectral_radius_transfer` | Yang–Mills lemma: spectral radius transfer. |
| 39 | `spectrum_gap_schema` | Yang–Mills lemma: spectrum gap schema. |
| 40 | `transfer_matrix_definition_schema` | Yang–Mills lemma: transfer matrix definition schema. |
| 41 | `transfer_matrix_norm_less_one` | Yang–Mills lemma: transfer matrix norm less one. |
| 42 | `vacuum_expectation_bounded` | Yang–Mills lemma: vacuum expectation bounded. |
| 43 | `vacuum_gap_lower_bound` | Yang–Mills lemma: vacuum gap lower bound. |
| 44 | `vacuum_gap_positive_schema` | Yang–Mills lemma: vacuum gap positive schema. |
| 45 | `vacuum_gap_positive_theorem` | Yang–Mills lemma: vacuum gap positive theorem. |

### Module: `Towers.YM.SU3Basis`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `gellMann₁_mem` | SU(3) heat-trace / Tauberian lemma: gellMann₁ mem. |
| 2 | `gellMann₂_mem` | SU(3) heat-trace / Tauberian lemma: gellMann₂ mem. |
| 3 | `gellMann₃_mem` | SU(3) heat-trace / Tauberian lemma: gellMann₃ mem. |
| 4 | `gellMann₄_mem` | SU(3) heat-trace / Tauberian lemma: gellMann₄ mem. |
| 5 | `gellMann₅_mem` | SU(3) heat-trace / Tauberian lemma: gellMann₅ mem. |
| 6 | `gellMann₆_mem` | SU(3) heat-trace / Tauberian lemma: gellMann₆ mem. |
| 7 | `gellMann₇_mem` | SU(3) heat-trace / Tauberian lemma: gellMann₇ mem. |
| 8 | `gellMann₈_mem` | SU(3) heat-trace / Tauberian lemma: gellMann₈ mem. |
| 9 | `inner_su3` | SU(3) heat-trace / Tauberian lemma: inner su3. |
| 10 | `inner_su3_add_left` | SU(3) heat-trace / Tauberian lemma: inner su3 add left. |
| 11 | `inner_su3_conj_symm` | SU(3) heat-trace / Tauberian lemma: inner su3 conj symm. |
| 12 | `inner_su3_smul_left` | SU(3) heat-trace / Tauberian lemma: inner su3 smul left. |
| 13 | `instance_inner_product_space_su3_core` | SU(3) heat-trace / Tauberian lemma: instance inner product space su3 core. |
| 14 | `norm_su3` | SU(3) heat-trace / Tauberian lemma: norm su3. |
| 15 | `su3_basis_def` | SU(3) heat-trace / Tauberian lemma: su3 basis def. |
| 16 | `su3_basis_linearIndependent` | SU(3) heat-trace / Tauberian lemma: su3 basis linearIndependent. |
| 17 | `su3_basis_spans` | SU(3) heat-trace / Tauberian lemma: su3 basis spans. |
| 18 | `su3_equiv_fin8_def` | SU(3) heat-trace / Tauberian lemma: su3 equiv fin8 def. |

### Module: `Towers.YM.SU3.Tauberian`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `dim_sq_le_casimir_cubed` | SU(3) heat-trace / Tauberian lemma: dim sq le casimir cubed. |
| 2 | `summable_heat_trace` | SU(3) heat-trace / Tauberian lemma: summable heat trace. |

### Module: `Towers.YM.SU3`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `instance_addcommgroup_su3` | Typeclass instance: AddCommGroup ↥su3_submodule (inherited from Submodule). |
| 2 | `instance_module_real_su3` | Typeclass instance: Module ℝ ↥su3_submodule (ℝ-module structure on su(3)). |
| 3 | `su3_add_mem` | su(3) is closed under addition: A,B ∈ su(3) → A+B ∈ su(3). |
| 4 | `su3_lie_algebra_def` | Definition of su(3) as the set of 3×3 anti-Hermitian traceless ℂ-matrices. |
| 5 | `su3_mem_iff_anti_hermitian_traceless` | A ∈ su(3) ↔ A† = -A ∧ tr(A) = 0 (membership characterization). |
| 6 | `su3_neg_mem` | su(3) is closed under negation: A ∈ su(3) → -A ∈ su(3). |
| 7 | `su3_smul_mem` | su(3) is closed under ℝ-scaling: A ∈ su(3), r:ℝ → r•A ∈ su(3). |
| 8 | `su3_sub_mem` | su(3) is closed under subtraction: A,B ∈ su(3) → A-B ∈ su(3). |
| 9 | `su3_submodule` | su(3) as a real Submodule ℝ of Mat(3,ℂ) (bundled closure lemmas). |
| 10 | `su3_submodule_mem_iff` | Carrier unpacker: x ∈ su3_submodule ↔ x ∈ su3 (definitional unfold). |
| 11 | `su3_zero_mem` | 0 ∈ su(3) (zero matrix is anti-Hermitian and traceless). |

### Module: `Towers.YM.TemperednessCore`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `tempered_of_clm` | Yang–Mills lemma: tempered of clm. |

### Module: `Towers.YM.TransferOperator`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `TransferOperator_vacuum_eq_id` | Transfer-operator / polymer-activity lemma: TransferOperator vacuum eq id. |
| 2 | `boltzmannWeight_const_one` | Transfer-operator / polymer-activity lemma: boltzmannWeight const one. |
| 3 | `boltzmannWeight_pos` | Transfer-operator / polymer-activity lemma: boltzmannWeight pos. |

### Module: `Towers.YM.Transfer`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `Perron_Frobenius_for_transfer` | Transfer-operator / polymer-activity lemma: Perron Frobenius for transfer. |
| 2 | `correlation_decay_from_T` | Transfer-operator / polymer-activity lemma: correlation decay from T. |
| 3 | `transfer_matrix_compact` | Transfer-operator / polymer-activity lemma: transfer matrix compact. |
| 4 | `transfer_matrix_selfadjoint` | Transfer-operator / polymer-activity lemma: transfer matrix selfadjoint. |

### Module: `Towers.YM.VaradhanStripWidened`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `Heat_kernel_envelope_real_le_varadhan_geometric_widened_upper` | Geometric upper bound for the widened Varadhan envelope on [1/200,200]. |
| 2 | `Heat_kernel_envelope_real_le_varadhan_widened` | H(t) ≤ C_widened·e^{-c/t} on [1/200, 200] (widened strip). |
| 3 | `Heat_kernel_envelope_real_le_varadhan_widened_upper` | Upper amplitude bound on the widened-strip Varadhan constant. |
| 4 | `varadhan_t_lo_widened_lt` | Widened strip lower bound: t_lo_widened < t_top_widened. |
| 5 | `varadhan_t_top_lt_widened` | Widened strip upper bound: t_top < t_top_widened. |

### Module: `Towers.YM.W1_One_Seventh_Proof`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `w1_seven_lt` | SU(3) heat-trace / Tauberian lemma: w1 seven lt. |
| 2 | `w1_seven_pos` | SU(3) heat-trace / Tauberian lemma: w1 seven pos. |

### Module: `Towers.YM.Wall251b_H4`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `su2_plaquetteEnergy_nonneg` | YM wall lemma: su2 plaquetteEnergy nonneg. |
| 2 | `su2_plaquetteEnergy_pos_iff` | YM wall lemma: su2 plaquetteEnergy pos iff. |
| 3 | `su2_star_mul_self` | YM wall lemma: su2 star mul self. |
| 4 | `su2_traceRe_eq_two_iff` | YM wall lemma: su2 traceRe eq two iff. |
| 5 | `su2_traceRe_le_two` | YM wall lemma: su2 traceRe le two. |
| 6 | `su2_wilson_hs_identity` | YM wall lemma: su2 wilson hs identity. |

### Module: `Towers.YM.Wall252_KP`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `kpModeWeight_lt` | YM wall lemma: kpModeWeight lt. |
| 2 | `kpModeWeight_nonneg` | YM wall lemma: kpModeWeight nonneg. |
| 3 | `kp_sum_lt_half` | YM wall lemma: kp sum lt half. |

### Module: `Towers.YM.Wall253_KP_Cluster`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `kp_cluster_criterion` | Transfer-operator / polymer-activity lemma: kp cluster criterion. |
| 2 | `kp_cluster_sum_lt_two` | Transfer-operator / polymer-activity lemma: kp cluster sum lt two. |
| 3 | `kp_cluster_summable` | Transfer-operator / polymer-activity lemma: kp cluster summable. |
| 4 | `kp_sum_lt_one` | Transfer-operator / polymer-activity lemma: kp sum lt one. |
| 5 | `kp_sum_nonneg` | Transfer-operator / polymer-activity lemma: kp sum nonneg. |

### Module: `Towers.YM.Wall254_OS_Positivity`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `gram_form_eq` | Measure / positivity lemma on SU(3): gram form eq. |
| 2 | `gram_re_nonneg` | Measure / positivity lemma on SU(3): gram re nonneg. |
| 3 | `os2_diagonal_nonneg` | Measure / positivity lemma on SU(3): os2 diagonal nonneg. |
| 4 | `os2_of_gram_realization` | Measure / positivity lemma on SU(3): os2 of gram realization. |

### Module: `Towers.YM.Wall255_JensenObstruction`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `e_bar_le_two` | YM wall lemma: e bar le two. |
| 2 | `e_bar_pos_of_meanEnergy_pos` | YM wall lemma: e bar pos of meanEnergy pos. |
| 3 | `inv8_pow_eq_exp_neg` | YM wall lemma: inv8 pow eq exp neg. |
| 4 | `jensen_obstruction` | YM wall lemma: jensen obstruction. |
| 5 | `meanEnergy_le_two_card` | YM wall lemma: meanEnergy le two card. |
| 6 | `meanEnergy_nonneg` | YM wall lemma: meanEnergy nonneg. |
| 7 | `mean_threshold_fails` | YM wall lemma: mean threshold fails. |
| 8 | `plaquetteEnergy_le_two` | YM wall lemma: plaquetteEnergy le two. |
| 9 | `polymerEnergy_le_two_card` | YM wall lemma: polymerEnergy le two card. |

### Module: `Towers.YM.Wall255_KP_Entropy`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `entropy_geometric_summable` | YM wall lemma: entropy geometric summable. |
| 2 | `entropy_geometric_tsum` | YM wall lemma: entropy geometric tsum. |
| 3 | `kp_entropy_weighted_summable` | YM wall lemma: kp entropy weighted summable. |
| 4 | `kp_polymer_entropy_weighted_summable` | YM wall lemma: kp polymer entropy weighted summable. |
| 5 | `seven_half_not_lt_one` | YM wall lemma: seven half not lt one. |
| 6 | `seven_q_lt_one_of_lt_inv_seven` | YM wall lemma: seven q lt one of lt inv seven. |

### Module: `Towers.YM.Wall256_MassGapConditional`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `mass_gap_pos_of_spectral_gap` | YM wall lemma: mass gap pos of spectral gap. |
| 2 | `neg_log_pos_of_lt_one` | YM wall lemma: neg log pos of lt one. |
| 3 | `rpow_eq_exp_neg_rate` | YM wall lemma: rpow eq exp neg rate. |

### Module: `Towers.YM.Wall256_Note`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `kp_summable_of_truncatedActivity` | YM wall lemma: kp summable of truncatedActivity. |
| 2 | `su2_gap_of_truncatedActivity` | YM wall lemma: su2 gap of truncatedActivity. |

### Module: `Towers.YM.Wall256_RateFunction`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `entropy_threshold_eq` | YM wall lemma: entropy threshold eq. |
| 2 | `exp_neg_lt_inv_seven_iff` | YM wall lemma: exp neg lt inv seven iff. |
| 3 | `kp_polymer_rate_summable` | YM wall lemma: kp polymer rate summable. |
| 4 | `kp_rate_summable` | YM wall lemma: kp rate summable. |
| 5 | `le_rateFn` | YM wall lemma: le rateFn. |
| 6 | `log_seven_pos` | YM wall lemma: log seven pos. |
| 7 | `mean_rate_fails_criterion` | YM wall lemma: mean rate fails criterion. |
| 8 | `rate_beats_entropy` | YM wall lemma: rate beats entropy. |
| 9 | `rate_tsum` | YM wall lemma: rate tsum. |
| 10 | `seven_exp_neg_lt_one_iff` | YM wall lemma: seven exp neg lt one iff. |

### Module: `Towers.YM.Wall257_RateLowerBound`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `I_E_unbounded` | YM wall lemma: I E unbounded. |
| 2 | `bddAbove_slopes` | YM wall lemma: bddAbove slopes. |
| 3 | `exists_rate_gt_log_seven` | YM wall lemma: exists rate gt log seven. |
| 4 | `quarter_sq_le_I_E` | YM wall lemma: quarter sq le I E. |
| 5 | `rate_gap_single_site_vs_polymer` | YM wall lemma: rate gap single site vs polymer. |

### Module: `Towers.YM.Wall257_StrongCoupling`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `exp_neg_mul_le_inv8_pow` | YM wall lemma: exp neg mul le inv8 pow. |
| 2 | `inv8_pow_eq_exp_neg` | YM wall lemma: inv8 pow eq exp neg. |
| 3 | `inv8_pow_le_inv7_pow` | YM wall lemma: inv8 pow le inv7 pow. |
| 4 | `polymerActivity_le_inv7_of_energy_lb` | YM wall lemma: polymerActivity le inv7 of energy lb. |
| 5 | `polymerActivity_le_inv8_of_energy_lb` | YM wall lemma: polymerActivity le inv8 of energy lb. |
| 6 | `polymerEnergy_vacuum_eq_zero` | YM wall lemma: polymerEnergy vacuum eq zero. |
| 7 | `vacuum_breaks_energy_lb` | YM wall lemma: vacuum breaks energy lb. |

### Module: `Towers.YM.Wall258_DependenceDefect`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `dependence_defect_kp_summable` | YM wall lemma: dependence defect kp summable. |
| 2 | `dependence_defect_kp_summable_Z4` | YM wall lemma: dependence defect kp summable Z4. |
| 3 | `linkIncidence_four` | YM wall lemma: linkIncidence four. |
| 4 | `rate_clears_after_defect` | YM wall lemma: rate clears after defect. |
| 5 | `threshold_mono` | YM wall lemma: threshold mono. |

### Module: `Towers.YM.Wall259_DependenceBound`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `defect_eq` | YM wall lemma: defect eq. |
| 2 | `dependence_bound_kp_summable` | YM wall lemma: dependence bound kp summable. |
| 3 | `polymerRate_eq` | YM wall lemma: polymerRate eq. |
| 4 | `polymer_criterion_of_single_site` | YM wall lemma: polymer criterion of single site. |
| 5 | `polymer_criterion_of_threshold` | YM wall lemma: polymer criterion of threshold. |

### Module: `Towers.YM.Wall260_ClayReduction`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `link_incidence_number_4d` | YM wall lemma: link incidence number 4d. |
| 2 | `new_clay_reduction` | YM wall lemma: new clay reduction. |
| 3 | `new_clay_reduction_Z4` | YM wall lemma: new clay reduction Z4. |
| 4 | `threshold_split` | YM wall lemma: threshold split. |

### Module: `Towers.YM.Wall261_H4Defect`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `graph_gap_pos` | YM wall lemma: graph gap pos. |
| 2 | `h4_clay_reduction` | YM wall lemma: h4 clay reduction. |
| 3 | `h4_defect_beats_z4` | YM wall lemma: h4 defect beats z4. |
| 4 | `h4_threshold_lt_z4` | YM wall lemma: h4 threshold lt z4. |
| 5 | `one_add_phi_lt_six` | YM wall lemma: one add phi lt six. |
| 6 | `phi_sq_eq` | YM wall lemma: phi sq eq. |

### Module: `Towers.YM.Wall262a_RatioModel`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `Hweight_nonneg` | YM wall lemma: Hweight nonneg. |
| 2 | `Hweight_values` | YM wall lemma: Hweight values. |
| 3 | `R_le` | YM wall lemma: R le. |
| 4 | `R_le_one_sub_half` | YM wall lemma: R le one sub half. |
| 5 | `exp_neg88_lower` | YM wall lemma: exp neg88 lower. |
| 6 | `factorial_smooth` | YM wall lemma: factorial smooth. |
| 7 | `seven_enters_at_seven` | YM wall lemma: seven enters at seven. |
| 8 | `term_nonneg` | YM wall lemma: term nonneg. |
| 9 | `threshold_factorization` | YM wall lemma: threshold factorization. |

### Module: `Towers.YM.Wall262_ConnectiveRatio`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `defect_bound_arith` | YM wall lemma: defect bound arith. |
| 2 | `defect_lt` | YM wall lemma: defect lt. |
| 3 | `exp_lower` | YM wall lemma: exp lower. |
| 4 | `phi_lt` | YM wall lemma: phi lt. |
| 5 | `su2_wins` | YM wall lemma: su2 wins. |
| 6 | `threshold_factorization` | YM wall lemma: threshold factorization. |

### Module: `Towers.YM.Wall263_CoxeterSpectral`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `coxeterCharpoly_phi` | Spectral schema or combinator: coxeterCharpoly phi. |
| 2 | `defect_bound_H4` | Spectral schema or combinator: defect bound H4. |
| 3 | `one_lt_phi` | Spectral schema or combinator: one lt phi. |
| 4 | `phi_lt_two` | Spectral schema or combinator: phi lt two. |
| 5 | `phi_not_root` | Spectral schema or combinator: phi not root. |

### Module: `Towers.YM.WeylDim`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `dim_cubic_bound` | Yang–Mills lemma: dim cubic bound. |

### Module: `Towers.YM.WilsonAction`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `plaquetteEnergy_const_one` | Yang–Mills lemma: plaquetteEnergy const one. |
| 2 | `wilsonAction_const_one_eq_zero` | Yang–Mills lemma: wilsonAction const one eq zero. |
| 3 | `wilsonAction_zero_beta` | Yang–Mills lemma: wilsonAction zero beta. |
| 4 | `wilsonPlaquette_const_one` | Yang–Mills lemma: wilsonPlaquette const one. |

### Module: `Towers.YM.WilsonPositivitySU2`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `hsNormSq2_eq_zero_iff` | Measure / positivity lemma on SU(3): hsNormSq2 eq zero iff. |
| 2 | `hsNormSq2_sub_one_eq` | Measure / positivity lemma on SU(3): hsNormSq2 sub one eq. |
| 3 | `plaquetteEnergy2_nonneg` | Measure / positivity lemma on SU(3): plaquetteEnergy2 nonneg. |
| 4 | `plaquetteEnergy2_pos_iff` | Measure / positivity lemma on SU(3): plaquetteEnergy2 pos iff. |
| 5 | `traceRe_eq_two_iff` | Re(tr(U)) ≤ 3 for any U ∈ SU(3) (trace inequality). |
| 6 | `traceRe_le_two` | Re(tr(U)) ≤ 3 for any U ∈ SU(3) (trace inequality). |

### Module: `Towers.YM.WilsonPositivity`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `hsNormSq_eq_zero_iff` | Measure / positivity lemma on SU(3): hsNormSq eq zero iff. |
| 2 | `plaquetteEnergy_nonneg` | Measure / positivity lemma on SU(3): plaquetteEnergy nonneg. |
| 3 | `plaquetteEnergy_pos_iff` | Measure / positivity lemma on SU(3): plaquetteEnergy pos iff. |
| 4 | `traceRe_eq_three_iff` | Re(tr(U)) ≤ 3 for any U ∈ SU(3) (trace inequality). |
| 5 | `traceRe_le_three` | Re(tr(U)) ≤ 3 for any U ∈ SU(3) (trace inequality). |
| 6 | `wilsonAction_pos_of_nontrivial` | Wilson action of the trivial configuration (all plaquettes = 1) is zero. |
| 7 | `wilsonPlaquette_star_mul_self` | Plaquette star-product identity: P† · P = I. |

### Module: `Towers.YM.Wilson`

| # | Theorem | Mathematical Content |
|---|---------|---------------------|
| 1 | `WilsonAction_nonneg` | Wilson action W(U) ≥ 0 for all gauge configurations U. |
| 2 | `WilsonAction_trivial_eq_zero` | Wilson action of the trivial configuration (all plaquettes = 1) is zero. |
| 3 | `YMHamiltonian_real_nonneg` | Real YM Hamiltonian H_real(U) ≥ 0 for all gauge fields U. |
| 4 | `YMHamiltonian_real_trivial_eq_zero` | Real YM Hamiltonian at the trivial configuration equals 0. |
| 5 | `plaquetteMat_trivial` | Trivial plaquette (identity) evaluates correctly. |
| 6 | `wDensity_nonneg` | Wilson density w(U) ≥ 0 pointwise. |
| 7 | `wDensity_trivial_eq_zero` | Wilson density at the trivial configuration is 0. |
