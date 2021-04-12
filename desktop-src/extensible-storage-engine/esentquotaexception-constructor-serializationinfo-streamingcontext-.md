---
description: 'Дополнительные сведения о: конструктор Есенткуотаексцептион (SerializationInfo, StreamingContext)'
title: Конструктор Есенткуотаексцептион (SerializationInfo, StreamingContext)
TOCTitle: EsentQuotaException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentQuotaException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentquotaexception.esentquotaexception(v=EXCHG.10)
ms:contentKeyID: 55102338
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentQuotaException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 36748053b8b9b48041c07ff51c99c0144093a9ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348325"
---
# <a name="esentquotaexception-constructor-serializationinfo-streamingcontext"></a>Конструктор Есенткуотаексцептион (SerializationInfo, StreamingContext)

Инициализирует новый экземпляр класса Есенткуотаексцептион. Этот конструктор используется для десериализации сериализованного исключения.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentQuotaException(info, context)
```

``` csharp
protected EsentQuotaException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a>Параметры

  - сведения  
    Тип: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)  
    
    Данные, необходимые для десериализации объекта.

<!-- end list -->

  - контекст  
    Тип: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)  
    
    Контекст десериализации.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс EsentQuotaException](./esentquotaexception-class.md)

[Элементы Есенткуотаексцептион](./esentquotaexception-members.md)

[Перегрузка Есенткуотаексцептион](./esentquotaexception-constructor.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
