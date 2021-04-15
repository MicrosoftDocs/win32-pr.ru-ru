---
description: Дополнительные сведения о методе API. Интерсектиндексес
title: API. Интерсектиндексес, метод
TOCTitle: 'IntersectIndexes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.IntersectIndexes(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.intersectindexes(v=EXCHG.10)
ms:contentKeyID: 55107220
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.IntersectIndexes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.IntersectIndexes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8dfe5784ecd5ab517e183f8eeeb5f79315fe585a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539734"
---
# <a name="apiintersectindexes-method"></a><span data-ttu-id="195b0-103">API. Интерсектиндексес, метод</span><span class="sxs-lookup"><span data-stu-id="195b0-103">Api.IntersectIndexes method</span></span>

<span data-ttu-id="195b0-104">Пересекает группу диапазонов индексов и возвращает закладки записей, которые находятся во всех диапазонах индекса.</span><span class="sxs-lookup"><span data-stu-id="195b0-104">Intersect a group of index ranges and return the bookmarks of the records which are found in all the index ranges.</span></span> <span data-ttu-id="195b0-105">См. также [жетинтерсектиндексес (JET_SESID, \[ \] , Int32, JET_RECORDLIST, интерсектиндексесгрбит)](./api.jetintersectindexes-method.md).</span><span class="sxs-lookup"><span data-stu-id="195b0-105">Also see [JetIntersectIndexes(JET_SESID, \[\], Int32, JET_RECORDLIST, IntersectIndexesGrbit)](./api.jetintersectindexes-method.md).</span></span>

<span data-ttu-id="195b0-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="195b0-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="195b0-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="195b0-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="195b0-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="195b0-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function IntersectIndexes ( _
    sesid As JET_SESID, _
    ParamArray tableids As JET_TABLEID() _
) As IEnumerable(Of Byte())
'Usage
Dim sesid As JET_SESID
Dim tableids As JET_TABLEID()
Dim returnValue As IEnumerable(Of Byte())

returnValue = Api.IntersectIndexes(sesid, _
    tableids)
```

``` csharp
public static IEnumerable<byte[]> IntersectIndexes(
    JET_SESID sesid,
    params JET_TABLEID[] tableids
)
```

#### <a name="parameters"></a><span data-ttu-id="195b0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="195b0-109">Parameters</span></span>

  - <span data-ttu-id="195b0-110">сесид</span><span class="sxs-lookup"><span data-stu-id="195b0-110">sesid</span></span>  
    <span data-ttu-id="195b0-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="195b0-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="195b0-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="195b0-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="195b0-113">таблеидс</span><span class="sxs-lookup"><span data-stu-id="195b0-113">tableids</span></span>  
    <span data-ttu-id="195b0-114">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="195b0-114">Type: \[\]</span></span>  
    
    <span data-ttu-id="195b0-115">Таблеидс для использования.</span><span class="sxs-lookup"><span data-stu-id="195b0-115">The tableids to use.</span></span> <span data-ttu-id="195b0-116">Каждый TableID должен быть из другого индекса в той же таблице и иметь активный диапазон индекса.</span><span class="sxs-lookup"><span data-stu-id="195b0-116">Each tableid must be from a different index on the same table and have an active index range.</span></span> <span data-ttu-id="195b0-117">Для создания диапазона индексов используйте [жетсетиндексранже (JET_SESID, JET_TABLEID, сетиндексранжегрбит)](./api.jetsetindexrange-method.md) .</span><span class="sxs-lookup"><span data-stu-id="195b0-117">Use [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md) to create an index range.</span></span>

#### <a name="return-value"></a><span data-ttu-id="195b0-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="195b0-118">Return value</span></span>

<span data-ttu-id="195b0-119">Тип: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<\[\]\></span><span class="sxs-lookup"><span data-stu-id="195b0-119">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<\[\]\></span></span>  
<span data-ttu-id="195b0-120">Закладки записей, которые находятся во всех диапазонах индексов.</span><span class="sxs-lookup"><span data-stu-id="195b0-120">The bookmarks of the records which are found in all the index ranges.</span></span> <span data-ttu-id="195b0-121">Закладки возвращаются в порядке первичного ключа.</span><span class="sxs-lookup"><span data-stu-id="195b0-121">The bookmarks are returned in primary key order.</span></span>  

## <a name="see-also"></a><span data-ttu-id="195b0-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="195b0-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="195b0-123">Справочник</span><span class="sxs-lookup"><span data-stu-id="195b0-123">Reference</span></span>

[<span data-ttu-id="195b0-124">Класс API</span><span class="sxs-lookup"><span data-stu-id="195b0-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="195b0-125">Члены API</span><span class="sxs-lookup"><span data-stu-id="195b0-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="195b0-126">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="195b0-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
