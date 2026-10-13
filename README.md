# Laba Nice Day Laundry Management System

A browser-based laundry shop management system designed around the
actual day-to-day workflow of **Laba Nice Day**.

The project currently serves as a functional public demo and prototype
for testing shop operations, refining workflows, and gathering feedback
before development of the production system.

## 🧾 Orders & Transactions

-   Create orders for walk-in and returning customers.
-   Save customer name, contact number, address, and transaction
    history.
-   Support multiple services and multiple physical laundry loads in one
    transaction.
-   Track Cash and GCash payments separately.
-   Show detailed charge and payment breakdowns.
-   Add charges such as Extra Dry after the original transaction.
-   Prevent release when there is an unpaid balance.
-   Support controlled transaction cancellation and amendment.
-   Require Owner/Admin approval for discounts, cancellations, and
    amendments.
-   Keep an audit trail instead of deleting transaction history.
-   Show concise load progress such as Washed, Waiting for Dryer,
    Drying, Waiting for Folding, and Ready.

## 🧺 Load Management

-   Treat each physical laundry load separately from the customer
    transaction.
-   One transaction can contain several loads.
-   Track each load through Washing, Drying, Folding, and Ready for
    Release.
-   Assign individual loads to washers and dryers.
-   Automatically queue loads when no compatible machine is available.
-   Mark selected queued loads as Priority without changing their
    visible queue order.
-   Process multiple loads efficiently using batch machine assignment.
-   Prevent the same machine from being assigned to two loads at once.

## 🫧 Detergent & Fabric Conditioner

-   Select the detergent and fabric conditioner used for each load.
-   Set default products for faster order entry.
-   Apply the same supplies to several loads at once.
-   Override supplies for individual loads when needed.
-   Support customer-provided detergent or fabric conditioner.
-   Avoid deducting shop inventory when the customer provides the
    product.
-   Demo inventory includes familiar product examples from brands such
    as Ariel, Breeze, Surf, Downy, and Del.

## 📦 Inventory Management

-   Track different detergent and fabric conditioner products.
-   Track liquid inventory in mL.
-   Track laundry bags by piece.
-   Receive stock using different package sizes such as bottles and
    pouches.
-   Track unopened stock, opened stock, and supplies transferred to
    dispensers.
-   Maintain dispensing containers separately from reserve inventory.
-   Make dispenser capacity optional.
-   View complete inventory movement history.

## ⚗️ Automatic Consumable Usage

-   Configure detergent and fabric conditioner usage per service.
-   Allow Standard Full Service, Heavy/Bulky, Comforter, and other
    services to use different amounts.
-   Support weight-based consumption rules.
-   Automatically deduct shop supplies when a load starts washing.
-   Override the normal amount for unusual loads.
-   Require a reason for consumable overrides and record it in the audit
    log.
-   Flag inventory discrepancies without preventing shop operations.

## ⚠️ Inventory Alerts

-   Configure optional low-refill alerts for dispensing containers.
-   Configure reorder/low-stock alerts for inventory products.
-   Identify empty or insufficient recorded stock.
-   Allow physical inventory corrections with a recorded reason.
-   Keep adjustments fully traceable through inventory and audit
    history.

## 🧼 Machine Operations

-   Configure washers and dryers individually.
-   Track machine availability and current loads.
-   Display elapsed cycle time and estimated remaining time.
-   Flag cycles running longer than expected.
-   Mark machines as non-operational with a reason.
-   Exclude unavailable machines from load assignment.
-   Show active laundry directly inside the machine cards.
-   Allow staff to work either from the load queue or from an available
    machine.

## ⏱️ Queues & Shop Workflow

-   Maintain separate Wash, Dry, and Folding queues.
-   Show actionable queue counts in Operations.
-   Automatically queue loads when all compatible machines are occupied.
-   Mark a waiting load as Priority without visually moving it to the
    top of the queue.
-   Show transactions that are ready for customer release.
-   Release all completed loads belonging to a transaction together.

## ➕ Extra Services

-   Add Extra Rinse to an active washing load.
-   Add Extra Dry to an active drying load.
-   Extend the existing machine cycle instead of creating another
    physical load.
-   Add the extra charge to the existing transaction.
-   Allow the additional charge to be paid before customer release.

## 🏢 Bulk & Advanced Orders

-   Support Business / Establishment customers.
-   Create bulk orders using total laundry weight.
-   Let the system suggest how the order should be divided into physical
    loads.
