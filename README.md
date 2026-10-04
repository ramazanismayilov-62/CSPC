# CSPC - Computer Science for Physics and Chemistry
My coursework repository. Each practical is under PW<n>/Lab <X>/.

## Setup
Create the environment for a given lab:
conda env create -f PW<n>/Lab\ <X>/environment.yml
conda activate cspc

---

## PW1 - Lab A: Reproducible Foundations

**What I built:**
- Set up the CSPC repo with a conda environment, ran a radioactive decay simulation, added tests, and compared pure-Python vs NumPy speed.

**Speed comparison (loop vs NumPy):**
- loop : 2.9795 s
- numpy : 0.0003 s
- speed-up: 10372.0x faster

**Tests:** all passing? yes

**Conclusion:**
- NumPy's vectorized operations are dramatically faster than pure-Python loops for large simulations. Working through Git branching and pushing to GitHub helped me understand the basic version-control workflow.
## PW1 --- Lab B

**What the data showed:** The observed counts start at 5000 and decrease
quickly over time, approaching zero around t = 15-20, which is typical
exponential decay.

**Match with the analytical law:** Yes. The observed points follow the
analytical curve N0·exp(-λt) with λ = 0.3 very closely; the small
differences look like random measurement noise.

**Snakemake pipeline:** The Snakefile defines one rule that builds
figure.png from decay_observed.csv and plot.py, and it only reruns the
plot when one of those inputs has changed.