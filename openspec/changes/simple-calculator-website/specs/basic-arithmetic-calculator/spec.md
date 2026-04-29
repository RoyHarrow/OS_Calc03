## ADDED Requirements

### Requirement: Calculator displays numeric input
The calculator SHALL display the current numeric input in a display area. The display SHALL show up to 15 digits and handle decimal points.

#### Scenario: Display shows digit input
- **WHEN** user clicks a digit button (0-9)
- **THEN** the digit is appended to the current input in the display

#### Scenario: Display shows decimal input
- **WHEN** user clicks the decimal point button
- **THEN** a decimal point is added to the current number (only one decimal allowed per number)

#### Scenario: Display clears on clear button
- **WHEN** user clicks the "C" (clear) button
- **THEN** the display shows "0" and resets the calculator state

### Requirement: Calculator performs addition
The calculator SHALL add two numbers when the "+" operator is pressed followed by "=".

#### Scenario: Add two positive numbers
- **WHEN** user enters "5 + 3 =" 
- **THEN** the display shows "8"

#### Scenario: Add with existing result
- **WHEN** user clicks "=" and then enters "+ 2 ="
- **THEN** the display shows the previous result plus 2

### Requirement: Calculator performs subtraction
The calculator SHALL subtract the second number from the first when the "-" operator is pressed followed by "=".

#### Scenario: Subtract two numbers
- **WHEN** user enters "10 - 4 ="
- **THEN** the display shows "6"

#### Scenario: Subtract resulting in negative
- **WHEN** user enters "3 - 8 ="
- **THEN** the display shows "-5"

### Requirement: Calculator performs multiplication
The calculator SHALL multiply two numbers when the "×" operator is pressed followed by "=".

#### Scenario: Multiply two numbers
- **WHEN** user enters "6 × 4 ="
- **THEN** the display shows "24"

#### Scenario: Multiply by zero
- **WHEN** user enters "5 × 0 ="
- **THEN** the display shows "0"

### Requirement: Calculator performs division
The calculator SHALL divide the first number by the second when the "÷" operator is pressed followed by "=".

#### Scenario: Divide two numbers
- **WHEN** user enters "20 ÷ 4 ="
- **THEN** the display shows "5"

#### Scenario: Division by zero shows error
- **WHEN** user enters "5 ÷ 0 ="
- **THEN** the display shows "Error" and calculator resets

### Requirement: Calculator handles chained operations
The calculator SHALL allow multiple operations to be chained, with each "=" computing the most recent operation.

#### Scenario: Chain multiple operations
- **WHEN** user enters "2 + 3 × 2 ="
- **THEN** the display shows "10" (performs 3 × 2 = 6, then 2 + 6 = 8... actually standard calculators do 2 + 3 = 5, then 5 × 2 = 10)

### Requirement: Calculator UI is responsive
The calculator SHALL display properly on both desktop and mobile devices with touch-friendly button sizes.

#### Scenario: Calculator fits mobile screen
- **WHEN** calculator is viewed on a 375px wide mobile screen
- **THEN** all buttons are visible without horizontal scrolling

#### Scenario: Calculator fits desktop screen
- **WHEN** calculator is viewed on a 1920px wide desktop screen
- **THEN** calculator is centered with appropriate sizing