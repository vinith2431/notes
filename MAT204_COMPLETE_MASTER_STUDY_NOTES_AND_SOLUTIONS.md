# MATHEMATICS FOR INTELLIGENT SYSTEMS 3 (23MAT204 / 25MAT206)
# THE ULTIMATE MASTER STUDY COMPENDIUM
## COMPLETE THEORY NOTES • ALL FORMULAS EXPLAINED • ALL ALGORITHMS • COMPLETE QUESTION BANK WITH DETAILED SOLUTIONS

> **Authoritative Comprehensive Course Document**
> This document brings together all lecture slides, textbook modules, algorithms, mathematical formulas, and every single problem set from the course folder into one complete, self-contained reference.

---

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


---


## Unit II: Partial Differential Equations (Questions 11 to 17)

### Question 11
**Question:**
Solve the first-order partial differential equation $\frac{\partial u}{\partial x} - \frac{\partial u}{\partial y} = 0$ by separation of variables, given the boundary condition $u(x, 0) = 2e^{3x}$.

**Solution:**
1. **Separation of Variables Ansatz:**
   Assume a product solution of the form:
   $$u(x, y) = X(x) Y(y)$$
   Then:
   $$\frac{\partial u}{\partial x} = X'(x) Y(y), \qquad \frac{\partial u}{\partial y} = X(x) Y'(y)$$
   Substituting into the PDE:
   $$X'(x) Y(y) - X(x) Y'(y) = 0 \implies X'(x) Y(y) = X(x) Y'(y)$$
   Dividing both sides by $X(x) Y(y)$:
   $$\frac{X'(x)}{X(x)} = \frac{Y'(y)}{Y(y)} = k \quad (\text{separation constant})$$

