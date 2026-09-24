# Lab 04 - SOP/POS and KMaps

## By: Zachary Coltrin and Michael Rangel
## Group 19

In this lab, you’ve learned how to apply KMaps, Sum Of Products and Products of
sums to simplify digital logic equations. Then, you’ve proven out that they work
using an implemented design on your Basys3 boards.

## Rubric

| Item | Description | Value |
| ---- | ----------- | ----- |
| Summary Answers | Your writings about what you learned in this lab. | 25% |
| Question 1 | Your answers to the question | 25% |
| Question 2 | Your answers to the question | 25% |
| Question 3 | Your answers to the question | 25% |

## Lab Summary

In this lab we learned how to use SOP AND POS kmaps to generate Vivado Code and light up LED's on the BAYSYS3 board. We also did a naive version that was an unoptimized version of our truth table.

## Lab Questions

### Why are the groups of 1’s (or 0’s) that we select in the KMap able to go across edges?

In our POS table, we do this to a group of 2 0s. We are able to do this because B=0 in both cases, which are on the opposite sides of the table. Another way to visualize this is that any square can be warped into a donut/torus, to make it 3 dimensional. 

### Why are the names Sum of Products and Products of Sums?

SOP AND POS are named that way because Sum of Products OR statements to connect groups of AND operators. The Product of Sums use Products to connect groups of OR operators. 

### Open the test.v file – how are we able to check that the signals match using XOR?

The test cases match all 3 lights together for each case. Light 0 is naive, light 1 is minterm and light 2 is maxterm. It checks the naive solution against the minterm and maxterm (in separate if cases) to see if they are both off. If either is, it tells us which case we failed. If it isn't it exits with all testcases pass.
