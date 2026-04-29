## Context

Add formula text input to the existing simple calculator. Users can now type formulas like "4+5=" or "4+5" directly into a text field and get the result.

**Current State:** Calculator at `simple-calculator/index.html` has button-based input only.

**Constraints:**
- Must work with existing button-based calculator (not replace it)
- Limit to 2 operands, 1 operator (as per requirements)
- Only support +, -, /, * operators
- = sign is optional

**Stakeholders:** Users who prefer typing over clicking buttons.

## Goals / Non-Goals

**Goals:**
- Add text input field above the calculator display
- Parse formula strings with regex: `number operator number [=]`
- Display result in the same display area
- Handle optional trailing = sign

**Non-Goals:**
- Support more than 2 operands (chained formulas)
- Support other operators (%, ^, etc.)
- Scientific calculator functions
- Formula history

## Decisions

| Decision | Rationale | Alternatives Considered |
|-----------|-----------|------------------------|
| Add input field above display | Keeps existing button UI intact | Replace button UI entirely |
| Use regex for parsing | Simple, fast parsing for 2-operand formulas | Parser library (overkill) |
| Display in same display area | Consistent UX | Separate result area |
| Optional = sign | User explicitly requested it | Require = sign |

## Risks / Trade-offs

- [Risk] Invalid input (letters, multiple operators) → **Mitigation**: Show "Error" for unparseable input
- [Risk] Division by zero → **Mitigation**: Show "Error" message
- [Risk] Very long numbers → **Mitigation**: Limit input to 15 characters