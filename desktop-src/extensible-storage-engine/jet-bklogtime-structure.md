---
description: 'Дополнительные сведения: структура JET_BKLOGTIME'
title: Структура JET_BKLOGTIME
TOCTitle: JET_BKLOGTIME Structure
ms:assetid: 31460079-7c5b-4145-837d-b112ba0117d6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269219(v=EXCHG.10)
ms:contentKeyID: 32765522
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
ms.openlocfilehash: 0b3ebfd1c0b807a491695ba18d6735e0230a16fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693438"
---
# <a name="jet_bklogtime-structure"></a><span data-ttu-id="579a5-103">Структура JET_BKLOGTIME</span><span class="sxs-lookup"><span data-stu-id="579a5-103">JET_BKLOGTIME Structure</span></span>


<span data-ttu-id="579a5-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="579a5-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_bklogtime-structure"></a><span data-ttu-id="579a5-105">Структура JET_BKLOGTIME</span><span class="sxs-lookup"><span data-stu-id="579a5-105">JET_BKLOGTIME Structure</span></span>

<span data-ttu-id="579a5-106">Структура **JET_BKLOGTIME** содержит элементы даты и времени события.</span><span class="sxs-lookup"><span data-stu-id="579a5-106">The **JET_BKLOGTIME** structure holds the date and time elements of an event.</span></span> <span data-ttu-id="579a5-107">Это расширение [JET_LOGTIME](./jet-logtime-structure.md).</span><span class="sxs-lookup"><span data-stu-id="579a5-107">It is an extension of [JET_LOGTIME](./jet-logtime-structure.md).</span></span>

<span data-ttu-id="579a5-108">**Windows Vista: JET_BKLOGTIME** впервые появился в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="579a5-108">**Windows Vista:  JET_BKLOGTIME** is introduced in Windows Vista.</span></span>

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
      union {
        char bFiller2;
        struct {
          unsigned char fOSSnapshot  :1;
          unsigned char fReserved  :7;
        };
      };
    } JET_BKLOGTIME;
