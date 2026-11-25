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
