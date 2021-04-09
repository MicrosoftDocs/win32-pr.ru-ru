---
description: 'Дополнительные сведения о методе: Колумнстреам. Write'
title: Колумнстреам. Write, метод
TOCTitle: 'Write method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.Write(System.Byte[],System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.write(v=EXCHG.10)
ms:contentKeyID: 55100987
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Write
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.Write
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 77b62e7dd028da3452082c973690ce0c0210b438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081428"
---
# <a name="columnstreamwrite-method"></a>Колумнстреам. Write, метод

Записывает последовательность байтов в текущий поток и перемещает текущую позицию внутри потока на число записанных байтов.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Overrides Sub Write ( _
    buffer As Byte(), _
    offset As Integer, _
    count As Integer _
)
'Usage
Dim instance As ColumnStream
Dim buffer As Byte()
Dim offset As Integer
Dim count As Integer

instance.Write(buffer, offset, count)
```

``` csharp
public override void Write(
    byte[] buffer,
    int offset,
    int count
)
```

#### <a name="parameters"></a>Параметры

  - buffer  
    Тип \[\]  
    
    Буфер, из которого производится запись.

<!-- end list -->

  - offset  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Смещение в буфере для записи.

<!-- end list -->

  - count  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Количество записываемых байтов.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс Колумнстреам](./columnstream-class.md)

[Элементы Колумнстреам](./columnstream-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
