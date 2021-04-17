---
description: 'Дополнительные сведения о методе: Гуидколумнвалуе. Жетвалуефромбитес'
title: Гуидколумнвалуе. Жетвалуефромбитес, метод
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.GuidColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.guidcolumnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55107384
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.GuidColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.GuidColumnValue.GetValueFromBytes
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 06f10cef46603d6cf023ed3786b3c6bbe1b1a3a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711452"
---
# <a name="guidcolumnvaluegetvaluefrombytes-method"></a>Гуидколумнвалуе. Жетвалуефромбитес, метод

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

[Класс Гуидколумнвалуе](./guidcolumnvalue-class.md)

[Элементы Гуидколумнвалуе](./guidcolumnvalue-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
