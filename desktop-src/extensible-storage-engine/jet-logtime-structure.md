---
description: 'Дополнительные сведения: структура JET_LOGTIME'
title: Структура JET_LOGTIME
TOCTitle: JET_LOGTIME Structure
ms:assetid: cb7c0b74-db7a-4e48-80b8-37b3fdf6d088
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294089(v=EXCHG.10)
ms:contentKeyID: 32765704
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
ms.openlocfilehash: 9c99e2c1f77a01c33a75d3e5d16c4fe58c122a4e
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "103821589"
---
# <a name="jet_logtime-structure"></a><span data-ttu-id="b4371-103">Структура JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="b4371-103">JET_LOGTIME Structure</span></span>


<span data-ttu-id="b4371-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b4371-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_logtime-structure"></a><span data-ttu-id="b4371-105">Структура JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="b4371-105">JET_LOGTIME Structure</span></span>

<span data-ttu-id="b4371-106">Структура **JET_LOGTIME** содержит элементы даты и времени события.</span><span class="sxs-lookup"><span data-stu-id="b4371-106">The **JET_LOGTIME** structure holds elements of the date and time of an event.</span></span>

```cpp
typedef struct {
  char bSeconds;
  char bMinutes;
  char bHours;
  char bDay;
  char bMonth;
  char bYear;
  union {
    char bFiller1;
    struct {
        unsigned char fTimeIsUTC: 1;
        unsigned char fUnused: 7;
    };
  };
  char bFiller2;
} JET_LOGTIME;
```

### <a name="members"></a><span data-ttu-id="b4371-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="b4371-107">Members</span></span>

<span data-ttu-id="b4371-108">**бсекондс**</span><span class="sxs-lookup"><span data-stu-id="b4371-108">**bSeconds**</span></span>

<span data-ttu-id="b4371-109">Время события в секундах.</span><span class="sxs-lookup"><span data-stu-id="b4371-109">The time of the event in seconds.</span></span> <span data-ttu-id="b4371-110">Это значение может быть от 0 до 59.</span><span class="sxs-lookup"><span data-stu-id="b4371-110">This value can be 0 to 59.</span></span> <span data-ttu-id="b4371-111">0 используется, если структура имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="b4371-111">0 is used when the structure is null.</span></span>

<span data-ttu-id="b4371-112">**бминутес**</span><span class="sxs-lookup"><span data-stu-id="b4371-112">**bMinutes**</span></span>

<span data-ttu-id="b4371-113">Время события в минутах.</span><span class="sxs-lookup"><span data-stu-id="b4371-113">The time of the event in minutes.</span></span> <span data-ttu-id="b4371-114">Это значение может быть от 0 до 59.</span><span class="sxs-lookup"><span data-stu-id="b4371-114">This value can be 0 to 59.</span></span> <span data-ttu-id="b4371-115">0 используется, если структура имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="b4371-115">0 is used when the structure is null.</span></span>

<span data-ttu-id="b4371-116">**бхаурс**</span><span class="sxs-lookup"><span data-stu-id="b4371-116">**bHours**</span></span>

<span data-ttu-id="b4371-117">Время события в часах.</span><span class="sxs-lookup"><span data-stu-id="b4371-117">The time of the event in hours.</span></span> <span data-ttu-id="b4371-118">Это значение может быть от 0 до 23.</span><span class="sxs-lookup"><span data-stu-id="b4371-118">This value can be 0 to 23.</span></span> <span data-ttu-id="b4371-119">0 используется, если структура имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="b4371-119">0 is used when the structure is null.</span></span>

<span data-ttu-id="b4371-120">**бдай**</span><span class="sxs-lookup"><span data-stu-id="b4371-120">**bDay**</span></span>

