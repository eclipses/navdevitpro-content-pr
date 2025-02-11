---
title: "ISNULLGUID Function (GUID)"
description: "The ISNULLGUID Function (GUID) indicates whether a value has been assigned to a GUID. A null GUID that consists only of zeros is valid but must never be used for references."
ms.custom: na
ms.date: 06/05/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.prod: "dynamics-nav-2018"
ms.assetid: e536abc9-b0bb-4010-bd77-22e537eb24ba
caps.latest.revision: 14
manager: edupont
---
# ISNULLGUID Function (GUID)
Indicates whether a value has been assigned to a GUID. A null GUID that consists only of zeros is valid but must never be used for references.  
  
## Syntax  
  
```  
  
Ok := ISNULLGUID(Guid);  
```  
  
#### Parameters  
 *Guid*  
 The GUID that you want to check whether it is null.  
  
## Property Value/Return Value  
 Type: Boolean  
  
 **true** if a value has been assigned to the GUID; otherwise, **false**.  
  
## Remarks  
 The GUID data type is useful when you want to uniquely identify data so that it can be exchanged with external applications. For example, if you want to transfer an item catalog to an external application, you add a GUID field to the record in the table and use it as the primary reference when you communicate with the external application. A GUID is a 16-byte binary data type that can be logically grouped into the following subgroups: 4byte-2byte-2byte-2byte-6byte.  
  
## Example  
 The following example initializes two variables named validGuid and nullGuid. The validGuid variable is assigned a valid GUID value, and the nullGuid variable is assigned a null GUID that consists of only zeros. The ISNULLGUID function determines whether the GUID that is contained in the *validGuid* parameter is null. In this case, the GUID is not null so a message that states that the GUID is not null is displayed and the value is displayed. The function then checks the *nullGuid* parameter. This time, a message that states that the GUID is null is displayed because the GUID is a null GUID that consists of only zeros. This example requires that you create the following variables and text constants in the **C/AL Globals** window.  
  
|Variable name|DataType|  
|-------------------|--------------|  
|validGuid|GUID|  
|nullGuid|GUID|  
  
|Text constant name|ENU value|  
|------------------------|---------------|  
|Text000|The GUID is null.|  
|Text001|The GUID is not null.\\|  
|Text002|The value is: %1.|  
  
```  
  
validGuid := '{FC841BE6-0ADA-46C4-A6A9-142AEC211613}';  
nullGuid  := '{00000000-0000-0000-0000-000000000000}';  
  
IF ISNULLGUID(validGuid) THEN  
  MESSAGE(Text000)  
ELSE   
  MESSAGE(Text001 + Text002, validGuid);  
IF ISNULLGUID(nullGuid) THEN  
  MESSAGE(Text000);  
```  
  
## See Also  
 [GUID Data Type](GUID-Data-Type.md)