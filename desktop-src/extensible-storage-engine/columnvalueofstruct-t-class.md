---
description: 'Дополнительные сведения о: Колумнвалуеофструкт <T> Class'
title: Класс ColumnValueOfStruct(T)
TOCTitle: ColumnValueOfStruct(T) class
ms:assetid: T:Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
ms:mtpsurl: https://msdn.microsoft.com/library/Dn334171(v=EXCHG.10)
ms:contentKeyID: 55100962
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 82083adcaaf0d9f5b4f2a720da83e95cd4b39401
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "104351092"
---
# <a name="columnvalueofstructt-class"></a>\<T\>Класс колумнвалуеофструкт

Задайте столбец типа структуры (например, Int32/GUID).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[System.Object](/dotnet/api/system.object)  
  [Microsoft. ISAM. ESENT. Interop. Колумнвалуе](./columnvalue-class.md)  
    Microsoft. ISAM. ESENT. Interop. Колумнвалуеофструкт\<T\>  
      

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public MustInherit Class ColumnValueOfStruct(Of T As {Structure, New, IEquatable(Of T)}) _
    Inherits ColumnValue
'Usage
Dim instance As ColumnValueOfStruct(Of T)
```

``` csharp
public abstract class ColumnValueOfStruct<T> : ColumnValue
where T : struct, new(), IEquatable<T>
```

#### <a name="type-parameters"></a>Параметры типа

  - T  
    Тип для установки.

## <a name="thread-safety"></a>Потокобезопасность

Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными. Потокобезопасная работа с членами экземпляров типа не гарантируется.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[\<T\>Элементы колумнвалуеофструкт](./columnvalueofstruct-t-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Производные типы

[System.Object](/dotnet/api/system.object)  
  [Microsoft. ISAM. ESENT. Interop. Колумнвалуе](./columnvalue-class.md)  
    Microsoft. ISAM. ESENT. Interop. Колумнвалуеофструкт\<T\>  
      [Microsoft. ISAM. ESENT. Interop. Булколумнвалуе](./boolcolumnvalue-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Битеколумнвалуе](./bytecolumnvalue-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Датетимеколумнвалуе](./datetimecolumnvalue-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Даублеколумнвалуе](./doublecolumnvalue-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Флоатколумнвалуе](./floatcolumnvalue-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Гуидколумнвалуе](./guidcolumnvalue-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Int16ColumnValue](./int16columnvalue-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Int32ColumnValue](./int32columnvalue-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Int64ColumnValue](./int64columnvalue-class.md)  
      [Microsoft. ISAM. ESENT. Interop. UInt16ColumnValue](./uint16columnvalue-class.md)  
      [Microsoft. ISAM. ESENT. Interop. UInt32ColumnValue](./uint32columnvalue-class.md)  
      [Microsoft. ISAM. ESENT. Interop. UInt64ColumnValue](./uint64columnvalue-class.md)