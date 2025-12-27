
# Asymptotic Analysis of the Zeta-Zero “π from Hitting Times” Construction  

## 0. Scope and status

This note separates four layers:

1. **Definition layer (exact):** \(S_\gamma(t)\), \(D_\gamma(t,p)\), \(\tau_p(\gamma)\).
2. **Continuum layer:** a deterministic boundary equation predicting the large-\(p\) scaling of \(\tau_p(\gamma)\) in the first block \(t\in[p,2p)\).
3. **Empirical layer:** sharp separation between **zeros** and nearby **non-zeros** (e.g. midpoints) in the behavior of \(\tau_p(\gamma)\), including an off-zero “toggle”.
4. **Rigorous layer (proved, conditional):** in the **first-block regime** \(u_*(\gamma)<2\) and under a mild **no pre-hit** condition (automatic for zeta zeros),
   - (**Zero ⇒ convergence**) if \(\zeta(\tfrac12+i\gamma)=0\), then \(\tau_p(\gamma)/p\to u_*(\gamma)\).
   - (**Nonzero ⇒ non-convergence**) if \(\zeta(\tfrac12+i\gamma)\neq0\), then \(\tau_p(\gamma)/p\) does **not** converge; it has accumulation points \(1\) and \(u_*(\gamma)\).

**Remarks  .**
- For the actual zeta-zero application, \(\gamma=\gamma_n\ge 14.1347\), hence \(|q|=\sqrt{\gamma^2+\tfrac14}>1\), so the “no pre-hit” lemma below applies.
- The first-block condition is automatic for all sufficiently large \(\gamma\): since \(\theta_*(\gamma)<\pi\), \(\log u_*(\gamma)=\theta_*(\gamma)/\gamma<\pi/\gamma\), hence \(u_*(\gamma)<e^{\pi/\gamma}\). In particular, if \(\gamma>\pi/\log 2\approx 4.532\), then \(u_*(\gamma)<2\).

The constant \(\pi\) and the coefficient series arise purely from the **continuum geometry** once the \(O(1)\) term \(\zeta(\tfrac12+i\gamma)\) vanishes (i.e. at a critical-line zero).

---

## 1. Definitions (exact)

Fix \(\gamma>0\) and set
\[
s:=\tfrac12+i\gamma,\qquad q:=1-s=\tfrac12-i\gamma.
\]
Define the partial Dirichlet sums (with \(S_\gamma(0):=0\))
\[
S_\gamma(t):=\sum_{k=1}^{t} k^{-s}=\sum_{k=1}^{t} k^{-1/2-i\gamma}\qquad (t\in\mathbb Z_{\ge0}).
\]
For integers \(p\ge2\), define
\[
p^q:=\exp(q\log p)\quad(\log p\in\mathbb R),
\]
and the renormalized defect
\[
D_\gamma(t,p):=S_\gamma(t)-p^{q}\,S_\gamma(\lfloor t/p\rfloor).
\]
Define the hitting time
\[
\tau_p(\gamma):=\inf\Big\{t\in\mathbb N:\ |D_\gamma(t,p)|\ge \sqrt p\Big\}.
\]
Let \(\{\gamma_n\}_{n\ge1}\) be the increasing ordinates of critical-line zeros:
\[
\zeta\!\left(\tfrac12+i\gamma_n\right)=0.
\]
The nested limit under discussion is
\[
\boxed{\quad \pi \stackrel{?}{=} \lim_{n\to\infty}\ \gamma_n\,\log\!\left(\lim_{p\to\infty}\frac{\tau_p(\gamma_n)}{p}\right)\quad}.
\]

---

## 2. First-block reduction and continuum boundary

