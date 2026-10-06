# Margix IMS - Complete Feature & Module Overview

This document provides a comprehensive breakdown of every feature built into the Margix Inventory Management System. It maps each capability to its exact page (URL route) and explains the practical business value of the feature.

---

## 1. Dashboard & Analytics
*High-level overview and insights into business performance.*

*   **Page:** `/` (Home/Dashboard)
    *   **Feature:** Live stock positions, recent activities, and high-level metric summaries.
    *   **How it helps:** Gives business owners and managers an instant, real-time snapshot of warehouse health the moment they log in. It prevents blind spots by putting the most critical data front and center.
*   **Page:** `/analytics`
    *   **Feature:** Visual charts and graphs analyzing sales trends, inventory turnover, and purchasing behavior.
    *   **How it helps:** Translates raw data into actionable visual insights. It helps management identify seasonal trends, forecast future demand, and make data-driven purchasing decisions.

## 2. Masters (Core Data Management)
*The foundational data structure where all products, people, and locations are managed.*

*   **Page:** `/masters/skus`
    *   **Feature:** The core product catalog to add, edit, and manage all items.
    *   **How it helps:** Acts as the single source of truth for product information, ensuring consistency across sales, purchasing, and stock tracking.
*   **Page:** `/masters/skus/labels`
    *   **Feature:** Barcode/QR label generation and printing.
    *   **How it helps:** Enables fast, error-free scanning during dispatch, receiving, and stock counts. It eliminates manual data entry errors.
*   **Page:** `/masters/categories`
    *   **Feature:** Product category management.
    *   **How it helps:** Allows grouping of products for easier navigation, organized reporting, and bulk management.
*   **Page:** `/masters/godowns`
    *   **Feature:** Warehouse and branch location management.
    *   **How it helps:** Crucial for multi-branch businesses. It allows the system to partition stock data so owners know exactly *what* inventory is sitting *where*.
*   **Page:** `/masters/suppliers` & `/masters/customers`
    *   **Feature:** Vendor and Customer CRM details.
    *   **How it helps:** Centralizes contact information, billing details, and histories, making creating invoices and purchase orders vastly faster and more accurate.
*   **Page:** `/masters/hsn`
    *   **Feature:** HSN Code and GST tax rate configurations.
    *   **How it helps:** Ensures total legal and tax compliance by automatically applying the correct tax brackets to products during invoicing.

## 3. Purchasing & Vendor Operations
*Handling the procurement of goods from vendors.*

*   **Page:** `/purchase-orders`, `/purchase-orders/new`, `/purchase-orders/[id]`
    *   **Feature:** Create, approve, and track Purchase Orders (POs) sent to vendors.
    *   **How it helps:** Formalizes the buying process. It tracks what was ordered versus what was delivered, preventing over-payment for unreceived goods.
*   **Page:** `/grns`, `/grns/[id]`
    *   **Feature:** Goods Receipt Notes (GRN).
    *   **How it helps:** The official warehouse checkpoint. When a truck arrives, staff use GRNs to verify physical goods against the PO, officially and securely bringing them into live stock.
*   **Page:** `/purchase-returns`, `/purchase-returns/new`
    *   **Feature:** Process returns back to the supplier.
    *   **How it helps:** Ensures that defective, expired, or over-shipped goods are properly tracked and returned, recovering costs and maintaining accurate vendor ledgers.

## 4. Sales & Outward Operations
*Handling customer orders and getting goods out the door.*

*   **Page:** `/invoices`, `/invoices/new`, `/invoices/[id]`
    *   **Feature:** Create and manage Sales Invoices for billing customers.
    *   **How it helps:** Generates professional, GST-compliant bills instantly. It directly ties sales to inventory, automatically deducting stock when an invoice is finalized.
*   **Page:** `/dispatches`, `/dispatches/new`
    *   **Feature:** Track the physical delivery and logistics of an invoice.
    *   **How it helps:** Separates the financial transaction (Invoice) from the physical movement (Dispatch). It allows logistics teams to track delivery status without needing access to financial data.
