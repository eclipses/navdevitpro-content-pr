---
title: "SETRECFILTER Function (RecordRef)"
description: SETRECFILTER Function (RecordRef) Sets a filter on a record that is referred to by a RecordRef. This topic contains information on the SETRECFILTER Function (RecordRef) syntax, parameters, remarks, and examples.
ms.custom: na
ms.date: 06/05/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.prod: "dynamics-nav-2018"
ms.assetid: 8c5d6a10-c8e9-492e-9f66-bbf07895d230
caps.latest.revision: 12
---
# SETRECFILTER Function (RecordRef)
Sets a filter on a record that is referred to by a RecordRef.  
  
## Syntax  
  
```  
  
RecordRef.SETRECFILTER  
```  
  
#### Parameters  
 *RecordRef*  
 Type: RecordRef  
  
 The RecordRef used to identify the record on which you want to place a filter.  
  
## Remarks  
 This function works the same as the [SETRECFILTER Function \(Record\)](SETRECFILTER-Function--Record-.md).  
  
## Example  
 The following example opens the Customer table as a RecordRef variable that is named MyRecordRef. The SETRECFILTER function sets the values in the current key of the current record as a record filter. The [GETFILTERS Function \(RecordRef\)](GETFILTERS-Function--RecordRef-.md) retrieves the filters that have been set and displays them in a message box. No. is displayed because the filter is set on the No. field, which is the current key. This example requires that you create the following variables and text constant and text constants in the **C/AL Globals** window.  
  
|Variable name|DataType|  
|-------------------|--------------|  
|MyRecordRef|RecordRef|  
|varFilters|Test|  
  
|Text constant name|ENU value|  
|------------------------|---------------|  
|Text000|The filter is set on the %1 field.|  
  
```  
  
MyRecordRef.OPEN(DATABASE::Customer);  
MyRecordRef.SETRECFILTER;  
varFilters := MyRecordRef.GETFILTERS;  
MESSAGE(Text000, varFilters);  
```  
  
## See Also  
 [RecordRef Data Type](RecordRef-Data-Type.md)