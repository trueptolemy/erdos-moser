# The Erdős–Moser equation - Unproven

**First draft.**

The Erdős–Moser equation is $1^k + 2^k + \cdots + (m-1)^k = m^k$ for integers $k \ge 1$ and $m \ge 2$. The only known solution is $(k,m)=(1,3)$. Moser ruled out solutions for odd $k \ge 3$.

- [Research manuscript (PDF)](erdos-moser-proof.pdf)
- [LaTeX source](erdos-moser-proof.tex)
- [Lean 4 source](erdos-moser-full.lean)

## Proof status

The manuscript revisits the odd-exponent case using $2$-adic valuations. For even exponents, it studies the boundary cases, a convexity argument for large $m$, and alternating-series and von Staudt–Clausen arguments for the intermediate range.

The degree-10 polynomial argument leaves a gap. At a hypothetical solution with $k \ge 12$, the higher-order Bernoulli terms can cancel the truncated expression. The finite rational-root check concerns a fixed polynomial, and the step from the full Faulhaber equation to that polynomial still needs a proof. [Manuscript §7.5](erdos-moser-proof.tex#L2269)

The Lean source imports Mathlib and contains two `sorry` placeholders. They occur in the large-$m$ argument for $k > 1{,}000$ and the alternating-series argument for $k > 10{,}000$. [Large-$m$ proof](erdos-moser-full.lean#L2445) · [Alternating-series proof](erdos-moser-full.lean#L2925)

## Build the PDF

Run `pdflatex -halt-on-error erdos-moser-proof.tex` twice from the repository root to resolve cross-references.
