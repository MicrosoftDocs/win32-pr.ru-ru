---
description: 'Дополнительные сведения о методе: Циммофдесериализер. Create (строка, UInt32)'
title: Метод CimMofDeserializer.Create (String, UInt32) (Microsoft.Management.Infrastructure.Serialization)
TOCTitle: CimMofDeserializer.Create method (String, UInt32) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.Create(System.String,System.UInt32)
ms.date: 11/13/2019
mtps_version: v=VS.85
f1_keywords:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.Create
- Microsoft::Management::Infrastructure::.Serialization::CimMofDeserializer::Create
dev_langs:
- CSharp
- C++
- VB
- FSharp
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.Create
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: c8f9b30fb0b9b06c2f1aaeb1fcfcaf65fb3606d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081312"
---
# <a name="cimmofdeserializercreate-method-string-uint32"></a>Циммофдесериализер. Create, метод (String, UInt32)

Создает и инициализирует пользовательский десериализатор на основе указанного формата и флагов.

**Пространство имен:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))  
**Сборка:**  Microsoft. Management. Infrastructure (в Microsoft.Management.Infrastructure.dll)  

## <a name="syntax"></a>Синтаксис

``` csharp
public static CimMofDeserializer Create(
    string format,
    uint flags
)
```

``` c++
public:
static CimMofDeserializer^ Create(
    String^ format,
    unsigned int flags
)
```

``` fsharp
static member Create : 
        format:string *
        flags:uint32 -> CimMofDeserializer
```

``` vb
Public Shared Function Create (
    format As String,
    flags As UInteger
) As CimMofDeserializer
```

#### <a name="parameters"></a>Параметры

  - format  
    Тип: [System. String](/dotnet/api/system.string?view=netframework-4.8)
    
    Формат сериализации. Поддерживается только "MI_XML".

<!-- end list -->

  - flags  
    Тип: [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)
    
    Флаги сериализации. Должно быть равно 0.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [Microsoft. Management. Infrastructure. Serialization. Циммофдесериализер](microsoft.management.infrastructure.serialization.cimmofdeserializer.md)

Созданный объект десериализатора.

## <a name="see-also"></a>См. также раздел

[Класс Циммофдесериализер](microsoft.management.infrastructure.serialization.cimmofdeserializer.md) 
 [Пространство имен Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))
