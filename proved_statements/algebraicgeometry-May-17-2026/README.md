# Algebraic Geometry Problem (May 17, 2026)

There is one problem in this folder. The problem concerns the **Local Invariant Cycle Theorem over integers for degree one cohomology (LICT_Z for H^1)**. 
## QED Configuration

- **Prover mode:** Decomposition mode
- **Literature survey:** Codex
- **Prover:** GPT-5.5
- **Verifiers:** Gemini, gemini-3.1-pro

**Before the human proof was released on the Internet (May 15, 2026), AI (GPT-5.5) had already produced an independent and different proof (April 25, 2026).**

## Problem Statement

Prove or disprove the following statement:

**(LICT_Z for H^1)** Let $X \to B$ be a one-parameter family of complex projective varieties over a holomorphic disk $B$, and the fiber of 0 is a simple normal crossing divisor. Let $t \in B \setminus \{0\}$, and denote the fiber over $t$ by $X_t$. Let $T$ be the monodromy operator acting on $H^1(X_t, \mathbb{Z})$. Then the natural restriction map
$$H^1(X, \mathbb{Z}) \to H^1(X_t, \mathbb{Z})^T$$
to the $T$-invariant submodule is surjective.

## Difficulty of the Problem

The problem is of moderate difficulty.

## AI's Proof (Summary)

The AI's proof uses the following approach:

The Clemens-Schmid sequence is sliced by the Wang sequence and the exact sequence of the pair $(X, X^*)$, both are exact integrally. Take an invariant class $\alpha \in H^1(X_t, \mathbb{Z})^T$. By the exactness of the Wang sequence, it lifts to a class $\tilde{\alpha} \in H^1(X^*, \mathbb{Z})$. The key steps are:

**Lemma 1:** The coboundary map $H^1(X^*, \mathbb{Z}) \to H^2(X, X^*, \mathbb{Z})$ is identified with the residue map, which takes each $\eta \in H^1(X^*, \mathbb{Z})$ to $\text{Res}_{D_i}(\eta)$ for each component $D_i$ of the central fiber $X_0 = \cup_i D_i$.

**Lemma 2:** For a given invariant class $\alpha \in H^1(X_t, \mathbb{Z})^T$, the lift $\tilde{\alpha} \in H^1(X^*, \mathbb{Z})$ satisfies $\text{Res}_{D_i}(\tilde{\alpha}) = \text{Res}_{D_j}(\tilde{\alpha})$ for all $i, j$.

Then, by Lemma 2, up to adjusting by a class pulled back from $H^1(B^*, \mathbb{Z})$, $\tilde{\alpha}$ lies in the kernel of the coboundary map $H^1(X^*, \mathbb{Z}) \to H^2(X, X^*, \mathbb{Z})$. Then by the exactness of the cohomology of the pair $(X, X^*)$, it lifts to $H^1(X, \mathbb{Z})$. Q.E.D.

## Expert Comments

The method in AI's proof that interprets the coboundary map $H^1(X^*) \to H^2(X, X^*)$ as the residue map (cf. Lemma 1) is **original**. This actually holds in higher degrees by working with Griffiths' residue, but in degree one, this interpretation is the classical residue and is particularly useful for LICT_Z, since one has Lemma 2, which is essential in the proof.

The proof is **elementary and elegant**. (Lemma 1 is essentially residue theory in complex analysis, and Lemma 2 is essentially reduced to Picard-Lefschetz theory for curves.) It provides a different point of view on the integral version of the invariant cycle theorem in degree one.


