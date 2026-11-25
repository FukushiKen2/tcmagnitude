# Critical-path audit — 2026-11-25

Scope: independent rereading of Sections 2, 3, 4, 5 and 7 of the manuscript. This is a proof-status inventory, not a referee certificate.

## Two independent inequalities

The quantitative theorem combines:

```
#C_g >= ||A_M||_Delta >= c_n ||M||^2.
```

The first inequality requires the Section 2 canonical comparison, Section 3 nerve, Section 6 regularity, and Section 7 cellular localization. The second requires the Section 4 norm-controlled bounded lift and Section 5 duality. The GC computation alone proves neither.

## Checks that pass at the algebraic/local level

1. The exterior augmentation quotient C_k(Y)/boundary -> wedge^k I, and the homogeneous exterior cup cochain t_k, have the claimed no-factorial formula; the differences form a unit-triangular wedge transformation.
2. The double-complex recursion a_(p+1)=-delta b_p and d_G b_p=(-1)^p a_p yields a_p-d_tot b_p=a_(p+1). The norm recursion produces (k+1)!.
3. The odd/even cup products in Section 5 give evaluation 1 and the claimed constants, conditional on Section 4's lift.
4. For local degree in Section 7, the barycentric coordinate differences equal -F/W with W continuous positive. Homotopy to constant positive W does not change the local Brouwer degree. Since N=2n is even, the orientation sign is sign(det dF).
5. The localization proof should explicitly explain that a preimage of a top-cell barycenter has exactly N+1 positive labels (otherwise nerve dimension exceeds N), all with equal length; at least one minimizes, so all minimize. Such preimages lie in C_g. This global argument is currently implicit.

## Outstanding rigorous checks

**P1: Section 4 bounded lift.** Independently check the bounded horizontal comparison quasi-isomorphism, sign-twisted vertical mean contraction, and initial relative primitive, including cochain identifications and exact norm controls. Formal telescoping alone does not certify this.

**P1: Section 2/7 global comparison.** Write an explicit equivariant chain comparison from the nerve map to the exterior canonical class, including orientation conventions, and a precise cellular degree argument for the quotient CW complex. This is needed for the integral localization identity.

**P2: Section 5 fundamental cocycle.** Verify the precise isometric bounded-cohomology/simplicial-volume duality used to choose a bounded alternating homogeneous cocycle representing normalized orientation.

**P2: Prior art.** Compare the genericity proof to Kupka-Peixoto-Pugh (2006) and GC upper bounds to Mescher-Stegemeyer. No exhaustive originality claim is justified.

## Verdict

The manuscript has a coherent two-result structure, with GC calculation independent of the quantitative cohomology/localization branch. The main counting theorem is **not yet independently referee-verified**, chiefly because the bounded-lift and global class-comparison steps require more detailed certification. Do not label the entire paper submission-ready on the strength of Section 6 alone.
