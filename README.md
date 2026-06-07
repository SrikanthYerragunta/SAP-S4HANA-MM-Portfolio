# SAP S/4HANA MM Complete End-to-End Functional Configuration Documentation

This repository hosts the comprehensive functional documentation and process verification logs for **Düsseldorf Manufacturing AG (DMAG)**, a fictional sandbox-based SAP S/4HANA practice implementation created for learning and demonstration purposes. 

The documentation provides a step-by-step blueprint of organizational setup, master data extension, transaction cycles, and cross-module financial integration.

---

## 📂 Portfolio Structure & Scope

The portfolio is divided into three distinct documentation components:

### 📄 [PART 1 — MM Configuration Portfolio](./PART_1_MM_Configuration_Portfolio.pdf)
Documents the core organizational blueprint and system setup parameters for the enterprise:
* **Enterprise Structure:** Setup of Company Code `DM01`, Plants (`DM01` Düsseldorf, `DM02` Dortmund, `DM03` Stuttgart), Storage Locations (`SL01–SL03`), and Purchasing Organization `DMPO`.
* **Master Data Maintenance:** Material Master configurations for `ROH`, `HALB`, and `FERT` types, and standard Business Partner vendor migration roles.
* **System Purchasing Controls:** Configuration details for the `ZDM01` pricing schema condition technique and classification-based Purchase Order release strategies.
* **Logistics Engine Verification:** High-level scope settings for automated replenishment planning, Stock Transport Orders (STO), Consignment, Subcontracting loops, Batch Management, Split Valuation by quality grade, and Physical Inventory cycles.

### 📄 [PART 2 — P2P End-to-End Cycle](./PART_2_P2P_End_To_End_Cycle.pdf)
Tracks the exact transactional document flow and user execution scripts within the sandbox environment:
* **Step-by-Step Document Trail:** Functional logging mapping Purchase Requisition ➡️ Request for Quotation ➡️ Quotation Maintenance ➡️ Price Comparison Matrix ➡️ Info Record ➡️ Purchase Order ➡️ Goods Receipt (`MIGO`) ➡️ Invoice Verification (`MIRO`).
* **Advanced Processing Formats:** Realized validation scenarios for Value Contracts, Scheduling Agreements, automated PO conversions, Parked Invoices, and Quota Arrangements.
* **L2/L3 Functional Troubleshooting:** Playbooks addressing common support bottlenecks including GR/IR quantity/value mismatches, workflow approval strategy blocks, condition pricing errors, and system invoice holds.

### 📄 [PART 3 — Material Ledger and OBYC](./PART_3_Material_Ledger_And_OBYC.pdf)
Detail logs covering system valuation rules, financial ledger compliance, and cross-module synchronization:
* **Material Ledger Setup:** Functional configuration for multi-currency inventory valuation tracking Company Code currency (`EUR`) and Group currency (`USD`) simultaneously.
* **Actual Costing Framework:** Period-end variance accumulation, multi-level revaluation architecture logs, and cost component analyses.
* **`OBYC` Automatic Account Determination:** Direct configuration rules linking materials and movement types to specific financial ledger accounts across transaction keys `BSX`, `WRX`, `PRD`, `GBB`, `FRE`, `KON`, and `INV`.
* **Month-End Closure Sequence:** System processing order from initial clearing reviews up to final actual costing run executions.

---

## 💼 Contact & Candidate Highlights
* **Target Role:** SAP S/4HANA MM Functional Consultant
* **Location Base:** Düsseldorf Area, Germany 🇩🇪
* **Legal Authorization:** Permanent Resident (Niederlassungserlaubnis) — No Sponsorship Required
* **Availability Window:** 2-Week Notice Period
