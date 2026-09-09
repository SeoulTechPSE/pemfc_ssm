# Steady-State Multiplicity and Stability of a Two-Dimensional Two-Phase PEMFC Cathode Model 

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
