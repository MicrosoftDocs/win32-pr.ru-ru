---
description: 'Дополнительные сведения о: конструктор Есентексцептион (String)'
title: Конструктор Есентексцептион (String) (Microsoft. ISAM. ESENT)
TOCTitle: EsentException constructor (String)
ms:assetid: M:Microsoft.Isam.Esent.EsentException.#ctor(System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.esentexception.esentexception(v=EXCHG.10)
ms:contentKeyID: 55100720
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.EsentException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 22a93625b7becbe083a42fbd6fcc71ad801173ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703152"
---
# <a name="esentexception-constructor-string"></a>Конструктор Есентексцептион (String)

Инициализирует новый экземпляр класса Есентексцептион с указанным сообщением об ошибке.

**Пространство имен:**  [Microsoft. ISAM. ESENT](./microsoft.isam.esent-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Protected Sub New ( _
    message As String _
)
'Usage
Dim message As String

Dim instance As New EsentException(message)
```

``` csharp
protected EsentException(
    string message
)
```

#### <a name="parameters"></a>Параметры

  - message  
    Тип: [System. String](/dotnet/api/system.string)  
    
    Сообщение, описывающее ошибку.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс Есентексцептион](./esentexception-class.md)

[Элементы Есентексцептион](./esentexception-members.md)

[Перегрузка Есентексцептион](./esentexception-constructor.md)

[Пространство имен Microsoft. ISAM. ESENT](./microsoft.isam.esent-namespace.md)
