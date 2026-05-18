# Proof

## Problem Statement

Prove or disprove the following statement:

Let \( X \to B \) be a one-parameter family of complex projective varieties over a holomorphic disk \( B \), and the fiber of 0 is a simple normal crossing divisor. Let \( t \in B \setminus \{0\} \), and denote the fiber over \( t \) by \( X_t \). Let \( T \) be the monodromy operator acting on \( H^1(X_t, \mathbb{Z}) \). Then the natural restriction map
\[
H^1(X, \mathbb{Z}) \to H^1(X_t, \mathbb{Z})^T
\]
to the \( T \)-invariant submodule is surjective.

## Proof

Write \(f:X\to B\), \(X_0=f^{-1}(0)\), \(B^*=B\setminus\{0\}\), \(X^*=f^{-1}(B^*)=X\setminus X_0\), \(j:X^*\hookrightarrow X\), and \(i_t:X_t\hookrightarrow X^*\). We use the standard semistable meaning of the hypothesis that \(X_0\) is a simple normal crossing divisor: \(X\) is smooth, \(X_0\) is reduced, and \(f\) is smooth over \(B^*\). This is the convention in the cited semistable local invariant-cycle literature. <cite>type=definition; label=semistable convention; title=Failure of the invariant cycle theorem over Z; authors=Donu Arapura, Francois Greer, and Yilong Zhang; source_url=https://arxiv.org/abs/2602.07302; verifier_locator=Introduction, p. 2; statement_match=exact; statement=the central fiber X0 is a reduced normal crossing divisor and the total space is smooth; usage=Fixes the standard semistable interpretation of the hypothesis that the central fiber is an SNC divisor.</cite>

We also use two integral exact-sequence inputs: the Wang exact sequence for \(f:X^*\to B^*\), and the long exact sequence of the pair \((X,X^*)\), equivalently the residue/Gysin sequence for the complement of the SNC divisor. <cite>type=theorem; label=integral Wang and pair exactness; title=Failure of the invariant cycle theorem over Z; authors=Donu Arapura, Francois Greer, and Yilong Zhang; source_url=https://arxiv.org/abs/2602.07302; verifier_locator=Section 8.1, display (14), p. 22; statement_match=exact; statement=the Wang sequence and the long exact sequence of the pair (X, X^*), both of which are exact over Z; usage=Provides the integral exactness used in STEP1 and the integral zero-residue extension criterion used in STEP5.</cite>

### STEP1: Lift invariant classes to the punctured total space

**Claim:** Let \(X^*=X\setminus X_0\), let \(i_t:X_t\hookrightarrow X^*\), and let \(T\) denote monodromy on \(H^1(X_t,\mathbb Z)\). For every \(\alpha\in H^1(X_t,\mathbb Z)\) satisfying \(T\alpha=\alpha\), there exists \(\beta\in H^1(X^*,\mathbb Z)\) such that
\[
i_t^*\beta=\alpha.
\]

**Proof:**
Since \(f:X^*\to B^*\) is a proper smooth map, it is a \(C^\infty\) fiber bundle over the punctured disk. Its monodromy around a positive generator of \(\pi_1(B^*,t)\) is \(T\). The degree-one part of the integral Wang exact sequence is
\[
H^1(X^*,\mathbb Z)\xrightarrow{i_t^*}H^1(X_t,\mathbb Z)
\xrightarrow{T-I}H^1(X_t,\mathbb Z).
\]
Exactness at \(H^1(X_t,\mathbb Z)\) gives
\[
\operatorname{im}(i_t^*)=\ker(T-I)=H^1(X_t,\mathbb Z)^T.
\]
Thus every \(T\)-invariant \(\alpha\) is \(i_t^*\beta\) for some \(\beta\in H^1(X^*,\mathbb Z)\).

**Dependencies:** S1; integral Wang and pair exactness citation above.

---

