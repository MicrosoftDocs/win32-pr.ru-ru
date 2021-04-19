---
description: 'Дополнительные сведения: структура JET_THREADSTATS'
title: Структура JET_THREADSTATS
TOCTitle: JET_THREADSTATS Structure
ms:assetid: 37e86e14-7719-4991-aae8-bcff1baa80df
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269227(v=EXCHG.10)
ms:contentKeyID: 32765529
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
ms.openlocfilehash: 2b84de9a4f64db5dda261b8ee177787f62fd01ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702800"
---
# <a name="jet_threadstats-structure"></a><span data-ttu-id="baeb7-103">Структура JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="baeb7-103">JET_THREADSTATS Structure</span></span>


<span data-ttu-id="baeb7-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="baeb7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_threadstats-structure"></a><span data-ttu-id="baeb7-105">Структура JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="baeb7-105">JET_THREADSTATS Structure</span></span>

<span data-ttu-id="baeb7-106">Структура **JET_THREADSTATS** содержит совокупную статистику по работе, выполненной ядром СУБД в текущем потоке.</span><span class="sxs-lookup"><span data-stu-id="baeb7-106">The **JET_THREADSTATS** structure contains cumulative statistics on the work performed by the database engine on the current thread.</span></span> <span data-ttu-id="baeb7-107">Эти сведения возвращаются через [жетжетсреадстатс](./jetgetthreadstats-function.md).</span><span class="sxs-lookup"><span data-stu-id="baeb7-107">This information is returned via [JetGetThreadStats](./jetgetthreadstats-function.md).</span></span>

<span data-ttu-id="baeb7-108">**Windows Vista:**  Структура **JET_THREADSTATS** появилась в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="baeb7-108">**Windows Vista:**  The **JET_THREADSTATS** structure is introduced in Windows Vista.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cPageReferenced;
      unsigned long cPageRead;
      unsigned long cPagePreread;
      unsigned long cPageDirtied;
      unsigned long cPageRedirtied;
      unsigned long cLogRecord;
      unsigned long cbLogRecord;
    } JET_THREADSTATS;
```

### <a name="members"></a><span data-ttu-id="baeb7-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="baeb7-109">Members</span></span>

<span data-ttu-id="baeb7-110">**кбструкт**</span><span class="sxs-lookup"><span data-stu-id="baeb7-110">**cbStruct**</span></span>

<span data-ttu-id="baeb7-111">Размер возвращаемой структуры **JET_THREADSTATS** в байтах.</span><span class="sxs-lookup"><span data-stu-id="baeb7-111">The size of the returned **JET_THREADSTATS** structure, in bytes.</span></span>

<span data-ttu-id="baeb7-112">**Примечание**  .  Структура **JET_THREADSTATS** будет расширена в будущем, чтобы она содержала больше статистики.</span><span class="sxs-lookup"><span data-stu-id="baeb7-112">**Note**  The **JET_THREADSTATS** structure will expand in the future to contain more statistics.</span></span> <span data-ttu-id="baeb7-113">Новая статистика будет добавлена в конец структуры и может быть извлечена с увеличением размера выходного буфера.</span><span class="sxs-lookup"><span data-stu-id="baeb7-113">New statistics will be added to the end of the structure and can be retrieved with an increased output buffer size.</span></span> <span data-ttu-id="baeb7-114">Наличие дополнительной статистики может быть выведено с помощью большего значения **кбструкт** .</span><span class="sxs-lookup"><span data-stu-id="baeb7-114">The presence of additional statistics can be inferred by a larger **cbStruct** value.</span></span>

<span data-ttu-id="baeb7-115">**кпажереференцед**</span><span class="sxs-lookup"><span data-stu-id="baeb7-115">**cPageReferenced**</span></span>

<span data-ttu-id="baeb7-116">Общее число страниц базы данных, посещенных ядром СУБД в текущем потоке.</span><span class="sxs-lookup"><span data-stu-id="baeb7-116">The total number of database pages visited by the database engine on the current thread.</span></span>

<span data-ttu-id="baeb7-117">**кпажереад**</span><span class="sxs-lookup"><span data-stu-id="baeb7-117">**cPageRead**</span></span>

<span data-ttu-id="baeb7-118">Общее число страниц базы данных, извлекаемых с диска ядром СУБД в текущем потоке.</span><span class="sxs-lookup"><span data-stu-id="baeb7-118">The total number of database pages fetched from disk by the database engine on the current thread.</span></span>

<span data-ttu-id="baeb7-119">**кпажепререад**</span><span class="sxs-lookup"><span data-stu-id="baeb7-119">**cPagePreread**</span></span>

<span data-ttu-id="baeb7-120">Общее число страниц базы данных, выбранных с диска ядром СУБД в текущем потоке.</span><span class="sxs-lookup"><span data-stu-id="baeb7-120">The total number of database pages prefetched from disk by the database engine on the current thread.</span></span>

<span data-ttu-id="baeb7-121">**кпажедиртиед**</span><span class="sxs-lookup"><span data-stu-id="baeb7-121">**cPageDirtied**</span></span>

<span data-ttu-id="baeb7-122">Общее число страниц базы данных без незаписанных изменений, которые были изменены ядром СУБД в текущем потоке.</span><span class="sxs-lookup"><span data-stu-id="baeb7-122">The total number of database pages, with no unwritten changes, that have been modified by the database engine on the current thread.</span></span>

<span data-ttu-id="baeb7-123">**кпажередиртиед**</span><span class="sxs-lookup"><span data-stu-id="baeb7-123">**cPageRedirtied**</span></span>

<span data-ttu-id="baeb7-124">Общее число страниц базы данных с незаписанными изменениями, которые были изменены ядром СУБД в текущем потоке.</span><span class="sxs-lookup"><span data-stu-id="baeb7-124">The total number of database pages, with unwritten changes, that have been modified by the database engine on the current thread.</span></span>

<span data-ttu-id="baeb7-125">**клогрекорд**</span><span class="sxs-lookup"><span data-stu-id="baeb7-125">**cLogRecord**</span></span>

<span data-ttu-id="baeb7-126">Общее число записей журнала транзакций, созданных ядром СУБД в текущем потоке.</span><span class="sxs-lookup"><span data-stu-id="baeb7-126">The total number of transaction log records that have been generated by the database engine on the current thread.</span></span>

<span data-ttu-id="baeb7-127">**кблогрекорд**</span><span class="sxs-lookup"><span data-stu-id="baeb7-127">**cbLogRecord**</span></span>

<span data-ttu-id="baeb7-128">Общий размер в байтах записей журнала транзакций, созданных ядром СУБД в текущем потоке.</span><span class="sxs-lookup"><span data-stu-id="baeb7-128">The total size in bytes of transaction log records that have been generated by the database engine on the current thread.</span></span>

### <a name="requirements"></a><span data-ttu-id="baeb7-129">Требования</span><span class="sxs-lookup"><span data-stu-id="baeb7-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="baeb7-130"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="baeb7-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="baeb7-131">Требуется Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="baeb7-131">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baeb7-132"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="baeb7-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="baeb7-133">Требуется Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="baeb7-133">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baeb7-134"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="baeb7-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="baeb7-135">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="baeb7-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="baeb7-136">См. также:</span><span class="sxs-lookup"><span data-stu-id="baeb7-136">See Also</span></span>

[<span data-ttu-id="baeb7-137">жетжетсреадстатс</span><span class="sxs-lookup"><span data-stu-id="baeb7-137">JetGetThreadStats</span></span>](./jetgetthreadstats-function.md)
