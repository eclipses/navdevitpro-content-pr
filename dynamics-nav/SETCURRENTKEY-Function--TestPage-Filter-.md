---
title: "SETCURRENTKEY Function (TestPage Filter)"
description: SETCURRENTKEY Function (TestPage Filter) sets the specified fields in a dataset on a test page as the current key.
ms.custom: na
ms.date: 06/05/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.prod: "dynamics-nav-2018"
ms.assetid: 46b3889b-272a-43cc-bf34-2498280d1b48
caps.latest.revision: 5
manager: edupont
---
# SETCURRENTKEY Function (TestPage Filter)
Sets the specified fields in a dataset on a test page as the current key.  
  
## Syntax  
  
```  
[Ok :=] TestPage.Filter.SETCURRENTKEY(Field1 [, Field2] ,...);  
```  
  
#### Parameters  
 *TestPage*  
 Type: TestPage  
  
 The test page that displays the dataset that contains the specified field.  
  
 *Part*  
 Type: Part  
  
 The control on the test page that contains the dataset.  
  
 *Filter*  
 Type: Filter  
  
 The filter that is applied to the dataset.  
  
 *Field1*  
 Type: Field  
  
 The field that you want to set as the current key.  
  
 *Field2*  
 Type: Field  
  
 Additional field that you want to set as the current key. This parameter is optional.  
  
## Property Value/Return Value  
 Type: Boolean  
  
 **true** if the current key was set; otherwise, **false**. This return value is optional.  
  
## Remarks  
 You can select additional fields to be included as the current key.  
  
## See Also  
 [TestPage Filter Functions](TestPage-Filter-Functions.md)