### STEP2: Local residue difference and saturated vanishing loop ⭐ KEY STEP

**Claim:** Write the reduced SNC fiber as \(X_0=\bigcup_{a=1}^r D_a\). For every \(\beta\in H^1(X^*,\mathbb Z)\), every point \(p\in D_a\cap D_b\) lying on a codimension-two stratum with \(a\ne b\), and the standard semistable local coordinates
\[
f=z_1\cdots z_k,\qquad D_a=\{z_1=0\},\qquad D_b=\{z_2=0\},
\]
let \(\delta_{ab,p}\in H_1(X_t,\mathbb Z)\) be the image of the loop
\[
\theta\mapsto (z_1,z_2,z_3,\ldots,z_k)
=(c e^{i\theta},c e^{-i\theta},c_3,\ldots,c_k)
\]
in the nearby fiber \(X_t\), with constants chosen so \(z_1\cdots z_k=t\). Then
\[
\operatorname{res}_{D_a}(\beta)-\operatorname{res}_{D_b}(\beta)
=
\langle i_t^*\beta,\delta_{ab,p}\rangle
\]
as integers, and
\[
\delta_{ab,p}\in \operatorname{Sat}\operatorname{im}\bigl(T_*-I:H_1(X_t,\mathbb Z)\to H_1(X_t,\mathbb Z)\bigr),
\]
i.e. there exists an integer \(e_{ab,p}\ge 1\) such that
\[
e_{ab,p}\delta_{ab,p}\in \operatorname{im}\bigl(T_*-I:H_1(X_t,\mathbb Z)\to H_1(X_t,\mathbb Z)\bigr).
\]
Consequently, if \(i_t^*\beta\in H^1(X_t,\mathbb Z)^T\), then
\[
\operatorname{res}_{D_a}(\beta)=\operatorname{res}_{D_b}(\beta)
\]
for every pair \(D_a,D_b\) meeting in a codimension-two stratum.

**Proof:**
<key-original-step>
We prove the three assertions in order.

First, fix a sufficiently small coordinate polydisk \(U\) around \(p\). In \(U\cap X^*\), let \(\mu_a\) be the positive meridian around \(D_a\), obtained by increasing \(\arg z_1\) once while all other coordinates are fixed and nonzero. Define \(\mu_b\) similarly by increasing \(\arg z_2\) once. By definition of the integral residue,
\[
\operatorname{res}_{D_a}(\beta)=\langle\beta,\mu_a\rangle,\qquad
\operatorname{res}_{D_b}(\beta)=\langle\beta,\mu_b\rangle .
\]
The loop \(\delta_{ab,p}\) winds once positively in the \(z_1\)-coordinate, once negatively in the \(z_2\)-coordinate, and has zero winding in the remaining \(z_i\)-coordinates. Therefore, in
\[
H_1(U\cap X^*,\mathbb Z)\cong \mathbb Z\langle\mu_1,\ldots,\mu_k\rangle
\]
its class is \([\mu_a]-[\mu_b]\). Since the loop is contained in \(X_t\), evaluating \(\beta\) on it is the same as evaluating \(i_t^*\beta\). Hence
\[
\langle i_t^*\beta,\delta_{ab,p}\rangle
=\langle\beta,\mu_a-\mu_b\rangle
=\operatorname{res}_{D_a}(\beta)-\operatorname{res}_{D_b}(\beta).
\]

Second, we prove the saturated-image assertion. We will use the following elementary lattice criterion. Let \(L\) be a finitely generated abelian group and \(M\subset L\). For \(v\in L\),
\[
v\in\operatorname{Sat}(M)
\]
if and only if every homomorphism \(\ell:L\to\mathbb Z\) with \(\ell(M)=0\) also satisfies \(\ell(v)=0\). Indeed, \(v\in\operatorname{Sat}(M)\) means that the class of \(v\) is torsion in \(L/M\), and homomorphisms to \(\mathbb Z\) detect exactly the torsion-free quotient of \(L/M\).