Write \(t=pu\) with \(u\in[1,2)\). Then \(\lfloor t/p\rfloor=1\), hence
\[
D_\gamma(pu,p)=S_\gamma(pu)-p^q.
\]
Using Abel/Euler–Maclaurin heuristics suggests
\[
S_\gamma(pu)=\frac{(pu)^q}{q}+\zeta(s)+O(p^{-1/2}),
\]
so
\[
D_\gamma(pu,p)=p^q\Big(\frac{u^q}{q}-1\Big)+\zeta(s)+O(p^{-1/2}).
\]
Since \(|p^q|=p^{\Re(q)}=\sqrt p\),
\[
\frac{|D_\gamma(pu,p)|}{\sqrt p}\approx \left|\frac{u^q}{q}-1+\frac{\zeta(s)}{p^q}\right|.
\]

- **At a critical-line zero** (\(\zeta(s)=0\)), the first nondegenerate hit is governed by
  \[
  \boxed{\quad \left|\frac{u^q}{q}-1\right|=1\quad (u>1). \quad}
  \]
- **Off a zero**, \(\zeta(s)\neq0\) gives an \(O(1)\) perturbation that competes with the degeneracy at \(u=1\).

---

## 3. Degeneracy at \(u=1\) on the critical line (exact)

### Proposition 3.1 (boundary degeneracy)
For \(s=\tfrac12+i\gamma\),
\[
\left|\frac{1^q}{q}-1\right|=1.
\]

**Proof.**
\[
\left|\frac{1^q}{q}-1\right|=\left|\frac{1-q}{q}\right|=\left|\frac{s}{q}\right|.
\]
But \(|s|=|q|=\sqrt{\gamma^2+\tfrac14}\), hence \(|s/q|=1\). ∎

Thus, in \(u\in[1,2)\) there are (at least) two boundary crossings:
1. **Degenerate crossing:** \(u=1\) (\(t=p\)).
2. **Principal crossing:** \(u=u_*(\gamma)>1\).

Define the principal branch:
\[
\boxed{\quad u_*(\gamma):=\min\Big\{u>1:\ \left|\frac{u^q}{q}-1\right|=1\Big\},\qquad \theta_*(\gamma):=\gamma\log u_*(\gamma). \quad}
\]

---

## 4. Exact continuum equation for \(\theta_*(\gamma)\)

Let \(u=\exp(\theta/\gamma)\) so \(\theta=\gamma\log u\). Then
\[
u^q=\exp\!\Big(q\frac{\theta}{\gamma}\Big)=\exp\!\Big(\frac{\theta}{2\gamma}\Big)e^{-i\theta}.
\]
The boundary condition \(\big|\frac{u^q}{q}-1\big|=1\) is equivalent to \(|z-1|=1\) with
\[
z=\frac{e^{\theta/(2\gamma)}e^{-i\theta}}{q}.
\]
Using \(|z-1|^2=1\iff |z|^2=2\Re z\), one obtains
\[
\boxed{\quad e^{\theta/(2\gamma)}=\cos\theta+2\gamma\sin\theta.\quad}
\]
Write \(\theta=\pi-\delta\) and \(\varepsilon:=1/\gamma\); equivalently
\[
\boxed{\quad 2\sin\delta-\varepsilon\cos\delta=\varepsilon\exp\!\Big(\frac{\pi-\delta}{2}\varepsilon\Big).\quad}
\]

---

## 5. Asymptotic expansion for the continuum root (universal)

Define \(\delta(\gamma):=\pi-\theta_*(\gamma)\). Then \(\delta(\gamma)\to0^+\) as \(\gamma\to\infty\) and admits a full expansion
\[
\boxed{\quad \delta(\gamma)=\sum_{k\ge1}\frac{a_k}{\gamma^k}. \quad}
\]

