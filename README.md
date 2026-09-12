# 🚗 WhatNext Vision Motors

## Salesforce CRM Implementation

DRIVE LINK FOR DEMO VIDEO: https://drive.google.com/file/d/1jcrUomyoJJS7BzFNRR0MDAzIRXIhi5NC/view?usp=sharing

**WhatNext Vision Motors** is a Salesforce CRM application designed to manage the day-to-day operations of an automotive dealership. It provides a centralized platform for managing vehicles, customers, dealers, vehicle orders, test drives, and service requests.

The system also uses **Salesforce Flow, Validation Rules, Apex Triggers, Lightning App, Reports, Dashboards, and Security features** to reduce manual work and improve the dealership's overall workflow.

---

## 📌 Project Overview

The application manages the complete vehicle sales process:

**Customer Interest → Vehicle → Test Drive → Vehicle Order → Dealer Assignment → Order Confirmation**

The system automatically checks vehicle stock before an order is confirmed. It also assigns a suitable dealer and sends reminders for scheduled test drives.

Orders that cannot be confirmed because of insufficient stock can be processed once the vehicle inventory is replenished.

---

## 🎯 Objectives

* Centralize vehicle, customer, dealer, order, test-drive, and service data.
* Track vehicle stock and availability.
* Automate dealer assignment.
* Prevent orders from being confirmed when vehicles are out of stock.
* Automatically reduce vehicle stock after order confirmation.
* Send reminders for upcoming test drives.
* Maintain proper user access and security.
* Provide reports and dashboards for business monitoring.
* Reduce repetitive manual work using Flow and Apex.

---

## 🛠️ Salesforce Technologies Used

| Technology                      | Purpose                                  |
| ------------------------------- | ---------------------------------------- |
| Salesforce Lightning Experience | Main development environment             |
| Custom Objects                  | Store dealership-related information     |
| Lookup Relationships            | Connect related records                  |
| Validation Rules                | Prevent invalid orders                   |
| Salesforce Flow                 | Automate dealer assignment and reminders |
| Apex                            | Implement custom business logic          |
| Apex Trigger                    | Validate stock and update inventory      |
| Lightning App                   | Provide centralized navigation           |
| Dynamic Forms                   | Display relevant fields conditionally    |
| Reports                         | Analyze dealership activities            |
| Dashboards                      | Visualize business information           |
| Profiles                        | Define baseline user permissions         |
| Roles & Role Hierarchy          | Control record visibility                |
| Permission Sets                 | Provide additional access                |
| Sharing Rules                   | Control record access                    |

---

## 🗂️ Custom Objects

The application contains six main custom objects:

### 1. Vehicle

Stores:

* Vehicle model
* Price
* Stock quantity
* Availability
* Associated dealer

### 2. Dealer

Stores:

* Dealer name
* Location
* City
* Contact information

### 3. Customer

Stores customer information used for:

* Vehicle purchases
* Test drives
* Service requests

### 4. Vehicle Order

Stores:

* Customer
* Vehicle
* Dealer
* Order date
* Order status

### 5. Vehicle Test Drive

Stores:

* Customer
* Vehicle
* Appointment date
* Test-drive status

### 6. Vehicle Service Request

Stores:

* Customer
* Vehicle
* Issue description
* Service status

The objects are connected using lookup relationships so that related records can be accessed easily.

---

## ⚙️ Automation

### 🔹 1. Dealer Assignment Flow

When a new vehicle order is created, the Flow:

1. Gets the customer information.
2. Identifies an appropriate/nearest dealer.
3. Updates the Vehicle Order with the dealer automatically.

This eliminates the need for staff to manually as
