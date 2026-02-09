# 🏎️ Car Dealer Registration Module Testing
> **Comprehensive QA audit of a multi-step test drive booking system.**

[![QA-Status](https://img.shields.io/badge/Status-Completed-success.svg)](#)
[![Test-Cases](https://img.shields.io/badge/Test--Cases-24-blue.svg)](#)
[![Bugs-Found](https://img.shields.io/badge/Bugs--Found-10-red.svg)](#)

This project involves the end-to-end manual testing of a Mercedes-Benz test drive registration module. The audit focuses on functional integrity, business logic consistency, and user experience (UX) flow.

---

## 📋 Project Scope & Requirements
The module is a 4-step sequential registration flow:
1. **Step 1:** Model Selection (visual carousel).
2. **Step 2:** Dealer & Location Selection.
3. **Step 3:** Personal Contact Information.
4. **Step 4:** Final Confirmation & Booking.

**Key Rule:** No data should be saved or emails sent, but the flow must be logically sound and validate all user inputs.

---

## 🛠️ Tech Stack & Environment
- **Browser:** Google Chrome (Latest Version)
- **Device:** Desktop (Windows 10)
- **Methodology:** Manual Functional Testing, UI/UX Audit, Business Logic Validation.

---

## 📊 Testing Executive Summary

| Total Scenarios | Passed ✅ | Failed ❌ | Critical Bugs ⚠️ |
| :--- | :---: | :---: | :---: |
| 24 Test Cases | 14 | 10 | 7 |

### Bug Severity Distribution
- **Critical:** 30% (Data Integrity & Core Logic)
- **High:** 40% (UI/UX & Navigation)
- **Medium/Low:** 30% (Visual & Minor UX)

---

## 🐞 Critical Findings (Bug Highlights)

### 🚨 [BUSINESS-001] Invalid Data Integrity
- **Issue:** A Porsche model (**"Cayenne 400"**) is incorrectly listed within the Mercedes-Benz car selection carousel.
- **Impact:** Severe brand inconsistency and business logic failure.

### 🚨 [CRITICAL-001] Mandatory Field Bypass
- **Issue:** User can proceed to Step 2 without selecting a car model. The "Continue" button is active by default.
- **Impact:** System allows incomplete leads to be generated.

### 🚨 [UX-005] Technical Variable Exposure
- **Issue:** The final confirmation screen displays unparsed placeholders like `{lastName}` and `{firstName}` instead of actual user data.
- **Impact:** Highly unprofessional user experience and technical data failure.

### 🚨 [FLOW-003] Incorrect Step Numbering
- **Issue:** The header displays the final step as **Step (5)**, even though it is the 4th screen.
- **Impact:** Causes user confusion regarding progress.

---

## 📝 Test Case Sample: Navigation Logic
| ID | Action | Expected Result | Status |
| :--- | :--- | :--- | :--- |
| **TC-001** | Click 'Continue' without selection | Button should be disabled until a model is selected. | **FAIL** ❌ |
| **TC-002** | Rapidly click navigation arrows | Smooth transition between model images. | **FAIL** ❌ |
| **TC-003** | Select a valid car model | Highlight selection and enable 'Continue'. | **PASS** ✅ |

---

## 📂 Deliverables
- [📄 Full Test Task Report (PDF)](./Test%20Task%20QA.pdf)
- [📊 Detailed Bug Report (Excel)](./TestTASK.xlsx)

---
**Contact:** Elvin Aghayev — *QA Specialist*