2. **Solving the Decoupled ODEs:**
   - For $X(x)$: $\frac{X'}{X} = k \implies \ln X = k x + c_1 \implies X(x) = C_1 e^{k x}$
   - For $Y(y)$: $\frac{Y'}{Y} = k \implies \ln Y = k y + c_2 \implies Y(y) = C_2 e^{k y}$
   Combining the two:
   $$u(x, y) = X(x) Y(y) = C e^{k(x + y)}$$
   where $C = C_1 C_2$.

3. **Applying the Boundary Condition:**
   Given $u(x, 0) = 2e^{3x}$:
   $$u(x, 0) = C e^{k(x + 0)} = C e^{k x} = 2e^{3x}$$
   Matching coefficients and exponents:
   $$C = 2, \qquad k = 3$$

4. **Final Solution:**
   $$u(x, y) = 2 e^{3(x + y)}$$
   *Verification:* $\frac{\partial u}{\partial x} = 6e^{3(x+y)}$, $\frac{\partial u}{\partial y} = 6e^{3(x+y)}$.
   $$\frac{\partial u}{\partial x} - \frac{\partial u}{\partial y} = 6e^{3(x+y)} - 6e^{3(x+y)} = 0 \quad \checkmark$$
   $u(x, 0) = 2e^{3(x+0)} = 2e^{3x} \quad \checkmark$.

---

### Question 12
**Question:**
Solve $u_t = u_{xx}$ on $0 < x < 1$ with zero-temperature endpoints $u(0, t) = u(1, t) = 0$ and $u(x, 0) = 3 \sin(\pi x)$. Use separation of variables or the relevant eigenfunction and state how the amplitude changes with time.

**Solution:**
1. **General Eigenfunction Expansion for 1D Heat Equation:**
   For $u_t = u_{xx}$ on $0 < x < L$ with homogeneous Dirichlet boundary conditions $u(0, t) = u(L, t) = 0$, the eigenfunctions are:
   $$X_n(x) = \sin\left( \frac{n\pi x}{L} \right), \qquad n = 1, 2, 3, \dots$$
   with corresponding time decay:
   $$T_n(t) = e^{-\lambda_n t} = e^{-\left(\frac{n\pi}{L}\right)^2 t}$$
   Here $L = 1$, so the spatial modes are $\sin(n\pi x)$ with decay rates $(n\pi)^2 = n^2 \pi^2$.

2. **Matching the Initial Condition:**
   $$u(x, 0) = 3 \sin(\pi x)$$
   This corresponds exactly to the fundamental mode $n = 1$:
   $$A_1 = 3, \qquad A_n = 0 \quad \forall n \ge 2$$

3. **Final Solution:**
   $$u(x, t) = 3 e^{-\pi^2 t} \sin(\pi x)$$

4. **How the Amplitude Changes with Time:**
   The spatial profile maintains its sinusoidal shape $\sin(\pi x)$ at all times. Its peak amplitude at the midpoint $x = 0.5$ is:
   $$A(t) = 3 e^{-\pi^2 t}$$
   The amplitude decays **exponentially to zero** at a rate governed by $\pi^2 \approx 9.8696 \text{ s}^{-1}$ (half-life $t_{1/2} = \frac{\ln 2}{\pi^2} \approx 0.0702$ seconds).

---

### Question 13
**Question:**
Solve $u_t = 2u_{xx}$ on $0 < x < \pi$ with $u(0, t) = u(\pi, t) = 0$ and $u(x, 0) = \sin x + 2 \sin(2x)$. Write $u(x, t)$ and explain why the second spatial mode decays faster.

**Solution:**
1. **General Solution Formulation:**
   Here $\alpha = 2$ and $L = \pi$.
   Eigenfunctions: $X_n(x) = \sin(n x)$.
   Eigenvalues: $\lambda_n = n^2$.
   Time factor: $T_n(t) = e^{-\alpha \lambda_n t} = e^{-2 n^2 t}$.
   The general solution is:
   $$u(x, t) = \sum_{n=1}^\infty A_n e^{-2 n^2 t} \sin(n x)$$

2. **Matching Initial Conditions:**
   $$u(x, 0) = A_1 \sin(x) + A_2 \sin(2x) = \sin(x) + 2 \sin(2x)$$
   Comparing coefficients:
   $$A_1 = 1, \qquad A_2 = 2, \qquad A_n = 0 \ (\forall n \ge 3)$$

3. **Final Analytical Solution:**
   $$u(x, t) = e^{-2 t} \sin(x) + 2 e^{-8 t} \sin(2x)$$

4. **Why the Second Spatial Mode Decays Faster:**
   - Mode 1 ($n = 1$): decays as $e^{-2(1^2) t} = e^{-2t}$ (decay rate = 2).
   - Mode 2 ($n = 2$): decays as $e^{-2(2^2) t} = e^{-8t}$ (decay rate = 8).
   **Physical Explanation:**
   The heat equation is a diffusive process governed by the spatial curvature $u_{xx}$. The second mode $\sin(2x)$ has twice the spatial frequency of $\sin(x)$, which means its second spatial derivative is $2^2 = 4$ times larger:
   $$\frac{\partial^2}{\partial x^2} \sin(2x) = -4 \sin(2x)$$
   Because diffusion is proportional to curvature, higher spatial oscillations create steeper temperature gradients, causing heat to flow much more rapidly between adjacent peaks and troughs. As a result, the second mode decays **4 times faster** than the fundamental mode.

---

### Question 14
**Question:**
Using $\hat{u}(\omega, t) = \int_{-\infty}^\infty u(x, t) e^{-i\omega x} dx$, solve $u_t + 3u_x = 0$, $-\infty < x < \infty$, $u(x, 0) = e^{-x^2}$.
(a) Transform the PDE to an ODE in $t$ for $\hat{u}$ and solve it.
(b) Invert (use the shift property of the Fourier transform) to obtain $u(x, t)$.
(c) Describe the solution physically (what happens to the initial profile?).

**Solution:**
1. **(a) Transforming PDE to ODE:**
   Apply Fourier transform with respect to $x$:
   $$\mathcal{F}\{u_t\} + 3 \mathcal{F}\{u_x\} = 0$$
   Using properties $\mathcal{F}\{u_t\} = \frac{\partial \hat{u}}{\partial t}$ and $\mathcal{F}\{u_x\} = i \omega \hat{u}(\omega, t)$:
   $$\frac{\partial \hat{u}(\omega, t)}{\partial t} + 3(i \omega) \hat{u}(\omega, t) = 0$$
   This is a simple separable first-order ODE in $t$:
   $$\frac{d\hat{u}}{\hat{u}} = -3i\omega \, dt \implies \hat{u}(\omega, t) = \hat{u}(\omega, 0) e^{-3 i \omega t}$$

2. **(b) Inverting via the Fourier Shift Property:**
   Recall the Fourier transform shift theorem:
   $$\mathcal{F}\{f(x - x_0)\} = \int_{-\infty}^\infty f(x - x_0) e^{-i\omega x} dx = e^{-i\omega x_0} \hat{f}(\omega)$$
   Taking the inverse Fourier transform:
   $$\mathcal{F}^{-1}\left\{ \hat{u}(\omega, 0) e^{-i\omega(3t)} \right\} = u(x - 3t, 0)$$
   Given the initial condition $u(x, 0) = e^{-x^2}$, replacing $x$ with $x - 3t$:
   $$u(x, t) = e^{-(x - 3t)^2}$$

3. **(c) Physical Description:**
   This is a pure one-dimensional advection (wave transport) process. The initial Gaussian bell profile $e^{-x^2}$ travels rigidly to the **right (positive $x$-direction) with a constant propagation speed $c = 3$**. Because there is no diffusion term ($u_{xx}$), the wave profile suffers **zero distortion, zero attenuation, and zero dispersion**; its shape and peak height (1.0) remain perfectly preserved for all time.

---

### Question 15
**Question:**
For the heat equation $u_t = 2u_{xx}$ on $\mathbb{R}$, show that $\hat{u}(\omega, t) = \hat{u}(\omega, 0) e^{-2\omega^2 t}$. Hence find the factor by which the Fourier mode with $\omega = 3$ decays between $t = 0$ and $t = 0.5$, and explain why high-frequency modes disappear faster than low-frequency ones.

**Solution:**
1. **Deriving Fourier Transform ODE:**
   Taking the Fourier transform of $u_t = 2u_{xx}$:
   $$\frac{\partial \hat{u}(\omega, t)}{\partial t} = 2 (-i \omega)^2 \hat{u}(\omega, t) = -2 \omega^2 \hat{u}(\omega, t)$$
   Separating variables and integrating:
   $$\frac{d\hat{u}}{\hat{u}} = -2\omega^2 dt \implies \ln \hat{u}(\omega, t) = -2\omega^2 t + C \implies \hat{u}(\omega, t) = \hat{u}(\omega, 0) e^{-2\omega^2 t} \quad \checkmark$$

2. **Decay Factor for Mode $\omega = 3$ at $t = 0.5$:**
   $$\text{Decay Factor } = \frac{\hat{u}(3, 0.5)}{\hat{u}(3, 0)} = e^{-2(3^2)(0.5)} = e^{-2(9)(0.5)} = e^{-9}$$
   Evaluating numerically:
   $$e^{-9} \approx 1.2341 \times 10^{-4} \quad (\text{a decay of } 99.9876\%)$$

3. **Why High-Frequency Modes Disappear Faster:**
   The decay rate is $2\omega^2$, which grows quadratically with spatial frequency $\omega$.
   - A low-frequency mode (small $\omega$) represents broad, smooth spatial variations with gentle slopes.
   - A high-frequency mode (large $\omega$) represents sharp, rapid spatial fluctuations with large second derivatives $u_{xx} \sim -\omega^2 u$.
   Because heat diffusion is driven by temperature curvature, heat transfers almost instantaneously between closely spaced alternating hot and cold ripples, rapidly smoothing out sharp features. The heat equation acts as an aggressive **low-pass filter**.

---

### Question 16
**Question:**
Solve the 1D heat equation $u_t = u_{xx}$, $0 < x < 1$, $u(0, t) = u(1, t) = 0$, $u(x, 0) = x(1 - x)$ by the explicit FTCS method with $h = 0.25$ and $r = k/h^2 = 0.25$. Find $k$ and calculate the approximate solution at all grid points for the first two time levels $t = k$ and $t = 2k$.

**Solution:**
1. **Finding Time Step $k$:**
   Given $h = 0.25$ and $r = \frac{k}{h^2} = 0.25$:
   $$k = r h^2 = 0.25 \times (0.25)^2 = 0.25 \times 0.0625 = 0.015625 = \frac{1}{64} \text{ s}$$

2. **Grid Points and Initial Values ($t = 0$):**
   Grid spacing $h = 0.25$:
   $x_0 = 0, x_1 = 0.25, x_2 = 0.5, x_3 = 0.75, x_4 = 1.0$.
   Boundary conditions: $u_0^n = 0$ and $u_4^n = 0$ for all $n$.
   Initial profile $u(x, 0) = x(1 - x)$:
   - $u_0^0 = 0$
   - $u_1^0 = 0.25(1 - 0.25) = 0.25(0.75) = 0.1875 = \frac{3}{16}$
   - $u_2^0 = 0.5(1 - 0.5) = 0.25 = \frac{4}{16}$
   - $u_3^0 = 0.75(1 - 0.75) = 0.1875 = \frac{3}{16}$
   - $u_4^0 = 0$

3. **FTCS Update Formula:**
   With $r = 0.25$, $1 - 2r = 1 - 0.5 = 0.5$:
   $$u_i^{n+1} = 0.25 u_{i-1}^n + 0.5 u_i^n + 0.25 u_{i+1}^n$$

4. **Time Level 1 ($t = k = 0.015625$):**
   - $u_1^1 = 0.25(u_0^0) + 0.5(u_1^0) + 0.25(u_2^0) = 0.25(0) + 0.5(0.1875) + 0.25(0.25) = 0.09375 + 0.0625 = 0.15625$
   - $u_2^1 = 0.25(u_1^0) + 0.5(u_2^0) + 0.25(u_3^0) = 0.25(0.1875) + 0.5(0.25) + 0.25(0.1875) = 0.046875 + 0.125 + 0.046875 = 0.21875$
   - $u_3^1 = 0.25(u_2^0) + 0.5(u_3^0) + 0.25(u_4^0) = 0.25(0.25) + 0.5(0.1875) + 0.25(0) = 0.0625 + 0.09375 = 0.15625$
   $$\mathbf{u}^1 = [0, \ 0.15625, \ 0.21875, \ 0.15625, \ 0]^T$$

5. **Time Level 2 ($t = 2k = 0.03125$):**
   - $u_1^2 = 0.25(u_0^1) + 0.5(u_1^1) + 0.25(u_2^1) = 0 + 0.5(0.15625) + 0.25(0.21875) = 0.078125 + 0.0546875 = 0.1328125$
   - $u_2^2 = 0.25(u_1^1) + 0.5(u_2^1) + 0.25(u_3^1) = 0.25(0.15625) + 0.5(0.21875) + 0.25(0.15625) = 0.0390625 + 0.109375 + 0.0390625 = 0.1875$
   - $u_3^2 = 0.25(u_2^1) + 0.5(u_3^1) + 0.25(u_4^1) = 0.25(0.21875) + 0.5(0.15625) + 0 = 0.0546875 + 0.078125 = 0.1328125$
   $$\mathbf{u}^2 = [0, \ 0.1328125, \ 0.1875, \ 0.1328125, \ 0]^T$$

---

### Question 17
**Question:**
For $u_t = u_{xx}$, use grid spacing $h = 0.25$ and time step $k = 0.025$. Calculate $r = k/h^2$, write the FTCS update, and check whether the standard stability condition $r \le 1/2$ is satisfied. If $u_{i-1}^n = 1, u_i^n = 2$, and $u_{i+1}^n = 1$, find $u_i^{n+1}$.

**Solution:**
1. **Calculating $r$:**
   $$r = \frac{k}{h^2} = \frac{0.025}{(0.25)^2} = \frac{0.025}{0.0625} = 0.4$$

2. **Checking Stability Condition:**
   The standard von Neumann stability condition for explicit FTCS is $r \le \frac{1}{2} = 0.5$.
   Since $r = 0.4 \le 0.5$, the stability condition is **satisfied**, and the scheme is numerically stable.

3. **FTCS Update Equation:**
   $$u_i^{n+1} = r u_{i-1}^n + (1 - 2r) u_i^n + r u_{i+1}^n$$
   With $r = 0.4$, $1 - 2r = 1 - 0.8 = 0.2$:
   $$u_i^{n+1} = 0.4 u_{i-1}^n + 0.2 u_i^n + 0.4 u_{i+1}^n$$

4. **Calculating $u_i^{n+1}$:**
   Given $u_{i-1}^n = 1, u_i^n = 2, u_{i+1}^n = 1$:
   $$u_i^{n+1} = 0.4(1) + 0.2(2) + 0.4(1) = 0.4 + 0.4 + 0.4 = 1.2$$

---

## Unit III: Gaussians, WLS, Markov Chains & MDP (Questions 18 to 23)

### Question 18
**Question:**
Assume that the sensor reading follows a normal distribution $X \sim \mathcal{N}(\mu, \sigma^2)$. Use the Gaussian probability density function to calculate the exact probability density at the specified observation $x$:
$$f_X(x) = \frac{1}{\sqrt{2\pi\sigma^2}} \exp\left( -\frac{(x - \mu)^2}{2\sigma^2} \right)$$
Such a temperature sensor produces readings that follow a normal distribution with mean $\mu = 25^\circ\text{C}$ and variance $\sigma^2 = 9^\circ\text{C}^2$. Calculate the probability density of observing a reading of $x = 31^\circ\text{C}$.

**Solution:**
1. **Given Parameters:**
   $\mu = 25$, $\sigma^2 = 9 \implies \sigma = 3$.
   Observation $x = 31$.

2. **Evaluating the Density Function:**
   $$x - \mu = 31 - 25 = 6$$
   $$(x - \mu)^2 = 6^2 = 36$$
   $$\frac{(x - \mu)^2}{2\sigma^2} = \frac{36}{2 \times 9} = \frac{36}{18} = 2$$
   The exponential term is $e^{-2}$.
   The normalization constant is:
   $$\frac{1}{\sqrt{2\pi \sigma^2}} = \frac{1}{\sqrt{2\pi \times 9}} = \frac{1}{3\sqrt{2\pi}}$$
   Therefore:
   $$f_X(31) = \frac{1}{3\sqrt{2\pi}} e^{-2} = \frac{e^{-2}}{3\sqrt{2\pi}}$$

3. **Numerical Value:**
   $e^{-2} \approx 0.135335$
   $3\sqrt{2\pi} \approx 3 \times 2.50663 = 7.519887$
   $$f_X(31) = \frac{0.135335}{7.519887} \approx 0.017997 \approx 0.0180$$

---

### Question 19
**Question:**
Fit the line $y = a + bx$ by ordinary least squares to the points $(1, 2), (2, 3), (3, 5), (4, 6)$. Write the normal equations $X^T X \beta = X^T y$ explicitly, solve them, and compute the sum of squared residuals.

**Solution:**
1. **Formulating Matrices:**
   Data points $(x_i, y_i)$: $(1, 2), (2, 3), (3, 5), (4, 6)$.
   Model: $y_i = a(1) + b(x_i)$.
   $$X = \begin{pmatrix} 1 & 1 \\ 1 & 2 \\ 1 & 3 \\ 1 & 4 \end{pmatrix}, \qquad y = \begin{pmatrix} 2 \\ 3 \\ 5 \\ 6 \end{pmatrix}, \qquad \beta = \begin{pmatrix} a \\ b \end{pmatrix}$$

2. **Computing $X^T X$ and $X^T y$:**
   $$X^T X = \begin{pmatrix} 1 & 1 & 1 & 1 \\ 1 & 2 & 3 & 4 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 2 \\ 1 & 3 \\ 1 & 4 \end{pmatrix} = \begin{pmatrix} 4 & 10 \\ 10 & 1^2 + 2^2 + 3^2 + 4^2 \end{pmatrix} = \begin{pmatrix} 4 & 10 \\ 10 & 30 \end{pmatrix}$$
   $$X^T y = \begin{pmatrix} 1 & 1 & 1 & 1 \\ 1 & 2 & 3 & 4 \end{pmatrix} \begin{pmatrix} 2 \\ 3 \\ 5 \\ 6 \end{pmatrix} = \begin{pmatrix} 2 + 3 + 5 + 6 \\ 1(2) + 2(3) + 3(5) + 4(6) \end{pmatrix} = \begin{pmatrix} 16 \\ 2 + 6 + 15 + 24 \end{pmatrix} = \begin{pmatrix} 16 \\ 47 \end{pmatrix}$$

3. **Writing Normal Equations Explicitly:**
   $$\begin{pmatrix} 4 & 10 \\ 10 & 30 \end{pmatrix} \begin{pmatrix} a \\ b \end{pmatrix} = \begin{pmatrix} 16 \\ 47 \end{pmatrix}$$

4. **Solving the System:**
   $$\det(X^T X) = (4)(30) - (10)(10) = 120 - 100 = 20$$
   $$(X^T X)^{-1} = \frac{1}{20} \begin{pmatrix} 30 & -10 \\ -10 & 4 \end{pmatrix}$$
   $$\beta = \frac{1}{20} \begin{pmatrix} 30 & -10 \\ -10 & 4 \end{pmatrix} \begin{pmatrix} 16 \\ 47 \end{pmatrix} = \frac{1}{20} \begin{pmatrix} 30(16) - 10(47) \\ -10(16) + 4(47) \end{pmatrix} = \frac{1}{20} \begin{pmatrix} 480 - 470 \\ -160 + 188 \end{pmatrix} = \frac{1}{20} \begin{pmatrix} 10 \\ 28 \end{pmatrix} = \begin{pmatrix} 0.5 \\ 1.4 \end{pmatrix}$$
   Fitted line: $y = 0.5 + 1.4 x$.

5. **Sum of Squared Residuals (SSR):**
   - At $x_1 = 1$: $\hat{y}_1 = 0.5 + 1.4(1) = 1.9 \implies e_1 = 2 - 1.9 = 0.1 \implies e_1^2 = 0.01$
   - At $x_2 = 2$: $\hat{y}_2 = 0.5 + 1.4(2) = 3.3 \implies e_2 = 3 - 3.3 = -0.3 \implies e_2^2 = 0.09$
   - At $x_3 = 3$: $\hat{y}_3 = 0.5 + 1.4(3) = 4.7 \implies e_3 = 5 - 4.7 = 0.3 \implies e_3^2 = 0.09$
   - At $x_4 = 4$: $\hat{y}_4 = 0.5 + 1.4(4) = 6.1 \implies e_4 = 6 - 6.1 = -0.1 \implies e_4^2 = 0.01$
   $$\text{SSR} = \sum_{i=1}^4 e_i^2 = 0.01 + 0.09 + 0.09 + 0.01 = 0.20$$

---

### Question 20
**Question:**
Fit $y = a + bx$ to $(0, 1), (1, 3), (2, 4)$ with weights $w = (1, 2, 1)$ by minimising $\sum_i w_i (y_i - a - b x_i)^2$. Write the weighted normal equations $X^T W X \beta = X^T W y$ and solve. Explain why the fitted line passes closer to the middle point than the ordinary least-squares line does.

**Solution:**
1. **Formulating Matrices:**
   $$X = \begin{pmatrix} 1 & 0 \\ 1 & 1 \\ 1 & 2 \end{pmatrix}, \qquad y = \begin{pmatrix} 1 \\ 3 \\ 4 \end{pmatrix}, \qquad W = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 1 \end{pmatrix}$$

2. **Computing $X^T W X$ and $X^T W y$:**
   $$X^T W = \begin{pmatrix} 1 & 1 & 1 \\ 0 & 1 & 2 \end{pmatrix} \begin{pmatrix} 1 & 0 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 1 \end{pmatrix} = \begin{pmatrix} 1 & 2 & 1 \\ 0 & 2 & 2 \end{pmatrix}$$
   $$X^T W X = \begin{pmatrix} 1 & 2 & 1 \\ 0 & 2 & 2 \end{pmatrix} \begin{pmatrix} 1 & 0 \\ 1 & 1 \\ 1 & 2 \end{pmatrix} = \begin{pmatrix} 1+2+1 & 0+2+2 \\ 0+2+2 & 0+2(1)+2(4) \end{pmatrix} = \begin{pmatrix} 4 & 4 \\ 4 & 6 \end{pmatrix}$$
   $$X^T W y = \begin{pmatrix} 1 & 2 & 1 \\ 0 & 2 & 2 \end{pmatrix} \begin{pmatrix} 1 \\ 3 \\ 4 \end{pmatrix} = \begin{pmatrix} 1(1) + 2(3) + 1(4) \\ 0(1) + 2(3) + 2(4) \end{pmatrix} = \begin{pmatrix} 1 + 6 + 4 \\ 6 + 8 \end{pmatrix} = \begin{pmatrix} 11 \\ 14 \end{pmatrix}$$

3. **Weighted Normal Equations:**
   $$\begin{pmatrix} 4 & 4 \\ 4 & 6 \end{pmatrix} \begin{pmatrix} a \\ b \end{pmatrix} = \begin{pmatrix} 11 \\ 14 \end{pmatrix}$$

4. **Solving the System:**
   $$\det(X^T W X) = (4)(6) - (4)(4) = 24 - 16 = 8$$
   $$(X^T W X)^{-1} = \frac{1}{8} \begin{pmatrix} 6 & -4 \\ -4 & 4 \end{pmatrix}$$
   $$\beta = \frac{1}{8} \begin{pmatrix} 6 & -4 \\ -4 & 4 \end{pmatrix} \begin{pmatrix} 11 \\ 14 \end{pmatrix} = \frac{1}{8} \begin{pmatrix} 66 - 56 \\ -44 + 56 \end{pmatrix} = \frac{1}{8} \begin{pmatrix} 10 \\ 12 \end{pmatrix} = \begin{pmatrix} 1.25 \\ 1.5 \end{pmatrix}$$
   Fitted line: $y = 1.25 + 1.5 x$.

5. **Comparison with OLS:**
   - Under WLS: at the middle point $x_2 = 1$, $\hat{y}_{\text{WLS}}(1) = 1.25 + 1.5(1) = 2.75$.
     Residual: $|3 - 2.75| = 0.25$.
   - Under standard OLS ($W = I$):
     $X^T X = \begin{pmatrix} 3 & 3 \\ 3 & 5 \end{pmatrix}$, $X^T y = \begin{pmatrix} 8 \\ 11 \end{pmatrix}$.
     Solving yields $\beta_{\text{OLS}} = \begin{pmatrix} 7/6 \\ 1.5 \end{pmatrix} \approx \begin{pmatrix} 1.167 \\ 1.5 \end{pmatrix}$.
     At $x_2 = 1$, $\hat{y}_{\text{OLS}}(1) = 1.167 + 1.5 = 2.667$.
     Residual: $|3 - 2.667| = 0.333$.
   - **Explanation:**
     The middle point $(1, 3)$ has weight $w_2 = 2$, double that of the outer points ($w_1 = w_3 = 1$). In the objective function $\sum w_i (y_i - \hat{y}_i)^2$, any error at the middle point is penalized twice as heavily. Consequently, the optimization algorithm pulls the fitted line closer to $(1, 3)$ (reducing its residual from 0.333 to 0.25) to minimize total weighted loss.

---

### Question 21
**Question:**
A customer moves among three shopping preferences: 1 = Online, 2 = In-store, and 3 = No Purchase. The transition matrix is
$$P = \begin{pmatrix} 0.6 & 0.3 & 0.1 \\ 0.2 & 0.6 & 0.2 \\ 0.3 & 0.2 & 0.5 \end{pmatrix}$$
If the customer initially chooses In-store, $X(0) = [0, 1, 0]$, determine the probability that the customer will choose Online after three transitions.

**Solution:**
1. **Initial Distribution:**
   $$\pi(0) = [0, 1, 0]$$
   We seek $\pi(3) = \pi(0) P^3$ and the first entry $\pi_1(3)$.

2. **Transition 1 ($n = 1$):**
   $$\pi(1) = \pi(0) P = [0, 1, 0] \begin{pmatrix} 0.6 & 0.3 & 0.1 \\ 0.2 & 0.6 & 0.2 \\ 0.3 & 0.2 & 0.5 \end{pmatrix} = [0.2, \ 0.6, \ 0.2]$$

3. **Transition 2 ($n = 2$):**
   $$\pi(2) = \pi(1) P = [0.2, \ 0.6, \ 0.2] \begin{pmatrix} 0.6 & 0.3 & 0.1 \\ 0.2 & 0.6 & 0.2 \\ 0.3 & 0.2 & 0.5 \end{pmatrix}$$
   - $\pi_1(2) = 0.2(0.6) + 0.6(0.2) + 0.2(0.3) = 0.12 + 0.12 + 0.06 = 0.30$
   - $\pi_2(2) = 0.2(0.3) + 0.6(0.6) + 0.2(0.2) = 0.06 + 0.36 + 0.04 = 0.46$
   - $\pi_3(2) = 0.2(0.1) + 0.6(0.2) + 0.2(0.5) = 0.02 + 0.12 + 0.10 = 0.24$
   $$\pi(2) = [0.30, \ 0.46, \ 0.24]$$

4. **Transition 3 ($n = 3$):**
   $$\pi(3) = \pi(2) P = [0.30, \ 0.46, \ 0.24] \begin{pmatrix} 0.6 & 0.3 & 0.1 \\ 0.2 & 0.6 & 0.2 \\ 0.3 & 0.2 & 0.5 \end{pmatrix}$$
   We calculate the Online state probability $\pi_1(3)$:
   $$\pi_1(3) = 0.30(0.6) + 0.46(0.2) + 0.24(0.3) = 0.180 + 0.092 + 0.072 = 0.344$$
   (Full vector: $\pi_2(3) = 0.414, \pi_3(3) = 0.242$).
   **Final Answer:** The probability that the customer will choose Online after three transitions is **0.344 (or 34.4%)**.

---

### Question 22
**Question:**
A daily weather model has states Sunny, Cloudy, and Rainy, in that order, with row-stochastic transition matrix
$$P = \begin{pmatrix} 0.6 & 0.3 & 0.1 \\ 0.2 & 0.6 & 0.2 \\ 0.1 & 0.3 & 0.6 \end{pmatrix}$$
If Day 0 is Cloudy, $\pi(0) = (0, 1, 0)$, compute $\pi(1) = \pi(0)P$ and $\pi(2) = \pi(1)P$. What is the probability of rain on Day 2?

**Solution:**
1. **Day 1 Distribution $\pi(1)$:**
   $$\pi(1) = \pi(0) P = [0, 1, 0] \begin{pmatrix} 0.6 & 0.3 & 0.1 \\ 0.2 & 0.6 & 0.2 \\ 0.1 & 0.3 & 0.6 \end{pmatrix} = [0.2, \ 0.6, \ 0.2]$$
   - Probability Sunny on Day 1 = 0.2
   - Probability Cloudy on Day 1 = 0.6
   - Probability Rainy on Day 1 = 0.2

2. **Day 2 Distribution $\pi(2)$:**
   $$\pi(2) = \pi(1) P = [0.2, \ 0.6, \ 0.2] \begin{pmatrix} 0.6 & 0.3 & 0.1 \\ 0.2 & 0.6 & 0.2 \\ 0.1 & 0.3 & 0.6 \end{pmatrix}$$
   - Sunny $\pi_1(2) = 0.2(0.6) + 0.6(0.2) + 0.2(0.1) = 0.12 + 0.12 + 0.02 = 0.26$
   - Cloudy $\pi_2(2) = 0.2(0.3) + 0.6(0.6) + 0.2(0.3) = 0.06 + 0.36 + 0.06 = 0.48$
   - Rainy $\pi_3(2) = 0.2(0.1) + 0.6(0.2) + 0.2(0.6) = 0.02 + 0.12 + 0.12 = 0.26$
   $$\pi(2) = [0.26, \ 0.48, \ 0.26]$$

3. **Probability of Rain on Day 2:**
   $$P(\text{Rain on Day 2}) = \pi_3(2) = 0.26 \quad (\text{or } 26\%)$$

---

### Question 23
**Question:**
A two-state Markov chain has $P = \begin{pmatrix} 0.9 & 0.1 \\ 0.4 & 0.6 \end{pmatrix}$. It starts in State 2. Determine the distribution after one and two transitions. Then solve $\pi P = \pi$ together with $\pi_1 + \pi_2 = 1$ to find the stationary distribution, and describe its meaning.

**Solution:**
1. **Transitions from State 2 ($\ action{initial state } \pi(0) = [0, 1]$):**
   - **After 1 transition:**
     $$\pi(1) = \pi(0) P = [0, 1] \begin{pmatrix} 0.9 & 0.1 \\ 0.4 & 0.6 \end{pmatrix} = [0.4, \ 0.6]$$
   - **After 2 transitions:**
     $$\pi(2) = \pi(1) P = [0.4, \ 0.6] \begin{pmatrix} 0.9 & 0.1 \\ 0.4 & 0.6 \end{pmatrix} = [0.4(0.9) + 0.6(0.4), \ 0.4(0.1) + 0.6(0.6)]$$
     $$\pi(2) = [0.36 + 0.24, \ 0.04 + 0.36] = [0.60, \ 0.40]$$

2. **Finding the Stationary Distribution:**
   We solve $\pi P = \pi$ subject to $\pi_1 + \pi_2 = 1$:
   $$[\pi_1, \pi_2] \begin{pmatrix} 0.9 & 0.1 \\ 0.4 & 0.6 \end{pmatrix} = [\pi_1, \pi_2]$$
   Equation from first column:
   $$0.9 \pi_1 + 0.4 \pi_2 = \pi_1 \implies 0.4 \pi_2 = 0.1 \pi_1 \implies \pi_1 = 4 \pi_2$$
   Substitute into normalization constraint $\pi_1 + \pi_2 = 1$:
   $$4 \pi_2 + \pi_2 = 1 \implies 5 \pi_2 = 1 \implies \pi_2 = \frac{1}{5} = 0.2$$
   $$\pi_1 = 4(0.2) = 0.8$$
   **Stationary Distribution:**
   $$\pi = [0.8, \ 0.2]$$

3. **Description and Meaning:**
   - **Long-term time proportion:** Over a very long run of the process, the system will spend $80\%$ of its time in State 1 and $20\%$ of its time in State 2.
   - **Ergodic limit / Forgetting initial state:** Regardless of whether the chain starts in State 1, State 2, or any probabilistic mixture, the state distribution $\pi(n) = \pi(0) P^n$ converges to $[0.8, 0.2]$ as $n \to \infty$.

---

## Unit IV: Quantum Computing, Gates & Bell's Inequality (Questions 24 to 33)

### Question 24
**Question:**
Explain how classical gates differ from quantum gates in terms of input states, output states, and reversibility. Why is a classical AND gate irreversible, while every quantum gate must be reversible? Which mathematical property of a quantum gate guarantees this? Why is it difficult for a classical supercomputer to simulate a large entangled quantum system? Explain how the growth of the quantum state space affects classical simulation. Does an exponentially large state space mean a quantum computer can read out exponentially much information? Justify your answer.

**Solution:**
1. **Classical vs Quantum Gates:**
   - **Input/Output states:** Classical gates act deterministically on discrete binary bit strings $\{0, 1\}^n$. Quantum gates act linearly on continuous complex superpositions of states in Hilbert space $\mathbb{C}^{2^n}$ ($|\psi\rangle = \sum c_x |x\rangle$).
   - **Reversibility:** Most classical gates are irreversible (many-to-one mappings where information is destroyed). All closed quantum gates are strictly **reversible** (one-to-one bijective unitary transformations).

2. **Irreversibility of Classical AND vs Quantum Reversibility:**
   - The classical AND gate takes 2 input bits and produces 1 output bit ($2 \to 1$).
     Truth table: $(0, 0) \mapsto 0$, $(0, 1) \mapsto 0$, $(1, 0) \mapsto 0$, $(1, 1) \mapsto 1$.
     If the output is 0, it is impossible to determine which of the three input combinations $(0,0), (0,1), (1,0)$ produced it. One bit of information is erased, which by **Landauer's Principle** dissipates at least $k_B T \ln 2$ energy as heat.
   - Quantum mechanics is governed by the Schrödinger equation, whose time-evolution operator is **unitary**: $U^\dagger U = I$.
     Unitary operators preserve the inner product and norm: $\langle U \psi | U \phi \rangle = \langle \psi | \phi \rangle$.
     Every unitary matrix possesses an exact inverse $U^{-1} = U^\dagger$. Therefore, every quantum gate is completely reversible without information loss.

3. **Classical Simulation Difficulty of Entangled Quantum Systems:**
   - **Exponential growth of state space:** An $n$-qubit quantum system has state space $(\mathbb{C}^2)^{\otimes n} \cong \mathbb{C}^{2^n}$.
   - Storing the state vector requires storing $2^n$ complex probability amplitudes.
     For $n = 50$: $2^{50} \approx 1.125 \times 10^{15}$ amplitudes (petabytes of memory).
     For $n = 300$: $2^{300} \approx 2 \times 10^{90}$, which exceeds the total number of atoms in the observable universe.
   - Applying an $n$-qubit gate requires multiplying a $2^n \times 2^n$ matrix by a $2^n$ vector, requiring exponential CPU time and memory on a classical computer.

4. **Can a Quantum Computer Read Out Exponentially Much Information?**
   **No! (Holevo's Theorem).**
   Although an $n$-qubit state evolves through an exponentially large $2^n$-dimensional space of amplitudes, quantum measurement causes the state to **collapse** to a single basis state according to Born's rule. A measurement of $n$ qubits yields only **$n$ classical bits of information**. The computational power comes not from reading out exponential information, but from quantum interference: orchestrating constructive interference on the correct answer while destructive interference cancels wrong answers before measurement.

---

### Question 25
**Question:**
Compare the action of a classical AND gate with a quantum gate such as the CNOT gate. Identify exactly where the classical gate loses information and how CNOT avoids this. Explain the roles of superposition, reversibility, and entanglement in quantum gate operations. Why does CNOT acting on a superposition control qubit produce a state that is not a product state, whereas CNOT acting on a basis-state control does not? Why can the simulation of general quantum circuits require exponentially more memory as the number of qubits increases?

**Solution:**
1. **Information Loss: Classical AND vs Quantum CNOT:**
   - **Classical AND:** Takes 2 bits in, gives 1 bit out. The map is 4-to-2: three distinct inputs $(0,0), (0,1), (1,0)$ all map to output 0. Given output 0, the input cannot be determined. Information is irrevocably lost.
   - **Quantum CNOT:** Takes 2 qubits in and outputs 2 qubits ($|c, t\rangle \mapsto |c, c \oplus t\rangle$).
     Mapping: $|00\rangle \mapsto |00\rangle$, $|01\rangle \mapsto |01\rangle$, $|10\rangle \mapsto |11\rangle$, $|11\rangle \mapsto |10\rangle$.
     This is a permutation of the 4 basis states (a bijection). Applying CNOT a second time completely restores the original inputs: $\text{CNOT}^2 = I$. Zero information is lost.

2. **Roles of Superposition, Reversibility, and Entanglement:**
   - **Superposition:** Allows quantum gates to operate simultaneously on linear combinations of inputs (quantum parallelism).
   - **Reversibility:** Ensures conservation of quantum information and probability amplitudes (no dissipation).
   - **Entanglement:** Creates non-local multi-qubit correlations that cannot be factored into independent subsystems, providing exponential state complexity.

3. **CNOT on Superposition Control vs Basis-State Control:**
   - **Case 1: Basis-state control.**
     Let input be $|0\rangle \otimes |\psi\rangle = |0\rangle(b_0|0\rangle + b_1|1\rangle) = b_0|00\rangle + b_1|01\rangle$.
     CNOT does nothing because control is 0: output is $|0\rangle(b_0|0\rangle + b_1|1\rangle)$, which is still a separable **product state**.
     If control is $|1\rangle$: $|1\rangle(b_0|0\rangle + b_1|1\rangle) \mapsto |1\rangle(b_0|1\rangle + b_1|0\rangle)$, which is also a separable **product state**.
   - **Case 2: Superposition control.**
     Let control qubit be in superposition: $\frac{|0\rangle + |1\rangle}{\sqrt{2}} \otimes |0\rangle = \frac{|00\rangle + |10\rangle}{\sqrt{2}}$.
     CNOT flips the second qubit *if and only if* the first is $|1\rangle$:
     $$\text{CNOT} \left( \frac{|00\rangle + |10\rangle}{\sqrt{2}} \right) = \frac{|00\rangle + |11\rangle}{\sqrt{2}} = |\Phi^+\rangle$$
     In this output, $c_{00} c_{11} - c_{01} c_{10} = (1/\sqrt{2})(1/\sqrt{2}) - 0 = 1/2 \ne 0$.
     This state **cannot be factored** into $(a_0|0\rangle + a_1|1\rangle) \otimes (b_0|0\rangle + b_1|1\rangle)$. It is an **entangled Bell state**.

4. **Exponential Memory for General Circuits:**
   When gates generate entanglement across qubits, the system cannot be tracked by keeping track of $n$ individual 2D qubit vectors ($2n$ numbers). Instead, the full entangled state vector requires tracking all $2^n$ joint amplitudes.

---

### Question 26
**Question:**
State Bell’s inequality (CHSH form) in words. What assumptions does a local hidden-variable theory make? Which of these assumptions (locality or realism) is abandoned by quantum mechanics, and why can this not be settled by any single measurement outcome? What does a violation tell us, and what does it not tell us (e.g. can it be used for faster-than-light signalling)? Why do the local measurement statistics of each party stay unchanged even though the joint correlations are non-classical?

**Solution:**
1. **CHSH Inequality in Words:**
   "If two separated parties independently measure two dichotomic ($\{+1, -1\}$) physical properties on a shared pair of particles, and if the measurement outcomes are predetermined by local hidden variables independent of the distant choice of measurement setting, then a specific linear combination of their four correlation expectations cannot exceed 2 in magnitude."
   $$|\mathbb{E}(AB) + \mathbb{E}(AB') + \mathbb{E}(A'B) - \mathbb{E}(A'B')| \le 2$$

2. **Assumptions of Local Hidden-Variable (LHV) Theory:**
   - **Realism:** Physical quantities possess objective, pre-existing values prior to measurement.
   - **Locality:** An action or choice of measurement basis made at location A cannot instantaneously change the physical reality or measurement probabilities at a space-like separated location B.

3. **What Quantum Mechanics Abandons and Why Single Shot Cannot Settle It:**
   Quantum mechanics abandons **local realism** (orthodox Copenhagen abandons realism, while Bohmian mechanics abandons locality).
   A single measurement run produces only a single pair of outcomes (e.g. $+1$ and $-1$), which is completely consistent with either classical or quantum theories. The quantum violation emerges only as a **statistical correlation over many repeated measurements** performed with different combinations of measurement angles.

4. **What a Violation Tells Us vs What It Does Not:**
   - **What it tells us:** Nature cannot be described by any local hidden-variable theory. Entanglement exhibits genuine non-local quantum correlations stronger than any classical physics allows ($S = 2\sqrt{2} > 2$).
   - **What it does NOT tell us:** It does **NOT allow faster-than-light (superluminal) communication**.
     *Why? (No-Signaling Theorem):*
     Alice's local measurement outcome is completely random: $P(A = +1) = 0.5$ and $P(A = -1) = 0.5$, regardless of whether Bob measures $B$ or $B'$, or does not measure at all. Bob's reduced density matrix is always the maximally mixed state $\rho_B = \frac{1}{2}I$. Alice cannot use entanglement to send a message to Bob because Bob sees only random noise unless he compares his results with Alice via a classical communication channel (limited by the speed of light).

---

### Question 27
**Question:**
The CNOT gate is
$$\begin{pmatrix} 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0 \end{pmatrix}$$
Show that it is unitary and its own inverse. Why must every valid quantum gate be unitary (relate this to probabilities)? Interpret “its own inverse” as an operational statement about applying the gate twice. Explain why it can create entanglement while single-qubit gates cannot. Give a concrete product-state input whose output is entangled, and state a simple test (e.g. a condition on the four amplitudes) showing the output cannot be written as a product.

**Solution:**
1. **Showing CNOT is Unitary and Self-Inverse:**
   Let $U = \text{CNOT}$.
   $$U^\dagger = U^T = \begin{pmatrix} 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0 \end{pmatrix} = U$$
   Computing $U^2$:
   $$U U = \begin{pmatrix} 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0 \end{pmatrix} \begin{pmatrix} 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0 \end{pmatrix} = \begin{pmatrix} 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1 \end{pmatrix} = I_4$$
   Because $U^\dagger U = I$, $U$ is **unitary**.
   Because $U^2 = I$, $U = U^{-1}$, meaning $U$ is **its own inverse**.

2. **Why Quantum Gates Must Be Unitary:**
   In quantum mechanics, the total probability across all measurement outcomes must always equal 1: $\||\psi\rangle\|^2 = \langle\psi|\psi\rangle = 1$.
   Under gate transformation $|\psi'\rangle = U|\psi\rangle$:
   $$\langle\psi'|\psi'\rangle = \langle U\psi | U\psi \rangle = \langle \psi | U^\dagger U | \psi \rangle$$
   For this to equal $\langle\psi|\psi\rangle = 1$ for **all** possible state vectors $|\psi\rangle$, we must have $U^\dagger U = I$. Unitary evolution guarantees **conservation of total probability**.

3. **Operational Meaning of "Its Own Inverse":**
   Applying the CNOT gate twice in succession on any state leaves the state completely unchanged:
   $$\text{CNOT}(\text{CNOT}|c, t\rangle) = \text{CNOT}|c, c \oplus t\rangle = |c, c \oplus c \oplus t\rangle = |c, 0 \oplus t\rangle = |c, t\rangle$$
   The gate undoes its own operation.

4. **Why CNOT Creates Entanglement While Single-Qubit Gates Cannot:**
   Any combination of single-qubit gates on a product state has the tensor form $(U_A \otimes U_B)(|\psi_A\rangle \otimes |\psi_B\rangle) = (U_A |\psi_A\rangle) \otimes (U_B |\psi_B\rangle)$, which is manifestly a **product state** (cannot create correlations between distinct qubits).
   CNOT is an **entangling two-qubit gate**: its action on the target qubit depends conditionally on the state of the control qubit.

5. **Concrete Input and Entanglement Test:**
   - **Input:** $|+\rangle |0\rangle = \left( \frac{|0\rangle + |1\rangle}{\sqrt{2}} \right) |0\rangle = \frac{1}{\sqrt{2}}|00\rangle + \frac{1}{\sqrt{2}}|10\rangle$. (Product state).
   - **Output:** $\text{CNOT}(|+\rangle |0\rangle) = \frac{|00\rangle + |11\rangle}{\sqrt{2}} = |\Phi^+\rangle$.
   - **Entanglement Test:**
     A general two-qubit state $|\psi\rangle = c_{00}|00\rangle + c_{01}|01\rangle + c_{10}|10\rangle + c_{11}|11\rangle$ is a product state if and only if:
     $$c_{00} c_{11} - c_{01} c_{10} = 0$$
     For $|\Phi^+\rangle$: $c_{00} = 1/\sqrt{2}, c_{01} = 0, c_{10} = 0, c_{11} = 1/\sqrt{2}$.
     $$c_{00} c_{11} - c_{01} c_{10} = \left(\frac{1}{\sqrt{2}}\right)\left(\frac{1}{\sqrt{2}}\right) - (0)(0) = \frac{1}{2} \ne 0$$
     Because the determinant is non-zero, the output state **cannot be factored into a product state and is therefore entangled**.

---

### Question 28
**Question:**
What does it mean physically that measurement “collapses” the state? How does measurement differ from unitary evolution (compare reversibility and determinism)? If the same observable is measured twice in succession, what is the second result and why? Why can a quantum state not be copied (no-cloning)? Sketch the argument using linearity, and explain why this does not forbid copying a known basis state $|0\rangle$ or $|1\rangle$.

**Solution:**
1. **Physical Meaning of Measurement "Collapse":**
   Prior to measurement, a quantum system can exist in a superposition of multiple mutually exclusive physical possibilities ($|\psi\rangle = \sum c_i |i\rangle$). Measurement physically forces the system to randomly select and realize one definite eigenstate $|k\rangle$ with probability $|c_k|^2$. All other probability amplitudes instantly vanish, and the pre-existing superposition is permanently destroyed.

2. **Measurement vs Unitary Evolution:**
   - **Determinism:** Unitary evolution is completely deterministic (given $|\psi(0)\rangle$, the future state $|\psi(t)\rangle = U(t)|\psi(0)\rangle$ is uniquely determined). Measurement is inherently **probabilistic** (only the probabilities $|c_i|^2$ are determined, not the specific outcome).
   - **Reversibility:** Unitary evolution is **reversible** ($U^\dagger = U^{-1}$). Measurement is **irreversible** (knowing the post-measurement collapsed state $|k\rangle$ does not allow reconstruction of the original superposition amplitudes $c_i$).

3. **Measuring Twice in Succession:**
   If an observable is measured and yields eigenvalue $\lambda_k$, the state instantly collapses to eigenstate $|k\rangle$.
   A second measurement performed immediately afterward in the same basis acts on $|k\rangle$. Because $|k\rangle$ is already an eigenstate of the observable:
   $$P(\lambda_k) = |\langle k | k \rangle|^2 = 1^2 = 1$$
   The second measurement yields **the exact same result $\lambda_k$ with 100% certainty**.

4. **The No-Cloning Theorem:**
   - *Statement:* No quantum operation can copy an arbitrary unknown quantum state.
   - *Proof using Linearity:*
     Suppose a unitary cloning machine $U$ exists such that for any state $|\psi\rangle$ and standard blank state $|0\rangle$:
     $$U (|\psi\rangle |0\rangle) = |\psi\rangle |\psi\rangle$$
     Let $|0\rangle$ and $|1\rangle$ be orthogonal basis states:
     $$U (|0\rangle |0\rangle) = |00\rangle, \qquad U (|1\rangle |0\rangle) = |11\rangle$$
     Now consider an arbitrary superposition $|+\rangle = \frac{|0\rangle + |1\rangle}{\sqrt{2}}$.
     By **linearity of quantum mechanics**:
     $$U (|+\rangle |0\rangle) = U \left( \frac{|0\rangle + |1\rangle}{\sqrt{2}} |0\rangle \right) = \frac{1}{\sqrt{2}} U(|00\rangle) + \frac{1}{\sqrt{2}} U(|10\rangle) = \frac{|00\rangle + |11\rangle}{\sqrt{2}}$$
     However, a true cloning of $|+\rangle$ must produce:
     $$|+\rangle |+\rangle = \left( \frac{|0\rangle + |1\rangle}{\sqrt{2}} \right) \left( \frac{|0\rangle + |1\rangle}{\sqrt{2}} \right) = \frac{|00\rangle + |01\rangle + |10\rangle + |11\rangle}{2}$$
     Clearly:
     $$\frac{|00\rangle + |11\rangle}{\sqrt{2}} \ne \frac{|00\rangle + |01\rangle + |10\rangle + |11\rangle}{2}$$
     This contradiction proves that **no linear unitary operator can clone an arbitrary quantum state**.
   - *Why known basis states $|0\rangle, |1\rangle$ can be copied:*
     The proof breaks down when the set of states to be copied are mutually orthogonal (such as classical bits $\{0, 1\}$). A CNOT gate with target $|0\rangle$ maps $|00\rangle \mapsto |00\rangle$ and $|10\rangle \mapsto |11\rangle$, perfectly copying the orthogonal basis states. No-cloning forbids copying non-orthogonal superpositions where relative phases matter.

---

### Question 29
**Question:**
Which of $\{X, Y, Z, H\}$ are Hermitian and unitary? What does each property mean physically (observable versus gate)? Why must a Hermitian unitary matrix have eigenvalues $\pm 1$, and why is it automatically its own inverse? Is every unitary gate Hermitian? Justify with a counterexample. Which maps $|0\rangle$ to an equal superposition, and does this gate change the measurement statistics of $|0\rangle$ in the computational basis?

**Solution:**
1. **Hermitian and Unitary Classification:**
   The matrices are:
   $$X = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}, \quad Y = \begin{pmatrix} 0 & -i \\ i & 0 \end{pmatrix}, \quad Z = \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}, \quad H = \frac{1}{\sqrt{2}}\begin{pmatrix} 1 & 1 \\ 1 & -1 \end{pmatrix}$$
   - **All four matrices $\{X, Y, Z, H\}$ are BOTH Hermitian ($A = A^\dagger$) AND Unitary ($A^\dagger A = I$).**
   - **Physical Meaning:**
     - **Hermitian ($A = A^\dagger$):** Represents a physical **observable** (a measurable quantity with real eigenvalues).
     - **Unitary ($U^\dagger U = I$):** Represents a valid **quantum gate** (a reversible time-evolution that preserves total probability).
     - Being both means these operators can serve simultaneously as measurable physical observables and as reversible logic gates.

2. **Why Hermitian Unitary Matrices Have Eigenvalues $\pm 1$ and Are Self-Inverse:**
   - Because $A$ is unitary: $A^\dagger A = I$.
   - Because $A$ is Hermitian: $A^\dagger = A$.
   - Substituting $A^\dagger = A$ into the unitary condition:
     $$A \cdot A = A^2 = I$$
     Thus $A = A^{-1}$, meaning **$A$ is automatically its own inverse**.
   - If $\lambda$ is an eigenvalue of $A$ with eigenvector $v$ ($A v = \lambda v$):
     $$A^2 v = \lambda^2 v = I v = v \implies \lambda^2 = 1 \implies \lambda = \pm 1$$
     Every eigenvalue must be $+1$ or $-1$.

3. **Is Every Unitary Gate Hermitian?**
   **No!**
   - **Counterexample:** The Phase gate $S$:
     $$S = \begin{pmatrix} 1 & 0 \\ 0 & i \end{pmatrix}$$
     $$S^\dagger = \begin{pmatrix} 1 & 0 \\ 0 & -i \end{pmatrix} \ne S$$
     $S$ is unitary ($S^\dagger S = I$), but it is **not Hermitian** because its eigenvalues are $\{1, i\}$, which are not real. Another counterexample is the $T$ gate.

4. **Gate Mapping $|0\rangle$ to Equal Superposition:**
   The **Hadamard gate $H$** maps $|0\rangle$ to an equal superposition:
   $$H|0\rangle = \frac{1}{\sqrt{2}}\begin{pmatrix} 1 & 1 \\ 1 & -1 \end{pmatrix}\begin{pmatrix} 1 \\ 0 \end{pmatrix} = \frac{1}{\sqrt{2}}\begin{pmatrix} 1 \\ 1 \end{pmatrix} = \frac{|0\rangle + |1\rangle}{\sqrt{2}} = |+\rangle$$
   - **Measurement Statistics in Computational Basis:**
     - Before applying $H$: state is $|0\rangle \implies P(0) = 1, P(1) = 0$.
     - After applying $H$: state is $|+\rangle \implies P(0) = |1/\sqrt{2}|^2 = 0.5, P(1) = |1/\sqrt{2}|^2 = 0.5$.
     **Yes, the Hadamard gate fundamentally changes the measurement statistics of $|0\rangle$ from a deterministic outcome to an unbiased 50/50 coin flip.**

---

### Question 30
**Question:**
Consider the normalized state
$$|\psi\rangle = \frac{3}{5} |0\rangle + \frac{4}{5} |1\rangle, \qquad |\pm\rangle = \frac{|0\rangle \pm |1\rangle}{\sqrt{2}}$$
(a) Identify the computational-basis amplitudes.
(b) Find $P(0)$ and $P(1)$.
(c) Compute $\langle+|\psi\rangle, \langle-|\psi\rangle$ and the measurement probabilities $P(+)$ and $P(-)$. Verify that probabilities sum to one in either basis.
(d) Explain the difference between an amplitude and a probability. Why does the same state give different outcome distributions in the two bases, and what does this say about the information carried by $P(0), P(1)$ alone?

**Solution:**
1. **(a) Computational-Basis Amplitudes:**
   Comparing $|\psi\rangle = c_0 |0\rangle + c_1 |1\rangle$:
   $$c_0 = \frac{3}{5} = 0.6, \qquad c_1 = \frac{4}{5} = 0.8$$

2. **(b) Probabilities $P(0)$ and $P(1)$:**
   By Born's rule:
   $$P(0) = |c_0|^2 = \left(\frac{3}{5}\right)^2 = \frac{9}{25} = 0.36$$
   $$P(1) = |c_1|^2 = \left(\frac{4}{5}\right)^2 = \frac{16}{25} = 0.64$$
   Check: $P(0) + P(1) = 0.36 + 0.64 = 1.00 \quad \checkmark$.

3. **(c) Projections and Probabilities in the $X$-basis:**
   $|\pm\rangle = \frac{1}{\sqrt{2}}|0\rangle \pm \frac{1}{\sqrt{2}}|1\rangle \implies \langle\pm| = \frac{1}{\sqrt{2}}\langle 0| \pm \frac{1}{\sqrt{2}}\langle 1|$.
   - Amplitude $\langle+|\psi\rangle$:
     $$\langle+|\psi\rangle = \frac{1}{\sqrt{2}}\left(\frac{3}{5}\right) + \frac{1}{\sqrt{2}}\left(\frac{4}{5}\right) = \frac{7}{5\sqrt{2}}$$
     $$P(+) = |\langle+|\psi\rangle|^2 = \left(\frac{7}{5\sqrt{2}}\right)^2 = \frac{49}{25 \times 2} = \frac{49}{50} = 0.98$$
   - Amplitude $\langle-|\psi\rangle$:
     $$\langle-|\psi\rangle = \frac{1}{\sqrt{2}}\left(\frac{3}{5}\right) - \frac{1}{\sqrt{2}}\left(\frac{4}{5}\right) = \frac{-1}{5\sqrt{2}}$$
     $$P(-) = |\langle-|\psi\rangle|^2 = \left(\frac{-1}{5\sqrt{2}}\right)^2 = \frac{1}{25 \times 2} = \frac{1}{50} = 0.02$$
   Check: $P(+) + P(-) = 0.98 + 0.02 = 1.00 \quad \checkmark$.

4. **(d) Amplitude vs Probability and Phase Information:**
   - **Amplitude:** A complex number $c_i \in \mathbb{C}$ carrying both **magnitude** $|c_i|$ and **phase** $\arg(c_i)$. Amplitudes interfere constructively and destructively.
   - **Probability:** A real non-negative number $P = |c_i|^2 \in [0, 1]$ representing observable frequency.
   - **Why distributions differ:** In the computational basis, the probabilities depend only on the individual magnitudes ($0.36$ and $0.64$). In the $|\pm\rangle$ basis, the amplitudes add linearly *before* squaring: $\frac{c_0 + c_1}{\sqrt{2}}$. Because $c_0$ and $c_1$ share the same positive sign, they interfere **constructively** in $|+\rangle$ giving $98\%$, and **destructively** in $|-\rangle$ giving only $2\%$.
   - **Information limit of $P(0), P(1)$:** Knowing $P(0) = 0.36$ and $P(1) = 0.64$ reveals only $|c_0|$ and $|c_1|$, but completely loses their relative phase. A state like $\frac{3}{5}|0\rangle - \frac{4}{5}|1\rangle$ has the identical $P(0), P(1)$ but gives $P(+) = 0.02$ and $P(-) = 0.98$. $P(0)$ and $P(1)$ alone do not uniquely specify a quantum state.

---

### Question 31
**Question:**
Compare the two states
$$|\psi_1\rangle = \frac{|0\rangle + |1\rangle}{\sqrt{2}}, \qquad |\psi_2\rangle = \frac{|0\rangle + i |1\rangle}{\sqrt{2}}$$
Find $P(0)$ and $P(1)$ for both states. Then find $P(+)$ for each and explain why relative phase may affect measurements in a different basis. Distinguish a global phase from a relative phase: show that $e^{i\theta} |\psi_1\rangle$ is physically indistinguishable from $|\psi_1\rangle$, but $|\psi_2\rangle$ is not. Name a measurement basis in which $|\psi_1\rangle$ and $|\psi_2\rangle$ can be told apart with certainty on a single shot, or argue that none exists.

**Solution:**
1. **Computational-Basis Probabilities $P(0)$ and $P(1)$:**
   - For $|\psi_1\rangle$: $c_0 = 1/\sqrt{2}, c_1 = 1/\sqrt{2}$.
     $$P_1(0) = |1/\sqrt{2}|^2 = 0.5, \qquad P_1(1) = |1/\sqrt{2}|^2 = 0.5$$
   - For $|\psi_2\rangle$: $c_0 = 1/\sqrt{2}, c_1 = i/\sqrt{2}$.
     $$P_2(0) = |1/\sqrt{2}|^2 = 0.5, \qquad P_2(1) = |i/\sqrt{2}|^2 = 0.5$$
   In the computational basis, both states yield **identical 50/50 statistics**.

2. **$X$-Basis Probability $P(+)$:**
   Recall $|+\rangle = \frac{|0\rangle + |1\rangle}{\sqrt{2}}$.
   - For $|\psi_1\rangle$:
     $$\langle+|\psi_1\rangle = \left(\frac{1}{\sqrt{2}}\right)\left(\frac{1}{\sqrt{2}}\right) + \left(\frac{1}{\sqrt{2}}\right)\left(\frac{1}{\sqrt{2}}\right) = \frac{1}{2} + \frac{1}{2} = 1$$
     $$P_1(+) = |1|^2 = 1.0 \quad (100\%)$$
   - For $|\psi_2\rangle$:
     $$\langle+|\psi_2\rangle = \left(\frac{1}{\sqrt{2}}\right)\left(\frac{1}{\sqrt{2}}\right) + \left(\frac{1}{\sqrt{2}}\right)\left(\frac{i}{\sqrt{2}}\right) = \frac{1 + i}{2}$$
     $$P_2(+) = \left| \frac{1 + i}{2} \right|^2 = \frac{1^2 + 1^2}{4} = \frac{2}{4} = 0.5 \quad (50\%)$$
   - **Why relative phase affects measurements:**
     The relative phase $\phi$ in $|0\rangle + e^{i\phi}|1\rangle$ governs how the amplitudes combine during a basis change. In the $X$-basis, amplitudes add as $1 + e^{i\phi}$. For $|\psi_1\rangle$ ($\phi = 0$), $1 + 1 = 2$ gives full constructive interference. For $|\psi_2\rangle$ ($\phi = \pi/2$), $1 + i$ yields partial interference ($|1+i|^2/4 = 1/2$).

3. **Global Phase vs Relative Phase:**
   - **Global Phase ($e^{i\theta}|\psi_1\rangle$):**
     Multiplying the entire vector by $e^{i\theta}$ leaves all measurement probabilities invariant across all possible bases $\{|m\rangle\}$:
     $$|\langle m | (e^{i\theta}|\psi_1\rangle) |^2 = |e^{i\theta}|^2 |\langle m | \psi_1 \rangle|^2 = 1 \cdot |\langle m | \psi_1 \rangle|^2 = |\langle m | \psi_1 \rangle|^2$$
     Therefore $e^{i\theta}|\psi_1\rangle$ is **physically indistinguishable** from $|\psi_1\rangle$.
   - **Relative Phase ($|\psi_2\rangle$ vs $|\psi_1\rangle$):**
     In $|\psi_2\rangle$, the factor $i = e^{i\pi/2}$ multiplies only $|1\rangle$. As proven above, $P(+) = 1.0$ for $|\psi_1\rangle$ while $P(+) = 0.5$ for $|\psi_2\rangle$. This is an experimentally observable difference, proving they are **physically distinct states**.

4. **Can They Be Told Apart with Certainty on a Single Shot?**
   **No single-shot measurement basis exists that distinguishes them with 100% certainty.**
   *Proof:* Two pure states can be distinguished with certainty on a single shot if and only if they are **mutually orthogonal** ($\langle\psi_1|\psi_2\rangle = 0$).
   Computing the inner product:
   $$\langle\psi_1|\psi_2\rangle = \left(\frac{\langle 0| + \langle 1|}{\sqrt{2}}\right) \left(\frac{|0\rangle + i|1\rangle}{\sqrt{2}}\right) = \frac{1 + i}{2} \ne 0$$
   Because $|\langle\psi_1|\psi_2\rangle| = \frac{1}{\sqrt{2}} \approx 0.7071 \ne 0$, they are not orthogonal.
   (However, measuring in the $X$-basis can rule out $|\psi_1\rangle$ if outcome $|-\rangle$ is obtained, since $P_1(-) = 0$ while $P_2(-) = 0.5$).

---

### Question 32
**Question:**
Consider a qubit initially in the state $|0\rangle = \begin{pmatrix} 1 \\ 0 \end{pmatrix}$.
(a) Apply the Hadamard gate $H$ and determine the output state.
(b) Apply the Pauli-$X$ gate to the output obtained in part (a).
(c) Explain the physical meaning of the final state. Why is the output of (a) unchanged by $X$ (what kind of vector is it for $X$)? Interpret $H$ and $X$ as rotations of the Bloch sphere and say which axis the final state lies on.

**Solution:**
1. **(a) Applying Hadamard Gate $H$ to $|0\rangle$:**
   $$H |0\rangle = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 & 1 \\ 1 & -1 \end{pmatrix} \begin{pmatrix} 1 \\ 0 \end{pmatrix} = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 \\ 1 \end{pmatrix} = \frac{|0\rangle + |1\rangle}{\sqrt{2}} = |+\rangle$$

2. **(b) Applying Pauli-$X$ Gate to Output of (a):**
   $$X |+\rangle = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix} \left( \frac{1}{\sqrt{2}} \begin{pmatrix} 1 \\ 1 \end{pmatrix} \right) = \frac{1}{\sqrt{2}} \begin{pmatrix} 0(1) + 1(1) \\ 1(1) + 0(1) \end{pmatrix} = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 \\ 1 \end{pmatrix} = |+\rangle$$
   The resulting state is still $|+\rangle$.

