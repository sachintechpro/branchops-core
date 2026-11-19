# BranchOps Core

**Interactive branch operations and job-execution simulator** for a residential windows-and-doors supply and installation business.

BranchOps Core is the branch's operational workspace after a signed agreement and cleared 30% advance payment. It follows each job from measurement verification through procurement, receiving, installation, inspection, financial closeout and warranty activation.

## Run the simulation

Open the GitHub Pages site or open `index.html` in a browser. Select a job and work through the lifecycle in order.

### Simulated end-to-end workflow
1. Measurement verification — site dimensions, product configuration, constraints and customer approval.
2. Procurement — purchase order, supplier acknowledgement, product details and lead-time confirmation.
3. Warehouse — delivery booking, goods receipt, quantity reconciliation, inspection, damage/shortage records and job allocation.
4. Installation — work order, crew booking, customer access, material pick, pre-start and installation completion.
5. Final inspection — workmanship checks, snag ownership and closure, site clean-up and customer acceptance.
6. Financial and document closeout — invoice reconciliation, outstanding balance, manuals, supplier warranties and closeout approval.
7. Warranty — product registration, workmanship coverage, exclusions, homeowner warranty pack and service contact.
8. Job completion — exception disposition and archive.

## PM and stakeholder capabilities
- Complete individual workflow tasks and advance only when the stage checklist is complete.
- Record PM decisions, stage notes and job activity.
- Raise exceptions with category, impact, accountable owner, mitigation and target date.
- Record PM responses and dispositions: resolved, transferred/monitored, or awaiting external response.
- Record inbound/outbound stakeholder communications by email, SMS, phone or internal handoff.
- Track communications with homeowner, measurement technician, supplier, warehouse, installation crew, finance, inspector and branch owner.
- Switch between seeded jobs and reset a scenario for another walkthrough.
- See illustrative benchmark targets in the KPI tooltips; these are planning examples, not industry guarantees or live measured performance.
- Browser local storage preserves the simulation on the same device/browser. No shared database is connected.

## Product boundaries
- **BranchOps Customer** — homeowner-facing quote, proposal and acceptance journey.
- **BranchOps Core** — branch operations, job state, PM decisions, approvals and execution.
- **BranchOps Partner** — supplier, warehouse, field and installation partner workflows.

The intended integration model is shared Job IDs with API/event-based handoffs. This build is a front-end simulation. It does not send real messages, create supplier orders, collect payments, register actual warranties, or integrate with the other apps.

## Activation rule
A job must not be activated until both the signed agreement and confirmed/cleared 30% advance payment are recorded.

## Deploy on GitHub Pages
Repository Settings → Pages → Deploy from a branch → `main` → `/(root)`.

## Deploy on Render (optional)
Use a Static Site with blank build command and publish directory `.`.
