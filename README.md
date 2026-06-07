# NextGen HR — Employee Risk Analysis

![NextGen Overview](nextgen-hr-overview.png)

## Overview
A structured SQL-based HR analytics project investigating employee flight risk, compensation inequity, and business risk across departments at NextGen. Built entirely in PostgreSQL using pgAdmin 4, the analysis translates raw HR data into actionable executive-level recommendations for talent retention and salary restructuring.

---

## Problem Statement
Organisations rarely know they are losing their best people until it is too late. This project interrogates NextGen's HR database to identify which employees are at risk of leaving, why they are leaving, which departments are most exposed, and whether compensation is correctly aligned to performance — before the damage becomes irreversible.

**Three core business problems identified:**
- **Employee Turnover** — Increasing concerns about why employees are leaving and which departments are most affected
- **Performance Variability** — Significant differences in performance scores across departments with no clear strategy to address gaps
- **Salary Disparities** — Lack of fairness between salary and performance — best performers not always the highest earners

---

## Tools & Techniques
- **PostgreSQL 18** — primary database environment
- **pgAdmin 4** — query development and execution
- **SQL techniques:** SELECT, WHERE, GROUP BY, ORDER BY, aggregate functions (COUNT, AVG, SUM), JOIN operations, CASE statements, risk classification logic
- **Data quality handling** — Department ID mismatch identified and resolved using employee table as master record

---

## Key Analysis & Findings

### Why Are Employees Leaving?
| Reason | Percentage |
|---|---|
| Personal Reasons | 39.29% |
| Found Another Job | 25.00% |
| Career Growth | 17.86% |
| Retired | 17.86% |

**Critical finding:** 42.86% of all leavers departed for entirely **preventable reasons** — directly addressable through better compensation and career development.

---

### Employee Risk by Department
| Department | Flight Risk | Business Risk | Stable |
|---|---|---|---|
| Engineering | 2 | 0 | 10 |
| HR | 7 | 4 | 37 |
| Marketing | 5 | 0 | 1 |
| Sales | 16 | 1 | 109 |

**83% of Marketing staff are flight risks** — despite being the highest performing department in the company.

---

### Performance vs Salary Correlation
| Department | Avg Performance | Avg Salary | Assessment |
|---|---|---|---|
| Marketing | 4.17 | £77,857 | **Underpaid** |
| HR | 4.11 | £81,818 | Fairly compensated |
| Sales | 4.07 | £82,069 | Fairly compensated |
| Engineering | 4.01 | £80,000 | Fairly compensated |

**Core inequity:** Marketing delivers the best performance yet receives the lowest average salary. Total salary budget is £4,850,000 — the money exists. The distribution is wrong.

---

### Additional Findings
- **16 high-performing Sales employees** earning only £60,000 — significantly underpaid relative to output
- **HR has 7 flight risks AND 4 business risks** simultaneously — high performers underpaid while underperformers are overpaid
- **Engineering is the most stable department** — only 2 flight risks out of 12, a benchmark for management practice

---

## Business Recommendations

| Priority | Department | Action |
|---|---|---|
| **P1** | Marketing | Immediate salary review, retention bonuses, career development meetings |
| **P2** | Sales | Review salary bands, introduce performance bonuses, create career progression pathway |
| **P3** | HR | Address pay equity, implement PIPs for 4 business risk employees |
| **P4** | Engineering | Monitor 2 flight risks, schedule salary reviews, maintain current management approach |

---

## Conclusion
NextGen is not losing poor performers — it is losing its **best people**. The root cause is compensation inequity, not performance failure. A company-wide salary equity review is the single highest-impact corrective action available.

---

## Technical Note
A data quality issue was identified during analysis — a Department ID mismatch between the employee and performance tables. This was documented and resolved by designating the employee table as the master record, ensuring analytical integrity throughout.

---

## Tools Used
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge)

---

## Author
**Vincent Idugboe**
Data & Business Intelligence Analyst | Sheffield, UK

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/idugboe-vincent-)