3. **(c) Physical Meaning and Eigenvector Interpretation:**
   - **Eigenvector of $X$:**
     $X |+\rangle = 1 \cdot |+\rangle$. The state $|+\rangle$ is an **eigenvector of the Pauli-$X$ operator with eigenvalue $+1$**.
     Because applying an operator to one of its eigenvectors scales it by its eigenvalue (here $\lambda = +1$), the state is completely invariant under the action of $X$.
   - **Bloch Sphere Rotation Interpretation:**
     - The initial state $|0\rangle$ lies at the **North Pole** ($+z$ axis).
     - The Hadamard gate $H = \frac{X + Z}{\sqrt{2}}$ represents a $180^\circ$ ($\pi$-radian) rotation around the diagonal $(x + z)$ axis. This rotation swings the state vector from the North Pole ($+z$) down to the equator, landing precisely on the **positive $x$-axis** ($|+\rangle$).
     - The Pauli-$X$ gate represents a $180^\circ$ rotation around the **$x$-axis**.
     - Because the state $|+\rangle$ already lies directly along the axis of rotation ($+x$ axis), rotating around the $x$-axis leaves the state vector completely stationary.

---

### Question 33
**Question:**
A qubit is initialized in the state $|1\rangle = \begin{pmatrix} 0 \\ 1 \end{pmatrix}$.
(a) Apply the Hadamard gate $H$ to the qubit.
(b) Apply the Pauli-$X$ gate to the resulting state and simplify.
(c) Determine the measurement probabilities of the final state.
(d) Compare with the previous question: are the final states of the two circuits the same physical state? Can they be distinguished by a computational-basis measurement? By an $X$-basis ($|\pm\rangle$) measurement? Explain the role of the minus sign.

