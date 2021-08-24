---
description: 'Дополнительные сведения о методе: Флоатколумнвалуе. Жетвалуефромбитес'
title: Флоатколумнвалуе. Жетвалуефромбитес, метод
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.FloatColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.floatcolumnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55103242
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.FloatColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.FloatColumnValue.GetValueFromBytes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 329ab0fb3a6d26173623ae8bb3d78506c17b6d1e0b2b7f33f13893b3877d3e4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968784"
---
# <a name="floatcolumnvaluegetvaluefrombytes-method"></a>Флоатколумнвалуе. Жетвалуефромбитес, метод

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

[Класс Флоатколумнвалуе](./floatcolumnvalue-class.md)

[Элементы Флоатколумнвалуе](./floatcolumnvalue-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
