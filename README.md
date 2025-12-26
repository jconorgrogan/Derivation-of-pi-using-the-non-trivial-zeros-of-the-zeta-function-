
# A Hitting-Time Identity at the Zeta Zeros and the Emergence of π

## 1. Setup and notation

Let  
\[
s=\tfrac12+i\gamma,\qquad q=1-s=\tfrac12-i\gamma,\qquad |q|=\sqrt{\gamma^2+\tfrac14}.
\]
Define
\[
S_\gamma(t):=\sum_{k=1}^{t} k^{-s},
\qquad
D_\gamma(t,p):=S_\gamma(t)-p^{\,q}S_\gamma(\lfloor t/p\rfloor),
\]
and the hitting time
\[
\tau_p(\gamma):=\inf\{t\in\mathbb Z_+:\ |D_\gamma(t,p)|\ge \sqrt p\}.
\]

Throughout we write
\[
A:=\frac1q-1=\frac{s}{q},
\]
so that \(|A|=1\) on the critical line and
\[
\Re(A)=\frac{\frac14-\gamma^2}{\frac14+\gamma^2}<0\quad\text{iff}\quad \gamma>\tfrac12.
\]

---

## 2. Euler–Maclaurin / Hurwitz–zeta asymptotics

### Lemma 1 (partial sums of \(k^{-s}\))

Fix \(s\neq1\) with \(\Re(s)=\tfrac12\). As \(t\to\infty\),
\[
S_\gamma(t)=\frac{t^{\,q}}{q}+\zeta(s)+\frac12\,t^{-s}+O_s(t^{-3/2}).
\tag{2.1}
\]
If \(\zeta(s)=0\), then
\[
S_\gamma(t)=\frac{t^{\,q}}{q}+\frac12\,t^{-s}+O_s(t^{-3/2}).
\tag{2.2}
\]
The error term is uniform for \(t\asymp p\) once \(s\) is fixed.

*Proof.* Use the identity \(S_\gamma(t)=\zeta(s)-\zeta(s,t+1)\) together with the Euler–Maclaurin expansion for the Hurwitz zeta \(\zeta(s,a)\). ∎

---

## 3. The boundary layer at \(t=p\)

### Proposition 2 (sub-threshold behavior at \(t=p\))

Assume \(\zeta(s)=0\) and \(\gamma>\tfrac12\). Then for all sufficiently large \(p\),
\[
|D_\gamma(p,p)|<\sqrt p.
\tag{3.1}
\]
In particular, if \(|q|>1\) (equivalently \(\gamma>\sqrt3/2\)), then \(\tau_p(\gamma)>p\) for all large \(p\).

*Proof.* For \(t=p\),
\[
D_\gamma(p,p)=S_\gamma(p)-p^q.
\]
Using (2.2),
\[
D_\gamma(p,p)=p^qA+\frac12 p^{-s}+O_s(p^{-3/2}).
\]
Write \(p^q=\sqrt p\,p^{-i\gamma}\) and \(p^{-s}=p^{-1/2}p^{-i\gamma}\). Factoring out the common phase \(p^{-i\gamma}\),
\[
D_\gamma(p,p)=p^{-i\gamma}\Bigl(\sqrt p\,A+\tfrac12 p^{-1/2}\Bigr)+O_s(p^{-3/2}).
\]
Squaring removes the phase:
\[
|D_\gamma(p,p)|^2
=\Bigl|\sqrt p\,A+\tfrac12 p^{-1/2}\Bigr|^2+O_s(p^{-1})
= p+\Re(A)+O_s(p^{-1}).
\]
Since \(\Re(A)<0\), we have \(|D_\gamma(p,p)|^2<p\) for all sufficiently large \(p\). ∎

---

## 4. First-block reduction and limiting profile

### Lemma 3 (first block)

If \(p\le t<2p\) (equivalently \(t=\lfloor pu\rfloor\) with \(u\in[1,2)\)), then
\[
D_\gamma(t,p)=S_\gamma(t)-p^q.
\tag{4.1}
\]

Assume \(\zeta(s)=0\). For \(u\in[1,2)\) and \(t=\lfloor pu\rfloor\),
\[
\frac{|D_\gamma(\lfloor pu\rfloor,p)|}{\sqrt p}
=
f_\gamma(u)+O_s\!\left(\frac1p\right),
\qquad
f_\gamma(u):=\left|\frac{u^q}{q}-1\right|,
\tag{4.2}
\]
uniformly on \(u\in[1,2)\).

*Proof.* Insert (2.2) into (4.1), note \(\lfloor pu\rfloor=pu+O(1)\), and divide by \(\sqrt p=|p^q|\). ∎

---

## 5. Geometry of the second crossing

### Lemma 4 (existence, uniqueness, and transversality of \(\kappa(\gamma)\))

Assume \(|q|>1\). Let
\[
r(u):=\frac{\sqrt u}{|q|},\qquad
\theta(u):=\arg(1/q)-\gamma\log u.
\]
Define \(g(u):=r(u)-2\cos\theta(u)\).

Then there exists a unique \(u=\kappa(\gamma)>1\) with
\[
g(\kappa(\gamma))=0
\quad\text{and}\quad
\theta(\kappa(\gamma))\in(-\pi/2,0).
\]
Moreover the crossing is simple:
\[
g'(\kappa(\gamma))\neq0.
\tag{5.1}
\]

Finally,
\[
\kappa(\gamma)<e^{\pi/\gamma}.
\tag{5.2}
\]