-   Allow staff to adjust the suggested load sizes before confirming.
-   Price the order based on the confirmed physical loads.
-   Track every resulting load separately while keeping them under one
    customer transaction.
-   Support categories such as towels, sheets, curtains, and other
    establishment laundry.

## 🚚 Pickup & Delivery

-   Support customer drop-off, shop pickup, customer collection, and
    delivery workflows.
-   Save delivery/pickup addresses with the transaction.
-   Track pickup and delivery status from Operations.
-   Open Google Maps with driving directions to the customer's address.
-   Support configurable delivery distance zones and charges.
-   Keep pickup and delivery status changes in the audit trail.

## 💳 GCash Workflow

-   Support a simulated GCash payment workflow in the public demo.
-   Record GCash reference numbers.
-   Capture/upload payment proof.
-   Compress payment images before browser storage.
-   Remind staff to verify that payment was actually received.
-   Do not treat screenshots alone as proof of successful payment.

> The public GitHub demo uses a fake payment QR and must not be used for
> real payments.

## 👥 Customers

-   Save customer information for future transactions.
-   Require customer name and contact number.
-   Store address when provided.
-   Support individual and business customers.
-   Allow Owner/Admin customer editing.
-   Record customer information changes in the audit trail.

## 🔐 Controls & Audit Trail

-   Maintain a detailed audit history of important actions.
-   Track transaction creation, payments, amendments, cancellations,
    discounts, machine actions, inventory changes, consumable overrides,
    and data repairs.
-   Require Owner/Admin approval or passcode for controlled actions.
-   Keep historical actions instead of silently overwriting or deleting
    records.
-   Export audit history to CSV.

## 🛠️ Data Integrity & Recovery

-   Automatically reconcile load status with Wash, Dry, and Folding
    queues.
-   Repair missing queue entries when a waiting load is found outside
    its expected queue.
-   Remove stale or duplicate queue references where they can be safely
    resolved.
-   Validate and reconcile data after restoring older backups.
-   Use previous stage progress when repairing older load records.
-   Detect conflicting machine assignments and flag them for Owner
    attention instead of silently guessing.
-   Provide **Check & Repair Data** for manual integrity checks.
-   Record automatic repairs and integrity warnings in the audit log.

## 📊 Owner Dashboard & Reports

-   View sales and payment summaries.
-   Monitor machine status.
-   Review current shop operations.
-   Track active and completed loads.
-   Export sales summaries to CSV.
-   Export detailed transaction/load data to CSV.
-   Export audit logs to CSV.

## 💾 Browser Storage & Backups

The current public demo is browser-based.

-   Data is stored locally on each tester's device.
-   Data is **not synchronized between devices**.
-   Different testers have independent demo data.
-   Application data can be exported and restored using backups.
-   Restored data is validated and reconciled before normal operations
    continue.
-   The browser prototype is intended for workflow testing and
    validation, not as the final production database.

## 🌐 Public Demo

The current demo is available through GitHub Pages:

https://rbcepres.github.io/laba-nice-day-demo/

The demo can be tested from Android, iPhone, Windows, and macOS using a
modern browser.

### Demo Limitations

-   No centralized database yet.
-   No real multi-device synchronization.
-   No production authentication system yet.
-   GCash integration is simulated.
-   Machine activity is currently entered manually.
-   ESP32-based physical machine monitoring is planned for a later
    stage.
-   The public demo should not contain real customer or payment
    information.

## 🚧 Planned Production Architecture

The prototype is being used to validate the shop workflow before
building the production application.

Planned stack:

-   React + TypeScript frontend
-   FastAPI backend
-   PostgreSQL database
-   SQLAlchemy data layer
-   Local-first shop server
-   Centralized multi-device data
-   User accounts and role-based permissions
-   ESP32 machine monitoring
-   MQTT machine telemetry
-   Automated backups and reporting

## 🎯 Project Goal

The goal is not simply to create a generic POS.

The system is being designed specifically around laundry operations:

**Customer → Transaction → Physical Loads → Machines & Queues → Folding
→ Payment → Release**

The long-term goal is to connect the software workflow with actual
machine activity, inventory consumption, payments, and shop operations
while keeping the attendant workflow simple and fast.

------------------------------------------------------------------------

**Developed by:** Ronald Cepres\
**Email:** rbcepres@gmail.com