### Coefficients \(a_k\) (to order 12)
\[
\begin{aligned}
a_1&=1,\\
a_2&=\frac{\pi}{4},\\
a_3&=\frac{\pi^2}{16}-\frac13,\\
a_4&=\frac{\pi(\pi^2-18)}{96}=\frac{\pi^3}{96}-\frac{3\pi}{16},\\
a_5&=\frac{\pi^4}{768}-\frac{\pi^2}{16}+\frac{19}{120},\\
a_6&=\frac{\pi(\pi^4-100\pi^2+920)}{7680}=\frac{\pi^5}{7680}-\frac{5\pi^3}{384}+\frac{23\pi}{192},\\
a_7&=\frac{\pi^6}{92160}-\frac{\pi^4}{768}+\frac{35\pi^2}{768}-\frac{263}{3360},\\
a_8&=\frac{\pi^7}{1290240}+\frac{7\pi^5}{30720}+\frac{19\pi^3}{2304}-\frac{87\pi}{1280},\\
a_9&=\frac{\pi^8}{20643840}+\frac{7\pi^6}{46080}-\frac{5\pi^4}{4608}-\frac{47\pi^2}{1920}+\frac{1517}{40320},\\
a_{10}&=\frac{\pi^9}{371589120}+\frac{16920\pi^7}{371589120}-\frac{509040\pi^5}{371589120}-\frac{24192\pi^3}{371589120}+\frac{12256128\pi}{371589120},\\
a_{11}&=\frac{\pi^{10}}{7431782400}+\frac{209\pi^8}{20643840}-\frac{491\pi^6}{884736}+\frac{1717\pi^4}{368640}+\frac{1775\pi^2}{258048}-\frac{1985}{118272},\\
a_{12}&=\frac{\pi^{11}}{163499212800}+\frac{304370\pi^9}{163499212800}-\frac{24055680\pi^7}{163499212800}
+\frac{458577504\pi^5}{163499212800}-\frac{1190133120\pi^3}{163499212800}-\frac{1967834880\pi}{163499212800}.
\end{aligned}
\]

### Parity structure
- \(k\) odd \(\Rightarrow a_k\) involves only even powers of \(\pi\).
- \(k\) even \(\Rightarrow a_k\) involves only odd powers of \(\pi\).

### Leading coefficient and denominators
For \(k\ge2\),
\[
[\pi^{k-1}]\,a_k=\frac{1}{2^k\,(k-1)!},\qquad a_1=1.
\]
Hence the leading denominator is \(D_k=2^k(k-1)!\) (OEIS A066318).

### Reformulation
Since \(\theta_*(\gamma)=\pi-\delta(\gamma)\),
\[
\boxed{\quad \theta_*(\gamma)=\gamma\log u_*(\gamma)=
\pi-\frac{1}{\gamma}-\frac{\pi}{4\gamma^2}-\frac{\pi^2/16-1/3}{\gamma^3}-\frac{\pi(\pi^2-18)}{96\gamma^4}-\cdots\quad}
\]
and
\[
\boxed{\quad \log u_*(\gamma)=\frac{\pi}{\gamma}-\frac{1}{\gamma^2}-\frac{\pi}{4\gamma^3}-\frac{\pi^2/16-1/3}{\gamma^4}-\cdots\quad}.
\]

---

## 6. Why the nested limit returns \(\pi\) (continuum)

For any \(\gamma\to\infty\),
\[
\gamma\log u_*(\gamma)=\theta_*(\gamma)=\pi-\delta(\gamma)\to\pi.
\]
Thus, if for zeros \(\gamma=\gamma_n\) the inner limit \(\lim_{p\to\infty}\tau_p(\gamma_n)/p=u_*(\gamma_n)\) holds, then
\[
\lim_{n\to\infty}\gamma_n\log\!\left(\lim_{p\to\infty}\frac{\tau_p(\gamma_n)}{p}\right)
=\lim_{n\to\infty}\gamma_n\log u_*(\gamma_n)=\lim_{n\to\infty}\theta_*(\gamma_n)=\pi.
\]

---

## 7. Rigorous asymptotics for \(S_\gamma(N)\) (uniform, explicit)

We use the periodic Bernoulli function
\[
B_1(\{x\})=\{x\}-\tfrac12,\qquad \{x\}=x-\lfloor x\rfloor,\qquad |B_1|\le\tfrac12.
\]

### Lemma 7.1 (Euler–Maclaurin with periodic remainder, first order)
If \(f\in C^1([1,N])\), then
\[
\sum_{n=1}^N f(n)=\int_1^N f(x)\,dx+\frac{f(1)+f(N)}2+\int_1^N B_1(\{x\})\,f'(x)\,dx.
\]

