# Binomial Tree vs. Black-Scholes Option Pricing

This project compares the pricing of a **European call option** using:
- A **Cox-Ross-Rubinstein (CRR)** calibrated **binomial tree** (with `O(N)` time complexity)
- The **Black-Scholes closed-form formula**

It also benchmarks **convergence, runtime, and delta stability** as the number of binomial tree steps increases.

---

## Key Features

- Implements the Black-Scholes pricing formula for European call options
- Implements a binomial tree pricer with dynamic CRR calibration:
  \[
  u = e^{\sigma \sqrt{\Delta t}}, \quad d = \frac{1}{u}
  \]
- Computes both:
  - Option **price**
  - Option **delta** (hedge ratio) at the root
- Tracks runtime performance per iteration count
- Produces convergence plots for:
  - Price vs. steps
  - Delta vs. steps
  - Runtime vs. steps

---

## Dependencies

- `numpy`
- `scipy`
- `pandas`
- `matplotlib`

Install with:

```bash
pip install numpy scipy pandas matplotlib
