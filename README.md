# BranchOps Core

**Branch operations control room** for a residential windows-and-doors sales, supply and installation business.

BranchOps Core is the operational system of record after the customer has signed the agreement and the **30% advance payment has cleared**. It coordinates job progress, dependencies and exceptions through closeout.

## Product boundaries
- **BranchOps Customer** — homeowner-facing quote, proposal and acceptance journey.
- **BranchOps Core** — branch operations, authoritative job state, approvals and job execution.
- **BranchOps Partner** — supplier, warehouse, field and installation partner workflows.

The intended integration model is shared Job IDs with API/event-based handoffs. This initial build is a standalone front-end workspace with local sample data; it does not yet connect to the other apps or external payment, e-signature, messaging, inventory or supplier systems.

## Included
- Dark metallic operations control-room interface.
- Active job board with search and stage/priority filters.
- Job detail workspace with lifecycle progress.
- Exception and approval queue.
- Local stage progression and follow-up review interactions.
- CSV export and responsive layout.

## Run locally
Open `index.html` in a browser.

## Deploy on Render
Create a **Static Site** connected to this repository:
- Build command: leave blank
- Publish directory: `.`

No backend or environment variables are required for this front-end build.

## Activation rule
A job must not be activated until both the signed agreement and confirmed/cleared 30% advance payment are recorded.
