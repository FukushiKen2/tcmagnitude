# Independent audit: generic negative-curvature metrics

Date: 2026-11-25. Source: Section 6, `6_generic_metrics_and_geodesic_complexity.tex`, as of commit 6406b96 and later finite-parameter update 4825937.

## The precise claim

For a closed manifold M admitting a smooth strictly negatively curved metric, let R_-(M) denote the open space of smooth strictly negatively curved metrics, with Whitney C-infinity topology. Let X be its universal cover. For a in pi_1(M), set L_a^g(u,v)=d_{X,g}(u,av). Say g is regular when, at every pair with a finite set S of all minimizing labels and |S|=k>=2, the differential of (L_a-L_{a0}) for a in S\{a0} has rank k-1.

**Conclusion:** the subset of regular g is open and dense in R_-(M). For regular g the exact-k multiplicity sets (when nonempty) are smooth embedded submanifolds of dimension 2n-k+1, and the 2n+1 stratum is finite.

The following verifies the *formal proof*, not literature-level originality.

## Step 1. Geometric input (independence of length variations)

For two distinct minimizers from x to y their interiors are disjoint. If z lies in both, each has an x-z segment of length d(x,z), and a z-y segment of length d(z,y). All cross concatenations have length d(x,y). A minimizing broken curve cannot have a corner, so both minimizers have the same tangent at z and coincide by uniqueness. In particular each minimizer has a small interior arc disjoint from all other finitely many minimizers.

For k distinct minimizers gamma_0,...,gamma_{k-1}, choose small, disjoint neighborhoods and tensors h_i=chi_i g with nonnegative chi_i supported there. For each j,
D_g L_{a_j}^g(h_i)=(1/2) integral_gamma_j h_i(gamma_dot,gamma_dot) ds.
This gives a diagonal invertible k x k derivative matrix. The k-1 differences relative to a0 consequently have surjective metric derivative. This applies only at *simultaneous global minima*, exactly where needed.

## Step 2. Uniform finite-label reduction

Take a compact fundamental region K in X, and fix a sufficiently small C-infinity neighborhood U of g0. Uniform bilipschitz comparison gives constants lambda>=1 such that lambda^-1 d0 <= dg <= lambda d0 on X for all g in U. The diameter of (M,g) is uniformly bounded on U, and each minimizing a for (u,v) in KxK obeys d0(K,aK)<= lambda * sup_U diam(M,g). The deck action is proper, so only finitely many a satisfy this bound. Let F be their common finite set.

**Quantifier:** F is chosen once for all metrics in U, independently of the endpoint pair in KxK.

## Step 3. Parameter space near a fixed g0

For every S subset F with k>=2, define C_S={(u,v) in KxK: all a in S are minimizing for g0}. This is closed in compact KxK.

If C_S is empty, theta_S=max_{a in S}(L_a^{g0}-m_{g0}) is continuous and strictly positive on KxK, so its minimum is >0. On shrinking U, simultaneous minimizers for S cannot occur.

If C_S is nonempty, for each z in C_S choose a finite set of smooth global symmetric 2-tensors on M whose derivatives of the S-length-difference map are onto. Since the distance branches are smooth near g0,z (the coincident minimizing distance is >0, and X is Hadamard), parameter surjectivity persists over some product neighborhood of (g0,z). By compactness of C_S, finitely many such neighborhoods and tensors suffice. Choose an open neighborhood O_S of C_S in XxX (relative to KxK) with compact complement in KxK and positive theta_S gap there. Shrink the parameter neighborhood so any simultaneous minimum for S occurs in O_S, and the universal distance-difference map is a submersion near all such minima.

Taking the span V of the finitely many tensor variations for every S and shrinking W around 0 in V preserves all the preceding conditions simultaneously; enlarging V never destroys metric-direction surjectivity. Negative curvature stays strict on a sufficiently small W, since M is compact.

## Step 4. Sard/parametric transversality, including boundary of K

For each S choose an open set U_S inside W x (XxX) on which the universal difference map F_S is smooth and submersive, containing every simultaneous minimizer over KxK for every h in W. The zero locus F_S^-1(0) in U_S is a smooth manifold. Its projection to W has a residual set of regular values by Sard/parametric transversality (finite-dimensional parameter space); for a regular parameter h, the endpoint-variable derivative d_(u,v) F_S(h,u,v) is surjective at every zero in (U_S)_h. This argument takes place on the boundaryless open manifold XxX rather than KxK, so no regularity of the boundary of a fundamental region is required. Intersect over finitely many S. Every actual simultaneous minimum on KxK lies in the checked region; equivariance extends regularity to all endpoint pairs.

