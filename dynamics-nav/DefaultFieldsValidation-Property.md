---
title: "DefaultFieldsValidation Property"
description: "The DefaultFieldsValidation Property sets a value that indicates whether fields are validated."
ms.custom: na
ms.date: 06/05/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.prod: "dynamics-nav-2018"
ms.assetid: 7733c6fd-3cbd-42bc-9ff3-8f7a5850cff8
caps.latest.revision: 6
manager: edupont
---
# DefaultFieldsValidation Property
Sets a value that indicates whether fields are validated.  
  
## Applies To  
 XMLports  
  
## Property Value  
 **Yes** if fields are validated; otherwise, **No**. The default value is **Yes**.  
  
## Remarks  
 This property sets the default value of the [FieldValidate Property](FieldValidate-Property.md). Therefore, if you change the setting of the DefaultFieldsValidation property, the change is implemented for all fields. However, for fields for which the FieldValidate property has been set to **Yes** or **No**, no change is made.  
  
 If you change the value of the FieldValidate property, the change does not affect the value of the DefaultFieldsValidation property. This means that FieldValidate can override DefaultFieldsValidation, but that it can also inherit the default value of DefaultFieldsValidation.  
  
## See Also  
 [Properties](Properties.md)