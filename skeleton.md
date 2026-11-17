Automating Elementary Number-theoretic Proofs using Grobner Bases

# Title slide

Tomaz Mascarenhas

Original work by John Harrison (smaller)

# Introduction

## Motivation
Cancellation example (Harrison's paper: ax === ay (mod n), coprime(a, n) -> x === y (mod n))

  - formal verification of software involving these operators
  - translation of bitvector problems with symbolic length
  - Harrison's original motivation: proving number theoretic goals in proof assistants

## State of existing methods
  - Encoding with fresh variables (which also happens in Harrison's method)
  - Incremental linearization
  - CAD with branch and bound (?)
  - Nothing really specialized to this kind of constraints

## Harrison's Method
  - An incomplete test based on ideal membership
  - Complete for properties that hold over any commutative ring
  - Implemented in HOL/Light

# Description of the Method

## Encoding the operators with fresh variables

## Normal form with quantifiers

## Ideal membership test

## Sound but incomplete
  - Example x^2 + x

## Completeness Result

# ? Review of the paper ?

# Integration in cvc5
  - As a step in the incremental linearization pipeline - after easy lemmas (zero, sign) and beofre hard ones (tangent plane, coverings)
  - In SMT it is not the case that the goal will be in the form expected by the method - we thus just idenitfy divisions and use it to generate lemmas about the respective remainders
