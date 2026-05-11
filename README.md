
# Part 4: AI Solution Design for a Business Problem

** Module 5 Assignment**

---

## Overview
This repository contains a complete AI solution design for a real-world business problem in the **Healthcare** domain. The solution covers problem formulation, data planning, model recommendation, evaluation strategy, and responsible AI considerations — based on the provided reference catalog and KPI dataset.

**Dataset Reference:** Part 4 reference files (Google Drive — Masai Assignment Folder)  
- `ai_usecase_reference_catalog.csv` — 10 domain-problem-model mappings  
- `business_kpi_sample.csv` — 12 months of baseline KPI data

---

## Domain Selected: Healthcare

**Business Problem:** AI-Powered Medical Image Triage System  
Medical scans (X-rays) are currently reviewed in arrival order — critical patients wait hours before being seen. This AI system automatically classifies scans by urgency level so radiologists can prioritize life-threatening cases immediately.

---

## Tasks Summary

| Task | Description | Answer |
|------|-------------|--------|
| Task 1 | Business Domain | Healthcare |
| Task 2 | Business Problem | Medical scan triage — no urgency prioritization in current process |
| Task 3 | AI Task Type | Image Classification (3 classes: Normal / Moderate / Critical) |
| Task 4 | Data Requirements | Labeled X-ray images, 30,000+ samples, DICOM format |
| Task 5 | Model Recommendation | ResNet-50 with Transfer Learning (CNN) |
| Task 6 | Evaluation Plan | Recall >95% (Critical class), F1 >90%, Alert time <15 min |
| Task 7 | Responsible AI | Bias audits, privacy compliance, human oversight, no autonomous decisions |
| Task 8 | Final Summary | One-page solution summary covering all aspects |

---

## Key Highlights

### Problem
- Scans reviewed in arrival order — no urgency sorting
- Average time from scan to radiologist alert: 6–12 hours
- Radiologist fatigue causes ~8% error rate on critical findings
- Severe radiologist shortage in rural/smaller hospitals

### AI Solution
A CNN (ResNet-50 Transfer Learning) model classifies each incoming scan as:
- **Normal** → Added to routine queue
- **Moderate** → Schedule review within 24 hours  
- **Critical** → Immediately alert radiologist

### Expected Impact (from KPI baseline data)
| Metric | Before | After AI |
|--------|--------|---------|
| Scan-to-alert time | 6–12 hours | <15 minutes |
| Critical miss rate | ~8% | <1% |
| Radiologist efficiency | Baseline | +40% |
| Patient satisfaction | 6.4/10 | >8.0/10 |
| Cost per diagnosis | High | -35% |

### Responsible AI
- Human radiologist confirms every AI decision — no autonomous clinical action
- All patient data de-identified before processing
- Regular demographic bias audits
- Monthly model performance reviews
- Full HIPAA/PDPA/GDPR compliance

---

## Repository Structure
```
part-4-ai-solution-design/
├── README.md                    ← This file
├── solution_report.md           ← Full detailed report (all 8 tasks)
└── diagrams/
    └── solution_architecture.png ← System flow + model architecture diagram
```

## How to Read This Project
1. Start with `solution_report.md` — it contains all 8 tasks answered in detail
2. Refer to `diagrams/solution_architecture.png` for the visual system design
3. This README gives a quick summary of the entire solution
