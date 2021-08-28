---
description: 'Дополнительные сведения о: конструктор Есентинвалидколумнексцептион (SerializationInfo, StreamingContext)'
title: Конструктор Есентинвалидколумнексцептион (SerializationInfo, StreamingContext)
TOCTitle: EsentInvalidColumnException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentInvalidColumnException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidcolumnexception.esentinvalidcolumnexception(v=EXCHG.10)
ms:contentKeyID: 55101741
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidColumnException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c042708140a5492e79aaa994226b10d9d2fc78ffddeaf82ce76e0532eabf0a22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723954"
---
# <a name="esentinvalidcolumnexception-constructor-serializationinfo-streamingcontext"></a>Конструктор Есентинвалидколумнексцептион (SerializationInfo, StreamingContext)

Инициализирует новый экземпляр класса Есентинвалидколумнексцептион. Этот конструктор используется для десериализации сериализованного исключения.

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

Dim instance As New EsentInvalidColumnException(info, context)
```

``` csharp
protected EsentInvalidColumnException(
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

[Класс Есентинвалидколумнексцептион](./esentinvalidcolumnexception-class.md)

[Элементы Есентинвалидколумнексцептион](./esentinvalidcolumnexception-members.md)

[Перегрузка Есентинвалидколумнексцептион](./esentinvalidcolumnexception-constructor2.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
