---
title: "FIELDINDEX Function (KeyRef)"
description: Details the syntax for the FIELDINDEX function which provides the FieldRef of the field that is indexed in the key referred to by the KeyRef variable.
ms.custom: na
ms.date: 06/05/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.prod: "dynamics-nav-2018"
ms.assetid: 8f2e7e16-93ab-4924-9ed6-64c85d6177d5
caps.latest.revision: 13
---
# FIELDINDEX Function (KeyRef)
Gets the FieldRef of the field that has this index in the key referred to by the *KeyRef* variable. Returns an error if no key is selected.  
  
## Syntax  
  
```  
  
FieldRef := KeyRef.FIELDINDEX(Index)  
```  
  
#### Parameters  
 *KeyRef*  
 Type: KeyRef  
  
 The KeyRef that refers to the key.  
  
 *Index*  
 Type: Integer  
  
 The input index.  
  
## Property Value/Return Value  
 Type: FieldRef  
  
 The FieldRef that refers to the field with this index in the key.  
  
## Remarks  
 The first field in the index must have index 1, the second index 2, and so on. The last field must have index = FIELDCOUNT. If the index is out of the range supplied or if no table is selected, the function returns an error.  
  
## Example  
 The following example displays the caption of a field in a record. The table with ID 18 \(the Customer table\) is open with a reference. The *Keyref* for the record is retrieved by using the [KEYINDEX Function \(RecordRef\)](KEYINDEX-Function--RecordRef-.md). The function retrieves the second key in the record and stores the value in the varKeyRef variable. The varKeyRef variable is then used to return the *FieldRef*. The varFieldRef variable is used to display the caption of the field. This example requires that you create the following variables in the **C/AL Globals** window.  
  
|Variable name|DataType|  
|-------------------|--------------|  
|RecRef|RecordRef|  
|varKeyRef|KeyRef|  
|varFieldRef|FieldRef|  
  
```  
  
RecRef.OPEN(18);  
varKeyRef := RecRef.KEYINDEX(2);  
varFieldRef := varKeyRef.FIELDINDEX(1);  
MESSAGE('The Field name is: %1' ,varFieldRef.CAPTION);  
```  
  
## See Also  
 [KeyRef Data Type](KeyRef-Data-Type.md)