We next reduce the local loop to a vanishing cycle in a nodal curve degeneration. If \(\dim_{\mathbb C}X_t=1\), take the curve family to be \(X\to B\) itself near \(p\). If \(\dim_{\mathbb C}X_t=n\ge2\), choose \(n-1\) sufficiently general very ample hypersurfaces through \(p\), with tangent spaces transverse to all local SNC strata, avoiding the codimension at least three strata away from \(p\), and locally given at \(p\) by \(z_3=\cdots=z_{n+1}=0\). Smoothness at \(p\) follows from this prescribed tangent choice, and Bertini's theorem gives smoothness away from \(p\). Thus their intersection is a smooth complete-intersection surface \(\mathcal C\subset X\) whose map \(\mathcal C\to B\) is a projective family of nodal curves, smooth over \(B^*\), and whose central fiber has at \(p\) the node \(z_1z_2=0\). <cite>type=theorem; label=Bertini hyperplane smoothness; title=The Stacks project, More on Morphisms, Section 37.32; authors=The Stacks Project Authors; source_url=https://stacks.math.columbia.edu/tag/0G4C; verifier_locator=Remark 37.32.4; statement_match=exact; statement=for a general \(v \in V = kT_0 \oplus \ldots \oplus kT_n\) the corresponding hyperplane section \(X \cap H_v\) is smooth; usage=Used to choose smooth complete-intersection slices through p, transverse to the SNC strata.</cite>

Let \(C_t=\mathcal C\cap X_t\), and let \(\nu:C_t\hookrightarrow X_t\) be the inclusion. The vanishing circle \(v_p\in H_1(C_t,\mathbb Z)\) associated with the node \(p\) is represented in the same local coordinates by the loop
\[
\theta\mapsto (c e^{i\theta},c e^{-i\theta},0,\ldots,0)
\]
inside the curve fiber, and \(\nu_*v_p=\delta_{ab,p}\).

We claim that every vanishing circle of the nodal curve family lies in
\[
\operatorname{Sat}\operatorname{im}(T_{\mathcal C,*}-I:H_1(C_t,\mathbb Z)\to H_1(C_t,\mathbb Z)).
\]
Let \(v_1,\ldots,v_s\in H_1(C_t,\mathbb Z)\) be all vanishing circles, and let \(\Delta_i\in H^1(C_t,\mathbb Z)\) be the Poincare dual of \(v_i\), so that evaluation of a class \(\lambda\in H^1(C_t,\mathbb Z)\) on \(v_i\) is, up to the fixed orientation sign, the cup-product pairing \((\lambda,\Delta_i)\). The Picard-Lefschetz formula for a nodal curve degeneration says that, for some sign \(\varepsilon=\pm1\),
\[
T_{\mathcal C}(\lambda)=\lambda+\varepsilon\sum_{i=1}^s(\lambda,\Delta_i)\Delta_i .
\]
<cite>type=theorem; label=Picard-Lefschetz formula; title=Abelian varieties with no power isogenous to a Jacobian; authors=Olivier de Gaay Fortman and Stefan Schreieder; source_url=https://arxiv.org/abs/2401.06577; verifier_locator=Lemma 2.19 and Lemma 2.20, pp. 15-16; statement_match=exact; statement=T(alpha) = alpha + sum_i (alpha · delta_i)delta_i; usage=Applied to the nodal curve slice to show that invariant integral H^1-classes vanish on each vanishing circle, hence each vanishing circle is in the saturation of im(T_*-I).</cite>

