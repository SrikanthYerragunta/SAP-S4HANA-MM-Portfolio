# SAP S/4HANA Materials Management (MM) Functional Portfolio

## 🏢 Enterprise Scenario: Düsseldorf Manufacturing AG
This repository documents a complete, end-to-end sandbox implementation mirroring a multi-plant German manufacturing scenario. Built using **SAP Best Practices** and **SAP Activate** methodologies, this project demonstrates hands-on configuration across Sourcing, Procurement, Inventory Management, and Finance integration.

---

## 🏗️ 1. Enterprise Structure Mapping
The organizational hierarchy is designed to support regional supply chain operations in Germany with localized valuation loops:
* **Company Code:** `1000` (DE Legal Entity)
* **Manufacturing Plants:** `DM01` (Düsseldorf - Main), `DM02` (Dortmund - Production), `DM03` (Stuttgart - Logistics Hub)
* **Purchasing Structure:** 1 Central Purchasing Organization, 3 Plant-specific Purchasing Groups.

---

## 🔄 2. Procure-to-Pay (P2P) Workflows & System Controls
The core logistics cycle maps the entire document trail from requirement generation to final financial settlement:
`Purchase Requisition (PR)` ➡️ `RFQ & Quotation Analysis` ➡️ `Purchase Order (PO)` ➡️ `Goods Receipt (MIGO)` ➡️ `Invoice Verification (MIRO)`

* **Approval Governance:** Configured a 4-level classification-based release strategy for purchasing documents using traits via `CL02` and `CT04` transactions, ensuring structured compliance thresholds.
* **Automated Replenishment:** Configured `MRP Live` workflows paired with automatic Purchase Order conversion (`ME59N`) utilizing maintained Source Lists and Info Records.

---

## 📊 3. Valuation & Cross-Module FI-MM Integration (`OBYC`)
To ensure seamless financial settlement and eliminate transactional posting errors, automatic account determination links have been configured as follows:


| Transaction (Event Key) | Account Modification | Valuation Class | Target G/L Account | Description |
| :--- | :--- | :--- | :--- | :--- |
| **BSX** | *None* | 3000 | 200100 | Raw Materials Stock Account |
| **WRX** | *None* | 3000 | 211200 | GR/IR Clearing Account |
| **PRD** | PRA | 3000 | 400300 | Cost (Price) Differences Account |
| **UMB** | *None* | 3000 | 400400 | Gain/Loss from Revaluation |

* **Material Ledger Activation:** Configured actual costing architecture moving dynamically across parallel currencies (**EUR** and **USD**) to model multi-currency corporate consolidation.
* **Special Procurement Structures:** Validated operating loops for multi-plant Stock Transport Orders (STO), Subcontracting processes (featuring Bill of Materials explosions via movement types `541`/`543`), and Consignment processing verified through `MRKO` settlements.

---

## 🛠️ L2/L3 Functional Support & Troubleshooting Framework
This landscape includes full structural resolution paths for common implementation issues:
1. **GR/IR Quantity/Price Mismatches:** Resolution steps for price variances exceeding tolerance limits (`OMR6`) causing `MIRO` blockages.
2. **Release Strategy Deadlocks:** Debugging missing characteristic valuations preventing PO routing workflows.
3. **Split Valuation Failures:** Managing inventory ledger corrections across unique batch quality segments.

---

## 📂 Repository Contents
* `Dusseldorf_Manufacturing_AG_Blueprint.pdf` -> Full functional specification map.
* `Configuration_Tables_Matrix.xlsx` -> Complete blueprint data spreadsheets.
