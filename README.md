# SAP S/4HANA Materials Management (MM) Functional Portfolio

## 🏢 Portfolio Project: Düsseldorf Manufacturing AG (Sandbox Scenario)
This repository documents a complete, end-to-end functional configuration portfolio built within an SAP S/4HANA sandbox environment. Designed around a fictional precision engineering scenario, this project serves as practical proof of my hands-on module configuration capabilities, business process design skills, and functional troubleshooting competency as I transition into SAP consulting.

---

## 🏗️ 1. Enterprise Structure & Master Data Design
Configured a multi-plant organizational hierarchy to model localized manufacturing and centralized procurement operations:
* **Organizational Setup:** Mapped Company Code (`DM01`), 3 production/assembly plants (Düsseldorf, Dortmund, Stuttgart), and respective storage locations (`SL01–SL03`).
* **Sourcing Architecture:** Configured a centralized Purchasing Organization (`DMPO`) and specialized Purchasing Groups (`DMG`).
* **Business Partner Framework:** Configured standard S/4HANA Business Partner (`BP`) roles (`FLVN00` for Finance and `FLVN01` for Purchasing), transitioning away from legacy vendor master approaches.

---

## 🔄 2. Procure-to-Pay (P2P) Workflows & System Controls
Implemented a standardized procurement lifecycle, ensuring strict data flow accuracy across transactions:
* **The Procurement Cycle:** Configured and validated document trails across Purchase Requisitions (`ME51N`), RFQs (`ME41`), Quotation Comparisons (`ME49`), Purchase Orders (`ME21N`), Goods Receipts (`MIGO`), and Invoice Verifications (`MIRO`).
* **Pricing & Approvals:** Configured a custom pricing procedure (`ZDM01`) using the condition technique (Gross, Discount, Freight) and built a 4-level classification-based approval release strategy for purchasing documents.
* **Automated Replenishment:** Set up basic `MRP Live` planning runs linked to automatic Purchase Order conversion (`ME59N`) via maintained Source Lists and Info Records.

---

## 📊 3. Valuation & Finance Integration (`OBYC`)
Configured automatic account determination to ensure seamless integration between Logistics (MM) and Financial Accounting (FI):
* **Core Postings:** Mapped standard valuation classes for raw materials, semi-finished items, and finished goods to their respective G/L accounts using transaction keys **BSX** (Inventory) and **WRX** (GR/IR Clearing).
* **Price & Variance Controls:** Configured **PRD** (Price Differences) and **GBB** (Offsetting Entries) rules to handle consumption to production orders and cost centers automatically.
* **Material Ledger & Special Procurement:** Activated standard multi-currency inventory valuation (EUR/USD parallel tracking) and validated sandbox processes for Stock Transport Orders (STO), Subcontracting, and Vendor Consignment.

---

## 🛠️ 4. Functional Support & Troubleshooting Simulation
Documented resolution steps for common Level 2/Level 3 end-user configuration issues inside the sandbox, focusing on:
* Resolving price and quantity mismatches on the GR/IR clearing account (`MB5S` / `MR11`).
* Debugging characteristic allocation errors that lock or break purchasing release workflows.
* Tracking pricing condition logic issues using access sequence analysis.

---

## 📂 Documentation & Portfolio Files
* 📄 `SAP_S4HANA_MM_Configuration_Blueprint.pdf` -> Full functional configuration maps.
* 📄 `P2P_Execution_Log_and_Validation.pdf` -> Transactional test scripts and system logs.
