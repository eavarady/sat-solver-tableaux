# SAT Solver using Tableaux Method

This project implements a SAT solver for propositional logic using the Tableaux method. It provides a systematic approach to determine whether a given formula is satisfiable (SAT) or unsatisfiable (UNSAT).

## Features
- **Formula Representation**: Supports constants, propositions, negations, conjunctions, disjunctions, implications, and equivalences.
- **Conversion to NNF**: Rewrites formulas into Negation Normal Form.
- **Simplification**: Simplifies formulas by applying rules like constant propagation, duplicate elimination, and complementary literal detection.
- **Tableaux Expansion**: Expands branches using AND and OR rules.
- **Satisfiability Check**: Determines if a formula is SAT or UNSAT.

## How It Works
1. **Define a Formula**: Use the `Formula` data type to represent logical formulas.
2. **Convert to NNF**: Use the `toNNF` function to rewrite the formula in Negation Normal Form.
3. **Simplify**: Apply the `simplify` function to reduce the formula.
4. **Expand Tableaux**: Use the `expand` function to systematically expand the tableaux.
5. **Check SAT**: Use the `checkSAT` function to determine satisfiability.

## Example
```haskell
-- Define a formula
let formula = And [Prop "P", Not (Prop "P")]

-- Check satisfiability
checkSAT formula
-- Output: "UNSAT"