**Solution:**
1. **(a) Applying Hadamard Gate $H$ to $|1\rangle$:**
   $$H |1\rangle = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 & 1 \\ 1 & -1 \end{pmatrix} \begin{pmatrix} 0 \\ 1 \end{pmatrix} = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 \\ -1 \end{pmatrix} = \frac{|0\rangle - |1\rangle}{\sqrt{2}} = |-\rangle$$

2. **(b) Applying Pauli-$X$ Gate to $|-\rangle$:**
   $$X |-\rangle = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix} \left( \frac{1}{\sqrt{2}} \begin{pmatrix} 1 \\ -1 \end{pmatrix} \right) = \frac{1}{\sqrt{2}} \begin{pmatrix} -1 \\ 1 \end{pmatrix} = -\left( \frac{|0\rangle - |1\rangle}{\sqrt{2}} \right) = -|-\rangle$$
   Notice that $X |-\rangle = -1 \cdot |-\rangle$ (an eigenstate with eigenvalue $-1$).

3. **(c) Measurement Probabilities of Final State:**
   The final state is $|\psi_{\text{final}}\rangle = -|-\rangle = -\frac{1}{\sqrt{2}}|0\rangle + \frac{1}{\sqrt{2}}|1\rangle$.
   - **Computational basis:**
     $$P(0) = |(-1/\sqrt{2})|^2 = \frac{1}{2} = 0.5, \qquad P(1) = |(1/\sqrt{2})|^2 = \frac{1}{2} = 0.5$$
   - **$X$-basis ($\{|+\rangle, |-\rangle\}$):**
     $$\langle+|\psi_{\text{final}}\rangle = -\langle+ | -\rangle = 0 \implies P(+) = 0$$
     $$\langle-|\psi_{\text{final}}\rangle = -\langle- | -\rangle = -1 \implies P(-) = |-1|^2 = 1.0$$

