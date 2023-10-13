# DNA Alignment
A project for COMP1051.

## Problem Statement
Given two DNA sequences $X=x_1x_2\dots x_n$ and $Y=y_1y_2\dots y_m$, an alignment is an addition of gaps between letters in order to line up letters from $X$ with letters from $Y$. There are penalties for adding gaps ($P_g$) and mismatching letters ($P_m$). The solution should find a way to create an alignment such that the total penality is minimised.

## Problem Details

### Scoring Scheme
We require a _scoring scheme_ to use to know how good an alignment is. The following data will be used.
| Event | Score | Notes |
| -- | -- | -- |
| Match | +5 | When a character in $X$ is aligned with an identical character in $Y$ |
| Mismatch | -4 | When a character in $X$ is aligned with a different character in $Y$ |
| Gap | -6 | When a character in $X$ is aligned with a gap character in $Y$ |

This means the total score of an alignment can be calculated by looking at each pair of aligned characters. For example, if $X=\texttt{AGCTA}$ and $Y=\texttt{ACTGA}$, then we can make the following alignment

| $\texttt{AGCT-A}$ |
| -- |
| $\texttt{A-CTGA}$ |

which has a score of $5 - 6 + 5 + 5 - 6 + 5 = 8$.