### Theorem 7.2 (uniform \(O(N^{-1/2})\) remainder with explicit constant)
For \(s=\tfrac12+i\gamma\) and \(N\ge1\),
\[
S_\gamma(N)=\frac{N^q}{q}+\zeta(s)+R(N),
\]
with
\[
|R(N)|\le\Big(\tfrac12+|s|\Big)\,N^{-1/2},\qquad |s|=\sqrt{\gamma^2+\tfrac14}.
\]
Consequently, for integers \(p\ge1\), \(u\in[1,2]\), \(N=\lfloor pu\rfloor\),
\[
S_\gamma(\lfloor pu\rfloor)=\frac{(pu)^q}{q}+\zeta(s)+R(p,u,\gamma),
\qquad |R(p,u,\gamma)|\le C(\gamma)\,p^{-1/2},
\]
with \(C(\gamma)=\tfrac12+|s|\), uniform in \(u\in[1,2]\).

*Proof (compressed).* Apply Lemma 7.1 to \(f(x)=x^{-s}\). Rearranging and subtracting the \(N\to\infty\) limit gives
\[
R(N)=\frac12 N^{-s}+s\int_N^\infty B_1(\{x\})x^{-s-1}\,dx.
\]
Bound \(|B_1|\le\frac12\) and integrate \(x^{-3/2}\) to obtain the stated inequality. ∎

### Theorem 7.3 (one-term refinement; boundary-layer control)
For \(s=\tfrac12+i\gamma\) and \(N\ge1\),
\[
S_\gamma(N)=\frac{N^q}{q}+\zeta(s)+\frac12N^{-s}+O_\gamma(N^{-3/2}).
\]
(An explicit \(O_\gamma(N^{-5/2})\) is available by extracting the next Euler–Maclaurin term; the weaker \(O_\gamma(N^{-3/2})\) suffices below.)

---

## 8. Rigorous first-block theorems for \(\tau_p(\gamma)\)

Assume the **first-block regime** \(u_*(\gamma)<2\), so the principal continuum crossing lies in \(t\in(p,2p)\) where \(\lfloor t/p\rfloor=1\) and
\[
D_\gamma(pu,p)=S_\gamma(pu)-p^q.
\]

### Lemma 8.0 (no pre-hit for large \(p\))
Fix \(\gamma>0\) and \(s=\tfrac12+i\gamma\), \(q=\tfrac12-i\gamma\). Assume \(|q|>1\) (equivalently \(\gamma>\sqrt3/2\)).
Then there exists \(p_0=p_0(\gamma)\) such that for all integers \(p\ge p_0\),
\[
\max_{1\le t < p} |D_\gamma(t,p)|
=\max_{1\le t < p}|S_\gamma(t)|<\sqrt p,
\]
hence \(\tau_p(\gamma)\ge p\).

*Proof.* For \(t<p\), \(\lfloor t/p\rfloor=0\) and \(D_\gamma(t,p)=S_\gamma(t)\).
By Theorem 7.2,
\[
|S_\gamma(t)|
\le \frac{|t^q|}{|q|}+|\zeta(s)|+|R(t)|
\le \frac{\sqrt t}{|q|}+|\zeta(s)|+\Big(\tfrac12+|s|\Big)t^{-1/2}.
\]
Thus for \(t\in[1,p]\),
\[
\max_{1\le t\le p}|S_\gamma(t)|
\le \frac{\sqrt p}{|q|}+|\zeta(s)|+\Big(\tfrac12+|s|\Big).
\]
Since \(|q|>1\), \(\sqrt p(1-1/|q|)\to\infty\), so for all sufficiently large \(p\) the RHS is \(<\sqrt p\). ∎

### Lemma 8.1 (normalized defect in the first block)
For \(u\in[1,2]\),
\[
\frac{D_\gamma(pu,p)}{\sqrt p}
=e^{-i\gamma\log p}\Big(\frac{u^q}{q}-1\Big)+\frac{\zeta(s)}{\sqrt p}\,e^{i\gamma\log p}+O_\gamma(p^{-1}),
\]
uniformly in \(u\in[1,2]\). In particular, if \(\zeta(s)=0\),
\[
\frac{|D_\gamma(pu,p)|}{\sqrt p}=\left|\frac{u^q}{q}-1\right|+O_\gamma(p^{-1})
\qquad\text{uniformly in }u\in[1,2].
\]

