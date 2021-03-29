---
description: 'Дополнительные сведения о методе: Колумнстреам. Read'
title: Колумнстреам. Read, метод
TOCTitle: 'Read method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.Read(System.Byte[],System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.read(v=EXCHG.10)
ms:contentKeyID: 55100988
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Read
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.Read
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e407a9069807d10eaabf4f7ac3fce3919576bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674245"
---
# <a name="columnstreamread-method"></a>Колумнстреам. Read, метод

Считывает последовательность байтов из текущего потока и перемещает позицию внутри потока на число считанных байтов.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Overrides Function Read ( _
    buffer As Byte(), _
    offset As Integer, _
    count As Integer _
) As Integer
'Usage
Dim instance As ColumnStream
Dim buffer As Byte()
Dim offset As Integer
Dim count As Integer
Dim returnValue As Integer

returnValue = instance.Read(buffer, offset, _
    count)
```

``` csharp
public override int Read(
    byte[] buffer,
    int offset,
    int count
)
```

#### <a name="parameters"></a>Параметры

  - buffer  
    Тип \[\]  
    
    Буфер, в который производится чтение.

<!-- end list -->

  - offset  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Смещение в буфере для чтения.

<!-- end list -->

  - count  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Количество байтов, чтение которых необходимо выполнить.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [System. Int32](/dotnet/api/system.int32)  
Число байтов, считанных в буфер.  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс Колумнстреам](./columnstream-class.md)

[Элементы Колумнстреам](./columnstream-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
