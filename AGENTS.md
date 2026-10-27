# Tiny Shop Checkout working guidance

## Purpose and scope

- This directory is a small Python checkout teaching project used to compare work with and without project instructions.
- This guidance applies to this directory and its descendants. Implementation lives in `src/checkout.py`, tests in `tests/test_checkout.py`, and synthetic example data in `sample_orders.json`.
- Read the relevant source, tests, README, and task card before making a requested change. Task cards describe exercises; do not implement them unless requested.
- Keep changes within the requested task. For this drafting task, do not modify application code or tests.

## Current public contract

- The public function is `calculate_total(items)`, imported as `from src.checkout import calculate_total`.
- Items are documented as a sequence of mappings with `name`, `price`, and `quantity`. The implementation reads only `price` and `quantity`, summing `float(item["price"]) * int(item["quantity"])`.
- Return a float, including `0.0` for an empty cart. Floats are intentional for this teaching exercise; preserve that contract when extending the function.
- The current function has no explicit input validation, rounding, or exception handling. Do not describe additional validation or error guarantees as existing behavior.
- Discount support and `format_total(total)` are future task-card exercises, not implemented interfaces. When Task B is requested, keep formatting separate from calculation as specified there.

## Working rules

- Follow the existing four-space indentation, snake_case function/test names, and standard-library `unittest` style.
- No package installation is currently required. Task A explicitly prohibits adding dependencies or changing the item schema; apply those restrictions when doing Task A.
- For requested checkout changes, add focused tests, including relevant boundary cases, and update documentation when public behavior changes.
- Report assumptions, changed files, verification commands and actual results, and any unrelated changes found during diff review. Do not claim checks passed unless they were run.

## Verification

Run the documented check from `learner/starter/` (the directory containing this file):

```sh
python3 -m unittest discover -s tests -v
```

- No install, application launch, lint, or build command is documented for the checkout project. Do not invent one.
- If the documented command cannot run in the environment, report the failure and any proposed alternative explicitly; do not report an unexecuted alternative as verified.

## Ambiguity handling

- Distinguish current implementation and tests from future exercise requirements. Identify conflicting evidence before changing a public contract.
- For a material ambiguity about expected behavior or scope, ask a focused question before making the dependent change. State minor assumptions explicitly.
- The integration template has no selected SDK, pinned version, or completed contract. Obtain the missing specification before implementing an integration; do not invent dependencies, architecture, or company policies.
