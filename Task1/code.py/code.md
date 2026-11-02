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

Copy this code into a Mermaid-compatible editor to generate the flowchart.

\#chatgpt-mermaid-\_r_cr\_{font-family:-apple-system-body,ui-sans-serif,-apple-system,system-ui,"Segoe UI",Helvetica,"Apple Color Emoji",Arial,sans-serif,"Segoe UI Emoji","Segoe UI Symbol";font-size:16px;fill:rgb(237, 237, 237);}@keyframes edge-animation-frame{from{stroke-dashoffset:0;}}@keyframes dash{to{stroke-dashoffset:0;}}#chatgpt-mermaid-\_r_cr\_ .edge-animation-slow{stroke-dasharray:9,5!important;stroke-dashoffset:900;animation:dash 50s linear infinite;stroke-linecap:round;}#chatgpt-mermaid-\_r_cr\_ .edge-animation-fast{stroke-dasharray:9,5!important;stroke-dashoffset:900;animation:dash 20s linear infinite;stroke-linecap:round;}#chatgpt-mermaid-\_r_cr\_ .error-icon{fill:rgb(48, 48, 48);}#chatgpt-mermaid-\_r_cr\_ .error-text{fill:rgb(237, 237, 237);stroke:rgb(237, 237, 237);}#chatgpt-mermaid-\_r_cr\_ .edge-thickness-normal{stroke-width:1px;}#chatgpt-mermaid-\_r_cr\_ .edge-thickness-thick{stroke-width:3.5px;}#chatgpt-mermaid-\_r_cr\_ .edge-pattern-solid{stroke-dasharray:0;}#chatgpt-mermaid-\_r_cr\_ .edge-thickness-invisible{stroke-width:0;fill:none;}#chatgpt-mermaid-\_r_cr\_ .edge-pattern-dashed{stroke-dasharray:3;}#chatgpt-mermaid-\_r_cr\_ .edge-pattern-dotted{stroke-dasharray:2;}#chatgpt-mermaid-\_r_cr\_ .marker{fill:rgb(175, 175, 175);stroke:rgb(175, 175, 175);}#chatgpt-mermaid-\_r_cr\_ .marker.cross{stroke:rgb(175, 175, 175);}#chatgpt-mermaid-\_r_cr\_ svg{font-family:-apple-system-body,ui-sans-serif,-apple-system,system-ui,"Segoe UI",Helvetica,"Apple Color Emoji",Arial,sans-serif,"Segoe UI Emoji","Segoe UI Symbol";font-size:16px;}#chatgpt-mermaid-\_r_cr\_ p{margin:0;}#chatgpt-mermaid-\_r_cr\_ .label{font-family:-apple-system-body,ui-sans-serif,-apple-system,system-ui,"Segoe UI",Helvetica,"Apple Color Emoji",Arial,sans-serif,"Segoe UI Emoji","Segoe UI Symbol";color:rgb(237, 237, 237);}#chatgpt-mermaid-\_r_cr\_ .cluster-label text{fill:rgb(237, 237, 237);}#chatgpt-mermaid-\_r_cr\_ .cluster-label span{color:rgb(237, 237, 237);}#chatgpt-mermaid-\_r_cr\_ .cluster-label span p{background-color:transparent;}#chatgpt-mermaid-\_r_cr\_ .label text,#chatgpt-mermaid-\_r_cr\_ span{fill:rgb(237, 237, 237);color:rgb(237, 237, 237);}#chatgpt-mermaid-\_r_cr\_ .node rect,#chatgpt-mermaid-\_r_cr\_ .node circle,#chatgpt-mermaid-\_r_cr\_ .node ellipse,#chatgpt-mermaid-\_r_cr\_ .node polygon,#chatgpt-mermaid-\_r_cr\_ .node path{fill:rgb(9, 23, 44);stroke:rgb(31, 78, 148);stroke-width:1px;}#chatgpt-mermaid-\_r_cr\_ .rough-node .label text,#chatgpt-mermaid-\_r_cr\_ .node .label text,#chatgpt-mermaid-\_r_cr\_ .image-shape .label,#chatgpt-mermaid-\_r_cr\_ .icon-shape .label{text-anchor:middle;}#chatgpt-mermaid-\_r_cr\_ .node .katex path{fill:#000;stroke:#000;stroke-width:1px;}#chatgpt-mermaid-\_r_cr\_ .rough-node .label,#chatgpt-mermaid-\_r_cr\_ .node .label,#chatgpt-mermaid-\_r_cr\_ .image-shape .label,#chatgpt-mermaid-\_r_cr\_ .icon-shape .label{text-align:center;}#chatgpt-mermaid-\_r_cr\_ .node.clickable{cursor:pointer;}#chatgpt-mermaid-\_r_cr\_ .root .anchor path{fill:rgb(175, 175, 175)!important;stroke-width:0;stroke:rgb(175, 175, 175);}#chatgpt-mermaid-\_r_cr\_ .arrowheadPath{fill:rgb(175, 175, 175);}#chatgpt-mermaid-\_r_cr\_ .edgePath .path{stroke:rgb(175, 175, 175);stroke-width:1px;}#chatgpt-mermaid-\_r_cr\_ .flowchart-link{stroke:rgb(175, 175, 175);fill:none;}#chatgpt-mermaid-\_r_cr\_ .edgeLabel{background-color:rgb(0, 0, 0);text-align:center;}#chatgpt-mermaid-\_r_cr\_ .edgeLabel p{background-color:rgb(0, 0, 0);}#chatgpt-mermaid-\_r_cr\_ .edgeLabel rect{opacity:0.5;background-color:rgb(0, 0, 0);fill:rgb(0, 0, 0);}#chatgpt-mermaid-\_r_cr\_ .labelBkg{background-color:rgba(0, 0, 0, 0.5);}#chatgpt-mermaid-\_r_cr\_ .cluster rect{fill:rgb(48, 48, 48);stroke:rgba(255, 255, 255, 0.15);stroke-width:1px;}#chatgpt-mermaid-\_r_cr\_ .cluster text{fill:rgb(237, 237, 237);}#chatgpt-mermaid-\_r_cr\_ .cluster span{color:rgb(237, 237, 237);}#chatgpt-mermaid-\_r_cr\_ div.mermaidTooltip{position:absolute;text-align:center;max-width:200px;padding:2px;font-family:-apple-system-body,ui-sans-serif,-apple-system,system-ui,"Segoe UI",Helvetica,"Apple Color Emoji",Arial,sans-serif,"Segoe UI Emoji","Segoe UI Symbol";font-size:12px;background:rgb(48, 48, 48);border:1px solid rgba(255, 255, 255, 0.15);border-radius:2px;pointer-events:none;z-index:100;}#chatgpt-mermaid-\_r_cr\_ .flowchartTitleText{text-anchor:middle;font-size:18px;fill:rgb(237, 237, 237);}#chatgpt-mermaid-\_r_cr\_ rect.text{fill:none;stroke-width:0;}#chatgpt-mermaid-\_r_cr\_ .icon-shape,#chatgpt-mermaid-\_r_cr\_ .image-shape{background-color:rgb(0, 0, 0);text-align:center;}#chatgpt-mermaid-\_r_cr\_ .icon-shape p,#chatgpt-mermaid-\_r_cr\_ .image-shape p{background-color:rgb(0, 0, 0);padding:2px;}#chatgpt-mermaid-\_r_cr\_ .icon-shape .label rect,#chatgpt-mermaid-\_r_cr\_ .image-shape .label rect{opacity:0.5;background-color:rgb(0, 0, 0);fill:rgb(0, 0, 0);}#chatgpt-mermaid-\_r_cr\_ .label-icon{display:inline-block;height:1em;overflow:visible;vertical-align:-0.125em;}#chatgpt-mermaid-\_r_cr\_ .node .label-icon path{fill:currentColor;stroke:revert;stroke-width:revert;}#chatgpt-mermaid-\_r_cr\_ .node .neo-node{stroke:rgb(31, 78, 148);}#chatgpt-mermaid-\_r_cr\_ [data-look="neo"].node rect,#chatgpt-mermaid-\_r_cr\_ [data-look="neo"].cluster rect,#chatgpt-mermaid-\_r_cr\_ [data-look="neo"].node polygon{stroke:url(#chatgpt-mermaid-\_r_cr\_-gradient);filter:drop-shadow( 1px 2px 2px rgba(185,185,185,1));}#chatgpt-mermaid-\_r_cr\_ [data-look="neo"].swimlane.cluster rect{filter:none;}#chatgpt-mermaid-\_r_cr\_ [data-look="neo"].node path{stroke:url(#chatgpt-mermaid-\_r_cr\_-gradient);stroke-width:1px;}#chatgpt-mermaid-\_r_cr\_ [data-look="neo"].node .outer-path{filter:drop-shadow( 1px 2px 2px rgba(185,185,185,1));}#chatgpt-mermaid-\_r_cr\_ [data-look="neo"].node .neo-line path{stroke:rgb(31, 78, 148);filter:none;}#chatgpt-mermaid-\_r_cr\_ [data-look="neo"].node circle{stroke:url(#chatgpt-mermaid-\_r_cr\_-gradient);filter:drop-shadow( 1px 2px 2px rgba(185,185,185,1));}#chatgpt-mermaid-\_r_cr\_ [data-look="neo"].node circle .state-start{fill:#000000;}#chatgpt-mermaid-\_r_cr\_ [data-look="neo"].icon-shape .icon{fill:url(#chatgpt-mermaid-\_r_cr\_-gradient);filter:drop-shadow( 1px 2px 2px rgba(185,185,185,1));}#chatgpt-mermaid-\_r_cr\_ [data-look="neo"].icon-shape .icon-neo path{stroke:url(#chatgpt-mermaid-\_r_cr\_-gradient);filter:drop-shadow( 1px 2px 2px rgba(185,185,185,1));}#chatgpt-mermaid-\_r_cr\_ .node text{font-size:14px;font-weight:600;letter-spacing:normal;fill:rgb(153, 206, 255);}#chatgpt-mermaid-\_r_cr\_ .edgeLabels text{font-size:13px;font-weight:600;letter-spacing:-0.08px;fill:rgb(153, 206, 255);}#chatgpt-mermaid-\_r_cr\_ .node tspan[font-weight="normal"],#chatgpt-mermaid-\_r_cr\_ .edgeLabels tspan[font-weight="normal"]{font-weight:600;}#chatgpt-mermaid-\_r_cr\_ .edgeLabel .label rect{opacity:1;rx:13px;ry:13px;fill:rgb(0, 14, 26);stroke:rgb(26, 62, 95);stroke-width:1px;}#chatgpt-mermaid-\_r_cr\_ .node rect,#chatgpt-mermaid-\_r_cr\_ .node circle,#chatgpt-mermaid-\_r_cr\_ .node ellipse,#chatgpt-mermaid-\_r_cr\_ .node polygon,#chatgpt-mermaid-\_r_cr\_ .node path{fill:rgb(0, 40, 77);stroke:rgba(255, 255, 255, 0.1);stroke-width:1px;}#chatgpt-mermaid-\_r_cr\_ .node rect{rx:16px;ry:16px;}#chatgpt-mermaid-\_r_cr\_ .mermaid-decision .label-container{fill:rgb(0, 14, 26);stroke:rgb(26, 62, 95);stroke-dasharray:2,2;}#chatgpt-mermaid-\_r_cr\_ .edgePaths .flowchart-link{stroke:rgb(175, 175, 175);stroke-width:1px;stroke-linecap:round;stroke-linejoin:round;}#chatgpt-mermaid-\_r_cr\_ .marker{fill:rgb(175, 175, 175);stroke:rgb(175, 175, 175);}#chatgpt-mermaid-\_r_cr\_ :root{--mermaid-font-family:-apple-system-body,ui-sans-serif,-apple-system,system-ui,"Segoe UI",Helvetica,"Apple Color Emoji",Arial,sans-serif,"Segoe UI Emoji","Segoe UI Symbol";}StartInput patient name, age andchargesAge and charges valid?Display invalid inputStopCalculate total billTotal bill greater than zero?Display invalid billAge = 60?Apply 10% senior concessionKeep bill unchangedOriginal total = 5000?Apply 5% concession toremaining billKeep remaining bill unchangedCalculate final payable amountFinal bill < 2000?Low-cost patientFinal bill <= 10000?Standard-cost patientHigh-cost patientDisplay bill and classificationNoYesNoYesYesNoYesNoYesNoYesNo
