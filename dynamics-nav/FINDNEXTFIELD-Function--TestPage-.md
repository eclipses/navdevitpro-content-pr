---
title: "FINDNEXTFIELD Function (TestPage)"
description: Describes the FINDNEXTFIELD function (TestPage) and provides syntax, parameters, and return value.
ms.custom: na
ms.date: 06/04/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.prod: "dynamics-nav-2018"
ms.assetid: 1d759dae-b951-4441-bffb-8db2047f0872
caps.latest.revision: 5
manager: edupont
---
# FINDNEXTFIELD Function (TestPage)
Finds the next field in the dataset that is displayed on a test page.  
  
## Syntax  
  
```  
[Ok :=]TestPage.FINDNEXTFIELD(Field, Value);  
```  
  
#### Parameters  
 TestPage  
 Type: TestPage  
  
 The test page that contains the dataset that you want to find.  
  
 *Field*  
 Type: Field  
  
 The field to find.  
  
 *Value*  
 Type: Any  
  
 The value of the field.  
  
## Property Value/Return Value  
 Type: Boolean  
  
 **true** if the first field is found; otherwise, **false**. The return value is optional.  
  
## See Also  
 [TestPage Functions](TestPage-Functions.md)