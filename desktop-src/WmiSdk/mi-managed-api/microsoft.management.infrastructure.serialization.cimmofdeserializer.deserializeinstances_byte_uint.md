---
description: 'Дополнительные сведения о методе: Циммофдесериализер. Десериализеинстанцес (Byte [], UInt32)'
title: Циммофдесериализер. Десериализеинстанцес, метод (Byte [], UInt32) (Microsoft. Management. инфраструктура. Serialization)
TOCTitle: CimMofDeserializer.DeserializeInstances method (Byte[], UInt32) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeInstances(System.Byte[],System.UInt32@)
ms.date: 11/14/2019
mtps_version: v=VS.85
dev_langs:
- csharp
- c++
- fsharp
- vb
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeInstances
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: 90cc4f9d88afa9f4ec566ff4733995bce8160eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539775"
---
# <a name="cimmofdeserializerdeserializeinstances-method-byteuint32"></a>Циммофдесериализер. Десериализеинстанцес, метод (Byte \[ \] , UInt32)

Десериализует экземпляры CIM на основе сериализованных данных.

**Пространство имен:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))  
**Сборка:**  Microsoft. Management. Infrastructure (в Microsoft.Management.Infrastructure.dll)  

## <a name="syntax"></a>Синтаксис

``` csharp
public IEnumerable<CimInstance> DeserializeInstances(
    byte[] serializedData,
    ref uint offset
)
```

``` c++
public:
IEnumerable<CimInstance^>^ DeserializeInstances(
    array<unsigned char>^ serializedData,
    unsigned int% offset
)
```

``` fsharp
member DeserializeInstances : 
        serializedData:byte[] *
        offset:uint32 byref -> IEnumerable<CimInstance>
```

``` vb
Public Function DeserializeInstances (
    serializedData As Byte(),
    ByRef offset As UInteger
) As IEnumerable(CimInstance)
```

#### <a name="parameters"></a>Параметры

  - сериализеддата  
    Тип: [System. Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]
    
    Буфер, содержащий сериализованные данные.

<!-- end list -->

  - offset  
    Тип: [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)
    
    Смещение в байтах к расположению, с которого начинается чтение данных. Когда метод возвращает значение, смещение будет указывать на следующий байт после десериализованных экземпляров.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))\>

Интерфейс [IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) , который может использоваться для перечисления классов CIM.

## <a name="see-also"></a>См. также раздел

[Класс CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))  
[Пространство имен Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))
