---
description: 'Дополнительные сведения о методе: Датетимеколумнвалуе. Жетвалуефромбитес'
title: Датетимеколумнвалуе. Жетвалуефромбитес, метод
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.DateTimeColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.datetimecolumnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55101200
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.DateTimeColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.DateTimeColumnValue.GetValueFromBytes
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 88ab0291e21839ccb666a3d9343a79787a5dad48c8ab8debbd1aafd17a8ab573
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119117534"
---
# <a name="datetimecolumnvaluegetvaluefrombytes-method"></a>Датетимеколумнвалуе. Жетвалуефромбитес, метод

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

  - Значение  
    Тип \[\]  
    
    Массив байтов.

<!-- end list -->

  - startIndex  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Начальная позицией в байтах.

<!-- end list -->

  - количество  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Число байтов для декодирования.

<!-- end list -->

  - Err  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Ошибка, возвращенная из ESENT.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс Датетимеколумнвалуе](./datetimecolumnvalue-class.md)

[Элементы Датетимеколумнвалуе](./datetimecolumnvalue-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