4. **(d) Comparison with Question 32:**
   - In Q32: initial state was $|0\rangle$, final state after $X H$ was $|+\rangle$.
   - In Q33: initial state was $|1\rangle$, final state after $X H$ is $-|-\rangle$.
   - **Are they the same physical state?**
     **NO.** $|+\rangle$ lies on the $+x$ axis, whereas $-|-\rangle$ (which equals $|-\rangle$ up to an unmeasurable global phase $-1 = e^{i\pi}$) lies on the $-x$ axis. They are **mutually orthogonal**: $\langle + | (-|-\rangle) = 0$.
   - **Computational-basis measurement:** In the computational basis, both states yield identical $P(0) = 0.5, P(1) = 0.5$, so they **cannot** be distinguished in this basis.
   - **$X$-basis measurement:** In the $X$-basis, Q32 gives outcome $|+\rangle$ with **100% probability**, whereas Q33 gives outcome $|-\rangle$ with **100% probability**. They can be distinguished **with 100% certainty on a single shot**.
   - **Role of the minus sign:** The global minus sign $-|-\rangle = e^{i\pi}|-\rangle$ has no physical consequence by itself, but the internal relative minus sign in $|-\rangle = \frac{|0\rangle - |1\rangle}{\sqrt{2}}$ represents a $180^\circ$ phase shift that causes complete destructive interference in the $|+\rangle$ projection and constructive interference in the $|-\rangle$ projection.

---

# Section B: Computational & Programming Questions (Questions 1 to 13)

### Question B1
**Question:**
Given $A = \begin{pmatrix} 2 & 1 & 0 \\ 0 & 1 & 1 \\ 1 & 0 & 2 \end{pmatrix}$, $B = \begin{pmatrix} 3 & 1 & 1 \\ 1 & 2 & 1 \\ 2 & 1 & 3 \end{pmatrix}$ as snapshots at $t_1, t_2$, compute the best-fit Koopman operator $K = B A^\dagger$, predict and display $C = K B$ at $t_3$. Also compute $\text{rank}(A)$ and decide whether $A^\dagger = A^{-1}$ here. Compute the eigenvalues of $K$ and state, from their magnitudes, whether the predicted dynamics grow, decay or oscillate. In a comment, explain why $K = B A^\dagger$ is the least-squares solution of $K A \approx B$.

**Solution & Code:**
1. **Mathematical Derivation:**
   - Determinant of $A$:
     $$\det(A) = 2(1 \cdot 2 - 1 \cdot 0) - 1(0 \cdot 2 - 1 \cdot 1) + 0 = 2(2) - 1(-1) = 4 + 1 = 5 \ne 0$$
   - Since $\det(A) = 5 \ne 0$, $A$ is non-singular with $\text{rank}(A) = 3$ (full rank). Therefore, $A^\dagger = A^{-1}$.
   - Inverse $A^{-1}$:
     $$A^{-1} = \frac{1}{5} \begin{pmatrix} 2 & -2 & 1 \\ 1 & 4 & -2 \\ -1 & 1 & 2 \end{pmatrix} = \begin{pmatrix} 0.4 & -0.4 & 0.2 \\ 0.2 & 0.8 & -0.4 \\ -0.2 & 0.2 & 0.4 \end{pmatrix}$$
   - Koopman Operator $K = B A^{-1}$:
     $$K = \begin{pmatrix} 3 & 1 & 1 \\ 1 & 2 & 1 \\ 2 & 1 & 3 \end{pmatrix} \begin{pmatrix} 0.4 & -0.4 & 0.2 \\ 0.2 & 0.8 & -0.4 \\ -0.2 & 0.2 & 0.4 \end{pmatrix} = \begin{pmatrix} 1.2 & -0.2 & 0.6 \\ 0.6 & 1.4 & -0.2 \\ 0.4 & 0.6 & 1.2 \end{pmatrix}$$
   - Predicted Snapshot $C = K B$ at $t_3$:
     $$C = \begin{pmatrix} 1.2 & -0.2 & 0.6 \\ 0.6 & 1.4 & -0.2 \\ 0.4 & 0.6 & 1.2 \end{pmatrix} \begin{pmatrix} 3 & 1 & 1 \\ 1 & 2 & 1 \\ 2 & 1 & 3 \end{pmatrix} = \begin{pmatrix} 4.6 & 1.4 & 2.8 \\ 2.8 & 3.2 & 1.4 \\ 4.2 & 2.8 & 4.6 \end{pmatrix}$$
   - Eigenvalues of $K$:
     $$\lambda_1 \approx 1.8439, \qquad \lambda_{2, 3} \approx 0.9781 \pm 0.4863 i$$
     Magnitudes: $|\lambda_1| = 1.8439 > 1$, $|\lambda_{2, 3}| = \sqrt{0.9781^2 + 0.4863^2} \approx 1.0923 > 1$.
     *Dynamics Interpretation:* Because the eigenvalues have magnitudes strictly greater than 1 ($|\lambda_i| > 1$), the system exhibits **growing (unstable) oscillatory dynamics** over time.
   - *Least-Squares Justification:* $K = B A^\dagger$ minimizes the Frobenius norm $\|K A - B\|_F^2 = \sum_j \|K a_j - b_j\|_2^2$. Taking the matrix derivative with respect to $K$ and setting to zero: $(K A - B) A^T = 0 \implies K (A A^T) = B A^T \implies K = B A^\dagger$.

```python
import numpy as np

A = np.array([[2, 1, 0], [0, 1, 1], [1, 0, 2]], dtype=float)
B = np.array([[3, 1, 1], [1, 2, 1], [2, 1, 3]], dtype=float)

# Rank and inverse check
r = np.linalg.matrix_rank(A)
is_invertible = (r == A.shape[0])
A_pinv = np.linalg.pinv(A)
A_inv = np.linalg.inv(A)

# Koopman operator K and prediction C
K = B @ A_pinv
C = K @ B

# Eigenvalues
evals = np.linalg.eigvals(K)
magnitudes = np.abs(evals)

print(f"Rank(A): {r}, Invertible: {is_invertible}")
print(f"Koopman operator K:\n{K}")
print(f"Predicted snapshot C at t3:\n{C}")
print(f"Eigenvalues of K: {evals}")
print(f"Magnitudes: {magnitudes}")
# Dynamics: Growing because max magnitude > 1
```

---

### Question B2
**Question:**
For the rectangular snapshots $A = \begin{pmatrix} 1 & 2 & 0 & 1 \\ 0 & 1 & 1 & 2 \\ 1 & 0 & 2 & 1 \end{pmatrix}$, $B = \begin{pmatrix} 2 & 3 & 1 & 2 \\ 1 & 1 & 3 & 2 \\ 2 & 2 & 2 & 3 \end{pmatrix}$, compute $K = B A^\dagger$ using the pseudoinverse, display $K$, $C = K B$, and the fit error $\|K A - B\|_F$. Verify the Moore–Penrose conditions for $A^\dagger$ numerically. Explain, using $\text{rank}(A)$ and the column space of $A$, why the fit error is (or is not) zero, and why $K$ is not unique when $A$ is rank deficient (which solution does the pseudoinverse select?).

**Solution & Code:**
1. **Mathematical Derivation:**
   - Dimensions of $A$: $3 \times 4$.
   - Rows of $A$: Row 1 + Row 2 = $(1, 3, 1, 3)$; Row 3 = $(1, 0, 2, 1)$. The rows are linearly independent, so $\text{rank}(A) = 3$.
   - Because $A$ has full row rank ($m = 3 \le n = 4$):
     $$A A^\dagger = I_3$$
     Right inverse: $A^\dagger = A^T (A A^T)^{-1}$.
   - Fit Error $\|K A - B\|_F$:
     $$K A - B = (B A^\dagger) A - B = B (A^\dagger A) - B = B (A^\dagger A - I_4)$$
     Since $A$ has 4 columns but rank 3, $A^\dagger A \ne I_4$ (it is a rank-3 projector in $\mathbb{R}^4$).
     Therefore $B A^\dagger A \ne B$ in general, resulting in a non-zero residual fit error $\|K A - B\|_F \approx 0.7071$.
   - *Why $K$ is non-unique and what $A^\dagger$ selects:*
     The system $K A \approx B$ is underdetermined in the column space of $K^T$ because $A$ has a 1-dimensional nullspace $\mathcal{N}(A)$. Any matrix $K_0$ whose rows lie in $\mathcal{N}(A)^T$ satisfies $K_0 A = 0$. Thus $K + K_0$ achieves the exact same fit error. The Moore-Penrose pseudoinverse $K = B A^\dagger$ uniquely selects the solution with the **minimum Frobenius norm $\|K\|_F$**.

```python
import numpy as np

A = np.array([[1, 2, 0, 1], [0, 1, 1, 2], [1, 0, 2, 1]], dtype=float)
B = np.array([[2, 3, 1, 2], [1, 1, 3, 2], [2, 2, 2, 3]], dtype=float)

A_pinv = np.linalg.pinv(A)
K = B @ A_pinv
C = K @ B
fit_error = np.linalg.norm(K @ A - B, 'fro')

# Moore-Penrose verification
mp1 = np.linalg.norm(A @ A_pinv @ A - A)
mp2 = np.linalg.norm(A_pinv @ A @ A_pinv - A_pinv)
mp3 = np.linalg.norm((A @ A_pinv).T - A @ A_pinv)
mp4 = np.linalg.norm((A_pinv @ A).T - A_pinv @ A)

print(f"Rank of A: {np.linalg.matrix_rank(A)}")
print(f"Koopman operator K:\n{K}")
print(f"Predicted snapshot C:\n{C}")
print(f"Frobenius fit error: {fit_error:.6f}")
print(f"MP Checks (should be ~0): MP1={mp1:.1e}, MP2={mp2:.1e}, MP3={mp3:.1e}, MP4={mp4:.1e}")
```

---

### Question B3
**Question:**
For the loss $f(x, y) = 3x^2 - 2xy + 2y^2$, compute the Hessian at $(1, 2)$, display its eigenvalues, and classify it as positive definite, negative definite or indefinite. Relate the eigenvalues to convexity of $f$ and to the shape of its level sets. Compute the condition number and the largest stable gradient-descent step $2/\lambda_{\max}$; run a few gradient-descent steps with one stable and one unstable $\alpha$ to confirm.

