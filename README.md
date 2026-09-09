# Steady-State Multiplicity and Stability of a Two-Dimensional
Two-Phase PEMFC Cathode Model — notebook manifest for GitHub release

This folder gathers every notebook that Paper 1's current text (as of 2026-09-09, including
Appendix D) actually draws its reported results from. All 36 files below were already present
somewhere in `PEMFC_revision/` (root or `ParameterSensitivity_RH_tau/`) — nothing had to be
recovered from outside the Drive. Files are **copied**, not moved; originals are untouched.

## Folder → paper section map

| Folder | Paper section | Notebooks |
|---|---|---|
| `00_original_branch/` | Sec. 5.1 (original branch, primary fold) | HighEta_Stability |
| `01_second_branch_discovery/` | Sec. 5.2 + Appendix A (mesh checks specific to 2nd branch) | SecondBranch_Continuation, SecondBranch_Stability, MeshContinuation_SecondBranch, FineMesh_SecondBranch_Trace, SecondBranchDown_Retry |
| `02_third_branch_discovery/` | Sec. 5.4 + Appendix A (fine-mesh trace/retry) | ThirdBranch_Continuation, ThirdBranch_Stability, FineMesh_ThirdBranch_Trace, FineMesh_ThirdBranch_DownRetry |
| `03_perturbation_direction_checks/` | Sec. 5 (perturbation-direction validation) | MinusDirection_OrangeCheck, MinusDirection_Summary, MinusDirection_TimeSeries_Plot |
| `04_appendixA_mesh_convergence/` | Appendix A (`#sec-meshconv`) | MeshConvergence, SecondThirdBranch_MeshCheck, SecondThirdBranch_FractionSweep, SecondThirdBranch_CwProfileCheck, Coarse_EigProxyCheck, Coarse_FullEigCheck, CwTrend_coarse, CwTrend_fine_idx2plus, CwTrend_fine_idx3minus, FineMesh_FoldRetry, FineMesh_FullEigCheck_idx2plus, FineMesh_FullEigCheck_idx3minus, RowScalingRobustnessCheck |
| `05_appendixB_cusp_investigation/` | Appendix B (`#sec-cuspinvestigation`) | MeshCuspSeed, CuspMeshCheck, ArclengthContinuation, CuspCoefficients |
| `06_branch_connectivity_switching/` | Sec. 6 supporting material | SecondBranchConnectivity, BranchSwitchingPredictor |
| `07_appendixC_RH_sensitivity/` | Appendix C (`#sec-rhsensitivity`), @tbl-rhsensitivity | PEMFC_Sensitivity_rh0p5, PEMFC_Sensitivity_rh1p0 |
| `08_appendixD_tau_sensitivity/` | Appendix D (`#sec-taubrugsensitivity`), @tbl-taubrugsensitivity | PEMFC_Sensitivity_tau1p3_HighEta_TauBrugContinuation (Parts R/S/T = Original/Second-idx2/Third-idx0 direct tau-direction continuation) |
| `09_utilities/` | Fig. marker/DOF reference | DOF_Coords_nx24_ny60_Lx0.2mm |

## Things to check before publishing

1. ~~Filename mismatch (dots vs. underscores)~~ -- **fixed 2026-09-09.** The Drive copy of the
   third-branch fine-mesh down-leg retry notebook was found saved as
   `PEMFC_Tau1_1_Lx0_2mm_FineMesh_ThirdBranch_DownRetry.ipynb` (underscores), while the paper text
   (line ~1108) cites `PEMFC_Tau1.1_Lx0.2mm_FineMesh_ThirdBranch_DownRetry.ipynb` (dots), matching
   every other companion notebook's naming convention. Renamed both the Drive original and the
   copy in `02_third_branch_discovery/` to the dotted form so the filename now matches the paper's
   in-text citation exactly.

2. **`ParameterSensitivity_RH_tau/` has ~30 other notebooks not included here on purpose.** Only
   the 3 notebooks in `07_.../08_...` actually feed Appendix C/D's tables. Everything else in that
   folder (GapBridge_*, PanelC_*, TauDirection_ArclengthContinuation[_Timeboxed], XY_FoldLocate,
   HighEta_TauBrugFoldBisection, DisconnectedBranchCheck, FoldConfirm, TraceSecondBranch,
   CwCeiling_Diagnostic, TauSeedPoint_FoldDiagnostic, BistableConfirm*, ContinuePastEta1p27,
   FoldDiagnostic, LowEtaWindow_Bridge, Baseline_EtaPeak_TauContinuation_FieldEvolution, tau1p2/
   tau1p5 exploratory notebooks, etc.) is exploratory work behind the *new* multistability findings
   at higher tau_brug — deliberately kept out of Paper 1 (per the 2026-09-08/09 integration
   decision) and reserved for a future, separate paper, the same way Paper 2's mixed-direction
   8-state material was kept out of Paper 1. Do not add these to the Paper 1 repo.

## Not otherwise flagged as missing

Every notebook checked against Paper 1's current text and against the 2026-09-01 reproducibility
audit (`paper1_critique_response_plan_2026-09-01.md`, Sec. 3.1) was located. The two notebooks that
audit had flagged highest-priority-missing (`MeshConvergence.ipynb`, `SecondBranchDown_Retry.ipynb`)
are both present and included above — that gap has since been closed.
