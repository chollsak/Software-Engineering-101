Let's go over an example of building some requirements for a project. This will help reinforce the points, and allow you to practice the skills you have learned.

We are designing software for a vending machine. If you are unfamiliar with what this is, check this link. This vending machine will be selling different types of sodas. It will accept payment in the form of either cash, or credit/debit card. We enter in the money, type in the appropriate number, and then the vending machine gives us the item.

From this idea, let's design the requirements for this project.

Questions for this assignment
Scenario: 

We are designing software for a vending machine. If you are unfamiliar with what this is, check this link. This vending machine will be selling different types of sodas. It will accept payment in the form of either cash, or credit/debit card. We enter in the money, type in the appropriate number, and then the vending machine gives us the item.

What are the World Assumptions that need to be made for this system?

What are the Requirements needed for this system? (Feel free to be creative here. The idea was very vague and open to interpretation.)

What are the Specifications needed for this system? (Do a bit of research on the software of vending machines.)


```
1. Scenario: 
    We are designing software for a vending machine. If you are unfamiliar with what this is, check this link. This vending machine will be selling different types of sodas. It will accept payment in the form of either cash, or credit/debit card. We enter in the money, type in the appropriate number, and then the vending machine gives us the item.

    What are the World Assumptions that need to be made for this system?
------------------------------------------------------
Answer: World assumptions are the conditions assumed to be true in the real world for the system to function as expected. For the vending machine:

User Interaction: Users know how to interact with the vending machine (e.g., input money, press buttons).
Users will select a valid soda option from the menu.

Hardware: The vending machine hardware (dispensing mechanism, cash/card reader, etc.) is functional and reliable.
The machine is located in an area with stable electricity.

Products: The vending machine is regularly restocked with sodas.
All products in the machine are not expired and are consumable.

Payment: Cash and card payments are processed securely.
Users input the correct amount (or card information) before a product is dispensed.

External Factors: The environment does not damage the machine (e.g., vandalism, extreme weather).
```

```
2. What are the Requirements needed for this system? (Feel free to be creative here. The idea was very vague and open to interpretation.)
---------------------------------
Answer: 

Functional Requirements

1. Product Display: Display available sodas, prices, and stock levels on a digital screen.
Show unavailable items as "Out of Stock."

2. Payment Processing: Accept cash (coins and bills).
Support credit/debit card payments via a card reader.
Provide a receipt (physical or digital).

3. User Interface: Provide a clear keypad or touchscreen for soda selection.
Show real-time feedback during user interactions (e.g., "Insert Payment," "Processing," "Dispensing Item").

4. Product Dispensing: Dispense the correct soda after successful payment.
Alert the user if the product cannot be dispensed.

5. Refund Mechanism: Allow users to cancel their transaction and retrieve their money (cash) before product selection.

Non-Functional Requirements

1. Usability: Ensure the interface is easy to use and accessible for all users, including those with disabilities.

2. Performance: Complete transactions within 10 seconds after payment.

3. Security:Encrypt card payment information.
Prevent unauthorized access to the machine.

4. Reliability: Operate continuously without errors for at least 30 days before requiring maintenance.
```

```
3. What are the Specifications needed for this system? (Do a bit of research on the software of vending machines.)

Hardware Specifications
1. Payment System: 
    1.1. Cash validator: Accepts coins (e.g., $0.05, $0.10, $0.25) and bills (e.g., $1, $5).
    1.2. Card reader: EMV chip and NFC (contactless payment) support.

2. Display:
    2.1. A touchscreen or LED display with a minimum resolution of 800x480.
    2.2. Brightness of at least 300 nits for outdoor visibility.

3. Product Storage and Dispensing:
    3.1. Capacity for 10 soda varieties, each with up to 20 units.
    3.2. Motorized spiral or robotic arm for dispensing.

4. Physical Design:
    4.1. Durable, tamper-proof casing.
    4.2. Dimensions: 72” x 36” x 30” (H x W x D).

Software Specifications
1. User Interface:
    1.1. Interactive menu for product selection and payment.
    1.2. Real-time stock updates for each product.

2. Payment System:
    2.1. Integrate with a payment gateway for card transactions.
    2.2. Provide change (cash) for overpayment.

3. Error Handling:
    3.1. Notify users of issues (e.g., "Insufficient Funds," "Out of Stock").
    3.2. Log errors for maintenance teams (e.g., jammed dispenser, card reader failure).

4. Inventory Management:
    4.1. Automatically track stock levels.
    4.2. Alert operators when stock is low.

5. Maintenance and Diagnostics:
    5.1. Remote monitoring via a connected dashboard.
    5.2. Self-diagnostic features to detect hardware failures.

6. Security:
    6.1. Secure boot for the machine's operating system.
    6.2. Automatic lock if tampering is detected.

7. Software Platform:
    7.1. Linux-based operating system for reliability.
    7.2. Software written in a high-level language like Python or Java for flexibility.

```



---

# Vending Machine Software Design

## **Scenario**
We are designing software for a vending machine that sells different types of sodas. This vending machine will accept payment in the form of either cash or credit/debit card. Users will insert payment, type the appropriate number for their selection, and the vending machine will dispense the chosen item.

---

## **World Assumptions**
These are the assumptions about the real-world environment in which the vending machine operates:

1. There will be a machine that houses the system.
2. There will be hardware set up to accept payments (cash and cards).
3. There will be hardware set up to stock and dispense goods.
4. The machine will have a constant electricity supply.
5. The machine will have an internet connection at all times.
6. There exists a currency or common form of payment that the machine will accept.
7. A plan will exist to restock the items within the machine regularly.
8. The machine will have a secure place to store cash and coins.
9. The machine will include a display and a numeric keypad or touchscreen for user input.

---

## **System Requirements**
These are the requirements for the vending machine system:

1. The system will accept and process cash payments from customers.
2. The system will accept and process card payments from customers.
3. The system will only dispense items after payment approval.
4. The system will allow customers to select a slot/item number after payment approval and dispense the corresponding item.
5. The system will keep track of inventory within the machine.
6. The system will alert the restocking team when a stocked item runs out.
7. The system will track all coins and dollar bills stored inside the machine.
8. The system will manage refunds for customers in case of overpayment or service cancellation.
9. The system will send card payment data to a central processing server.
10. The system will lock itself if it detects tilting or tampering.
11. The system will provide an interface for configuring item prices.

---

## **System Specifications**
These are the technical specifications required for the vending machine system:

1. Transactions must not take longer than **3000ms (3 seconds)** to complete.
2. Card payments will be processed by the **Stripe server**.
3. The system will update the stocking status of the machine by contacting a **local stock server**.
4. The machine will include a **cash validator** capable of accepting:
   - Coins: $0.05, $0.10, $0.25
   - Bills: $1, $5
5. The machine will support a **card reader** with:
   - EMV chip and NFC (contactless payment) support.
6. The machine will include a display with:
   - **Minimum resolution**: 800x480
   - **Brightness**: At least 300 nits for outdoor visibility.
7. The machine will have a **storage and dispensing system**:
   - Capacity for **10 soda varieties**, each with up to **20 units**.
   - Motorized spiral or robotic arm for item dispensing.
8. The machine will have a **durable, tamper-proof casing** with dimensions:
   - **72” x 36” x 30” (H x W x D)**.

---

## **Key Notes**
- This document outlines the assumptions, requirements, and specifications necessary for designing a vending machine system.
- Differences in ideas and interpretations between team members can help refine the solution, emphasizing the importance of collaboration in designing the final system.

---