*   **Page:** `/sales-returns`, `/sales-returns/new`
    *   **Feature:** Process items returned by customers.
    *   **How it helps:** Ensures returned stock is properly inspected and added back into the warehouse inventory, while adjusting the customer's financial account.

## 5. Inventory & Stock Control
*Core warehouse and stock tracking functionalities.*

*   **Page:** `/stock`, `/stock/[skuId]`
    *   **Feature:** Real-time view of current stock balances per item and Godown.
    *   **How it helps:** Eliminates guesswork. Sales teams can instantly confirm if an item is available to sell, preventing stockouts and disappointed customers.
*   **Page:** `/opening-stock`, `/opening-stock/new`
    *   **Feature:** Setting initial stock levels.
    *   **How it helps:** Streamlines onboarding for new branches or the annual auditing process by cleanly setting a baseline stock count.
*   **Page:** `/adjustments`, `/adjustments/new`
    *   **Feature:** Manual stock corrections (damages, expiries, counting errors).
    *   **How it helps:** Keeps the system accurate to the real world. When goods are broken or lost, it allows staff to legally adjust the system without falsifying sales.
*   **Page:** `/transfers`, `/transfers/new`
    *   **Feature:** Moving stock between different Godowns/Warehouses.
    *   **How it helps:** Maintains strict visibility of inventory during transit. If branch A is low on stock, branch B can transfer it, and the system tracks the exact movement.
*   **Page:** `/ledger`
    *   **Feature:** Immutable chronological log of all stock movements.
    *   **How it helps:** The ultimate security and audit tool. If stock numbers look wrong, the ledger proves exactly when, why, and how the stock changed, preventing employee theft or unseen errors.

## 6. Reports & Reporting
*Detailed tabular data for business analysis.*

*   **Page:** `/reports/stock-summary`
    *   **Feature:** Consolidated view of all stock counts and financial value.
    *   **How it helps:** Critical for accounting and insurance purposes. Shows exactly how much capital is tied up in physical inventory.
*   **Page:** `/reports/movements`
    *   **Feature:** Filterable history of specific item inward/outward movements.
    *   **How it helps:** Helps trace the exact lifecycle of a specific product batch to resolve disputes or trace defective items.
*   **Page:** `/reports/slow-stock` & `/reports/dead-stock`
    *   **Feature:** Identifies slow-moving and completely stagnant inventory.
    *   **How it helps:** Highly valuable for cash flow. Alerts owners to discount or liquidate dead stock so money can be reinvested into faster-selling items.

## 7. Alerts & Notifications
*Automated system warnings.*

*   **Page:** `/alerts`
    *   **Feature:** Centralized inbox for triggered warnings (like low-stock or expiry).
    *   **How it helps:** Proactive management. Instead of manually checking stock levels every day, the system automatically tells purchasing staff when it's time to reorder.

## 8. Admin, Security & Settings
*System configuration and employee management.*

*   **Page:** `/admin/users`
    *   **Feature:** Employee role and access management.
    *   **How it helps:** Security. Ensures a cashier cannot manipulate warehouse stock, and warehouse staff cannot view financial profits.
*   **Page:** `/audit`
    *   **Feature:** Data Security Audit Trail.
    *   **How it helps:** Total accountability. It records exactly which user edited an invoice, changed a setting, or deleted a record, acting as a deterrent against malicious activity.
*   **Page:** `/admin/notifications` & `/admin/numbering`
    *   **Feature:** Configuration for notification routing and document sequencing.
    *   **How it helps:** Customizes the software to fit the specific operational workflows and legal numbering formats of the business.

## 9. Accounting Integration
*Financial syncing.*

*   **Page:** `/tally`
    *   **Feature:** Dedicated dashboard for Tally ERP integration.
    *   **How it helps:** Bridges the gap between warehouse operations and strict financial accounting. It automatically pushes sales and purchase data to Tally, eliminating double data entry for the accounting team.