## Step 5. Openness

Suppose regular g is the limit of nonregular g_i. Fix K and a common finite F as above. Select a nonregular pair in KxK for each g_i. After a subsequence, the same set S of minimizing labels witnesses rank deficiency; also endpoints converge. The limiting branches are smooth because at least two distinct labels minimize and the distance is positive. Their derivatives converge, so rank deficiency persists (vanishing of all (k-1)-minors is closed). At the limit S still minimizes. If more labels minimize, regularity of the full difference system would force regularity of *every* subset, a contradiction. Hence the regular locus is open.

## Step 6. Multiplicity strata

At a regular point with exactly k minimizing labels, the other labels have a locally uniform positive gap (finite-label reduction). The exact-k locus in a neighborhood is precisely the transverse zero locus of the k-1 difference functions, so is a smooth embedded submanifold of codimension k-1. The rank condition forces k-1<=2n, hence k<=2n+1. The top multiplicity stratum has dimension zero. Because {m_g>=2n+1} is closed and equals {m_g=2n+1} for regular g, its compactness and local discreteness imply finiteness.

## Explicit audit cautions

1. The final statement should say “when nonempty, B_k has **dimension** 2n-k+1”, rather than implicitly asserting all k-strata are nonempty.
2. The metric submersion step relies on support disjointness **on M**, not only on the universal cover. Its proof uses the global minimizing property to rule out projected intersection points; one must not merely cite disjointness of distinct lifts in X.
3. In Step 4 Sard's theorem is applied in an **open subset of the universal endpoint manifold XxX**, not to a nonsmooth-boundary fundamental domain KxK.
4. This verification is a formal mathematical audit, not a proof of originality; the literature on generic cut locus and Maxwell strata should still be compared.
5. A separate final check remains: the proof of the finite-valued covering selection theorem and the standard literature computation TC(M)=2n+1 must be correct for the stated GC corollary.


## Literature overlap found 2026-11-25 (important)

Kupka, Peixoto and Pugh, *Focal stability of Riemann metrics*, J. reine angew. Math. **593** (2006), 31–72, DOI 10.1515/CRELLE.2006.029, develops generic transversality and multiplicity bounds for geodesics of equal length between endpoints. Reported sharpened bounds include at most \(2m+1\) equal-length geodesics joining distinct points on a compact \(m\)-manifold for generic metrics; check the exact hypotheses and proof in the original before asserting a precise theorem. This overlaps substantially with the geometric genericity portion of Section 6 (where only minimizing geodesics are used). The current manuscript must not claim novelty for generic length-multiplicity alone without a theorem-by-theorem comparison.

A second background source is Itoh–Sakai on cut loci and the generic-metric singularity-theory literature. Neither source has yet been established to imply the **finite-valued covering selection theorem** or the particular geodesic-complexity equality. Separate validity of the selection proof from novelty of the general-position input.

The general selection theorem, the generic-regularity claim, and the GC equality should remain separate components in the dependency audit.


## Original-source comparison added 2026-11-25

**Kupka–Peixoto–Pugh (2006), *Focal stability of Riemann metrics*, J. reine angew. Math. 593, 31–72, DOI 10.1515/CRELLE.2006.029** is now cited in the article's bibliography, introduction, and Section 6.

The original abstract and Theorem 1.2 state: on a compact m-manifold, for a residual set of metrics, there are at most **2m+2** geodesics of any given equal length joining any pair p,q (including p=q). **Section 7 explicitly sharpens this to 2m+1 when p != q**. The distinction is important: reporting 2m+1 as the unrestricted uniform bound is inaccurate. The article also comments that negative curvature makes the proof more directly global, thanks to uniqueness in homotopy classes, smooth endpoint dependence, and absence of self-intersections upstairs.

Comparison of proven statements:
- KPP: residual generic metrics, all (possibly nonminimizing) geodesics with the same given length, bound 2m+2 universally and 2m+1 for distinct endpoints; analyses the multiexponential map and transversality.
- Current Section 6: a claimed **open dense** set within strictly negatively curved metrics, for which the *simultaneously minimizing distance branches* have full rank \(k-1\); this implies smooth strata of exact minimum multiplicity, a finite top stratum, and an upper bound on geodesic complexity using the separately proved finite-valued covering selection theorem.
- A count-only KPP bound does not establish Section 6's full-rank condition, even though its ideas substantially overlap. Check the full KPP transversality constructions before claiming novelty of the stronger geometric statement.
- Targeted searches of published GC work (Recio-Mitter and Mescher–Stegemeyer, including cut locus fibered-decomposition bounds) did not reveal the exact generic-negative-curvature GC equality. This is an incomplete novelty survey, not proof of absence.