Now take any homomorphism \(\ell:H_1(C_t,\mathbb Z)\to\mathbb Z\) that vanishes on \(\operatorname{im}(T_{\mathcal C,*}-I)\). Via the universal coefficient identification \(H^1(C_t,\mathbb Z)=\operatorname{Hom}(H_1(C_t,\mathbb Z),\mathbb Z)\), let \(\lambda\) be the corresponding cohomology class. For every \(x\in H_1(C_t,\mathbb Z)\),
\[
\bigl(T_{\mathcal C}\lambda-\lambda\bigr)(x)
=\lambda\bigl((T_{\mathcal C,*}-I)x\bigr)
=0,
\]
so \(\lambda\) is monodromy-invariant. Substituting this into the Picard-Lefschetz formula gives
\[
0=\varepsilon\sum_{i=1}^s(\lambda,\Delta_i)\Delta_i.
\]
Cup-product pairing this equality with \(\lambda\) gives
\[
0=\varepsilon\sum_{i=1}^s(\lambda,\Delta_i)(\Delta_i,\lambda)
=-\varepsilon\sum_{i=1}^s(\lambda,\Delta_i)^2.
\]
The last integer sum can vanish only if \((\lambda,\Delta_i)=0\) for every \(i\). Therefore \(\ell(v_i)=0\) for every vanishing circle \(v_i\). By the lattice criterion, each \(v_i\), in particular \(v_p\), lies in the saturation of \(\operatorname{im}(T_{\mathcal C,*}-I)\).

Parallel transport of the curve fibers is the restriction of parallel transport of the ambient fibers, so
\[
\nu_*\bigl((T_{\mathcal C,*}-I)y\bigr)=(T_*-I)\nu_*y
\]
for every \(y\in H_1(C_t,\mathbb Z)\). Since some positive multiple of \(v_p\) lies in \(\operatorname{im}(T_{\mathcal C,*}-I)\), applying \(\nu_*\) shows that the same positive multiple of
\[
\delta_{ab,p}=\nu_*v_p
\]
lies in \(\operatorname{im}(T_*-I)\). Thus
\[
\delta_{ab,p}\in \operatorname{Sat}\operatorname{im}(T_*-I:H_1(X_t,\mathbb Z)\to H_1(X_t,\mathbb Z)).
\]

Third, suppose \(i_t^*\beta\) is \(T\)-invariant. For every \(x\in H_1(X_t,\mathbb Z)\),
\[
\langle i_t^*\beta,(T_*-I)x\rangle
=\langle (T-I)i_t^*\beta,x\rangle
=0.
\]
Because \(i_t^*\beta\) is integer-valued, it also vanishes on the saturation of \(\operatorname{im}(T_*-I)\). Applying this to \(\delta_{ab,p}\) gives
\[
\langle i_t^*\beta,\delta_{ab,p}\rangle=0.
\]
The residue-difference formula already proved then gives
\[
\operatorname{res}_{D_a}(\beta)-\operatorname{res}_{D_b}(\beta)=0,
\]
which is the required equality of adjacent residues.
</key-original-step>

**Dependencies:** S2, S3; Bertini hyperplane smoothness citation; Picard-Lefschetz formula citation.

---

### STEP3: Invariant lifts have diagonal residue

**Claim:** For every \(\beta\in H^1(X^*,\mathbb Z)\) satisfying \(i_t^*\beta\in H^1(X_t,\mathbb Z)^T\), there exists an integer \(m\in\mathbb Z\) such that
\[
\operatorname{res}(\beta)=m(1,1,\ldots,1)\in \bigoplus_{a=1}^r \mathbb Z[D_a].
\]

**Proof:**
Let \(\Gamma\) be the dual graph of the SNC divisor \(X_0=\bigcup_{a=1}^rD_a\): its vertices are the components \(D_a\), and two vertices are joined by an edge when the corresponding components meet. Under the usual convention that a complex projective variety is connected, the fiber \(X_0\) is connected; because the components \(D_a\) are connected, this is equivalent to connectedness of \(\Gamma\).

