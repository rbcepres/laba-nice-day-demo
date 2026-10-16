# Laba Nice Day Laundry Management System

Laba Nice Day Laundry Management System is a browser-based demo for managing a laundry shop from customer intake through load processing, payment, and release. It demonstrates a practical counter and operations workflow for attendants while also providing management, configuration, reporting, and access-control features.

## Try the Demo

https://rbcepres.github.io/laba-nice-day-demo/

The demo stores its data in the browser. Use sample information only; do not enter real customer or payment data.

## Capabilities

### Orders and customers
- Create orders for new and returning customers.
- Record contact and pickup/delivery information.
- Support multiple services and multiple physical loads in one transaction.
- Review transaction details, charges, payments, balances, and progress.
- Maintain customer history for repeat visits.

### Laundry load workflow
- Track individual loads through washing, drying, folding, and ready-for-release stages.
- Support Full Service, Wash Only, Dry Only, and configurable service workflows.
- Assign compatible washers and dryers to eligible loads.
- Queue loads when machines are unavailable and support priority handling.
- Review and label multiple loads belonging to the same transaction.
- Record detergent, fabric conditioner, load weight, and optional load notes where applicable.

### Machines and operations
- View washer and dryer availability and active work from Operations.
- Assign loads manually or use Auto-fill to assign eligible waiting loads.
- Track cycle progress and extend active rinse/dry work when required.
- Provide an owner-facing operations snapshot.

### Payments and transaction controls
- Record Cash and GCash payment information supported by the current demo workflow.
- Show subtotal, discounts, additional charges, total, payment, and balance information.
- Prevent release when an outstanding balance remains.
- Support controlled discounts, amendments, cancellations, and other protected actions based on user permissions.

### Receipt and load-label printing
- Preview receipts and load labels before printing.
- Print directly to a supported Bluetooth ESC/POS thermal printer where Web Bluetooth is available.
- Use browser/system printing as a fallback.
- Configure receipt shop information and default receipt-copy count.
- Adjust receipt copies from the print preview.
- Reprint receipts with clear reprint identification and audit recording.
- Offer receipt and load-label previews automatically after a new order when enabled.
- Open a connected printer-driven cash drawer automatically when a newly confirmed order is paid in Cash.

### Inventory and supplies
- Maintain laundry products and supply information.
- Configure default detergent and fabric conditioner selections.
- Associate applicable consumables with individual loads.
- Track inventory activity through the demo management workflow.

### Users and permissions
- Support System Administrator, Owner, Manager, and Attendant roles.
- Switch users, lock the application, and track local demo shifts.
- Require an authorized user's PIN for protected actions.
- Configure role permissions and manage users from the administration interface.

### Dashboard, history, and data tools
- View sales, transaction, payment, and operations summaries.
- Review transaction history and audit activity.
- Export demo backups and CSV reports.
- Restore compatible demo backups and use built-in data/installation repair tools.

## Demo Accounts

- **Demo Sys Admin User** — PIN `0987`
- **Demo Owner User** — PIN `5678`
- **Demo Attendant User** — PIN `1234`

No Manager account is seeded by default, but an authorized user can create one in Users & Access.

## Demo Notes

This is a functional browser prototype, not the final production deployment. Data, authentication, permissions, and uploaded proof images are stored locally in the browser and are intended for workflow demonstration rather than production security. Hardware-dependent capabilities such as Bluetooth printing depend on browser, device, and printer compatibility.

## Developer

Ronald Cepres  
rbcepres@gmail.com
