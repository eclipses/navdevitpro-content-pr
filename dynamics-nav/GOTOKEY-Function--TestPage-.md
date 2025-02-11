---
title: "GOTOKEY Function (TestPage)"
description: "The GOTOKEY Function (TestPage) finds the row in a dataset on the test page that is identified by the specified values."
ms.custom: na
ms.date: 06/04/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.prod: "dynamics-nav-2018"
ms.assetid: e880f74c-c0a9-498f-8c91-bfcf207680bf
caps.latest.revision: 3
author: jswymer
manager: edupont
---
# GOTOKEY Function (TestPage)
Finds the row in a dataset on the test page that is identified by the specified values.  
  
## Syntax  
  
```  
[Ok :=]TestPage.GOTOKEY([Value],...);  
```  
  
#### Parameters  
 *TestPage*  
 Type: TestPage  
  
 The test page that contains the dataset.  
  
 *Value*  
 Type: Text or Integer  
  
 The value or list of values to use to find the row. If this parameter is omitted, the value of the primary key that is defined for the underlying table is used.  
  
## Property Value/Return Value  
 Type: Boolean  
  
 **true** if the specified row is found; otherwise, **false**. The return value is optional.  

## Remarks
The GOTOKEY function loops over all records until it finds the identifies row.  For each record, the [OnAfterGetCurrentRecord trigger](OnAfterGetCurrRecord-Trigger.md) is executed.  
  
## See Also  
 [TestPage Functions](TestPage-Functions.md)