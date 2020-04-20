# Power BI Embedded


This template deploys **Power BI Embedded**. **Power BI Embedded** is a **companion service to Power BI. It allows developers use Power BI capabilities with embedded analytics.**

## Power BI Embedded overview and deployed resources

This solution provides a template for deploying Power BI Embedded. 

### Resource provider

Microsoft.PowerBI

+ **Resource type**: capacities


## Prerequisites

Azure subscription is the only prerequiste for service deployment; however, published Power BI reports from a configured Power BI Service are needed for integration.

## Deployment steps

Modify the azuredeploy.parameters.json file to include the following for each customer: 
- name
- location
- sku (Allowed values: 
                "A1",
                "A2",
                "A3",
                "A4",
                "A5",
                "A6") 
- tags (such as owner)

*See this article for current SKU descriptions: https://docs.microsoft.com/en-us/power-bi/developer/embedded/embedded-capacity#sku-memory-and-computing-power*

From a PowerShell window, execute the deploy.ps1 script with the following parameters:

+ ServiceName    -  The name of the Azure service being deployed
+ ResourceGroup  -  The name of the resource group for deployment

```
.\deploy.ps1  <ServiceName> <ResourceGroup>
```

_Example:_

  .\deploy.ps1 msp-sample-pbie msp-pbie-rg

  Will deploy the template located at .\msp-sample-vnet\azuredeploy.json into the *msp-sample* resource group.

## Removal steps

From a PowerShell window, execute the remove.ps1 script with the following parameters:

+ ServiceName    -  The name of the Azure service being removed
+ ResourceGroup  -  The name of the resource group for removal

```
.\remove.ps1  <ServiceName> <ResourceGroup>

```
_Example:_

  .\remove.ps1 msp-sample-pbie msp-pbie-rg

  Will remove the service *msp-sample-pbie* from the *msp-pbie-rg* resource group.


## Usage

https://docs.microsoft.com/en-us/power-bi/developer/embedded/embedded-faq

https://docs.microsoft.com/en-us/power-bi/developer/embedding


### Development

https://powerbi.microsoft.com/en-us/developers/embedded-analytics/isv/

https://docs.microsoft.com/en-us/power-bi/developer/embed-sample-for-customers#step-1-setup-your-embedded-analytics-development-environment

