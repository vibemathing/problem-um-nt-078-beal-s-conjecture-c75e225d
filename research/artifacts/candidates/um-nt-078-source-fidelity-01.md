# Candidate source-fidelity audit: Beal's Conjecture (NT-078)

**Verdict:** `candidate_only`  
**Problem:** `problem:um-nt-078-beal-s-conjecture-c75e225d`  
**Attempt:** `attempt:um-nt-078-beal-s-conjecture-c75e225d-source-fidelity-01`  
**Route:** `route:um-nt-078-beal-s-conjecture-c75e225d-source-fidelity`  
**Obligation:** `obligation:um-nt-078-beal-s-conjecture-c75e225d-statement-fidelity`  
**Protected base:** `7cc54d4f77d9f65203884f2339228d2567fc8e0d`  
**Audit date:** 2026-09-09

This note audits statement fidelity only. It does not prove or refute Beal's Conjecture, modify the frozen ProblemContract, or admit mathematical Evidence or a Result.

## 1. Frozen repository statement

> For \(A^x+B^y=C^z\) with \(x,y,z>2\), must \(A,B,C\) share a common prime factor?

Taken as a standalone mathematical sentence, this text does not state the domains of \(A,B,C,x,y,z\), does not explicitly quantify them, and does not state positivity. Those omissions materially affect the proposition: allowing zero, negative, rational, real, or complex values produces a different problem.

## 2. Source comparison

| Source | Domain supplied | Exponent condition | Conclusion | Status/attribution role |
|---|---|---|---|---|
| UnsolvedMath NT-078, “Problem Statement” | Not in the one-sentence field | \(x,y,z>2\) | \(A,B,C\) share a common prime factor | Matches the frozen sentence |
| UnsolvedMath NT-078, “Background” | \(A,B,C,x,y,z\) are positive integers | \(x,y,z>2\) | A common prime factor; negation described by \(\gcd(A,B,C)=1\) | Supplies the missing domain and intended primitive formulation |
| R. D. Mauldin / University of North Texas sponsor page | \(A,B,C,x,y,z\) are positive integers | \(x,y,z>2\) | \(A,B,C\) have a common prime factor | Independent statement maintained in connection with the Beal prize |
| MathWorld, “Beal's Conjecture” | All six variables are positive integers | \(x,y,z>2\) | \(A,B,C\) have a common factor | Corroborates the mathematical content and notes the alternative Tijdeman–Zagier name |

## 3. Source-complete reading

The sources support the following explicit expansion of the intended statement:

\[
\forall A,B,C,x,y,z\in\mathbb Z_{>0},\quad
\bigl(x>2\land y>2\land z>2\land A^x+B^y=C^z\bigr)
\Longrightarrow
\exists p\ \bigl(p\text{ prime}\land p\mid A\land p\mid B\land p\mid C\bigr).
\]

Equivalently, the intended negation is the existence of positive integers
\(A,B,C,x,y,z\), with \(x,y,z>2\), satisfying

\[
A^x+B^y=C^z
\quad\text{and}\quad
\gcd(A,B,C)=1.
\]

This formal expansion is a source annotation, not a silent edit to the frozen ProblemContract.

## 4. Terminology audit

“Share a common prime factor” means that one prime divides all three bases. Its negation is \(\gcd(A,B,C)=1\).

The UnsolvedMath background uses “\(A,B,C\) are coprime.” In source-fidelity work this should be recorded as joint coprimality, \(\gcd(A,B,C)=1\), rather than silently rewritten as pairwise coprimality. For actual solutions of \(A^x+B^y=C^z\), joint coprimality does imply pairwise coprimality: if a prime divides any two of \(A,B,C\), the equation forces it to divide the third. That derived lemma does not change the source wording.

## 5. Fidelity findings

1. **Complete as a standalone statement:** No. The frozen sentence omits the positive-integer domain and explicit quantifier scope.
2. **Recoverable from the cited source context:** Yes. The NT-078 background supplies the domain, and the sponsor-maintained statement independently gives the same domain and conclusion.
3. **Textually truncated relative to the NT-078 “Problem Statement” field:** No detected truncation; the frozen sentence matches that field's mathematical wording.
4. **Semantically self-contained:** No. The missing domain must be carried as an explicit source-fidelity gap.
5. **Current problem status:** NT-078 labels the problem “Open” and reports a literature review checked 2026-08-17. This is a research tracker classification, not mathematical proof that no later result exists.
6. **Attribution:** “Beal's Conjecture” is a supported common title. The audit does not assert exclusive historical priority; MathWorld records the alternative name “Tijdeman–Zagier conjecture.”
7. **Unambiguous after source expansion:** Yes, provided all six variables are positive integers and “common prime factor” is interpreted as one prime dividing all three bases.

## 6. Candidate disposition

The statement-fidelity obligation should not be treated as closed merely because this candidate is transported or merged. A trusted statement-faithfulness review should decide how to preserve both facts:

- the canonical sentence is frozen exactly as ingested;
- its intended quantified domain is supplied only by surrounding/external source context.

A versioned annotation is safer than silently altering the canonical text.

## 7. Limitations

- This audit is source comparison, not independent verification of the conjecture's open status.
- The current AMS prize page was not used as a directly retrieved primary text in this candidate; the UNT sponsor page links to the AMS rules.
- No priority-history investigation beyond the named sources was attempted.
- No proof, computation, formal kernel check, or counterexample search was performed.

## 8. Sources retrieved

- UnsolvedMath, NT-078, “Beal's Conjecture,” retrieved 2026-09-09: `https://www.unsolvedmath.com/problems/NT-078`
- R. Daniel Mauldin / University of North Texas, “The Beal Conjecture and Prize,” retrieved 2026-09-09: `https://sites.math.unt.edu/~mauldin/beal.html`
- Eric W. Weisstein, “Beal's Conjecture,” MathWorld, page marked updated 2026-09-02 and retrieved 2026-09-09: `https://mathworld.wolfram.com/BealsConjecture.html`
