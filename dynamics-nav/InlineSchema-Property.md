---
title: "InlineSchema Property"
description: "This topic describes the InlineSchema property, which specifies whether an XML schema definition should be included inside an XML document."
ms.custom: na
ms.date: 06/05/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.prod: "dynamics-nav-2018"
ms.assetid: ef675ff7-3085-4678-8fb8-527f7b0af53a
caps.latest.revision: 5
manager: edupont
---
# InlineSchema Property
Specifies whether an XML schema definition should be included inside an XML document.  
  
## Applies To  
  
-   XMLports  
  
## Property Value  
 **true** if the XML schema definition should be included in the XML document; otherwise, **false**.  
  
## Remarks  
 Inline schemas are XML schema definitions that can be included inside XML instance documents instead of importing it from an external source. Like an external schema, an inline schema can be used to verify that the XML document instance matches the schema constraints.  
  
 Inline schemas can be useful in many situations. You can use inline schemas in the following situations:  
  
-   When the architecture uses internal DTDs, and the developers wants to preserve that design pattern.  
  
-   When it is difficult to access external files or URLs. For example, when there are security or platform restrictions.  
  
-   When there is so much diversity in the XML document and the schema. The document is easier to process if the schema is inside the XML document.  
  
## See Also  
 [Properties](Properties.md)   
 [XMLport Data Type](XMLport-Data-Type.md)