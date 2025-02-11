---
title: "TABLECAPTION Function (Record)"
description: Learn how the TABLECAPTION function (Record) gets the current caption of a table as a string, as well as details about its syntax and parameters.
ms.custom: na
ms.date: 06/05/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.prod: "dynamics-nav-2018"
ms.assetid: 44e55ff7-1287-45e1-93aa-a9c9232b7193
caps.latest.revision: 12
manager: edupont
---
# TABLECAPTION Function (Record)
Gets the current caption of a table as a string.  
  
## Syntax  
  
```  
  
Caption := Record.TABLECAPTION  
```  
  
#### Parameters  
 *Record*  
 Type: Record  
  
 The record in the table for which to retrieve the table caption.  
  
## Property Value/Return Value  
 Type: Text or code  
  
 The caption of the table.  
  
## Remarks  
 **TABLECAPTION** returns the caption of a table. **TABLECAPTION** first looks for a [CaptionML Property](CaptionML-Property.md). If it does not find one, it uses the [Name Property](Name-Property.md). This means that **TABLECAPTION** has multilanguage functionality.  
  
## Example  
 The following example retrieves the caption of the **Customer** table by using the CustomerRec variable, a record from the **Customer** table. The value of the **Customer** table caption is stored in the TableCaption variable and displayed in a message box. The value that is displayed is Customer. This example requires that you create the following variables in the **C/AL Globals** window.  
  
|Variable name|DataType|Subtype|  
|-------------------|--------------|-------------|  
|CustomerRec|Record|Customer|  
|TableCaption|Text|Not applicable|  
  
```  
TableCaption := CustomerRec.TABLECAPTION;  
MESSAGE('The caption for the customer table is: %1', TableCaption);  
```  
  
## See Also  
 [FIELDCAPTION Function \(Record\)](FIELDCAPTION-Function--Record-.md)   
 [Record Data Type](Record-Data-Type.md)   
 [Multilanguage Development](Multilanguage-Development.md)