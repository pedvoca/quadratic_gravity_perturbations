# Quadratic-gravity FLRW perturbations

Wolfram Language notebooks deriving the linear scalar perturbation equations of quadratic gravity about a spatially flat FLRW background. The calculation uses the Stelle action

$$
\mathcal{L}=R+\alpha R^2+\beta W_{\mu\nu\rho\sigma}W^{\mu\nu\rho\sigma},
$$

and follows longitudinal-gauge dust perturbations through the sub-horizon and quasi-static Fourier reduction.

## Repository contents

| Notebook | Role |
| --- | --- |
| `notebooks/QuadraticGravity_PerturbedFLRW.nb` | **Primary notebook.** Step-by-step derivation of the field equation, flat-FLRW perturbations, dust conservation equations, xPand linearization, and the Fourier/slip/growth reduction. |
| `notebooks/RW_perturbed_QG.nb` | Supporting xAct/xPert/xPand calculation. |
| `notebooks/perturbedFLRWxpandnotebook.nb` | Supporting xPand perturbed-FLRW calculation. |

The primary notebook is self-contained and does not programmatically import the supporting notebooks.

## Requirements

- Wolfram Mathematica / Wolfram Desktop (the consolidated notebook was created with Mathematica 15.0)
- The [xAct](http://xact.es/) suite, including `xTensor`, `xPert`, and `xPand`

xAct registrations persist within a Mathematica kernel.  Begin from a fresh kernel and evaluate the primary notebook from top to bottom.  Its initialization cell contains a macOS/Apple-Silicon compatibility path for xAct; change `xActApplicationsDirectory` if your installation lives elsewhere.

## Reproducing the reduction

1. Open `notebooks/QuadraticGravity_PerturbedFLRW.nb`.
2. Start a fresh kernel, then evaluate all cells in order.
3. Follow **Step 7: sub-horizon and quasi-static Fourier reduction**. It uses
   \(k^2/(a^2H^2)\gg1\) and applies the quasi-static limit only to the metric potentials. It extracts the normal-normal and traceless spatial scalar equations and obtains:
   - the gravitational slip $Q(k,a)=\Phi/\Psi$,
   - the modified Poisson factor $f_Q(k,a)$, and
   - the quasi-static dust-growth equation and effective Newton coupling: $\ddot{\delta}+2H\dot{\delta}-4\pi G_{\mathrm{eff}}(k,a)\,\bar{\rho}_{m}\delta\simeq0$, with $G_{\mathrm{eff}}(k,a)=-2f_Q(k,a)G$.

The notebooks contain saved outputs from prior evaluations.  They are useful for inspection, but a fresh evaluation is the authoritative reproducibility check.

## Scope

This repository tracks the notebooks and documentation only. Manuscript sources, slide decks, PDFs, kernel caches, and Wolfram temporary files are excluded so the derivation remains compact and reviewable.
