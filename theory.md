# Mathematics for Intelligent Systems 3 (23MAT204 / 25MAT206)
## Comprehensive Master Theory, Formulas & Algorithms Guide
### Complete Reference for Units I, II, III, and IV

---

# Table of Contents
1. [Unit I: Optimization and Linear Algebra for AI](#unit-i-optimization-and-linear-algebra-for-ai)
   - [1.1 Mathematical Workhorse: CR Decomposition, SVD & Pseudoinverse](#11-mathematical-workhorse-cr-decomposition-svd--pseudoinverse)
   - [1.2 Convex Functions and the 4 Methods to Test Convexity](#12-convex-functions-and-the-4-methods-to-test-convexity)
   - [1.3 Direct Methods for Unconstrained Convex Optimization](#13-direct-methods-for-unconstrained-convex-optimization)
     - [Gradient Descent (First-Order)](#gradient-descent)
     - [Newton's Method (Second-Order)](#newtons-method)
     - [Conjugate Direction & Conjugate Gradient Method (CGM)](#conjugate-gradient-method-cgm)
     - [Coordinate Descent](#coordinate-descent)
   - [1.4 Sparsity-Inducing Penalty Functions](#14-sparsity-inducing-penalty-functions)
     - [L0 vs L1 vs L2 (LASSO vs Ridge)](#l0-vs-l1-vs-l2-lasso-vs-ridge)
     - [Subgradients and Proximal Gradient (ISTA / FISTA)](#subgradients-and-proximal-gradient-ista--fista)
     - [Other Sparsity Penalties: Elastic Net, Group LASSO, SCAD, MCP](#other-sparsity-penalties)
   - [1.5 Constrained Convex Optimization and KKT Conditions](#15-constrained-convex-optimization-and-kkt-conditions)
     - [Lagrangian, Dual Problem & Slater's Condition](#lagrangian-dual-problem--slaters-condition)
     - [The Karush-Kuhn-Tucker (KKT) Necessary & Sufficient Conditions](#kkt-conditions)
     - [Active Set Strategy & Water-Filling](#active-set-strategy--water-filling)
   - [1.6 Formulating Problems as Linear Programming (LP) and Quadratic Programming (QP)](#16-formulating-problems-as-lp-and-qp)
   - [1.7 Projected Gradient Descent (PGD) Method](#17-projected-gradient-descent-pgd-method)
   - [1.8 Support Vector Machines (SVM)](#18-support-vector-machines-svm)
     - [Hard-Margin Primal and Dual Formulations](#hard-margin-svm)
     - [Soft-Margin Formulation and Slack Variables (Role of C)](#soft-margin-svm)
     - [Kernel Trick and Non-linear SVM](#kernel-trick)
   - [1.9 Krylov Subspace Methods: Arnoldi, Lanczos, FOM & GMRES](#19-krylov-subspace-methods)
   - [1.10 Reproducing Kernel Hilbert Spaces (RKHS) & Random Kitchen Sinks (RKS)](#110-reproducing-kernel-hilbert-spaces-rkhs--random-kitchen-sinks-rks)
   - [1.11 Dynamic Mode Decomposition (DMD) & Koopman Operator Theory](#111-dynamic-mode-decomposition-dmd--koopman-operator-theory)
   - [1.12 Tensors and Higher-Order SVD (HOSVD)](#112-tensors-and-higher-order-svd-hosvd)
2. [Unit II: Partial Differential Equations in Physics and Engineering](#unit-ii-partial-differential-equations-in-physics-and-engineering)
   - [2.1 Vector Calculus Toolkit for PDEs](#21-vector-calculus-toolkit-for-pdes)
   - [2.2 Formulation and Classification of PDEs](#22-formulation-and-classification-of-pdes)
   - [2.3 Analytical Methods: Separation of Variables & Transform Techniques](#23-analytical-methods)
   - [2.4 Numerical Finite Difference Methods (FDM)](#24-numerical-finite-difference-methods-fdm)
     - [Explicit FTCS Scheme and von Neumann Stability Analysis](#explicit-ftcs-scheme)
     - [Implicit BTCS and Crank-Nicolson Schemes](#implicit-btcs-and-crank-nicolson-schemes)
     - [Explicit Scheme for the Wave Equation and the CFL Condition](#explicit-scheme-for-the-wave-equation)
     - [Elliptic PDEs (Laplace / Poisson) and Iterative Relaxation (Jacobi, Gauss-Seidel, SOR)](#elliptic-pdes-and-relaxation-methods)
   - [2.5 Computational Implementations: MATLAB, Excel, and Simulink Method of Lines](#25-computational-implementations)
3. [Unit III: Multivariate Gaussians, Weighted Least Squares, Markov Chains, and MDP](#unit-iii-multivariate-gaussians-weighted-least-squares-markov-chains-and-mdp)
   - [3.1 Multivariate Gaussian Distributions](#31-multivariate-gaussian-distributions)
     - [Geometry, Covariance Ellipsoids & Mahalanobis Distance](#geometry-of-multivariate-gaussians)
     - [Marginal and Conditional Distributions via Schur Complement](#marginal-and-conditional-distributions)
   - [3.2 Weighted Least Squares (WLS)](#32-weighted-least-squares-wls)
     - [Formulation, Derivation of Normal Equations & BLUE Property](#wls-formulation-and-normal-equations)
     - [Equivalence to Rescaled OLS and Connection to Gaussian Likelihood](#wls-as-rescaled-ols)
   - [3.3 Discrete-Time Markov Chains (DTMC)](#33-discrete-time-markov-chains-dtmc)
     - [Transition Matrices, Chapman-Kolmogorov & Multi-Step Distributions](#dtmc-foundations)
     - [Stationary Distributions, Irreducibility & Ergodicity](#stationary-distributions)
   - [3.4 Markov Decision Processes (MDP) and Dynamic Programming](#34-markov-decision-processes-mdp-and-dynamic-programming)
     - [Components: States, Actions, Transitions, Rewards, Discounting](#mdp-components)
     - [Bellman Expectation and Optimality Equations](#bellman-equations)
     - [Value Iteration and Policy Iteration Algorithms](#value-and-policy-iteration)
4. [Unit IV: Introduction to Quantum Computing, Bell's Inequality, and Quantum Gates](#unit-iv-introduction-to-quantum-computing-bells-inequality-and-quantum-gates)
   - [4.1 Mathematical Foundations of Quantum Information](#41-mathematical-foundations-of-quantum-information)
     - [Dirac Bra-Ket Notation, State Space C2 & Normalization](#dirac-notation-and-qubit-state-space)
     - [The Bloch Sphere Representation](#the-bloch-sphere)
   - [4.2 Physical Realization: Electron Spin-1/2 and Pauli Operators](#42-physical-realization-electron-spin)
   - [4.3 Superposition, Bases, and Global vs Relative Phase](#43-superposition-bases-and-phase)
   - [4.4 Quantum Measurement, Born's Rule, and State Collapse](#44-quantum-measurement-and-state-collapse)
   - [4.5 Multi-Qubit Systems, Tensor Products, and Entanglement](#45-multi-qubit-systems-and-entanglement)
     - [Product States vs Entangled States](#product-vs-entangled-states)
     - [The Four Bell States (EPR Pairs)](#the-four-bell-states)
   - [4.6 Bell's Inequality and the CHSH Test](#46-bells-inequality-and-the-chsh-test)
     - [Local Hidden Variables vs Quantum Mechanics](#local-hidden-variables)
     - [The CHSH Inequality: Classical Bound <= 2 vs Quantum Tsirelson Bound 2*sqrt(2)](#chsh-inequality)
     - [No-Signaling Principle](#no-signaling-principle)
   - [4.7 Quantum Gates, Circuits, Reversibility, and Universality](#47-quantum-gates-and-circuits)
     - [Unitary Matrices as Quantum Gates](#unitary-matrices)
     - [Single-Qubit Gates (X, Y, Z, H, S, T, Rotations)](#single-qubit-gates)
     - [Two-Qubit Gates (CNOT, Controlled Phase, SWAP)](#two-qubit-gates)
     - [Bell State Generation Circuit](#bell-state-circuit)
     - [Reversibility vs Classical Irreversibility & The No-Cloning Theorem](#no-cloning-theorem)

---

# Unit I: Optimization and Linear Algebra for AI

## 1.1 Mathematical Workhorse: CR Decomposition, SVD & Pseudoinverse

### 1.1.1 Column-Row (CR) Decomposition
Every matrix $A \in \mathbb{R}^{m \times n}$ of rank $r$ can be factored into:
$$A = C R$$
where:
- $C \in \mathbb{R}^{m \times r}$ contains the $r$ linearly independent pivot columns of $A$. $C$ forms a basis for the column space $\mathcal{C}(A)$.
- $R \in \mathbb{R}^{r \times n}$ contains the non-zero rows of the reduced row echelon form (RREF) of $A$. $R$ forms a basis for the row space $\mathcal{C}(A^T)$.

### 1.1.2 Singular Value Decomposition (SVD)
Any matrix $A \in \mathbb{R}^{m \times n}$ can be factored as:
$$A = U \Sigma V^T = \sum_{i=1}^r \sigma_i u_i v_i^T$$
where:
- $U \in \mathbb{R}^{m \times m}$ is orthogonal ($U^T U = I_m$), columns $u_i$ are left singular vectors (eigenvectors of $A A^T$).
- $\Sigma \in \mathbb{R}^{m \times n}$ is diagonal with singular values $\sigma_1 \ge \sigma_2 \ge \dots \ge \sigma_r > 0$.
- $V \in \mathbb{R}^{n \times n}$ is orthogonal ($V^T V = I_n$), columns $v_i$ are right singular vectors (eigenvectors of $A^T A$).

### 1.1.3 The Moore-Penrose Pseudoinverse ($A^\dagger$ or $A^+$)
For any matrix $A$, its Moore-Penrose pseudoinverse $A^\dagger \in \mathbb{R}^{n \times m}$ is the unique matrix satisfying the **four Moore-Penrose conditions**:
1. **$A A^\dagger A = A$** (acts as a weak inverse on $\mathcal{C}(A)$)
2. **$A^\dagger A A^\dagger = A^\dagger$** ($A^\dagger$ is its own weak inverse)
3. **$(A A^\dagger)^T = A A^\dagger$** ($A A^\dagger$ is the symmetric orthogonal projector onto $\mathcal{C}(A)$)
4. **$(A^\dagger A)^T = A^\dagger A$** ($A^\dagger A$ is the symmetric orthogonal projector onto $\mathcal{C}(A^T)$)

**Computation via Decompositions:**
- **Via SVD:** If $A = U \Sigma V^T$, then:
  $$A^\dagger = V \Sigma^\dagger U^T = \sum_{i=1}^r \frac{1}{\sigma_i} v_i u_i^T$$
  where $\Sigma^\dagger$ transposes $\Sigma$ and replaces non-zero singular values $\sigma_i$ with $1/\sigma_i$.
- **Via Full Column Rank ($m \ge n$, $\text{rank}(A)=n$):**
  $$A^\dagger = (A^T A)^{-1} A^T \quad \text{(Left inverse, } A^\dagger A = I_n\text{)}$$
- **Via Full Row Rank ($m \le n$, $\text{rank}(A)=m$):**
  $$A^\dagger = A^T (A A^T)^{-1} \quad \text{(Right inverse, } A A^\dagger = I_m\text{)}$$
- **Via CR Decomposition:** If $A = C R$ where $C$ has full column rank and $R$ has full row rank:
  $$A^\dagger = R^\dagger C^\dagger = R^T (R R^T)^{-1} (C^T C)^{-1} C^T$$

**Least Squares Solution:**
For any linear system $A x = b$, the vector $x^* = A^\dagger b$ is the unique minimum-norm least-squares solution:
$$x^* = \arg\min_{x} \|x\|_2 \quad \text{subject to } x \in \arg\min_z \|A z - b\|_2$$

---

## 1.2 Convex Functions and the 4 Methods to Test Convexity

### 1.2.1 Definitions
- **Convex Set:** A set $C \subseteq \mathbb{R}^n$ is convex if for all $x, y \in C$ and $\theta \in [0, 1]$:
  $$\theta x + (1 - \theta) y \in C$$
- **Convex Function:** A function $f: C \to \mathbb{R}$ on a convex set $C$ is convex if:
  $$f(\theta x + (1 - \theta) y) \le \theta f(x) + (1 - \theta) f(y) \quad \forall x, y \in C, \ \theta \in [0, 1]$$
  Geometrically: The line segment connecting $(x, f(x))$ and $(y, f(y))$ lies on or above the graph of $f$.
- **Strictly Convex Function:** The inequality is strict for all $x \ne y$ and $\theta \in (0, 1)$. Strict convexity guarantees that if a local minimum exists, it is the **unique global minimum**.
- **Concave Function:** $f$ is concave if $-f$ is convex, i.e., $f(\theta x + (1 - \theta) y) \ge \theta f(x) + (1 - \theta) f(y)$.

### 1.2.2 The 4 Methods to Test Convexity

1. **Definition Test (Jensen's Inequality / Chord Test):**
   Directly verify whether $f(\theta x + (1 - \theta) y) \le \theta f(x) + (1 - \theta) f(y)$ holds for all points and all $\theta \in [0, 1]$. Useful for basic functions like $|x|$ or $\|x\|$.

2. **First Derivative Condition (Tangent Hyperplane Test):**
   Let $f$ be continuously differentiable. $f$ is convex on convex domain $C$ if and only if:
   $$f(y) \ge f(x) + \nabla f(x)^T (y - x) \quad \forall x, y \in C$$
   *Interpretation:* The first-order Taylor approximation is a global lower bound on the function. Tangent lines/hyperplanes lie below the function.
   *Strict convexity:* $f(y) > f(x) + \nabla f(x)^T (y - x)$ for all $y \ne x$.

3. **Second Derivative Test (for Single Variable Functions):**
   Let $f: \mathbb{R} \to \mathbb{R}$ be twice continuously differentiable.
   - Convex on interval $I \iff f''(x) \ge 0$ for all $x \in I$.
   - Strictly convex if $f''(x) > 0$ for all $x \in I$.
   - Concave $\iff f''(x) \le 0$. Strictly concave if $f''(x) < 0$.

4. **Hessian Matrix Test (for Multivariable Functions):**
   Let $f: \mathbb{R}^n \to \mathbb{R}$ be twice continuously differentiable. The Hessian matrix is the $n \times n$ symmetric matrix of second partial derivatives:
   $$H(x) = \nabla^2 f(x) = \begin{pmatrix} \frac{\partial^2 f}{\partial x_1^2} & \frac{\partial^2 f}{\partial x_1 \partial x_2} & \dots & \frac{\partial^2 f}{\partial x_1 \partial x_n} \\ \frac{\partial^2 f}{\partial x_2 \partial x_1} & \frac{\partial^2 f}{\partial x_2^2} & \dots & \frac{\partial^2 f}{\partial x_2 \partial x_n} \\ \vdots & \vdots & \ddots & \vdots \\ \frac{\partial^2 f}{\partial x_n \partial x_1} & \frac{\partial^2 f}{\partial x_n \partial x_2} & \dots & \frac{\partial^2 f}{\partial x_n^2} \end{pmatrix}$$
   - **Convex $\iff H(x) \succeq 0$ (Positive Semidefinite)** for all $x$. All eigenvalues $\lambda_i \ge 0$, or all principal minors $\ge 0$.
   - **Strictly Convex if $H(x) \succ 0$ (Positive Definite)** for all $x$. All eigenvalues $\lambda_i > 0$, or all leading principal minors $> 0$ (Sylvester's criterion).
   - **Concave $\iff H(x) \preceq 0$ (Negative Semidefinite)** for all $x$. All eigenvalues $\lambda_i \le 0$.
   - **Strictly Concave if $H(x) \prec 0$ (Negative Definite)** for all $x$. All eigenvalues $\lambda_i < 0$.
   - **Indefinite:** If $H$ has both positive and negative eigenvalues, $f$ is neither convex nor concave (e.g. saddle points).

---

## 1.3 Direct Methods for Unconstrained Convex Optimization

We consider minimizing a convex differentiable function $f: \mathbb{R}^n \to \mathbb{R}$.

### 1.3.1 Gradient Descent (First-Order Method)
**Core Idea:** Repeatedly take steps in the direction of the negative gradient (the direction of steepest local decrease):
$$x_{k+1} = x_k - \alpha_k \nabla f(x_k)$$
where $\alpha_k > 0$ is the step size (learning rate).

**Step Size Rules:**
- **Fixed step size:** $\alpha_k = \alpha$. For $L$-Lipschitz gradient ($\|\nabla f(x) - \nabla f(y)\| \le L \|x - y\|$), GD converges if $0 < \alpha < \frac{2}{L}$. For a quadratic $f(x) = \frac{1}{2} x^T A x - b^T x$, $L = \lambda_{\max}(A)$, so convergence requires:
  $$0 < \alpha < \frac{2}{\lambda_{\max}(A)}$$
- **Exact Line Search:** Choose $\alpha_k = \arg\min_{\alpha > 0} f(x_k - \alpha \nabla f(x_k))$.
  For quadratic $f(x) = \frac{1}{2} x^T A x - b^T x$ with residual $r_k = b - A x_k = -\nabla f(x_k)$:
  $$\alpha_k = \frac{r_k^T r_k}{r_k^T A r_k}$$

**Crucial Orthogonality Property:**
In exact line search, consecutive gradients are always orthogonal:
$$\nabla f(x_{k+1})^T \nabla f(x_k) = 0 \quad \text{or} \quad r_{k+1}^T r_k = 0$$
*Proof:* Let $g(\alpha) = f(x_k + \alpha d_k)$ where $d_k = -\nabla f(x_k)$. At the minimizer $\alpha_k$, the derivative must vanish:
$$\frac{d}{d\alpha} f(x_k + \alpha d_k) \Big|_{\alpha = \alpha_k} = \nabla f(x_{k+1})^T d_k = -\nabla f(x_{k+1})^T \nabla f(x_k) = 0$$
*Consequence:* On ill-conditioned problems (large condition number $\kappa = \lambda_{\max}/\lambda_{\min}$), this orthogonality forces gradient descent to **zig-zag** inefficiently across narrow valleys, leading to slow linear convergence with factor $\frac{\kappa - 1}{\kappa + 1} \approx 1 - \frac{2}{\kappa}$.

### 1.3.2 Newton's Method (Second-Order Method)
**Core Idea:** Approximate $f$ by its second-order Taylor polynomial at $x_k$:
$$f(x_k + \Delta x) \approx f(x_k) + \nabla f(x_k)^T \Delta x + \frac{1}{2} \Delta x^T \nabla^2 f(x_k) \Delta x$$
Setting the gradient of this quadratic approximation with respect to $\Delta x$ to zero gives:
$$\nabla f(x_k) + \nabla^2 f(x_k) \Delta x = 0 \implies \Delta x = - [\nabla^2 f(x_k)]^{-1} \nabla f(x_k)$$
**Newton Update:**
$$x_{k+1} = x_k - [\nabla^2 f(x_k)]^{-1} \nabla f(x_k)$$

**Key Properties:**
- **Exact 1-step convergence on quadratics:** If $f(x) = \frac{1}{2} x^T A x - b^T x$, $\nabla^2 f(x) = A$ is constant, and $\nabla f(x) = A x - b$. Then $x_1 = x_0 - A^{-1}(A x_0 - b) = A^{-1}b = x^*$.
- **Quadratic Convergence near the minimum:** On general smooth strictly convex functions, Newton's method exhibits quadratic convergence (the number of accurate digits roughly doubles every iteration):
  $$\|x_{k+1} - x^*\| \le M \|x_k - x^*\|^2$$
- **Computational Trade-off:** Computing and inverting/factoring the $n \times n$ Hessian costs $O(n^3)$ operations per iteration, which becomes intractable when $n > 10^4$.

### 1.3.3 Conjugate Direction & Conjugate Gradient Method (CGM)
CGM solves symmetric positive definite (SPD) linear systems $A x = b$ (or minimizes $f(x) = \frac{1}{2}x^T A x - b^T x$) in at most $n$ iterations without inverting $A$.

**Definition of $A$-Conjugacy:**
A set of non-zero directions $\{d_0, d_1, \dots, d_{n-1}\}$ is said to be **$A$-conjugate** (or $A$-orthogonal) if:
$$d_i^T A d_j = 0 \quad \forall i \ne j$$
Because $A \succ 0$, $A$-conjugate vectors are linearly independent.

**Conjugate Direction Algorithm:**
Starting from $x_0$, for $k = 0, 1, \dots, n-1$:
1. Step size along direction $d_k$:
   $$\alpha_k = -\frac{d_k^T (A x_k - b)}{d_k^T A d_k} = \frac{d_k^T r_k}{d_k^T A d_k}$$
2. State update:
   $$x_{k+1} = x_k + \alpha_k d_k$$
3. Residual update:
   $$r_{k+1} = r_k - \alpha_k A d_k$$

**The Conjugate Gradient Algorithm (CG):**
Instead of pre-supplying directions, CG computes conjugate directions on the fly from the residuals.
- **Initialisation:** Choose $x_0$. Compute $r_0 = b - A x_0$. Set $d_0 = r_0$.
- **For $k = 0, 1, 2, \dots$ until $\|r_k\| < \epsilon$:**
  1. $\alpha_k = \frac{r_k^T r_k}{d_k^T A d_k}$
  2. $x_{k+1} = x_k + \alpha_k d_k$
  3. $r_{k+1} = r_k - \alpha_k A d_k$
  4. $\beta_k = \frac{r_{k+1}^T r_{k+1}}{r_k^T r_k}$ (Fletcher-Reeves formula)
  5. $d_{k+1} = r_{k+1} + \beta_k d_k$

**Orthogonality and Conjugacy Invariants:**
- Residuals are mutually orthogonal: $r_i^T r_j = 0$ for all $i \ne j$.
- Directions are mutually $A$-conjugate: $d_i^T A d_j = 0$ for all $i \ne j$.
- Subspace property: $\text{span}\{d_0, \dots, d_k\} = \text{span}\{r_0, \dots, r_k\} = \mathcal{K}_{k+1}(A, r_0)$.

**Convergence Rate Bound:**
$$\|x_k - x^*\|_A \le 2 \left( \frac{\sqrt{\kappa} - 1}{\sqrt{\kappa} + 1} \right)^k \|x_0 - x^*\|_A$$
where $\kappa = \frac{\lambda_{\max}(A)}{\lambda_{\min}(A)}$ is the condition number.
*Comparison:* CG depends on $\sqrt{\kappa}$, while steepest descent depends on $\kappa$. For $\kappa = 100$, steepest descent contracts by $\frac{99}{101} \approx 0.980$, whereas CG contracts by $\frac{\sqrt{100}-1}{\sqrt{100}+1} = \frac{9}{11} \approx 0.818$. CG converges dramatically faster!

### 1.3.4 Coordinate Descent
**Algorithm:** Cycle through coordinates $j = 1, 2, \dots, n$, minimizing $f(x)$ with respect to coordinate $x_j$ while keeping all other coordinates fixed:
$$x_j^{(k+1)} = \arg\min_{z} f(x_1^{(k+1)}, \dots, x_{j-1}^{(k+1)}, z, x_{j+1}^{(k)}, \dots, x_n^{(k)})$$
- **Separable Objectives:** If $f(x) = \sum_{j=1}^n f_j(x_j)$, coordinate descent finds the exact minimizer in **1 single cycle**.
- **Coupled Ill-conditioned Objectives:** When variables are strongly coupled (e.g. cross terms $x_1 x_2$), coordinate descent must take tiny zig-zag steps along coordinate axes, converging slowly.

---

## 1.4 Sparsity-Inducing Penalty Functions

### 1.4.1 Why Sparsity Matters (High Dimensions $N \ll n$)
In modern data science, the number of features $n$ frequently exceeds the sample size $N$ (e.g. $N = 100$ patients, $n = 10,000$ gene expressions). Ordinary Least Squares (OLS) overfits completely, memorizing noise and assigning non-zero weights to all 10,000 features. Sparsity forces most coefficients to be exactly zero, achieving:
1. **Feature selection & interpretability:** Identifies the few truly causal variables.
2. **Generalization:** Prevents overfitting and variance explosion.

### 1.4.2 $L_0$, $L_1$ (LASSO), and $L_2$ (Ridge) Penalties
- **$L_0$ "Norm":** $\|w\|_0 = \sum_{i=1}^n \mathbb{I}(w_i \ne 0)$ (counts non-zero entries).
  - *Problem:* Discontinuous, non-convex. Finding the best $k$-sparse model is NP-hard (requires evaluating $\binom{n}{k}$ combinatorial models).
- **$L_2$ Penalty (Ridge Regression / Tikhonov Regularization):**
  $$\min_w \frac{1}{2} \|X w - y\|_2^2 + \frac{\lambda}{2} \|w\|_2^2$$
  - Closed-form solution: $w_{\text{ridge}} = (X^T X + \lambda I)^{-1} X^T y$.
  - *Limitation:* Shrinks coefficients towards zero, but **never produces exact zeros**.
- **$L_1$ Penalty (LASSO - Least Absolute Shrinkage and Selection Operator):**
  $$\min_w \frac{1}{2} \|X w - y\|_2^2 + \lambda \|w\|_1 \quad \text{where } \|w\|_1 = \sum_{i=1}^n |w_i|$$
  - The $L_1$ norm is the tightest convex relaxation of the $L_0$ norm.
  - **Why $L_1$ produces exact zeros:**
    1. *Geometric View:* The constraint region $\|w\|_1 \le t$ is a diamond/polytope with sharp corners on the coordinate axes. The smooth ellipsoidal contours of the least-squares loss first contact the constraint diamond at one of these sharp corners (where one or more coordinates are exactly zero).
    2. *Subgradient View:* The derivative of $|w_i|$ at zero is the subdifferential interval $[-1, 1]$. If the data gradient is smaller than $\lambda$, the stationarity condition can be satisfied at $w_i = 0$.

### 1.4.3 Subgradients and the Proximal Operator
Because $|w_i|$ is not differentiable at $w_i = 0$, we use subgradients.
- **Subgradient Definition:** A vector $g$ is a subgradient of convex function $f$ at $x$ if:
  $$f(y) \ge f(x) + g^T (y - x) \quad \forall y$$
- **Subdifferential of Absolute Value:**
  $$\partial |x| = \begin{cases} \{+1\} & x > 0 \\ [-1, 1] & x = 0 \\ \{-1\} & x < 0 \end{cases}$$
- **Proximal Operator:** For function $g(x)$, defined as:
  $$\text{prox}_{\gamma g}(v) = \arg\min_x \left( g(x) + \frac{1}{2\gamma} \|x - v\|_2^2 \right)$$
- **Soft-Thresholding Operator (Proximal Operator of $L_1$):**
  For $g(x) = \lambda |x|$, the proximal operator is the soft-thresholding function $\mathcal{S}_{\lambda \gamma}(v)$:
  $$\mathcal{S}_{\tau}(v) = \text{sign}(v) \max(|v| - \tau, 0) = \begin{cases} v - \tau & v > \tau \\ 0 & |v| \le \tau \\ v + \tau & v < -\tau \end{cases}$$

### 1.4.4 Iterative Shrinkage-Thresholding Algorithm (ISTA)
For minimizing $F(w) = f(w) + \lambda \|w\|_1$ where $f(w) = \frac{1}{2}\|X w - y\|_2^2$:
$$w_{k+1} = \mathcal{S}_{\alpha \lambda} \left( w_k - \alpha X^T(X w_k - y) \right)$$
where step size $\alpha < 1/\lambda_{\max}(X^T X)$.
- **FISTA (Fast ISTA):** Incorporates Nesterov momentum, accelerating convergence from $O(1/k)$ to $O(1/k^2)$.

### 1.4.5 Other Sparsity Penalties
- **Elastic Net:** Combines $L_1$ and $L_2$ penalties:
  $$\mathcal{P}_{\text{enet}}(w) = \lambda_1 \|w\|_1 + \frac{\lambda_2}{2} \|w\|_2^2$$
  Overcomes LASSO limitations when features are highly correlated (encourages grouping effect) and handles $n > N$.
- **Group LASSO:** Enforces group-level sparsity: $\sum_{g=1}^G \|w_g\|_2$. Entire groups of features are selected or zeroed out together.
- **SCAD (Smoothly Clipped Absolute Deviation) & MCP (Minimax Concave Penalty):** Non-convex penalties designed to eliminate the estimation bias that $L_1$ imposes on large coefficients.

---

## 1.5 Constrained Convex Optimization and KKT Conditions

### 1.5.1 Standard Form Problem
$$\begin{aligned} \min_{x \in \mathbb{R}^n} \quad & f_0(x) \\ \text{subject to} \quad & f_i(x) \le 0, \quad i = 1, \dots, m \\ & h_j(x) = a_j^T x - b_j = 0, \quad j = 1, \dots, p \end{aligned}$$
where $f_0, f_1, \dots, f_m$ are convex, and equality constraints $h_j$ are affine.

### 1.5.2 The Lagrangian and the Dual Problem
- **Lagrangian Function:**
  $$L(x, \lambda, \nu) = f_0(x) + \sum_{i=1}^m \lambda_i f_i(x) + \sum_{j=1}^p \nu_j h_j(x)$$
  where $\lambda_i \ge 0$ are Lagrange multipliers for inequality constraints, and $\nu_j \in \mathbb{R}$ are multipliers for equality constraints.
- **Lagrange Dual Function:**
  $$g(\lambda, \nu) = \inf_{x} L(x, \lambda, \nu)$$
  *Crucial Fact:* $g(\lambda, \nu)$ is always concave, even if the primal problem is non-convex.
- **Weak Duality:** For any $\lambda \ge 0$ and any $\nu$, $g(\lambda, \nu) \le p^*$ (where $p^*$ is primal optimal value).
- **Strong Duality ($d^* = p^*$):** Holds under **Slater's Condition**:
  There exists a strictly feasible point $\tilde{x}$ such that $f_i(\tilde{x}) < 0$ for all non-affine inequalities, and $A \tilde{x} = b$.

### 1.5.3 Karush-Kuhn-Tucker (KKT) Conditions
For a convex optimization problem with differentiable functions where Slater's condition holds, a point $x^*$ and multipliers $(\lambda^*, \nu^*)$ are optimal if and only if they satisfy the **4 KKT Conditions**:

1. **Stationarity:**
   $$\nabla f_0(x^*) + \sum_{i=1}^m \lambda_i^* \nabla f_i(x^*) + \sum_{j=1}^p \nu_j^* \nabla h_j(x^*) = 0$$
2. **Primal Feasibility:**
   $$f_i(x^*) \le 0 \quad (i = 1, \dots, m), \qquad h_j(x^*) = 0 \quad (j = 1, \dots, p)$$
3. **Dual Feasibility:**
   $$\lambda_i^* \ge 0 \quad (i = 1, \dots, m)$$
4. **Complementary Slackness:**
   $$\lambda_i^* f_i(x^*) = 0 \quad (i = 1, \dots, m)$$

**Physical / Active Set Meaning of Complementary Slackness:**
For each inequality constraint $i$:
- **Case 1: Inactive constraint ($f_i(x^*) < 0$).** The constraint is strictly satisfied in the interior. Complementary slackness forces $\lambda_i^* = 0$. The constraint exerts no force on the optimal solution.
- **Case 2: Active constraint ($f_i(x^*) = 0$).** The solution sits on the boundary. $\lambda_i^* \ge 0$. The multiplier represents the normal force / shadow price preventing the objective from descending further into the forbidden region:
  $$\lambda_i^* = -\frac{\partial p^*}{\partial u_i} \quad \text{where } f_i(x) \le u_i$$

---

## 1.6 Formulating Problems as LP and QP

### 1.6.1 Linear Programming (LP)
An optimization problem where both the objective and all constraints are linear (affine):
- **Standard Form:**
  $$\min_{x} c^T x \quad \text{subject to } A x = b, \ x \ge 0$$
- **Inequality Form:**
  $$\min_{x} c^T x \quad \text{subject to } G x \le h$$
- **Transformation Tricks:**
  - $\max c^T x \iff \min -c^T x$.
  - Free variable $x_j \in \mathbb{R}$: split into $x_j = x_j^+ - x_j^-$ with $x_j^+, x_j^- \ge 0$.
  - Absolute values in objective $\min |x_j|$: introduce $t_j \ge 0$ with $-t_j \le x_j \le t_j$.
  - Inequalities to equalities: add slack variable $s \ge 0$ ($a^T x \le b \iff a^T x + s = b$) or surplus variable ($a^T x \ge b \iff a^T x - s = b$).

### 1.6.2 Quadratic Programming (QP)
An optimization problem where the objective is quadratic and constraints are linear:
$$\min_{x} \frac{1}{2} x^T P x + q^T x \quad \text{subject to } G x \le h, \ A x = b$$
where $P \in \mathbb{S}_+^n$ (symmetric positive semidefinite matrix, ensuring convexity).
- **Markowitz Portfolio Optimization:**
  $$\min_w w^T \Sigma w \quad \text{subject to } \mu^T w = \bar{R}, \ \mathbf{1}^T w = 1, \ w \ge 0$$
- **LASSO converted to QP:**
  Let $w = u - v$ with $u, v \ge 0$:
  $$\min_{u, v} \frac{1}{2} \|X(u - v) - y\|_2^2 + \lambda \mathbf{1}^T(u + v) \quad \text{s.t. } u \ge 0, v \ge 0$$

---

## 1.7 Projected Gradient Descent (PGD) Method

When minimizing a smooth convex function $f(x)$ over a closed convex set $C$:
$$\min_{x \in C} f(x)$$
**Algorithm:**
$$x_{k+1} = \Pi_C \left( x_k - \alpha_k \nabla f(x_k) \right)$$
where $\Pi_C(v)$ is the **Euclidean projection** of vector $v$ onto set $C$:
$$\Pi_C(v) = \arg\min_{x \in C} \|x - v\|_2$$

### Closed-Form Projections for Common Sets:
1. **Non-negative Orthant $\mathbb{R}_+^n = \{x : x \ge 0\}$:**
   $$[\Pi_{\mathbb{R}_+^n}(v)]_i = \max(v_i, 0)$$
2. **Euclidean $\ell_2$-Ball $B(R) = \{x : \|x\|_2 \le R\}$:**
   $$\Pi_{B(R)}(v) = \begin{cases} v & \text{if } \|v\|_2 \le R \\ R \frac{v}{\|v\|_2} & \text{if } \|v\|_2 > R \end{cases}$$
3. **Affine Subspace $\{x : A x = b\}$ (full row rank $A$):**
   $$\Pi(v) = v - A^T (A A^T)^{-1} (A v - b)$$
4. **Probability Simplex $\Delta_n = \{x \in \mathbb{R}^n : x_i \ge 0, \sum_{i=1}^n x_i = 1\}$:**
   Computed via soft-thresholding and sorting: $[\Pi_{\Delta}(v)]_i = \max(v_i - \theta, 0)$ where $\theta$ is chosen so $\sum \max(v_i - \theta, 0) = 1$.
5. **Positive Semidefinite Cone $\mathbb{S}_+^n$:**
   Diagonalize $X = \sum \lambda_i u_i u_i^T$. Project eigenvalues onto $\mathbb{R}_+$:
   $$\Pi_{\mathbb{S}_+^n}(X) = \sum_{i=1}^n \max(\lambda_i, 0) u_i u_i^T$$

---

## 1.8 Support Vector Machines (SVM)

### 1.8.1 Hard-Margin SVM (Linearly Separable Data)
Given training pairs $\{(x_i, y_i)\}_{i=1}^N$ with $x_i \in \mathbb{R}^d$ and $y_i \in \{-1, +1\}$.
Hyperplane: $w^T x + b = 0$. Decision rule: $\hat{y} = \text{sign}(w^T x + b)$.
Margin width between canonical planes $w^T x + b = +1$ and $w^T x + b = -1$ is:
$$\gamma = \frac{2}{\|w\|_2}$$
To maximize the margin $\frac{2}{\|w\|}$, we minimize $\frac{1}{2}\|w\|^2$.

**Primal Problem:**
$$\min_{w, b} \frac{1}{2} \|w\|_2^2 \quad \text{subject to } y_i(w^T x_i + b) \ge 1, \quad i = 1, \dots, N$$

**Derivation of Dual via KKT:**
Lagrangian: $L(w, b, \alpha) = \frac{1}{2}\|w\|^2 - \sum_{i=1}^N \alpha_i [y_i(w^T x_i + b) - 1]$ with $\alpha_i \ge 0$.
- $\nabla_w L = w - \sum_{i=1}^N \alpha_i y_i x_i = 0 \implies w^* = \sum_{i=1}^N \alpha_i y_i x_i$
- $\frac{\partial L}{\partial b} = -\sum_{i=1}^N \alpha_i y_i = 0$
Substituting back into $L$ yields the **Dual SVM Problem**:
$$\max_{\alpha} \sum_{i=1}^N \alpha_i - \frac{1}{2} \sum_{i=1}^N \sum_{j=1}^N \alpha_i \alpha_j y_i y_j (x_i^T x_j) \quad \text{subject to } \alpha_i \ge 0, \ \sum_{i=1}^N \alpha_i y_i = 0$$

**Support Vectors:** Points where $\alpha_i > 0$. By complementary slackness:
$$y_i(w^T x_i + b) = 1$$
These points lie exactly on the margin boundary and completely determine $w^*$ and $b^*$. Points with $\alpha_i = 0$ have no effect on the boundary.

### 1.8.2 Soft-Margin SVM (Non-separable Data)
Introduce slack variables $\xi_i \ge 0$ allowing margin violations:
$$\min_{w, b, \xi} \frac{1}{2} \|w\|_2^2 + C \sum_{i=1}^N \xi_i \quad \text{subject to } y_i(w^T x_i + b) \ge 1 - \xi_i, \ \xi_i \ge 0$$
- **Role of Regularization Parameter $C$:**
  - **Large $C$:** Heavy penalty on misclassifications. Forces narrower margin, very sensitive to outliers, fewer support vectors, risks overfitting.
  - **Small $C$:** Prioritizes wide margin over training accuracy. Tolerates errors, more support vectors, smoother boundary, avoids overfitting.
- **Dual Problem:** Identical to hard-margin dual, except $\alpha_i$ is bounded:
  $$0 \le \alpha_i \le C$$

### 1.8.3 Kernel Trick
Map input $x \mapsto \phi(x)$ into higher-dimensional feature space. Replace inner product $x_i^T x_j$ with kernel function:
$$K(x_i, x_j) = \langle \phi(x_i), \phi(x_j) \rangle$$
- **Linear Kernel:** $K(x, z) = x^T z$
- **Polynomial Kernel:** $K(x, z) = (x^T z + c)^d$
- **Gaussian Radial Basis Function (RBF) Kernel:** $K(x, z) = \exp\left( -\gamma \|x - z\|^2 \right) = \exp\left( -\frac{\|x - z\|^2}{2\sigma^2} \right)$

---

## 1.9 Krylov Subspace Methods

### 1.9.1 Definition and Properties
The $m$-th Krylov subspace generated by matrix $A \in \mathbb{R}^{n \times n}$ and starting vector $b \in \mathbb{R}^n$ is:
$$\mathcal{K}_m(A, b) = \text{span} \{ b, A b, A^2 b, \dots, A^{m-1} b \}$$
- **Polynomial Viewpoint:** Every vector $x \in \mathcal{K}_m(A, b)$ can be expressed as $x = p(A) b$ where $p$ is a polynomial of degree $\le m - 1$.
- **Grade of $b$ with respect to $A$:** The smallest integer $d$ such that $\mathcal{K}_d(A, b) = \mathcal{K}_{d+1}(A, b)$. Then $\dim(\mathcal{K}_m(A, b)) = \min(m, d)$. By Cayley-Hamilton, $d \le n$.

### 1.9.2 The Arnoldi Algorithm
Computes an orthonormal basis $\{q_1, \dots, q_m\}$ of $\mathcal{K}_m(A, b)$ using modified Gram-Schmidt:
1. $q_1 = b / \|b\|_2$
2. For $j = 1, 2, \dots, m$:
   - $v = A q_j$
   - For $i = 1$ to $j$:
     - $h_{i, j} = q_i^T v$
     - $v = v - h_{i, j} q_i$
   - $h_{j+1, j} = \|v\|_2$
   - If $h_{j+1, j} = 0$, stop (invariant subspace reached).
   - $q_{j+1} = v / h_{j+1, j}$

**Fundamental Matrix Relation:**
$$A Q_m = Q_m H_m + h_{m+1, m} q_{m+1} e_m^T = Q_{m+1} \tilde{H}_m$$
where $Q_m = [q_1, \dots, q_m] \in \mathbb{R}^{n \times m}$ has orthonormal columns, and $H_m = Q_m^T A Q_m$ is an $m \times m$ **upper Hessenberg matrix** ($h_{i, j} = 0$ for $i > j + 1$).
- **Ritz Values:** The eigenvalues of $H_m$ approximate the extreme eigenvalues of $A$.

### 1.9.3 Lanczos Algorithm (Symmetric Case $A = A^T$)
When $A$ is symmetric, $H_m = Q_m^T A Q_m$ is symmetric:
$$(Q_m^T A Q_m)^T = Q_m^T A^T Q_m = Q_m^T A Q_m = H_m$$
A matrix that is simultaneously symmetric and upper Hessenberg **must be tridiagonal**:
$$T_m = \begin{pmatrix} \alpha_1 & \beta_1 & & \\ \beta_1 & \alpha_2 & \beta_2 & \\ & \ddots & \ddots & \ddots \\ & & \beta_{m-1} & \alpha_m \end{pmatrix}$$
This reduces the full orthogonalization loop to a **short three-term recurrence**:
$$A q_j = \beta_{j-1} q_{j-1} + \alpha_j q_j + \beta_j q_{j+1}$$
*Advantage:* Only requires storing the previous two vectors!

### 1.9.4 GMRES vs FOM vs CG
- **FOM (Full Orthogonalization Method):** Seeks $x_m \in x_0 + \mathcal{K}_m$ such that residual $r_m \perp \mathcal{K}_m$ (Galerkin condition).
- **GMRES (Generalized Minimal Residual):** Minimizes $\|A x_m - b\|_2$ over $x_m \in x_0 + \mathcal{K}_m$ for general non-symmetric matrices.
  *Memory Scaling:* GMRES requires storing all $m$ Arnoldi basis vectors $q_1, \dots, q_m$. Memory grows linearly $O(m n)$, requiring restarts GMRES($k$).
- **CG:** Works for symmetric positive definite matrices; uses 3-term recurrence, using $O(n)$ fixed memory per iteration.

---

## 1.10 Reproducing Kernel Hilbert Spaces (RKHS) & Random Kitchen Sinks (RKS)

### 1.10.1 Hilbert Space and the Riesz Representation Theorem
- A Hilbert space $\mathcal{H}$ is a complete vector space equipped with an inner product $\langle \cdot, \cdot \rangle_{\mathcal{H}}$.
- **Evaluation Functional:** For $x \in \mathcal{X}$, $L_x(f) = f(x)$.
- **Definition of RKHS:** A Hilbert space of functions where point evaluation $L_x$ is continuous for all $x$.
- **Riesz Representation Theorem:** Continuity implies there exists a unique element $K_x \in \mathcal{H}$ such that:
  $$f(x) = \langle f, K_x \rangle_{\mathcal{H}} \quad \forall f \in \mathcal{H}$$
  The function $K(x, y) = \langle K_x, K_y \rangle_{\mathcal{H}}$ is the **Reproducing Kernel**.

### 1.10.2 The Representer Theorem
For any empirical risk minimization problem with strictly increasing regularizer $g$:
$$\min_{f \in \mathcal{H}} \sum_{i=1}^N L(y_i, f(x_i)) + g(\|f\|_{\mathcal{H}})$$
the optimal solution admits a finite expansion in terms of training points:
$$f^*(x) = \sum_{i=1}^N \alpha_i K(x, x_i)$$
This reduces an infinite-dimensional optimization over $\mathcal{H}$ to finding $N$ coefficients $\alpha \in \mathbb{R}^N$.

### 1.10.3 Random Kitchen Sinks (RKS)
Kernel methods scale as $O(N^2)$ to $O(N^3)$, which is too slow for large $N$.
**Bochner's Theorem:** A continuous shift-invariant kernel $K(x, y) = k(x - y)$ is positive definite if and only if $k(\Delta)$ is the Fourier transform of a non-negative measure $p(\omega)$:
$$k(x - y) = \int_{\mathbb{R}^d} p(\omega) e^{i \omega^T (x - y)} d\omega = \mathbb{E}_\omega [\cos(\omega^T (x - y))]$$
**Rahimi & Recht (2007) Algorithm:**
1. Sample $D$ random frequency vectors $\omega_1, \dots, \omega_D \sim p(\omega)$ (for Gaussian RBF, $p(\omega) \sim \mathcal{N}(0, 2\gamma I)$).
2. Sample $D$ random phase angles $b_1, \dots, b_D \sim \text{Uniform}[0, 2\pi)$.
3. Construct explicit $D$-dimensional randomized feature map:
   $$z(x) = \sqrt{\frac{2}{D}} \begin{pmatrix} \cos(\omega_1^T x + b_1) \\ \vdots \\ \cos(\omega_D^T x + b_D) \end{pmatrix}$$
Then $z(x)^T z(y) \approx K(x, y)$, allowing non-linear kernel problems to be solved via **fast linear solvers in $O(N D)$ time**.

---

## 1.11 Dynamic Mode Decomposition (DMD) & Koopman Operator Theory

### 1.11.1 The Koopman Operator
For a nonlinear dynamical system $x_{k+1} = F(x_k)$, the **Koopman operator** $\mathcal{K}$ acts on observable functions $g(x)$:
$$\mathcal{K} g(x) = g(F(x))$$
$\mathcal{K}$ is **linear** even though $F(x)$ is nonlinear, trading finite-dimensional nonlinear dynamics for an **infinite-dimensional linear system**.

### 1.11.2 SVD-Based Dynamic Mode Decomposition (DMD) Algorithm
Given snapshot data $x_1, x_2, \dots, x_m \in \mathbb{R}^n$ at uniform interval $\Delta t$:
1. Form snapshot matrices:
   $$X = [x_1, x_2, \dots, x_{m-1}], \qquad Y = [x_2, x_3, \dots, x_m]$$
2. Compute thin SVD of $X$:
   $$X \approx U_r \Sigma_r V_r^T$$
   where $r$ is the chosen truncation rank based on singular value decay.
3. Compute the reduced-order evolution matrix:
   $$\tilde{A} = U_r^T Y V_r \Sigma_r^{-1} \in \mathbb{R}^{r \times r}$$
4. Compute eigendecomposition of $\tilde{A}$:
   $$\tilde{A} W = W \Lambda \quad \text{where } \Lambda = \text{diag}(\lambda_1, \dots, \lambda_r)$$
5. Compute exact DMD modes $\Phi$:
   $$\Phi = Y V_r \Sigma_r^{-1} W$$
6. Compute continuous eigenvalues:
   $$\mu_i = \frac{\ln(\lambda_i)}{\Delta t} = \sigma_i + i \omega_i$$
   - Growth/decay rate: $\sigma_i = \text{Re}(\mu_i)$ (decay if $\sigma_i < 0$, growth if $\sigma_i > 0$).
   - Physical frequency: $f_i = \frac{|\text{Im}(\mu_i)|}{2\pi} = \frac{|\omega_i|}{2\pi}$ Hz.
7. Compute mode amplitudes $b = \Phi^\dagger x_1$.
State forecast at any time $t$:
$$x(t) \approx \sum_{i=1}^r b_i \phi_i e^{\mu_i t}$$

---

## 1.12 Tensors and Higher-Order SVD (HOSVD)

### 1.12.1 Tensor Basics
- A tensor $\mathcal{X} \in \mathbb{R}^{I_1 \times I_2 \times \dots \times I_N}$ is an $N$-way multidimensional array.
- **Mode-$n$ Matricization (Unfolding):** Arranges mode-$n$ fibers as columns of a matrix $X_{(n)} \in \mathbb{R}^{I_n \times (\prod_{k \ne n} I_k)}$.
- **Mode-$n$ Product:** Multiplication of tensor $\mathcal{X}$ with matrix $U \in \mathbb{R}^{J \times I_n}$ along mode $n$:
  $$(\mathcal{X} \times_n U)_{i_1 \dots i_{n-1} j i_{n+1} \dots i_N} = \sum_{i_n=1}^{I_n} \mathcal{X}_{i_1 \dots i_n \dots i_N} U_{j, i_n}$$

### 1.12.2 Higher-Order SVD (HOSVD / Tucker Decomposition)
Decomposes tensor $\mathcal{X}$ into a dense core tensor $\mathcal{S}$ multiplied by orthogonal matrices along each mode:
$$\mathcal{X} = \mathcal{S} \times_1 U^{(1)} \times_2 U^{(2)} \dots \times_N U^{(N)}$$
**Algorithm:**
1. For each mode $n = 1, \dots, N$:
   - Form mode-$n$ unfolding matrix $X_{(n)}$.
   - Compute SVD: $X_{(n)} = U^{(n)} \Sigma^{(n)} V^{(n)T}$.
   - The left singular vectors form the mode-$n$ factor matrix $U^{(n)}$.
2. Compute the core tensor by projecting $\mathcal{X}$ onto all factor matrices:
   $$\mathcal{S} = \mathcal{X} \times_1 (U^{(1)})^T \times_2 (U^{(2)})^T \dots \times_N (U^{(N)})^T$$

**Properties of Core Tensor $\mathcal{S}$:**
- **All-orthogonality:** Two slices along the same mode are mutually orthogonal.
- **Ordering:** Slice norms decrease monotonically: $\|S_{i_n = 1}\|_F \ge \|S_{i_n = 2}\|_F \ge \dots$.

---

# Unit II: Partial Differential Equations in Physics and Engineering

## 2.1 Vector Calculus Toolkit for PDEs

Let $\phi(x, y, z)$ be a scalar field and $\mathbf{F} = (F_1, F_2, F_3)$ be a vector field.
- **Del Operator:** $\nabla = \left( \frac{\partial}{\partial x}, \frac{\partial}{\partial y}, \frac{\partial}{\partial z} \right)$.
- **Gradient:** $\nabla \phi = \left( \frac{\partial \phi}{\partial x}, \frac{\partial \phi}{\partial y}, \frac{\partial \phi}{\partial z} \right)$.
  Points in the direction of maximum rate of increase of $\phi$. The directional derivative along unit vector $\mathbf{u}$ is $D_{\mathbf{u}} \phi = \nabla \phi \cdot \mathbf{u}$.
- **Divergence:** $\nabla \cdot \mathbf{F} = \frac{\partial F_1}{\partial x} + \frac{\partial F_2}{\partial y} + \frac{\partial F_3}{\partial z}$.
  Measures outward flux density (net source/sink per unit volume).
- **Curl:** $\nabla \times \mathbf{F} = \det \begin{pmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ \frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\ F_1 & F_2 & F_3 \end{pmatrix}$.
  Measures rotational circulation density.
- **Laplacian:** $\nabla^2 \phi = \nabla \cdot (\nabla \phi) = \frac{\partial^2 \phi}{\partial x^2} + \frac{\partial^2 \phi}{\partial y^2} + \frac{\partial^2 \phi}{\partial z^2}$.
  Measures the difference between the value of $\phi$ at a point and the average value in its infinitesimal neighborhood.

**Fundamental Integral Theorems:**
- **Divergence Theorem (Gauss):**
  $$\iiint_V (\nabla \cdot \mathbf{F}) \, dV = \iint_{\partial V} \mathbf{F} \cdot \mathbf{n} \, dS$$
- **Stokes' Theorem:**
  $$\iint_S (\nabla \times \mathbf{F}) \cdot \mathbf{n} \, dS = \oint_{\partial S} \mathbf{F} \cdot d\mathbf{r}$$

---

## 2.2 Formulation and Classification of PDEs

### 2.2.1 Canonical Physical PDEs
1. **Heat / Diffusion Equation (Parabolic):**
   $$\frac{\partial u}{\partial t} = \alpha \nabla^2 u$$
   *Derivation:* From conservation of thermal energy $\frac{\partial}{\partial t}\iiint \rho c_p u \, dV = -\iint \mathbf{q} \cdot \mathbf{n} \, dS$ and Fourier's Law of conduction $\mathbf{q} = -k \nabla u$.
2. **Wave Equation (Hyperbolic):**
   $$\frac{\partial^2 u}{\partial t^2} = c^2 \nabla^2 u$$
   *Derivation:* From Newton's second law on a flexible elastic string/membrane with tension $T$ and linear density $\rho$, with wave speed $c = \sqrt{T/\rho}$.
3. **Laplace / Poisson Equation (Elliptic):**
   $$\nabla^2 u = 0 \quad \text{(Laplace)}, \qquad \nabla^2 u = f(x, y) \quad \text{(Poisson)}$$
   Describes steady-state heat distribution, electrostatic potential, and gravitational potential.

### 2.2.2 Classification of Second-Order Linear PDEs in 2 Variables
$$A \frac{\partial^2 u}{\partial x^2} + B \frac{\partial^2 u}{\partial x \partial y} + C \frac{\partial^2 u}{\partial y^2} + D \frac{\partial u}{\partial x} + E \frac{\partial u}{\partial y} + F u = G$$
Discriminant: $\Delta = B^2 - 4AC$.
- **Hyperbolic ($\Delta > 0$):** Wave-like propagation, finite speed of information along real characteristics (e.g. Wave equation $u_{tt} - c^2 u_{xx} = 0 \implies B=0, A=1, C=-c^2 \implies \Delta = 4c^2 > 0$).
- **Parabolic ($\Delta = 0$):** Dissipative/diffusive processes, infinite propagation speed, smoothing of discontinuities (e.g. Heat equation $u_t - \alpha u_{xx} = 0 \implies A=-\alpha, B=0, C=0 \implies \Delta = 0$).
- **Elliptic ($\Delta < 0$):** Equilibrium/steady-state processes, no real characteristics, boundary value problems (e.g. Laplace equation $u_{xx} + u_{yy} = 0 \implies A=1, B=0, C=1 \implies \Delta = -4 < 0$).

---

## 2.3 Analytical Methods

### 2.3.1 Method of Characteristics (First-Order PDEs)
For $a(x, y) u_x + b(x, y) u_y = c(x, y, u)$:
Characteristic ODE system:
$$\frac{dx}{a} = \frac{dy}{b} = \frac{du}{c}$$
1. Solve $\frac{dy}{dx} = \frac{b}{a}$ to obtain characteristic curves $\phi(x, y) = C_1$.
2. Solve $\frac{du}{dx} = \frac{c}{a}$ along the curves to find $u$.

### 2.3.2 Separation of Variables
For $u_t = \alpha u_{xx}$ on $0 < x < L$ with $u(0, t) = u(L, t) = 0$ and $u(x, 0) = f(x)$:
1. Assume $u(x, t) = X(x) T(t)$. Substituting into PDE:
   $$\frac{T'(t)}{\alpha T(t)} = \frac{X''(x)}{X(x)} = -\lambda$$
2. Spatial ODE (Sturm-Liouville):
   $$X''(x) + \lambda X(x) = 0, \quad X(0) = 0, \ X(L) = 0$$
   Non-trivial solutions exist only for eigenvalues:
   $$\lambda_n = \left( \frac{n\pi}{L} \right)^2, \quad X_n(x) = \sin\left( \frac{n\pi x}{L} \right), \quad n = 1, 2, 3, \dots$$
3. Temporal ODE:
   $$T_n'(t) + \alpha \lambda_n T_n(t) = 0 \implies T_n(t) = e^{-\alpha \left( \frac{n\pi}{L} \right)^2 t}$$
4. Superposition and Initial Condition:
   $$u(x, t) = \sum_{n=1}^\infty A_n e^{-\alpha \left( \frac{n\pi}{L} \right)^2 t} \sin\left( \frac{n\pi x}{L} \right)$$
   where Fourier coefficients are:
   $$A_n = \frac{2}{L} \int_0^L f(x) \sin\left( \frac{n\pi x}{L} \right) dx$$
*Insight:* Modes with higher $n$ decay exponentially faster with rate proportional to $n^2$.

### 2.3.3 Fourier Transform Method (Infinite Domain $-\infty < x < \infty$)
$$\hat{u}(\omega, t) = \mathcal{F}\{u(x, t)\} = \int_{-\infty}^\infty u(x, t) e^{-i \omega x} dx$$
Properties: $\mathcal{F}\{u_x\} = i\omega \hat{u}$, $\mathcal{F}\{u_{xx}\} = -\omega^2 \hat{u}$.
- **Advection Equation $u_t + c u_x = 0$:**
  $$\frac{\partial \hat{u}}{\partial t} + i c \omega \hat{u} = 0 \implies \hat{u}(\omega, t) = \hat{u}(\omega, 0) e^{-i c \omega t}$$
  By Fourier shift theorem $\mathcal{F}^{-1}\{\hat{f}(\omega) e^{-i \omega a}\} = f(x - a)$:
  $$u(x, t) = f(x - c t) \quad \text{(Wave travelling right with speed } c\text{)}$$
- **Heat Equation $u_t = \alpha u_{xx}$:**
  $$\frac{\partial \hat{u}}{\partial t} = -\alpha \omega^2 \hat{u} \implies \hat{u}(\omega, t) = \hat{u}(\omega, 0) e^{-\alpha \omega^2 t}$$
  High frequencies $\omega$ decay at rate $e^{-\alpha \omega^2 t}$, acting as a low-pass filter.

---

## 2.4 Numerical Finite Difference Methods (FDM)

Grid spacing: spatial step $h = \Delta x$, time step $k = \Delta t$.
Mesh points: $x_i = i h$, $t_n = n k$, approximate value $u_i^n \approx u(x_i, t_n)$.

### 2.4.1 Derivative Approximations
- **Forward difference:** $\frac{\partial u}{\partial t}\Big|_i^n = \frac{u_i^{n+1} - u_i^n}{k} + O(k)$
- **Backward difference:** $\frac{\partial u}{\partial t}\Big|_i^n = \frac{u_i^n - u_i^{n-1}}{k} + O(k)$
- **Central difference (spatial):** $\frac{\partial^2 u}{\partial x^2}\Big|_i^n = \frac{u_{i+1}^n - 2u_i^n + u_{i-1}^n}{h^2} + O(h^2)$

### 2.4.2 Explicit FTCS Scheme for the Heat Equation
$$\frac{u_i^{n+1} - u_i^n}{k} = \alpha \frac{u_{i+1}^n - 2u_i^n + u_{i-1}^n}{h^2}$$
Let $r = \frac{\alpha k}{h^2}$ (mesh Fourier number). The explicit update equation is:
$$u_i^{n+1} = r u_{i-1}^n + (1 - 2r) u_i^n + r u_{i+1}^n$$
- **von Neumann Stability Analysis:**
  Substitute Fourier mode $u_i^n = G^n e^{i \beta i h}$ into update equation:
  $$G = 1 - 2r + 2r \cos(\beta h) = 1 - 4r \sin^2\left( \frac{\beta h}{2} \right)$$
  For stability, we require $|G| \le 1$ for all $\beta h \in [0, \pi]$:
  $$-1 \le 1 - 4r \sin^2\left( \frac{\beta h}{2} \right) \le 1 \implies 4r \le 2 \implies r = \frac{\alpha k}{h^2} \le \frac{1}{2}$$
- **Physical / Maximum Principle Interpretation:**
  When $r \le 1/2$, the weights $(r, 1-2r, r)$ are all non-negative and sum to 1. The new value $u_i^{n+1}$ is a **convex weighted average** of its neighbors, guaranteeing that the numerical solution satisfies the discrete maximum principle (no spurious oscillations). If $r > 1/2$, the center weight becomes negative, causing catastrophic, explosive oscillations.

### 2.4.3 Implicit BTCS & Crank-Nicolson Schemes
- **BTCS (Backward Time Central Space):**
  $$\frac{u_i^{n+1} - u_i^n}{k} = \alpha \frac{u_{i+1}^{n+1} - 2u_i^{n+1} + u_{i-1}^{n+1}}{h^2}$$
  $$-r u_{i-1}^{n+1} + (1 + 2r) u_i^{n+1} - r u_{i+1}^{n+1} = u_i^n$$
  **Unconditionally stable** for any $r > 0$. Requires solving a tridiagonal linear system at each time step using the $O(N)$ **Thomas Algorithm (TDMA)**. Truncation error: $O(k + h^2)$.
- **Crank-Nicolson Scheme:**
  Averages explicit FTCS and implicit BTCS at time level $n + 1/2$:
  $$\frac{u_i^{n+1} - u_i^n}{k} = \frac{\alpha}{2} \left( \frac{u_{i+1}^{n+1} - 2u_i^{n+1} + u_{i-1}^{n+1}}{h^2} + \frac{u_{i+1}^n - 2u_i^n + u_{i-1}^n}{h^2} \right)$$
  $$-\frac{r}{2} u_{i-1}^{n+1} + (1 + r) u_i^{n+1} - \frac{r}{2} u_{i+1}^{n+1} = \frac{r}{2} u_{i-1}^n + (1 - r) u_i^n + \frac{r}{2} u_{i+1}^n$$
  - **Properties:** Unconditionally stable, second-order accurate in both time and space: $O(k^2 + h^2)$.

### 2.4.4 Explicit Scheme for the Wave Equation ($u_{tt} = c^2 u_{xx}$)
$$\frac{u_i^{n+1} - 2u_i^n + u_i^{n-1}}{k^2} = c^2 \frac{u_{i+1}^n - 2u_i^n + u_{i-1}^n}{h^2}$$
Let Courant number $C = \frac{c k}{h}$.
$$u_i^{n+1} = 2(1 - C^2) u_i^n + C^2 (u_{i+1}^n + u_{i-1}^n) - u_i^{n-1}$$
- **Courant-Friedrichs-Lewy (CFL) Stability Condition:**
  $$C = \frac{c \Delta t}{\Delta x} \le 1$$
  *Physical Meaning:* The numerical domain of dependence must contain the physical domain of dependence (the time step $\Delta t$ cannot exceed the time it takes for a wave to travel between adjacent grid points).

### 2.4.5 Elliptic PDEs (Laplace / Poisson) and Iterative Relaxation
Discretizing $\nabla^2 u = u_{xx} + u_{yy} = 0$ on uniform grid $\Delta x = \Delta y = h$:
$$u_{i+1, j} + u_{i-1, j} + u_{i, j+1} + u_{i, j-1} - 4 u_{i, j} = 0 \implies u_{i, j} = \frac{1}{4} (u_{i+1, j} + u_{i-1, j} + u_{i, j+1} + u_{i, j-1})$$
- **Jacobi Iteration:**
  $$u_{i, j}^{(k+1)} = \frac{1}{4} \left( u_{i+1, j}^{(k)} + u_{i-1, j}^{(k)} + u_{i, j+1}^{(k)} + u_{i, j-1}^{(k)} \right)$$
- **Gauss-Seidel Iteration:** Uses newly updated values immediately:
  $$u_{i, j}^{(k+1)} = \frac{1}{4} \left( u_{i+1, j}^{(k)} + u_{i-1, j}^{(k+1)} + u_{i, j+1}^{(k)} + u_{i, j-1}^{(k+1)} \right)$$
- **Successive Over-Relaxation (SOR):**
  $$u_{i, j}^{(k+1)} = (1 - \omega) u_{i, j}^{(k)} + \frac{\omega}{4} \left( u_{i-1, j}^{(k+1)} + u_{i+1, j}^{(k)} + u_{i, j-1}^{(k+1)} + u_{i, j+1}^{(k)} \right)$$
  where $\omega \in (1, 2)$ is the over-relaxation factor that accelerates convergence.

---

# Unit III: Multivariate Gaussians, Weighted Least Squares, Markov Chains, and MDP

## 3.1 Multivariate Gaussian Distributions

### 3.1.1 Probability Density Function (PDF)
A random vector $X = (X_1, \dots, X_n)^T \in \mathbb{R}^n$ follows a multivariate Gaussian distribution $X \sim \mathcal{N}(\mu, \Sigma)$ with mean vector $\mu \in \mathbb{R}^n$ and covariance matrix $\Sigma \in \mathbb{S}_{++}^n$ if:
$$p(x) = \frac{1}{(2\pi)^{n/2} |\Sigma|^{1/2}} \exp\left( -\frac{1}{2} (x - \mu)^T \Sigma^{-1} (x - \mu) \right)$$

### 3.1.2 Geometry & Mahalanobis Distance
The quadratic form in the exponent defines the squared **Mahalanobis Distance**:
$$D_M^2(x, \mu) = (x - \mu)^T \Sigma^{-1} (x - \mu)$$
- **Contours of Equal Probability Density:** Ellipsoids given by $(x - \mu)^T \Sigma^{-1} (x - \mu) = c^2$.
- **Principal Axes:** Eigendecomposition $\Sigma = V \Lambda V^T$. The principal axes of the ellipsoids align with the eigenvectors $v_i$ of $\Sigma$, with semi-axis lengths proportional to $\sqrt{\lambda_i}$.
- **Uncorrelated vs Independent:** For general distributions, uncorrelated does not imply independent. However, **for jointly Gaussian variables, zero correlation (diagonal $\Sigma$) is equivalent to statistical independence**.

### 3.1.3 Marginal and Conditional Distributions (Schur Complement)
Partition $X = \begin{pmatrix} X_1 \\ X_2 \end{pmatrix}$, $\mu = \begin{pmatrix} \mu_1 \\ \mu_2 \end{pmatrix}$, $\Sigma = \begin{pmatrix} \Sigma_{11} & \Sigma_{12} \\ \Sigma_{21} & \Sigma_{22} \end{pmatrix}$.
1. **Marginal Distribution:**
   $$X_1 \sim \mathcal{N}(\mu_1, \Sigma_{11}), \qquad X_2 \sim \mathcal{N}(\mu_2, \Sigma_{22})$$
   (Simply extract the corresponding subvector and submatrix).
2. **Conditional Distribution:** Given observation $X_2 = x_2$, the conditional distribution $X_1 \mid X_2 = x_2$ is also Gaussian:
   $$X_1 \mid X_2 = x_2 \sim \mathcal{N}(\mu_{1|2}, \Sigma_{1|2})$$
   where:
   - **Conditional Mean:**
     $$\mu_{1|2} = \mu_1 + \Sigma_{12} \Sigma_{22}^{-1} (x_2 - \mu_2)$$
   - **Conditional Covariance (Schur Complement of $\Sigma_{22}$ in $\Sigma$):**
     $$\Sigma_{1|2} = \Sigma_{11} - \Sigma_{12} \Sigma_{22}^{-1} \Sigma_{21}$$
   *Key Takeaway:* The conditional mean shifts linearly based on the deviation $(x_2 - \mu_2)$, while the conditional covariance is strictly reduced (information gained) and **does not depend on the observed value $x_2$**.

---

## 3.2 Weighted Least Squares (WLS)

### 3.2.1 Motivation: Heteroscedastic Noise
Ordinary Least Squares (OLS) assumes errors are homoscedastic (constant variance $\sigma^2$). In real sensor networks and experimental measurements, different observations have different measurement uncertainties:
$$y_i = x_i^T \beta + \epsilon_i, \quad \mathbb{E}[\epsilon_i] = 0, \quad \text{Var}(\epsilon_i) = \sigma_i^2$$
Observations with high uncertainty (large $\sigma_i^2$) contain less information and should have less influence on the parameter estimate. The optimal weights are:
$$w_i = \frac{1}{\sigma_i^2}$$

### 3.2.2 Objective and Normal Equations
$$J(\beta) = \sum_{i=1}^N w_i (y_i - x_i^T \beta)^2 = (y - X \beta)^T W (y - X \beta)$$
where $W = \text{diag}(w_1, w_2, \dots, w_N)$.
Setting gradient $\nabla_\beta J(\beta) = -2 X^T W (y - X \beta) = 0$ yields the **Weighted Normal Equations**:
$$(X^T W X) \beta = X^T W y$$
$$\hat{eta}_{\text{WLS}} = (X^T W X)^{-1} X^T W y$$

### 3.2.3 Equivalence to Rescaled OLS
Since $W$ is positive diagonal, factor $W = D^2 = D^T D$ where $D = \text{diag}(\sqrt{w_1}, \dots, \sqrt{w_N})$.
Then:
$$J(\beta) = \|D(y - X \beta)\|_2^2 = \|\tilde{y} - \tilde{X}\beta\|_2^2 \quad \text{where } \tilde{y} = D y, \ \tilde{X} = D X$$
Thus, WLS is equivalent to applying ordinary least squares to data rescaled by $\sqrt{w_i}$.
By the **Gauss-Markov Theorem**, $\hat{eta}_{\text{WLS}}$ is the Best Linear Unbiased Estimator (BLUE).

---

## 3.3 Discrete-Time Markov Chains (DTMC)

### 3.3.1 Definition & Transition Matrix
A sequence of discrete random variables $X_0, X_1, X_2, \dots$ taking values in finite state space $S = \{1, 2, \dots, M\}$ satisfies the **Markov Property** if:
$$P(X_{n+1} = j \mid X_n = i, X_{n-1} = i_{n-1}, \dots, X_0 = i_0) = P(X_{n+1} = j \mid X_n = i) = P_{ij}$$
The $M \times M$ transition matrix $P = [P_{ij}]$ is **row-stochastic**:
$$P_{ij} \ge 0, \qquad \sum_{j=1}^M P_{ij} = 1 \quad \forall i$$

### 3.3.2 Multi-Step Transitions & State Distribution
- **Chapman-Kolmogorov Equations:** $P(X_{n+m} = j \mid X_0 = i) = (P^m)_{ij}$.
- **Distribution Evolution:** Let $\pi^{(n)} = [P(X_n = 1), \dots, P(X_n = M)]$ be the row vector of state probabilities at step $n$:
  $$\pi^{(n)} = \pi^{(0)} P^n$$

### 3.3.3 Stationary Distribution
A probability row vector $\pi = (\pi_1, \dots, \pi_M)$ is stationary if:
$$\pi P = \pi \quad \text{subject to} \quad \sum_{i=1}^M \pi_i = 1, \ \pi_i \ge 0$$
- $\pi$ is a left eigenvector of $P$ corresponding to eigenvalue $\lambda = 1$.
- **Ergodic Theorem:** If the Markov chain is irreducible (any state can be reached from any other state) and aperiodic (returns are not confined to multiples of an integer $> 1$), then:
  $$\lim_{n \to \infty} \pi^{(n)} = \pi \quad \text{regardless of initial distribution } \pi^{(0)}$$
  The system forgets its initial condition.

---

## 3.4 Markov Decision Processes (MDP) and Dynamic Programming

### 3.4.1 Formal Framework
An MDP is a 5-tuple $(\mathcal{S}, \mathcal{A}, \mathcal{P}, \mathcal{R}, \gamma)$:
- $\mathcal{S}$: Set of states.
- $\mathcal{A}$: Set of actions.
- $\mathcal{P}$: Transition probability function $\mathcal{P}(s' \mid s, a) = P(S_{t+1} = s' \mid S_t = s, A_t = a)$.
- $\mathcal{R}$: Reward function $\mathcal{R}(s, a) = \mathbb{E}[R_{t+1} \mid S_t = s, A_t = a]$.
- $\gamma \in [0, 1)$: Discount factor (ensures infinite-horizon sums converge and models time preference).

### 3.4.2 Policies, Returns, and Value Functions
- **Policy $\pi(a \mid s)$:** Probability of choosing action $a$ in state $s$.
- **Discounted Return:** $G_t = \sum_{k=0}^\infty \gamma^k R_{t+k+1}$.
- **State-Value Function $V^\pi(s)$:** Expected return starting from state $s$ following policy $\pi$:
  $$V^\pi(s) = \mathbb{E}_\pi [G_t \mid S_t = s]$$
- **Action-Value Function $Q^\pi(s, a)$:** Expected return taking action $a$ in state $s$, then following $\pi$:
  $$Q^\pi(s, a) = \mathbb{E}_\pi [G_t \mid S_t = s, A_t = a] = \mathcal{R}(s, a) + \gamma \sum_{s'} \mathcal{P}(s' \mid s, a) V^\pi(s')$$

### 3.4.3 Bellman Equations
1. **Bellman Expectation Equation for $V^\pi$:**
   $$V^\pi(s) = \sum_{a \in \mathcal{A}} \pi(a \mid s) \left[ \mathcal{R}(s, a) + \gamma \sum_{s' \in \mathcal{S}} \mathcal{P}(s' \mid s, a) V^\pi(s') \right]$$
   In matrix form for deterministic policy: $V^\pi = R^\pi + \gamma P^\pi V^\pi \implies V^\pi = (I - \gamma P^\pi)^{-1} R^\pi$.
2. **Bellman Optimality Equation:**
   $$V^*(s) = \max_{a \in \mathcal{A}} \left[ \mathcal{R}(s, a) + \gamma \sum_{s' \in \mathcal{S}} \mathcal{P}(s' \mid s, a) V^*(s') \right]$$

### 3.4.4 Dynamic Programming Algorithms
- **Value Iteration:**
  $$V_{k+1}(s) = \max_{a \in \mathcal{A}} \left[ \mathcal{R}(s, a) + \gamma \sum_{s'} \mathcal{P}(s' \mid s, a) V_k(s') \right]$$
  By the **Banach Fixed-Point Theorem**, the Bellman optimality backup is a $\gamma$-contraction mapping in the $\ell_\infty$ norm:
  $$\|V_{k+1} - V^*\|_\infty \le \gamma \|V_k - V^*\|_\infty$$
  Guaranteed to converge geometrically to the unique optimal value function $V^*$.
- **Policy Iteration:**
  1. *Policy Evaluation:* Solve $(I - \gamma P^{\pi_k}) V^{\pi_k} = R^{\pi_k}$.
  2. *Policy Improvement:* $\pi_{k+1}(s) = \arg\max_{a} \left[ \mathcal{R}(s, a) + \gamma \sum_{s'} \mathcal{P}(s' \mid s, a) V^{\pi_k}(s') \right]$.
  Converges to optimal policy $\pi^*$ in a finite number of iterations.

---

# Unit IV: Introduction to Quantum Computing, Bell's Inequality, and Quantum Gates

## 4.1 Mathematical Foundations of Quantum Information

### 4.1.1 Qubit State Space and Dirac Bra-Ket Notation
A classical bit takes values in $\{0, 1\}$. A quantum bit (qubit) is a two-dimensional complex Hilbert space $\mathbb{C}^2$.
- **Computational Basis:**
  $$|0\rangle = \begin{pmatrix} 1 \\ 0 \end{pmatrix}, \qquad |1\rangle = \begin{pmatrix} 0 \\ 1 \end{pmatrix}$$
- **General Qubit State (Ket):**
  $$|\psi\rangle = a |0\rangle + b |1\rangle = \begin{pmatrix} a \\ b \end{pmatrix}, \quad a, b \in \mathbb{C}$$
- **Normalization (Total Probability = 1):**
  $$\langle\psi|\psi\rangle = |a|^2 + |b|^2 = 1$$
- **Dual Vector (Bra):** $\langle\psi| = |\psi\rangle^\dagger = (\bar{a}, \bar{b})$ (conjugate transpose).
- **Inner Product (Scalar):** $\langle\phi|\psi\rangle = \bar{c} a + \bar{d} b \in \mathbb{C}$.
- **Outer Product (Operator / Matrix):**
  $$|\psi\rangle\langle\phi| = \begin{pmatrix} a \\ b \end{pmatrix} \begin{pmatrix} \bar{c} & \bar{d} \end{pmatrix} = \begin{pmatrix} a\bar{c} & a\bar{d} \\ b\bar{c} & b\bar{d} \end{pmatrix}$$
- **Completeness Relation:** $|0\rangle\langle 0| + |1\rangle\langle 1| = \begin{pmatrix} 1 & 0 \\ 0 & 0 \end{pmatrix} + \begin{pmatrix} 0 & 0 \\ 0 & 1 \end{pmatrix} = I_2$.

### 4.1.2 The Bloch Sphere
Every single-qubit pure state can be written (up to unmeasurable global phase) as:
$$|\psi\rangle = \cos\left(\frac{\theta}{2}\right) |0\rangle + e^{i \phi} \sin\left(\frac{\theta}{2}\right) |1\rangle$$
where $\theta \in [0, \pi]$ is the polar angle and $\phi \in [0, 2\pi)$ is the azimuthal phase angle.
- **North Pole ($\theta = 0$):** $|0\rangle$
- **South Pole ($\theta = \pi$):** $|1\rangle$
- **Equator ($\theta = \pi/2$):**
  - $\phi = 0 \implies |+\rangle = \frac{|0\rangle + |1\rangle}{\sqrt{2}}$ ($+x$ axis)
  - $\phi = \pi \implies |-\rangle = \frac{|0\rangle - |1\rangle}{\sqrt{2}}$ ($-x$ axis)
  - $\phi = \pi/2 \implies |+i\rangle = \frac{|0\rangle + i|1\rangle}{\sqrt{2}}$ ($+y$ axis)
  - $\phi = 3\pi/2 \implies |-i\rangle = \frac{|0\rangle - i|1\rangle}{\sqrt{2}}$ ($-y$ axis)

---

## 4.2 Physical Realization: Electron Spin-1/2 and Pauli Operators

The intrinsic angular momentum (spin) of an electron forms a physical qubit: spin-up along $z$ is $|0\rangle$, spin-down along $z$ is $|1\rangle$.
The spin operators are $\hat{S}_k = \frac{\hbar}{2} \sigma_k$, where $\sigma_k$ are the **Pauli Matrices**:
$$\sigma_x = X = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}, \qquad \sigma_y = Y = \begin{pmatrix} 0 & -i \\ i & 0 \end{pmatrix}, \qquad \sigma_z = Z = \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}$$
**Pauli Properties:**
- Hermitian: $X = X^\dagger, Y = Y^\dagger, Z = Z^\dagger$.
- Unitary: $X^2 = Y^2 = Z^2 = I$.
- Eigenvalues: $\pm 1$.
- Anti-commutation: $X Y = i Z = -Y X$.
- **Stern-Gerlach Experiment:** Inhomogeneous magnetic field $\mathbf{B}$ splits an atomic beam into discrete spatial beams corresponding to eigenvalues $\pm \hbar/2$, proving spatial quantization of angular momentum.

---

## 4.3 Superposition, Bases, and Global vs Relative Phase

### 4.3.1 Superposition is Basis-Dependent
- State $|+\rangle = \frac{|0\rangle + |1\rangle}{\sqrt{2}}$ is in an equal superposition of computational basis states $\{|0\rangle, |1\rangle\}$.
- However, with respect to the $X$-basis $\{|+\rangle, |-\rangle\}$, $|+\rangle$ is an **eigenstate with definite eigenvalue $+1$** (no superposition).

### 4.3.2 Global Phase vs Relative Phase
- **Global Phase:** $|\psi'\rangle = e^{i \theta} |\psi\rangle$.
  For any observable $A$: $\langle \psi' | A | \psi' \rangle = e^{-i \theta} e^{i \theta} \langle \psi | A | \psi \rangle = \langle \psi | A | \psi \rangle$.
  Measurement probabilities in *any* basis are identical: $|\langle m | e^{i \theta} \psi \rangle|^2 = |e^{i \theta}|^2 |\langle m | \psi \rangle|^2 = |\langle m | \psi \rangle|^2$. **Global phase has zero physical effect and cannot be detected.**
- **Relative Phase:** $|\psi\rangle = \frac{|0\rangle + e^{i \phi}|1\rangle}{\sqrt{2}}$.
  Changing $\phi$ rotates the state around the equator of the Bloch sphere.
  - In computational basis: $P(0) = 1/2, P(1) = 1/2$ for all $\phi$.
  - In $X$-basis: $P(+) = |\langle + | \psi \rangle|^2 = \left| \frac{1 + e^{i \phi}}{2} \right|^2 = \cos^2(\phi/2)$.
  **Relative phase creates constructive and destructive quantum interference and is physically measurable.**

---

## 4.4 Quantum Measurement, Born's Rule, and State Collapse

### 4.4.1 Born's Rule
When measuring state $|\psi\rangle = a|0\rangle + b|1\rangle$ in the orthonormal basis $\{|m_i\rangle\}$:
1. The measurement yields outcome $m_i$ with probability:
   $$P(m_i) = |\langle m_i | \psi \rangle|^2 = \langle \psi | P_{m_i} | \psi \rangle$$
   where $P_{m_i} = |m_i\rangle\langle m_i|$ is the projection operator.
2. Total probability is conserved: $\sum_i P(m_i) = \sum_i \langle \psi | |m_i\rangle\langle m_i| \psi \rangle = \langle \psi | I | \psi \rangle = 1$.

### 4.4.2 State Collapse
Immediately upon obtaining outcome $m_k$, the state **collapses discontinuously and irreversibly** to the corresponding basis state:
$$|\psi\rangle \xrightarrow{\text{measurement}} |m_k\rangle$$
If measured again immediately in the same basis, the probability of getting outcome $m_k$ is $100\%$.

### 4.4.3 Comparison: Unitary Evolution vs Measurement
| Property | Unitary Evolution ($U$) | Measurement ($P_m$) |
|---|---|---|
| **Determinism** | Deterministic: $|\psi(t)\rangle = e^{-iHt/\hbar}|\psi(0)\rangle$ | Probabilistic: outcome according to Born rule |
| **Reversibility** | Reversible: $U^{-1} = U^\dagger$ | Irreversible: collapse destroys superposition |
| **Linearity** | Linear: $U(a|\psi\rangle + b|\phi\rangle) = a U|\psi\rangle + b U|\phi\rangle$ | Non-linear: projection and re-normalization |

### 4.4.4 The No-Cloning Theorem
*Theorem:* There is no quantum operation (unitary $U$) that can create an identical copy of an arbitrary unknown quantum state $|\psi\rangle$.
*Proof:* Suppose such a unitary $U$ exists:
$$U (|\psi\rangle |0\rangle) = |\psi\rangle |\psi\rangle \quad \text{and} \quad U (|\phi\rangle |0\rangle) = |\phi\rangle |\phi\rangle$$
Take inner product between these two equations:
$$\langle \psi | \langle 0 | U^\dagger U | \phi \rangle | 0 \rangle = \langle \psi | \langle \psi | \phi \rangle | \phi \rangle$$
Since $U^\dagger U = I$ and $\langle 0 | 0 \rangle = 1$:
$$\langle \psi | \phi \rangle = (\langle \psi | \phi \rangle)^2$$
This requires $\langle \psi | \phi \rangle = 0$ or $\langle \psi | \phi \rangle = 1$.
Thus, cloning is possible only if the states are orthogonal (like classical bits 0 and 1). **An arbitrary unknown quantum superposition cannot be cloned.**

---

## 4.5 Multi-Qubit Systems, Tensor Products, and Entanglement

### 4.5.1 Composite State Space
For an $n$-qubit system, the state space is the tensor product of single-qubit spaces:
$$\mathcal{H} = \mathbb{C}^2 \otimes \mathbb{C}^2 \otimes \dots \otimes \mathbb{C}^2 = (\mathbb{C}^2)^{\otimes n} \cong \mathbb{C}^{2^n}$$
A state of $n$ qubits is a linear combination of $2^n$ basis vectors:
$$|\psi\rangle = \sum_{x \in \{0, 1\}^n} c_x |x\rangle, \quad \sum_{x} |c_x|^2 = 1$$
Classical simulation requires storing and updating $2^n$ complex numbers (at $n=50$, $2^{50} \approx 10^{15}$ amplitudes $\approx$ petabytes of RAM; at $n=300$, $2^{300}$ exceeds the number of atoms in the observable universe).

### 4.5.2 Product States vs Entangled States
- **Product (Separable) State:** A 2-qubit state $|\psi\rangle$ that can be factored as:
  $$|\psi\rangle = |\psi_A\rangle \otimes |\psi_B\rangle = (a_0 |0\rangle + a_1 |1\rangle) \otimes (b_0 |0\rangle + b_1 |1\rangle) = a_0 b_0 |00\rangle + a_0 b_1 |01\rangle + a_1 b_0 |10\rangle + a_1 b_1 |11\rangle$$
  *Non-entanglement Test for state $c_{00}|00\rangle + c_{01}|01\rangle + c_{10}|10\rangle + c_{11}|11\rangle$:*
  $$c_{00} c_{11} - c_{01} c_{10} = 0$$
- **Entangled State:** A state that **cannot** be factored into individual qubit states. For example, in the state:
  $$|\Phi^+\rangle = \frac{|00\rangle + |11\rangle}{\sqrt{2}}$$
  Here $c_{00} = 1/\sqrt{2}, c_{01} = 0, c_{10} = 0, c_{11} = 1/\sqrt{2}$. The determinant is $c_{00} c_{11} - c_{01} c_{10} = 1/2 \ne 0$. Thus $|\Phi^+\rangle$ is **maximally entangled**.

### 4.5.3 The Four Bell States (Maximally Entangled Basis)
$$\begin{aligned} |\Phi^+\rangle &= \frac{|00\rangle + |11\rangle}{\sqrt{2}}, \qquad &|\Phi^-\rangle &= \frac{|00\rangle - |11\rangle}{\sqrt{2}} \\ |\Psi^+\rangle &= \frac{|01\rangle + |10\rangle}{\sqrt{2}}, \qquad &|\Psi^-\rangle &= \frac{|01\rangle - |10\rangle}{\sqrt{2}} \end{aligned}$$
*Measurement Correlations on $|\Phi^+\rangle$:* Measuring qubit A in the computational basis gives 0 or 1 each with probability 50%. But immediately upon measuring qubit A as 0 (or 1), qubit B is guaranteed to collapse to 0 (or 1) with 100% certainty, even if separated across galaxies!

---

## 4.6 Bell's Inequality and the CHSH Test

### 4.6.1 Local Realism vs Quantum Mechanics
- **Realism:** Physical systems possess definite objective values before measurement.
- **Locality (Einstein Locality):** Measurements at space-like separation cannot influence each other faster than light.
- **Local Hidden Variable (LHV) Model:** Assumes an underlying parameter $\lambda$ determines measurement outcomes $A(a, \lambda) = \pm 1$ and $B(b, \lambda) = \pm 1$.

### 4.6.2 The CHSH Inequality (Clauser-Horne-Shimony-Holt)
Alice chooses measurement settings $A$ or $A'$; Bob chooses settings $B$ or $B'$. All outcomes are $\pm 1$.
Consider the identity for numbers $A, A', B, B' \in \{-1, +1\}$:
$$A B + A B' + A' B - A' B' = A(B + B') + A'(B - B')$$
Since $B, B' \in \{-1, +1\}$, one of $(B + B')$ or $(B - B')$ must be $\pm 2$ while the other is 0. Thus:
$$|A B + A B' + A' B - A' B'| \le 2$$
Taking the expectation over hidden variable distribution $p(\lambda)$ gives the **CHSH Inequality (Classical Bound)**:
$$|S| = |\mathbb{E}(A B) + \mathbb{E}(A B') + \mathbb{E}(A' B) - \mathbb{E}(A' B')| \le 2$$

### 4.6.3 Quantum Mechanical Violation (Tsirelson's Bound)
Using the entangled Bell state $|\Phi^+\rangle$ and measuring along angles:
Alice: $A = 0^\circ, A' = 90^\circ$; Bob: $B = 45^\circ, B' = -45^\circ$.
The quantum correlation is $\langle A B \rangle = \cos(2(\theta_A - \theta_B))$:
- $\mathbb{E}(A B) = \cos(-45^\circ) = \frac{\sqrt{2}}{2}$
- $\mathbb{E}(A B') = \cos(45^\circ) = \frac{\sqrt{2}}{2}$
- $\mathbb{E}(A' B) = \cos(45^\circ) = \frac{\sqrt{2}}{2}$
- $\mathbb{E}(A' B') = \cos(135^\circ) = -\frac{\sqrt{2}}{2}$
Evaluating the CHSH correlator:
$$S_{\text{quantum}} = \frac{\sqrt{2}}{2} + \frac{\sqrt{2}}{2} + \frac{\sqrt{2}}{2} - \left(-\frac{\sqrt{2}}{2}\right) = 4 \times \frac{\sqrt{2}}{2} = 2\sqrt{2} \approx 2.828 > 2$$
- $2\sqrt{2}$ is the maximum possible quantum correlation (**Tsirelson's Bound**).
- **Physical Meaning:** Rules out all local hidden variable theories. Nature is fundamentally non-classical.
- **No-Signaling Theorem:** This violation cannot transmit messages faster than light. Alice's local reduced density matrix $\rho_A = \text{Tr}_B(|\Phi^+\rangle\langle\Phi^+|) = \frac{1}{2}I_2$ is identical regardless of Bob's measurement setting.

---

## 4.7 Quantum Gates, Circuits, Reversibility, and Universality

### 4.7.1 What Makes a Matrix a Valid Quantum Gate?
Every quantum gate representing closed-system evolution must be a **Unitary Matrix**:
$$U^\dagger U = U U^\dagger = I$$
*Why Unitary?*
1. Preserves state normalization: $\|U|\psi\rangle\|^2 = \langle \psi | U^\dagger U | \psi \rangle = \langle \psi | \psi \rangle = 1$ (probabilities always sum to 1).
2. Guarantees **reversibility**: every quantum operation can be run backward via $U^\dagger = U^{-1}$.
3. Preserves inner products / orthogonality: $\langle U \phi | U \psi \rangle = \langle \phi | \psi \rangle$.

### 4.7.2 Single-Qubit Gates
- **Pauli-X (NOT gate, bit flip):**
  $$X = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}, \quad X|0\rangle = |1\rangle, \ X|1\rangle = |0\rangle$$
- **Pauli-Y (bit and phase flip):**
  $$Y = \begin{pmatrix} 0 & -i \\ i & 0 \end{pmatrix}, \quad Y|0\rangle = i|1\rangle, \ Y|1\rangle = -i|0\rangle$$
- **Pauli-Z (phase flip):**
  $$Z = \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}, \quad Z|0\rangle = |0\rangle, \ Z|1\rangle = -|1\rangle$$
- **Hadamard Gate $H$ (creates superposition):**
  $$H = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 & 1 \\ 1 & -1 \end{pmatrix}, \quad H|0\rangle = |+\rangle, \ H|1\rangle = |-\rangle$$
  $H$ maps computational basis $\{|0\rangle, |1\rangle\} \leftrightarrow$ Hadamard basis $\{|+\rangle, |-\rangle\}$.
- **Phase Gate $S$ and $T$ Gate:**
  $$S = \begin{pmatrix} 1 & 0 \\ 0 & i \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 0 & e^{i\pi/2} \end{pmatrix} \quad (S^2 = Z), \qquad T = \begin{pmatrix} 1 & 0 \\ 0 & e^{i\pi/4} \end{pmatrix} \quad (T^2 = S)$$
- **Rotation Gates:**
  $$R_x(\theta) = e^{-i\theta X/2} = \begin{pmatrix} \cos(\theta/2) & -i\sin(\theta/2) \\ -i\sin(\theta/2) & \cos(\theta/2) \end{pmatrix}$$
  $$R_y(\theta) = e^{-i\theta Y/2} = \begin{pmatrix} \cos(\theta/2) & -\sin(\theta/2) \\ \sin(\theta/2) & \cos(\theta/2) \end{pmatrix}$$
  $$R_z(\theta) = e^{-i\theta Z/2} = \begin{pmatrix} e^{-i\theta/2} & 0 \\ 0 & e^{i\theta/2} \end{pmatrix}$$

### 4.7.3 Two-Qubit Gates: CNOT Gate
The Controlled-NOT gate flips the target qubit if and only if the control qubit is $|1\rangle$:
$$\text{CNOT} |c, t\rangle = |c, c \oplus t\rangle$$
$$\text{CNOT} = \begin{pmatrix} 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0 \end{pmatrix}$$
- **Self-Inverse:** $\text{CNOT}^2 = I$ (applying CNOT twice restores the original state).
- **Entanglement Capability:** While single-qubit gates cannot create entanglement ($U_A \otimes U_B$ always maps product states to product states), CNOT acting across qubits generates entanglement.

### 4.7.4 Bell State Generation Circuit
Start with $|00\rangle$.
1. Apply $H$ to qubit 1:
   $$(H \otimes I) |00\rangle = (H|0\rangle) \otimes |0\rangle = \left( \frac{|0\rangle + |1\rangle}{\sqrt{2}} \right) \otimes |0\rangle = \frac{|00\rangle + |10\rangle}{\sqrt{2}}$$
2. Apply CNOT with qubit 1 as control and qubit 2 as target:
   $$\text{CNOT} \left( \frac{|00\rangle + |10\rangle}{\sqrt{2}} \right) = \frac{\text{CNOT}|00\rangle + \text{CNOT}|10\rangle}{\sqrt{2}} = \frac{|00\rangle + |11\rangle}{\sqrt{2}} = |\Phi^+\rangle$$

### 4.7.5 Classical vs Quantum Gates: Reversibility & Landauer's Principle
- **Classical AND Gate:** Inputs $(0, 0), (0, 1), (1, 0) \mapsto 0$ and $(1, 1) \mapsto 1$. 2 input bits $\to$ 1 output bit. Knowing the output is 0, the inputs cannot be reconstructed. **Information is erased**, dissipating at least $k_B T \ln 2$ heat per bit (**Landauer's Principle**).
- **Quantum Gates:** Unitary bijections ($U^{-1} = U^\dagger$). Number of inputs equals number of outputs. **Zero information is erased**, making quantum evolution strictly reversible.
- **Universality:** Any quantum circuit can be approximated to arbitrary accuracy using a finite universal gate set, such as $\{H, T, \text{CNOT}\}$ (Solovay-Kitaev Theorem).

---
