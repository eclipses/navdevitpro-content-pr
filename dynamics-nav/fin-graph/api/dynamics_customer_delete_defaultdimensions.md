---
title: Delete customer defaultDimensions | Microsoft Docs
description: Deletes the default dimensions of the customer in Dynamics 365 Business Central.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.prod: dynamics-nav-2018
ms.topic: reference
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 08/22/2018
ms.author: solsen
ROBOTS: NOINDEX
---

# Delete customer defaultDimensions
Deletes the default dimensions of the customer in [!INCLUDE[d365fin_long_md](../../includes/d365fin_long_md.md)].

## HTTP request
Replace the URL prefix for [!INCLUDE[d365fin_long_md](../../includes/d365fin_long_md.md)] depending on environment following the [guideline](../../endpoints-apis-for-dynamics.md).
```
DELETE businesscentralPrefix/companies({companyId})/customers({customerId})/defaultDimensions({customerId},{dimensionId})
```

## Request headers

|Header         |Value                     |
|---------------|--------------------------|
|Authorization  |Bearer {token}. Required. |
|If-Match       |Required. When this request header is included and the eTag provided does not match the current tag on the **customers**, the **customers** will not be updated. |

## Request body
Do not supply a request body for this method.

## Response
If successful, this method returns a ```204 No Content``` response code and it deletes the default dimensions for the customer and corresponding dimension.

## Example

**Request**

Here is an example of the request.

```json
DELETE https://{businesscentralPrefix}/api/beta/companies({companyId})/customers({customerId})/defaultDimensions({customerId},{dimensionId})
```

**Response** 

No Content.

## See also
[Tips for working with the APIs](/dynamics365/business-central/dev-itpro/developer/devenv-connect-apps-tips)  
[Graph Reference](../api/dynamics_graph_reference.md)  
[Working with [!INCLUDE[d365fin_long_md](../../includes/d365fin_long_md.md)] in Microsoft Graph](../resources/dynamics_overview.md)  
[Enabling the APIs for Dynamics 365 Business Central](../../enabling-apis-for-dynamics-nav.md)  
[Endpoints for the APIs](../../endpoints-apis-for-dynamics.md)  
[Error Codes](../dynamics_error_codes.md)  
[Customer](../resources/dynamics_customer.md)  
[Create customer defaultDimensions](dynamics_customer_create_defaultdimensions.md)  
[Update customer defaultDimensions](dynamics_customer_update_defaultdimensions.md)  
[Get customer defaultDimensions](dynamics_customer_get_defaultdimensions.md)  
