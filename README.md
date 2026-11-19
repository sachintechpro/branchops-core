# BranchOps Core

**Company operating system and job orchestration prototype** for a residential windows-and-doors retail, supply and installation business.

BranchOps Core is the host company's internal system of record for job operations. It coordinates employees, customers, external service providers, documents, schedules, financial checkpoints and workflow events around a shared Job ID.

## Role-based experience

- **Business Owner / CEO — Master Control Panel:** company-wide job board, portfolio visibility, financial activation status, exceptions and operational oversight.
- **Project Manager / Sales / Support — Operations Control Panel:** job queue, next workflow gates, customer and partner coordination, communications and exceptions.
- **External partners — task-specific smart-app concepts:** measurement capture, installation completion and delivery/receiving evidence. These are not internal BranchOps accounts or access to company dashboards. A production implementation should use narrowly scoped, expiring task links and server-side authorization.

The prototype includes drill-down into the existing detailed job execution workspace.

## Job lifecycle

1. Measurement verification
2. Procurement and supplier confirmation
3. Warehouse receiving and inspection
4. Installation planning and execution
5. Final inspection and closeout
6. Financial and document closeout
7. Warranty
8. Completion and archive

A job must not be activated until the signed agreement and confirmed/cleared 30% advance payment are recorded. The current bank confirmation and reconciliation controls are simulated manual steps, not a bank integration.

## Coordination and audit concepts

The detailed job workspace supports recording PM decisions, stage notes, exceptions, communications and activity. The intended production platform will also capture email/SMS, DocuSign, scheduling, payment, vendor and delivery events in a centralized, append-only audit history.

## Run the prototype

Open the GitHub Pages site or open `index.html` in a browser. Use the role tabs to switch between the owner view, operations view and external smart-app concepts. Select a job to open its detailed execution workspace.

Browser local storage preserves prototype state on the same browser/device. Metrics are calculated from the seeded/local job records; they are not live business reporting.

## Production architecture — not yet connected

The intended architecture is company-controlled and API-first:

- Google Workspace identity, Drive, Gmail and Calendar integrations.
- DocuSign for contract envelopes and signature evidence.
- Payment/accounting/banking integrations for verified receipts and reconciliation.
- Email and SMS providers for consent-aware two-way communication.
- Supplier, shipping, routing and scheduling integrations where APIs are available.
- Central backend, database, event processing, webhook verification, notification delivery and immutable audit history.

Company documents should remain in the host company's Google Drive where possible, with BranchOps storing secure references and metadata. External services will necessarily process the minimum information needed to provide their service; production data governance, retention and security controls must be configured explicitly.

**Important prototype boundary:** this is a front-end demonstration. It does not provide real authentication, role enforcement, shared multi-user storage, secure external task links, camera measurement/AI, real file uploads, email/SMS delivery, DocuSign, bank feeds, supplier APIs or live scheduling. Role switching is for demonstration only. Do not enter real customer, financial or confidential information.

## Deploy on GitHub Pages

Repository Settings → Pages → Deploy from a branch → `main` → `/(root)`.