*Proof.* Combine Theorem 7.2 with \(|p^q|=\sqrt p\). ∎

### Lemma 8.2 (degenerate point is subcritical at a zero)
Assume \(\zeta(s)=0\). Then for all sufficiently large integers \(p\),
\[
|D_\gamma(p,p)|<\sqrt p.
\]
Moreover, if \(|q|>1\), then by Lemma 8.0 also \(\tau_p(\gamma)\ge p\), hence \(\tau_p(\gamma)>p\) for all sufficiently large \(p\).

*Proof.* By Theorem 7.3 at \(N=p\),
\[
S_\gamma(p)=\frac{p^q}{q}+\frac12p^{-s}+O_\gamma(p^{-3/2}),
\]
so
\[
D_\gamma(p,p)=S_\gamma(p)-p^q=p^q\Big(\frac1q-1\Big)+\frac12p^{-s}+O_\gamma(p^{-3/2}).
\]
Write \(B:=\frac1q-1=\frac{s}{q}\), so \(|B|=1\). Also \(p^q=\sqrt p\,e^{-i\gamma\log p}\) and \(p^{-s}=p^{-1/2}e^{-i\gamma\log p}\). Hence
\[
D_\gamma(p,p)=\sqrt p\,e^{-i\gamma\log p}\Big(B+\frac{1}{2p}+O_\gamma(p^{-2})\Big),
\]
so
\[
|D_\gamma(p,p)|^2=p\Big|B+\frac{1}{2p}+O_\gamma(p^{-2})\Big|^2
=p+\Re(B)+O_\gamma(p^{-1}).
\]
Finally,
\[
\Re(B)=\Re\!\Big(\frac{s}{q}\Big)=\frac{\tfrac14-\gamma^2}{\tfrac14+\gamma^2}<0,
\]
so for large \(p\), \(|D_\gamma(p,p)|^2<p\), i.e. \(|D_\gamma(p,p)|<\sqrt p\). The final sentence follows by Lemma 8.0. ∎

### Theorem 8.3 (zeros ⇒ convergence, first block)
Assume \(\zeta(\tfrac12+i\gamma)=0\), \(u_*(\gamma)<2\), and \(|q|>1\). Then
\[
\boxed{\quad \lim_{p\to\infty}\frac{\tau_p(\gamma)}{p}=u_*(\gamma).\quad}
\]

*Proof (compressed sandwich).* By Lemma 8.0, \(\tau_p(\gamma)\ge p\) for large \(p\); by Lemma 8.2, \(|D_\gamma(p,p)|<\sqrt p\) for large \(p\), hence \(\tau_p(\gamma)>p\).
On any compact \(K\subset(1,2)\) avoiding \(u=1\) and \(u=u_*\), the continuous function \(u\mapsto\big|\frac{u^q}{q}-1\big|\) is uniformly \(<1\) for \(u<u_*\) and uniformly \(>1\) for \(u>u_*\). Lemma 8.1 supplies a uniform \(O_\gamma(p^{-1})\) modulus perturbation, so the strict inequalities persist for large \(p\), giving
\[
u_*-\varepsilon\le \tau_p(\gamma)/p\le u_*+\varepsilon
\]
for all large \(p\). Let \(\varepsilon\downarrow0\). ∎

---

## 9. Off-zero toggle: rigorous non-convergence (first block)

Define \(A:=\frac{1}{q}-1=\frac{s}{q}\), so \(|A|=1\) on the critical line.

### Lemma 9.1 (phase targeting by rounding exponentials)
Fix \(\gamma>0\). For any \(\vartheta\in\mathbb R\), define
\[
p_k:=\left\lfloor \exp\!\Big(\frac{\vartheta+2\pi k}{\gamma}\Big)+\frac12\right\rfloor.
\]
Then \(p_k\to\infty\) and
\[
\gamma\log p_k=\vartheta+2\pi k+o(1)\qquad (k\to\infty).
\]

