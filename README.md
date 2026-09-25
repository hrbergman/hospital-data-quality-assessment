### Data Quality Assessment & Remediation - Hospital Patient Records
**Tools: Python, pandas, NumPy, Matplotlib, Plotly, scikit-learn** | M.S. Data Analytics Project (D206 - Data Cleaning)

Before any analysis could be trusted, this 10,000-patient, 52-variable hospital dataset needed a full audit. I profiled every field against the organization's data dictionary, documented what was wrong and why it mattered, and designed a remediation plan that balanced data completeness against the risk of introducing false information.
 
- Built a two-level profiling approach: a dataset-wide scan for structure, counts, and types, followed by a column-by-column review for duplicates, nulls, cardinality, and value ranges
- Uncovered schema problems that would have silently skewed analysis, including charge fields labeled as totals that actually stored daily averages, a "State" field containing non-state regions, and 26 time zone values where only 7 US time zones exist
- Chose field-specific handling for missing values based on business meaning, leaving sensitive health indicators blank rather than imputing them so gaps stayed visible for follow-up
- Proposed standardized naming conventions and clearer field definitions, including renaming ambiguous demographic fields to reflect that they may describe the insurance policyholder rather than the patient
- Applied Principal Component Analysis to the cleaned quantitative variables and retained six components using eigenvalue and scree plot criteria

[Documentation](https://github.com/hrbergman/postgresql-customer-services-query/blob/main/postgresql-customer-services-query/data-acquisition-documentation.pdf)
| 
[Video Presentation](https://youtu.be/jKOE0cG68rc)
