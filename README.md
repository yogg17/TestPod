# TestPod: Automated Subjective Evaluation System
[![Spring](https://img.shields.io/badge/Framework-Spring%20MVC-green.svg)]()
[![NLP](https://img.shields.io/badge/NLP-Apache%20OpenNLP-blue.svg)]()
[![Database](https://img.shields.io/badge/Database-MySQL-orange.svg)]()

### **Overview**
TestPod is a full-stack web application designed to bridge the gap between automated objective testing and manual subjective grading. It leverages **Natural Language Processing (NLP)** and **Rule-based Fuzzy Logic** to evaluate essay-based questions, significantly reducing the administrative burden on teaching faculty while providing students with immediate, transparent feedback.

### **Core Capabilities**
* **Automated Evaluation Engine:** Utilizes the Maximum Entropy Algorithm for POS tagging and sentence detection to analyze the semantic structure of student responses.
* **Intelligent Grading Logic:** Implements a hierarchical evaluation model that maps student "answer skeletons" against faculty-provided keys using weighted average scoring.
* **Fuzzy Logic Inference:** Employs rule-based fuzzy logic to handle the nuances of natural language, generating discrete scores and performance remarks.
* **Comprehensive Analytics:** Offers a dedicated Faculty Dashboard featuring test statistics, student performance distributions, and step-by-step evaluation reports.

---

### **System Architecture & Workflow**



1.  **Ingestion:** Faculty upload questions and "Gold Standard" answer keys.
2.  **Decomposition:** The system uses `SentenceDetectorME` to segment text and `en-pos-maxent` for Part-of-Speech tagging.
3.  **Skeletonization:** Answers are transformed into a `<POS Tag, Token>` mapping, removing noise (case conversion, trailing spaces).
4.  **Comparison:** The student container is cross-referenced with the faculty container to generate a **Similarity Index Matrix**.
5.  **Scoring:** The matrix is de-fuzzified and marks are calculated using a weighted average technique.

---

### **Technical Stack**

| Layer | Technology | Key Implementation |
| :--- | :--- | :--- |
| **Backend** | Spring MVC (Java) | Controller-driven architecture with Java Bean containers. |
| **NLP Engine** | Apache OpenNLP | Tokenization, POS Tagging, and Sentence Segmentation. |
| **Database** | MySQL | Relational storage for Test IDs, metadata, and user stats. |
| **Evaluation** | Fuzzy Logic | Rule-based remark generation and de-fuzzification. |
| **Front-End** | JSP & JSTL | Dynamic UI for Examination Centres and Dashboards. |

---

### **Key Modules**
* **Examination Centre:** Secure portal for students to access tests via unique IDs and submit responses.
* **Auto-Generated Reports:** High-fidelity feedback loops providing a step-by-step breakdown of how a score was derived.
* **Digital Question Paper:** An optimized interface for long-form text entry and real-time submission.

### **Demonstration**
* **Video Walkthrough:** [TestPod Implementation Demo](https://www.youtube.com/watch?v=3l3mN8IC6Ps)

### Snapshots of TestPod
#### Home page

![alt text for screen readers](./screenshots/home_page.png "TestPod")

#### Login

![alt text for screen readers](./screenshots/login.png "TestPod")

#### Faculty Dashboard

![alt text for screen readers](./screenshots/faculty_dashboard.png "TestPod")

#### Exam Dashboard

![alt text for screen readers](./screenshots/exam_dashboard.png "TestPod")

#### Auto Generated Report

![alt text for screen readers](./screenshots/auto_gen_report.png "TestPod")

#### Examination Centre

![alt text for screen readers](./screenshots/exam_center.png "TestPod")

#### Digital Question Paper

![alt text for screen readers](./screenshots/digital_qp.png "TestPod")
---
*Developed to modernize the backbone of the education industry through scalable AI solutions.*

