---
description: Начат новый сегмент.
ms.assetid: 9742436a-e233-4641-a0d5-aa240cde5f28
title: EC_SEGMENT_STARTED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7e7df85bddb78fe2687a017b481e6db62ba37c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651647"
---
# <a name="ec_segment_started"></a><span data-ttu-id="292f3-103">\_сегмент EC \_ запущен</span><span class="sxs-lookup"><span data-stu-id="292f3-103">EC\_SEGMENT\_STARTED</span></span>

<span data-ttu-id="292f3-104">Начат новый сегмент.</span><span class="sxs-lookup"><span data-stu-id="292f3-104">A new segment has started.</span></span>

## <a name="parameters"></a><span data-ttu-id="292f3-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="292f3-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="292f3-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="292f3-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="292f3-107">( **\_ время ссылки на\*\*\*\*константу** \* ) указатель на значение **\_ времени ссылки** , указывающее накопленное время потока с начала сегмента в 100-наносекундных единицах.</span><span class="sxs-lookup"><span data-stu-id="292f3-107">(**const** **REFERENCE\_TIME**\*) Pointer to a **REFERENCE\_TIME** value that specifies the accumulated stream time since the start of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="292f3-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="292f3-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="292f3-109">(**DWORD**) Номер сегмента (от нуля).</span><span class="sxs-lookup"><span data-stu-id="292f3-109">(**DWORD**) Segment number (zero-based).</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="292f3-110">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="292f3-110">Default Action</span></span>

<span data-ttu-id="292f3-111">Это событие не отправляется в приложение.</span><span class="sxs-lookup"><span data-stu-id="292f3-111">This event is not sent to the application.</span></span> <span data-ttu-id="292f3-112">Приложения не могут переопределять действие по умолчанию для этого события.</span><span class="sxs-lookup"><span data-stu-id="292f3-112">Applications cannot override the default action for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="292f3-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="292f3-113">Remarks</span></span>

<span data-ttu-id="292f3-114">Если фильтр будет отправлять конец сегмента [**EC \_ \_ \_**](ec-end-of-segment.md) в конце сегмента, он отправляет это событие в начале сегмента.</span><span class="sxs-lookup"><span data-stu-id="292f3-114">If a filter will send an [**EC\_END\_OF\_SEGMENT**](ec-end-of-segment.md) at the end of a segment, it sends this event at the start of the segment.</span></span> <span data-ttu-id="292f3-115">Диспетчер графов фильтров использует это уведомление о событии, чтобы вычислить, сколько \_ \_ уведомлений в виде конца сегмента EC \_ должно рассчитываться в конце сегмента.</span><span class="sxs-lookup"><span data-stu-id="292f3-115">The filter graph manager uses this event notification to compute how many EC\_END\_OF\_SEGMENT notifications it should expect at the end of the segment.</span></span>

<span data-ttu-id="292f3-116">По умолчанию фильтры не отправляют данные о [**\_ завершении событий \_ \_ сегмента EC**](ec-end-of-segment.md) в конце сегментов и поэтому не должны отсылать это событие.</span><span class="sxs-lookup"><span data-stu-id="292f3-116">By default, filters do not send [**EC\_END\_OF\_SEGMENT**](ec-end-of-segment.md) events at the end of segments, and therefore should not send this event.</span></span> <span data-ttu-id="292f3-117">Дополнительные сведения см. в разделе [**имедиасикинг:: сетпоситионс**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span><span class="sxs-lookup"><span data-stu-id="292f3-117">For more information, see [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span></span>

## <a name="requirements"></a><span data-ttu-id="292f3-118">Требования</span><span class="sxs-lookup"><span data-stu-id="292f3-118">Requirements</span></span>



| <span data-ttu-id="292f3-119">Требование</span><span class="sxs-lookup"><span data-stu-id="292f3-119">Requirement</span></span> | <span data-ttu-id="292f3-120">Значение</span><span class="sxs-lookup"><span data-stu-id="292f3-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="292f3-121">Header</span><span class="sxs-lookup"><span data-stu-id="292f3-121">Header</span></span><br/> | <dl> <span data-ttu-id="292f3-122"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="292f3-122"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="292f3-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="292f3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="292f3-124">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="292f3-124">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="292f3-125">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="292f3-125">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




