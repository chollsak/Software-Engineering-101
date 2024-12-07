# Requirements Notes

## Requirements Definition
Requirements define the problem at hand. In this step, we are trying to find out the **"what"**, not the **"how"**. This phase focuses on establishing goals for the system without determining how to achieve them.

### Example
Suppose we need a form to track financial transactions:
- Define what the form should track: name, date, amount, bank account.
- Specify that the data needs to be stored in a database.

These are requirements. However, deciding the best way to achieve these goals belongs to the design phase.

### Key Point
Requirements are used to define the problem and create a shared understanding of goals. Throughout the production process, requirements are revisited to ensure the product solves the original problem.

---

## Requirements vs Specifications

### Definitions
- **Requirements**: A non-technical definition of what the system should do.
- **Specifications**: A technical definition of the constraints or standards the system must meet.

### Example
- **Requirement**: "Should record bank account information."
- **Specification**: "Encrypt the bank account information with at least an AES 256 standard."

Specifications define technical standards but do not determine how to meet them—that happens in the design phase.

---

## Non-Functional vs Functional Requirements

### Functional Requirements
These pertain to the **functionality** of the system. Ask: "What should the program do?"

#### Examples
- The system should collect user information.
- The system should provide a cart system for collecting items.
- The system should allow users to rate and review products.

### Non-Functional Requirements
These cover areas that don't directly affect the program's functionality, often constraints from regulations, company policies, or client requirements.

#### Examples
- The program must be coded in Java.
- The product must use SSL due to European law XYZ.

---

### Categories of Non-Functional Requirements

1. **Product**
   - Defines the behavior of the product (code, servers, etc.).
   - Example: Product must be coded in Java; Product must use Microsoft-based servers.

2. **Organizational**
   - Includes company policies, standards, styles, and rules.
   - Example: The project will follow Scrum methodology; Every function must be documented.

3. **External**
   - Encompasses external laws, regulations, or trends.
   - Example: Product must use SSL due to law XYZ; Product should adopt new technique XYZ for data collection.
