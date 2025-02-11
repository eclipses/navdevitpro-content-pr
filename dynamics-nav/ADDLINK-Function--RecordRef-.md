---
title: "ADDLINK Function (RecordRef)"
description: "The ADDLINK function (RecordRef) adds a link to a record in a table. This article describes its syntax, property/return value, remarks, and example."
ms.custom: na
ms.date: 06/05/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.prod: "dynamics-nav-2018"
ms.assetid: fa6aa219-fa2b-4a51-9c7d-dd9dd6fcb63b
caps.latest.revision: 14
manager: edupont
---
# ADDLINK Function (RecordRef)
Adds a link to a record in a table.  
  
## Syntax  
  
```  
  
[ID := ]ADDLINK(URL[, Description])  
```  
  
#### Parameters  
 *URL*  
 Type: String  
  
 The link that you want to add to the record.  
  
 *Description*  
 Type: String  
  
 Optional description of the link.  
  
## Property Value/Return Value  
 Type: Integer  
  
 The ID of the URL that you want to add to the record. Every time that you add a link to a page or a table, an entry is created in the Record Link system table. Each entry is given an ID.  
  
## Remarks  
 The URL can be a link to a Web site, a file stored on the local or on a remote computer, or a link to a [!INCLUDE[navnow](includes/navnow_md.md)] page. You can then view the link in the **Links** FactBox on pages that display the record.  
  
## Example  
 The following example adds a link to a record in the Customer table. The code starts by opening table 18 \(Customer\) as a RecordRef variable that is named CustomerRecref. The [FIELD Function \(RecordRef\)](FIELD-Function--RecordRef-.md) creates a FieldRef variable that is named MyFieldRef for the first field \(No.\). Next, `MyFieldRef.VALUE` is set to record 01121212. The [FIND Function \(RecordRef\)](FIND-Function--RecordRef-.md) function searches the records for record no. 01121212. If the record is found, then the ADDLINK function adds a link to the record. The link is assigned a link ID, which is stored in the LinkID variable. The link ID is displayed in a message box. You can view the link you added in the **Links** FactBox on the Customer List or Customer Card pages. This example requires that you create the following variables and text constants in **C/AL Globals** window.  
  
|Variable name|DataType|  
|-------------------|--------------|  
|CustomerNum|Code|  
|varLink|Text|  
|CustomerRecref|RecordRef|  
|MyFieldRef|FieldRef|  
|LinkID|Integer|  
  
|Text constant name|DataType|ENU value|  
|------------------------|--------------|---------------|  
|Text000|Text|The link with ID %1 has been added.|  
|Text001|Text|The customer cannot be found.|  
  
```  
CustomerNum := '01121212';  
CustomerRecref.OPEN(18);  
MyFieldRef := CustomerRecref.FIELD(1);  
MyFieldRef.VALUE := CustomerNum;  
IF CustomerRecref.FIND('=') THEN BEGIN  
  LinkID := CustomerRecref.ADDLINK(varLink);  
  MESSAGE(Text000, LinkID);  
END  
ELSE  
  MESSAGE(Text001);  
```  
  
## See Also  
 [RecordRef Data Type](RecordRef-Data-Type.md)