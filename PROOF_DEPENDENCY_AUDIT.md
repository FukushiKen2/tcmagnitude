# Dependency audit — 2026-11-25

This is an independent proof-dependency inventory, **not** a certification that every theorem is correct. It distinguishes formal deductions from inputs that must still be verified in a referee-level proof.

## Main quantitative theorem

Let N=2n and C_g={(x,y): m_g(x,y)=N+1}. The claimed count is

    #C_g >= ||A_M||_Delta >= c_n ||M||^2.

The first inequality uses localization (Section 7), the second bounded-cohomological duality (Sections 4–5). Genericity (Section 6) ensures that C_g is finite and the nerve has dimension <=N.

### Branch I: cohomological lower bound

1. **[Sec. 2, lem:exterior-quotient]** Chain quotient C_k(Y)/boundary = wedge^k I. Elementary algebra; chain-level map and equivariance are explicitly written.
2. **[Sec. 2, prop:comparison]** The cocycle t_k on the homogeneous bar resolution represents the exterior canonical class, and its evaluation on [M x M] corresponds to f_*[M x M]. Chain-level calculation is written; rigorous treatment of equivariant chain approximation and local coefficients should be checked independently.
3. **[Sec. 4, lem:horizontal-contraction and lem:AW-comparison]** Total complex computes bounded group cohomology. Explicit contraction and Alexander–Whitney comparison supplied.
4. **[Sec. 4, lem:bounded-vertical and lem:relative-primitive]** Amenable stabilizers provide norm-one vertical contractions in positive degrees; relative bar-prism starts the lifting. Key analytic/normed-cochain step requiring an external expert check.
5. **[Sec. 4, thm:bounded-lift and prop:difference-lift-bound]** A class whose representative restricts to zero on H lifts to an alternating cocycle on S with explicit bound k(k+1)!; special difference cocycle has n(n+1)! bound. Recurrence and arithmetic were checked. Its categorical interpretation should be compared to existing boundedly acyclic-action results.
6. **[Sec. 5, eq:orientation-norm]** Efficient group orientation cocycle from simplicial-volume duality, using the asphericity and isometric comparison theorem. Standard external input.
7. **[Sec. 5, eq:odd-bound and eq:even-bound]** Cup-product evaluation is 1, leading respectively to c_n = 1/(2n(2n+1)!) for odd n and 2/(n^2((n+1)!)^2) for even n. Algebraic arithmetic checked, conditional on steps 2–6.
8. **[Sec. 5, lem:upper-norm]** Optional upper bound ||A_M||_Delta <= ||M x M|| via Hahn–Banach and cochain duality. Not needed for the lower-count argument.

### Branch II: geometric localization

9. **[Sec. 6, lem:metric-submersion and thm:genericity]** The metric variation gives surjectivity of length differences at simultaneous minima. Openness/density uses finite-label reduction and parametric transversality; this deserves a standalone expert check for all label configurations.
10. **[Sec. 3, lem:uniform-allowance, prop:Phi]** Uniform nerve identification and equivariant partition of unity.
11. **[Sec. 3, lem:no-inversions and prop:top-simplex]** Quotient CW chains and finite top multiplicity locus.
12. **[Sec. 7, lem:local-degree and lem:localized-cycle]** Continuous local-degree calculation; explicitly avoids differentiating the nonsmooth minimum. Need care that the allowance can be chosen uniformly while computing barycenter preimages.
13. **[Sec. 7, thm:localization]** A_M is represented by sum of signed top-cell exterior generators. Therefore ||A_M||_Delta <= #C_g.
14. Steps 7 and 13 yield the counting theorem. No dependency on the geodesic-complexity selection lemma.

### Branch III: other conclusions

15. **[Sec. 2, prop:MH-minimal]** Minimal-length degree-two endpoint magnitude homology equals augmentation kernel of the minimizing-label set, rank m_g(x,y)-1; the proof uses magnitude boundaries in degrees 2 and 3.
16. **[Sec. 6, lem:selection and thm:generic-GC]** GC<=2n+1 from continuous sheet selection on locally closed strata; TC<=GC and the known TC value imply equality. This branch is *not* needed for the quantitative count.
17. **[Updated 2026-11-25]** The final equality between GC and maximal magnitude rank now uses Horja's established existence theorem for at least 2n+1 minimizing geodesics, together with the regularity upper bound. It no longer depends on the quantitative counting theorem.

## External prior work affecting novelty

- Paul Horja, *On the number of geodesic segments connecting two points on manifolds of non-positive curvature*, Trans. Amer. Math. Soc. 349 (1997), 5021–5030; arXiv:dg-ga/9502009. The existence of a pair with at least 2n+1 minimizing geodesics in every closed negatively curved manifold **is already known**. The asserted quadratic count is not contained in this existence statement.
- Dranishnikov: calculation of TC for torsion-free hyperbolic groups.
- Li–Löh–Moraschini: boundedly acyclic actions and relative simplicial volume, directly related to the double-complex method.
- Recio-Mitter and Mescher–Stegemeyer: geodesic complexity and cut-locus methods.

## Audit verdict (NOT A PROOF CERTIFICATE)

- Proven internal *formal implications*: (A) if the bounded lifting and comparison claims hold, the cup-product estimates imply the c_n lower bound; (B) if genericity and localization hold, the nerve cycle implies ||A_M||_Delta<=#C_g.
- High-priority remaining independent checks: (i) norm-controlled bounded-cohomology lifting with the chosen cochain conventions; (ii) comparison of the exterior canonical class with the geometric nerve's fundamental cycle, including local-coefficient orientation; (iii) parametric transversality/stratification across metric variations; (iv) mathematical and bibliographic novelty of quadratic quantitative bound.
- Avoid claiming the entire manuscript has been fully validated merely because the arithmetic constants or double-complex signs are consistent.
