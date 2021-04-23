---
description: Дополнительные сведения о методе API. Ресетиндексранже
title: API. Ресетиндексранже, метод
TOCTitle: 'ResetIndexRange method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.ResetIndexRange(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.resetindexrange(v=EXCHG.10)
ms:contentKeyID: 55100832
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.ResetIndexRange
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.ResetIndexRange
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 434740a549fa83d4601bf88ab09f307f4d19f189
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272917"
---
# <a name="apiresetindexrange-method"></a><span data-ttu-id="2bebf-103">API. Ресетиндексранже, метод</span><span class="sxs-lookup"><span data-stu-id="2bebf-103">Api.ResetIndexRange method</span></span>

<span data-ttu-id="2bebf-104">Удаляет диапазон индексов, созданный с помощью [жетсетиндексранже (JET_SESID, JET_TABLEID, сетиндексранжегрбит)](./api.jetsetindexrange-method.md) или [трисетиндексранже (JET_SESID, JET_TABLEID, сетиндексранжегрбит)](./api.trysetindexrange-method.md).</span><span class="sxs-lookup"><span data-stu-id="2bebf-104">Removes an index range created with [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md) or [TrySetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.trysetindexrange-method.md).</span></span> <span data-ttu-id="2bebf-105">Если диапазон индекса отсутствует, этот метод не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="2bebf-105">If no index range is present this method does nothing.</span></span>

<span data-ttu-id="2bebf-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2bebf-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2bebf-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2bebf-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2bebf-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2bebf-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub ResetIndexRange ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.ResetIndexRange(sesid, tableid)
```

``` csharp
public static void ResetIndexRange(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="2bebf-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2bebf-109">Parameters</span></span>

  - <span data-ttu-id="2bebf-110">сесид</span><span class="sxs-lookup"><span data-stu-id="2bebf-110">sesid</span></span>  
    <span data-ttu-id="2bebf-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2bebf-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="2bebf-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="2bebf-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="2bebf-113">TableID</span><span class="sxs-lookup"><span data-stu-id="2bebf-113">tableid</span></span>  
    <span data-ttu-id="2bebf-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2bebf-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="2bebf-115">Курсор, для которого необходимо удалить диапазон индексов.</span><span class="sxs-lookup"><span data-stu-id="2bebf-115">The cursor to remove the index range on.</span></span>

## <a name="see-also"></a><span data-ttu-id="2bebf-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2bebf-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2bebf-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="2bebf-117">Reference</span></span>

[<span data-ttu-id="2bebf-118">Класс API</span><span class="sxs-lookup"><span data-stu-id="2bebf-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="2bebf-119">Члены API</span><span class="sxs-lookup"><span data-stu-id="2bebf-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="2bebf-120">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="2bebf-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