**Solution & Code:**
1. **Mathematical Derivation:**
   $$f(x, y) = 3x^2 - 2xy + 2y^2$$
   - Gradient: $\nabla f(x, y) = \begin{pmatrix} 6x - 2y \\ -2x + 4y \end{pmatrix}$.
   - Hessian:
     $$H = \begin{pmatrix} 6 & -2 \\ -2 & 4 \end{pmatrix}$$
     $H$ is constant everywhere (including at $(1, 2)$).
   - Eigenvalues:
     $$\det(H - \lambda I) = (6 - \lambda)(4 - \lambda) - 4 = \lambda^2 - 10\lambda + 20 = 0$$
     $$\lambda = \frac{10 \pm \sqrt{100 - 80}}{2} = \frac{10 \pm \sqrt{20}}{2} = 5 \pm \sqrt{5}$$
     $$\lambda_1 = 5 + \sqrt{5} \approx 7.2361, \qquad \lambda_2 = 5 - \sqrt{5} \approx 2.7639$$
   - Classification: Both $\lambda_1, \lambda_2 > 0 \implies H$ is **positive definite** ($H \succ 0$). Therefore $f$ is **strictly convex**.
   - Level sets: $3x^2 - 2xy + 2y^2 = c$ are **ellipses** centered at $(0, 0)$. The principal axes align with the eigenvectors of $H$, with aspect ratio $\sqrt{\lambda_1/\lambda_2} \approx \sqrt{2.618} \approx 1.618$.
   - Condition number:
     $$\kappa = \frac{\lambda_{\max}}{\lambda_{\min}} = \frac{5 + \sqrt{5}}{5 - \sqrt{5}} \approx \frac{7.2361}{2.7639} \approx 2.618$$
   - Stability Limit:
     $$\alpha_{\max} = \frac{2}{\lambda_{\max}} = \frac{2}{5 + \sqrt{5}} \approx \frac{2}{7.2361} \approx 0.2764$$
   - For stable step: choose $\alpha = 0.2 < 0.2764$ (converges).
   - For unstable step: choose $\alpha = 0.35 > 0.2764$ (diverges with oscillating explosion).

```python
import numpy as np

H = np.array([[6, -2], [-2, 4]], dtype=float)
evals, evecs = np.linalg.eigh(H)
l_min, l_max = evals[0], evals[1]
cond_num = l_max / l_min
alpha_stable_bound = 2.0 / l_max

print(f"Eigenvalues: {l_min:.4f}, {l_max:.4f}")
print(f"Condition number: {cond_num:.4f}")
print(f"Max stable step size alpha_max: {alpha_stable_bound:.4f}")

def run_gd(alpha, steps=5):
    pt = np.array([1.0, 2.0])
    print(f"\n--- Running GD with alpha = {alpha} ---")
    for s in range(steps):
        grad = np.array([6*pt[0] - 2*pt[1], -2*pt[0] + 4*pt[1]])
        pt = pt - alpha * grad
        loss = 3*pt[0]**2 - 2*pt[0]*pt[1] + 2*pt[1]**2
        print(f"Step {s+1}: pt = [{pt[0]:.4f}, {pt[1]:.4f}], loss = {loss:.4f}")

run_gd(alpha=0.20)  # Stable
run_gd(alpha=0.35)  # Unstable
```

---

### Question B4
**Question:**
For the loss $f(x, y) = x^3 + 2y^3 - 3xy$, compute the gradient and Hessian symbolically, evaluate the Hessian at $(1, 1)$, print its eigenvalues and classify it. Find all critical points and classify each. Explain why the second-order test is conclusive at some of them, and why a local minimum of $f$ here is not a global minimum.

**Solution & Code:**
1. **Mathematical Derivation:**
   $$f(x, y) = x^3 + 2y^3 - 3xy$$
   - Gradient:
     $$\nabla f(x, y) = \begin{pmatrix} 3x^2 - 3y \\ 6y^2 - 3x \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \end{pmatrix}$$
     From first equation: $3y = 3x^2 \implies y = x^2$.
     Substitute into second: $6(x^2)^2 - 3x = 0 \implies 3x(2x^3 - 1) = 0$.
     Real critical points:
     1. $x = 0 \implies y = 0 \implies (0, 0)$
     2. $x = (1/2)^{1/3} = 2^{-1/3} \approx 0.7937 \implies y = x^2 = 2^{-2/3} \approx 0.6300 \implies (2^{-1/3}, 2^{-2/3})$
   - Hessian:
     $$H(x, y) = \begin{pmatrix} 6x & -3 \\ -3 & 12y \end{pmatrix}$$
     Determinant: $\det(H) = 72xy - 9$.
   - **Classification of Critical Points:**
     - **At $(0, 0)$:**
       $H(0, 0) = \begin{pmatrix} 0 & -3 \\ -3 & 0 \end{pmatrix}$.
       $\det(H) = -9 < 0$. Eigenvalues are $\pm 3$.
       Because $\det(H) < 0$, $(0, 0)$ is a **Saddle Point**.
     - **At $(2^{-1/3}, 2^{-2/3})$:**
       $xy = 2^{-1/3} \cdot 2^{-2/3} = 2^{-1} = 0.5$.
       $\det(H) = 72(0.5) - 9 = 36 - 9 = 27 > 0$.
       $H_{11} = 6(2^{-1/3}) \approx 4.76 > 0$.
       Because $\det(H) > 0$ and $H_{11} > 0$, the Hessian is positive definite ($H \succ 0$).
       Therefore $(2^{-1/3}, 2^{-2/3})$ is a **strict Local Minimum**.
   - **At $(1, 1)$:**
     $H(1, 1) = \begin{pmatrix} 6 & -3 \\ -3 & 12 \end{pmatrix}$.
     $\det(H) = 72 - 9 = 63 > 0, H_{11} = 6 > 0 \implies$ Positive definite.
     Eigenvalues: $\lambda \approx 4.757, 13.243$.
   - **Why the Local Minimum is NOT a Global Minimum:**
     Along the line $y = 0$, $f(x, 0) = x^3$.
     As $x \to -\infty$, $f(x, 0) = x^3 \to -\infty$.
     The function is **unbounded below**, so no finite global minimum exists.

```python
import sympy as sp

x, y = sp.symbols('x y', real=True)
f = x**3 + 2*y**3 - 3*x*y

grad = [sp.diff(f, x), sp.diff(f, y)]
H = sp.hessian(f, (x, y))

# Critical points
crit_pts = sp.solve(grad, (x, y))
print(f"Real Critical Points: {crit_pts}")

for pt in crit_pts:
    H_pt = H.subs({x: pt[0], y: pt[1]})
    det_val = H_pt.det()
    tr_val = H_pt.trace()
    eigs = [complex(e.evalf()) for e in H_pt.eigenvals().keys()]
    print(f"\nPoint {pt}:")
    print(f"  Hessian:\n{H_pt}")
    print(f"  det(H): {det_val}, Eigenvalues: {eigs}")
    if det_val < 0:
        print("  -> SADDLE POINT")
    elif det_val > 0 and H_pt[0,0] > 0:
        print("  -> LOCAL MINIMUM")
```

---

### Questions B5 & B6: Characteristics for First-Order PDEs
**Question B5:**
Compute and display the general solution $u(x, y)$ of $u_x + 2u_y = x^2$ using symbolic computation, and verify by substituting back that the residual is zero. Identify the characteristic curves, state what quantity is constant along them, and explain why the general solution contains an arbitrary function. What extra data would pin down a unique solution?

**Solution B5:**
- Characteristic equations: $\frac{dx}{1} = \frac{dy}{2} = \frac{du}{x^2}$.
- From $\frac{dy}{dx} = 2 \implies y - 2x = C_1$.
  The characteristic curves are parallel lines $y - 2x = \text{constant}$. Along each line, the quantity $\xi = y - 2x$ is constant.
- Along the characteristic curve, $\frac{du}{dx} = x^2 \implies u = \frac{x^3}{3} + C_2$.
- The integration constant $C_2$ can be any function of the characteristic curve label $C_1$:
  $$u(x, y) = \frac{x^3}{3} + f(y - 2x)$$
- *Verification:*
  $u_x = x^2 - 2f'(y - 2x)$, $u_y = f'(y - 2x)$.
  $u_x + 2u_y = [x^2 - 2f'] + 2[f'] = x^2$. Residual $= 0$.
- *Why arbitrary function:* A 1st-order PDE only dictates how $u$ changes *along* characteristic trajectories; it imposes no restriction on how the baseline value changes *across* different characteristic lines.
- *Extra data:* A boundary condition along a curve non-tangent to the characteristics, e.g. $u(0, y) = g(y)$ (Cauchy condition).

**Question B6:**
Compute and display the general solution of $3u_x - u_y = y + 1$ symbolically and verify it by substitution.

**Solution B6:**
- Characteristic equations: $\frac{dx}{3} = \frac{dy}{-1} = \frac{du}{y + 1}$.
- From $\frac{dx}{dy} = -3 \implies x + 3y = C_1$.
- Along characteristics: $\frac{du}{dy} = -(y + 1) \implies u = -\frac{y^2}{2} - y + f(C_1)$.
- General solution:
  $$u(x, y) = -\frac{y^2}{2} - y + f(x + 3y)$$
- Verification: $u_x = f'(x+3y)$, $u_y = -y - 1 + 3f'(x+3y)$.
  $3u_x - u_y = 3f' - (-y - 1 + 3f') = y + 1$. Exactly satisfied.

---

### Questions B7 & B8: FTCS Scheme, Stability & Amplification Factor
**Question B7:**
Three grid points have $u_{i-1} = 0.2, u_i = 0.3, u_{i+1} = 0.15$ (outer values held fixed), with $r = 0.5$. Use the FTCS formula to compute and display the central value up to $u_i^3$. Explain why FTCS is an explicit scheme and what $r = k/h^2$ measures. Show that for $r \le 1/2$, the update is a weighted average with non-negative weights and state what this implies about the maximum principle.

**Solution B7:**
- FTCS formula: $u_i^{n+1} = r u_{i-1}^n + (1 - 2r) u_i^n + r u_{i+1}^n$.
- For $r = 0.5$, the middle weight $1 - 2r = 1 - 2(0.5) = 0$.
  $$u_i^{n+1} = 0.5 u_{i-1}^n + 0.5 u_{i+1}^n$$
- Outer values fixed: $u_{i-1} = 0.2, u_{i+1} = 0.15$.
  - Time step 1: $u_i^1 = 0.5(0.2) + 0.5(0.15) = 0.1 + 0.075 = 0.175$.
  - Time step 2: $u_i^2 = 0.5(0.2) + 0.5(0.15) = 0.175$.
  - Time step 3: $u_i^3 = 0.175$.
  The central value snaps to the average of its boundaries ($0.175$) in 1 step and remains constant.
- *Why explicit:* $u_i^{n+1}$ is computed directly using known values from time level $n$, without solving simultaneous equations.
- *Physical meaning of $r$:* Ratio of physical diffusion distance to grid cell dimension.
- *Maximum Principle:* When $r \le 1/2$, the weights $(r, 1-2r, r)$ are all $\ge 0$ and sum to 1. $u_i^{n+1}$ is a convex combination of neighbors, guaranteeing $\min(u^n) \le u_i^{n+1} \le \max(u^n)$. No unphysical local extrema can arise.

**Question B8:**
Take $N = 10$ intervals on $[0, 1]$, $u(x, 0) = 1$ at midpoint and 0 elsewhere, with zero ends. Run 20 FTCS steps for $r = 0.4$ and $r = 0.6$. Print max $|u|$ and min $u$ for each. Evaluate von Neumann amplification factor $G(\theta) = 1 - 4r \sin^2(\theta/2)$ over $\theta \in [0, \pi]$, report $\max |G|$, and connect it to the observed instability.

**Solution B8:**
- For $r = 0.4$:
  $G(\theta) = 1 - 1.6 \sin^2(\theta/2) \in [1 - 1.6, 1] = [-0.6, 1]$.
  $\max |G(\theta)| = 1.0 \le 1$.
  The numerical solution is stable, diffusing smoothly: $\max |u| \to 0$, $\min u = 0$.
- For $r = 0.6$:
  $G(\theta) = 1 - 2.4 \sin^2(\theta/2) \in [1 - 2.4, 1] = [-1.4, 1]$.
  At highest spatial frequency $\theta = \pi$: $G(\pi) = -1.4$.
  Because $|G| = 1.4 > 1$, the mode $(-1)^i$ is multiplied by $(-1.4)$ at every time step.
  After 20 steps: $(-1.4)^{20} \approx 833.5$. The solution develops violent, growing, sign-alternating spikes with large negative values ($\min u \ll 0$), violating the maximum principle and blowing up exponentially.

---

### Questions B9 & B10: Gradient Descent Convergence Dynamics
**Question B9:**
Minimise $f(x) = x^2 - 6x + 10$ from $x_0 = 8$ with $\alpha = 0.1$ for 10 iterations. Show numerically that the error contracts by factor $1 - \alpha f''(x^*)$ each step, and predict the number of iterations needed to reach tolerance $10^{-6}$. For what range of $\alpha$ does the iteration converge?

**Solution B9:**
- $f'(x) = 2x - 6 = 2(x - 3)$, $f''(x) = 2$.
  Minimizer: $x^* = 3$.
  Error update: $e_{k+1} = x_{k+1} - 3 = x_k - \alpha(2x_k - 6) - 3 = (1 - 2\alpha)(x_k - 3) = (1 - 2\alpha) e_k$.
  Contraction factor: $1 - \alpha f''(x^*) = 1 - 2(0.1) = 0.8$.
  $e_0 = 8 - 3 = 5$.
  $e_k = 5(0.8)^k$.
- To reach $|e_k| \le 10^{-6}$:
  $$5(0.8)^k \le 10^{-6} \implies 0.8^k \le 2 \times 10^{-7} \implies k \ge \frac{\ln(2 \times 10^{-7})}{\ln(0.8)} \approx \frac{-15.4249}{-0.22314} \approx 69.12$$
  **70 iterations** are needed.
- Convergence range: $|1 - 2\alpha| < 1 \iff -1 < 1 - 2\alpha < 1 \iff 0 < \alpha < 1$.

**Question B10:**
Minimise $f(x, y) = (x - 1)^2 + 4(y + 2)^2$ from $(3, 2)$ with $\alpha \in \{0.1, 0.3, 0.7\}$. Predict convergence using Hessian eigenvalues and $\alpha < 2/\lambda_{\max}$. Explain which coordinate converges slowly and which diverges first.

**Solution B10:**
- Hessian: $H = \begin{pmatrix} 2 & 0 \\ 0 & 8 \end{pmatrix}$.
  Eigenvalues: $\lambda_x = 2, \lambda_y = 8$. Condition number $\kappa = 8/2 = 4$.
  Stability limit: $\alpha_{\max} = \frac{2}{\lambda_{\max}} = \frac{2}{8} = 0.25$.
- Error factors: $\rho_x = 1 - 2\alpha$, $\rho_y = 1 - 8\alpha$.
  - For $\alpha = 0.1 < 0.25$: $\rho_x = 0.8, \rho_y = 0.2$. Both converge. $x$ converges slower ($\rho_x = 0.8$) because $\lambda_x$ is smaller.
  - For $\alpha = 0.3 > 0.25$: $\rho_x = 0.4$ (converges in $x$), but $\rho_y = 1 - 2.4 = -1.4$ ($|\rho_y| > 1$). $y$ diverges with growing oscillations!
  - For $\alpha = 0.7$: $\rho_x = -0.4$ (converges in $x$), but $\rho_y = 1 - 5.6 = -4.6$ (explodes violently in $y$).

---

