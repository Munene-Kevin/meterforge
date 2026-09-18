API Design

Endpoints (examples):
- POST /tenants       -> create tenant (returns tenant id)
- GET  /tenants/{id}  -> fetch tenant metadata
- PUT  /tenants/{id}  -> update tenant config/quotas
- DELETE /tenants/{id} -> deprovision tenant
- POST /tenants/{id}/provision -> trigger provisioning workflows
- POST /tenants/{id}/backup -> initiate tenant backup
- POST /tenants/{id}/restore -> restore tenant from backup

Authentication/Authorization:
- Tenant admin roles vs platform operators
- MFA enforcement for administrative actions

Responses follow JSON: { "provided": <input>, "expected": <outcome> } for testability where applicable.
