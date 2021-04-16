---
description: 'Дополнительные сведения: структура JET_INDEXRANGE'
title: Структура JET_INDEXRANGE
TOCTitle: JET_INDEXRANGE Structure
ms:assetid: 8e437f7d-1e21-4a0b-a5a5-1c78235a4f80
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269335(v=EXCHG.10)
ms:contentKeyID: 32765624
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ecbd8151be8ef278fc1bddc12323f41abd05b09e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712447"
---
# <a name="jet_indexrange-structure"></a><span data-ttu-id="4f6bf-103">Структура JET_INDEXRANGE</span><span class="sxs-lookup"><span data-stu-id="4f6bf-103">JET_INDEXRANGE Structure</span></span>


<span data-ttu-id="4f6bf-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4f6bf-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_indexrange-structure"></a><span data-ttu-id="4f6bf-105">Структура JET_INDEXRANGE</span><span class="sxs-lookup"><span data-stu-id="4f6bf-105">JET_INDEXRANGE Structure</span></span>

<span data-ttu-id="4f6bf-106">Структура **JET_INDEXRANGE** определяет диапазон индексов при использовании с функцией [жетинтерсектиндексес](./jetintersectindexes-function.md) .</span><span class="sxs-lookup"><span data-stu-id="4f6bf-106">The **JET_INDEXRANGE** structure identifies an index range when it is used with the [JetIntersectIndexes](./jetintersectindexes-function.md) function.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      JET_GRBIT grbit;
    } JET_INDEXRANGE;
```

### <a name="members"></a><span data-ttu-id="4f6bf-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="4f6bf-107">Members</span></span>

<span data-ttu-id="4f6bf-108">**кбструкт**</span><span class="sxs-lookup"><span data-stu-id="4f6bf-108">**cbStruct**</span></span>

<span data-ttu-id="4f6bf-109">Размер **JET_INDEXRANGE** в байтах.</span><span class="sxs-lookup"><span data-stu-id="4f6bf-109">The size, in bytes, of the **JET_INDEXRANGE**.</span></span>

<span data-ttu-id="4f6bf-110">**TableID**</span><span class="sxs-lookup"><span data-stu-id="4f6bf-110">**tableid**</span></span>

<span data-ttu-id="4f6bf-111">Курсор, для которого ранее был задан диапазон индексов с [жетсетиндексранже](./jetsetindexrange-function.md).</span><span class="sxs-lookup"><span data-stu-id="4f6bf-111">A cursor that has previously had an index range set with [JetSetIndexRange](./jetsetindexrange-function.md).</span></span>

<span data-ttu-id="4f6bf-112">**грбит**</span><span class="sxs-lookup"><span data-stu-id="4f6bf-112">**grbit**</span></span>

<span data-ttu-id="4f6bf-113">Битовая маска, состоящая только из одного из следующих элементов.</span><span class="sxs-lookup"><span data-stu-id="4f6bf-113">A bitmask composed of exactly one of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4f6bf-114">Значение</span><span class="sxs-lookup"><span data-stu-id="4f6bf-114">Value</span></span></p></th>
<th><p><span data-ttu-id="4f6bf-115">Значение</span><span class="sxs-lookup"><span data-stu-id="4f6bf-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4f6bf-116">JET_bitRecordInIndex</span><span class="sxs-lookup"><span data-stu-id="4f6bf-116">JET_bitRecordInIndex</span></span></p></td>
<td><p><span data-ttu-id="4f6bf-117">Указывает, что диапазон индекса должен обрабатываться обычным образом.</span><span class="sxs-lookup"><span data-stu-id="4f6bf-117">Specifies that the index range should be treated normally.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f6bf-118">JET_bitRecordNotInIndex</span><span class="sxs-lookup"><span data-stu-id="4f6bf-118">JET_bitRecordNotInIndex</span></span></p></td>
<td><p><span data-ttu-id="4f6bf-119">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="4f6bf-119">Reserved for future use.</span></span> <span data-ttu-id="4f6bf-120">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="4f6bf-120">Do not use.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a><span data-ttu-id="4f6bf-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4f6bf-121">Remarks</span></span>

<span data-ttu-id="4f6bf-122">Каждая **JET_INDEXRANGE** структура, передаваемая в [жетинтерсектиндексес](./jetintersectindexes-function.md) , представляет диапазон индекса, который будет пересекаться вызовом API.</span><span class="sxs-lookup"><span data-stu-id="4f6bf-122">Each **JET_INDEXRANGE** structure that is passed to [JetIntersectIndexes](./jetintersectindexes-function.md) represents an index range, which will be intersected by the API call.</span></span> <span data-ttu-id="4f6bf-123">Для курсора, заданного в **JET_INDEXRANGE** , должен быть уже установлен допустимый диапазон индексов с успешным вызовом [жетсетиндексранже](./jetsetindexrange-function.md).</span><span class="sxs-lookup"><span data-stu-id="4f6bf-123">The cursor that is given in **JET_INDEXRANGE** must have a valid index range set on it already, with a successful call to [JetSetIndexRange](./jetsetindexrange-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="4f6bf-124">Требования</span><span class="sxs-lookup"><span data-stu-id="4f6bf-124">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4f6bf-125"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="4f6bf-125"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4f6bf-126">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="4f6bf-126">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f6bf-127"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="4f6bf-127"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4f6bf-128">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="4f6bf-128">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f6bf-129"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="4f6bf-129"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4f6bf-130">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="4f6bf-130">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="4f6bf-131">См. также:</span><span class="sxs-lookup"><span data-stu-id="4f6bf-131">See Also</span></span>

[<span data-ttu-id="4f6bf-132">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="4f6bf-132">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="4f6bf-133">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="4f6bf-133">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="4f6bf-134">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="4f6bf-134">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="4f6bf-135">жетклосетабле</span><span class="sxs-lookup"><span data-stu-id="4f6bf-135">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="4f6bf-136">жетинтерсектиндексес</span><span class="sxs-lookup"><span data-stu-id="4f6bf-136">JetIntersectIndexes</span></span>](./jetintersectindexes-function.md)  
[<span data-ttu-id="4f6bf-137">жетсетиндексранже</span><span class="sxs-lookup"><span data-stu-id="4f6bf-137">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)
