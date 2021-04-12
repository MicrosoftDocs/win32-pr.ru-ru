---
description: Структура СЕССИОНСТАТС предоставляет статистику о сеансе.
ms.assetid: 51a6a601-634e-4d97-8c85-d3961400a2d1
title: Структура СЕССИОНСТАТС (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SESSIONSTATS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4eddfa6b0a45627c59e61fd083eb11b8d5f26caf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263948"
---
# <a name="sessionstats-structure"></a><span data-ttu-id="b3c84-103">Структура СЕССИОНСТАТС</span><span class="sxs-lookup"><span data-stu-id="b3c84-103">SESSIONSTATS structure</span></span>

<span data-ttu-id="b3c84-104">Структура **сессионстатс** предоставляет статистику о [*сеансе*](s.md).</span><span class="sxs-lookup"><span data-stu-id="b3c84-104">The **SESSIONSTATS** structure provides statistics about a [*session*](s.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b3c84-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b3c84-105">Syntax</span></span>


```C++
typedef struct _SESSIONSTATS {
  DWORD NextSession;
  DWORD StationOwner;
  DWORD StationPartner;
  DWORD Flags;
  DWORD TotalPacketsSent;
} SESSIONSTATS, *LPSESSIONSTATS;
```



## <a name="members"></a><span data-ttu-id="b3c84-106">Члены</span><span class="sxs-lookup"><span data-stu-id="b3c84-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b3c84-107">**некстсессион**</span><span class="sxs-lookup"><span data-stu-id="b3c84-107">**NextSession**</span></span>
</dt> <dd>

<span data-ttu-id="b3c84-108">Индекс следующего сеанса владельца станции.</span><span class="sxs-lookup"><span data-stu-id="b3c84-108">Index of the station owner's next session.</span></span>

</dd> <dt>

<span data-ttu-id="b3c84-109">**статионовнер**</span><span class="sxs-lookup"><span data-stu-id="b3c84-109">**StationOwner**</span></span>
</dt> <dd>

<span data-ttu-id="b3c84-110">Индекс станции-владельца в связанном массиве структуры [статионстатс](stationstats.md) .</span><span class="sxs-lookup"><span data-stu-id="b3c84-110">Index of a owner station within the associated [STATIONSTATS](stationstats.md) structure array.</span></span> <span data-ttu-id="b3c84-111">Станция-владелец — это станция, которая инициировала сеанс, станция, которая отправила пакеты сеанса.</span><span class="sxs-lookup"><span data-stu-id="b3c84-111">The owner station is the station that initiated the session, the station that sent the packets of the session.</span></span>

</dd> <dt>

<span data-ttu-id="b3c84-112">**статионпартнер**</span><span class="sxs-lookup"><span data-stu-id="b3c84-112">**StationPartner**</span></span>
</dt> <dd>

<span data-ttu-id="b3c84-113">Индекс другой станции в связанном массиве структуры [статионстатс](stationstats.md) .</span><span class="sxs-lookup"><span data-stu-id="b3c84-113">Index of the other station within the associated [STATIONSTATS](stationstats.md) structure array.</span></span> <span data-ttu-id="b3c84-114">Партнерская станция — это станция, которая получила пакеты сеанса.</span><span class="sxs-lookup"><span data-stu-id="b3c84-114">The partner station is the station that received the packets of the session.</span></span>

</dd> <dt>

<span data-ttu-id="b3c84-115">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="b3c84-115">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="b3c84-116">Этот элемент устарел.</span><span class="sxs-lookup"><span data-stu-id="b3c84-116">This member is obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="b3c84-117">**тоталпаккетссент**</span><span class="sxs-lookup"><span data-stu-id="b3c84-117">**TotalPacketsSent**</span></span>
</dt> <dd>

<span data-ttu-id="b3c84-118">Число пакетов, отправленных в сеансе.</span><span class="sxs-lookup"><span data-stu-id="b3c84-118">Number of packets sent in the session.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3c84-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b3c84-119">Remarks</span></span>

<span data-ttu-id="b3c84-120">Сетевой монитор хранит сведения о сеансе и станции в двух связанных массивах, элементы которых являются структурами **сессионстатс** и [статионстатс](stationstats.md) соответственно.</span><span class="sxs-lookup"><span data-stu-id="b3c84-120">Network Monitor stores session and station information in two associated arrays, whose elements are **SESSIONSTATS** and [STATIONSTATS](stationstats.md) structures respectively.</span></span> <span data-ttu-id="b3c84-121">Члены этих структур можно использовать для перехода между ними.</span><span class="sxs-lookup"><span data-stu-id="b3c84-121">The members of these structures can be used to navigate between them.</span></span> <span data-ttu-id="b3c84-122">Например, чтобы перейти к следующему сеансу для конкретного владельца станции, используйте **некстсессион**.</span><span class="sxs-lookup"><span data-stu-id="b3c84-122">For example, to move to the next session for a specific station owner, use **NextSession**.</span></span> <span data-ttu-id="b3c84-123">Чтобы перейти к владельцу и партнерской станции сеанса в массиве СТАТИОНСТАТС, используйте индекс, указанный в **статионовнер** и **статионпартнер**.</span><span class="sxs-lookup"><span data-stu-id="b3c84-123">To jump to the owner and partner station of the session in the STATIONSTATS array, use the index provided in **StationOwner** and **StationPartner**.</span></span>

> [!Note]  
> <span data-ttu-id="b3c84-124">Массив СЕССИОНСТАТС содержит элемент для каждого сеанса в текущей записи.</span><span class="sxs-lookup"><span data-stu-id="b3c84-124">The SESSIONSTATS array contains an element for each session in the current capture.</span></span> <span data-ttu-id="b3c84-125">Алгоритм сетевой монитор, используемый для добавления элементов в массив СЕССИОНСТАТС, основан на эффективной записи информации во время выполнения записи.</span><span class="sxs-lookup"><span data-stu-id="b3c84-125">The algorithm Network Monitor uses to add elements to the SESSIONSTATS array is based on efficiently recording information while the capture is in progress.</span></span> <span data-ttu-id="b3c84-126">Следовательно, следующий сеанс для определенной станции-владельца не всегда является следующим элементом массива.</span><span class="sxs-lookup"><span data-stu-id="b3c84-126">Consequently, the next session for a specific owner station is not always the next element in the array.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b3c84-127">Требования</span><span class="sxs-lookup"><span data-stu-id="b3c84-127">Requirements</span></span>



| <span data-ttu-id="b3c84-128">Требование</span><span class="sxs-lookup"><span data-stu-id="b3c84-128">Requirement</span></span> | <span data-ttu-id="b3c84-129">Значение</span><span class="sxs-lookup"><span data-stu-id="b3c84-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b3c84-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b3c84-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b3c84-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b3c84-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b3c84-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b3c84-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b3c84-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b3c84-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b3c84-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b3c84-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3c84-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3c84-135"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3c84-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b3c84-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3c84-137">Иделайдк:: Жетконверсатионстатистикс</span><span class="sxs-lookup"><span data-stu-id="b3c84-137">IDelaydC::GetConversationStatistics</span></span>](idelaydc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="b3c84-138">ИРТК:: Жетконверсатионстатистикс</span><span class="sxs-lookup"><span data-stu-id="b3c84-138">IRTC::GetConversationStatistics</span></span>](irtc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="b3c84-139">Истатс:: Жетконверсатионстатистикс</span><span class="sxs-lookup"><span data-stu-id="b3c84-139">IStats::GetConversationStatistics</span></span>](istats-getconversationstatistics.md)
</dt> </dl>

 

 




