---
title: "ACTIVE Function (FieldRef)"
description: "The ACTIVE Function (FieldRef) checks whether the field that is currently selected is enabled. This article describes its syntax, property/return value, remarks, and example."
ms.custom: na
ms.date: 06/05/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.prod: "dynamics-nav-2018"
ms.assetid: 8dbe2401-6f58-4e13-85f5-3fb5db9228d1
caps.latest.revision: 18
---
# ACTIVE Function (FieldRef)
Checks whether the field that is currently selected is enabled.  
  
## Syntax  
  
```  
  
Ok := FieldRef.ACTIVE  
```  
  
#### Parameters  
 *FieldRef*  
 Type: FieldRef  
  
 Refers to the current field.  
  
## Property Value/Return Value  
 Type: Boolean  
  
 **true** if the field is enabled; otherwise, **false**.  
  
## Remarks  
 Each field in a record can be set as enabled or disabled in the table description.  
  
 You cannot use a disabled field because disabled fields cannot contain data.  
  
 This function is like the [FIELDACTIVE Function \(Record\)](FIELDACTIVE-Function--Record-.md) function.  
  
## Example  
 The following example opens table 18 \(Customer\) as a RecordRef variable that is named Recref. The [FIELD Function \(RecordRef\)](FIELD-Function--RecordRef-.md) uses Recref to create a FieldRef variable that is named MyFieldRef. MyFieldRef sets a reference to the first field \(field 1\) in the table. The [SETRANGE Function \(FieldRef\)](SETRANGE-Function--FieldRef-.md) sets a filter that selects record 30000. The [FIND Function \(RecordRef\)](FIND-Function--RecordRef-.md) selects the record and then loops through fields1 through 6. For each field, the ACTIVE function determines whether the field is enabled. If the field is enabled, a message that states that the field is enabled is displayed. Otherwise, a message that states that the field is not enabled is displayed.  
  
> [!NOTE]  
>  You can use the name of the table instead of the table number to open the table by using the following syntax: Recref.OPEN\(DATABASE::Customer\).  
  
 This example requires that you create the following variables and text constants in the **C/AL Globals** windows.  
  
|Variable name|DataType|  
|-------------------|--------------|  
|Recref|RecordRef|  
|MyFieldRef|FieldRef|  
|i|Integer|  
  
|Text constant|ENU value|  
|-------------------|---------------|  
|Text000|Field %1 is enabled.|  
|Text001|Field %1 is not enabled.|  
  
```  
  
Recref.OPEN(18);  
MyFieldRef := Recref.FIELD(1);  
MyFieldRef.SETRANGE('30000');  
Recref.FIND('-');  
FOR i := 1 TO 5 DO BEGIN  
  MyFieldRef := Recref.FIELDINDEX(i);  
  IF MyFieldRef.ACTIVE THEN  
    MESSAGE(Text000, i)  
  ELSE BEGIN  
    MESSAGE(Text001, i)  
  END;  
END;  
  
```  
  
## See Also  
 [FieldRef Data Type](FieldRef-Data-Type.md)