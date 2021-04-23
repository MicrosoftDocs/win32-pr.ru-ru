---
description: 'Дополнительные сведения: структура JET_RECPOS'
title: Структура JET_RECPOS
TOCTitle: JET_RECPOS Structure
ms:assetid: 7c335120-4b84-4095-8f13-e5315d4996b1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269308(v=EXCHG.10)
ms:contentKeyID: 32765598
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
ms.openlocfilehash: e24e16aaac4228f35350f55f57a14f2820add0cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712421"
---
# <a name="jet_recpos-structure"></a><span data-ttu-id="0d0a1-103">Структура JET_RECPOS</span><span class="sxs-lookup"><span data-stu-id="0d0a1-103">JET_RECPOS Structure</span></span>


<span data-ttu-id="0d0a1-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0d0a1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_recpos-structure"></a><span data-ttu-id="0d0a1-105">Структура JET_RECPOS</span><span class="sxs-lookup"><span data-stu-id="0d0a1-105">JET_RECPOS Structure</span></span>

<span data-ttu-id="0d0a1-106">Структура **JET_RECPOS** содержит коллекцию целых чисел, представляющих дробную точку в индексе.</span><span class="sxs-lookup"><span data-stu-id="0d0a1-106">The **JET_RECPOS** structure contains a collection of integers that represent a fractional position within an index.</span></span> <span data-ttu-id="0d0a1-107">**центриеслт** — число индексных записей, меньших, чем текущий ключ индекса.</span><span class="sxs-lookup"><span data-stu-id="0d0a1-107">**centriesLT** is the number of index entries less than the current index key.</span></span> <span data-ttu-id="0d0a1-108">**центриесинранже** — количество записей индекса, равное текущему ключу.</span><span class="sxs-lookup"><span data-stu-id="0d0a1-108">**centriesInRange** is the number of index entries equal to the current key.</span></span> <span data-ttu-id="0d0a1-109">**центриесинранже** не поддерживается и всегда возвращается как 1.</span><span class="sxs-lookup"><span data-stu-id="0d0a1-109">**centriesInRange** is not supported and is always returned as 1.</span></span> <span data-ttu-id="0d0a1-110">**центриестотал** — количество индексных записей в индексе.</span><span class="sxs-lookup"><span data-stu-id="0d0a1-110">**centriesTotal** is the number of index entries in the index.</span></span> <span data-ttu-id="0d0a1-111">Все значения являются приближениями без гарантии точности.</span><span class="sxs-lookup"><span data-stu-id="0d0a1-111">All values are approximations with no guarantee of accuracy.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long centriesLT;
      unsigned long centriesInRange;
      unsigned long centriesTotal;
    } JET_RECPOS;
```

### <a name="members"></a><span data-ttu-id="0d0a1-112">Элементы</span><span class="sxs-lookup"><span data-stu-id="0d0a1-112">Members</span></span>

<span data-ttu-id="0d0a1-113">**кбструкт**</span><span class="sxs-lookup"><span data-stu-id="0d0a1-113">**cbStruct**</span></span>

<span data-ttu-id="0d0a1-114">Размер структуры [JET_RETINFO](./jet-retinfo-structure.md) в байтах.</span><span class="sxs-lookup"><span data-stu-id="0d0a1-114">The size of the [JET_RETINFO](./jet-retinfo-structure.md) structure, in bytes.</span></span> <span data-ttu-id="0d0a1-115">Это значение подтверждает наличие следующих полей.</span><span class="sxs-lookup"><span data-stu-id="0d0a1-115">This value confirms the presence of the following fields.</span></span>

<span data-ttu-id="0d0a1-116">**центриеслт**</span><span class="sxs-lookup"><span data-stu-id="0d0a1-116">**centriesLT**</span></span>

<span data-ttu-id="0d0a1-117">Приблизительное количество элементов индекса меньше текущего.</span><span class="sxs-lookup"><span data-stu-id="0d0a1-117">The approximate number of index entries less than the current key.</span></span>

<span data-ttu-id="0d0a1-118">**центриесинранже**</span><span class="sxs-lookup"><span data-stu-id="0d0a1-118">**centriesInRange**</span></span>

<span data-ttu-id="0d0a1-119">Приблизительное число записей индекса, равное текущему ключу.</span><span class="sxs-lookup"><span data-stu-id="0d0a1-119">The approximate number of index entries equal to the current key.</span></span> <span data-ttu-id="0d0a1-120">Это поле всегда имеет значение 1, независимо от количества записей индекса, фактически равного текущему ключу.</span><span class="sxs-lookup"><span data-stu-id="0d0a1-120">This field is always set to 1, regardless of the number of index entries that are actually equal to the current key.</span></span>

<span data-ttu-id="0d0a1-121">**центриестотал**</span><span class="sxs-lookup"><span data-stu-id="0d0a1-121">**centriesTotal**</span></span>

<span data-ttu-id="0d0a1-122">Приблизительное количество записей в индексе.</span><span class="sxs-lookup"><span data-stu-id="0d0a1-122">The approximate number of entries in the index.</span></span>

### <a name="requirements"></a><span data-ttu-id="0d0a1-123">Требования</span><span class="sxs-lookup"><span data-stu-id="0d0a1-123">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0d0a1-124"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="0d0a1-124"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0d0a1-125">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="0d0a1-125">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d0a1-126"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="0d0a1-126"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0d0a1-127">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="0d0a1-127">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d0a1-128"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="0d0a1-128"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0d0a1-129">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="0d0a1-129">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="0d0a1-130">См. также:</span><span class="sxs-lookup"><span data-stu-id="0d0a1-130">See Also</span></span>

[<span data-ttu-id="0d0a1-131">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="0d0a1-131">JET_RETINFO</span></span>](./jet-retinfo-structure.md)  
[<span data-ttu-id="0d0a1-132">жетжетрекордпоситион</span><span class="sxs-lookup"><span data-stu-id="0d0a1-132">JetGetRecordPosition</span></span>](./jetgetrecordposition-function.md)