### Questions B11 & B12: Conjugate Direction Method
**Question B11:**
Given $A = \begin{pmatrix} 4 & 0 & 1 \\ 0 & 3 & 1 \\ 1 & 1 & 2 \end{pmatrix}$, $b = (5, 6, 4)^T$, $x_0 = (1, 1, 1)^T$, and $D = \begin{pmatrix} 1 & 0 & 3 \\ 0 & 1 & 4 \\ 0 & 0 & -12 \end{pmatrix}$. Verify $D^T A D$ is diagonal and $A \succ 0$. Run the method and compare with standard basis $e_1, e_2, e_3$.

**Solution B11:**
- Checking $A$-conjugacy:
  $$D^T A D = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 3 & 4 & -12 \end{pmatrix} \begin{pmatrix} 4 & 0 & 1 \\ 0 & 3 & 1 \\ 1 & 1 & 2 \end{pmatrix} \begin{pmatrix} 1 & 0 & 3 \\ 0 & 1 & 4 \\ 0 & 0 & -12 \end{pmatrix} = \begin{pmatrix} 4 & 0 & 0 \\ 0 & 3 & 0 \\ 0 & 0 & 204 \end{pmatrix}$$
  Off-diagonal entries are 0, so the columns of $D$ are **mutually $A$-conjugate**.
- Eigenvalues of $A$: $\approx 1.121, 3.347, 4.532 > 0 \implies A \succ 0$.
- With conjugate directions $D$, the method terminates in **exactly 3 steps with zero residual**.
- With standard basis $e_1, e_2, e_3$, taking 1 step along each axis leaves a non-zero residual because the axes are not $A$-conjugate (cross-terms cause updates to interfere).

**Question B12:**
Given $A = \begin{pmatrix} 5 & 2 \\ 2 & 3 \end{pmatrix}$, $b = (7, 5)^T$, $x_0 = 0$. Start from $e_1, e_2$, build $A$-conjugate directions by Gram-Schmidt in the $A$-inner product, verify $d_0^T A d_1 = 0$, run the method.

**Solution B12:**
- $d_0 = e_1 = \begin{pmatrix} 1 \\ 0 \end{pmatrix}$.
- Gram-Schmidt in $A$-inner product $\langle u, v \rangle_A = u^T A v$:
  $$d_1 = e_2 - \frac{\langle e_2, d_0 \rangle_A}{\langle d_0, d_0 \rangle_A} d_0 = \begin{pmatrix} 0 \\ 1 \end{pmatrix} - \frac{e_2^T A d_0}{d_0^T A d_0} d_0$$
  $d_0^T A d_0 = 5$.
  $e_2^T A d_0 = \begin{pmatrix} 0 & 1 \end{pmatrix} \begin{pmatrix} 5 \\ 2 \end{pmatrix} = 2$.
  $$d_1 = \begin{pmatrix} 0 \\ 1 \end{pmatrix} - \frac{2}{5} \begin{pmatrix} 1 \\ 0 \end{pmatrix} = \begin{pmatrix} -0.4 \\ 1.0 \end{pmatrix}$$
- Check: $d_0^T A d_1 = \begin{pmatrix} 1 & 0 \end{pmatrix} \begin{pmatrix} 5 & 2 \\ 2 & 3 \end{pmatrix} \begin{pmatrix} -0.4 \\ 1.0 \end{pmatrix} = \begin{pmatrix} 5 & 2 \end{pmatrix} \begin{pmatrix} -0.4 \\ 1.0 \end{pmatrix} = -2 + 2 = 0 \quad \checkmark$.
- Running algorithm: Reaches exact solution $x^* = A^{-1}b = \begin{pmatrix} 1 \\ 1 \end{pmatrix}$ in exactly 2 steps.

---

### Question B13: Full SVD-Based DMD Implementation
**Question B13:**
Implement SVD-based DMD on a synthetic damped oscillation $x(t) = e^{-0.5t}(\cos 2\pi t, \sin 2\pi t)^T$ sampled at $\Delta t = 0.1$. Convert $\lambda$ to $\mu = \ln(\lambda)/\Delta t$ and verify recovered decay rate and frequency.

**Solution & Code:**
```python
import numpy as np

# Generate synthetic dataset
dt = 0.1
t = np.arange(0, 5.0, dt)
X_data = np.array([np.exp(-0.5*t) * np.cos(2*np.pi*t),
                   np.exp(-0.5*t) * np.sin(2*np.pi*t)])

# Step 1: Snapshot matrices
X = X_data[:, :-1]
X_prime = X_data[:, 1:]

# Step 2: SVD
U, S, Vt = np.linalg.svd(X, full_matrices=False)
r = 2  # retain leading 2 modes
Ur = U[:, :r]
Sr = np.diag(S[:r])
Vr = Vt[:r, :].T

# Step 3: Reduced operator A_tilde
A_tilde = Ur.T @ X_prime @ Vr @ np.linalg.inv(Sr)

# Step 4: Eigendecomposition
evals, W = np.linalg.eig(A_tilde)

# Step 5: Exact DMD modes
Phi = X_prime @ Vr @ np.linalg.inv(Sr) @ W

# Step 6: Amplitudes
b = np.linalg.lstsq(Phi, X[:, 0], rcond=None)[0]

# Continuous eigenvalues
mu = np.log(evals) / dt
decay_rate = np.real(mu)
freq_hz = np.abs(np.imag(mu)) / (2 * np.pi)

print("--- DMD Results ---")
print(f"Discrete Eigenvalues: {evals}")
print(f"Continuous Eigenvalues mu: {mu}")
print(f"Recovered Decay Rate: {decay_rate[0]:.4f} (True: -0.5)")
print(f"Recovered Frequency:  {freq_hz[0]:.4f} Hz (True: 1.0 Hz)")
```

---

# Direct Methods Practice Problems

### Problem DM-1: Gradient Descent Consecutive Gradients Orthogonality
**Question:** Prove that in exact line-search gradient descent, consecutive search directions are always orthogonal: $r_k^T r_{k+1} = 0$.
**Solution:**
At step $k$, $\alpha_k$ minimizes $\phi(\alpha) = f(x_k + \alpha r_k)$. Setting $\phi'(\alpha_k) = 0$:
$$\phi'(\alpha_k) = \nabla f(x_k + \alpha_k r_k)^T r_k = \nabla f(x_{k+1})^T r_k = -r_{k+1}^T r_k = 0 \implies r_{k+1}^T r_k = 0$$

