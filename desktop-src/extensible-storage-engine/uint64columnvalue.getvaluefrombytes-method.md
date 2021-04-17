---
description: 'Дополнительные сведения о методе: UInt64ColumnValue. Жетвалуефромбитес'
title: UInt64ColumnValue. Жетвалуефромбитес, метод
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.UInt64ColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.uint64columnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55104084
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.UInt64ColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.UInt64ColumnValue.GetValueFromBytes
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0ccf4a0d85c6d712a81222f77b954d46f55a28df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711305"
---
# <a name="uint64columnvaluegetvaluefrombytes-method"></a>UInt64ColumnValue. Жетвалуефромбитес, метод

Данные, полученные из ESENT, декодируются и задают значение в объекте Колумнвалуе.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Protected Overrides Sub GetValueFromBytes ( _
    value As Byte(), _
    startIndex As Integer, _
    count As Integer, _
    err As Integer _
)
'Usage
Dim value As Byte()
Dim startIndex As Integer
Dim count As Integer
Dim err As Integer

Me.GetValueFromBytes(value, startIndex, _
    count, err)
```

``` csharp
protected override void GetValueFromBytes(
    byte[] value,
    int startIndex,
    int count,
    int err
)
```

#### <a name="parameters"></a>Параметры

  - значение  
    Тип \[\]  
    
    Массив байтов.

<!-- end list -->

  - startIndex  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Начальная позицией в байтах.

<!-- end list -->

  - count  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Число байтов для декодирования.

<!-- end list -->

  - Err  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Ошибка, возвращенная из ESENT.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс UInt64ColumnValue](./uint64columnvalue-class.md)

[Элементы UInt64ColumnValue](./uint64columnvalue-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