*Proof.* On \(\theta\in(-\pi/2,0)\),
\[
g'(u)=r'(u)-\frac{d}{du}(2\cos\theta(u))
=\frac{1}{2|q|\sqrt u}-\frac{2\gamma}{u}\sin\theta(u).
\]
Since \(\sin\theta(u)<0\) on this branch, both terms are positive, hence \(g'(u)>0\). Thus any root is unique and transversal.

Existence follows by noting that \(g(u)>0\) near \(u=1^+\) and \(g(u)<0\) once \(\theta\) approaches \(0\). The bound (5.2) follows from \(\theta(\kappa)>-\pi/2\). ∎

---

## 6. Existence of the scaling limit at a zero

### Theorem A (existence of \(\kappa(\gamma)\))

Assume:
- \(\zeta(\tfrac12+i\gamma)=0\),
- \(\gamma>\max\{\tfrac12,\pi/\log2\}\).

Then
\[
\lim_{p\to\infty}\frac{\tau_p(\gamma)}{p}=\kappa(\gamma),
\]
where \(\kappa(\gamma)\in(1,2)\) is the unique solution of
\[
\left|\frac{\kappa(\gamma)^q}{q}-1\right|=1
\quad\text{on the branch }\theta\in(-\pi/2,0).
\tag{6.1}
\]

*Proof.* By Proposition 2, \(|D_\gamma(p,p)|<\sqrt p\) for large \(p\), hence \(\tau_p>p\). By Lemma 3, on \(u\in[1,2)\) the normalized process converges uniformly to \(f_\gamma(u)\). Lemma 4 shows that \(f_\gamma(u)=1\) has a unique, simple root \(\kappa(\gamma)>1\) in \((1,2)\). Uniform convergence plus transversality implies stability of the first crossing, hence \(\tau_p(\gamma)/p\to\kappa(\gamma)\). ∎

---

## 7. The π-law and asymptotic expansion

### Theorem B (asymptotics of \(\kappa(\gamma)\))

Let \(x(\gamma):=\gamma\log\kappa(\gamma)\). Then, as \(\gamma\to\infty\),
\[
x(\gamma)
= \pi - \frac{1}{\gamma}
- \frac{\pi}{4\gamma^{2}}
+\frac{1}{\gamma^{3}}\!\left(\frac13-\frac{\pi^{2}}{16}\right)
+O(\gamma^{-4}).
\tag{7.1}
\]
In particular,
\[
\lim_{\gamma\to\infty}x(\gamma)=\pi.
\]

*Proof.* From (6.1), writing \(\kappa=e^{x/\gamma}\),
\[
\frac{\kappa^q}{q}=\frac{e^{x/(2\gamma)}}{|q|}e^{i(\alpha-x)},
\qquad \alpha:=\arg(1/q)=\arctan(2\gamma).
\]
The condition \(|z-1|=1\) gives the exact implicit equation
\[
2\cos(\alpha-x)=\frac{e^{x/(2\gamma)}}{|q|}.
\tag{7.2}
\]
Since the right-hand side is \(O(1/\gamma)\), we must have \(\alpha-x=-\pi/2+O(1/\gamma)\), hence \(x=\pi+O(1/\gamma)\).

Set \(\delta:=\alpha+\pi/2-x\). Then (7.2) becomes
\[
2\sin\delta=\frac{1}{|q|}\exp\!\left(\frac{\alpha+\pi/2-\delta}{2\gamma}\right).
\]
Expanding \(\alpha=\arctan(2\gamma)\), \(|q|^{-1}\), \(\sin\delta\), and the exponential in powers of \(1/\gamma\), and solving order by order yields (7.1). ∎

---

## 8. Off-zero failure of convergence

### Theorem C (nonconvergence off zeros)

Assume \(|q|>1\) and \(\zeta(\tfrac12+i\gamma)\neq0\). Then
\[
\liminf_{p\to\infty}\frac{\tau_p(\gamma)}{p}=1,
\qquad
\limsup_{p\to\infty}\frac{\tau_p(\gamma)}{p}>1,
\]
so \(\tau_p(\gamma)/p\) does not converge.

*Proof.* From (2.1) at \(t=p\),
\[
D_\gamma(p,p)=\sqrt p\,e^{-i\gamma\log p}A+\zeta(s)+O(p^{-1/2}),
\]
hence
\[
|D_\gamma(p,p)|^2
= p + 2\sqrt p\,\Re\!\big(e^{-i\gamma\log p}A\,\overline{\zeta(s)}\big)+O(1).
\tag{8.1}
\]
By choosing integers \(p\) so that the phase \(e^{-i\gamma\log p}\) aligns or anti-aligns with \(\overline{A}\,\zeta(s)\), the middle term in (8.1) is positive along one subsequence and negative along another. Since \(|q|>1\) implies \(|D_\gamma(t,p)|<\sqrt p\) for all \(t<p\) and large \(p\), these subsequences give \(\tau_p=p\) and \(\tau_p>p\) respectively, proving the stated liminf/limsup. ∎

---

## 9. Corollary (the π identity along zeta zeros)

Let \(\gamma_n\) be the ordinates of the nontrivial zeros of \(\zeta(s)\) on the critical line. Then
\[
\boxed{
\pi
=
\lim_{n\to\infty}
\gamma_n\cdot
\log\!\left(
\lim_{p\to\infty}\frac{\tau_p(\gamma_n)}{p}
\right).
}
\]

---

**Summary.**  
At a zeta zero, the boundary-layer correction forces the walk to remain sub-threshold at \(t=p\), leading to a deterministic second crossing with scaling factor \(\kappa(\gamma)\). The implicit equation for \(\kappa(\gamma)\) yields the universal \(\pi\)-law. Off zeros, the uncontrolled \(\zeta(s)\) term destroys convergence, explaining the observed zero-specific rigidity.
