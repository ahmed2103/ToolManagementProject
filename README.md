# D365 F&O Tool Tracking & Asset Management Module

## 📌 Project Overview

An end-to-end custom module built for **Microsoft Dynamics 365 Finance & Operations** that enables organizations to efficiently manage internal equipment, tools, and assets. This solution tracks the complete asset lifecycle—from initial registration through employee loaning—with automated validation, comprehensive reporting, and security controls.

## 🎯 Key Business Features

- **Asset Lifecycle Management:** Register, track, and manage tools and equipment from creation to retirement
- **Employee Loaning System:** Assign tools to workers with automated status validation
- **Automated Validation:** Business rules enforce tool eligibility before loaning (e.g., prevent damaged tools from being assigned)
- **Comprehensive Reporting:** SSRS-integrated reports for asset liability and inventory tracking
- **Data Integration:** OData and Excel integration via custom Data Entities
- **Security & Access Control:** Role-based security privileges for granular user permissions

## 🛠️ Technical Architecture

### Core Technologies
- **Language:** X++ (Dynamics 365 F&O)
- **Database:** SQL Server (D365 backend)
- **Reporting:** SQL Server Reporting Services (SSRS)
- **Integration:** OData, Excel Add-in, Data Entities
- **Design Pattern:** Standard D365 Form Design Patterns

### Key Technical Components

| Component | Purpose |
|-----------|---------|
| **Custom Tables** | Database schema for tools, assets, and loan records |
| **Extended Data Types (EDTs)** | Reusable data type definitions with validation |
| **X++ Classes** | Business logic, event handlers, and validation controllers |
| **Forms** | User interface for asset registration, loaning, and management |
| **Data Entities** | OData exposure for external system integration |
| **SSRS Reports** | Asset liability and inventory reports |
| **Security Privileges** | Role-based access control and feature permissions |
| **Menu Items** | Navigation and report launching |

## 📂 Project Structure (AOT Metadata)

The project follows the standard Microsoft Dynamics 365 F&O package structure for seamless deployment and source control:

```
ToolTrackingModule/
├── AxClass/                    # Business logic, controllers, and event handlers
├── AxDataEntityView/           # Data entities for OData & Excel integration
├── AxEdt/                      # Custom Extended Data Types (EDTs) and Deltas
├── AxForm/                     # Form UI designs and form-level business logic
├── AxMenu/                     # Custom navigation menu structures
├── AxMenuExtension/            # Extensions to standard D365 menus
├── AxMenuItemDisplay/          # Menu items for form navigation
├── AxMenuItemOutput/           # Menu items for SSRS report launches
├── AxReport/                   # SSRS report designs and RDP (Report Data Provider) classes
├── AxSecurityPrivilege/        # Security roles, duties, and permissions
└── AxTable/                    # Database tables, indexes, and table-level methods
```

## 🔄 Business Process Flow

### 1. **Tool Registration**
- Users create new tool records in the system
- Set initial status (e.g., "Available", "In Use", "Damaged", "Retired")
- Define tool properties (name, category, serial number, owner)

### 2. **Loan Assignment**
- Workers request or are assigned tools from inventory
- System validates tool eligibility before assignment
- Loan record is created with timestamp and assignment details

### 3. **Automated Validation**
- X++ `validateWrite()` and `insert()` methods enforce business rules
- Example: Damaged tools cannot be loaned to employees
- If validation fails, a `checkFailed` warning is triggered and the transaction is blocked

### 4. **Reporting & Analytics**
- Generate asset liability reports showing who has which tools
- Track inventory levels and tool availability
- Monitor tool status and depreciation

## 🔒 Security Framework

The module implements a layered security approach:

- **Role-Based Access Control:** Define which users can create, modify, or delete assets
- **Privilege-Based Permissions:** Granular controls over form access and report visibility
- **Audit Trail:** Track changes to asset records for compliance
- **Data Entity Security:** Control external system access to sensitive tool data

## 🔗 Integration Capabilities

- **OData API:** Expose tool and asset data for third-party integrations
- **Excel Add-in:** Seamless bulk import/export of tool inventory
- **D365 Standard Integration:** Works with Finance, Supply Chain Management, and Human Resources modules

## 📊 Reporting

The module includes pre-built SSRS reports:

- **Asset Liability Report:** Shows all tools currently assigned to employees
- **Inventory Report:** Current stock levels and tool availability
- **Status Summary:** Overview of tool conditions and maintenance needs

## ⚙️ Customization & Extension

This module is designed for extensibility:

- Add custom fields to tool records
- Extend validation logic with additional business rules
- Create new reports based on project requirements
- Integrate with external systems via Data Entities

## 🚀 Deployment

The module is packaged as a standard D365 F&O AOT package and can be deployed via:

- Visual Studio build and package deployment
- Lifecycle Services (LCS) environment deployment
- Source control integration (Git, Azure DevOps)

## 📋 Prerequisites

- Microsoft Dynamics 365 Finance & Operations (latest versions)
- System admin or developer access for deployment
- SQL Server Reporting Services (SSRS) configured
- Basic understanding of D365 F&O module structure

## 📧 Support & Contact

**Author:** Ahmed Fathy Hasona  
**Title:** Full-Stack Developer & D365 F&O Technical Consultant Trainee  
**Expertise:** X++ Development, Custom Module Architecture, SSRS Reporting, D365 F&O Integration

---

**Last Updated:** February 2026  
**Version:** 1.0  
**Status:** Production Ready
