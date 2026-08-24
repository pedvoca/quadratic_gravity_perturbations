# Quadratic-gravity cosmological perturbations

Wolfram Language notebooks for deriving the linear scalar perturbation equations of quadratic gravity about a spatially flat FLRW background.  The calculation uses the Stelle action

\[
$\mathcal{L}=R+\alpha R^2+\beta W_{\mu\nu\rho\sigma}W^{\mu\nu\rho\sigma}$,
\]

and follows the longitudinal-gauge dust system through its sub-horizon, quasi-static Fourier-space reduction.

## Repository contents

| Notebook | Role |
| --- | --- |
| `notebooks/QuadraticGravity_PerturbedFLRW.nb` | **Primary notebook.** Consolidates the field-equation variation, flat-FLRW setup, dust stress tensor and conservation equations, xPand linearization, and the late-time Fourier/slip/growth reduction. |
| `notebooks/RW_perturbed_QG.nb` | Original xAct/xPert/xPand derivation retained as a source calculation. |
| `notebooks/perturbedFLRWxpandnotebook.nb` | Original xPand perturbed-FLRW calculation retained as a source calculation. |

The primary notebook is self-contained and does not programmatically import either source notebook.  The two source notebooks are versioned so that the derivation history is preserved.

## Requirements

- Wolfram Mathematica / Wolfram Desktop (the consolidated notebook was created with Mathematica 15.0)
- The [xAct](http://xact.es/) suite, including `xTensor`, `xPert`, and `xPand`

xAct registrations persist within a Mathematica kernel.  Begin from a fresh kernel and evaluate the primary notebook from top to bottom.  Its initialization cell contains a macOS/Apple-Silicon compatibility path for xAct; change `xActApplicationsDirectory` if your installation lives elsewhere.

## Reproducing the reduction

1. Open `notebooks/QuadraticGravity_PerturbedFLRW.nb`.
2. Start a fresh kernel, then evaluate all cells in order.
3. Follow the final **Conformally-flat, sub-horizon and Fourier reduction** section.  It extracts the normal-normal and traceless spatial scalar equations and obtains:
   - the gravitational slip \(Q(k,a)=\Phi/\Psi\),
   - the modified Poisson factor \(f_Q(k,a)\), and
   - the quasi-static dust-growth equation
     \[
     \ddot\delta+2H\dot\delta+f_Q(k,a)\,\bar\rho_m\delta\simeq0.
     \]

The notebooks contain saved outputs from prior evaluations.  They are useful for inspection, but a fresh evaluation is the authoritative reproducibility check.

## Scope

This repository intentionally tracks the notebooks and their documentation only.  Manuscript sources, slide decks, PDFs, kernel caches, and Wolfram temporary files are excluded so the derivation history remains compact and reviewable.
