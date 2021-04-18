---
description: 'Дополнительные сведения: структура JET_INDEXID'
title: Структура JET_INDEXID
TOCTitle: JET_INDEXID Structure
ms:assetid: 8b1d90f0-bc93-4b30-90d1-b9e93ad26654
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269327(v=EXCHG.10)
ms:contentKeyID: 32765617
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
ms.openlocfilehash: e1a9c6a971e44604240d750163f0570937f9d4db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713150"
---
# <a name="jet_indexid-structure"></a><span data-ttu-id="16fa2-103">Структура JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="16fa2-103">JET_INDEXID Structure</span></span>


<span data-ttu-id="16fa2-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="16fa2-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_indexid-structure"></a><span data-ttu-id="16fa2-105">Структура JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="16fa2-105">JET_INDEXID Structure</span></span>

<span data-ttu-id="16fa2-106">Структура **JET_INDEXID** содержит идентификатор индекса.</span><span class="sxs-lookup"><span data-stu-id="16fa2-106">The **JET_INDEXID** structure holds an index ID.</span></span> <span data-ttu-id="16fa2-107">Идентификатор индекса — это указание, которое используется для ускорения выбора текущего индекса с помощью [жетсеткуррентиндекс](./jetsetcurrentindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="16fa2-107">An index ID is a hint that is used to accelerate the selection of the current index using [JetSetCurrentIndex](./jetsetcurrentindex-function.md).</span></span> <span data-ttu-id="16fa2-108">Это наиболее полезно при наличии очень большого количества индексов в таблице.</span><span class="sxs-lookup"><span data-stu-id="16fa2-108">It is most useful when there is a very large number of indexes over a table.</span></span> <span data-ttu-id="16fa2-109">Идентификатор индекса можно получить с помощью [жетжетиндексинфо](./jetgetindexinfo-function.md) или [жетжеттаблеиндексинфо](./jetgettableindexinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="16fa2-109">The index ID can be retrieved using [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

```cpp
    typedef struct tagJET_INDEXID {
      unsigned long cbStruct;
      char rgbIndexId[sizeof(JET_API_PRT) + sizeof(unsigned long) + sizeof(unsigned long)];
    } JET_INDEXID;
```

### <a name="members"></a><span data-ttu-id="16fa2-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="16fa2-110">Members</span></span>

<span data-ttu-id="16fa2-111">**кбструкт**</span><span class="sxs-lookup"><span data-stu-id="16fa2-111">**cbStruct**</span></span>

<span data-ttu-id="16fa2-112">Размер идентификатора индекса в байтах.</span><span class="sxs-lookup"><span data-stu-id="16fa2-112">The size, in bytes, of the index ID.</span></span>

<span data-ttu-id="16fa2-113">Это фактический размер идентификатора индекса, возвращаемого в выходном буфере из [жетжетиндексинфо](./jetgetindexinfo-function.md) или [жетжеттаблеиндексинфо](./jetgettableindexinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="16fa2-113">This is the actual size of the index ID that is returned in the output buffer from [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

<span data-ttu-id="16fa2-114">**ргбиндексид**</span><span class="sxs-lookup"><span data-stu-id="16fa2-114">**rgbIndexId**</span></span>

<span data-ttu-id="16fa2-115">Непрозрачный большой двоичный объект данных, используемый ядром для быстрого обнаружения индекса в его кэше схемы.</span><span class="sxs-lookup"><span data-stu-id="16fa2-115">An opaque BLOB of information that is used by the engine to quickly identify an index in its schema cache.</span></span>

<span data-ttu-id="16fa2-116">Не пытайтесь интерпретировать большой двоичный объект данных.</span><span class="sxs-lookup"><span data-stu-id="16fa2-116">Do not attempt to interpret the BLOB of information.</span></span> <span data-ttu-id="16fa2-117">Размер не является установленным.</span><span class="sxs-lookup"><span data-stu-id="16fa2-117">It is not a set size.</span></span>

### <a name="requirements"></a><span data-ttu-id="16fa2-118">Требования</span><span class="sxs-lookup"><span data-stu-id="16fa2-118">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="16fa2-119"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="16fa2-119"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="16fa2-120">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="16fa2-120">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16fa2-121"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="16fa2-121"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="16fa2-122">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="16fa2-122">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16fa2-123"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="16fa2-123"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="16fa2-124">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="16fa2-124">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="16fa2-125">См. также:</span><span class="sxs-lookup"><span data-stu-id="16fa2-125">See Also</span></span>

[<span data-ttu-id="16fa2-126">жетжетиндексинфо</span><span class="sxs-lookup"><span data-stu-id="16fa2-126">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="16fa2-127">жетжеттаблеиндексинфо</span><span class="sxs-lookup"><span data-stu-id="16fa2-127">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="16fa2-128">жетжеттаблеинфо</span><span class="sxs-lookup"><span data-stu-id="16fa2-128">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)  
[<span data-ttu-id="16fa2-129">жетсеткуррентиндекс</span><span class="sxs-lookup"><span data-stu-id="16fa2-129">JetSetCurrentIndex</span></span>](./jetsetcurrentindex-function.md)
