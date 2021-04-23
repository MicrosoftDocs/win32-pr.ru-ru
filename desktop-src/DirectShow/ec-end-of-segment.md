---
description: Достигнут конец сегмента.
ms.assetid: 07f141b1-2e96-49e2-9cf7-581690e245b5
title: EC_END_OF_SEGMENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a779b0f46a031ad694bd3fed3fe29536424a3a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675444"
---
# <a name="ec_end_of_segment"></a><span data-ttu-id="4fb22-103">\_конец \_ \_ сегмента EC</span><span class="sxs-lookup"><span data-stu-id="4fb22-103">EC\_END\_OF\_SEGMENT</span></span>

<span data-ttu-id="4fb22-104">Достигнут конец сегмента.</span><span class="sxs-lookup"><span data-stu-id="4fb22-104">The end of a segment was reached.</span></span>

## <a name="parameters"></a><span data-ttu-id="4fb22-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="4fb22-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fb22-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="4fb22-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="4fb22-107">( **\_ время ссылки на\*\*\*\*константу** \* ) указатель на значение **\_ времени ссылки** , указывающее накопленное время потока с начала сегмента в 100-наносекундных единицах.</span><span class="sxs-lookup"><span data-stu-id="4fb22-107">(**const** **REFERENCE\_TIME**\*) Pointer to a **REFERENCE\_TIME** value that specifies the accumulated stream time since the start of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="4fb22-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="4fb22-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="4fb22-109">(**DWORD**) Номер сегмента (от нуля).</span><span class="sxs-lookup"><span data-stu-id="4fb22-109">(**DWORD**) Segment number (zero-based).</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="4fb22-110">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="4fb22-110">Default Action</span></span>

<span data-ttu-id="4fb22-111">Диспетчер графов фильтров проверяет количество событий **\_ завершения \_ \_ сегмента EC** по числу событий [**\_ \_ начала сегмента EC**](ec-segment-started.md) .</span><span class="sxs-lookup"><span data-stu-id="4fb22-111">The filter graph manager checks the number of **EC\_END\_OF\_SEGMENT** events against the number of [**EC\_SEGMENT\_STARTED**](ec-segment-started.md) events.</span></span> <span data-ttu-id="4fb22-112">Если они совпадают, перенаправляет событие **\_ конца \_ \_ сегмента EC** в приложение.</span><span class="sxs-lookup"><span data-stu-id="4fb22-112">If they match, it forwards the **EC\_END\_OF\_SEGMENT** event to the application.</span></span> <span data-ttu-id="4fb22-113">Приложения не могут переопределять действие по умолчанию для этого события.</span><span class="sxs-lookup"><span data-stu-id="4fb22-113">Applications cannot override the default action for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fb22-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4fb22-114">Remarks</span></span>

<span data-ttu-id="4fb22-115">Этот код события поддерживает простой цикл.</span><span class="sxs-lookup"><span data-stu-id="4fb22-115">This event code supports seamless looping.</span></span> <span data-ttu-id="4fb22-116">Когда вызов метода [**имедиасикинг:: сетпоситионс**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) включает \_ флаг «поиск \_ сегмента», фильтр источника отправляет этот код события вместо вызова [**Ипин:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream).</span><span class="sxs-lookup"><span data-stu-id="4fb22-116">When a call to the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method includes the AM\_SEEKING\_Segment flag, the source filter sends this event code instead of calling [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream).</span></span>

## <a name="requirements"></a><span data-ttu-id="4fb22-117">Требования</span><span class="sxs-lookup"><span data-stu-id="4fb22-117">Requirements</span></span>



| <span data-ttu-id="4fb22-118">Требование</span><span class="sxs-lookup"><span data-stu-id="4fb22-118">Requirement</span></span> | <span data-ttu-id="4fb22-119">Значение</span><span class="sxs-lookup"><span data-stu-id="4fb22-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4fb22-120">Header</span><span class="sxs-lookup"><span data-stu-id="4fb22-120">Header</span></span><br/> | <dl> <span data-ttu-id="4fb22-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fb22-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fb22-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4fb22-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fb22-123">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="4fb22-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="4fb22-124">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="4fb22-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




