---
title: "TableSeparator Property"
description: Learn how the TableSeparator property specifies the table separator for a table, as well as other details about the property. 
ms.custom: na
ms.date: 06/05/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.prod: "dynamics-nav-2018"
ms.assetid: 02bbb812-0ff4-429a-b1c0-8b28270a781b
caps.latest.revision: 10
manager: edupont
---
# TableSeparator Property
Specifies the table separator for a table.  
  
## Applies To  
  
-   XMLports  
  
## Property Value  
  
|**Value**|**Description**|  
|---------------|---------------------|  
|**\<None>**|There is no table separator.|  
|**\<NewLine>**|Any combination of CR and LF characters.|  
|**\<CR/LF>**|CR followed by LF.|  
|**\<CR>**|CR alone.|  
|**\<LF>**|LF alone.|  
|**\<TAB>**|Tabulator alone.|  
|**Other strings**|The literal string entered.|  
  
## Remarks  
 This property specifies how tables should be separated. The default value is a new line \(**\<NewLine>**\). **TableSeparator** property is only used if the **Format Property** is set to **Variable Text** or **Fixed Text**. Otherwise, the setting is ignored.  
  
 You can set the table separator in C/AL code so that the XMLport can import and export tables with different separators. For example, if your XMLport must import from a file or stream where one table uses a single **NewLine** elements and another uses two **NewLine** elements, you can change the table separator at run time.  
  
## See Also  
 [Properties](Properties.md)