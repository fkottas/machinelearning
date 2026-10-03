# Exact mathematics for the model lectures

Use the following equations exactly as written in LaTeX. Each slide should define the symbols immediately below the equation and then give one numerical or financial interpretation.

## Logistic regression

\[
p_i=P(Y_i=1\mid\mathbf{x}_i)=\sigma(\eta_i)=\frac{1}{1+e^{-\eta_i}},
\qquad
\eta_i=\beta_0+\mathbf{x}_i^{\top}\boldsymbol{\beta}.
\]

Here \(p_i\) is the predicted probability of default for observation \(i\), \(\mathbf{x}_i\) is the feature vector, \(\beta_0\) is the intercept, and \(\boldsymbol{\beta}\) contains the feature coefficients.

## Logistic log-likelihood and log-loss

\[
\ell(\boldsymbol{\beta})=
\sum_{i=1}^{n}\left[y_i\log(p_i)+(1-y_i)\log(1-p_i)\right].
\]

\[
\operatorname{LogLoss}=-\frac{1}{n}\sum_{i=1}^{n}\left[y_i\log(p_i)+(1-y_i)\log(1-p_i)\right].
\]

The model maximises the log-likelihood, equivalently minimises the negative average log-likelihood.

## Regularisation

\[
\min_{\beta_0,\boldsymbol{\beta}}
\left\{-\ell(\beta_0,\boldsymbol{\beta})
 +\lambda\left[\alpha\lVert\boldsymbol{\beta}\rVert_1
 +(1-\alpha)\frac{1}{2}\lVert\boldsymbol{\beta}\rVert_2^2\right]\right\}.
\]

Here \(\lambda\ge0\) controls the total penalty and \(\alpha\in[0,1]\) controls the mixture. \(\alpha=1\) gives Lasso and \(\alpha=0\) gives Ridge.

## Decision-tree impurity

\[
G(t)=1-\sum_{k=1}^{K}p_{k\mid t}^{2},
\qquad
H(t)=-\sum_{k=1}^{K}p_{k\mid t}\log(p_{k\mid t}).
\]

Here \(p_{k\mid t}\) is the proportion of class \(k\) in node \(t\). A split is useful when it reduces weighted impurity.

## Cross-validation estimate

\[
\widehat{R}_{\mathrm{CV}}=\frac{1}{K}\sum_{k=1}^{K}
\frac{1}{|I_k|}\sum_{i\in I_k}L\left(y_i,\widehat{f}^{(-k)}(\mathbf{x}_i)\right).
\]

The model \(\widehat{f}^{(-k)}\) is trained without fold \(k\), and \(I_k\) is the validation index set for that fold.

## Gradient boosting

\[
F_m(\mathbf{x})=F_{m-1}(\mathbf{x})+\nu h_m(\mathbf{x}),
\qquad 0<\nu\le1.
\]

The learner \(h_m\) is fitted to the negative gradient of the loss at the current model. The learning rate \(\nu\) controls the size of each update.

## Support-vector machine

\[
\min_{\mathbf{w},b,\boldsymbol{\xi}}
\frac{1}{2}\lVert\mathbf{w}\rVert_2^2+C\sum_{i=1}^{n}\xi_i
\]

subject to

\[
y_i(\mathbf{w}^{\top}\mathbf{x}_i+b)\ge1-\xi_i,
\qquad \xi_i\ge0.
\]

The slack variables \(\xi_i\) allow margin violations. \(C\) controls the trade-off between a wide margin and training violations.

## Calibration

For probability bins \(B_1,\ldots,B_M\), a simple expected calibration error is

\[
\operatorname{ECE}=\sum_{m=1}^{M}\frac{|B_m|}{n}
\left|\operatorname{acc}(B_m)-\operatorname{conf}(B_m)\right|.
\]

The accuracy term is the observed event frequency in the bin and the confidence term is the mean predicted probability in the bin.

## Neural network forward pass

\[
\mathbf{h}^{(1)}=\phi\left(W^{(1)}\mathbf{x}+\mathbf{b}^{(1)}\right),
\qquad
\widehat{y}=\sigma\left(W^{(2)}\mathbf{h}^{(1)}+b^{(2)}\right).
\]

The hidden activation \(\phi\) introduces nonlinearity. For binary classification, \(\sigma\) maps the final score to a probability.

## Financial evaluation

For a sequence of periodic simple returns \(R_1,\ldots,R_T\), cumulative wealth from initial wealth \(W_0\) is

\[
W_T=W_0\prod_{t=1}^{T}(1+R_t).
\]

The annualised Sharpe ratio, when the periodic risk-free rate is taken as zero for the teaching example, is

\[
\operatorname{Sharpe}=\frac{\overline{R}}{s_R}\sqrt{m},
\]

where \(m\) is the number of periods per year. State the frequency and the risk-free-rate assumption on the slide.
