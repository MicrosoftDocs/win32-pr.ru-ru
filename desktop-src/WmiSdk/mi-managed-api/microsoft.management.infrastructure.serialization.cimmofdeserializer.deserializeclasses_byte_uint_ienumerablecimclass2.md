---
description: 'Дополнительные сведения о методе: Циммофдесериализер. Десериализеклассес (Byte [], UInt32, IEnumerable <CimClass> , онкласснидед, жетинклудедфилеконтент)'
title: Метод Циммофдесериализер. Десериализеклассес (Byte [], UInt32, IEnumerable (Цимкласс), Онкласснидед, Жетинклудедфилеконтент) (Microsoft. Management. инфраструктура. Serialization)
TOCTitle: CimMofDeserializer.DeserializeClasses method (Byte[], UInt32, IEnumerable(CimClass), OnClassNeeded, GetIncludedFileContent) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses(System.Byte[],System.UInt32@,System.Collections.Generic.IEnumerable{Microsoft.Management.Infrastructure.CimClass},Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded,Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent)
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
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: 5fd78e1c377db3a8fba0005539bb5d7c28cab232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344335"
---
# <a name="cimmofdeserializerdeserializeclasses-method-byteuint32ienumerablecimclass-onclassneeded-getincludedfilecontent"></a><span data-ttu-id="f5dd0-103">Метод Циммофдесериализер. Десериализеклассес (Byte \[ \] , UInt32, IEnumerable \<CimClass\> , онкласснидед, жетинклудедфилеконтент)</span><span class="sxs-lookup"><span data-stu-id="f5dd0-103">CimMofDeserializer.DeserializeClasses method (Byte\[\], UInt32, IEnumerable\<CimClass\>, OnClassNeeded, GetIncludedFileContent)</span></span>

<span data-ttu-id="f5dd0-104">Десериализует классы CIM на основе сериализованных данных, коллекции родительских классов CIM и обратных вызовов.</span><span class="sxs-lookup"><span data-stu-id="f5dd0-104">Deserializes CIM classes based on serialized data, a collection of parent CIM classes, and callbacks.</span></span>

<span data-ttu-id="f5dd0-105">**Пространство имен:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f5dd0-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="f5dd0-106">**Сборка:**  Microsoft. Management. Infrastructure (в Microsoft.Management.Infrastructure.dll)</span><span class="sxs-lookup"><span data-stu-id="f5dd0-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="f5dd0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5dd0-107">Syntax</span></span>

``` csharp
public IEnumerable<CimClass> DeserializeClasses(
    byte[] serializedData,
    ref uint offset,
    IEnumerable<CimClass> classes,
    OnClassNeeded onClassNeededCallback,
    GetIncludedFileContent getIncludedFileCallback
)
```

``` c++
public:
IEnumerable<CimClass^>^ DeserializeClasses(
    array<unsigned char>^ serializedData,
    unsigned int% offset,
    IEnumerable<CimClass^>^ classes,
    OnClassNeeded^ onClassNeededCallback,
    GetIncludedFileContent^ getIncludedFileCallback
)
```

``` fsharp
member DeserializeClasses : 
        serializedData:byte[] *
        offset:uint32 byref *
        classes:IEnumerable<CimClass> *
        onClassNeededCallback:OnClassNeeded *
        getIncludedFileCallback:GetIncludedFileContent -> IEnumerable<CimClass>
```

``` vb
Public Function DeserializeClasses (
    serializedData As Byte(),
    ByRef offset As UInteger,
    classes As IEnumerable(Of CimClass),
    onClassNeededCallback As OnClassNeeded,
    getIncludedFileCallback As GetIncludedFileContent
) As IEnumerable(CimClass)
```

