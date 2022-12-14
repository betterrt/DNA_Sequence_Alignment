# DNA-Sequence-Alignment

## Objective

The program will find the similarity between two DNA sequences, which is described by the cost of the alignment. What's more, the program can also find the alignments of two DNA sequences, the time used and the memory used.

## Definition of Alignment

Suppose we are given two strings π and π, where π consists of the sequence of symbols π₯1, π₯2 , ... , π₯π and π consists of the sequence of symbols π¦1, π¦2 , ... , π¦π.
Consider the sets {1, 2, ... , π} and {1, 2, ... , π} as representing the different positions in the strings π and π, and consider a matching of these sets. We say that a matching π of these two sets is an alignment if there are no βcrossingβ pairs:if (π, π), (π', π') Ο΅ π and π < π', then π < π'. Intuitively, an alignment gives a way of lining up the two strings, by telling us which pairs of positions will be lined up with one another.

## Definition of Similarity

The definition of similarity will be based on finding the optimal alignment between two DNA sequences π and π, according to the following criteria. Suppose π is a given alignment between π and π:
1. First, there is a parameter Ξ΄ > 0 that defines a gap penalty. For each position of π or π that is not matched in π( i.e. it is a gap), we incur a cost of Ξ΄.
2. Second, for each pair of letters π, π in our alphabet, there is a mismatch cost of Ξ±ππ for lining up π with π. Thus, for each (π, π) Ο΅ π, we pay the appropriate mismatch cost Ξ±π₯ππ¦π for lining up π₯π with π¦π. assumes that = 0 for each letter βthere is no mismatch cost to line up Ξ±ππ π a letter with another copy of itselfβalthough this will not be necessary in anything that follows.
3. The cost of π is the sum of its gap and mismatch costs, and we seek an alignment of minimum cost, which descirbe the similaity of these two DNA sequences.

Example: Say we have first DNA sequence "AGCT" and second DNA sequence "AGT". The best aligment will be "AGCT" and "AG_T" where "_" means a gap.

## Basic and Efficient Method

The basic method is to use DP, which have a quadratic time complexity and space complexity.

The efficient method is to combine DP and D&C, which has also a quadratic time complexoty but a linear space complexity.
