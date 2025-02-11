---
title: "LOCKTABLE Function (Record)"
description: "The LOCKTABLE Function (Record) locks a table to protect it from write transactions that conflict with each other."
ms.custom: na
ms.date: 06/05/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.prod: "dynamics-nav-2018"
ms.assetid: ba5aa5db-100c-4081-80e0-986cbc8e034d
caps.latest.revision: 10
manager: edupont
---
# LOCKTABLE Function (Record)
Locks a table to protect it from write transactions that conflict with each other.  
  
## Syntax  
  
```  
Record.LOCKTABLE([Wait: Boolean], [VersionCheck: Boolean])
```  
  
#### Parameters  
 *Record*  
 Type: Record  
  
 The record that refers to the table that you want to lock.  

*Wait*  
&emsp;Type: Boolean

Specifies what to do if the table is already locked. If this parameter is true and if another application has already locked the table, the system will wait until the table is unlocked. If this parameter is false and if another application has already locked the table, a run-time error occurs.  

*VersionCheck*  
&emsp;Type: Boolean

If this parameter is true, the version of the record will be checked. If this parameter is false, blank, or not used, the version will not be checked. 

  
## Remarks  
 Because all write operations automatically lock the table that is being used, **LOCKTABLE** appears unnecessary. However, you could have a transaction in which an application wants to inspect data and then only possibly change it. You require a guarantee that the data being changed has not been modified by other applications since the read operation. The solution is to explicitly lock the table before the read operation. This guarantees that no other application makes changes between the read operation and the possible write operation. 

 
The table lock is released (unlocked) when the transaction is committed. 
  
## Example  
 This example uses pseudo-language to show the scope of write locks. Both an explicit lock and an automatic lock are illustrated.  
  
 The first line \(1\) explicitly locks table A. If this explicit lock was not set on table A, the Database Management System \(DBMS\) would automatically lock this table when a record was inserted \(3\). Table B is not locked explicitly, but is locked automatically by the DBMS when a record is inserted \(4\). Both locks are active until the system exits the C/AL code module \(5\).  
  
```  
BeginWriteTransaction   
TableA.LockTable // (1)  
FindRec(TableA, ...) // (2)  
.  
.  
InsertRec(TableA,...) // (3)  
.  
InsertRec(TableB) // (4)  
.  
.  
EndWriteTransaction // (5)  
```  
  
 If a data update depends on a prior read operation and there is a long time between the read operation and the write operation, then you may not want to lock the table as you usually would during a transaction. This enables you to avoid preventing other users from updating the table until your transaction is committed.  
  
## See Also  
 [Record Data Type](Record-Data-Type.md)