## Closer examination of KPP multi-exponential transversality (2026-11-25)

**Sources inspected:** KPP 2006 original text, Section 6 (Theorem 6.1: fixed basepoint multi-exponential transversality for k>=3) and Section 7 (Lemma 7.3, Corollary 7.5, proof of Theorem 1.2). KPP's proof of the uniform bound uses a multi-exponential map with **varying initial point** and transversality to the diagonal. Its negative-curvature remark notes uniqueness of the geodesic in each homotopy class and smooth dependence on endpoints; these are precisely the smooth-branch facts used in this manuscript.

**Local mathematical equivalence under no conjugate points.** For a fixed configuration of k distinct geodesics with locally well-defined smooth branches from x to y, use initial vectors v_i and set
\[
{\mathscr E}_g(x,v_0,\ldots,v_{k-1})
=((\exp_x^g(v_0),|v_0|_g),\ldots,
  (\exp_x^g(v_{k-1}),|v_{k-1}|_g)).
\]
If every \(\exp_x^g\) has invertible derivative at the v_i, the equal-endpoint equations cut out a smooth submanifold locally parameterized by \((x,y)\), on which the equal-length equations become precisely \(L_{a_i}(x,y)-L_{a_0}(x,y)=0\) (using lengths rather than energy, away from zero). Since the endpoint equations have surjective derivative in the v_i directions, transversality of \({\mathscr E}_g\) to the full endpoint-and-length diagonal is **equivalent** to full rank of the k-1 length differences in the (x,y) variables. This is an application of eliminating a transverse system of constraints.

**What is (and is not) thereby in KPP.** Their proof uses precisely such varying-basepoint multi-transversality for the index bound and includes supporting submersion lemmas. This is much closer to the current geometric regularity condition than the numerical bound alone. But the theorem statement giving an upper bound on the *number* of equal-length geodesics is logically insufficient by itself to assert the full-rank coincidence strata for *every k*. To replace the manuscript's transversality proof with a direct citation, it remains necessary to identify a KPP statement or argument giving simultaneous generic transversality for **all k>=2**, including the k=2 case and every minimizing branch configuration, and to distinguish residual genericity from the manuscript's open-dense condition. Until that exact strengthening is checked, keep the independent shorter proof and cite KPP as substantive precursor.

**Novelty adjustment:** Do not claim the **mechanism** of distance-difference multi-transversality itself is entirely new; it is closely related, and in the absence of conjugate points locally equivalent, to KPP's varying-basepoint multi-exponential transversality. The GC consequence remains a separately supported candidate.


## Stress test: square flat two-torus (2026-11-25)

Let \(M=\mathbb R^2/\mathbb Z^2\) have its standard flat metric. Take \(x=[(0,0)]\), \(y=[(1/2,1/2)]\). There are exactly four shortest geodesics, represented by the four displacement vectors
\[
 w_{ij}=(1/2+i,1/2+j),\qquad i,j\in\{0,-1\}.
\]
For each label \(a\), in local Euclidean endpoint coordinates
\[
L_a(u,v)=\lVert v-u+a\rVert.
\]
Consequently every differential \(d(L_a-L_{a_0})\) vanishes on the two-dimensional diagonal translation directions \(\{(\delta u,\delta v):\delta u=\delta v\}\). In particular, its rank is at most two although \(k-1=3\) when \(k=4\). The square flat torus is **not regular** according to the manuscript's definition.

This is a useful stress test, not a counterexample to the negative-curvature theorem. It proves that mere **finiteness** and even a small **number** of minimizing geodesics do not imply the required independence of endpoint length differences. It also warns against extending the genericity statement unchanged to the space of nonpositively curved metrics: on a two-torus nonpositive curvature forces flatness by Gauss--Bonnet, so the permitted metric perturbations are severely restricted.

## Comparison with GC literature (2026-11-25)

Mescher--Stegemeyer, *Geodesic complexity via fibered decompositions of cut loci*, J. Appl. Comput. Topol. 7 (2023), Theorem 3.2, bounds GC by one plus a sum of sectional categories on a **given fibered decomposition** of the total cut locus. It does not, from the theorem statement alone, imply the manuscript's dimension-only \(N+1\) selection bound for an arbitrary proper finite-valued subset of a covering. Whether the latter is contained in more general stratified-map or dimension-theoretic literature remains an open bibliographic question. The numerical claim GC=TC for generic negative-curvature metrics still requires this independent selection argument; prior-art absence is not established by the targeted search.
