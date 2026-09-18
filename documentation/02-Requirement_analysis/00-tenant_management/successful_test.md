# Tenant Management - Successful Test Cases

TM-01: Data Isolation
Description: Verify tenant data isolation across network, application, and persistence layers.
Provided: Tenant A creates a resource (API object and DB row). Tenant B attempts to access the same resource via API and direct DB query.
Expected: Tenant B receives authorization error (403) or no data returned; logs show enforcement at application/persistence layers and network isolation rules applied.

TM-02: Administrative Security
Description: Verify tenant administrative access requires MFA and per-tenant KMS support.
Provided: Admin account enabled for Tenant X with MFA configured; encrypted tenant-specific secret stored in KMS.
Expected: Administrative login requires second factor; secrets can only be decrypted with tenant-specific KMS key and access is logged.

TM-03: Scalability & Quotas
Description: Verify horizontal scaling and per-tenant quotas enforcement.
Provided: Simulated load representing 10,000 tenants with quota-exceeding requests from Tenant Y for CPU, storage, and API throughput.
Expected: Platform scales (additional instances/nodes launched or capacity applied) and Tenant Y receives quota limit responses when exceeding configured quotas; other tenants unaffected.

TM-04: Performance
Description: Verify API latency and provisioning time per tenant.
Provided: Normal load scenario per tenant; 1000 sample API requests and a tenant provisioning request.
Expected: Median API latency < 200 ms, 95th percentile < 1 s; tenant provisioning completes within 60 seconds.

TM-05: Availability
Description: Verify uptime targets and per-tenant failover.
Provided: Planned maintenance and simulated node failure affecting a subset of instances serving Tenant Z.
Expected: Platform availability remains within SLA (99.95% annualized for test window) and Tenant Z traffic fails over to alternate instance or region with minimal impact per documented strategy.

TM-06: Compliance & Data Governance
Description: Verify per-tenant retention, export, and irreversible deletion; audit log retention.
Provided: Tenant requests data export and deletion; audit logs for admin actions exist for >1 year.
Expected: Exported data matches tenant data; irreversible deletion removes tenant data from active and backup stores per policy; audit logs remain tamper-evident and retrievable for ≥1 year.

TM-07: Observability & Monitoring
Description: Verify per-tenant metrics, logs, and tenant-scoped alerts/dashboards.
Provided: Tenants emit errors and latency spikes; an alert rule configured for Tenant Q.
Expected: Metrics and logs are visible scoped to Tenant Q; alert triggers and dashboard shows tenant-specific panels.

TM-08: Backup & Restore
Description: Verify per-tenant backup and restore with RPO/RTO constraints.
Provided: Tenant backup created; simulated failure with restore request for Tenant M.
Expected: Restore succeeds from backup within defined RTO for that tier and data loss does not exceed 24-hour RPO; backups are encrypted and isolated.

TM-09: Multi-tenancy Modes
Description: Verify support for shared-schema, isolated-schema, and isolated-instance modes.
Provided: Three tenants configured each with different tenancy modes performing typical operations.
Expected: Each tenant operates correctly within its mode; isolation and performance characteristics match mode expectations.

TM-10: Rate Limiting & Quotas Behavior
Description: Verify per-tenant rate limiting returns correct error responses.
Provided: Tenant S issues requests that exceed configured rate limit.
Expected: Excess requests receive standardized rate-limit responses (HTTP 429) with informative headers/body and normal requests are unaffected.

TM-11: Auditability & Traceability
Description: Verify traceability of cross-tenant operations and audit tools.
Provided: An operator performs a cross-tenant administrative action affecting Tenant R.
Expected: Action is recorded with tenant context, operator identity, timestamp, and is queryable via audit tools; trace links operations to affected tenants.

TM-12: Maintainability & Per-tenant Migrations
Description: Verify tenant configuration changes and per-tenant schema migrations.
Provided: Apply configuration change for Tenant V and run a per-tenant schema migration.
Expected: Configuration applies without full-system redeploy; migration completes for Tenant V without impacting others and can be rolled back if needed.

