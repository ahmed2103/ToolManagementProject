# D365 F&O Tool Tracking & Asset Management Module

## 📌 Project Overview

An enterprise-grade custom module built on **Microsoft Dynamics 365 Finance & Operations** to manage internal tools and assets lifecycle.

The solution enables organizations to register tools, control employee issuance and returns, enforce business validation rules, and generate operational reports — all aligned with D365 architectural best practices.

---

## 🛠️ Technical Highlights

### 🔹 Custom AOT Components
- Custom **Tables**, **Extended Data Types (EDTs)**, and **Enums**
- Proper table relations and indexes
- Replacement keys and reference integrity

### 🔹 Business Logic (X++)
- Validation rules implemented in:
  - `validateWrite()`
  - `insert()`
  - `modifiedField()`
- Prevents:
  - Issuing unavailable tools
  - Issuing tools to employees with overdue returns
- Enforced state transitions via Enum-driven logic

### 🔹 Reporting (SSRS)
- Parameterized SSRS report:
  - Employee liability report
  - Tool issuance history
- RDP-based implementation with temporary tables

### 🔹 Security Framework
- Custom **Security Privileges**
- Controlled access to:
  - Tool master data
  - Issue/Return transactions
  - Reporting

### 🔹 Integration Ready
- Custom **Data Entities**
- OData-enabled for external integration
- Compatible with Excel add-in and bulk import scenarios

### 🔹 UI/UX Design
- Built using standard D365 **Form Patterns** (e.g., Details Master)
- Native user experience aligned with Microsoft design guidelines

---

## 📂 Project Structure (AOT Metadata)

This project follows the standard package-based metadata structure used in Dynamics 365 F&O:
