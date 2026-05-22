# Analysis Problems (May 19, 2026)

This folder contains proofs for **lower bounds of advection-diffusion equations** across three distinct scenarios. The work is documented in [arXiv:2605.20623](https://arxiv.org/abs/2605.20623).

**Paper:** "Lower Bounds for Advection-Diffusion Equations: An Exploration with AI-Generated Proofs"
**Authors:** Chenyang An, Xiaoqian Xu

## QED Configuration

- **Prover mode:** Decomposition mode
- **Literature survey:** Codex
- **Prover:** GPT-5.5
- **Verifiers:** GPT-5.5

## Results

| Section | Problem | Result |
|---------|---------|--------|
| 2 | Polynomial bound for inviscid shears | Proved |
| 3 | Uniform positive lower bound on mixing scales for diffusive shears | Proved |
| 4 | Exponential bound for rapidly oscillating time-periodic flows | Proved |

## Background

The paper establishes explicit lower bounds for advection-diffusion equations in three settings:
1. A polynomial bound for inviscid shears
2. A uniform positive lower bound on mixing scales for diffusive shears
3. An exponential bound for rapidly oscillating time-periodic flows

The proofs were generated entirely by the multi-agent math proving system QED, without expert human intervention.

## Expert Comments

### Section 2: Polynomial bound for inviscid shears

This section shows that AI is good at handling prove-or-disprove problems. If one direction is not that hard, then AI may be able to solve it. This is quite different from human researchers.

### Section 3: Uniform positive lower bound for diffusive shears

This section demonstrates that given results from humans, AI can easily fill in the gaps and optimize the constants. This illustrates universally useful ways of using AI in mathematical research.

### Section 4: Exponential bound for oscillating flows

This section is remarkable. The problem itself is very intuitive, and one might plan to work on it, but that would mean spending a couple of months learning Floquet theory—quite painful for someone not versed in functional analysis. This problem could easily be part of a research proposal, expecting months or even a year of work. But AI solved it nicely.

The proof is, in some sense, quite standard. What is hard is the combination of standard techniques, especially standard techniques from quite different fields. This is also a very common scenario for human researchers, particularly when training students.

## Overall Assessment

This paper captures three very typical scenarios that a human researcher might face:
1. Trying to determine whether to prove or disprove something
2. Trying to optimize or revise existing proofs
3. Trying to use some particular technique (that may come with a learning cost) to solve a new problem

These scenarios cover a large portion of mathematical research problems. AI demonstrates strong potential—or ability—to contribute meaningfully.

If this paper were written by human beings, it would merit submission to a journal like JDE (Journal of Differential Equations) or SIMA (SIAM Journal on Mathematical Analysis) or higher. It shows that the lower bound for AI capability (since there is almost no cost in human effort, like learning or thinking) is already quite high.

This may suggest that mathematics under a certain level—a level that we cannot even call medium for average mathematicians—should be seen as trivial.

## References

- An, Chenyang; Xu, Xiaoqian. "Lower Bounds for Advection-Diffusion Equations: An Exploration with AI-Generated Proofs". [arXiv:2605.20623](https://arxiv.org/abs/2605.20623), May 2026.