For every edge between \(D_a\) and \(D_b\), choose a point \(p\) in a codimension-two stratum of \(D_a\cap D_b\). STEP2 gives
\[
\operatorname{res}_{D_a}(\beta)=\operatorname{res}_{D_b}(\beta).
\]
Because \(\Gamma\) is connected, for each \(D_a\) there is a path
\[
D_1=D_{a_0},D_{a_1},\ldots,D_{a_N}=D_a
\]
in \(\Gamma\). Repeatedly applying the adjacent equality along this path gives
\[
\operatorname{res}_{D_a}(\beta)=\operatorname{res}_{D_1}(\beta).
\]
Set \(m=\operatorname{res}_{D_1}(\beta)\in\mathbb Z\). Then every component residue is \(m\), so
\[
\operatorname{res}(\beta)=m(1,1,\ldots,1).
\]

**Dependencies:** STEP2.

---

### STEP4: Kill the common residue without changing the fiber class

**Claim:** Let \(\eta\in H^1(B\setminus\{0\},\mathbb Z)\) be the generator with value \(1\) on the positively oriented circle around \(0\). If \(\beta\in H^1(X^*,\mathbb Z)\) satisfies
\[
\operatorname{res}(\beta)=m(1,\ldots,1),
\]
then
\[
\widetilde\beta:=\beta-m f^*\eta
\]
satisfies
\[
i_t^*\widetilde\beta=i_t^*\beta
\quad\text{and}\quad
\operatorname{res}(\widetilde\beta)=0.
\]

**Proof:**
Let \(\mu_a\) be a positive meridian around \(D_a\). In semistable local coordinates near a general point of \(D_a\),
\[
f=z_1\cdots z_k
\]
with \(D_a=\{z_1=0\}\). Along \(\mu_a\), the coordinate \(z_1\) winds once positively and all other \(z_i\)'s are fixed and nonzero. Therefore \(f(\mu_a)\) winds once positively around \(0\in B\). Since \(\eta\) evaluates to \(1\) on that base loop,
\[
\operatorname{res}_{D_a}(f^*\eta)=\langle f^*\eta,\mu_a\rangle=1.
\]
This holds for every \(a\), so
\[
\operatorname{res}(f^*\eta)=(1,\ldots,1).
\]
Hence
\[
\operatorname{res}(\widetilde\beta)
=\operatorname{res}(\beta)-m\operatorname{res}(f^*\eta)
=m(1,\ldots,1)-m(1,\ldots,1)=0.
\]
Finally, \(f\circ i_t:X_t\to B^*\) is the constant map with value \(t\), so
\[
i_t^*f^*\eta=(f\circ i_t)^*\eta=0.
\]
Thus
\[
i_t^*\widetilde\beta=i_t^*\beta-m\,i_t^*f^*\eta=i_t^*\beta.
\]

**Dependencies:** S2, STEP3.

---

### STEP5: Zero-residue classes extend across the central fiber

**Claim:** For every \(\widetilde\beta\in H^1(X^*,\mathbb Z)\) satisfying
\[
\operatorname{res}(\widetilde\beta)=0,
\]
there exists \(\gamma\in H^1(X,\mathbb Z)\) such that
\[
j^*\gamma=\widetilde\beta,
\]
where \(j:X^*\hookrightarrow X\) is the inclusion.

**Proof:**
The integral long exact sequence of the pair \((X,X^*)\), written in residue/Gysin form for the complement of the SNC divisor, contains the exact segment
\[
H^1(X,\mathbb Z)\xrightarrow{j^*}H^1(X^*,\mathbb Z)
\xrightarrow{\operatorname{res}}\bigoplus_{a=1}^r\mathbb Z[D_a].
\]
Exactness at \(H^1(X^*,\mathbb Z)\) gives
\[
\ker(\operatorname{res})=\operatorname{im}(j^*).
\]
Since \(\operatorname{res}(\widetilde\beta)=0\), there exists \(\gamma\in H^1(X,\mathbb Z)\) with \(j^*\gamma=\widetilde\beta\).