### Theorem 9.2 (nonzeros ⇒ non-convergence, first block)
Assume \(\zeta(\tfrac12+i\gamma)\neq0\), \(u_*(\gamma)<2\), and \(|q|>1\). Then \(\tau_p(\gamma)/p\) does **not** converge; it has accumulation points
\[
\boxed{\quad 1\quad\text{and}\quad u_*(\gamma).\quad}
\]

*Proof (compressed).* By Theorem 7.2 at \(N=p\),
\[
D_\gamma(p,p)=S_\gamma(p)-p^q
=\sqrt p\,e^{-i\gamma\log p}A+\zeta(s)+O_\gamma(p^{-1/2}).
\]
Hence
\[
|D_\gamma(p,p)|^2-p
=2\sqrt p\,\Re\!\big(e^{-i\gamma\log p}A\,\overline{\zeta(s)}\big)+|\zeta(s)|^2+O_\gamma(1).
\]
Let \(C:=A\,\overline{\zeta(s)}\neq0\). Choose \(\vartheta_+=\arg C\), \(\vartheta_-=\vartheta_++\pi\). By Lemma 9.1 there exist subsequences \(p_k^\pm\to\infty\) with
\(e^{-i\gamma\log p_k^\pm}\to e^{-i\vartheta_\pm}\), so \(\Re(e^{-i\gamma\log p_k^+}C)\to|C|>0\) and \(\Re(e^{-i\gamma\log p_k^-}C)\to-|C|<0\). Thus for large \(k\),
\[
|D_\gamma(p_k^+,p_k^+)|>\sqrt{p_k^+}.
\]
By Lemma 8.0 (no pre-hit), \(\tau_{p_k^+}(\gamma)=p_k^+\), hence \(\tau_{p_k^+}(\gamma)/p_k^+\to1\).

Along \(p_k^-\), for large \(k\), \(|D_\gamma(p_k^-,p_k^-)|<\sqrt{p_k^-}\), so \(\tau_{p_k^-}(\gamma)>p_k^-\). In the first block, Lemma 8.1 shows that the \(\zeta(s)\)-term contributes only \(O(p^{-1/2})\) to the normalized defect uniformly in \(u\in[1,2]\); the same sandwich argument as Theorem 8.3 forces \(\tau_{p_k^-}(\gamma)/p_k^-\to u_*(\gamma)\). Hence \(1\) and \(u_*(\gamma)\) are accumulation points. ∎

---

## 10. Why \(\pi\) appears (geometric core)

In the first block at a zero,
\[
\frac{D_\gamma(pu,p)}{p^q}\approx \frac{u^q}{q}-1.
\]
Let \(z(u):=\frac{u^q}{q}=\frac{u^{1/2}}{|q|}\exp\!\big(-i(\gamma\log u+\arg q)\big)\), a logarithmic spiral.
The boundary \(|D|\approx|p^q|\) becomes \(|z(u)-1|=1\), i.e. a circle of radius 1 centered at 1. For large \(\gamma\), \(|z(u)|\asymp 1/\gamma\) near the relevant crossing, and \(|1-z|=1\) linearizes to \(\Re z\approx0\). Since \(\arg z(u)\) advances by \(-\gamma\log u\), the first nondegenerate return to the local boundary direction occurs after a half-turn:
\[
\gamma\log u\approx\pi,
\]
i.e. \(\theta_*=\gamma\log u_*\to\pi\).

---

## 11. Open questions (frontier)

### Rigorous analysis
1. **Multi-block extension:** remove \(u_*(\gamma)<2\). For \(u\ge2\), \(\lfloor t/p\rfloor\) changes and
   \[
   D_\gamma(pu,p)=S_\gamma(pu)-p^q S_\gamma(\lfloor u\rfloor)
   \]
   becomes piecewise in \(u\). Prove analogues of Theorems 8.3 and 9.2 across blocks.