### Problem DM-2: Newton's Method on Non-Quadratic $f(x) = x^4$
**Question:** Apply two iterations of Newton's method to $f(x) = x^4$ from $x_0 = 1$.
**Solution:**
$f'(x) = 4x^3, f''(x) = 12x^2$.
Newton update: $x_{k+1} = x_k - \frac{f'(x_k)}{f''(x_k)} = x_k - \frac{4x_k^3}{12x_k^2} = x_k - \frac{1}{3}x_k = \frac{2}{3}x_k$.
- Step 1: $x_1 = \frac{2}{3}(1) = \frac{2}{3} \approx 0.6667$.
- Step 2: $x_2 = \frac{2}{3}\left(\frac{2}{3}\right) = \frac{4}{9} \approx 0.4444$.
*Note:* Because $f$ is not quadratic and $f''(0) = 0$, convergence is linear with factor $2/3$, not quadratic.

---

# WhatsApp Image Practice Problems

### Problem WA-1: Krylov Subspaces and Grade
**Question:** For $A = \begin{pmatrix} 2 & 0 \\ 0 & 5 \end{pmatrix}$ and $b = (1, 1)^T$, write out $\mathcal{K}_1(A, b)$ and $\mathcal{K}_2(A, b)$ explicitly as spans, and state the grade of $b$ with respect to $A$.
**Solution:**
- $\mathcal{K}_1(A, b) = \text{span}\{b\} = \text{span}\left\{ \begin{pmatrix} 1 \\ 1 \end{pmatrix} \right\}$.
- $A b = \begin{pmatrix} 2(1) \\ 5(1) \end{pmatrix} = \begin{pmatrix} 2 \\ 5 \end{pmatrix}$.
  Since $(1, 1)^T$ and $(2, 5)^T$ are linearly independent:
  $$\mathcal{K}_2(A, b) = \text{span}\left\{ \begin{pmatrix} 1 \\ 1 \end{pmatrix}, \begin{pmatrix} 2 \\ 5 \end{pmatrix} \right\} = \mathbb{R}^2$$
- Since $n = 2$ and $\mathcal{K}_2 = \mathbb{R}^2$, the **grade of $b$ with respect to $A$ is $d = 2$**.

### Problem WA-2: Arnoldi Reduction to Lanczos Tridiagonal Form
**Question:** Explain in one or two sentences why the Arnoldi process reduces to a three-term recurrence (Lanczos) whenever $A$ is symmetric, using $H_m = Q_m^T A Q_m$.
**Solution:**
If $A = A^T$, then $H_m = Q_m^T A Q_m$ is symmetric ($(Q_m^T A Q_m)^T = Q_m^T A^T Q_m = H_m$). By the Arnoldi construction, $H_m$ is also upper Hessenberg ($h_{ij} = 0$ for $i > j + 1$). A matrix that is simultaneously symmetric and upper Hessenberg must have zeros below the first subdiagonal and above the first superdiagonal, making it **tridiagonal**, which yields the three-term recurrence.

### Problem WA-3: Hand Step of Conjugate Gradient
**Question:** For $A = \begin{pmatrix} 3 & 1 \\ 1 & 2 \end{pmatrix}, b = (2, 1)^T, x_0 = (0, 0)^T$, carry out one full step of CG: compute $r_0, \alpha_0, x_1, r_1$. Verify $r_0^T r_1 = 0$.
**Solution:**
- $r_0 = b - A x_0 = (2, 1)^T$. $d_0 = r_0 = (2, 1)^T$.
- $A r_0 = \begin{pmatrix} 3(2) + 1(1) \\ 1(2) + 2(1) \end{pmatrix} = \begin{pmatrix} 7 \\ 4 \end{pmatrix}$.
- $r_0^T r_0 = 2^2 + 1^2 = 5$.
- $d_0^T A d_0 = 2(7) + 1(4) = 14 + 4 = 18$.
- $\alpha_0 = \frac{r_0^T r_0}{d_0^T A d_0} = \frac{5}{18} \approx 0.2778$.
- $x_1 = x_0 + \alpha_0 d_0 = \frac{5}{18} \begin{pmatrix} 2 \\ 1 \end{pmatrix} = \begin{pmatrix} 5/9 \\ 5/18 \end{pmatrix} \approx \begin{pmatrix} 0.5556 \\ 0.2778 \end{pmatrix}$.
- $r_1 = r_0 - \alpha_0 A d_0 = \begin{pmatrix} 2 \\ 1 \end{pmatrix} - \frac{5}{18} \begin{pmatrix} 7 \\ 4 \end{pmatrix} = \begin{pmatrix} 2 - 35/18 \\ 1 - 20/18 \end{pmatrix} = \begin{pmatrix} 1/18 \\ -2/18 \end{pmatrix} = \begin{pmatrix} 1/18 \\ -1/9 \end{pmatrix}$.
- Verification: $r_0^T r_1 = 2(1/18) + 1(-1/9) = \frac{1}{9} - \frac{1}{9} = 0 \quad \checkmark$.

### Problem WA-4: GMRES Memory Scaling
**Question:** True or False: "GMRES needs the same amount of memory per iteration regardless of how many iterations have been run."
**Solution:**
**False.** GMRES uses the full Arnoldi iteration, requiring every previous orthogonal basis vector $q_1, \dots, q_m$ to be stored in memory to orthogonalize new vectors. Memory grows linearly $O(m n)$ with iteration count $m$.

### Problem WA-5: Condition Number and Convergence Factor Comparison
**Question:** A symmetric positive definite system has condition number $\kappa = 100$. Compare CG's factor $\frac{\sqrt{\kappa}-1}{\sqrt{\kappa}+1}$ to steepest descent's factor $\frac{\kappa-1}{\kappa+1}$.
**Solution:**
- CG factor: $\frac{\sqrt{100}-1}{\sqrt{100}+1} = \frac{10-1}{10+1} = \frac{9}{11} \approx 0.8182$.
- Steepest descent factor: $\frac{100-1}{100+1} = \frac{99}{101} \approx 0.9802$.
CG contracts error much faster per step. Steepest descent needs roughly $\kappa$-scaled iterations, while CG needs only $\sqrt{\kappa}$-scaled iterations (a factor of 10 difference).

---

# LP, QP, Sparsity & Constrained Optimization Practice Problems

### Problem LP-1: Furniture Workshop LP Formulation
**Problem:** A workshop produces chairs ($x_1$) and tables ($x_2$). Each chair yields \$20 profit, needs 1 hr labor and 2 units wood. Each table yields \$30 profit, needs 2 hrs labor and 1 unit wood. Total labor available is 100 hrs, total wood is 80 units. Formulate and solve the LP.
**Formulation:**
$$\max_{x_1, x_2} 20x_1 + 30x_2 \iff \min_{x_1, x_2} -20x_1 - 30x_2$$
$$\text{s.t.} \quad x_1 + 2x_2 \le 100, \quad 2x_1 + x_2 \le 80, \quad x_1 \ge 0, \ x_2 \ge 0$$
**Solution:**
Corner points of feasible polytope:
1. $(0, 0) \implies \text{Profit} = \$0$
2. $(40, 0) \implies \text{Profit} = \$800$
3. $(0, 50) \implies \text{Profit} = \$1500$
4. Intersection: $x_1 + 2x_2 = 100$ and $2x_1 + x_2 = 80 \implies 3x_1 = 60 \implies x_1 = 20, x_2 = 40$.
   $\text{Profit} = 20(20) + 30(40) = 400 + 1200 = \$1600$.
Optimal production: **20 chairs and 40 tables with maximum profit \$1600**.

### Problem QP-1: Minimum Distance Projection onto Polyhedron
**Problem:** Minimize the squared distance from $(5, 5)$ to the feasible set $x_1 + x_2 \le 4, x_1 \ge 0, x_2 \ge 0$.
**Formulation:**
$$\min_{x_1, x_2} \frac{1}{2} [(x_1 - 5)^2 + (x_2 - 5)^2] \quad \text{s.t.} \quad x_1 + x_2 \le 4, \ x_1 \ge 0, \ x_2 \ge 0$$
**Solution via KKT:**
At the optimum, the constraint $x_1 + x_2 = 4$ is active, while non-negativities are strictly inactive.
Lagrangian: $L = \frac{1}{2}(x_1 - 5)^2 + \frac{1}{2}(x_2 - 5)^2 + \lambda(x_1 + x_2 - 4)$.
- $\frac{\partial L}{\partial x_1} = x_1 - 5 + \lambda = 0 \implies x_1 = 5 - \lambda$
- $\frac{\partial L}{\partial x_2} = x_2 - 5 + \lambda = 0 \implies x_2 = 5 - \lambda$
Substitute into $x_1 + x_2 = 4$:
$$(5 - \lambda) + (5 - \lambda) = 4 \implies 10 - 2\lambda = 4 \implies \lambda = 3 \ge 0$$
Thus $x_1^* = 2, x_2^* = 2$.
Optimal point: **$(2, 2)$**, with minimum squared distance $(2-5)^2 + (2-5)^2 = 9 + 9 = 18$.

---

---

# Advanced Practice Problems from Course Materials

## 1. Advanced Constrained Optimization & KKT Problems

### Problem KKT-1: Equality-Constrained Least Squares
**Problem:** Minimize $\|A x - b\|_2^2$ subject to linear equality constraint $C x = d$, where $A \in \mathbb{R}^{m \times n}$ has full column rank and $C \in \mathbb{R}^{p \times n}$ has full row rank ($p < n$).
**Solution:**
1. Objective: $f(x) = \frac{1}{2} x^T (2 A^T A) x - (2 A^T b)^T x + b^T b$.
2. Lagrangian:
   $$L(x, \nu) = \frac{1}{2} \|A x - b\|_2^2 + \nu^T (C x - d)$$
3. KKT Stationarity:
   $$\nabla_x L = A^T (A x - b) + C^T \nu = 0 \implies (A^T A) x + C^T \nu = A^T b$$
4. Primal Feasibility:
   $$C x = d$$
5. Combined KKT (Saddle-Point) Linear System:
   $$\begin{pmatrix} A^T A & C^T \\ C & 0 \end{pmatrix} \begin{pmatrix} x^* \\ \nu^* \end{pmatrix} = \begin{pmatrix} A^T b \\ d \end{pmatrix}$$
   Because $A^T A \succ 0$ and $C$ has full row rank, this KKT block matrix is invertible.
   Solving for $x^*$ from the first block: $x = (A^T A)^{-1}(A^T b - C^T \nu)$.
   Substituting into $C x = d$:
   $$C (A^T A)^{-1} A^T b - C (A^T A)^{-1} C^T \nu = d$$
   $$\nu^* = \left( C (A^T A)^{-1} C^T \right)^{-1} \left( C (A^T A)^{-1} A^T b - d \right)$$
   $$x^* = (A^T A)^{-1} A^T b - (A^T A)^{-1} C^T \nu^*$$
   Notice: $(A^T A)^{-1} A^T b$ is the unconstrained least-squares solution, and the second term is the orthogonal correction projecting onto the affine subspace $C x = d$.

---

### Problem KKT-2: The Water-Filling Algorithm (Information Theory)
**Problem:** Maximize total communication channel capacity:
$$\max_{x} \sum_{i=1}^n \log(\alpha_i + x_i) \quad \text{subject to } \sum_{i=1}^n x_i = P, \quad x_i \ge 0 \ \forall i$$
where $\alpha_i = \sigma_i^2 / |h_i|^2$ is the noise-to-gain ratio of channel $i$, and $P$ is total transmit power.
**Solution:**
1. Reformulate as convex minimization:
   $$\min_x -\sum_{i=1}^n \log(\alpha_i + x_i) \quad \text{s.t.} \quad \sum_{i=1}^n x_i - P = 0, \quad -x_i \le 0 \ (i = 1, \dots, n)$$
2. Lagrangian:
   $$L(x, \nu, \lambda) = -\sum_{i=1}^n \log(\alpha_i + x_i) + \nu \left( \sum_{i=1}^n x_i - P \right) - \sum_{i=1}^n \lambda_i x_i$$
3. KKT Stationarity:
   $$\frac{\partial L}{\partial x_i} = -\frac{1}{\alpha_i + x_i} + \nu - \lambda_i = 0 \implies \frac{1}{\alpha_i + x_i} = \nu - \lambda_i$$
4. Complementary Slackness: $\lambda_i x_i = 0$ with $\lambda_i \ge 0, x_i \ge 0$.
   - If $x_i > 0 \implies \lambda_i = 0 \implies \frac{1}{\alpha_i + x_i} = \nu \implies x_i = \frac{1}{\nu} - \alpha_i$.
   - If $x_i = 0 \implies \lambda_i \ge 0 \implies \frac{1}{\alpha_i} \le \nu \implies \frac{1}{\nu} \le \alpha_i$.
5. Closed-Form Water-Filling Solution:
   $$x_i^* = \max\left( \frac{1}{\nu} - \alpha_i, 0 \right) = \left( \frac{1}{\nu} - \alpha_i \right)^+$$
   where water level $1/\nu$ is the unique scalar determined by the power constraint:
   $$\sum_{i=1}^n \max\left( \frac{1}{\nu} - \alpha_i, 0 \right) = P$$
   *Physical Meaning:* Power is poured like water into channels with the lowest noise levels $\alpha_i$. Noisy channels with $\alpha_i \ge 1/\nu$ receive zero power.

---

### Problem KKT-3: Optimization on the Unit Circle (Non-convex constraint)
**Problem:** Minimize $f(x, y) = x + 2y$ subject to $x^2 + y^2 = 1$.
**Solution:**
1. Lagrangian: $L(x, y, \nu) = x + 2y + \nu (x^2 + y^2 - 1)$.
2. Stationarity:
   - $\frac{\partial L}{\partial x} = 1 + 2\nu x = 0 \implies x = -\frac{1}{2\nu}$
   - $\frac{\partial L}{\partial y} = 2 + 2\nu y = 0 \implies y = -\frac{1}{\nu}$
3. Substitute into $x^2 + y^2 = 1$:
   $$\left(-\frac{1}{2\nu}\right)^2 + \left(-\frac{1}{\nu}\right)^2 = \frac{1}{4\nu^2} + \frac{1}{\nu^2} = \frac{5}{4\nu^2} = 1 \implies \nu^2 = \frac{5}{4} \implies \nu = \pm \frac{\sqrt{5}}{2}$$
4. Evaluating Critical Points:
   - For $\nu = +\frac{\sqrt{5}}{2}$:
     $x = -\frac{1}{\sqrt{5}}, \quad y = -\frac{2}{\sqrt{5}} \implies f = -\frac{1}{\sqrt{5}} - \frac{4}{\sqrt{5}} = -\sqrt{5} \approx -2.236$
   - For $\nu = -\frac{\sqrt{5}}{2}$:
     $x = +\frac{1}{\sqrt{5}}, \quad y = +\frac{2}{\sqrt{5}} \implies f = +\sqrt{5} \approx +2.236$
5. Conclusion:
   - Global minimum is at $(x^*, y^*) = \left(-\frac{1}{\sqrt{5}}, -\frac{2}{\sqrt{5}}\right)$ with minimum value $-\sqrt{5}$.
   - *Note on Convexity:* Because the equality constraint $x^2 + y^2 = 1$ is non-linear (the circle boundary is non-convex), KKT conditions produce multiple stationary points (both minimum and maximum). One must evaluate the objective to classify them.

---

## 2. Projected Gradient Descent (PGD) Solved Problems

### Problem PGD-1: PGD onto the Non-Negative Orthant
**Problem:** Minimize $f(x_1, x_2) = (x_1 - 3)^2 + (x_2 + 2)^2$ subject to $x \ge 0$, starting from $x^{(0)} = (0, 0)$ with step size $\alpha = 0.5$.
**Solution:**
- $\nabla f(x) = \begin{pmatrix} 2(x_1 - 3) \\ 2(x_2 + 2) \end{pmatrix}$.
- Unconstrained gradient descent step: $v^{(k+1)} = x^{(k)} - \alpha \nabla f(x^{(k)})$.
- Projection onto non-negative orthant: $[\Pi(v)]_i = \max(v_i, 0)$.
- **Iteration 1:**
  $x^{(0)} = (0, 0)^T$.
  $\nabla f(0, 0) = \begin{pmatrix} -6 \\ 4 \end{pmatrix}$.
  $v^{(1)} = \begin{pmatrix} 0 \\ 0 \end{pmatrix} - 0.5 \begin{pmatrix} -6 \\ 4 \end{pmatrix} = \begin{pmatrix} 3 \\ -2 \end{pmatrix}$.
  $x^{(1)} = \Pi(v^{(1)}) = \begin{pmatrix} \max(3, 0) \\ \max(-2, 0) \end{pmatrix} = \begin{pmatrix} 3 \\ 0 \end{pmatrix}$.
- **Iteration 2:**
  $\nabla f(3, 0) = \begin{pmatrix} 2(3 - 3) \\ 2(0 + 2) \end{pmatrix} = \begin{pmatrix} 0 \\ 4 \end{pmatrix}$.
  $v^{(2)} = \begin{pmatrix} 3 \\ 0 \end{pmatrix} - 0.5 \begin{pmatrix} 0 \\ 4 \end{pmatrix} = \begin{pmatrix} 3 \\ -2 \end{pmatrix}$.
  $x^{(2)} = \Pi(v^{(2)}) = \begin{pmatrix} 3 \\ 0 \end{pmatrix} = x^{(1)}$.
  The iterate has converged to the exact constrained minimizer $x^* = (3, 0)^T$.

---

### Problem PGD-2: PGD onto the Euclidean Ball
**Problem:** Minimize $f(x, y) = (x - 3)^2 + (y - 4)^2$ subject to $x^2 + y^2 \le 4$ (ball of radius $R = 2$). Perform one PGD step from $(0, 0)$ with $\alpha = 0.5$.
**Solution:**
- $\nabla f(0, 0) = \begin{pmatrix} -6 \\ -8 \end{pmatrix}$.
- Gradient step:
  $$v^{(1)} = \begin{pmatrix} 0 \\ 0 \end{pmatrix} - 0.5 \begin{pmatrix} -6 \\ -8 \end{pmatrix} = \begin{pmatrix} 3 \\ 4 \end{pmatrix}$$
- Norm of $v^{(1)}$: $\|v^{(1)}\|_2 = \sqrt{3^2 + 4^2} = 5 > R = 2$.
- Projection onto ball of radius 2:
  $$\Pi_{B(2)}(v^{(1)}) = R \frac{v^{(1)}}{\|v^{(1)}\|_2} = 2 \frac{\begin{pmatrix} 3 \\ 4 \end{pmatrix}}{5} = \begin{pmatrix} 6/5 \\ 8/5 \end{pmatrix} = \begin{pmatrix} 1.2 \\ 1.6 \end{pmatrix}$$
  The iterate lies on the boundary of the ball pointing toward the unconstrained minimum $(3, 4)$.

---

## 3. Support Vector Machines: Worked Hand Computations & CVXOPT

### Problem SVM-1: 3-Point SVM Solved by Hand
**Problem:** Given training points in $\mathbb{R}^2$:
- $x_1 = (1, 1), \ y_1 = +1$
- $x_2 = (2, 2), \ y_2 = +1$
- $x_3 = (2, 0), \ y_3 = -1$
Find the optimal separating hyperplane $w^T x + b = 0$ by solving the dual problem by hand.
**Solution:**
1. Dual formulation:
   $$\max_\alpha \alpha_1 + \alpha_2 + \alpha_3 - \frac{1}{2} \sum_{i=1}^3 \sum_{j=1}^3 \alpha_i \alpha_j y_i y_j (x_i^T x_j) \quad \text{s.t.} \quad \alpha_i \ge 0, \quad \alpha_1 + \alpha_2 - \alpha_3 = 0$$
2. Inner products:
   $x_1^T x_1 = 2$, $x_1^T x_2 = 4$, $x_1^T x_3 = 2$, $x_2^T x_2 = 8$, $x_2^T x_3 = 4$, $x_3^T x_3 = 4$.
3. Inspection reveals $x_2 = (2, 2)$ is further from $x_3 = (2, 0)$ than $x_1 = (1, 1)$ is.
   Guess support vectors are $x_1$ and $x_3$ with $\alpha_2 = 0$.
   From $\alpha_1 + \alpha_2 - \alpha_3 = 0 \implies \alpha_3 = \alpha_1$.
4. Dual objective with $\alpha_2 = 0, \alpha_3 = \alpha_1$:
   $$g(\alpha_1) = 2\alpha_1 - \frac{1}{2} [\alpha_1^2(2) + \alpha_1^2(4) - 2\alpha_1^2(2)] = 2\alpha_1 - \frac{1}{2}(2\alpha_1^2) = 2\alpha_1 - \alpha_1^2$$
   Setting $g'(\alpha_1) = 2 - 2\alpha_1 = 0 \implies \alpha_1 = 1$.
   Thus $\alpha_1^* = 1, \alpha_2^* = 0, \alpha_3^* = 1$.
5. Reconstructing $w^*$ and $b^*$:
   $$w^* = \alpha_1 y_1 x_1 + \alpha_3 y_3 x_3 = 1(+1)\begin{pmatrix} 1 \\ 1 \end{pmatrix} + 1(-1)\begin{pmatrix} 2 \\ 0 \end{pmatrix} = \begin{pmatrix} 1 - 2 \\ 1 - 0 \end{pmatrix} = \begin{pmatrix} -1 \\ 1 \end{pmatrix}$$
6. Computing intercept $b^*$:
   From support vector $x_1 = (1, 1)$ ($y_1 = +1$):
   $$y_1(w^T x_1 + b) = 1 \implies 1((-1)(1) + 1(1) + b) = 1 \implies b = 1$$
   Check with $x_3 = (2, 0)$ ($y_3 = -1$):
   $y_3(w^T x_3 + b) = -1((-1)(2) + 1(0) + 1) = -1(-1) = 1 \quad \checkmark$.
7. Optimal Hyperplane:
   $$-x_1 + x_2 + 1 = 0 \iff x_2 - x_1 + 1 = 0$$
   Margin: $\gamma = \frac{2}{\|w\|} = \frac{2}{\sqrt{(-1)^2 + 1^2}} = \frac{2}{\sqrt{2}} = \sqrt{2}$.

---

### Problem SVM-2: Python CVXOPT Quadratic Programming Solver for SVM
**Implementation:**
```python
import numpy as np
from cvxopt import matrix, solvers

# Data points
X = np.array([[1.0, 1.0], [2.0, 2.0], [2.0, 0.0]])
y = np.array([1.0, 1.0, -1.0])
N = len(y)

# Formulate Gram matrix P where P_ij = y_i y_j (x_i^T x_j)
K = X @ X.T
P = matrix(np.outer(y, y) * K)
q = matrix(-np.ones(N))

# G x <= h: -alpha_i <= 0
G = matrix(-np.eye(N))
h = matrix(np.zeros(N))

# A x = b: sum(y_i alpha_i) = 0
A = matrix(y.reshape(1, -1))
b = matrix(np.zeros(1))

# Solve QP
solvers.options['show_progress'] = False
sol = solvers.qp(P, q, G, h, A, b)
alphas = np.ravel(sol['x'])

# Support vectors
sv_idx = np.where(alphas > 1e-5)[0]
w = np.sum((alphas * y)[:, None] * X, axis=0)
b_val = y[sv_idx[0]] - np.dot(X[sv_idx[0]], w)

print(f"Dual alphas: {alphas.round(4)}")
print(f"Optimal w: {w.round(4)}, b: {b_val.round(4)}")
print(f"Support vector indices: {sv_idx}")
```

---

## 4. Higher-Order SVD (HOSVD) Worked Example

### Problem HOSVD-1: 3-Way Tensor Decomposition
**Problem:** Consider a $2 \times 2 \times 2$ tensor $\mathcal{X}$ with frontal slices:
$$X_1 = \begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix}, \qquad X_2 = \begin{pmatrix} 5 & 6 \\ 7 & 8 \end{pmatrix}$$
Compute its mode-1, mode-2, and mode-3 unfolding matrices, and outline the HOSVD factor matrices.
**Solution:**
1. **Mode-1 Unfolding $X_{(1)}$ ($2 \times 4$):**
   Arranges mode-1 fibers (columns of slices) side by side:
   $$X_{(1)} = [X_1 \mid X_2] = \begin{pmatrix} 1 & 2 & 5 & 6 \\ 3 & 4 & 7 & 8 \end{pmatrix}$$
2. **Mode-2 Unfolding $X_{(2)}$ ($2 \times 4$):**
   Arranges mode-2 fibers (rows of slices) side by side:
   $$X_{(2)} = [X_1^T \mid X_2^T] = \begin{pmatrix} 1 & 3 & 5 & 7 \\ 2 & 4 & 6 & 8 \end{pmatrix}$$
3. **Mode-3 Unfolding $X_{(3)}$ ($2 \times 4$):**
   Arranges mode-3 fibers (tubes across slices) side by side:
   $$X_{(3)} = \begin{pmatrix} 1 & 3 & 2 & 4 \\ 5 & 7 & 6 & 8 \end{pmatrix}$$
4. **Factor Matrices:**
   - Factor matrix $U^{(1)}$: Left singular vectors of $X_{(1)}$.
   - Factor matrix $U^{(2)}$: Left singular vectors of $X_{(2)}$.
   - Factor matrix $U^{(3)}$: Left singular vectors of $X_{(3)}$.
5. **Core Tensor $\mathcal{S}$:**
   Project $\mathcal{X}$ onto the three factor matrices:
   $$\mathcal{S} = \mathcal{X} \times_1 (U^{(1)})^T \times_2 (U^{(2)})^T \times_3 (U^{(3)})^T$$
   The resulting core tensor $\mathcal{S}$ satisfies the all-orthogonality property.

---
