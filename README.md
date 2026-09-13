# HandsMen Threads – Elevating the Art of Sophistication in Men's Fashion

## 📌 Project Overview

HandsMen Threads is a Salesforce CRM project developed to manage and automate the core business operations of a men's fashion organization.

The system provides a centralized platform for managing customers, products, orders, inventory, and marketing campaigns. Salesforce automation, security, Flow, and Apex are used to improve business efficiency and maintain accurate data.

---

## 🎯 Project Objectives

- Manage customer information
- Manage products and inventory
- Track customer orders
- Maintain accurate stock levels
- Automate customer loyalty status
- Automate order confirmation
- Generate low-stock inventory alerts
- Provide role-based access to users
- Improve overall CRM management

---

## 🛠️ Technologies Used

- Salesforce CRM
- Salesforce Lightning
- Salesforce Flow
- Apex
- Batch Apex
- Scheduled Apex
- Custom Objects
- Custom Fields
- Formula Fields
- Validation Rules
- Lookup Relationships
- Master-Detail Relationships
- Profiles
- Roles
- Permission Sets
- Git
- GitHub
- VS Code
- Salesforce CLI

---

## 📦 Custom Objects

The project includes the following custom Salesforce objects:

1. **HandsMen Customer**
2. **HandsMen Product**
3. **HandsMen Order**
4. **Inventory**
5. **Marketing Campaign**

---

## 🔗 Object Relationships

The project uses Salesforce relationships to connect business data.

- Marketing Campaign → HandsMen Customer
- HandsMen Product → HandsMen Order
- HandsMen Order → HandsMen Customer
- Inventory → HandsMen Product

The Inventory-to-Product relationship uses a **Master-Detail Relationship**, while the other relationships use **Lookup Relationships**.

---

## ⚡ Salesforce Automation

### 1. Customer Loyalty Status Automation

A scheduled Flow automatically updates customer loyalty status based on total purchases.

| Total Purchases | Loyalty Status |
|---|---|
| Greater than 1000 | Gold |
| Less than 500 | Bronze |
| 500 to 1000 | Silver |

The Flow runs on a scheduled basis and updates customer records automatically.

### 2. Order Confirmation Automation

An automated Flow is used to process order confirmation and send an order confirmation notification.

### 3. Inventory Stock Alert

A Flow is implemented to identify low-stock inventory and generate a stock alert.

---

## 💻 Apex Development

The project includes Apex components for business automation and inventory processing.

### Apex Classes

- `InventoryBatchJob`
- `OrderTriggerHandler`

### Apex Trigger

- `OrderTrigger`

### Batch Apex

`InventoryBatchJob` implements Batchable and Schedulable Apex to process inventory records and execute inventory-related operations in batches.

---

## 📧 Email Automation

An email template named:

**Order Confirmation Email**

is implemented to notify customers when their order has been confirmed.

The project also includes a stock alert automation for inventory management.

---

## 🔐 Security and Access

Salesforce security features are used to control access to the application.

The project includes:

- Roles
- Profiles
- Permission Sets
- Object-Level Permissions

A custom profile named **Platform 1** is used for appropriate access to HandsMen Products and Inventory.

---

## ✅ Data Validation

Validation rules are implemented to maintain data accuracy.

### Inventory

Inventory quantity cannot be less than or equal to zero.

### Customer

Customer email must contain the required Gmail format.

### Order

Order total amount must be greater than zero.

---

## 📊 Lightning Application

A custom Salesforce Lightning application named:

**HandsMen Threads**

provides centralized navigation for the project.

The application includes access to:

- HandsMen Customers
- HandsMen Products
- HandsMen Orders
- Inventory
- Marketing Campaigns
- Reports
- Dashboard
- Accounts
- Contacts

---

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
