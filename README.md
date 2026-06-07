# SAP S/4HANA MM Complete End-to-End Functional Configuration Documentation

This repository contains the functional documentation and process verification logs for Düsseldorf Manufacturing AG (DMAG). This is a fictional sandbox-based SAP S/4HANA practice project created for learning and demonstration purposes. 

The documents show how I set up the organizational structure, extended master data, executed business processes, and handled financial integration in a test environment.

---

## 📂 Portfolio Structure and Scope

The portfolio is divided into three separate documents:

### 📄 [PART 1 — MM Configuration Portfolio](./PART_1_MM_Configuration_Portfolio.pdf)
This document outlines the basic organizational setup and system parameters for the business scenario:
* **Enterprise Structure:** Setup of the Company Code, Plants (Düsseldorf, Dortmund, Stuttgart), Storage Locations, and a Central Purchasing Organization.
* **Master Data Maintenance:** Material Master settings for raw materials, semi-finished items, and finished goods, along with standard Business Partner supplier setup.
* **Purchasing Controls:** Configuration details for a custom pricing schema and multi-level approval release strategies for purchase orders.
* **Logistics Scope:** Basic settings for automated replenishment planning, Stock Transport Orders, Vendor Consignment, Subcontracting loops, Batch Management, Split Valuation by quality grade, and Physical Inventory cycles.

### 📄 [PART 2 — P2P End-to-End Cycle](./PART_2_P2P_End_To_End_Cycle.pdf)
This document tracks the standard transactional flow and user steps verified within the test environment:
* **Step-by-Step Business Flow:** Documentation mapping the path from a Purchase Requisition, to a Request for Quotation, Quotation Maintenance, Price Comparison, Info Record, Purchase Order, Goods Receipt, and final Invoice Verification.
* **Additional Scenarios:** Process logs for Value Contracts, Scheduling Agreements, automated PO conversions, Parked Invoices, and Quota Arrangements.
* **Functional Troubleshooting:** Solutions for common user support issues, including GR/IR quantity or value mismatches, workflow approval blocks, pricing calculation errors, and system invoice holds.

### 📄 [PART 3 — Material Ledger and OBYC](./PART_3_Material_Ledger_And_OBYC.pdf)
This document covers material valuation rules, financial ledger integration, and system synchronization:
* **Material Ledger Setup:** Configuration for multi-currency inventory valuation, tracking both the local currency (EUR) and group currency (USD) at the same time.
* **Actual Costing Framework:** High-level summary of month-end variance accumulation, revaluation steps, and cost analysis.
* **Automatic Account Determination:** Configuration rules linking materials and stock movements to specific general ledger accounts using standard transaction keys like BSX, WRX, PRD, GBB, FRE, KON, and INV.
* **Month-End Sequence:** The processing order required to close the month, from clearing reviews to final costing execution.
