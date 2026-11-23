# Tema 7: Bayesian inference with PyMC

All the code is in `Tema7_PMP.ipynb`, one section per exercise. Run it top to bottom.
Each `Exercitiul` folder has the plots for that exercise and a README with the results and what they mean.

| Exercise | Chains | Draws per chain | Tuning steps | Sampler |
|---|---|---|---|---|
| 1. Population size | 4 | 5000 | 1000 | Metropolis (N is discrete) |
| 2. Two treatments | 4 | 2000 | 1000 | NUTS |
| 3. Gradual rate change | 4 | 2000 | 2000 | NUTS, target_accept = 0.95 |

I'm on ArviZ 1.x, where `az.plot_posterior` no longer exists, so the plots are made with matplotlib and the HDIs come from `az.hdi` / `az.summary(..., ci_kind="hdi", ci_prob=0.95)`.
