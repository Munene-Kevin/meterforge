1. Tenant
    → A SaaS company using MeterForge.
    → MeterForge is a multi-tenant system, meaning that each tenant has its own isolated environment and data. Each tenant can have multiple users, and each user can have different roles and permissions within the tenant's environment.
2. User
    → An individual belonging to a tenant, who uses the MeterForge platform.
    → Users can have different roles and permissions within their tenant's environment.
3. Role
    → Defines the level of access and permissions a user has within a tenant's environment.
    → Roles can be assigned to users to control what actions they can perform and what data they can access.
4. Customer
    → A customer is an entity that a tenant serves or manages within the MeterForge platform.
    → Customers can have associated data, such as usage metrics, billing information, and service configurations.
5. Plan
    → A subscription plan that a tenant can choose for their MeterForge account.
    → A plan can define things such as price, billing period, included usage, usage limits, features.
6. Pricing 
    → Pricing represents how a tenant charges for its plans usage.
    → MeterForge is particularly concerned with usage-based and subscription-related billing, so pricing becomes an important domain concept.
7. Subscription
    → A subscription represents a customer's active engagement with a tenant's plan.
    → Subscriptions can have associated data, such as start and end dates, billing cycles, and usage metrics.
    → The subscription has a lifecycle, such as:
                      Trial → Active → Past Due → Canceled
8. Usage
    → Usage represents the consumption of resources or services by a customer within a tenant's environment.
    → eg; API calls, storage, compute hours, transactions, etc.
    → Usage data can be collected and analyzed to determine billing, performance, and resource allocation.
9. Usage Event
    → A usage event represents a specific instance of resource consumption by a customer.
    → Usage events can be recorded and processed to calculate usage metrics, billing, and performance analysis.
    → Many usage events can belong to one customer.
10. Metric
    → A metric represents a specific measurement or data point related to usage, performance, or other aspects of the MeterForge platform.
    → Metrics can be used to monitor system health, track performance, and inform decision-making.
11. Billing Period
    → Defines the time frame for which usage and billing are calculated for a subscription.
12. Invoice
    → An invoice represents a billing statement generated for a customer based on their subscription and usage.
    → Invoices can include details such as usage charges, plan fees, taxes, and payment information.
13. Payment
    → A payment represents a transaction made by a customer to settle their invoice.
    → Payments can be processed through various payment methods and can have associated data, such as payment status, amount, and date.
    → Payment system is an external system that is integrated with MeterForge to handle payment processing, such as Stripe, PayPal, or other payment gateways.
14. Revenue 
    → Revenue recognition is the process of recognizing revenue from customer subscriptions and usage in accordance with accounting standards.
    → MeterForge needs to ensure that revenue is recognized accurately and in a timely manner, based on the subscription and usage data.
    → MeterForge may derive metrics such as: monthly recurring revenue, revenue growth, revenue per customer, revenue by plan.
15. Churn
    → Churn represents the loss of customers or subscriptions over time.
    → MeterForge needs to track churn metrics to understand customer retention, identify potential issues, and inform business decisions.
    → Churn can be calculated based on subscription cancellations, non-renewals, or other factors that indicate a customer is no longer engaged with the platform.
16. Customer Growth
    → Customer growth represents the increase in the number of customers or subscriptions over time.
    → MeterForge needs to track customer growth metrics to understand market adoption, identify trends, and inform business decisions.
    → Customer growth can be calculated based on new subscriptions, upgrades, or other factors that indicate a customer is actively engaged with the platform.
17. Aggregated Usage
    → Aggregated usage represents the total consumption of resources or services by a customer or tenant over a specific time period.
    → Aggregated usage data can be used for billing, performance analysis, and resource allocation.
    → Aggregated usage can be calculated based on individual usage events, and can be broken down by time period, resource type, or other relevant factors.