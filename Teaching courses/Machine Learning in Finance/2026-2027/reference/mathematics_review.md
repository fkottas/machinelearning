# Mathematics reference · Lecture 0 + Lecture 1

This page uses GitHub-compatible display-math blocks. The equations are written with `$$ ... $$` so the symbols render as mathematics instead of broken inline text. Each equation is followed by definitions and a financial interpretation.

| Slide | Topic | Equation |
|---:|---|---|
| 71 | Arithmetic mean | `$$\\bar{x}=\\frac{1}{n}\\sum_{i=1}^{n}x_i$$` |
| 72 | Median | `$$\\tilde{x}=\\begin{cases}x_{((n+1)/2)}, & n\\text{ odd},\\\\[4pt]\\dfrac{x_{(n/2)}+x_{(n/2+1)}}{2}, & n\\text{ even}.\\end{cases}$$` |
| 73 | Sample variance and standard deviation | `$$s^2=\\frac{1}{n-1}\\sum_{i=1}^{n}(x_i-\\bar{x})^2,\\qquad s=\\sqrt{s^2}$$` |
| 74 | Z-score | `$$z_i=\\frac{x_i-\\bar{x}}{s}$$` |
| 75 | Simple and log returns | `$$R_t=\\frac{P_t-P_{t-1}}{P_{t-1}},\\qquad r_t=\\ln\\left(\\frac{P_t}{P_{t-1}}\\right)$$` |
| 78 | Correlation | `$$\\operatorname{Corr}(X,Y)=\\frac{\\operatorname{Cov}(X,Y)}{s_Xs_Y}$$` |

## How to read the equations

- `x_i` is observation `i`; `n` is the number of observations.
- `P_t` is the price at time `t`; `R_t` is the simple return; `r_t` is the log return.
- `s` is the sample standard deviation, so the denominator uses `n−1` for the sample variance.
- The median requires the observations to be ordered before the middle position is selected.
- Correlation is unit-free and measures linear association; it does not establish causality.

## Financial interpretation

The mean is sensitive to extreme observations, whereas the median is more robust in a skewed financial variable. Returns convert price levels into changes that can be compared across time. Standard deviation measures sample dispersion, and correlation summarises linear co-movement between two variables. None of these descriptive statistics is a prediction or a causal estimate.

The equations on slides 71–72 are preserved in the PPTX as rendered equation graphics. The unwanted background was removed without removing the equation, and the median expression no longer contains an extra closing parenthesis.
