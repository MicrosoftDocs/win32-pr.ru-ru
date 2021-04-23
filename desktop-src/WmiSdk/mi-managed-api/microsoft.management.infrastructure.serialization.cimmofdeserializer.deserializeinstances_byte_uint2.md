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
# <a name="cimmofdeserializerdeserializeinstances-method-byteuint32-onclassneeded-getincludedfilecontent"></a><span data-ttu-id="dfe07-103">Циммофдесериализер. Десериализеинстанцес, метод (Byte \[ \] , UInt32, Онкласснидед, жетинклудедфилеконтент)</span><span class="sxs-lookup"><span data-stu-id="dfe07-103">CimMofDeserializer.DeserializeInstances method (Byte\[\], UInt32, OnClassNeeded, GetIncludedFileContent)</span></span>

<span data-ttu-id="dfe07-104">Десериализует экземпляры CIM на основе сериализованных данных и обратных вызовов.</span><span class="sxs-lookup"><span data-stu-id="dfe07-104">Deserializes CIM instances based on serialized data, and callbacks.</span></span>

<span data-ttu-id="dfe07-105">**Пространство имен:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dfe07-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="dfe07-106">**Сборка:**  Microsoft. Management. Infrastructure (в Microsoft.Management.Infrastructure.dll)</span><span class="sxs-lookup"><span data-stu-id="dfe07-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="dfe07-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dfe07-107">Syntax</span></span>

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

#### <a name="parameters"></a><span data-ttu-id="dfe07-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="dfe07-108">Parameters</span></span>

  - <span data-ttu-id="dfe07-109">сериализеддата</span><span class="sxs-lookup"><span data-stu-id="dfe07-109">serializedData</span></span>  
    <span data-ttu-id="dfe07-110">Тип: [System. Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span><span class="sxs-lookup"><span data-stu-id="dfe07-110">Type: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span></span>
    
    <span data-ttu-id="dfe07-111">Буфер, содержащий сериализованные данные.</span><span class="sxs-lookup"><span data-stu-id="dfe07-111">A buffer that contains the serialized data.</span></span>

<!-- end list -->

  - <span data-ttu-id="dfe07-112">offset</span><span class="sxs-lookup"><span data-stu-id="dfe07-112">offset</span></span>  
    <span data-ttu-id="dfe07-113">Тип: [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="dfe07-113">Type: [System.UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="dfe07-114">Смещение в байтах к расположению, с которого начинается чтение данных.</span><span class="sxs-lookup"><span data-stu-id="dfe07-114">The byte offset to the location at which to begin reading the data.</span></span> <span data-ttu-id="dfe07-115">Когда метод возвращает значение, смещение будет указывать на следующий байт после десериализованных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="dfe07-115">When the method returns, the offset will be pointing to the next byte after the deserialized instances.</span></span>

<!-- end list -->

  - <span data-ttu-id="dfe07-116">онкласснидедкаллбакк</span><span class="sxs-lookup"><span data-stu-id="dfe07-116">onClassNeededCallback</span></span>  
    <span data-ttu-id="dfe07-117">Тип: [онкласснидед](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)</span><span class="sxs-lookup"><span data-stu-id="dfe07-117">Type: [OnClassNeeded](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)</span></span>
    
    <span data-ttu-id="dfe07-118">Функция обратного вызова, используемая для предоставления запрошенного объекта класса во время десериализации.</span><span class="sxs-lookup"><span data-stu-id="dfe07-118">A callback function used to provide a requested class object during deserialization.</span></span>

<!-- end list -->

  - <span data-ttu-id="dfe07-119">жетинклудедфилекаллбакк</span><span class="sxs-lookup"><span data-stu-id="dfe07-119">getIncludedFileCallback</span></span>  
    <span data-ttu-id="dfe07-120">Тип: [жетинклудедфилеконтент](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)</span><span class="sxs-lookup"><span data-stu-id="dfe07-120">Type: [GetIncludedFileContent](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)</span></span>
    
    <span data-ttu-id="dfe07-121">Функция обратного вызова, используемая для предоставления содержимого буфера файла указанного файла.</span><span class="sxs-lookup"><span data-stu-id="dfe07-121">A callback function used to provide the file buffer contents of a specified file.</span></span>

#### <a name="return-value"></a><span data-ttu-id="dfe07-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dfe07-122">Return value</span></span>

<span data-ttu-id="dfe07-123">Тип: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="dfe07-123">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))\></span></span>

<span data-ttu-id="dfe07-124">Интерфейс [IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) , который может использоваться для перечисления классов CIM.</span><span class="sxs-lookup"><span data-stu-id="dfe07-124">An [IEnumerable\<T\>](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) interface that can be used to enumerate the CIM classes.</span></span>

## <a name="see-also"></a><span data-ttu-id="dfe07-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dfe07-125">See also</span></span>

<span data-ttu-id="dfe07-126">[Класс CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dfe07-126">[CimInstance class](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))</span></span>  
<span data-ttu-id="dfe07-127">[Пространство имен Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dfe07-127">[Microsoft.Management.Infrastructure.Serialization namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
