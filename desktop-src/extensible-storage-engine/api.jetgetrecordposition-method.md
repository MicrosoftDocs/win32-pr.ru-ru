---
description: Дополнительные сведения о методе API. Жетжетрекордпоситион
title: API. Жетжетрекордпоситион, метод
TOCTitle: 'JetGetRecordPosition method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetRecordPosition(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_RECPOS@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetrecordposition(v=EXCHG.10)
ms:contentKeyID: 55100722
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetRecordPosition
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetRecordPosition
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 00350853172d784c270c197e7c58ad6fa616560f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540834"
---
# <a name="apijetgetrecordposition-method"></a><span data-ttu-id="704d3-103">API. Жетжетрекордпоситион, метод</span><span class="sxs-lookup"><span data-stu-id="704d3-103">Api.JetGetRecordPosition method</span></span>

<span data-ttu-id="704d3-104">Возвращает вертикальную точку текущей записи в текущем индексе в форме [JET_RECPOS](./jet-recpos-class.md) структуры.</span><span class="sxs-lookup"><span data-stu-id="704d3-104">Returns the fractional position of the current record in the current index in the form of a [JET_RECPOS](./jet-recpos-class.md) structure.</span></span> <span data-ttu-id="704d3-105">См. также раздел [жетготопоситион (JET_SESID, JET_TABLEID, JET_RECPOS)](./api.jetgotoposition-method.md).</span><span class="sxs-lookup"><span data-stu-id="704d3-105">Also see [JetGotoPosition(JET_SESID, JET_TABLEID, JET_RECPOS)](./api.jetgotoposition-method.md).</span></span>

<span data-ttu-id="704d3-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="704d3-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="704d3-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="704d3-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="704d3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="704d3-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetRecordPosition ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef recpos As JET_RECPOS _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim recpos As JET_RECPOSApi.JetGetRecordPosition(sesid, _
    tableid, recpos)
```

``` csharp
public static void JetGetRecordPosition(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out JET_RECPOS recpos
)
```

#### <a name="parameters"></a><span data-ttu-id="704d3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="704d3-109">Parameters</span></span>

  - <span data-ttu-id="704d3-110">сесид</span><span class="sxs-lookup"><span data-stu-id="704d3-110">sesid</span></span>  
    <span data-ttu-id="704d3-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="704d3-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="704d3-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="704d3-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="704d3-113">TableID</span><span class="sxs-lookup"><span data-stu-id="704d3-113">tableid</span></span>  
    <span data-ttu-id="704d3-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="704d3-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="704d3-115">Курсор, расположенный на записи.</span><span class="sxs-lookup"><span data-stu-id="704d3-115">The cursor positioned on the record.</span></span>

<!-- end list -->

  - <span data-ttu-id="704d3-116">рекпос</span><span class="sxs-lookup"><span data-stu-id="704d3-116">recpos</span></span>  
    <span data-ttu-id="704d3-117">Тип: [Microsoft.ISAM.ESENT.Interop.JET_RECPOS](./jet-recpos-class.md)</span><span class="sxs-lookup"><span data-stu-id="704d3-117">Type: [Microsoft.Isam.Esent.Interop.JET_RECPOS](./jet-recpos-class.md)</span></span>  
    
    <span data-ttu-id="704d3-118">Возвращает приблизительную дробную точку записи.</span><span class="sxs-lookup"><span data-stu-id="704d3-118">Returns the approximate fractional position of the record.</span></span>

## <a name="see-also"></a><span data-ttu-id="704d3-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="704d3-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="704d3-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="704d3-120">Reference</span></span>

[<span data-ttu-id="704d3-121">Класс API</span><span class="sxs-lookup"><span data-stu-id="704d3-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="704d3-122">Члены API</span><span class="sxs-lookup"><span data-stu-id="704d3-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="704d3-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="704d3-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
