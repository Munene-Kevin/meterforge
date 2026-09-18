Deployment & Ops notes

- Support horizontal scaling: make Tenant Service stateless; store state in DB and object stores
- Per-tenant failover: use region/zone-aware configuration in tenant metadata
- Backups: per-tenant backup objects stored with tenant id prefix and encrypted with tenant KMS key
