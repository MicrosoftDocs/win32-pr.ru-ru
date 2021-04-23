---
description: Дополнительные сведения о методе API. Трисетиндексранже
title: API. Трисетиндексранже, метод
TOCTitle: 'TrySetIndexRange method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TrySetIndexRange(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trysetindexrange(v=EXCHG.10)
ms:contentKeyID: 55100893
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TrySetIndexRange
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TrySetIndexRange
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d175fdfc931d24742d61f962a45e690a5c49c2be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818449"
---
# <a name="apitrysetindexrange-method"></a><span data-ttu-id="1d7ca-103">API. Трисетиндексранже, метод</span><span class="sxs-lookup"><span data-stu-id="1d7ca-103">Api.TrySetIndexRange method</span></span>

<span data-ttu-id="1d7ca-104">Временно ограничивает набор записей индекса, которые курсор может проанализировать с помощью Жетмове, начиная с текущего элемента индекса и заканчивая элементом индекса, который соответствует критериям поиска, заданным в этом курсоре, и указанным критериям.</span><span class="sxs-lookup"><span data-stu-id="1d7ca-104">Temporarily limits the set of index entries that the cursor can walk using JetMove to those starting from the current index entry and ending at the index entry that matches the search criteria specified by the search key in that cursor and the specified bound criteria.</span></span> <span data-ttu-id="1d7ca-105">Ключ поиска должен быть ранее создан с помощью Жетмакекэй.</span><span class="sxs-lookup"><span data-stu-id="1d7ca-105">A search key must have been previously constructed using JetMakeKey.</span></span> <span data-ttu-id="1d7ca-106">Возвращает значение true, если диапазон индекса не является пустым, и false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="1d7ca-106">Returns true if the index range is non-empty, false otherwise.</span></span>

<span data-ttu-id="1d7ca-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1d7ca-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1d7ca-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1d7ca-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1d7ca-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d7ca-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TrySetIndexRange ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SetIndexRangeGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SetIndexRangeGrbit
Dim returnValue As Boolean

returnValue = Api.TrySetIndexRange(sesid, _
    tableid, grbit)
```

``` csharp
public static bool TrySetIndexRange(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SetIndexRangeGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="1d7ca-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="1d7ca-110">Parameters</span></span>

  - <span data-ttu-id="1d7ca-111">сесид</span><span class="sxs-lookup"><span data-stu-id="1d7ca-111">sesid</span></span>  
    <span data-ttu-id="1d7ca-112">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1d7ca-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1d7ca-113">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="1d7ca-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1d7ca-114">TableID</span><span class="sxs-lookup"><span data-stu-id="1d7ca-114">tableid</span></span>  
    <span data-ttu-id="1d7ca-115">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1d7ca-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="1d7ca-116">Курсор для позиции.</span><span class="sxs-lookup"><span data-stu-id="1d7ca-116">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="1d7ca-117">грбит</span><span class="sxs-lookup"><span data-stu-id="1d7ca-117">grbit</span></span>  
    <span data-ttu-id="1d7ca-118">Тип: [Microsoft. ISAM. ESENT. Interop. сетиндексранжегрбит](./setindexrangegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="1d7ca-118">Type: [Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit](./setindexrangegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="1d7ca-119">Параметр поиска.</span><span class="sxs-lookup"><span data-stu-id="1d7ca-119">Seek option.</span></span>

#### <a name="return-value"></a><span data-ttu-id="1d7ca-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1d7ca-120">Return value</span></span>

<span data-ttu-id="1d7ca-121">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="1d7ca-121">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="1d7ca-122">Значение true, если поиск выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="1d7ca-122">True if the seek was successful.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1d7ca-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d7ca-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1d7ca-124">Справочник</span><span class="sxs-lookup"><span data-stu-id="1d7ca-124">Reference</span></span>

[<span data-ttu-id="1d7ca-125">Класс API</span><span class="sxs-lookup"><span data-stu-id="1d7ca-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1d7ca-126">Члены API</span><span class="sxs-lookup"><span data-stu-id="1d7ca-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1d7ca-127">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="1d7ca-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
