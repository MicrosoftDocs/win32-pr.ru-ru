---
description: 'Дополнительные сведения о методе: Циммофдесериализер. Десериализеинстанцес (Byte [], UInt32, Онкласснидед, Жетинклудедфилеконтент)'
title: Метод Циммофдесериализер. Десериализеинстанцес (Byte [], UInt32, Онкласснидед, Жетинклудедфилеконтент) (Microsoft. Management. инфраструктура. Serialization)
TOCTitle: CimMofDeserializer.DeserializeInstances method (Byte[], UInt32, OnClassNeeded, GetIncludedFileContent) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeInstances(System.Byte[],System.UInt32@,Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded,Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent)
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
ms.openlocfilehash: 17a8a84f841f07439b716909fbc8d63232032263
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719414"
---
# <a name="cimmofdeserializerdeserializeinstances-method-byteuint32-onclassneeded-getincludedfilecontent"></a>Циммофдесериализер. Десериализеинстанцес, метод (Byte \[ \] , UInt32, Онкласснидед, жетинклудедфилеконтент)

Десериализует экземпляры CIM на основе сериализованных данных и обратных вызовов.

**Пространство имен:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))  
**Сборка:**  Microsoft. Management. Infrastructure (в Microsoft.Management.Infrastructure.dll)  

## <a name="syntax"></a>Синтаксис

``` csharp
public IEnumerable<CimInstance> DeserializeInstances(
    byte[] serializedData,
    ref uint offset,
    OnClassNeeded onClassNeededCallback,
    GetIncludedFileContent getIncludedFileCallback
)
```

``` c++
public:
IEnumerable<CimInstance^>^ DeserializeInstances(
    array<unsigned char>^ serializedData,
    unsigned int% offset,
    OnClassNeeded^ onClassNeededCallback,
    GetIncludedFileContent^ getIncludedFileCallback
)
```

``` fsharp
member DeserializeInstances : 
        serializedData:byte[] *
        offset:uint32 byref *
        onClassNeededCallback:OnClassNeeded *
        getIncludedFileCallback:GetIncludedFileContent -> IEnumerable<CimInstance>
```

``` vb
Public Function DeserializeInstances (
    serializedData As Byte(),
    ByRef offset As UInteger,
    onClassNeededCallback As OnClassNeeded,
    getIncludedFileCallback As GetIncludedFileContent
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

<!-- end list -->

  - онкласснидедкаллбакк  
    Тип: [онкласснидед](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)
    
    Функция обратного вызова, используемая для предоставления запрошенного объекта класса во время десериализации.

<!-- end list -->

  - жетинклудедфилекаллбакк  
    Тип: [жетинклудедфилеконтент](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)
    
    Функция обратного вызова, используемая для предоставления содержимого буфера файла указанного файла.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))\>

Интерфейс [IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) , который может использоваться для перечисления классов CIM.

## <a name="see-also"></a>См. также раздел

[Класс CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))  
[Пространство имен Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))