```

### <a name="members"></a><span data-ttu-id="579a5-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="579a5-109">Members</span></span>

<span data-ttu-id="579a5-110">**бсекондс**</span><span class="sxs-lookup"><span data-stu-id="579a5-110">**bSeconds**</span></span>

<span data-ttu-id="579a5-111">Время события в секундах.</span><span class="sxs-lookup"><span data-stu-id="579a5-111">The time of the event in seconds.</span></span> <span data-ttu-id="579a5-112">Это может быть 0 (ноль) до 60.</span><span class="sxs-lookup"><span data-stu-id="579a5-112">This can be 0 (zero) to 60.</span></span> <span data-ttu-id="579a5-113">0 (нуль) используется, если структура **JET_BKLOGTIME** имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="579a5-113">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="579a5-114">**бминутес**</span><span class="sxs-lookup"><span data-stu-id="579a5-114">**bMinutes**</span></span>

<span data-ttu-id="579a5-115">Время события в минутах.</span><span class="sxs-lookup"><span data-stu-id="579a5-115">The time of the event in minutes.</span></span> <span data-ttu-id="579a5-116">Это может быть 0 (ноль) до 60.</span><span class="sxs-lookup"><span data-stu-id="579a5-116">This can be 0 (zero) to 60.</span></span> <span data-ttu-id="579a5-117">0 (нуль) используется, если структура **JET_BKLOGTIME** имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="579a5-117">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="579a5-118">**бхаурс**</span><span class="sxs-lookup"><span data-stu-id="579a5-118">**bHours**</span></span>

<span data-ttu-id="579a5-119">Время события в часах.</span><span class="sxs-lookup"><span data-stu-id="579a5-119">The time of the event in hours.</span></span> <span data-ttu-id="579a5-120">Может иметь значение от 0 до 24.</span><span class="sxs-lookup"><span data-stu-id="579a5-120">This can be 0 (zero) to 24.</span></span> <span data-ttu-id="579a5-121">0 (нуль) используется, если структура **JET_BKLOGTIME** имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="579a5-121">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="579a5-122">**бдай**</span><span class="sxs-lookup"><span data-stu-id="579a5-122">**bDay**</span></span>

<span data-ttu-id="579a5-123">День месяца события.</span><span class="sxs-lookup"><span data-stu-id="579a5-123">The day of the month of the event.</span></span> <span data-ttu-id="579a5-124">Может иметь значение от 0 до 31.</span><span class="sxs-lookup"><span data-stu-id="579a5-124">This can be 0 (zero) to 31.</span></span> <span data-ttu-id="579a5-125">0 (нуль) используется, если структура **JET_BKLOGTIME** имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="579a5-125">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="579a5-126">**бмонс**</span><span class="sxs-lookup"><span data-stu-id="579a5-126">**bMonth**</span></span>

<span data-ttu-id="579a5-127">Месяц года события.</span><span class="sxs-lookup"><span data-stu-id="579a5-127">The month of the year of the event.</span></span> <span data-ttu-id="579a5-128">Это может быть 0 (нуля) до 12.</span><span class="sxs-lookup"><span data-stu-id="579a5-128">This can be 0 (zero) to 12.</span></span> <span data-ttu-id="579a5-129">0 (нуль) используется, если структура **JET_BKLOGTIME** имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="579a5-129">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="579a5-130">**беар**</span><span class="sxs-lookup"><span data-stu-id="579a5-130">**bYear**</span></span>

<span data-ttu-id="579a5-131">Год (смещение на 1900) события.</span><span class="sxs-lookup"><span data-stu-id="579a5-131">The year (offset by 1900) of the event.</span></span> <span data-ttu-id="579a5-132">Чтобы достичь фактического года, добавьте 1900 к этому значению.</span><span class="sxs-lookup"><span data-stu-id="579a5-132">To achieve the actual year, add 1900 to this value.</span></span> <span data-ttu-id="579a5-133">0 (нуль) используется, если структура **JET_BKLOGTIME** имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="579a5-133">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="579a5-134">**bFiller1**</span><span class="sxs-lookup"><span data-stu-id="579a5-134">**bFiller1**</span></span>

<span data-ttu-id="579a5-135">Это поле следует игнорировать.</span><span class="sxs-lookup"><span data-stu-id="579a5-135">This field should be ignored.</span></span>

<span data-ttu-id="579a5-136">**фтимеисутк**</span><span class="sxs-lookup"><span data-stu-id="579a5-136">**fTimeIsUTC**</span></span>

<span data-ttu-id="579a5-137">Время указано в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="579a5-137">The time is in UTC format.</span></span>

<span data-ttu-id="579a5-138">**фунусед**</span><span class="sxs-lookup"><span data-stu-id="579a5-138">**fUnused**</span></span>

<span data-ttu-id="579a5-139">Это поле следует игнорировать.</span><span class="sxs-lookup"><span data-stu-id="579a5-139">This field should be ignored.</span></span>

<span data-ttu-id="579a5-140">**bFiller2**</span><span class="sxs-lookup"><span data-stu-id="579a5-140">**bFiller2**</span></span>

<span data-ttu-id="579a5-141">Это поле следует игнорировать.</span><span class="sxs-lookup"><span data-stu-id="579a5-141">This field should be ignored.</span></span>

<span data-ttu-id="579a5-142">**фосснапшот**</span><span class="sxs-lookup"><span data-stu-id="579a5-142">**fOSSnapshot**</span></span>

<span data-ttu-id="579a5-143">Если это событие является резервной копией, этот флаг содержит одно из следующих возможных значений:</span><span class="sxs-lookup"><span data-stu-id="579a5-143">If this event is a backup, this flag contains one of the following possible values:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="579a5-144">Имя</span><span class="sxs-lookup"><span data-stu-id="579a5-144">Name</span></span></p></th>
<th><p><span data-ttu-id="579a5-145">Значение</span><span class="sxs-lookup"><span data-stu-id="579a5-145">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="579a5-146">Потоковая Архивация</span><span class="sxs-lookup"><span data-stu-id="579a5-146">streaming backup</span></span></p></td>
<td><p><span data-ttu-id="579a5-147">Ноль (0)</span><span class="sxs-lookup"><span data-stu-id="579a5-147">0 (zero)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="579a5-148">Резервное копирование моментальных снимков</span><span class="sxs-lookup"><span data-stu-id="579a5-148">snapshot backup</span></span></p></td>
<td><p><span data-ttu-id="579a5-149">1</span><span class="sxs-lookup"><span data-stu-id="579a5-149">1</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="579a5-150">**фресервед**</span><span class="sxs-lookup"><span data-stu-id="579a5-150">**fReserved**</span></span>

<span data-ttu-id="579a5-151">Это поле следует игнорировать.</span><span class="sxs-lookup"><span data-stu-id="579a5-151">This field should be ignored.</span></span>

### <a name="remarks"></a><span data-ttu-id="579a5-152">Комментарии</span><span class="sxs-lookup"><span data-stu-id="579a5-152">Remarks</span></span>

<span data-ttu-id="579a5-153">Эта структура используется при отладке.</span><span class="sxs-lookup"><span data-stu-id="579a5-153">This structure is used when debugging.</span></span>

### <a name="requirements"></a><span data-ttu-id="579a5-154">Требования</span><span class="sxs-lookup"><span data-stu-id="579a5-154">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="579a5-155"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="579a5-155"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="579a5-156">Требуется Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="579a5-156">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="579a5-157"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="579a5-157"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="579a5-158">Требуется Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="579a5-158">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="579a5-159"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="579a5-159"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="579a5-160">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="579a5-160">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="579a5-161">См. также:</span><span class="sxs-lookup"><span data-stu-id="579a5-161">See Also</span></span>

[<span data-ttu-id="579a5-162">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="579a5-162">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="579a5-163">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="579a5-163">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)
