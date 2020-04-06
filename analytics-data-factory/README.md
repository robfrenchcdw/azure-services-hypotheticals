# Azure Data Factory V2

This template deploys an **Azure Data Factory V2**. The **Azure Data Factory V2** is a **cloud-based ETL and data integration service that allows you to create data-driven workflows for orchestrating data movement and transforming data at scale**

## Overview and deployed resources

This solution will deploy a single Azure Data Factory. The following resources are deployed as part of the solution:

### Resource provider 

Microsoft.DataFactory


## Prerequisites

An exisitng resource group is required for this deployment. This can be manually created, added in as an automated step before this script, or be used with an exisitng resrce group

## Deployment steps

Modify the azuredeploy.parameters.json file to include the following for each customer: 
- name
- location

**Additional Parameters here**
- tags (such as owner)

From a PowerShell window, execute the deploy.ps1 script with the following parameters:

+ ServiceName    -  The name of the Azure service being deployed
+ ResourceGroup  -  The name of the resource group for deployment

```
.\deploy.ps1  <ServiceName> <ResourceGroup>

```

_Example:_

  .\deploy.ps1 msp-sample-adf msp-adf-rg

  Will deploy the template located at .\msp-sample-vnet\azuredeploy.json into the *msp-adf-rg* resource group.

## Removal steps

From a PowerShell window, execute the remove.ps1 script with the following parameters:

+ ServiceName    -  The name of the Azure service being deployed
+ ResourceGroup  -  The name of the resource group for deployment

```
.\remove.ps1  <ServiceName> <ResourceGroup>

```
_Example:_

  .\remove.ps1 msp-sample-adf msp-adf-rg

  Will remove the service *msp-sample-adf* from the *msp-adf-rg* resource group.

### Connect

Connecting to Data Factory

#### Management

How to manage the solution

## Notes

Solution notes

`Tags: Tag1, Tag2, Tag3`