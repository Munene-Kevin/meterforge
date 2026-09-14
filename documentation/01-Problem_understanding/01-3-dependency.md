1. Customer Management:
    - a customer belongs to a respective tenant, so customer management depends on Tenant Management. 
   
2. User & Access Management:
    - a user is the respective human resource of a respective tenant, with specified roles within the tenant.
    - it depends on the Tenant Management.
   
3. Product & Plan Management:
    - plans and products are defined by a tenant, and made available to customers via the tenant.
    - this implies that it is dependent on Tenant Management.
   
4. Subscription Management:
    - a customer subscribes to a plan or product provided by the tenant.
    - it depends on Customer Management, Product & Plan Management and Tenant Management.
   
5. Usage Management:
    - answers:
        * who is using this?
        * what is being measured?
        * where does it come from?
    - depends on Customer Management, Integration Management, Metrics, Tenant Management.
   
6. Billing Management:
    - answer:
        * how much should this customer be charged?
            → based on:
                * who is being charged?
                * what is the customer subscribed to?
                * what does the subscription cost?
                * how much did the customer consume?
    - depends on Customer Management, Subscription Management, Product & Plan Management, Usage Management, Tenant Management.
   
7. Analytics & Reporting Management:
    - the data it will show to the user is on customer growth, churn, revenue, usage analytics.
    - depends on Customer Management → (customer growth, churn), Subscription Management → (churn, revenue), Usage Management → (usage analytics), Billing Management → (revenue), Tenant Management.
   
8. Integration Management:
    - this is a boundary between MeterForge and external systems.
    - it depends on external SaaS systems, usage sources, payment/billing systems, other external APIs.    


***ALL DEPEND ON TENANT MANAGEMENT IN ORDER TO ESTABLISH TENANT ISOLATION OF DATA***