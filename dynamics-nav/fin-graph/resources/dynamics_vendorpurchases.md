---
title: vendorPurchases resource type | Microsoft Docs
description: A vendor purchase object in Dynamics 365 Business Central.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen

ms.prod: dynamics-nav-2018
ms.topic: reference
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 03/19/2018
ms.author: solsen
ROBOTS: NOINDEX
---

# vendorPurchases resource type
Represents a vendor purchase in [!INCLUDE[d365fin_long_md](../../includes/d365fin_long_md.md)].

> [!NOTE]  
> For information about enabling APIs for [!INCLUDE[navnow](../../includes/navnow_md.md)] see [Enabling the APIs for Dynamics 365 Business Central](../../enabling-apis-for-dynamics-nav.md).

## Methods

| Method       | Return Type  |Description|
|:---------------|:--------|:----------|
|[GET vendorPurchases](../api/dynamics_vendorpurchases_get.md)|vendorPurchases|Gets a vendor purchase object.|

## Properties

| Property     | Type   |Description|
|:---------------|:--------|:----------|
|vendorId|GUID|Represents the vendor ID.|
|vendorNumber|string|Represents the vendor number.|
|name|string|Represents the name of the vendor .|
|totalPurchaseAmount|numeric|Represents the vendor purchases.|
|dateFilter_FilterOnly|date|Represents the date filter for the vendor purchases.|


## Relationships
None

## JSON representation

Here is a JSON representation of the resource.


```json
{
    "vendorId": "GUID",
    "vendorNumber": "string",
    "name": "string",
    "totalPurchaseAmount": "decimal",
    "dateFilter_FilterOnly": "date"
}
```
## See also
[Graph Reference](../api/dynamics_graph_reference.md)  
[Working with [!INCLUDE[d365fin_long_md](../../includes/d365fin_long_md.md)] in Microsoft Graph](../resources/dynamics_overview.md)  
[Enabling the APIs for Dynamics 365 Business Central](../../enabling-apis-for-dynamics-nav.md)  
[Endpoints for the APIs](../../endpoints-apis-for-dynamics.md)  
[Error Codes](../dynamics_error_codes.md)  
[Get Vendor Purchases](../api/dynamics_vendorpurchases_get.md)  
