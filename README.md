# D365 F&O Tool Tracking & Asset Management Module

## 📌 Project Overview
An end-to-end custom module built for **Microsoft Dynamics 365 Finance & Operations**. This solution is designed for organizations that need to manage internal equipment, tools, and assets. It tracks the lifecycle of an asset from registration to employee loaning, including automated validation and reporting.

## 🛠️ Key Technical Features
* **Custom AOT Elements:** Built from the ground up using custom Tables, EDTs, and Enums.
* **Business Logic (X++):** Specialized validation logic in `validateWrite` and `insert` methods to enforce business rules (e.g., status checks).
* **Reporting:** Integrated **SSRS Reports** for asset liability and inventory tracking.
* **Security Framework:** Defined **Security Privileges** to manage user access levels.
* **Integration Ready:** Includes **Data Entities** for seamless OData and Office integration.
* **UI/UX:** Adheres to standard D365 **Design Patterns** for a native user experience.

## 📂 Project Structure (AOT Metadata)
The project follows the standard D365 F&O package structure for seamless deployment and source control:

```text
├───AxClass              # Business logic controllers and event handlers
├───AxDataEntityView    # Data entities for OData & Excel integration
├───AxEdt               # Custom Extended Data Types (EDTs) and Deltas
├───AxForm              # User Interface designs and form logic
├───AxMenu              # Custom menu structures
├───AxMenuExtension     # Extensions for standard D365 menus
├───AxMenuItemDisplay   # Menu items for forms access
├───AxMenuItemOutput    # Menu items for launching SSRS reports
├───AxReport            # SSRS Report designs and RDP classes
├───AxSecurityPrivilege # Granular security roles and permissions
└───AxTable             # Database schema and table-level methods

## 📝 How it Works
1.  **Define Tools:** Users add tools to the system and set their initial status.
2.  **Loan Process:** When a tool is assigned to a worker, the system checks the tool's status via X++ code.
3.  **Validation:** If the tool is "Damaged", the system triggers a `checkFailed` warning and prevents the transaction.

## 👤 Author
**Ahmed Fathy Hasona** *Full-Stack Developer & D365 F&O Technical Consultant Trainee*
