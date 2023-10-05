# UKSC Azure Modules

This repository contains Bicep modules used to deploy the UK Supreme Court website to Azure.

## Modules

### CMS Module

The `cms.bicep` module is used to deploy the CMS for the UK Supreme Court website.

#### Parameters

- `location`: The location where the resources will be deployed. Defaults to the resource group location.
- `tenantId`: The ID of the tenant where the resources will be deployed. Defaults to the subscription tenant ID.
- `resourcePrefix`: A unique string used to prefix the names of the deployed resources. Defaults to a unique string based on the resource group ID.
- `databaseName`: The name of the database to create for the CMS.
- `databaseCollation`: The collation to use for the database. Defaults to `SQL_Latin1_General_CP1_CI_AS`.
- `databaseEdition`: The edition of the database. Defaults to `Standard`.
- `databaseSize`: The size of the database. Defaults to `5 GB`.
- `databaseMaxSize`: The maximum size of the database. Defaults to `10 GB`.
- `databaseServiceObjective`: The service objective of the database. Defaults to `S0`.

#### Deployment

To deploy the CMS module, follow these steps:

1. Clone the repository and navigate to the `cms` directory.
2. Run the `bicep build` command to build the module.
3. Run the `az deployment group create` command to deploy the module to Azure.

For more information on deploying Bicep modules, see the [Bicep documentation](https://docs.microsoft.com/en-us/azure/azure-resource-manager/bicep/overview).

### Component Module

The `component.bicep` module is used to deploy the components for the UK Supreme Court website.

#### Parameters

- `location`: The location where the resources will be deployed. Defaults to the resource group location.
- `tenantId`: The ID of the tenant where the resources will be deployed. Defaults to the subscription tenant ID.
- `resourcePrefix`: A unique string used to prefix the names of the deployed resources. Defaults to a unique string based on the resource group ID.
- `appInsightsName`: The name of the Application Insights instance to use for logging.
- `appInsightsLocation`: The location of the Application Insights instance. Defaults to the resource group location.

#### Deployment

To deploy the component module, follow these steps:

1. Clone the repository and navigate to the `component` directory.
2. Run the `bicep build` command to build the module.
3. Run the `az deployment group create` command to deploy the module to Azure.

For more information on deploying Bicep modules, see the [Bicep documentation](https://docs.microsoft.com/en-us/azure/azure-resource-manager/bicep/overview).

### UKSC Website Module

The `uksc-website.bicep` module is used to deploy the UK Supreme Court website to Azure.

#### Parameters

- `location`: The location where the resources will be deployed. Defaults to the resource group location.
- `tenantId`: The ID of the tenant where the resources will be deployed. Defaults to the subscription tenant ID.
- `resourcePrefix`: A unique string used to prefix the names of the deployed resources. Defaults to a unique string based on the resource group ID.
- `appServicePlanId`: The ID of the App Service Plan to use for the website.
- `frontDoorId`: The ID of the Front Door to use for the website.
- `cmsHostName`: The hostname to use for the CMS.

#### Deployment

To deploy the UKSC website module, follow these steps:

1. Clone the repository and navigate to the `uksc-website` directory.
2. Run the `bicep build` command to build the module.
3. Run the `az deployment group create` command to deploy the module to Azure.

For more information on deploying Bicep modules, see the [Bicep documentation](https://docs.microsoft.com/en-us/azure/azure-resource-manager/bicep/overview).
