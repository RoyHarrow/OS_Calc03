## Why

Users want to enter formulas directly as text (e.g., "4+5=") rather than using button clicks. This provides a more natural input method for simple calculations and aligns with how users typically write mathematical expressions.

## What Changes

- Add a text input field for formula entry
- Parse formula strings containing two operands and one operator
- Support basic operators: + (add), - (subtract), / (divide), * (multiply)
- Make the = sign optional at the end of the formula
- Display the calculated result

## Capabilities

### New Capabilities

- **formula-input**: Allow users to enter simple mathematical formulas as text (e.g., "4+5=" or "4+5") and receive the calculated result

### Modified Capabilities

- (none - new capability)

## Impact

- Modify existing calculator HTML to add text input option
- Add JavaScript parsing logic for formula strings
- No new dependencies or external systems