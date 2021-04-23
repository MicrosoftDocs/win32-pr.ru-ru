---
description: 'Дополнительные сведения о методе: Циммофдесериализер. Десериализеклассес (Byte [], UInt32)'
title: Циммофдесериализер. Десериализеклассес, метод (Byte [], UInt32) (Microsoft. Management. инфраструктура. Serialization)
TOCTitle: CimMofDeserializer.DeserializeClasses method (Byte[], UInt32) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses(System.Byte[],System.UInt32@)
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
ms.openlocfilehash: 983fa9e8fe36b872d05c3140c74f572b7d1ebf50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539778"
---
# <a name="cimmofdeserializerdeserializeclasses-method-byteuint32"></a><span data-ttu-id="f8149-103">Циммофдесериализер. Десериализеклассес, метод (Byte \[ \] , UInt32)</span><span class="sxs-lookup"><span data-stu-id="f8149-103">CimMofDeserializer.DeserializeClasses method (Byte\[\], UInt32)</span></span>

<span data-ttu-id="f8149-104">Десериализует классы CIM на основе сериализованных данных.</span><span class="sxs-lookup"><span data-stu-id="f8149-104">Deserializes CIM classes based on serialized data.</span></span>

<span data-ttu-id="f8149-105">**Пространство имен:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f8149-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="f8149-106">**Сборка:**  Microsoft. Management. Infrastructure (в Microsoft.Management.Infrastructure.dll)</span><span class="sxs-lookup"><span data-stu-id="f8149-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="f8149-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8149-107">Syntax</span></span>

``` csharp
public IEnumerable<CimClass> DeserializeClasses(
    byte[] serializedData,
    ref uint offset
)
```

``` c++
public:
IEnumerable<CimClass^>^ DeserializeClasses(
    array<unsigned char>^ serializedData,
    unsigned int% offset
)
```

``` fsharp
member DeserializeClasses : 
        serializedData:byte[] *
        offset:uint32 byref -> IEnumerable<CimClass>
```

``` vb
Public Function DeserializeClasses (
    serializedData As Byte(),
    ByRef offset As UInteger
) As IEnumerable(CimClass)
```

#### <a name="parameters"></a><span data-ttu-id="f8149-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8149-108">Parameters</span></span>

  - <span data-ttu-id="f8149-109">сериализеддата</span><span class="sxs-lookup"><span data-stu-id="f8149-109">serializedData</span></span>  
    <span data-ttu-id="f8149-110">Тип: [System. Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span><span class="sxs-lookup"><span data-stu-id="f8149-110">Type: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span></span>
    
    <span data-ttu-id="f8149-111">Буфер, содержащий сериализованные данные.</span><span class="sxs-lookup"><span data-stu-id="f8149-111">A buffer that contains the serialized data.</span></span>

<!-- end list -->

  - <span data-ttu-id="f8149-112">offset</span><span class="sxs-lookup"><span data-stu-id="f8149-112">offset</span></span>  
    <span data-ttu-id="f8149-113">Тип: [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="f8149-113">Type: [System.UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="f8149-114">Смещение в байтах к расположению, с которого начинается чтение данных.</span><span class="sxs-lookup"><span data-stu-id="f8149-114">The byte offset to the location at which to begin reading the data.</span></span> <span data-ttu-id="f8149-115">Когда метод возвращает значение, смещение будет указывать на следующий байт после десериализованных классов.</span><span class="sxs-lookup"><span data-stu-id="f8149-115">When the method returns, the offset will be pointing to the next byte after the deserialized classes.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f8149-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f8149-116">Return value</span></span>

<span data-ttu-id="f8149-117">Тип: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="f8149-117">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span></span>

<span data-ttu-id="f8149-118">Интерфейс [IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) , который может использоваться для перечисления классов CIM.</span><span class="sxs-lookup"><span data-stu-id="f8149-118">An [IEnumerable\<T\>](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) interface that can be used to enumerate the CIM classes.</span></span>

## <a name="see-also"></a><span data-ttu-id="f8149-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8149-119">See also</span></span>

<span data-ttu-id="f8149-120">[Класс Цимкласс](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f8149-120">[CimClass class](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span></span>  
<span data-ttu-id="f8149-121">[Пространство имен Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f8149-121">[Microsoft.Management.Infrastructure.Serialization namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
