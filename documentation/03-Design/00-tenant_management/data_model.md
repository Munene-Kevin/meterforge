Data Model (high level)

Tenant:
- id (UUID)
- name
- tier
- tenancy_mode (shared-schema | isolated-schema | isolated-instance)
- quotas {cpu, storage, api_throughput}
- kms_key_id
- created_at, updated_at

Notes:
- For shared-schema mode, tenant_id is included in tenant-scoped tables.
- For isolated-schema/instance, separate DB/schema references are stored in tenant metadata.
