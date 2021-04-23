---
description: Дополнительные сведения о методе API. Жетсетиндексранже
title: API. Жетсетиндексранже, метод
TOCTitle: 'JetSetIndexRange method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetIndexRange(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetindexrange(v=EXCHG.10)
ms:contentKeyID: 55100817
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetIndexRange
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetIndexRange
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3ad13e04674de60aa1c0f55cf4cd4570f8b7ddaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072668"
---
# <a name="apijetsetindexrange-method"></a><span data-ttu-id="41345-103">API. Жетсетиндексранже, метод</span><span class="sxs-lookup"><span data-stu-id="41345-103">Api.JetSetIndexRange method</span></span>

<span data-ttu-id="41345-104">Временно ограничивает набор записей индекса, которые курсор может проанализировать с помощью [жетмове (JET_SESID, JET_TABLEID, Int32, мовегрбит)](./api.jetmove-method-jet-sesid-jet-tableid-int32-movegrbit-.md) , начиная с текущего элемента индекса и заканчивая записью индекса, которая соответствует критериям поиска, заданным в ключе поиска в этом курсоре, и указанным критериям привязки.</span><span class="sxs-lookup"><span data-stu-id="41345-104">Temporarily limits the set of index entries that the cursor can walk using [JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit)](./api.jetmove-method-jet-sesid-jet-tableid-int32-movegrbit-.md) to those starting from the current index entry and ending at the index entry that matches the search criteria specified by the search key in that cursor and the specified bound criteria.</span></span> <span data-ttu-id="41345-105">Ключ поиска должен быть ранее создан с помощью [жетмакекэй (JET_SESID, JET_TABLEID, \[ \] , Int32, макекэйгрбит)](./api.jetmakekey-method.md).</span><span class="sxs-lookup"><span data-stu-id="41345-105">A search key must have been previously constructed using [JetMakeKey(JET_SESID, JET_TABLEID, \[\], Int32, MakeKeyGrbit)](./api.jetmakekey-method.md).</span></span> <span data-ttu-id="41345-106">См. также [трисетиндексранже (JET_SESID, JET_TABLEID, сетиндексранжегрбит)](./api.trysetindexrange-method.md).</span><span class="sxs-lookup"><span data-stu-id="41345-106">Also see [TrySetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.trysetindexrange-method.md).</span></span>

<span data-ttu-id="41345-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="41345-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="41345-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="41345-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="41345-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="41345-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetIndexRange ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SetIndexRangeGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SetIndexRangeGrbitApi.JetSetIndexRange(sesid, tableid, _
    grbit)
```

``` csharp
public static void JetSetIndexRange(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SetIndexRangeGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="41345-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="41345-110">Parameters</span></span>

  - <span data-ttu-id="41345-111">сесид</span><span class="sxs-lookup"><span data-stu-id="41345-111">sesid</span></span>  
    <span data-ttu-id="41345-112">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="41345-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="41345-113">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="41345-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="41345-114">TableID</span><span class="sxs-lookup"><span data-stu-id="41345-114">tableid</span></span>  
    <span data-ttu-id="41345-115">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="41345-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="41345-116">Курсор, для которого задается диапазон индекса.</span><span class="sxs-lookup"><span data-stu-id="41345-116">The cursor to set the index range on.</span></span>

<!-- end list -->

  - <span data-ttu-id="41345-117">грбит</span><span class="sxs-lookup"><span data-stu-id="41345-117">grbit</span></span>  
    <span data-ttu-id="41345-118">Тип: [Microsoft. ISAM. ESENT. Interop. сетиндексранжегрбит](./setindexrangegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="41345-118">Type: [Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit](./setindexrangegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="41345-119">Параметры диапазона индекса.</span><span class="sxs-lookup"><span data-stu-id="41345-119">Index range options.</span></span>

## <a name="see-also"></a><span data-ttu-id="41345-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="41345-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="41345-121">Справочник</span><span class="sxs-lookup"><span data-stu-id="41345-121">Reference</span></span>

[<span data-ttu-id="41345-122">Класс API</span><span class="sxs-lookup"><span data-stu-id="41345-122">Api class</span></span>](./api-class.md)

[<span data-ttu-id="41345-123">Члены API</span><span class="sxs-lookup"><span data-stu-id="41345-123">Api members</span></span>](./api-members.md)

[<span data-ttu-id="41345-124">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="41345-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
