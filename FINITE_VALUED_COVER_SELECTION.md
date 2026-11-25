# Finite-valued covering selection theorem

This note isolates the selection theorem used in Section 6 of the article. It is an independently stated and checked mathematical argument, not a claim of bibliographic novelty.

## Theorem

Let \(B\) be a second-countable smooth manifold of dimension \(N\), \(q:E\to B\) a smooth covering, and \(Z\subset E\) a closed subset such that \(q|_Z:Z\to B\) is proper and onto, with nonempty finite fibers. Let
\[
B_k=\{b\in B:\#(q^{-1}(b)\cap Z)=k\}.
\]
Suppose every nonempty \(B_k\) is a smooth **embedded** submanifold of \(B\), of dimension \(d_k\leq N-k+1\). Then there exist at most \(N+1\) pairwise disjoint locally closed subsets \(A_0,\ldots,A_N\) covering \(B\), such that \(q|_Z\) admits a continuous section over each \(A_j\).

The theorem does **not** assume \(q|_Z\) is a covering map: candidate sheets may disappear as the base point moves.

## Proof audit

**(1) Finite local list of possible sheets.** Over an evenly covered neighborhood \(U\) of \(b\), each point of \(Z_b\) lies in a distinct smooth local sheet of \(q\). Properness of \(q|_Z\) implies there is a smaller neighborhood \(U'\) such that no points of \(Z\) over \(U'\) lie on any other sheet. Otherwise a sequence \(b_i\to b\), \(z_i\in Z_{b_i}\) outside all selected sheets would have a convergent subsequence by properness, contradicting the description of \(Z_b\). Consequently fiber cardinality \(k(b)\) is upper semicontinuous. In particular \(B_k=\{k\geq k\}\cap\{k<k+1\}\) is locally closed. The dimension bound forces \(k\leq N+1\) on nonempty strata.

**(2) Generic auxiliary functions.** Choose \(N+1\) smooth functions \(f_0,\ldots,f_N:E\to\mathbb R\) generically. For each \(B_k\), work in a countable family of smooth charts on which its \(k\) active sheets may be enumerated as smooth local sections \(z_1,\ldots,z_k\). For a collection of partitions \(\mathcal P=(\mathcal P_0,\ldots,\mathcal P_N)\) of \(\{1,\ldots,k\}\), let \(D_{\mathcal P}\subset(\mathbb R^k)^{N+1}\) impose within-block equalities of the corresponding coordinates. It has codimension
\[
r(\mathcal P)=\sum_{j=0}^N(k-|\mathcal P_j|).
\]
The map \((f,b)\mapsto((f_j(z_i(b)))_{i=1}^k)_{j=0}^N\) is a submersion in the smooth-function variables: at any \(b\) the evaluation points \(z_i(b)\) are distinct, so their values can be changed independently by compactly supported smooth bump functions on \(E\). The standard parametric transversality theorem, applied in countable coordinate charts and on compact exhaustions, gives a residual tuple \(f\) transverse to every \(D_{\mathcal P}\), simultaneously. If \(r(\mathcal P)>d_k\), the corresponding inverse image is empty. For the actual equality partitions at \(b\in B_k\), therefore,
\[
r(b)=\sum_{j=0}^N(k-|\mathcal P_j(b)|)\leq d_k\leq N-k+1.
\]

**(3) Distinguishing candidates.** If two active sheets had the same evaluation vector \((f_0,\ldots,f_N)\), they would be in a common block of every \(\mathcal P_j\). Each \(k-|\mathcal P_j|\) would then be at least one; hence \(r(b)\geq N+1\), contradicting the preceding inequality. Consequently the lexicographically least evaluation vector determines a **unique** active sheet for each \(b\).

**(4) The coloring is upper semicontinuous.** Define
\[
c(b)=k(b)-1+r(b).
\]
From the dimension estimate, \(0\leq c(b)\leq N\). Near any fixed \(b\), all active candidates are among finitely many sheets indexed by \(Z_b\), so \(k(b')\leq k(b)\). Each equality partition \(\mathcal P_j(b')\) is the restriction of a refinement of the partition at \(b\): two values unequal at \(b\) remain unequal for sufficiently nearby \(b'\). This implies
\[
k(b')-|\mathcal P_j(b')|\leq k(b)-|\mathcal P_j(b)|
\]
for each \(j\), so \(c(b')\leq c(b)\). Hence \(c\) is integer-valued and upper semicontinuous.

**(5) Locally closed planners.** Set \(A_j=\{b:c(b)=j\}\). Since \(c\) is upper semicontinuous and integer-valued, \(\{c\geq j\}\) is closed and \(\{c<j+1\}\) is open; their intersection \(A_j\) is locally closed. At \(b\in A_j\), for nearby \(b'\in A_j\), each of the nonnegative summands \(k-1\) and \(k-|\mathcal P_i|\) in \(c\) can only decrease. Their sum does not change, so none decreases. Thus all active candidates persist and all equality partitions remain unchanged. Signs of unequal evaluations also remain unchanged. The lexicographically minimal candidate is therefore represented by a fixed smooth covering sheet near \(b\) inside \(A_j\). This proves continuity of the section.

The \(A_j\) cover \(B\), are pairwise disjoint and locally closed; hence they give the asserted planner decomposition. \(\square\)

## Application to geodesic complexity

Take \(B=M\times M\), \(N=2n\), \(E\to B\) the covering of fixed-endpoint homotopy classes of paths, and \(Z\) the subset consisting of classes whose unique lifted geodesic minimizes distance. Under the regularity assumption in Section 6, the exact \(k\)-multiplicity locus is a smooth embedded submanifold of codimension \(k-1\), so \(d_k=2n-k+1\). The theorem gives
\[
\mathrm{GC}(M,g)\leq2n+1.
\]
Combining with \(\mathrm{TC}(M)=2n+1\) proves equality **conditionally on** the separate generic-regularity theorem. The selection theorem itself does not require negative curvature.

## Scope / caveats

- The embedding assumption on \(B_k\) matters. A merely abstract smooth manifold structure on the set \(B_k\) is insufficient for the transversality argument.
- The \((N+1)\)-function transversality argument is an application of standard differential topology, and it does not by itself establish that this theorem is new relative to the literature on set-valued selections, Schwarz genus, or cut-locus stratifications.
- This independent note validates the selection part of Section 6 only. The open-dense regularity assertion, plus the existing TC calculation, are separate inputs.
