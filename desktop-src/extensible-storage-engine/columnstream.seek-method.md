---
description: 'Дополнительные сведения о методе: Колумнстреам. Seek'
title: Колумнстреам. Seek, метод
TOCTitle: 'Seek method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.Seek(System.Int64,System.IO.SeekOrigin)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.seek(v=EXCHG.10)
ms:contentKeyID: 55100949
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Seek
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.Seek
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5489bb0ee9a4a1550166e14a945a2a6d58c45af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543439"
---
# <a name="columnstreamseek-method"></a>Колумнстреам. Seek, метод

Задает позицию в текущем потоке.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Overrides Function Seek ( _
    offset As Long, _
    origin As SeekOrigin _
) As Long
'Usage
Dim instance As ColumnStream
Dim offset As Long
Dim origin As SeekOrigin
Dim returnValue As Long

returnValue = instance.Seek(offset, origin)
```

``` csharp
public override long Seek(
    long offset,
    SeekOrigin origin
)
```

#### <a name="parameters"></a>Параметры

  - offset  
    Тип: [System. Int64](/dotnet/api/system.int64)  
    
    Смещение в байтах относительно параметра origin.

<!-- end list -->

  - Исходное подключение  
    Тип: [System. IO. SeekOrigin](/dotnet/api/system.io.seekorigin)  
    
    Значение SeekOrigin, указывающее точку ссылки для новой позиции.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [System. Int64](/dotnet/api/system.int64)  
Новая позицией в текущем потоке.  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс Колумнстреам](./columnstream-class.md)

[Элементы Колумнстреам](./columnstream-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
