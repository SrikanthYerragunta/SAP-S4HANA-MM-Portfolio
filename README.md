SAP S/4HANA MM: Complete Functional Configuration Documentation

This repository contains the functional documentation and process verification logs for Düsseldorf Manufacturing AG (DMAG), a fictional sandbox based SAP S/4HANA practice project created for learning and demonstration purposes.

The documents show how I set up the organizational structure, extended master data, executed business processes, and handled financial integration in a test environment.

📂 Portfolio Structure and Scope

The portfolio is divided into three documents, plus one combined version.

📘 Complete Portfolio (all three parts in one file)

📄 Part 1: MM Configuration Portfolio

The basic organizational setup and system parameters for the business scenario:

Enterprise Structure: Company Code, Plants (Düsseldorf, Dortmund, Stuttgart), Storage Locations, and a Central Purchasing Organization.
Master Data Maintenance: Material Master settings for raw materials, semi finished items, and finished goods, along with Business Partner supplier setup.
Purchasing Controls: A custom pricing schema and multi level release strategies for purchase orders.
Logistics Scope: Automated replenishment planning, Stock Transport Orders, Vendor Consignment, Subcontracting, Batch Management, Split Valuation by quality grade, and Physical Inventory cycles.

📄 Part 2: P2P End to End Cycle

The standard transactional flow and user steps verified in the test environment:

Business Flow: Purchase Requisition, Request for Quotation, Quotation Maintenance, Price Comparison, Info Record, Purchase Order, Goods Receipt, and Invoice Verification.
Additional Scenarios: Value Contracts, Scheduling Agreements, automated PO conversion, Parked Invoices, and Quota Arrangements.
Functional Troubleshooting: GR/IR quantity or value mismatches, workflow approval blocks, pricing calculation errors, and invoice blocks.

📄 Part 3: Material Ledger and OBYC

Material valuation, financial integration, and month end processing:

Material Ledger Setup: Multi currency inventory valuation in local currency (EUR) and group currency (USD).
Actual Costing: Month end variance accumulation, revaluation, and cost analysis.
Automatic Account Determination: Linking materials and stock movements to G/L accounts using transaction keys BSX, WRX, PRD, GBB, FRE, KON, and INV.
Month End Sequence: The processing order from clearing reviews to final costing execution.
👤 About Me

SAP S/4HANA MM (Sourcing & Procurement) consultant in transition, with SAP Ariba as a secondary focus, building on 15+ years of enterprise client engagement in IT services.
