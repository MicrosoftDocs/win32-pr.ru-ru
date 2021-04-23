---
description: Дополнительные сведения о методе API. Тримове
title: API. Тримове, метод
TOCTitle: 'TryMove method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryMove(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_Move,Microsoft.Isam.Esent.Interop.MoveGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trymove(v=EXCHG.10)
ms:contentKeyID: 55100883
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryMove
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryMove
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6d4b3aa596bb5e813d87dcc6f278112fe1e4cbdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692107"
---
# <a name="apitrymove-method"></a><span data-ttu-id="c3e0f-103">API. Тримове, метод</span><span class="sxs-lookup"><span data-stu-id="c3e0f-103">Api.TryMove method</span></span>

<span data-ttu-id="c3e0f-104">Попробуйте выполнить навигацию по индексу.</span><span class="sxs-lookup"><span data-stu-id="c3e0f-104">Try to navigate through an index.</span></span> <span data-ttu-id="c3e0f-105">Если переход выполнен, этот метод возвращает значение true.</span><span class="sxs-lookup"><span data-stu-id="c3e0f-105">If the navigation succeeds this method returns true.</span></span> <span data-ttu-id="c3e0f-106">Если нет записи для перехода к этому методу, возвращает значение false; исключение будет создано для других ошибок.</span><span class="sxs-lookup"><span data-stu-id="c3e0f-106">If there is no record to navigate to this method returns false; an exception will be thrown for other errors.</span></span>

<span data-ttu-id="c3e0f-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c3e0f-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c3e0f-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c3e0f-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c3e0f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c3e0f-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TryMove ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    move As JET_Move, _
    grbit As MoveGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim move As JET_Move
Dim grbit As MoveGrbit
Dim returnValue As Boolean

returnValue = Api.TryMove(sesid, _
    tableid, move, grbit)
```

``` csharp
public static bool TryMove(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_Move move,
    MoveGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="c3e0f-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c3e0f-110">Parameters</span></span>

  - <span data-ttu-id="c3e0f-111">сесид</span><span class="sxs-lookup"><span data-stu-id="c3e0f-111">sesid</span></span>  
    <span data-ttu-id="c3e0f-112">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c3e0f-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c3e0f-113">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="c3e0f-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c3e0f-114">TableID</span><span class="sxs-lookup"><span data-stu-id="c3e0f-114">tableid</span></span>  
    <span data-ttu-id="c3e0f-115">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c3e0f-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="c3e0f-116">Курсор для позиции.</span><span class="sxs-lookup"><span data-stu-id="c3e0f-116">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="c3e0f-117">перенос</span><span class="sxs-lookup"><span data-stu-id="c3e0f-117">move</span></span>  
    <span data-ttu-id="c3e0f-118">Тип: [Microsoft.ISAM.ESENT.Interop.JET_Move](./jet-move-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="c3e0f-118">Type: [Microsoft.Isam.Esent.Interop.JET_Move](./jet-move-enumeration.md)</span></span>  
    
    <span data-ttu-id="c3e0f-119">Направление перемещения.</span><span class="sxs-lookup"><span data-stu-id="c3e0f-119">The direction to move in.</span></span>

<!-- end list -->

  - <span data-ttu-id="c3e0f-120">грбит</span><span class="sxs-lookup"><span data-stu-id="c3e0f-120">grbit</span></span>  
    <span data-ttu-id="c3e0f-121">Тип: [Microsoft. ISAM. ESENT. Interop. мовегрбит](./movegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="c3e0f-121">Type: [Microsoft.Isam.Esent.Interop.MoveGrbit](./movegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="c3e0f-122">Параметры перемещения.</span><span class="sxs-lookup"><span data-stu-id="c3e0f-122">Move options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="c3e0f-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c3e0f-123">Return value</span></span>

<span data-ttu-id="c3e0f-124">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="c3e0f-124">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="c3e0f-125">Значение true, если перемещение прошло успешно.</span><span class="sxs-lookup"><span data-stu-id="c3e0f-125">True if the move was successful.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c3e0f-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c3e0f-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c3e0f-127">Справочник</span><span class="sxs-lookup"><span data-stu-id="c3e0f-127">Reference</span></span>

[<span data-ttu-id="c3e0f-128">Класс API</span><span class="sxs-lookup"><span data-stu-id="c3e0f-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c3e0f-129">Члены API</span><span class="sxs-lookup"><span data-stu-id="c3e0f-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c3e0f-130">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="c3e0f-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