<span data-ttu-id="b4371-121">День месяца события.</span><span class="sxs-lookup"><span data-stu-id="b4371-121">The day of the month of the event.</span></span> <span data-ttu-id="b4371-122">Это значение может быть от 0 до 31.</span><span class="sxs-lookup"><span data-stu-id="b4371-122">This value can be 0 to 31.</span></span> <span data-ttu-id="b4371-123">0 используется, если структура имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="b4371-123">0 is used when the structure is null.</span></span>

<span data-ttu-id="b4371-124">**бмонс**</span><span class="sxs-lookup"><span data-stu-id="b4371-124">**bMonth**</span></span>

<span data-ttu-id="b4371-125">Месяц года события.</span><span class="sxs-lookup"><span data-stu-id="b4371-125">The month of the year of the event.</span></span> <span data-ttu-id="b4371-126">Это значение может быть от 0 до 12.</span><span class="sxs-lookup"><span data-stu-id="b4371-126">This value can be 0 to 12.</span></span> <span data-ttu-id="b4371-127">0 используется, если структура имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="b4371-127">0 is used when the structure is null.</span></span>

<span data-ttu-id="b4371-128">**беар**</span><span class="sxs-lookup"><span data-stu-id="b4371-128">**bYear**</span></span>

<span data-ttu-id="b4371-129">Год события (смещение на 1900).</span><span class="sxs-lookup"><span data-stu-id="b4371-129">The year of the event (offset by 1900).</span></span> <span data-ttu-id="b4371-130">Чтобы достичь фактического года, добавьте 1900 к этому значению.</span><span class="sxs-lookup"><span data-stu-id="b4371-130">To achieve the actual year, add 1900 to this value.</span></span> <span data-ttu-id="b4371-131">0 используется, если структура имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="b4371-131">0 is used when the structure is null.</span></span>

<span data-ttu-id="b4371-132">**bFiller1**</span><span class="sxs-lookup"><span data-stu-id="b4371-132">**bFiller1**</span></span>

<span data-ttu-id="b4371-133">Это поле следует игнорировать.</span><span class="sxs-lookup"><span data-stu-id="b4371-133">This field should be ignored.</span></span>

<span data-ttu-id="b4371-134">**фтимеисутк**</span><span class="sxs-lookup"><span data-stu-id="b4371-134">**fTimeIsUTC**</span></span>

<span data-ttu-id="b4371-135">Время указано в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="b4371-135">The time is in UTC format.</span></span>

<span data-ttu-id="b4371-136">**фунусед**</span><span class="sxs-lookup"><span data-stu-id="b4371-136">**fUnused**</span></span>

<span data-ttu-id="b4371-137">Это поле следует игнорировать.</span><span class="sxs-lookup"><span data-stu-id="b4371-137">This field should be ignored.</span></span>

<span data-ttu-id="b4371-138">**bFiller2**</span><span class="sxs-lookup"><span data-stu-id="b4371-138">**bFiller2**</span></span>

<span data-ttu-id="b4371-139">Это поле следует игнорировать.</span><span class="sxs-lookup"><span data-stu-id="b4371-139">This field should be ignored.</span></span>

### <a name="remarks"></a><span data-ttu-id="b4371-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b4371-140">Remarks</span></span>

<span data-ttu-id="b4371-141">Эта структура предназначена главным образом для использования при отладке.</span><span class="sxs-lookup"><span data-stu-id="b4371-141">This structure is meant primarily for usage in debugging.</span></span>

### <a name="requirements"></a><span data-ttu-id="b4371-142">Требования</span><span class="sxs-lookup"><span data-stu-id="b4371-142">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4371-143"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="b4371-143"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b4371-144">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="b4371-144">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4371-145"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b4371-145"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b4371-146">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b4371-146">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4371-147"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="b4371-147"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b4371-148">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="b4371-148">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="b4371-149">См. также:</span><span class="sxs-lookup"><span data-stu-id="b4371-149">See Also</span></span>

[<span data-ttu-id="b4371-150">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="b4371-150">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)
