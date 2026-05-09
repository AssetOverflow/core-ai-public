# CORE Yellowpaper: Geometric Foundations

**High-Level Overview — Mathematical Motivation**

> The full Yellowpaper, including complete metric definitions, Clifford primitive specifications, and all derivations, is available to credentialed reviewers upon request. See [SECURITY.md](../SECURITY.md).

---

## What the Yellowpaper Contains

The full Yellowpaper derives the mathematical foundations underlying the CORE architecture from first principles. This public overview provides section headers and motivating descriptions only.

---

## Section 1: Why Hyperbolic Space for Episodic Memory

**Motivation:** Episodic memory must accommodate richly branching, hierarchical structure. Hyperbolic geometry is the natural substrate for tree-structured or hierarchical data because hyperbolic space grows exponentially with radius — meaning that exponentially many distinct memory traces can be encoded at equal geodesic distances from the origin.

A transformer KV cache grows linearly in context length; a hyperbolic manifold grows in representational capacity exponentially with geometric depth. For long-horizon context, there is no flat-space equivalent.

---

## Section 2: Clifford Geometric Algebra as the Representation Language

**Motivation:** Natural language has intrinsic grade structure: entities are things, relations are operators between things, and assertions are weightings on propositions. Clifford geometric algebra is the unique algebra that naturally represents this hierarchy — scalars, vectors, bivectors (rotors), and trivectors correspond precisely to assertion weights, entities, relations, and modality frames.

Representing all of these as undifferentiated high-dimensional vectors (as in standard embeddings) discards the grade structure and loses the ability to enforce type-safe geometric operations.

---

## Section 3: The Propagation Operator Family

**Motivation:** Computation in CORE is field propagation rather than attention. The propagation operators are the analogs of network layers in a transformer, but they act on the Clifford field rather than on token matrices.

The full Yellowpaper derives the properties that the propagation operators must satisfy to preserve manifold invariants. The operator specifications themselves are proprietary and not included in this public document.

---

## Section 4: Dual-Correction and the Clifford Reverse

**Motivation:** In Clifford algebra, every multivector has a natural reverse (the conjugate) obtained by reversing the order of basis vector products. The reverse of a forward propagation operator is its natural corrective counterpart.

The dual-correction principle — that every forward operator must have a corrective conjugate — is not a design choice but a consequence of the algebra. CORE uses this structure to implement phase-cancellation corrections that are algebraically invertible.

---

## Section 5: The Three-Manifold Fiber Bundle

**Motivation:** M_W, M_E, and M_S are not three independent spaces. They are fibers in a temporal bundle: M_W is the base, M_E accumulates as sessions extend, and M_S is the long-run limit as episodic content consolidates.

The bundle structure means that information can flow between manifolds only through well-defined fiber projection and consolidation operations — there is no uncontrolled leakage between memory timescales.

---

## Section 6: Grade Purity as a Topological Invariant

**Motivation:** If Grade-1 vectors (entities) are allowed to drift into Grade-2 bivector space (relations), the semantic structure of the field degrades. Grade purity is a topological invariant of the field, analogous to a conservation law.

The geometric invariant registry in CORE tracks six named invariants. The full specifications are in the private repository. The public record is that these invariants exist, are tracked at runtime, and trigger corrective action when violated.
