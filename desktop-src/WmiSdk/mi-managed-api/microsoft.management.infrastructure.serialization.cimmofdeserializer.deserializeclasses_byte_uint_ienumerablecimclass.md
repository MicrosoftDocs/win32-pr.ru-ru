---
description: 'Дополнительные сведения о методе: Циммофдесериализер. Десериализеклассес (Byte [], UInt32, IEnumerable <CimClass> )'
title: Метод Циммофдесериализер. Десериализеклассес (Byte [], UInt32, IEnumerable (Цимкласс)) (Microsoft. Management. инфраструктура. Serialization)
TOCTitle: CimMofDeserializer.DeserializeClasses method (Byte[], UInt32, IEnumerable(CimClass)) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses(System.Byte[],System.UInt32@,System.Collections.Generic.IEnumerable{Microsoft.Management.Infrastructure.CimClass})
ms.date: 11/13/2019
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
ms.openlocfilehash: edcdb84e9c3a3fe7a070263385c9ee6551341152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719688"
---
# <a name="cimmofdeserializerdeserializeclasses-method-byteuint32ienumerablecimclass"></a><span data-ttu-id="264f9-103">Циммофдесериализер. Десериализеклассес, метод (Byte \[ \] , UInt32, IEnumerable \<CimClass\> )</span><span class="sxs-lookup"><span data-stu-id="264f9-103">CimMofDeserializer.DeserializeClasses method (Byte\[\], UInt32, IEnumerable\<CimClass\>)</span></span>

<span data-ttu-id="264f9-104">Десериализует классы CIM на основе сериализованных данных и коллекцию родительских классов CIM.</span><span class="sxs-lookup"><span data-stu-id="264f9-104">Deserializes CIM classes based on serialized data, and a collection of parent CIM classes.</span></span>

<span data-ttu-id="264f9-105">**Пространство имен:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="264f9-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="264f9-106">**Сборка:**  Microsoft. Management. Infrastructure (в Microsoft.Management.Infrastructure.dll)</span><span class="sxs-lookup"><span data-stu-id="264f9-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="264f9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="264f9-107">Syntax</span></span>

``` csharp
public IEnumerable<CimClass> DeserializeClasses(
    byte[] serializedData,
    ref uint offset,
    IEnumerable<CimClass> classes
)
```

``` c++
public:
IEnumerable<CimClass^>^ DeserializeClasses(
    array<unsigned char>^ serializedData,
    unsigned int% offset,
    IEnumerable<CimClass^>^ classes
)
```

``` fsharp
member DeserializeClasses : 
        serializedData:byte[] *
        offset:uint32 byref *
        classes:IEnumerable<CimClass> -> IEnumerable<CimClass>
```

``` vb
Public Function DeserializeClasses (
    serializedData As Byte(),
    ByRef offset As UInteger,
    classes As IEnumerable(Of CimClass)
) As IEnumerable(CimClass)
```

#### <a name="parameters"></a><span data-ttu-id="264f9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="264f9-108">Parameters</span></span>

  - <span data-ttu-id="264f9-109">сериализеддата</span><span class="sxs-lookup"><span data-stu-id="264f9-109">serializedData</span></span>  
    <span data-ttu-id="264f9-110">Тип: [System. Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span><span class="sxs-lookup"><span data-stu-id="264f9-110">Type: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span></span>
    
    <span data-ttu-id="264f9-111">Буфер, содержащий сериализованные данные.</span><span class="sxs-lookup"><span data-stu-id="264f9-111">A buffer that contains the serialized data.</span></span>

<!-- end list -->

  - <span data-ttu-id="264f9-112">offset</span><span class="sxs-lookup"><span data-stu-id="264f9-112">offset</span></span>  
    <span data-ttu-id="264f9-113">Тип: [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="264f9-113">Type: [System.UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="264f9-114">Смещение в байтах к расположению, с которого начинается чтение данных.</span><span class="sxs-lookup"><span data-stu-id="264f9-114">The byte offset to the location at which to begin reading the data.</span></span> <span data-ttu-id="264f9-115">Когда метод возвращает значение, смещение будет указывать на следующий байт после десериализованных классов.</span><span class="sxs-lookup"><span data-stu-id="264f9-115">When the method returns, the offset will be pointing to the next byte after the deserialized classes.</span></span>

<!-- end list -->

  - <span data-ttu-id="264f9-116">-классы;</span><span class="sxs-lookup"><span data-stu-id="264f9-116">classes</span></span>  
    <span data-ttu-id="264f9-117">Тип: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="264f9-117">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span></span>
    
    <span data-ttu-id="264f9-118">Необязательный кэш родительских классов CIM.</span><span class="sxs-lookup"><span data-stu-id="264f9-118">An optional cache of parent CIM classes.</span></span>

#### <a name="return-value"></a><span data-ttu-id="264f9-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="264f9-119">Return value</span></span>

<span data-ttu-id="264f9-120">Тип: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="264f9-120">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span></span>

<span data-ttu-id="264f9-121">Интерфейс [IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) , который может использоваться для перечисления классов CIM.</span><span class="sxs-lookup"><span data-stu-id="264f9-121">An [IEnumerable\<T\>](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) interface that can be used to enumerate the CIM classes.</span></span>

## <a name="see-also"></a><span data-ttu-id="264f9-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="264f9-122">See also</span></span>

<span data-ttu-id="264f9-123">[Класс Цимкласс](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="264f9-123">[CimClass class](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span></span>  
<span data-ttu-id="264f9-124">[Пространство имен Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="264f9-124">[Microsoft.Management.Infrastructure.Serialization namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
