---
description: 'Дополнительные сведения: структура JET_BKINFO'
title: Структура JET_BKINFO
TOCTitle: JET_BKINFO Structure
ms:assetid: dfaf1d72-1d5f-4777-91c1-6affb735b092
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294120(v=EXCHG.10)
ms:contentKeyID: 32765734
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
ms.openlocfilehash: 6c4849c23e742657d8f5eaba8a030426f7a2a440
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272134"
---
# <a name="jet_bkinfo-structure"></a><span data-ttu-id="b1d80-103">Структура JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="b1d80-103">JET_BKINFO Structure</span></span>


<span data-ttu-id="b1d80-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b1d80-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_bkinfo-structure"></a><span data-ttu-id="b1d80-105">Структура JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="b1d80-105">JET_BKINFO Structure</span></span>

<span data-ttu-id="b1d80-106">Структура **JET_BKINFO** содержит коллекцию данных о конкретном событии резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="b1d80-106">The **JET_BKINFO** structure holds a collection of data about a specific backup event.</span></span>

```cpp
    typedef struct {
      JET_LGPOS lgposMark;
      union {
        JET_LOGTIME logtimeMark;
        JET_BKLOGTIME bklogtimeMark;
      };
      unsigned long genLow;
      unsigned long genHigh;
    } JET_BKINFO;
```

### <a name="members"></a><span data-ttu-id="b1d80-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="b1d80-107">Members</span></span>

<span data-ttu-id="b1d80-108">**лгпосмарк**</span><span class="sxs-lookup"><span data-stu-id="b1d80-108">**lgposMark**</span></span>

<span data-ttu-id="b1d80-109">Идентификатор этой резервной копии.</span><span class="sxs-lookup"><span data-stu-id="b1d80-109">The ID of this backup.</span></span>

<span data-ttu-id="b1d80-110">**логтимемарк**</span><span class="sxs-lookup"><span data-stu-id="b1d80-110">**logtimeMark**</span></span>

<span data-ttu-id="b1d80-111">Время события резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="b1d80-111">The time of this backup event.</span></span>

<span data-ttu-id="b1d80-112">**бклогтимемарк**</span><span class="sxs-lookup"><span data-stu-id="b1d80-112">**bklogtimeMark**</span></span>

<span data-ttu-id="b1d80-113">Время события резервного копирования с дополнительными битами для указания резервной копии моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="b1d80-113">The time of this backup event, with additional bits to indicate a snapshot backup.</span></span>

<span data-ttu-id="b1d80-114">**Windows Vista: бклогтимемарк** появился в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b1d80-114">**Windows Vista:  bklogtimeMark** is introduced in Windows Vista.</span></span>

<span data-ttu-id="b1d80-115">**женлов**</span><span class="sxs-lookup"><span data-stu-id="b1d80-115">**genLow**</span></span>

<span data-ttu-id="b1d80-116">Младший номер создания журнала, связанный с этим событием резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="b1d80-116">The low log generation number associated with this backup event.</span></span>

<span data-ttu-id="b1d80-117">**женхигх**</span><span class="sxs-lookup"><span data-stu-id="b1d80-117">**genHigh**</span></span>

<span data-ttu-id="b1d80-118">Старший номер создания журнала, связанный с этим событием резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="b1d80-118">The high log generation number associated with this backup event.</span></span>

### <a name="remarks"></a><span data-ttu-id="b1d80-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b1d80-119">Remarks</span></span>

<span data-ttu-id="b1d80-120">Эта структура используется в структуре [JET_DBINFOMISC](./jet-dbinfomisc-structure.md) для представления данных о событии резервного копирования базы данных.</span><span class="sxs-lookup"><span data-stu-id="b1d80-120">This structure is used inside the [JET_DBINFOMISC](./jet-dbinfomisc-structure.md) structure to represent data about the database backup event.</span></span>

### <a name="requirements"></a><span data-ttu-id="b1d80-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b1d80-121">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b1d80-122"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="b1d80-122"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b1d80-123">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="b1d80-123">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1d80-124"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b1d80-124"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b1d80-125">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b1d80-125">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1d80-126"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="b1d80-126"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b1d80-127">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="b1d80-127">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="b1d80-128">См. также:</span><span class="sxs-lookup"><span data-stu-id="b1d80-128">See Also</span></span>

[<span data-ttu-id="b1d80-129">JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="b1d80-129">JET_LGPOS</span></span>](./jet-lgpos-structure.md)  
[<span data-ttu-id="b1d80-130">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="b1d80-130">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="b1d80-131">JET_BKLOGTIME</span><span class="sxs-lookup"><span data-stu-id="b1d80-131">JET_BKLOGTIME</span></span>](./jet-bklogtime-structure.md)  
[<span data-ttu-id="b1d80-132">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="b1d80-132">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)
