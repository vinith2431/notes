# Mathematics for Intelligent Systems 3 (23MAT204 / 25MAT206)
## Complete Formula Cheat-Sheet & Quick Reference Guide

---

# Table of Contents
1. [Unit I: Optimization and Linear Algebra for AI](#unit-i-formulas)
2. [Unit II: Partial Differential Equations](#unit-ii-formulas)
3. [Unit III: Multivariate Gaussians, WLS & Markovian Systems](#unit-iii-formulas)
4. [Unit IV: Quantum Computing, Gates & Bell's Inequality](#unit-iv-formulas)

---

# Unit I: Formulas

### 1. Matrix Factorizations & Inverses
- **CR Decomposition:** $A = C R$
  - $C \in \mathbb{R}^{m \times r}$ (pivot columns, basis for $\mathcal{C}(A)$)
  - $R \in \mathbb{R}^{r \times n}$ (non-zero RREF rows, basis for $\mathcal{C}(A^T)$)
- **Singular Value Decomposition (SVD):**
  $$A = U \Sigma V^T = \sum_{i=1}^r \sigma_i u_i v_i^T$$
  - $U^T U = I_m$, $V^T V = I_n$, $\sigma_1 \ge \sigma_2 \ge \dots \ge \sigma_r > 0$.
- **Moore-Penrose Conditions (Pseudoinverse $A^\dagger$):**
  1. $A A^\dagger A = A$
  2. $A^\dagger A A^\dagger = A^\dagger$
  3. $(A A^\dagger)^T = A A^\dagger$
  4. $(A^\dagger A)^T = A^\dagger A$
- **Computing Pseudoinverse $A^\dagger$:**
  - SVD form: $A^\dagger = V \Sigma^\dagger U^T$
  - Full column rank ($m \ge n$): $A^\dagger = (A^T A)^{-1} A^T$ (left inverse)
  - Full row rank ($m \le n$): $A^\dagger = A^T (A A^T)^{-1}$ (right inverse)
  - CR form: $A^\dagger = R^\dagger C^\dagger = R^T (R R^T)^{-1} (C^T C)^{-1} C^T$
- **Minimum-Norm Least Squares:** $x^* = A^\dagger b$.

### 2. Convexity Tests
- **Jensen's Inequality:** $f(\theta x + (1 - \theta) y) \le \theta f(x) + (1 - \theta) f(y), \quad \theta \in [0, 1]$.
- **First-Order Condition:** $f(y) \ge f(x) + \nabla f(x)^T (y - x), \quad \forall x, y$.
- **Second-Order Condition (1D):** $f''(x) \ge 0$ (strictly convex if $f''(x) > 0$).
- **Hessian Matrix Test (Multivariate):** $H(x) = \nabla^2 f(x) \succeq 0$ (positive semidefinite).
  - Strictly convex if $H(x) \succ 0$ (all eigenvalues $\lambda_i > 0$).
  - Strictly concave if $H(x) \prec 0$ (all eigenvalues $\lambda_i < 0$).

### 3. Optimization Direct Methods
- **Gradient Descent:** $x_{k+1} = x_k - \alpha \nabla f(x_k)$
  - Stability condition for quadratic $f(x) = \frac{1}{2}x^T A x - b^T x$:
    $$0 < \alpha < \frac{2}{\lambda_{\max}(A)}$$
  - Exact line search step size: $\alpha_k = \frac{r_k^T r_k}{r_k^T A r_k}$, where $r_k = b - A x_k = -\nabla f(x_k)$.
  - Consecutive gradient orthogonality: $r_{k+1}^T r_k = 0$.
- **Newton's Method:** $x_{k+1} = x_k - [\nabla^2 f(x_k)]^{-1} \nabla f(x_k)$
  - Exact in 1 step for quadratic functions.
  - Quadratic local convergence: $\|x_{k+1} - x^*\| \le M \|x_k - x^*\|^2$.
- **Conjugate Gradient Method (CG):**
  - $A$-Conjugacy: $d_i^T A d_j = 0 \quad (\forall i \ne j)$.
  - Step size: $\alpha_k = \frac{r_k^T r_k}{d_k^T A d_k}$
  - State update: $x_{k+1} = x_k + \alpha_k d_k$
  - Residual update: $r_{k+1} = r_k - \alpha_k A d_k$
  - Fletcher-Reeves update: $\beta_k = \frac{r_{k+1}^T r_{k+1}}{r_k^T r_k}$
  - Direction update: $d_{k+1} = r_{k+1} + \beta_k d_k$
  - Error contraction bound:
    $$\|x_k - x^*\|_A \le 2 \left( \frac{\sqrt{\kappa} - 1}{\sqrt{\kappa} + 1} \right)^k \|x_0 - x^*\|_A, \quad \kappa = \frac{\lambda_{\max}(A)}{\lambda_{\min}(A)}$$

### 4. Sparsity & Proximal Operators
- **Soft-Thresholding Operator (Proximal Operator of $L_1$):**
  $$\mathcal{S}_\tau(v) = \text{sign}(v) \max(|v| - \tau, 0)$$
- **ISTA Update:** $w_{k+1} = \mathcal{S}_{\alpha \lambda}\left( w_k - \alpha X^T (X w_k - y) \right)$ with $\alpha < 1/\lambda_{\max}(X^T X)$.
- **Ridge Solution ($L_2$):** $w_{\text{ridge}} = (X^T X + \lambda I)^{-1} X^T y$.

### 5. Constrained Optimization & KKT
- **Lagrangian:** $L(x, \lambda, \nu) = f_0(x) + \sum_{i=1}^m \lambda_i f_i(x) + \sum_{j=1}^p \nu_j h_j(x)$.
- **The 4 KKT Conditions:**
  1. *Stationarity:* $\nabla f_0(x^*) + \sum_{i=1}^m \lambda_i^* \nabla f_i(x^*) + \sum_{j=1}^p \nu_j^* \nabla h_j(x^*) = 0$
  2. *Primal Feasibility:* $f_i(x^*) \le 0, \quad h_j(x^*) = 0$
  3. *Dual Feasibility:* $\lambda_i^* \ge 0$
  4. *Complementary Slackness:* $\lambda_i^* f_i(x^*) = 0$
- **Water-Filling Formula:** $x_i^* = \max\left( \frac{1}{\nu} - \alpha_i, 0 \right)$ with $\sum x_i^* = P$.

### 6. Projected Gradient Descent (PGD)
- **PGD Iteration:** $x_{k+1} = \Pi_C \left( x_k - \alpha \nabla f(x_k) \right)$
- **Orthant Projection:** $[\Pi_{\mathbb{R}_+^n}(v)]_i = \max(v_i, 0)$.
- **Ball Projection:** $\Pi_{B(R)}(v) = R \frac{v}{\|v\|_2}$ (if $\|v\|_2 > R$).
- **Affine Projection ($Ax = b$):** $\Pi(v) = v - A^T (A A^T)^{-1} (A v - b)$.

### 7. Support Vector Machines (SVM)
- **Margin Width:** $\gamma = \frac{2}{\|w\|_2}$.
- **Primal Soft-Margin:** $\min_{w, b, \xi} \frac{1}{2}\|w\|_2^2 + C \sum_{i=1}^N \xi_i \quad \text{s.t.} \quad y_i(w^T x_i + b) \ge 1 - \xi_i, \ \xi_i \ge 0$.
- **Dual Problem:**
  $$\max_\alpha \sum_{i=1}^N \alpha_i - \frac{1}{2} \sum_{i=1}^N \sum_{j=1}^N \alpha_i \alpha_j y_i y_j K(x_i, x_j) \quad \text{s.t.} \quad 0 \le \alpha_i \le C, \ \sum_{i=1}^N \alpha_i y_i = 0$$
- **Hyperplane Normal:** $w^* = \sum_{i \in \text{SV}} \alpha_i y_i x_i$.
- **RBF Gaussian Kernel:** $K(x, z) = \exp\left( -\gamma \|x - z\|^2 \right) = \exp\left( -\frac{\|x - z\|^2}{2\sigma^2} \right)$.

### 8. Krylov Subspaces, Arnoldi & DMD
- **Krylov Subspace:** $\mathcal{K}_m(A, b) = \text{span}\{b, Ab, A^2 b, \dots, A^{m-1} b\}$.
- **Arnoldi Relation:** $A Q_m = Q_m H_m + h_{m+1, m} q_{m+1} e_m^T$.
- **Lanczos (Symmetric):** $H_m = T_m$ (tridiagonal) $\implies A q_j = \beta_{j-1} q_{j-1} + \alpha_j q_j + \beta_j q_{j+1}$.
- **SVD-Based DMD:**
  - Reduced matrix: $\tilde{A} = U_r^T Y V_r \Sigma_r^{-1}$.
  - Continuous eigenvalues: $\mu_i = \frac{\ln(\lambda_i)}{\Delta t} = \sigma_i + i \omega_i$.
  - Decay rate: $\sigma_i = \text{Re}(\mu_i)$. Physical frequency: $f_i = \frac{|\text{Im}(\mu_i)|}{2\pi} \text{ Hz}$.
  - DMD modes: $\Phi = Y V_r \Sigma_r^{-1} W$, where $\tilde{A} W = W \Lambda$.
- **HOSVD Mode-$n$ Unfolding:** $X_{(n)} \in \mathbb{R}^{I_n \times \prod_{k \ne n} I_k} \implies X_{(n)} = U^{(n)} \Sigma^{(n)} V^{(n)T}$.

---

# Unit II: Formulas

### 1. Vector Calculus Operators
- **Gradient:** $\nabla \phi = \left( \frac{\partial \phi}{\partial x}, \frac{\partial \phi}{\partial y}, \frac{\partial \phi}{\partial z} \right)$
- **Divergence:** $\nabla \cdot \mathbf{F} = \frac{\partial F_1}{\partial x} + \frac{\partial F_2}{\partial y} + \frac{\partial F_3}{\partial z}$
- **Curl:** $\nabla \times \mathbf{F} = \left( \frac{\partial F_3}{\partial y} - \frac{\partial F_2}{\partial z}, \ \frac{\partial F_1}{\partial z} - \frac{\partial F_3}{\partial x}, \ \frac{\partial F_2}{\partial x} - \frac{\partial F_1}{\partial y} \right)$
- **Laplacian:** $\nabla^2 u = \frac{\partial^2 u}{\partial x^2} + \frac{\partial^2 u}{\partial y^2} + \frac{\partial^2 u}{\partial z^2}$
- **Divergence Theorem:** $\iiint_V (\nabla \cdot \mathbf{F}) \, dV = \iint_{\partial V} \mathbf{F} \cdot \mathbf{n} \, dS$
- **Stokes' Theorem:** $\iint_S (\nabla \times \mathbf{F}) \cdot \mathbf{n} \, dS = \oint_{\partial S} \mathbf{F} \cdot d\mathbf{r}$

### 2. PDE Classification ($A u_{xx} + B u_{xy} + C u_{yy} + \dots = 0$)
- **Discriminant:** $\Delta = B^2 - 4AC$
  - $\Delta > 0 \iff$ **Hyperbolic** (Wave equation: $u_{tt} - c^2 u_{xx} = 0$)
  - $\Delta = 0 \iff$ **Parabolic** (Heat equation: $u_t - \alpha u_{xx} = 0$)
  - $\Delta < 0 \iff$ **Elliptic** (Laplace equation: $u_{xx} + u_{yy} = 0$)

### 3. Analytical PDE Solutions
- **Method of Characteristics (1st-Order):** $\frac{dx}{a} = \frac{dy}{b} = \frac{du}{c}$.
- **1D Heat Equation Fourier Series:**
  $$u(x, t) = \sum_{n=1}^\infty A_n e^{-\alpha \left(\frac{n\pi}{L}\right)^2 t} \sin\left(\frac{n\pi x}{L}\right), \quad A_n = \frac{2}{L} \int_0^L f(x) \sin\left(\frac{n\pi x}{L}\right) dx$$
- **Fourier Transform on $\mathbb{R}$:**
  - $\mathcal{F}\{u_x\} = i\omega \hat{u}$, $\mathcal{F}\{u_{xx}\} = -\omega^2 \hat{u}$.
  - Heat solution in frequency domain: $\hat{u}(\omega, t) = \hat{u}(\omega, 0) e^{-\alpha \omega^2 t}$.
  - Advection solution ($u_t + c u_x = 0$): $u(x, t) = f(x - ct)$.

### 4. Numerical Finite Differences (FDM)
- **Mesh Ratios:** $h = \Delta x$, $k = \Delta t$.
  - Heat mesh ratio: $r = \frac{\alpha k}{h^2} = \frac{\alpha \Delta t}{\Delta x^2}$.
  - Courant number (wave): $C = \frac{c k}{h} = \frac{c \Delta t}{\Delta x}$.
- **Explicit FTCS Heat Update:**
  $$u_i^{n+1} = r u_{i-1}^n + (1 - 2r) u_i^n + r u_{i+1}^n$$
  - von Neumann amplification factor: $G(\theta) = 1 - 4r \sin^2(\theta/2)$.
  - **Stability Criterion:** $r = \frac{\alpha \Delta t}{\Delta x^2} \le \frac{1}{2}$.
- **Implicit BTCS Heat Update:**
  $$-r u_{i-1}^{n+1} + (1 + 2r) u_i^{n+1} - r u_{i+1}^{n+1} = u_i^n \quad (\text{unconditionally stable})$$
- **Crank-Nicolson Scheme:**
  $$-\frac{r}{2} u_{i-1}^{n+1} + (1 + r) u_i^{n+1} - \frac{r}{2} u_{i+1}^{n+1} = \frac{r}{2} u_{i-1}^n + (1 - r) u_i^n + \frac{r}{2} u_{i+1}^n$$
  - Error: $O(\Delta t^2 + \Delta x^2)$, unconditionally stable.
- **Wave Explicit Scheme:**
  $$u_i^{n+1} = 2(1 - C^2) u_i^n + C^2 (u_{i+1}^n + u_{i-1}^n) - u_i^{n-1}$$
  - **CFL Stability Condition:** $C = \frac{c \Delta t}{\Delta x} \le 1$.
- **Elliptic Relaxation (Laplace 5-Point Stencil):**
  - Gauss-Seidel: $u_{i, j}^{(k+1)} = \frac{1}{4}(u_{i-1, j}^{(k+1)} + u_{i+1, j}^{(k)} + u_{i, j-1}^{(k+1)} + u_{i, j+1}^{(k)})$.
  - SOR: $u_{i, j}^{(k+1)} = (1 - \omega) u_{i, j}^{(k)} + \frac{\omega}{4}(u_{i-1, j}^{(k+1)} + u_{i+1, j}^{(k)} + u_{i, j-1}^{(k+1)} + u_{i, j+1}^{(k)}), \quad \omega \in (1, 2)$.

---

# Unit III: Formulas

### 1. Multivariate Gaussian Distribution
- **PDF in $\mathbb{R}^n$:**
  $$p(x) = \frac{1}{(2\pi)^{n/2} |\Sigma|^{1/2}} \exp\left( -\frac{1}{2} (x - \mu)^T \Sigma^{-1} (x - \mu) \right)$$
- **Mahalanobis Distance:** $D_M^2(x, \mu) = (x - \mu)^T \Sigma^{-1} (x - \mu)$.
- **Partitioned Gaussian Properties:**
  $$X = \begin{pmatrix} X_1 \\ X_2 \end{pmatrix} \sim \mathcal{N}\left( \begin{pmatrix} \mu_1 \\ \mu_2 \end{pmatrix}, \begin{pmatrix} \Sigma_{11} & \Sigma_{12} \\ \Sigma_{21} & \Sigma_{22} \end{pmatrix} \right)$$
  - Marginal: $X_1 \sim \mathcal{N}(\mu_1, \Sigma_{11})$.
  - Conditional: $X_1 \mid X_2 = x_2 \sim \mathcal{N}(\mu_{1|2}, \Sigma_{1|2})$.
    $$\mu_{1|2} = \mu_1 + \Sigma_{12} \Sigma_{22}^{-1} (x_2 - \mu_2)$$
    $$\Sigma_{1|2} = \Sigma_{11} - \Sigma_{12} \Sigma_{22}^{-1} \Sigma_{21} \quad (\text{Schur complement, independent of } x_2)$$

### 2. Weighted Least Squares (WLS)
- **Objective:** $J(\beta) = (y - X \beta)^T W (y - X \beta) = \sum_{i=1}^N w_i (y_i - x_i^T \beta)^2$, with $w_i = 1/\sigma_i^2$.
- **Normal Equations:** $(X^T W X) \beta = X^T W y$.
- **WLS Estimator:** $\hat{\beta}_{\text{WLS}} = (X^T W X)^{-1} X^T W y$.
- **Equivalence to Scaled OLS:** Let $W = D^2 \implies (D X) \beta \approx D y$.

### 3. Discrete-Time Markov Chains (DTMC)
- **Transition Matrix:** $P_{ij} = P(X_{n+1} = j \mid X_n = i) \ge 0, \quad \sum_{j} P_{ij} = 1$.
- **Chapman-Kolmogorov / Multi-Step Distribution:** $\pi^{(n)} = \pi^{(0)} P^n$.
- **Stationary Distribution:** $\pi P = \pi, \quad \sum_i \pi_i = 1, \quad \pi_i \ge 0$.

### 4. Markov Decision Processes (MDP)
- **Discounted Return:** $G_t = \sum_{k=0}^\infty \gamma^k R_{t+k+1}, \quad \gamma \in [0, 1)$.
- **Bellman Expectation Equation:**
  $$V^\pi(s) = \sum_{a} \pi(a \mid s) \left[ \mathcal{R}(s, a) + \gamma \sum_{s'} \mathcal{P}(s' \mid s, a) V^\pi(s') \right]$$
  - Matrix form: $V^\pi = (I - \gamma P^\pi)^{-1} R^\pi$.
- **Bellman Optimality Equation:**
  $$V^*(s) = \max_{a} \left[ \mathcal{R}(s, a) + \gamma \sum_{s'} \mathcal{P}(s' \mid s, a) V^*(s') \right]$$
- **Value Iteration:** $V_{k+1}(s) = \max_a \left[ \mathcal{R}(s, a) + \gamma \sum_{s'} \mathcal{P}(s' \mid s, a) V_k(s') \right]$ ($\gamma$-contraction mapping).

---

# Unit IV: Formulas

### 1. Quantum State Spaces & Bloch Sphere
- **General Qubit State:** $|\psi\rangle = a |0\rangle + b |1\rangle, \quad a, b \in \mathbb{C}, \quad |a|^2 + |b|^2 = 1$.
- **Computational Basis:** $|0\rangle = \begin{pmatrix} 1 \\ 0 \end{pmatrix}, \quad |1\rangle = \begin{pmatrix} 0 \\ 1 \end{pmatrix}$.
- **Bloch Sphere Parametrization:**
  $$|\psi\rangle = \cos\left(\frac{\theta}{2}\right) |0\rangle + e^{i\phi} \sin\left(\frac{\theta}{2}\right) |1\rangle, \quad \theta \in [0, \pi], \ \phi \in [0, 2\pi)$$
- **Born's Rule:** $P(m) = |\langle m | \psi \rangle|^2 = \langle \psi | P_m | \psi \rangle$.
- **Completeness:** $|0\rangle\langle 0| + |1\rangle\langle 1| = I_2$.

### 2. Quantum Observables & Gates
- **Unitary Gate Condition:** $U^\dagger U = U U^\dagger = I \implies U^{-1} = U^\dagger$.
- **Pauli Matrices:**
  $$X = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}, \qquad Y = \begin{pmatrix} 0 & -i \\ i & 0 \end{pmatrix}, \qquad Z = \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}$$
- **Hadamard Gate:** $H = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 & 1 \\ 1 & -1 \end{pmatrix}$
  - $H|0\rangle = |+\rangle = \frac{|0\rangle + |1\rangle}{\sqrt{2}}$, $H|1\rangle = |-\rangle = \frac{|0\rangle - |1\rangle}{\sqrt{2}}$.
- **Phase & Rotation Gates:**
  - $S = \begin{pmatrix} 1 & 0 \\ 0 & i \end{pmatrix}$, $T = \begin{pmatrix} 1 & 0 \\ 0 & e^{i\pi/4} \end{pmatrix}$.
  - $R_x(\theta) = \cos(\theta/2)I - i\sin(\theta/2)X$, $R_y(\theta) = \cos(\theta/2)I - i\sin(\theta/2)Y$, $R_z(\theta) = e^{-i\theta Z/2}$.
- **CNOT Gate:** $\text{CNOT} |c, t\rangle = |c, c \oplus t\rangle \implies \text{CNOT} = \begin{pmatrix} 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0 \end{pmatrix}$.

### 3. Multi-Qubit & Entanglement
- **Product State Condition for $|\psi\rangle = c_{00}|00\rangle + c_{01}|01\rangle + c_{10}|10\rangle + c_{11}|11\rangle$:**
  $$c_{00} c_{11} - c_{01} c_{10} = 0 \quad (\ne 0 \iff \text{entangled})$$
- **The Four Bell States (Maximally Entangled):**
  $$|\Phi^\pm\rangle = \frac{|00\rangle \pm |11\rangle}{\sqrt{2}}, \qquad |\Psi^\pm\rangle = \frac{|01\rangle \pm |10\rangle}{\sqrt{2}}$$
- **Bell State Generation Circuit:** $\text{CNOT}_{1 \to 2} (H_1 \otimes I_2) |00\rangle = |\Phi^+\rangle$.

### 4. Bell's Inequality (CHSH)
- **CHSH Operator:** $S = AB + AB' + A'B - A'B'$.
- **Classical Local Realism Bound:** $|S| \le 2$.
- **Quantum Tsirelson's Bound:** $|S| = 2\sqrt{2} \approx 2.828$.
