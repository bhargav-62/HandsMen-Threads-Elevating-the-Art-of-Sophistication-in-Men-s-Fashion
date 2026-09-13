# HandsMen Threads – Elevating the Art of Sophistication in Men's Fashion

## 📌 Project Overview

HandsMen Threads is a Salesforce CRM solution designed to manage and automate the operations of a men's fashion business.

The project provides a centralized system for managing customers, products, orders, inventory, and marketing campaigns. Salesforce automation is used to improve order processing, inventory management, customer loyalty, and business operations.

## 🎯 Objectives

- Manage customer information efficiently
- Manage products and inventory
- Track customer orders
- Maintain accurate inventory levels
- Automate customer loyalty status updates
- Automate order confirmation notifications
- Generate low-stock inventory alerts
- Provide controlled access to users based on their roles and profiles

## 🛠️ Technologies Used

- Salesforce CRM
- Salesforce Lightning
- Custom Objects
- Custom Fields
- Validation Rules
- Formula Fields
- Lookup Relationships
- Master-Detail Relationship
- Lightning App
- Profiles and Roles
- Permission Sets
- Salesforce Flows
- Apex
- Batch Apex
- Scheduled Apex
- Git & GitHub

## 📊 Salesforce Data Model

The project contains the following custom objects:

- **HandsMen Customer**
- **HandsMen Product**
- **HandsMen Order**
- **Inventory**
- **Marketing Campaign**

### Key Relationships

- Marketing Campaign → HandsMen Customer
- HandsMen Product → HandsMen Order
- HandsMen Order → HandsMen Customer
- Inventory → HandsMen Product

## ⚙️ Automation

### 1. Customer Loyalty Automation

A scheduled Salesforce Flow automatically updates customer loyalty status based on total purchases:

| Total Purchases | Loyalty Status |
|---|---|
| Greater than 1000 | Gold |
| Less than 500 | Bronze |
| 500 – 1000 | Silver |

### 2. Order Confirmation

An automated flow sends an order confirmation notification when an order is confirmed.

### 3. Inventory Stock Alert

A flow is used to identify low-stock inventory and trigger a stock alert.

### 4. Inventory Batch Processing

A Batch Apex and Schedulable Apex process is implemented for inventory management and scheduled execution.

## 🔐 Security and Access

The project uses Salesforce security features including:

- Roles
- Profiles
- Permission Sets
- Object-Level Permissions

A custom **Platform 1** profile was created with appropriate permissions for HandsMen Products and Inventory.

## ✅ Validation Rules

Validation rules are implemented to maintain data accuracy.

Examples include:

- Inventory quantity cannot be less than or equal to zero
- Customer email must contain `@gmail.com`
- Order total amount must be greater than zero

## 📧 Email Automation

An order confirmation email template is implemented:

**Order Confirmation Email**

It is used to notify customers when their order has been confirmed.

## 💻 Apex Components

The project includes:

- `InventoryBatchJob`
- `OrderTriggerHandler`
- `OrderTrigger`

These components support inventory processing and order-related automation.

## 📁 Project Structure

```text
HandsMenThreads/
│
├── force-app/
│   └── main/
│       └── default/
│           ├── applications/
│           ├── classes/
│           ├── flows/
│           ├── layouts/
│           ├── objects/
│           ├── permissionsets/
│           ├── profiles/
│           ├── roles/
│           ├── tabs/
│           └── triggers/
│
├── config/
├── scripts/
├── .vscode/
├── package.json
├── sfdx-project.json
└── README.md