#### <a name="parameters"></a><span data-ttu-id="f5dd0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f5dd0-108">Parameters</span></span>

  - <span data-ttu-id="f5dd0-109">сериализеддата</span><span class="sxs-lookup"><span data-stu-id="f5dd0-109">serializedData</span></span>  
    <span data-ttu-id="f5dd0-110">Тип: [System. Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span><span class="sxs-lookup"><span data-stu-id="f5dd0-110">Type: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span></span>
    
    <span data-ttu-id="f5dd0-111">Буфер, содержащий сериализованные данные.</span><span class="sxs-lookup"><span data-stu-id="f5dd0-111">A buffer that contains the serialized data.</span></span>

<!-- end list -->

  - <span data-ttu-id="f5dd0-112">offset</span><span class="sxs-lookup"><span data-stu-id="f5dd0-112">offset</span></span>  
    <span data-ttu-id="f5dd0-113">Тип: [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="f5dd0-113">Type: [System.UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="f5dd0-114">Смещение в байтах к расположению, с которого начинается чтение данных.</span><span class="sxs-lookup"><span data-stu-id="f5dd0-114">The byte offset to the location at which to begin reading the data.</span></span> <span data-ttu-id="f5dd0-115">Когда метод возвращает значение, смещение будет указывать на следующий байт после десериализованных классов.</span><span class="sxs-lookup"><span data-stu-id="f5dd0-115">When the method returns, the offset will be pointing to the next byte after the deserialized classes.</span></span>

<!-- end list -->

  - <span data-ttu-id="f5dd0-116">-классы;</span><span class="sxs-lookup"><span data-stu-id="f5dd0-116">classes</span></span>  
    <span data-ttu-id="f5dd0-117">Тип: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="f5dd0-117">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span></span>
    
    <span data-ttu-id="f5dd0-118">Необязательный кэш родительских классов CIM.</span><span class="sxs-lookup"><span data-stu-id="f5dd0-118">An optional cache of parent CIM classes.</span></span>

<!-- end list -->

  - <span data-ttu-id="f5dd0-119">онкласснидедкаллбакк</span><span class="sxs-lookup"><span data-stu-id="f5dd0-119">onClassNeededCallback</span></span>  
    <span data-ttu-id="f5dd0-120">Тип: [онкласснидед](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)</span><span class="sxs-lookup"><span data-stu-id="f5dd0-120">Type: [OnClassNeeded](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)</span></span>
    
    <span data-ttu-id="f5dd0-121">Функция обратного вызова, используемая для предоставления запрошенного объекта класса во время десериализации.</span><span class="sxs-lookup"><span data-stu-id="f5dd0-121">A callback function used to provide a requested class object during deserialization.</span></span>

<!-- end list -->

  - <span data-ttu-id="f5dd0-122">жетинклудедфилекаллбакк</span><span class="sxs-lookup"><span data-stu-id="f5dd0-122">getIncludedFileCallback</span></span>  
    <span data-ttu-id="f5dd0-123">Тип: [жетинклудедфилеконтент](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)</span><span class="sxs-lookup"><span data-stu-id="f5dd0-123">Type: [GetIncludedFileContent](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)</span></span>
    
    <span data-ttu-id="f5dd0-124">Функция обратного вызова, используемая для предоставления содержимого буфера файла указанного файла.</span><span class="sxs-lookup"><span data-stu-id="f5dd0-124">A callback function used to provide the file buffer contents of a specified file.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f5dd0-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f5dd0-125">Return value</span></span>

<span data-ttu-id="f5dd0-126">Тип: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="f5dd0-126">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span></span>

<span data-ttu-id="f5dd0-127">Интерфейс [IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) , который может использоваться для перечисления классов CIM.</span><span class="sxs-lookup"><span data-stu-id="f5dd0-127">An [IEnumerable\<T\>](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) interface that can be used to enumerate the CIM classes.</span></span>

## <a name="see-also"></a><span data-ttu-id="f5dd0-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f5dd0-128">See also</span></span>

<span data-ttu-id="f5dd0-129">[Класс Цимкласс](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f5dd0-129">[CimClass class](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span></span>  
<span data-ttu-id="f5dd0-130">[Пространство имен Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f5dd0-130">[Microsoft.Management.Infrastructure.Serialization namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
