# Hospital Billing and Patient Classification – Python Case Study

This solution uses only the assigned introductory Python syllabus: variables, data types, operators, conditional statements, loops, strings, lists, tuples, nested lists, tuple unpacking, algorithms, pseudocode, and flowcharts.

## 1. Problem statement

Develop a Python program to calculate a patient's hospital bill by processing consultation, diagnostic, and treatment charges. Apply concessions according to the patient's category, validate billing constraints, calculate the final amount, and classify the patient according to a payment policy.

### Billing rules used

These are sample rules for the academic case study; they are not actual hospital pricing policies.

| Item                       | Rule                                        |
| -------------------------- | ------------------------------------------- |
| Consultation               | ₹500                                        |
| Diagnostics                | ₹1,000                                      |
| Treatment                  | ₹2,000                                      |
| Senior citizen concession  | 10%                                         |
| Regular patient concession | 0%                                          |
| Billing constraint         | Charges and final bill must not be negative |
| Payment classification     | Based on the final bill                     |

Payment classification:

- Below ₹1,000: Low bill
- ₹1,000 to ₹3,000: Medium bill
- Above ₹3,000: High bill

Concessions are applied to the total bill before classification.

## 2. Algorithm

1. Start.
2. Input the patient's name, age, and patient category.
3. Input consultation, diagnostic, and treatment charges.
4. Validate that age and charges are non-negative.
5. Calculate the total bill.
6. If the patient is a senior citizen (age 60 or above), apply a 10% concession.
7. Calculate the final bill.
8. Classify the final bill as low, medium, or high.
9. Display the patient details, charges, concession, final bill, and classification.
10. Stop.

## 3. Pseudocode

```
START

INPUT patient_name
INPUT age

IF age < 0
    DISPLAY "Invalid age"
    STOP
END IF

INPUT consultation_charge
INPUT diagnostic_charge
INPUT treatment_charge

IF any charge < 0
    DISPLAY "Invalid billing amount"
    STOP
END IF

total = consultation_charge
        + diagnostic_charge
        + treatment_charge

IF age >= 60
    concession_rate = 10
ELSE
    concession_rate = 0
END IF

concession = total * concession_rate / 100
final_bill = total - concession

IF final_bill < 1000
    classification = "Low bill"
ELSE IF final_bill <= 3000
    classification = "Medium bill"
ELSE
    classification = "High bill"
END IF

DISPLAY patient details
DISPLAY total, concession, final_bill
DISPLAY classification

STOP
```

## 4. Flowchart

Start

Input patient details and charges

Validate age and charges

Calculate total bill

Age ≥ 60?

Yes

Apply 10% concession

No

No concession

Calculate final bill

Classify as low, medium, or high

Display billing report

Stop

## 5. Python source code

The following program uses basic Python constructs and includes input validation, conditional concessions, a loop for collecting charges, a list, a tuple, and tuple unpacking.

```
        )        # Calculate total bill        total = 0        for amount in charges:            total += amount        # Conditional concession        if age >= 60:            rate = 10        else:            rate = 0        concession = total * rate / 100        final_bill = total - concession        # Patient classification        if final_bill < 1000:            category = "Low bill"        elif final_bill <= 3000:            category = "Medium bill"        else:            category = "High bill"        # Tuple unpacking        consultation_name, consultation_amount, \        diagnostic_name, diagnostic_amount, \        treatment_name, treatment_amount = billing_details        # Display report        print("\n----- BILLING REPORT -----")        print("Patient Name:", name)        print("Patient Age:", age)        print(consultation_name, ": Rs.", consultation_amount)        print(diagnostic_name, ": Rs.", diagnostic_amount)        print(treatment_name, ": Rs.", treatment_amount)        print("Total Bill: Rs.", round(total, 2))        print("Concession Rate:", rate, "%")        print("Concession Amount: Rs.", round(concession, 2))        print("Final Bill: Rs.", round(final_bill, 2))        print("Patient Classification:", category)
```

## 6. Sample input

```
HOSPITAL BILLING SYSTEM
Enter patient name: Ravi
Enter patient age: 65
Enter Consultation charge: 500
Enter Diagnostics charge: 1000
Enter Treatment charge: 2000
```

## 7. Sample output

```
----- BILLING REPORT -----
Patient Name: Ravi
Patient Age: 65
Consultation : Rs. 500.0
Diagnostics : Rs. 1000.0
Treatment : Rs. 2000.0
Total Bill: Rs. 3500.0
Concession Rate: 10 %
Concession Amount: Rs. 350.0
Final Bill: Rs. 3150.0
Patient Classification: High bill
```

## 8. Mermaid flowchart code
```

    A([Start]) --> B[/Input patient name, age and charges/]
    B --> C{Age and charges valid?}
    C -- No --> D[Display invalid input]
    D --> Z([Stop])
    C -- Yes --> E[Calculate total bill]
    E --> F{Total bill greater than zero?}
    F -- No --> G[Display invalid bill]
    G --> Z
    F -- Yes --> H{Age >= 60?}
    H -- Yes --> I[Apply 10% senior concession]
    H -- No --> J[Keep bill unchanged]
    I --> K{Original total >= 5000?}
    J --> K
    K -- Yes --> L[Apply 5% concession to remaining bill]
    K -- No --> M[Keep remaining bill unchanged]
    L --> N[Calculate final payable amount]
    M --> N
    N --> O{Final bill < 2000?}
    O -- Yes --> P[Low-cost patient]
    O -- No --> Q{Final bill <= 10000?}
    Q -- Yes --> R[Standard-cost patient]
    Q -- No --> S[High-cost patient]
    P --> T[Display bill and classification]
    R --> T
    S --> T
    T --> Z
```
