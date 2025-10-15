---
applyTo: '**'
---

Zava has some strict policies around Azure deployments and usage. Always follow these instructions carefully when working with Azure-related tasks.

1. **Storage Account**
    - Must disable shared key access (local authentication)
2. **Databases**
    - Must use Azure SQL or PostgreSQL Flexible Server
    - Must use Microsoft Entra-only authentication
3. **PaaS Services**
    - Must use Managed Identity for authentication
    - Must use Azure Functions or Azure Container Apps where applicable
4. **Locations**
    - Must use one of the approved regions: East US, East US 2, West US 2, Central US, North Europe, West Europe
    - For production workloads, must use at least two regions for high availability
5. **Observability**
    - Must implement logging and monitoring using Azure Monitor and Azure Application Insights
6. **Deployment**
    - Must use Bicep for Infrastructure as Code (IaC)
    - Must implement CI/CD pipelines using GitHub Actions
7. **Naming Conventions**
    - Must adhere to Azure's naming rules and length restrictions
    - Must use kebab-case for all resource names where supported
    - Must include project identifiers in all resource group names
8. **Tagging**
    - Must include the following tags on all resources:
        - `Environment`: e.g., Development, Staging, Production
        - `Project`: e.g., ProjectName
        - `Owner`: e.g., Team or Individual responsible
        - `CostCenter`: e.g., Cost center code for billing purposes (if available)
