# Hospital Billing and Patient Classification – Python Case Study

## 1. Problem Statement

Develop a Python program to calculate a patient's hospital bill by processing consultation, diagnostic, and treatment charges. Apply concessions based on patient category, validate billing constraints, and classify patients according to the payment policy.

Assumed payment policy for this case study:

- Senior citizens aged 60 or above receive a 10% concession.
- Patients with a total bill of ₹5,000 or more receive a 5% concession.
- Concessions are applied successively: the senior citizen concession first, followed by the bill-based concession.
- Charges must be non-negative, and the total bill must be greater than zero.
- Patients are classified by final payable amount:
  - Below ₹2,000: Low-cost patient
  - ₹2,000–₹10,000: Standard-cost patient
  - Above ₹10,000: High-cost patient

Note: These are sample rules for an academic case study, not actual hospital billing regulations.

## 2. Algorithm

1. Start.
2. Read the patient's name and age.
3. Read consultation, diagnostic, and treatment charges.
4. Check whether age and charges are valid.
5. Calculate the total bill by adding all three charges.
6. If the total bill is zero, display an invalid bill message and stop.
7. If the patient is aged 60 or above, apply a 10% concession.
8. If the original total bill is ₹5,000 or more, apply an additional 5% concession to the remaining amount.
9. Calculate the final payable amount.
10. Classify the patient based on the final payable amount.
11. Display the bill details, concessions, final amount, and patient classification.
12. Stop.



## 5. Sample Input

```
Enter patient name: Ravi
Enter patient age: 65
Enter consultation charges: 1000
Enter diagnostic charges: 3000
Enter treatment charges: 2000
```

## 6. Sample Output

```
--- Hospital Bill ---
Patient Name: Ravi
Patient Age: 65
Total Charges: Rs. 6000.00
Total Concession: Rs. 840.00
Final Payable: Rs. 5160.00
Patient Classification: Standard-cost patient
```

### Calculation

- Total charges = ₹1,000 + ₹3,000 + ₹2,000 = ₹6,000
- Senior citizen concession = 10% of ₹6,000 = ₹600
- Remaining bill = ₹6,000 − ₹600 = ₹5,400
- Bill-based concession = 5% of ₹5,400 = ₹270
- Total concession = ₹600 + ₹270 = ₹870
- Final payable = ₹6,000 − ₹870 = ₹5,130

Correction to the sample output above: The correct total concession is ₹870.00, the final payable is ₹5,130.00, and the patient classification remains Standard-cost patient.

## 7. Mermaid Flowchart Code
'''mermaid
flowchart TD
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
    '''

