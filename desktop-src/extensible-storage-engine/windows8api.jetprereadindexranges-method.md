---
description: 'Дополнительные сведения о методе: Windows8Api. Жетпререадиндексранжес'
title: Windows8Api. Жетпререадиндексранжес, метод (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'JetPrereadIndexRanges method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetPrereadIndexRanges(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_RANGE[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[],Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetprereadindexranges(v=EXCHG.10)
ms:contentKeyID: 55104451
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetPrereadIndexRanges
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetPrereadIndexRanges
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 986213a054dec54e92e4ecfe6fb0abd541b451ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701766"
---
# <a name="windows8apijetprereadindexranges-method"></a><span data-ttu-id="2cda7-103">Windows8Api. Жетпререадиндексранжес, метод</span><span class="sxs-lookup"><span data-stu-id="2cda7-103">Windows8Api.JetPrereadIndexRanges method</span></span>

<span data-ttu-id="2cda7-104">Если записи с указанными диапазонами ключей отсутствуют в буферном кэше, запустите асинхронные операции чтения, чтобы перенести записи в буферный кэш базы данных.</span><span class="sxs-lookup"><span data-stu-id="2cda7-104">If the records with the specified key ranges are not in the buffer cache, then start asynchronous reads to bring the records into the database buffer cache.</span></span>

<span data-ttu-id="2cda7-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2cda7-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="2cda7-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2cda7-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2cda7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2cda7-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetPrereadIndexRanges ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexRanges As JET_INDEX_RANGE(), _
    rangeIndex As Integer, _
    rangeCount As Integer, _
    <OutAttribute> ByRef rangesPreread As Integer, _
    columnsPreread As JET_COLUMNID(), _
    grbit As PrereadIndexRangesGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexRanges As JET_INDEX_RANGE()
Dim rangeIndex As Integer
Dim rangeCount As Integer
Dim rangesPreread As Integer
Dim columnsPreread As JET_COLUMNID()
Dim grbit As PrereadIndexRangesGrbitWindows8Api.JetPrereadIndexRanges(sesid, _
    tableid, indexRanges, rangeIndex, _
    rangeCount, rangesPreread, columnsPreread, _
    grbit)
```

``` csharp
public static void JetPrereadIndexRanges(
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

#### <a name="parameters"></a><span data-ttu-id="2cda7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2cda7-108">Parameters</span></span>

  - <span data-ttu-id="2cda7-109">сесид</span><span class="sxs-lookup"><span data-stu-id="2cda7-109">sesid</span></span>  
    <span data-ttu-id="2cda7-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2cda7-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="2cda7-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="2cda7-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="2cda7-112">TableID</span><span class="sxs-lookup"><span data-stu-id="2cda7-112">tableid</span></span>  
    <span data-ttu-id="2cda7-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2cda7-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="2cda7-114">Таблица, для которой выдаются сведения о предчтении.</span><span class="sxs-lookup"><span data-stu-id="2cda7-114">The table to issue the prereads against.</span></span>

<!-- end list -->

  - <span data-ttu-id="2cda7-115">индексранжес</span><span class="sxs-lookup"><span data-stu-id="2cda7-115">indexRanges</span></span>  
    <span data-ttu-id="2cda7-116">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="2cda7-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="2cda7-117">Диапазоны ключей для чтения.</span><span class="sxs-lookup"><span data-stu-id="2cda7-117">The key ranges to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="2cda7-118">rangeIndex</span><span class="sxs-lookup"><span data-stu-id="2cda7-118">rangeIndex</span></span>  
    <span data-ttu-id="2cda7-119">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="2cda7-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="2cda7-120">Индекс первого диапазона ключей в массиве для чтения.</span><span class="sxs-lookup"><span data-stu-id="2cda7-120">The index of the first key range in the array to read.</span></span>

<!-- end list -->

  - <span data-ttu-id="2cda7-121">ранжекаунт</span><span class="sxs-lookup"><span data-stu-id="2cda7-121">rangeCount</span></span>  
    <span data-ttu-id="2cda7-122">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="2cda7-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="2cda7-123">Максимальное число диапазонов ключей для чтения.</span><span class="sxs-lookup"><span data-stu-id="2cda7-123">The maximum number of key ranges to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="2cda7-124">ранжеспререад</span><span class="sxs-lookup"><span data-stu-id="2cda7-124">rangesPreread</span></span>  
    <span data-ttu-id="2cda7-125">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="2cda7-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="2cda7-126">Возвращает количество ключей, фактически прочитанных в данный период.</span><span class="sxs-lookup"><span data-stu-id="2cda7-126">Returns the number of keys actually preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="2cda7-127">колумнспререад</span><span class="sxs-lookup"><span data-stu-id="2cda7-127">columnsPreread</span></span>  
    <span data-ttu-id="2cda7-128">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="2cda7-128">Type: \[\]</span></span>  
    
    <span data-ttu-id="2cda7-129">Список идентификаторов столбцов для столбцов с длинными значениями для чтения.</span><span class="sxs-lookup"><span data-stu-id="2cda7-129">List of column ids for long value columns to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="2cda7-130">грбит</span><span class="sxs-lookup"><span data-stu-id="2cda7-130">grbit</span></span>  
    <span data-ttu-id="2cda7-131">Тип: [Microsoft. ISAM. ESENT. Interop. Windows8. пререадиндексранжесгрбит](./prereadindexrangesgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="2cda7-131">Type: [Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="2cda7-132">Параметры для чтения.</span><span class="sxs-lookup"><span data-stu-id="2cda7-132">Preread options.</span></span> <span data-ttu-id="2cda7-133">Используется для указания направления выполнения перед чтением.</span><span class="sxs-lookup"><span data-stu-id="2cda7-133">Used to specify the direction of the preread.</span></span>

## <a name="see-also"></a><span data-ttu-id="2cda7-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2cda7-134">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2cda7-135">Справочник</span><span class="sxs-lookup"><span data-stu-id="2cda7-135">Reference</span></span>

[<span data-ttu-id="2cda7-136">Класс Windows8Api</span><span class="sxs-lookup"><span data-stu-id="2cda7-136">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="2cda7-137">Элементы Windows8Api</span><span class="sxs-lookup"><span data-stu-id="2cda7-137">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="2cda7-138">Пространство имен Microsoft. ISAM. ESENT. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="2cda7-138">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
