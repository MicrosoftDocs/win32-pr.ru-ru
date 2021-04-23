---
description: Дополнительные сведения о методе API. Жетинтерсектиндексес
title: API. Жетинтерсектиндексес, метод
TOCTitle: 'JetIntersectIndexes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_INDEXRANGE[],System.Int32,Microsoft.Isam.Esent.Interop.JET_RECORDLIST@,Microsoft.Isam.Esent.Interop.IntersectIndexesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetintersectindexes(v=EXCHG.10)
ms:contentKeyID: 55100761
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3bae632f386ef944e79a17813d1cc86451441e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999652"
---
# <a name="apijetintersectindexes-method"></a><span data-ttu-id="13d2c-103">API. Жетинтерсектиндексес, метод</span><span class="sxs-lookup"><span data-stu-id="13d2c-103">Api.JetIntersectIndexes method</span></span>

<span data-ttu-id="13d2c-104">Выполняет пересечение нескольких наборов записей индекса из разных вторичных индексов по той же таблице.</span><span class="sxs-lookup"><span data-stu-id="13d2c-104">Computes the intersection between multiple sets of index entries from different secondary indices over the same table.</span></span> <span data-ttu-id="13d2c-105">Эта операция полезна для поиска набора записей в таблице, соответствующих двум или более критериям, которые могут быть выражены с помощью диапазонов индексов.</span><span class="sxs-lookup"><span data-stu-id="13d2c-105">This operation is useful for finding the set of records in a table that match two or more criteria that can be expressed using index ranges.</span></span> <span data-ttu-id="13d2c-106">См. также [интерсектиндексес (JET_SESID, \[ \] )](./api.intersectindexes-method.md).</span><span class="sxs-lookup"><span data-stu-id="13d2c-106">Also see [IntersectIndexes(JET_SESID, \[\])](./api.intersectindexes-method.md).</span></span>

<span data-ttu-id="13d2c-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="13d2c-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="13d2c-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="13d2c-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="13d2c-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13d2c-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetIntersectIndexes ( _
    sesid As JET_SESID, _
    ranges As JET_INDEXRANGE(), _
    numRanges As Integer, _
    <OutAttribute> ByRef recordlist As JET_RECORDLIST, _
    grbit As IntersectIndexesGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim ranges As JET_INDEXRANGE()
Dim numRanges As Integer
Dim recordlist As JET_RECORDLIST
Dim grbit As IntersectIndexesGrbitApi.JetIntersectIndexes(sesid, _
    ranges, numRanges, recordlist, grbit)
```

``` csharp
public static void JetIntersectIndexes(
    JET_SESID sesid,
    JET_INDEXRANGE[] ranges,
    int numRanges,
    out JET_RECORDLIST recordlist,
    IntersectIndexesGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="13d2c-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="13d2c-110">Parameters</span></span>

  - <span data-ttu-id="13d2c-111">сесид</span><span class="sxs-lookup"><span data-stu-id="13d2c-111">sesid</span></span>  
    <span data-ttu-id="13d2c-112">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="13d2c-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="13d2c-113">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="13d2c-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="13d2c-114">ranges</span><span class="sxs-lookup"><span data-stu-id="13d2c-114">ranges</span></span>  
    <span data-ttu-id="13d2c-115">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="13d2c-115">Type: \[\]</span></span>  
    
    <span data-ttu-id="13d2c-116">Диапазон индекса для пересечения.</span><span class="sxs-lookup"><span data-stu-id="13d2c-116">An the index ranges to intersect.</span></span> <span data-ttu-id="13d2c-117">Для таблеидс в диапазонах должны быть заданы диапазоны индексов.</span><span class="sxs-lookup"><span data-stu-id="13d2c-117">The tableids in the ranges must have index ranges set on them.</span></span> <span data-ttu-id="13d2c-118">Для создания диапазона индексов используйте [жетсетиндексранже (JET_SESID, JET_TABLEID, сетиндексранжегрбит)](./api.jetsetindexrange-method.md) .</span><span class="sxs-lookup"><span data-stu-id="13d2c-118">Use [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md) to create an index range.</span></span>

<!-- end list -->

  - <span data-ttu-id="13d2c-119">нумранжес</span><span class="sxs-lookup"><span data-stu-id="13d2c-119">numRanges</span></span>  
    <span data-ttu-id="13d2c-120">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="13d2c-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="13d2c-121">Количество диапазонов индекса.</span><span class="sxs-lookup"><span data-stu-id="13d2c-121">The number of index ranges.</span></span>

<!-- end list -->

  - <span data-ttu-id="13d2c-122">рекордлист</span><span class="sxs-lookup"><span data-stu-id="13d2c-122">recordlist</span></span>  
    <span data-ttu-id="13d2c-123">Тип: [Microsoft.ISAM.ESENT.Interop.JET_RECORDLIST](./jet-recordlist-class.md)</span><span class="sxs-lookup"><span data-stu-id="13d2c-123">Type: [Microsoft.Isam.Esent.Interop.JET_RECORDLIST](./jet-recordlist-class.md)</span></span>  
    
    <span data-ttu-id="13d2c-124">Возвращает сведения о временной таблице, содержащей результаты пересечения.</span><span class="sxs-lookup"><span data-stu-id="13d2c-124">Returns information about the temporary table containing the intersection results.</span></span>

<!-- end list -->

  - <span data-ttu-id="13d2c-125">грбит</span><span class="sxs-lookup"><span data-stu-id="13d2c-125">grbit</span></span>  
    <span data-ttu-id="13d2c-126">Тип: [Microsoft. ISAM. ESENT. Interop. интерсектиндексесгрбит](./intersectindexesgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="13d2c-126">Type: [Microsoft.Isam.Esent.Interop.IntersectIndexesGrbit](./intersectindexesgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="13d2c-127">Параметры пересечения.</span><span class="sxs-lookup"><span data-stu-id="13d2c-127">Intersection options.</span></span>

## <a name="see-also"></a><span data-ttu-id="13d2c-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="13d2c-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="13d2c-129">Справочник</span><span class="sxs-lookup"><span data-stu-id="13d2c-129">Reference</span></span>

[<span data-ttu-id="13d2c-130">Класс API</span><span class="sxs-lookup"><span data-stu-id="13d2c-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="13d2c-131">Члены API</span><span class="sxs-lookup"><span data-stu-id="13d2c-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="13d2c-132">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="13d2c-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