**Dependencies:** S2; integral Wang and pair exactness citation.

---

### STEP6: Construct the required lift on \(X\)

**Claim:** For every \(\alpha\in H^1(X_t,\mathbb Z)^T\), there exists \(\gamma\in H^1(X,\mathbb Z)\) such that
\[
\gamma|_{X_t}=\alpha.
\]

**Proof:**
Let \(\alpha\in H^1(X_t,\mathbb Z)^T\). By STEP1, choose \(\beta\in H^1(X^*,\mathbb Z)\) such that
\[
i_t^*\beta=\alpha.
\]
By STEP3, the residue of \(\beta\) is diagonal:
\[
\operatorname{res}(\beta)=m(1,\ldots,1)
\]
for some \(m\in\mathbb Z\). By STEP4,
\[
\widetilde\beta=\beta-m f^*\eta
\]
satisfies \(\operatorname{res}(\widetilde\beta)=0\) and \(i_t^*\widetilde\beta=i_t^*\beta=\alpha\). By STEP5, choose \(\gamma\in H^1(X,\mathbb Z)\) such that
\[
j^*\gamma=\widetilde\beta.
\]
Since the inclusion \(X_t\hookrightarrow X\) factors as \(X_t\xrightarrow{i_t}X^*\xrightarrow{j}X\), we obtain
\[
\gamma|_{X_t}=i_t^*j^*\gamma=i_t^*\widetilde\beta=\alpha.
\]

**Dependencies:** STEP1, STEP3, STEP4, STEP5.

---

### GOAL: Main Result

**Claim:** Prove or disprove the following statement:

Let \( X \to B \) be a one-parameter family of complex projective varieties over a holomorphic disk \( B \), and the fiber of 0 is a simple normal crossing divisor. Let \( t \in B \setminus \{0\} \), and denote the fiber over \( t \) by \( X_t \). Let \( T \) be the monodromy operator acting on \( H^1(X_t, \mathbb{Z}) \). Then the natural restriction map
\[
H^1(X, \mathbb{Z}) \to H^1(X_t, \mathbb{Z})^T
\]
to the \( T \)-invariant submodule is surjective.

**Proof:**
The restriction map lands in \(H^1(X_t,\mathbb Z)^T\) because its image factors through \(H^1(X^*,\mathbb Z)\), whose restriction to \(H^1(X_t,\mathbb Z)\) lies in the kernel of \(T-I\) by the Wang exact sequence. STEP6 proves the reverse containment: every \(\alpha\in H^1(X_t,\mathbb Z)^T\) is the restriction of some \(\gamma\in H^1(X,\mathbb Z)\). Therefore the natural restriction map
\[
H^1(X,\mathbb Z)\longrightarrow H^1(X_t,\mathbb Z)^T
\]
is surjective. Thus the stated assertion is true.

**Dependencies:** STEP6.

## Key Ideas

The proof first lifts an invariant integral class from the smooth fiber to the punctured total space using the integral Wang sequence. Such a lift may have residues around the components of the central divisor. The key local calculation shows that the difference of two adjacent residues is the value of the fiber class on a local vanishing loop, and that this loop lies in the saturation of \(\operatorname{im}(T_*-I)\). An invariant integral class vanishes on that saturation, so adjacent residues are equal. Connectedness of the SNC dual graph makes all residues one common integer, and subtracting that integer times \(f^*\eta\) kills the residue without changing the restriction to \(X_t\). The zero-residue class then extends across \(X_0\) by the integral pair/Gysin exact sequence.

## Deviations from Decomposition Plan

Used a hyperplane-slice proof of the saturated-image assertion in STEP2, reducing the local loop to a vanishing circle in a nodal curve degeneration and applying Picard-Lefschetz there. This supplies the detailed justification requested by the decomposition plan. Otherwise followed the decomposition plan.
