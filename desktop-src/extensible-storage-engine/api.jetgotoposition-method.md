---
description: Дополнительные сведения о методе API. Жетготопоситион
title: API. Жетготопоситион, метод
TOCTitle: 'JetGotoPosition method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGotoPosition(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_RECPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgotoposition(v=EXCHG.10)
ms:contentKeyID: 55100756
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGotoPosition
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGotoPosition
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5917e729d1a9ae5ae0a3715d6a2a2a81f45f75e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701743"
---
# <a name="apijetgotoposition-method"></a><span data-ttu-id="5def4-103">API. Жетготопоситион, метод</span><span class="sxs-lookup"><span data-stu-id="5def4-103">Api.JetGotoPosition method</span></span>

<span data-ttu-id="5def4-104">Перемещает курсор на новое место, которое представляет собой часть пути с помощью текущего индекса.</span><span class="sxs-lookup"><span data-stu-id="5def4-104">Moves a cursor to a new location that is a fraction of the way through the current index.</span></span> <span data-ttu-id="5def4-105">См. также раздел [жетжетрекордпоситион (JET_SESID, JET_TABLEID, JET_RECPOS)](./api.jetgetrecordposition-method.md).</span><span class="sxs-lookup"><span data-stu-id="5def4-105">Also see [JetGetRecordPosition(JET_SESID, JET_TABLEID, JET_RECPOS)](./api.jetgetrecordposition-method.md).</span></span>

<span data-ttu-id="5def4-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5def4-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5def4-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5def4-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5def4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5def4-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGotoPosition ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    recpos As JET_RECPOS _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim recpos As JET_RECPOSApi.JetGotoPosition(sesid, tableid, _
    recpos)
```

``` csharp
public static void JetGotoPosition(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_RECPOS recpos
)
```

#### <a name="parameters"></a><span data-ttu-id="5def4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5def4-109">Parameters</span></span>

  - <span data-ttu-id="5def4-110">сесид</span><span class="sxs-lookup"><span data-stu-id="5def4-110">sesid</span></span>  
    <span data-ttu-id="5def4-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5def4-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="5def4-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="5def4-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="5def4-113">TableID</span><span class="sxs-lookup"><span data-stu-id="5def4-113">tableid</span></span>  
    <span data-ttu-id="5def4-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5def4-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="5def4-115">Курсор для позиции.</span><span class="sxs-lookup"><span data-stu-id="5def4-115">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="5def4-116">рекпос</span><span class="sxs-lookup"><span data-stu-id="5def4-116">recpos</span></span>  
    <span data-ttu-id="5def4-117">Тип: [Microsoft.ISAM.ESENT.Interop.JET_RECPOS](./jet-recpos-class.md)</span><span class="sxs-lookup"><span data-stu-id="5def4-117">Type: [Microsoft.Isam.Esent.Interop.JET_RECPOS](./jet-recpos-class.md)</span></span>  
    
    <span data-ttu-id="5def4-118">Приближенное положение для перемещения.</span><span class="sxs-lookup"><span data-stu-id="5def4-118">The approximate position to move to.</span></span>

## <a name="see-also"></a><span data-ttu-id="5def4-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5def4-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5def4-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="5def4-120">Reference</span></span>

[<span data-ttu-id="5def4-121">Класс API</span><span class="sxs-lookup"><span data-stu-id="5def4-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="5def4-122">Члены API</span><span class="sxs-lookup"><span data-stu-id="5def4-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="5def4-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="5def4-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
