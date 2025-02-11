---
title: "Layout Property"
description: "The Layout Property sets whether the fields in Group controls are arranged horizontally in a row or vertically in a column."
ms.custom: na
ms.date: 06/05/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.prod: "dynamics-nav-2018"
ms.assetid: 7c117ea8-3426-4e48-8991-10b08feec6c3
caps.latest.revision: 9
---
# Layout Property
Sets whether the fields in Group controls are arranged horizontally in a row or vertically in a column.  
  
## Applies To  
  
-   Group controls, including Group, Repeater, CueGroup, FixedLayout, and GridLayout subtypes on pages.  
  
## Property Values  
  
|Value|[!INCLUDE[bp_tabledescription](includes/bp_tabledescription_md.md)]|  
|-----------|---------------------------------------|  
|**Rows**|Arranges fields within Group controls in rows.|  
|**Columns**|Arranges fields within Group controls in columns. This is the default setting.|  
|**Undefined**|Same as the **Columns** setting.|  
  
## Remarks  
 You use a Group control to arrange fields in rows and columns. To define the rows and columns of fields, you add **SubType** Group controls to the Group control. Each **SubType** control contains the fields that you want to display. You can use the **Layout** property to specify whether the fields in a group are arranged in rows or columns.  
  
## See Also  
 [How to: Arrange Fields in Rows and Columns Using the GridLayout Control](How-to--Arrange-Fields-in-Rows-and-Columns-Using-the-GridLayout-Control.md)