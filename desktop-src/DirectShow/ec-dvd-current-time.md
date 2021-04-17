---
description: Сигнализирует о начале каждой единицы видеообъекта (ВОБУ) — сегмента видео, 0,4 – 1,0 секунд в длину.
ms.assetid: 1f2def2f-3a6b-458b-b564-09b6cf74543c
title: EC_DVD_CURRENT_TIME (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CURRENT_TIME
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 0f1bb2f5f31efa881917ac71ea381cc0a82e8744
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651856"
---
# <a name="ec_dvd_current_time"></a><span data-ttu-id="93e7b-103">\_ \_ Текущее время на DVD-диске EC \_</span><span class="sxs-lookup"><span data-stu-id="93e7b-103">EC\_DVD\_CURRENT\_TIME</span></span>

<span data-ttu-id="93e7b-104">Сигнализирует о начале каждой единицы видеообъекта (ВОБУ) — сегмента видео, 0,4 – 1,0 секунд в длину.</span><span class="sxs-lookup"><span data-stu-id="93e7b-104">Signals the beginning of every video object unit (VOBU), a video segment which is 0.4 to 1.0 seconds in length.</span></span>

## <a name="parameters"></a><span data-ttu-id="93e7b-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="93e7b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93e7b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="93e7b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="93e7b-107">Значение **типа DWORD** , указывающее время текущего времени воспроизведения в формате двоично-кодированных десятичных значений (BCD) часов, минут, секунд, кадров (чч: мм: СС: FF).</span><span class="sxs-lookup"><span data-stu-id="93e7b-107">**DWORD** value indicating the current playback timecode in a binary coded decimal (BCD) hours, minutes, seconds, frames (HH:MM:SS:FF) format.</span></span> <span data-ttu-id="93e7b-108">Элемент структуры времени в формате [**DVD \_**](/windows/win32/api/strmif/ns-strmif-dvd_timecode) .</span><span class="sxs-lookup"><span data-stu-id="93e7b-108">Member of the [**DVD\_TIMECODE**](/windows/win32/api/strmif/ns-strmif-dvd_timecode) structure.</span></span>

</dd> <dt>

<span data-ttu-id="93e7b-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="93e7b-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="93e7b-110">Логическое значение (**bool**), указывающее временной код.</span><span class="sxs-lookup"><span data-stu-id="93e7b-110">Boolean (**BOOL**) value indicating the timecode.</span></span> <span data-ttu-id="93e7b-111">Ноль (0) указывает 25 кадров в секунду, а 1 — 30 кадров в секунду (не отброшенных).</span><span class="sxs-lookup"><span data-stu-id="93e7b-111">Zero (0) indicates 25 frames per second while 1 indicates 30 frames per second (nondropped).</span></span> <span data-ttu-id="93e7b-112">Значение 2 указывает, что время воспроизведения не может быть определено.</span><span class="sxs-lookup"><span data-stu-id="93e7b-112">A value of 2 indicates the playback time cannot be determined.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="93e7b-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="93e7b-113">Remarks</span></span>

<span data-ttu-id="93e7b-114">Это событие сигнализирует только простым линейным роликам.</span><span class="sxs-lookup"><span data-stu-id="93e7b-114">Only simple linear movies signal this event.</span></span>

<span data-ttu-id="93e7b-115">Это событие возникает в домене Title.</span><span class="sxs-lookup"><span data-stu-id="93e7b-115">This event is raised in the title domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="93e7b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="93e7b-116">Requirements</span></span>



| <span data-ttu-id="93e7b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="93e7b-117">Requirement</span></span> | <span data-ttu-id="93e7b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="93e7b-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93e7b-119">Header</span><span class="sxs-lookup"><span data-stu-id="93e7b-119">Header</span></span><br/> | <dl> <span data-ttu-id="93e7b-120"><dt>Двдевкоде. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="93e7b-120"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93e7b-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93e7b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93e7b-122">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="93e7b-122">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="93e7b-123">Коды уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="93e7b-123">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="93e7b-124">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="93e7b-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




