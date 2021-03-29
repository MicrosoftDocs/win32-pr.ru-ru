---
description: 'Дополнительные сведения о методе: Windows8Api. Пререадкэйранжес'
title: Windows8Api. Пререадкэйранжес, метод (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'PrereadKeyRanges method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.PrereadKeyRanges(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[][],System.Int32[],System.Byte[][],System.Int32[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[],Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.prereadkeyranges(v=EXCHG.10)
ms:contentKeyID: 55104465
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.PrereadKeyRanges
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.PrereadKeyRanges
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 091c1f92512fd9a55bb4acd4d824567acc19fdde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991384"
---
# <a name="windows8apiprereadkeyranges-method"></a><span data-ttu-id="11eed-103">Windows8Api. Пререадкэйранжес, метод</span><span class="sxs-lookup"><span data-stu-id="11eed-103">Windows8Api.PrereadKeyRanges method</span></span>

<span data-ttu-id="11eed-104">Если записи с указанными диапазонами ключей отсутствуют в буферном кэше, запустите асинхронные операции чтения, чтобы перенести записи в буферный кэш базы данных.</span><span class="sxs-lookup"><span data-stu-id="11eed-104">If the records with the specified key ranges are not in the buffer cache then start asynchronous reads to bring the records into the database buffer cache.</span></span>

<span data-ttu-id="11eed-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="11eed-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="11eed-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="11eed-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="11eed-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11eed-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub PrereadKeyRanges ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    keysStart As Byte()(), _
    keyStartLengths As Integer(), _
    keysEnd As Byte()(), _
    keyEndLengths As Integer(), _
    rangeIndex As Integer, _
    rangeCount As Integer, _
    <OutAttribute> ByRef rangesPreread As Integer, _
    columnsPreread As JET_COLUMNID(), _
    grbit As PrereadIndexRangesGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim keysStart As Byte()()
Dim keyStartLengths As Integer()
Dim keysEnd As Byte()()
Dim keyEndLengths As Integer()
Dim rangeIndex As Integer
Dim rangeCount As Integer
Dim rangesPreread As Integer
Dim columnsPreread As JET_COLUMNID()
Dim grbit As PrereadIndexRangesGrbitWindows8Api.PrereadKeyRanges(sesid, tableid, _
    keysStart, keyStartLengths, keysEnd, _
    keyEndLengths, rangeIndex, rangeCount, _
    rangesPreread, columnsPreread, grbit)
```

``` csharp
public static void PrereadKeyRanges(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[][] keysStart,
    int[] keyStartLengths,
    byte[][] keysEnd,
    int[] keyEndLengths,
    int rangeIndex,
    int rangeCount,
    out int rangesPreread,
    JET_COLUMNID[] columnsPreread,
    PrereadIndexRangesGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="11eed-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="11eed-108">Parameters</span></span>

  - <span data-ttu-id="11eed-109">сесид</span><span class="sxs-lookup"><span data-stu-id="11eed-109">sesid</span></span>  
    <span data-ttu-id="11eed-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="11eed-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="11eed-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="11eed-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="11eed-112">TableID</span><span class="sxs-lookup"><span data-stu-id="11eed-112">tableid</span></span>  
    <span data-ttu-id="11eed-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="11eed-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="11eed-114">Таблица, для которой выдаются сведения о предчтении.</span><span class="sxs-lookup"><span data-stu-id="11eed-114">The table to issue the prereads against.</span></span>

<!-- end list -->

  - <span data-ttu-id="11eed-115">кэйсстарт</span><span class="sxs-lookup"><span data-stu-id="11eed-115">keysStart</span></span>  
    <span data-ttu-id="11eed-116">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="11eed-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="11eed-117">Начало диапазона ключевых диапазонов для чтения.</span><span class="sxs-lookup"><span data-stu-id="11eed-117">The start of key ranges to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="11eed-118">кэйстартленгсс</span><span class="sxs-lookup"><span data-stu-id="11eed-118">keyStartLengths</span></span>  
    <span data-ttu-id="11eed-119">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="11eed-119">Type: \[\]</span></span>  
    
    <span data-ttu-id="11eed-120">Длина начальных клавиш для чтения.</span><span class="sxs-lookup"><span data-stu-id="11eed-120">The lengths of the start keys to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="11eed-121">кэйсенд</span><span class="sxs-lookup"><span data-stu-id="11eed-121">keysEnd</span></span>  
    <span data-ttu-id="11eed-122">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="11eed-122">Type: \[\]</span></span>  
    
    <span data-ttu-id="11eed-123">Конец диапазона ключей для чтения.</span><span class="sxs-lookup"><span data-stu-id="11eed-123">The end of key rangess to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="11eed-124">кэйендленгсс</span><span class="sxs-lookup"><span data-stu-id="11eed-124">keyEndLengths</span></span>  
    <span data-ttu-id="11eed-125">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="11eed-125">Type: \[\]</span></span>  
    
    <span data-ttu-id="11eed-126">Длина конечных клавиш для чтения.</span><span class="sxs-lookup"><span data-stu-id="11eed-126">The lengths of the end keys to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="11eed-127">rangeIndex</span><span class="sxs-lookup"><span data-stu-id="11eed-127">rangeIndex</span></span>  
    <span data-ttu-id="11eed-128">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="11eed-128">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="11eed-129">Индекс первого диапазона ключей в массиве для чтения.</span><span class="sxs-lookup"><span data-stu-id="11eed-129">The index of the first key range in the array to read.</span></span>

<!-- end list -->

  - <span data-ttu-id="11eed-130">ранжекаунт</span><span class="sxs-lookup"><span data-stu-id="11eed-130">rangeCount</span></span>  
    <span data-ttu-id="11eed-131">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="11eed-131">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="11eed-132">Максимальное число диапазонов ключей для чтения.</span><span class="sxs-lookup"><span data-stu-id="11eed-132">The maximum number of key ranges to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="11eed-133">ранжеспререад</span><span class="sxs-lookup"><span data-stu-id="11eed-133">rangesPreread</span></span>  
    <span data-ttu-id="11eed-134">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="11eed-134">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="11eed-135">Возвращает количество ключей, фактически прочитанных в данный период.</span><span class="sxs-lookup"><span data-stu-id="11eed-135">Returns the number of keys actually preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="11eed-136">колумнспререад</span><span class="sxs-lookup"><span data-stu-id="11eed-136">columnsPreread</span></span>  
    <span data-ttu-id="11eed-137">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="11eed-137">Type: \[\]</span></span>  
    
    <span data-ttu-id="11eed-138">Список идентификаторов столбцов для столбцов с длинными значениями для чтения.</span><span class="sxs-lookup"><span data-stu-id="11eed-138">List of column ids for long value columns to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="11eed-139">грбит</span><span class="sxs-lookup"><span data-stu-id="11eed-139">grbit</span></span>  
    <span data-ttu-id="11eed-140">Тип: [Microsoft. ISAM. ESENT. Interop. Windows8. пререадиндексранжесгрбит](./prereadindexrangesgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="11eed-140">Type: [Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="11eed-141">Параметры для чтения.</span><span class="sxs-lookup"><span data-stu-id="11eed-141">Preread options.</span></span> <span data-ttu-id="11eed-142">Используется для указания направления выполнения перед чтением.</span><span class="sxs-lookup"><span data-stu-id="11eed-142">Used to specify the direction of the preread.</span></span>

## <a name="see-also"></a><span data-ttu-id="11eed-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11eed-143">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="11eed-144">Справочник</span><span class="sxs-lookup"><span data-stu-id="11eed-144">Reference</span></span>

[<span data-ttu-id="11eed-145">Класс Windows8Api</span><span class="sxs-lookup"><span data-stu-id="11eed-145">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="11eed-146">Элементы Windows8Api</span><span class="sxs-lookup"><span data-stu-id="11eed-146">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="11eed-147">Пространство имен Microsoft. ISAM. ESENT. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="11eed-147">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
