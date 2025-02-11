---
title: "COPY Function (File)"
description: "This document describes the COPY function (File), which copies a file from one specified location to another."
ms.custom: na
ms.date: 06/04/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.prod: "dynamics-nav-2018"
ms.assetid: 8116f838-de15-44f0-a1e7-9292c6a7c4f6
caps.latest.revision: 15
manager: edupont
---
# COPY Function (File)
Use this function to copy a file.  
  
## Syntax  
  
```  
  
[Ok :=] File.COPY(FromName, ToName)  
```  
  
#### Parameters  
 *FromName*  
 Type: Text or code  
  
 The name of the file that you want to make a copy of, including its path. When you enter the path, consider these shortcuts:  
  
- You can omit the drive designation if the file is located on the current drive.  
  
- You can omit the full path if the file is located in the current directory.  
  
- You can enter only the subdirectory name if the file is located in a subdirectory of the current directory.  
  
  *ToName*  
  Type: Text or code  
  
  The name that you want to assign to the copy that includes its path. When you enter the path, consider these shortcuts:  
  
- You can omit the drive designation if the file is located on the current drive.  
  
- You can omit the full path if the file is located in the current directory.  
  
- You can enter only the subdirectory name if the file is located in a subdirectory of the current directory.  
  
## Property Value/Return Value  
 Type: Boolean  
  
 This optional return parameter shows you whether the file was copied.  
  
## Remarks  
 If you do not use the return value and the file cannot be copied, a run-time error will occur. If you do include the return value in your code, you must handle any errors yourself.  
  
## Example  
 The following example copies a file that is named OldFile from a folder that is named Old on drive C to a folder that is named New. If the file is copied, a message is displayed and the program continues. Otherwise, an error occurs. This example requires that you create the following variables in the **C/AL Globals** window. This example assumes that you have created the following file 'c:\\Old\\' OldFile.  
  
|Variable name|DataType|  
|-------------------|--------------|  
|OldFile|Text|  
|NewFile|Text|  
  
```  
  
OldFile := 'old.txt';  
NewFile := 'new.txt';  
IF FILE.COPY('c:\Old\' + OldFile, 'c:\New\' + NewFile) THEN  
  // Continue your program.  
  MESSAGE('The file was copied.')  
ELSE  
  // Handle the error.  
  MESSAGE('The file was not copied.')  
```  
  
## See Also  
 [File Data Type](File-Data-Type.md)