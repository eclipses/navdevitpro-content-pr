---
title: "ERASE Function (File)"
description: Describes the ERASE function (file) and provides syntax, parameters, return value, and an example.
ms.custom: na
ms.date: 06/04/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.prod: "dynamics-nav-2018"
ms.assetid: 29e195c8-557d-43a7-b416-37c2ec246cfc
caps.latest.revision: 13
---
# ERASE Function (File)
Deletes a file.  
  
## Syntax  
  
```  
  
[Ok :=]ERASE(Name)  
```  
  
#### Parameters  
 *Name*  
 Type: Text or code  
  
 The name of the file that you want to delete, including the path. When you enter the path, consider these shortcuts:  
  
-   You can omit the drive designation if the file is located on the current drive.  
  
-   You can omit the full path if the file is located in the current directory.  
  
-   You can enter only the subdirectory name if the file is located in a subdirectory of the current directory  
  
## Property Value/Return Value  
 Type: Boolean  
  
 Specifies whether the file was deleted.  
  
 **true** if the file was deleted; otherwise, **false**.  
  
 If you omit this optional return value and the file is not deleted, a run-time error occurs. If you include the return value, you must handle any errors.  
  
## Remarks  
 If the user who runs this function does not have the required permission to delete the file or if the file is read-only, then the file is not deleted.  
  
## Example  
 The following example deletes the file that is named C:\\TestFolder\\NewTestFile.txt.This example assumes that you have created the file on your computer.  
  
```  
ERASE('C:\TestFolder\NewTestFile.txt');  
```  
  
## See Also  
 [File Data Type](File-Data-Type.md)