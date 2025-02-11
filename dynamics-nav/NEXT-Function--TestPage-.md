---
title: "NEXT Function (TestPage)"
description: Details the code and syntax for the NEXT function which sets the current row of the test page as the next row in the dataset.
ms.custom: na
ms.date: 06/04/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.prod: "dynamics-nav-2018"
ms.assetid: 25e24fec-2c36-4f59-af74-518d4221b3f7
caps.latest.revision: 10
manager: edupont
---
# NEXT Function (TestPage)
Sets the current row of the test page as the next row in the dataset.  
  
## Syntax  
  
```  
  
OK := TestPage.NEXT  
```  
  
#### Parameters  
 *TestPage*  
 Type: TestPage  
  
 The test page variable that you use to refer to the test page.  
  
## Property Value/Return Value  
 Type: Boolean  
  
 **true** if the current row was set to the next row in the dataset successfully; otherwise, **false**.  
  
## Remarks  
 If *TestPage* is closed or has never been opened, then the function call fails.  
  
## Example  
 This example requires that you create a TestPage variable named CustomerList with a Subtype of Customer List.  
  
```  
CustomerList.OPENVIEW;  
// Loops through all customers and displays the customer name.  
IF CustomerList.FIRST THEN  
  REPEAT  
    MESSAGE(CustomerList.Name.Value);  
UNTIL NOT CustomerList.NEXT;  
  
```