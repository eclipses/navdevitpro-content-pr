---
title: "INIT Function (RecordRef)"
description: "This topic describes the INIT function (RecordRef), which initializes a record in a table by assigning default values to each field in the record."
ms.custom: na
ms.date: 06/05/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.prod: "dynamics-nav-2018"
ms.assetid: e3321633-2c2f-49ac-85e0-80bccdeb337e
caps.latest.revision: 11
manager: edupont
---
# INIT Function (RecordRef)
Initializes a record in a table.  
  
## Syntax  
  
```  
  
RecordRef.INIT  
```  
  
#### Parameters  
 *RecordRef*  
 Type: RecordRef  
  
 The RecordRef that is used to identify the record that you want to initialize.  
  
## Remarks  
 This function assigns default values to each field in the record. The values that are assigned in the record correspond to those defined when the table was created. If no value was assigned when the table was created, the values are assigned based on the data type, as shown in the following table.  
  
|Data type|Default value|  
|---------------|-------------------|  
|BigInteger|0|  
|BigText|\<Empty>|  
|BLOB|\<Empty>|  
|Boolean|No|  
|Code|'' \(empty string\)|  
|Date|0d \(Undefined date\)|  
|DateFormula|'' \(empty string\)|  
|DateTime|0DT \(Undefined datetime\)|  
|Decimal|0.0|  
|Duration|0|  
|GUID|00000000-0000-0000-0000-000000000000|  
|Integer|0|  
|Option|0|  
|RecordID|\<Empty>|  
|TableFilter|\<Empty>|  
|Text|'' \(empty string\)|  
|Time|0T \(Undefined time\)|  
  
 Primary key and timestamp fields are not initialized.  
  
 After the function executes, you can change the values in any or all of the fields before you call the [INSERT Function \(RecordRef\)](INSERT-Function--RecordRef-.md) to enter the record in the table. Be sure that the fields that make up the primary key contain values that make the total primary key unique. If the primary key is not unique \(such as the record already exists\), then the record is rejected.  
  
 The function works the same as the [INIT Function \(Record\)](INIT-Function--Record-.md).  
  
## Example  
 The following example opens a table 18 \(Customer\) with a RecordRef variable that is named CustomerRecref. The [FIELD Function \(RecordRef\)](FIELD-Function--RecordRef-.md) creates a FieldRef variable that is named MyFieldRef for the field. The INIT function initializes the values in the fields by using default values and then uses the [INSERT Function \(RecordRef\)](INSERT-Function--RecordRef-.md) to insert a new record. The new record is 1120. This is the primary key for the new record.  
  
> [!NOTE]  
>  In this example, the INIT function is called before the primary key is assigned a value. The INIT function does not initialize primary key fields. Therefore calling the INIT function before or after you assign values to the primary key field does not make any difference.  
  
 This example requires that you create the following variables and text constants in the **C/AL Globals** window.  
  
|Variable name|DataType|  
|-------------------|--------------|  
|CustomerRecref|RecordRef|  
|MyFieldRef|FieldRef|  
  
|Text constant|ENU value|  
|-------------------|---------------|  
|Text000|The value of the field before initialization is %1.|  
|Text001|The value of the field after you insert the record is %1.|  
  
```  
  
CustomerRecref.OPEN(18);  
MyFieldRef := CustomerRecref.FIELD(1);  
CustomerRecref.INIT;  
MESSAGE(‘%1’, MyFieldRef.VALUE);  
MyFieldRef.VALUE := '1120';  
CustomerRecref.INSERT;  
MESSAGE(‘%1’, MyFieldRef.VALUE);  
  
```  
  
## See Also  
 [RecordRef Data Type](RecordRef-Data-Type.md)