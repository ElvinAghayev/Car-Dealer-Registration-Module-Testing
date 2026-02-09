# Car-Dealer-Registration-Module-Testing
Comprehensive QA testing for a multi-step test drive registration module, identifying critical business logic errors and UX flaws.

# QA Project: Test Drive Registration Module Testing

This project focuses on the manual testing of a step-by-step car test drive registration module. It covers end-to-end user flows, data integrity validation, and business requirement compliance.

## 🛠️ Testing Environment
- **Device:** Desktop
- **Browser:** Google Chrome (Latest Version)
- **Object under test:** Car Dealer Registration Module

---

## 📋 Project Requirements
- Step-by-step registration for a car test drive.
- Validate model selection, dealer location, and user contact information.
- Ensure logical flow between steps (navigation).
- Desktop version optimization.

---

## 📂 Testing Scope
I performed an in-depth analysis of the application, identifying:
- **Core Logic Errors:** Proceeding without required data.
- **Business Integrity:** Ensuring all models belong to the correct brand.
- **UI/UX Consistency:** Navigation flow and visual feedback.

---

## 📊 Testing Statistics
| Total Test Cases | Passed | Failed | Critical Bugs |
| :--- | :---: | :---: | :---: |
| 24 Scenarios | 14 | 10 | 7 |

---

## 🐞 Key Findings & Critical Bugs

### 1. [BUSINESS-001] Invalid Data Integrity
- **Summary:** A Porsche model ("Cayenne 400") is listed in the Mercedes-Benz car selection.
- **Severity:** Critical (Business Logic Error).

### 2. [CRITICAL-001] Missing Mandatory Field Validation
- **Summary:** User can proceed to Step 2 without selecting any car model.
- **Severity:** Critical (Core Logic).

### 3. [CRITICAL-005] Technical Variable Exposure
- **Summary:** The final confirmation screen displays unparsed technical placeholders like `{lastName}` and `{firstName}`.
- **Severity:** High (UI/UX & Data Integrity).

### 4. [FLOW-003] Incorrect Navigation Numbering
- **Summary:** The header displays Step 4 as "(5)", causing confusion in the sequential flow.
- **Severity:** High.

---

## 📝 Test Case Example: TC-001
**Goal:** Verify that the "Continue" button is only enabled after a model is selected.
- **Steps:**
  1. Open the Registration Module (Step 1).
  2. Observe the "Continue" button status without selecting a car.
  3. Select a car model.
- **Actual Result:** The button is active by default before any selection is made.
- **Status:** **FAIL**

---

## 🏁 Conclusion
The module currently allows users to complete a registration with missing or incorrect data, which would lead to failed business leads. Critical improvements are needed in mandatory field validation and data parsing before deployment.

---
*For the full test suite and bug reports, please refer to: [TestTASK.xlsx](./TestTASK.xlsx)*
