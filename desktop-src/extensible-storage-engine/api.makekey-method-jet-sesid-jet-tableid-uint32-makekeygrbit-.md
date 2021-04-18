---
description: 'Дополнительные сведения: метод API. Макекэй (JET_SESID, JET_TABLEID, UInt32, Макекэйгрбит)'
title: Метод API. Макекэй (JET_SESID, JET_TABLEID, UInt32, Макекэйгрбит)
TOCTitle: MakeKey method (JET_SESID, JET_TABLEID, UInt32, MakeKeyGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.MakeKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.UInt32,Microsoft.Isam.Esent.Interop.MakeKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.makekey(v=EXCHG.10)
ms:contentKeyID: 55100848
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.MakeKey
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 45edbf959058ccb1c50b82a13f0ca84cdd16a7dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693495"
---
# <a name="apimakekey-method-jet_sesid-jet_tableid-uint32-makekeygrbit"></a><span data-ttu-id="e4d98-103">Метод API. Макекэй (JET_SESID, JET_TABLEID, UInt32, Макекэйгрбит)</span><span class="sxs-lookup"><span data-stu-id="e4d98-103">Api.MakeKey method (JET_SESID, JET_TABLEID, UInt32, MakeKeyGrbit)</span></span>

<span data-ttu-id="e4d98-104">Конструирует ключ поиска, который затем может использоваться [жетсик (JET_SESID, JET_TABLEID, сикгрбит)](./api.jetseek-method.md) и [жетсетиндексранже (JET_SESID, JET_TABLEID, сетиндексранжегрбит)](./api.jetsetindexrange-method.md).</span><span class="sxs-lookup"><span data-stu-id="e4d98-104">Constructs a search key that may then be used by [JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) and [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span></span>

<span data-ttu-id="e4d98-105">Этот API несовместим с CLS.</span><span class="sxs-lookup"><span data-stu-id="e4d98-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="e4d98-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e4d98-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e4d98-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e4d98-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e4d98-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e4d98-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Sub MakeKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As UInteger, _
    grbit As MakeKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As UInteger
Dim grbit As MakeKeyGrbitApi.MakeKey(sesid, tableid, data, _
    grbit)
```

``` csharp
[CLSCompliantAttribute(false)]
public static void MakeKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    uint data,
    MakeKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="e4d98-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4d98-109">Parameters</span></span>

  - <span data-ttu-id="e4d98-110">сесид</span><span class="sxs-lookup"><span data-stu-id="e4d98-110">sesid</span></span>  
    <span data-ttu-id="e4d98-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e4d98-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e4d98-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="e4d98-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e4d98-113">TableID</span><span class="sxs-lookup"><span data-stu-id="e4d98-113">tableid</span></span>  
    <span data-ttu-id="e4d98-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e4d98-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e4d98-115">Курсор, на котором создается ключ.</span><span class="sxs-lookup"><span data-stu-id="e4d98-115">The cursor to create the key on.</span></span>

<!-- end list -->

  - <span data-ttu-id="e4d98-116">.</span><span class="sxs-lookup"><span data-stu-id="e4d98-116">data</span></span>  
    <span data-ttu-id="e4d98-117">Тип: [System. UInt32](/dotnet/api/system.uint32)</span><span class="sxs-lookup"><span data-stu-id="e4d98-117">Type: [System.UInt32](/dotnet/api/system.uint32)</span></span>  
    
    <span data-ttu-id="e4d98-118">Данные столбца для текущего ключевого столбца текущего индекса.</span><span class="sxs-lookup"><span data-stu-id="e4d98-118">Column data for the current key column of the current index.</span></span>

<!-- end list -->

  - <span data-ttu-id="e4d98-119">грбит</span><span class="sxs-lookup"><span data-stu-id="e4d98-119">grbit</span></span>  
    <span data-ttu-id="e4d98-120">Тип: [Microsoft. ISAM. ESENT. Interop. макекэйгрбит](./makekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e4d98-120">Type: [Microsoft.Isam.Esent.Interop.MakeKeyGrbit](./makekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="e4d98-121">Ключевые параметры.</span><span class="sxs-lookup"><span data-stu-id="e4d98-121">Key options.</span></span>

## <a name="see-also"></a><span data-ttu-id="e4d98-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e4d98-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e4d98-123">Справочник</span><span class="sxs-lookup"><span data-stu-id="e4d98-123">Reference</span></span>

[<span data-ttu-id="e4d98-124">Класс API</span><span class="sxs-lookup"><span data-stu-id="e4d98-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e4d98-125">Члены API</span><span class="sxs-lookup"><span data-stu-id="e4d98-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e4d98-126">Перегрузка Макекэй</span><span class="sxs-lookup"><span data-stu-id="e4d98-126">MakeKey overload</span></span>](./api.makekey-method.md)

[<span data-ttu-id="e4d98-127">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e4d98-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
