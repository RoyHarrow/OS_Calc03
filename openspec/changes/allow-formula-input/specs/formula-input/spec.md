## ADDED Requirements

### Requirement: Formula text input field
The calculator SHALL provide a text input field where users can type mathematical formulas.

#### Scenario: Input field is visible
- **WHEN** user views the calculator page
- **THEN** a text input field is displayed above the calculator buttons

### Requirement: Parse addition formula
The calculator SHALL parse and evaluate formulas with the + operator.

#### Scenario: Formula with equals sign
- **WHEN** user enters "4+5=" in the text input and presses Enter
- **THEN** the display shows "9"

#### Scenario: Formula without equals sign
- **WHEN** user enters "4+5" in the text input and presses Enter
- **THEN** the display shows "9"

### Requirement: Parse subtraction formula
The calculator SHALL parse and evaluate formulas with the - operator.

#### Scenario: Subtraction formula
- **WHEN** user enters "10-3=" in the text input and presses Enter
- **THEN** the display shows "7"

#### Scenario: Negative result
- **WHEN** user enters "3-8=" in the text input and presses Enter
- **THEN** the display shows "-5"

### Requirement: Parse multiplication formula
The calculator SHALL parse and evaluate formulas with the * operator.

#### Scenario: Multiplication formula
- **WHEN** user enters "4*5=" in the text input and presses Enter
- **THEN** the display shows "20"

### Requirement: Parse division formula
The calculator SHALL parse and evaluate formulas with the / operator.

#### Scenario: Division formula
- **WHEN** user enters "20/4=" in the text input and presses Enter
- **THEN** the display shows "5"

### Requirement: Handle division by zero
The calculator SHALL display an error when dividing by zero.

#### Scenario: Division by zero
- **WHEN** user enters "5/0=" in the text input and presses Enter
- **THEN** the display shows "Error"

### Requirement: Reject invalid formulas
The calculator SHALL display an error for invalid formula input.

#### Scenario: Non-numeric input
- **WHEN** user enters "abc" in the text input and presses Enter
- **THEN** the display shows "Error"

#### Scenario: Multiple operators
- **WHEN** user enters "4+5+3=" in the text input and presses Enter
- **THEN** the display shows "Error" (more than 2 operands)

#### Scenario: No operator
- **WHEN** user enters "123" in the text input and presses Enter
- **THEN** the display shows "Error" (no operator found)

### Requirement: Limit to basic operators
The calculator SHALL only accept +, -, /, * operators.

#### Scenario: Unsupported operator
- **WHEN** user enters "4%2=" in the text input and presses Enter
- **THEN** the display shows "Error"