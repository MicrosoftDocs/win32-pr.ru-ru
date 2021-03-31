---
description: 'Дополнительные сведения: структура JET_RECORDLIST'
title: Структура JET_RECORDLIST
TOCTitle: JET_RECORDLIST Structure
ms:assetid: 6b4d97a0-4b42-4f7c-bb18-b6db3c92668a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269287(v=EXCHG.10)
ms:contentKeyID: 32765579
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
ms.openlocfilehash: 16aca3a13bbae7c61bfe03aca49acea775820d39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912991"
---
# <a name="jet_recordlist-structure"></a><span data-ttu-id="366ef-103">Структура JET_RECORDLIST</span><span class="sxs-lookup"><span data-stu-id="366ef-103">JET_RECORDLIST Structure</span></span>


<span data-ttu-id="366ef-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="366ef-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_recordlist-structure"></a><span data-ttu-id="366ef-105">Структура JET_RECORDLIST</span><span class="sxs-lookup"><span data-stu-id="366ef-105">JET_RECORDLIST Structure</span></span>

<span data-ttu-id="366ef-106">Структура **JET_RECORDLIST** находит записи, находящиеся в пересечении указанных диапазонов индексов, когда они используются с функцией [жетинтерсектиндексес](./jetintersectindexes-function.md) .</span><span class="sxs-lookup"><span data-stu-id="366ef-106">The **JET_RECORDLIST** structure finds records that are in the intersection of specified index ranges when they are used with the [JetIntersectIndexes](./jetintersectindexes-function.md) function.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidBookmark;
    } JET_RECORDLIST;
```

### <a name="members"></a><span data-ttu-id="366ef-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="366ef-107">Members</span></span>

<span data-ttu-id="366ef-108">**кбструкт**</span><span class="sxs-lookup"><span data-stu-id="366ef-108">**cbStruct**</span></span>

<span data-ttu-id="366ef-109">Размер структуры **JET_RECORDLIST** в байтах.</span><span class="sxs-lookup"><span data-stu-id="366ef-109">The size of the **JET_RECORDLIST** structure, in bytes.</span></span>

<span data-ttu-id="366ef-110">**TableID**</span><span class="sxs-lookup"><span data-stu-id="366ef-110">**tableid**</span></span>

<span data-ttu-id="366ef-111">Идентификатор таблицы временной таблицы, содержащей закладки для результатов запроса.</span><span class="sxs-lookup"><span data-stu-id="366ef-111">The table identifier of a temporary table that contains the bookmarks for the results of the query.</span></span> <span data-ttu-id="366ef-112">Таблица будет автоматически закрыта при откате текущей транзакции с помощью [жетроллбакк](./jetrollback-function.md); в противном случае он должен быть закрыт с помощью [жетклосетабле](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="366ef-112">The table will automatically be closed if the current transaction is rolled back with [JetRollback](./jetrollback-function.md); otherwise, it must be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

<span data-ttu-id="366ef-113">**крекорд**</span><span class="sxs-lookup"><span data-stu-id="366ef-113">**cRecord**</span></span>

<span data-ttu-id="366ef-114">Количество строк во временной таблице.</span><span class="sxs-lookup"><span data-stu-id="366ef-114">The number of rows in the temporary table.</span></span>

<span data-ttu-id="366ef-115">**колумнидбукмарк**</span><span class="sxs-lookup"><span data-stu-id="366ef-115">**columnidBookmark**</span></span>

<span data-ttu-id="366ef-116">Идентификатор столбца закладки во временной таблице.</span><span class="sxs-lookup"><span data-stu-id="366ef-116">The column identifier of the bookmark column in the temporary table.</span></span>

### <a name="remarks"></a><span data-ttu-id="366ef-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="366ef-117">Remarks</span></span>

<span data-ttu-id="366ef-118">Временная таблица, идентифицируемая **tableid** , имеет один столбец.</span><span class="sxs-lookup"><span data-stu-id="366ef-118">The temporary table that is identified by **tableid** has a single column.</span></span> <span data-ttu-id="366ef-119">Этот один столбец содержит закладки, и каждая запись должна помещаться в буфер размером JET_cbBookmarkMost байт.</span><span class="sxs-lookup"><span data-stu-id="366ef-119">That single column holds bookmarks, and each record should fit in a buffer of size JET_cbBookmarkMost bytes.</span></span>

### <a name="requirements"></a><span data-ttu-id="366ef-120">Требования</span><span class="sxs-lookup"><span data-stu-id="366ef-120">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="366ef-121"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="366ef-121"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="366ef-122">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="366ef-122">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="366ef-123"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="366ef-123"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="366ef-124">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="366ef-124">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="366ef-125"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="366ef-125"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="366ef-126">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="366ef-126">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="366ef-127">См. также:</span><span class="sxs-lookup"><span data-stu-id="366ef-127">See Also</span></span>

[<span data-ttu-id="366ef-128">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="366ef-128">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="366ef-129">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="366ef-129">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="366ef-130">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="366ef-130">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="366ef-131">жетклосетабле</span><span class="sxs-lookup"><span data-stu-id="366ef-131">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="366ef-132">жетинтерсектиндексес</span><span class="sxs-lookup"><span data-stu-id="366ef-132">JetIntersectIndexes</span></span>](./jetintersectindexes-function.md)  
[<span data-ttu-id="366ef-133">жетроллбакк</span><span class="sxs-lookup"><span data-stu-id="366ef-133">JetRollback</span></span>](./jetrollback-function.md)
