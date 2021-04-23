---
description: 'Дополнительные сведения: метод API. Жетмове (JET_SESID, JET_TABLEID, Int32, Мовегрбит)'
title: Метод API. Жетмове (JET_SESID, JET_TABLEID, Int32, Мовегрбит)
TOCTitle: JetMove method (JET_SESID, JET_TABLEID, Int32, MoveGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetMove(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int32,Microsoft.Isam.Esent.Interop.MoveGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetmove(v=EXCHG.10)
ms:contentKeyID: 55100765
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetMove
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f6d77914a3dc4728626db8e4ffe271851099e5e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712927"
---
# <a name="apijetmove-method-jet_sesid-jet_tableid-int32-movegrbit"></a><span data-ttu-id="e6319-103">Метод API. Жетмове (JET_SESID, JET_TABLEID, Int32, Мовегрбит)</span><span class="sxs-lookup"><span data-stu-id="e6319-103">Api.JetMove method (JET_SESID, JET_TABLEID, Int32, MoveGrbit)</span></span>

<span data-ttu-id="e6319-104">Навигация по индексу.</span><span class="sxs-lookup"><span data-stu-id="e6319-104">Navigate through an index.</span></span> <span data-ttu-id="e6319-105">Курсор может располагаться в начале или в конце индекса и перемещаться назад и вперед по заданному числу записей индекса.</span><span class="sxs-lookup"><span data-stu-id="e6319-105">The cursor can be positioned at the start or end of the index and moved backwards and forwards by a specified number of index entries.</span></span> <span data-ttu-id="e6319-106">См. также [тримовефирст (JET_SESID, JET_TABLEID)](./api.trymovefirst-method.md), [тримовеласт (JET_SESID, JET_TABLEID)](./api.trymovelast-method.md), [тримовенекст (JET_SESID, JET_TABLEID)](./api.trymovenext-method.md), [тримовепревиаус (JET_SESID, JET_TABLEID)](./api.trymoveprevious-method.md).</span><span class="sxs-lookup"><span data-stu-id="e6319-106">Also see [TryMoveFirst(JET_SESID, JET_TABLEID)](./api.trymovefirst-method.md), [TryMoveLast(JET_SESID, JET_TABLEID)](./api.trymovelast-method.md), [TryMoveNext(JET_SESID, JET_TABLEID)](./api.trymovenext-method.md), [TryMovePrevious(JET_SESID, JET_TABLEID)](./api.trymoveprevious-method.md).</span></span>

<span data-ttu-id="e6319-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e6319-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e6319-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e6319-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e6319-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6319-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetMove ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    numRows As Integer, _
    grbit As MoveGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim numRows As Integer
Dim grbit As MoveGrbitApi.JetMove(sesid, tableid, numRows, _
    grbit)
```

``` csharp
public static void JetMove(
    JET_SESID sesid,
    JET_TABLEID tableid,
    int numRows,
    MoveGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="e6319-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6319-110">Parameters</span></span>

  - <span data-ttu-id="e6319-111">сесид</span><span class="sxs-lookup"><span data-stu-id="e6319-111">sesid</span></span>  
    <span data-ttu-id="e6319-112">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e6319-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e6319-113">Сеанс, используемый для вызова.</span><span class="sxs-lookup"><span data-stu-id="e6319-113">The session to use for the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="e6319-114">TableID</span><span class="sxs-lookup"><span data-stu-id="e6319-114">tableid</span></span>  
    <span data-ttu-id="e6319-115">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e6319-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e6319-116">Курсор для позиции.</span><span class="sxs-lookup"><span data-stu-id="e6319-116">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="e6319-117">нумровс</span><span class="sxs-lookup"><span data-stu-id="e6319-117">numRows</span></span>  
    <span data-ttu-id="e6319-118">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e6319-118">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e6319-119">Смещение, которое указывает, насколько далеко переместить курсор.</span><span class="sxs-lookup"><span data-stu-id="e6319-119">An offset which indicates how far to move the cursor.</span></span>

<!-- end list -->

  - <span data-ttu-id="e6319-120">грбит</span><span class="sxs-lookup"><span data-stu-id="e6319-120">grbit</span></span>  
    <span data-ttu-id="e6319-121">Тип: [Microsoft. ISAM. ESENT. Interop. мовегрбит](./movegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e6319-121">Type: [Microsoft.Isam.Esent.Interop.MoveGrbit](./movegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="e6319-122">Параметры перемещения.</span><span class="sxs-lookup"><span data-stu-id="e6319-122">Move options.</span></span>

## <a name="see-also"></a><span data-ttu-id="e6319-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6319-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e6319-124">Справочник</span><span class="sxs-lookup"><span data-stu-id="e6319-124">Reference</span></span>

[<span data-ttu-id="e6319-125">Класс API</span><span class="sxs-lookup"><span data-stu-id="e6319-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e6319-126">Члены API</span><span class="sxs-lookup"><span data-stu-id="e6319-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e6319-127">Перегрузка Жетмове</span><span class="sxs-lookup"><span data-stu-id="e6319-127">JetMove overload</span></span>](./api.jetmove-method.md)

[<span data-ttu-id="e6319-128">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e6319-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
