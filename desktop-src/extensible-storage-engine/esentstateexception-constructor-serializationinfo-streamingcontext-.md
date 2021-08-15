---
description: 'Дополнительные сведения о: конструктор Есентстатиксцептион (SerializationInfo, StreamingContext)'
title: Конструктор Есентстатиксцептион (SerializationInfo, StreamingContext)
TOCTitle: EsentStateException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentStateException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstateexception.esentstateexception(v=EXCHG.10)
ms:contentKeyID: 55102710
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentStateException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 935cf9cbe6120e305de3ed9578e607fb366d36b66d10ccbb33e17a3a2ce71153
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118769667"
---
# <a name="esentstateexception-constructor-serializationinfo-streamingcontext"></a>Конструктор Есентстатиксцептион (SerializationInfo, StreamingContext)

Инициализирует новый экземпляр класса Есентстатиксцептион. Этот конструктор используется для десериализации сериализованного исключения.

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

Dim instance As New EsentStateException(info, context)
```

``` csharp
protected EsentStateException(
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

[Класс EsentStateException](./esentstateexception-class.md)

[Элементы Есентстатиксцептион](./esentstateexception-members.md)

[Перегрузка Есентстатиксцептион](./esentstateexception-constructor.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
