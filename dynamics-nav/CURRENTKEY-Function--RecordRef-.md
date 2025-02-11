---
title: "CURRENTKEY Function (RecordRef)"
description: Describes the CURRENTKEY function (RecordRef) and provides syntax, parameters, return value, and an example.
ms.custom: na
ms.date: 06/05/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.prod: "dynamics-nav-2018"
ms.assetid: 74966ab9-31c5-482e-88bb-624fffecf150
caps.latest.revision: 8
manager: edupont
---
# CURRENTKEY Function (RecordRef)
Gets the current key of the table referred to by the RecordRef. The current key is returned as a string.  
  
## Syntax  
  
```  
  
CurrentKey := RecordRef.CURRENTKEY  
```  
  
#### Parameters  
 *RecordRef*  
 Type: RecordRef  
  
 The RecordRef that refers to the table for which you want to identify the current key.  
  
## Property Value/Return Value  
 Type: Text  
  
 The name of the current key of the record.  
  
## Example  
 This example requires that you create the following text constants and variables in the **C/AL Globals** window.  
  
|Text constant|ENU value|  
|-------------------|---------------|  
|Text000|The current key in the "%1" table is "%2".|  
  
|Variable|Data type|  
|--------------|---------------|  
|RecRef|RecordRef|  
  
```  
RecRef.OPEN(18);  
MESSAGE(Text000,RecRef.CAPTION,RecRef.CURRENTKEY)  
```  
  
 `RecRef.Open(18)` - Opens table 18 or causes a run-time error if table 18 does not exist.  
  
 `RecRef.Caption` - Returns the caption of the table.  
  
 `RecRef.CURRENTKEY` - Returns the caption of the current key in the table.  
  
## See Also  
 [RecordRef Data Type](RecordRef-Data-Type.md)