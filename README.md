# D365 F&O Tool Tracking System (Custom Module)

## 📌 Project Overview
A custom extension for **Microsoft Dynamics 365 Finance & Operations** designed to streamline the process of tracking internal tools and assets. This module allows organizations to manage their inventory of tools and monitor loan transactions to employees, ensuring accountability and reducing asset loss.

## 🛠️ Technical Features
* **Custom Data Model:** Created specialized Tables (`AMSToolTable`, `AMSToolLoanTable`) and Extended Data Types (EDTs) for scalable architecture.
* **Advanced Business Logic (X++):** * Implemented validation logic to prevent loaning tools marked as "Damaged".
    * Handled data relations between Workers (HcmWorker) and Assets.
* **UI/UX:** Designed standardized Forms using Microsoft's **Simple List** and **Simple List & Details** patterns.
* **Data Integrity:** Enforced referential integrity through AOT Relations and Delete Actions.

## 🚀 Development Environment
* **Platform:** Microsoft Dynamics 365 Finance and Operations.
* **Tools:** Visual Studio 2019/2022 (VHD OneBox Environment).
* **Language:** X++ (Object-Oriented).
* **Database:** SQL Server.

## 📂 Project Structure
* **/Tables:** Definitions for tools, statuses, and loan history.
* **/EDTs:** Custom data types for Tool IDs and Labels.
* **/Enums:** Base Enums for Tool Status (Available, Loaned, Damaged).
* **/Forms:** User interfaces for data entry and tracking.

## 📝 How it Works
1.  **Define Tools:** Users add tools to the system and set their initial status.
2.  **Loan Process:** When a tool is assigned to a worker, the system checks the tool's status via X++ code.
3.  **Validation:** If the tool is "Damaged", the system triggers a `checkFailed` warning and prevents the transaction.

## 👤 Author
**Ahmed Fathy Hasona** *Full-Stack Developer & D365 F&O Technical Consultant Trainee*
