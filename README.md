# Laba Nice Day — Demo

Browser-based workflow prototype for the Laba Nice Day laundry management system. The Demo validates real shop operations before the production React/FastAPI/PostgreSQL application is built.

## Core workflow

Customer → Transaction → Physical Loads → Wash / Dry / Fold → Payment → Release

Physical loads are independent operational units. A transaction may contain multiple loads and mixed service types. Human-friendly labels such as `#1054-A` are used for physical identification, while service type and optional load notes remain visible in operational views.

## Current capabilities

- Customer and transaction creation, including Regular/Establishment and Standard/Bulk classifications.
- Drop-off, shop pickup, customer pickup, and shop delivery workflows.
- Configurable services, pricing, wash-service supply requirements, and consumable quantities.
- Mixed-service load handling with washer and dryer assignment in one assignment flow.
- Auto-fill machine assignment with manual review and queue fallback.
- Wash, Dry, and Folding queues; priority marking; machine timers; Extra Rinse and Extra Dry.
- Inventory products, containers, stock receipt, movements, adjustments, alerts, and per-load consumable selection.
- Cash and simulated GCash payment workflows.
- Receipt and physical load-label print preview with 58mm and 80mm paper settings.
- Users & Access with System Administrator, Owner, Manager, and Attendant roles.
- Audit logging, browser backup/restore, CSV exports, deterministic Demo reset, and operational data reconciliation.

## Demo accounts

- Demo Sys Admin User — PIN `0987`
- Demo Owner User — PIN `5678`
- Demo Attendant User — PIN `1234`

Manager is an available role but is not seeded by default.

## Browser data

The Demo stores data locally in the browser. Data is not synchronized between devices or testers. Export a backup before installing a new Demo version if the current test data matters.

`Reset Demo Data` creates one deterministic default state. `Check & Repair Data` is intended for operational inconsistencies such as queue membership and machine assignments, not for silently recreating missing core collections.

## Printing

Printing uses an in-app preview followed by the browser print flow. Receipt and load-label output supports 58mm and 80mm paper widths. Automatic printing is off by default. The printing foundation is intentionally transport-independent so production can later support browser, ESC/POS, USB, LAN, or server print transports.

## Demo limitations

- No centralized database or multi-device synchronization.
- Browser-local authentication is not production-grade security.
- GCash is simulated; the shared Demo must never contain real payment QR/details.
- Machine activity is entered manually.
- ESP32/MQTT monitoring and production deployment are future work.

## Planned production architecture

- React + TypeScript frontend
- FastAPI + Python backend
- SQLAlchemy
- PostgreSQL
- LAN-first shop server
- Backend-enforced permissions and append-oriented audit logging
- ESP32 + MQTT machine telemetry

The production system will treat load workflow state as authoritative. Individual machine tracking is planned as an optional operational capability rather than a prerequisite for load progression.

## Demo

GitHub Pages is the canonical Demo deployment:

https://rbcepres.github.io/laba-nice-day-demo/

## Developer

Ronald Cepres  
rbcepres@gmail.com