2. **Uniformity in \(\gamma\):** track constants in Theorems 7.2–7.3 as \(\gamma\to\infty\), sufficient for explicit rates in \(\tau_p/p\to u_*(\gamma)\) along zeros.

### Robustness / variants
3. **Threshold robustness:** replace \(\sqrt p\) by \(c\sqrt p\). Continuum predicts \(\left|\frac{u^q}{q}-1\right|=c\); prove the corresponding dichotomy.

4. **Defect modifications:** replace \(\lfloor t/p\rfloor\) by smoother downsampling; determine which features (\(\theta_*\to\pi\), toggle dichotomy) persist.

5. **Coupled limits:** find \(p=p(\gamma)\) scalings yielding a single-parameter limit, avoiding nesting.

### Zeta-specific signals
6. **Finite-\(p\) signatures:** does \(\Delta_p(\gamma_n):=\tau_p(\gamma_n)-p\,u_*(\gamma_n)\) encode \(\zeta'(\tfrac12+i\gamma_n)\) or local zero spacing?

7. **Tomography:** can the oscillation pattern \(I_p(\gamma)=\mathbf{1}\{\tau_p(\gamma)=p\}\) be inverted to estimate \(\zeta(\tfrac12+i\gamma)\) efficiently?

---

## Appendix A: minimal reproducibility code (Python)

```python
import numpy as np, math, mpmath as mp
mp.mp.dps = 60

def zeta_zero_gamma(n): return float(mp.im(mp.zetazero(n)))

def compute_S(gamma, N):
    k = np.arange(1, N+1, dtype=np.float64)
    terms = (k**-0.5) * np.exp(-1j*gamma*np.log(k))
    return np.cumsum(terms, dtype=np.complex128)

def tau_from_S(S, gamma, p, max_mult=6):
    thr = math.sqrt(p)
    # t < p: floor(t/p)=0 so D=S(t)
    if np.any(np.abs(S[:p-1]) >= thr):
        return int(np.argmax(np.abs(S[:p-1]) >= thr) + 1)
    pq = math.sqrt(p) * np.exp(-1j*gamma*math.log(p))
    for m in range(1, max_mult):
        start, end = m*p, min((m+1)*p, len(S)+1)
        seg = S[start-1:end-1] - pq*S[m-1]   # S[m-1]=S_gamma(m)
        hit = np.abs(seg) >= thr
        if np.any(hit): return int(start + np.argmax(hit))
    return None

def theta_continuum(gamma):
    g = mp.mpf(gamma)
    def H(th): return mp.cos(th) + 2*g*mp.sin(th) - mp.e**(th/(2*g))
    pi = mp.pi
    left = pi - mp.mpf('0.2')
    while H(left) < 0: left -= mp.mpf('0.2')
    right = pi
    for _ in range(200):
        mid = (left+right)/2
        if H(mid) > 0: left = mid
        else: right = mid
    return float((left+right)/2)

def u_star(gamma):
    th = theta_continuum(gamma)
    return math.exp(th/gamma)

# example: compare tau/p to u_star at a zero
n, p = 2, 100000
gamma = zeta_zero_gamma(n)
S = compute_S(gamma, 6*p)
tau = tau_from_S(S, gamma, p)
print("tau/p:", tau/p, "u*:", u_star(gamma))

Appendix B: coefficient generation (formal series)
The coefficients
a
k
a_k
ak can be generated by solving
2
sin
⁡
δ
−
ε
cos
⁡
δ
=
ε
e
(
π
−
δ
)
ε
/
2
2\sin\delta-\varepsilon\cos\delta=\varepsilon e^{(\pi-\delta)\varepsilon/2}
2sinδ−εcosδ=εe(π−δ)ε/2
as a formal series
δ
=
∑
k
≥
1
a
k
ε
k
\delta=\sum_{k\ge1}a_k\varepsilon^k
δ=∑k≥1 ak εk and matching coefficients of
ε
k
\varepsilon^k
εk recursively. (Any CAS that supports truncated power series arithmetic suffices.)


