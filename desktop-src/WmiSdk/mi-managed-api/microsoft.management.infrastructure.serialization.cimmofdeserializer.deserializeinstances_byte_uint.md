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
# <a name="cimmofdeserializerdeserializeinstances-method-byteuint32"></a><span data-ttu-id="56a7f-103">Циммофдесериализер. Десериализеинстанцес, метод (Byte \[ \] , UInt32)</span><span class="sxs-lookup"><span data-stu-id="56a7f-103">CimMofDeserializer.DeserializeInstances method (Byte\[\], UInt32)</span></span>

<span data-ttu-id="56a7f-104">Десериализует экземпляры CIM на основе сериализованных данных.</span><span class="sxs-lookup"><span data-stu-id="56a7f-104">Deserializes CIM instances based on serialized data.</span></span>

<span data-ttu-id="56a7f-105">**Пространство имен:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="56a7f-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="56a7f-106">**Сборка:**  Microsoft. Management. Infrastructure (в Microsoft.Management.Infrastructure.dll)</span><span class="sxs-lookup"><span data-stu-id="56a7f-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="56a7f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56a7f-107">Syntax</span></span>

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

#### <a name="parameters"></a><span data-ttu-id="56a7f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="56a7f-108">Parameters</span></span>

  - <span data-ttu-id="56a7f-109">сериализеддата</span><span class="sxs-lookup"><span data-stu-id="56a7f-109">serializedData</span></span>  
    <span data-ttu-id="56a7f-110">Тип: [System. Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span><span class="sxs-lookup"><span data-stu-id="56a7f-110">Type: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span></span>
    
    <span data-ttu-id="56a7f-111">Буфер, содержащий сериализованные данные.</span><span class="sxs-lookup"><span data-stu-id="56a7f-111">A buffer that contains the serialized data.</span></span>

<!-- end list -->

  - <span data-ttu-id="56a7f-112">offset</span><span class="sxs-lookup"><span data-stu-id="56a7f-112">offset</span></span>  
    <span data-ttu-id="56a7f-113">Тип: [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="56a7f-113">Type: [System.UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="56a7f-114">Смещение в байтах к расположению, с которого начинается чтение данных.</span><span class="sxs-lookup"><span data-stu-id="56a7f-114">The byte offset to the location at which to begin reading the data.</span></span> <span data-ttu-id="56a7f-115">Когда метод возвращает значение, смещение будет указывать на следующий байт после десериализованных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="56a7f-115">When the method returns, the offset will be pointing to the next byte after the deserialized instances.</span></span>

#### <a name="return-value"></a><span data-ttu-id="56a7f-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="56a7f-116">Return value</span></span>

<span data-ttu-id="56a7f-117">Тип: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="56a7f-117">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))\></span></span>

<span data-ttu-id="56a7f-118">Интерфейс [IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) , который может использоваться для перечисления классов CIM.</span><span class="sxs-lookup"><span data-stu-id="56a7f-118">An [IEnumerable\<T\>](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) interface that can be used to enumerate the CIM classes.</span></span>

## <a name="see-also"></a><span data-ttu-id="56a7f-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56a7f-119">See also</span></span>

<span data-ttu-id="56a7f-120">[Класс CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="56a7f-120">[CimInstance class](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))</span></span>  
<span data-ttu-id="56a7f-121">[Пространство имен Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="56a7f-121">[Microsoft.Management.Infrastructure.Serialization namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
