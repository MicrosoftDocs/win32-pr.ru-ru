---
description: 'Дополнительные сведения о методе: Windows8Api. Жеттрипререадиндексранжес'
title: Windows8Api. Жеттрипререадиндексранжес, метод (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'JetTryPrereadIndexRanges method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetTryPrereadIndexRanges(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_RANGE[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[],Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jettryprereadindexranges(v=EXCHG.10)
ms:contentKeyID: 55104421
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetTryPrereadIndexRanges
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetTryPrereadIndexRanges
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9a9664e658254de057b0e3aa8ae86813eb996a14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692570"
---
# <a name="windows8apijettryprereadindexranges-method"></a><span data-ttu-id="96099-103">Windows8Api. Жеттрипререадиндексранжес, метод</span><span class="sxs-lookup"><span data-stu-id="96099-103">Windows8Api.JetTryPrereadIndexRanges method</span></span>

<span data-ttu-id="96099-104">Если записи с указанными диапазонами ключей отсутствуют в буферном кэше, запустите асинхронные операции чтения, чтобы перенести записи в буферный кэш базы данных.</span><span class="sxs-lookup"><span data-stu-id="96099-104">If the records with the specified key ranges are not in the buffer cache, then start asynchronous reads to bring the records into the database buffer cache.</span></span>

<span data-ttu-id="96099-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="96099-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="96099-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="96099-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="96099-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="96099-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetTryPrereadIndexRanges ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexRanges As JET_INDEX_RANGE(), _
    rangeIndex As Integer, _
    rangeCount As Integer, _
    <OutAttribute> ByRef rangesPreread As Integer, _
    columnsPreread As JET_COLUMNID(), _
    grbit As PrereadIndexRangesGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexRanges As JET_INDEX_RANGE()
Dim rangeIndex As Integer
Dim rangeCount As Integer
Dim rangesPreread As Integer
Dim columnsPreread As JET_COLUMNID()
Dim grbit As PrereadIndexRangesGrbit
Dim returnValue As Boolean

returnValue = Windows8Api.JetTryPrereadIndexRanges(sesid, _
    tableid, indexRanges, rangeIndex, _
    rangeCount, rangesPreread, columnsPreread, _
    grbit)
```

``` csharp
public static bool JetTryPrereadIndexRanges(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_INDEX_RANGE[] indexRanges,
    int rangeIndex,
    int rangeCount,
    out int rangesPreread,
    JET_COLUMNID[] columnsPreread,
    PrereadIndexRangesGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="96099-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="96099-108">Parameters</span></span>

  - <span data-ttu-id="96099-109">сесид</span><span class="sxs-lookup"><span data-stu-id="96099-109">sesid</span></span>  
    <span data-ttu-id="96099-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="96099-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="96099-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="96099-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="96099-112">TableID</span><span class="sxs-lookup"><span data-stu-id="96099-112">tableid</span></span>  
    <span data-ttu-id="96099-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="96099-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="96099-114">Таблица, для которой выдаются сведения о предчтении.</span><span class="sxs-lookup"><span data-stu-id="96099-114">The table to issue the prereads against.</span></span>

<!-- end list -->

  - <span data-ttu-id="96099-115">индексранжес</span><span class="sxs-lookup"><span data-stu-id="96099-115">indexRanges</span></span>  
    <span data-ttu-id="96099-116">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="96099-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="96099-117">Диапазоны ключей для чтения.</span><span class="sxs-lookup"><span data-stu-id="96099-117">The key ranges to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="96099-118">rangeIndex</span><span class="sxs-lookup"><span data-stu-id="96099-118">rangeIndex</span></span>  
    <span data-ttu-id="96099-119">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="96099-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="96099-120">Индекс первого диапазона ключей в массиве для чтения.</span><span class="sxs-lookup"><span data-stu-id="96099-120">The index of the first key range in the array to read.</span></span>

<!-- end list -->

  - <span data-ttu-id="96099-121">ранжекаунт</span><span class="sxs-lookup"><span data-stu-id="96099-121">rangeCount</span></span>  
    <span data-ttu-id="96099-122">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="96099-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="96099-123">Максимальное число диапазонов ключей для чтения.</span><span class="sxs-lookup"><span data-stu-id="96099-123">The maximum number of key ranges to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="96099-124">ранжеспререад</span><span class="sxs-lookup"><span data-stu-id="96099-124">rangesPreread</span></span>  
    <span data-ttu-id="96099-125">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="96099-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="96099-126">Возвращает количество ключей, фактически прочитанных в данный период.</span><span class="sxs-lookup"><span data-stu-id="96099-126">Returns the number of keys actually preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="96099-127">колумнспререад</span><span class="sxs-lookup"><span data-stu-id="96099-127">columnsPreread</span></span>  
    <span data-ttu-id="96099-128">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="96099-128">Type: \[\]</span></span>  
    
    <span data-ttu-id="96099-129">Список идентификаторов столбцов для столбцов с длинными значениями для чтения.</span><span class="sxs-lookup"><span data-stu-id="96099-129">List of column ids for long value columns to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="96099-130">грбит</span><span class="sxs-lookup"><span data-stu-id="96099-130">grbit</span></span>  
    <span data-ttu-id="96099-131">Тип: [Microsoft. ISAM. ESENT. Interop. Windows8. пререадиндексранжесгрбит](./prereadindexrangesgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="96099-131">Type: [Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="96099-132">Параметры для чтения.</span><span class="sxs-lookup"><span data-stu-id="96099-132">Preread options.</span></span> <span data-ttu-id="96099-133">Используется для указания направления выполнения перед чтением.</span><span class="sxs-lookup"><span data-stu-id="96099-133">Used to specify the direction of the preread.</span></span>

#### <a name="return-value"></a><span data-ttu-id="96099-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="96099-134">Return value</span></span>

<span data-ttu-id="96099-135">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="96099-135">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="96099-136">**\[ значение \] true** , если выполнено некоторое предсчитывание, и **\[ false \]** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="96099-136">**\[true\]** if some preread done, **\[false\]** otherwise.</span></span>  

## <a name="see-also"></a><span data-ttu-id="96099-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96099-137">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="96099-138">Справочник</span><span class="sxs-lookup"><span data-stu-id="96099-138">Reference</span></span>

[<span data-ttu-id="96099-139">Класс Windows8Api</span><span class="sxs-lookup"><span data-stu-id="96099-139">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="96099-140">Элементы Windows8Api</span><span class="sxs-lookup"><span data-stu-id="96099-140">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="96099-141">Пространство имен Microsoft. ISAM. ESENT. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="96099-141">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
