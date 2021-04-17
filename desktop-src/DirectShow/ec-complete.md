---
description: Все данные из определенного потока были подготовлены к просмотру.
ms.assetid: 46037d53-085d-4fd0-91a0-408702cbfce5
title: EC_COMPLETE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cd6d548a56173b9c6ea83426ddab3fa8556e312
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675570"
---
# <a name="ec_complete"></a><span data-ttu-id="c9a22-103">EC \_ завершено</span><span class="sxs-lookup"><span data-stu-id="c9a22-103">EC\_COMPLETE</span></span>

<span data-ttu-id="c9a22-104">Все данные из определенного потока были подготовлены к просмотру.</span><span class="sxs-lookup"><span data-stu-id="c9a22-104">All data from a particular stream has been rendered.</span></span>

## <a name="parameters"></a><span data-ttu-id="c9a22-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9a22-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9a22-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="c9a22-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="c9a22-107">(**HRESULT**) Состояние потока по завершении.</span><span class="sxs-lookup"><span data-stu-id="c9a22-107">(**HRESULT**) Status of the stream on completion.</span></span> <span data-ttu-id="c9a22-108">Если во время воспроизведения ошибок не возникло, значение равно S \_ .</span><span class="sxs-lookup"><span data-stu-id="c9a22-108">If no errors occurred during playback, the value is S\_OK.</span></span>

</dd> <dt>

<span data-ttu-id="c9a22-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="c9a22-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="c9a22-110">(**IUnknown** \* ) Ноль или указатель на интерфейс [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) визуализатора.</span><span class="sxs-lookup"><span data-stu-id="c9a22-110">(**IUnknown**\*) Zero, or a pointer to the renderer's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="c9a22-111">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c9a22-111">Default Action</span></span>

<span data-ttu-id="c9a22-112">По умолчанию диспетчер графов фильтров не перенаправляет это событие в приложение.</span><span class="sxs-lookup"><span data-stu-id="c9a22-112">By default, the filter graph manager does not forward this event to the application.</span></span> <span data-ttu-id="c9a22-113">Однако после того, как все потоки в отчете Graph **EC \_ завершены**, диспетчер графов фильтров публикует в приложении отдельное событие **EC \_ Complete** .</span><span class="sxs-lookup"><span data-stu-id="c9a22-113">However, after all the streams in the graph report **EC\_COMPLETE**, the filter graph manager posts a separate **EC\_COMPLETE** event to the application.</span></span>

<span data-ttu-id="c9a22-114">Если для этого события отключено действие по умолчанию, приложение получает все события **EC \_ Complete** из модулей подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="c9a22-114">If the default action is disabled for this event, the application receives all of the **EC\_COMPLETE** events from the renderers.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9a22-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c9a22-115">Remarks</span></span>

<span data-ttu-id="c9a22-116">Фильтр модуля подготовки отчетов отправляет это событие при получении уведомления конца потока.</span><span class="sxs-lookup"><span data-stu-id="c9a22-116">A renderer filter sends this event when it receives an end-of-stream notice.</span></span> <span data-ttu-id="c9a22-117">(В конце потока сообщается метод [**Ипин:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .) Фильтр отправляет ровно одно событие **\_ завершения EC** для каждого потока.</span><span class="sxs-lookup"><span data-stu-id="c9a22-117">(End-of-stream is signaled through the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.) The filter sends exactly one **EC\_COMPLETE** event for each stream.</span></span> <span data-ttu-id="c9a22-118">Перед отправкой события фильтр должен обработать все ожидающие выборки.</span><span class="sxs-lookup"><span data-stu-id="c9a22-118">The filter must process any pending samples before it sends the event.</span></span> <span data-ttu-id="c9a22-119">Остановка модуля подготовки отчетов сбрасывает все кэшированное состояние конца потока.</span><span class="sxs-lookup"><span data-stu-id="c9a22-119">Stopping a renderer resets any end-of-stream state that was cached.</span></span>

<span data-ttu-id="c9a22-120">Если модуль подготовки отчетов приостановлен, он не отправляет **EC \_ Complete** до тех пор, пока не будет вызван метод [**имедиафилтер:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) .</span><span class="sxs-lookup"><span data-stu-id="c9a22-120">If the renderer is paused, it does not send **EC\_COMPLETE** until the [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method is called.</span></span> <span data-ttu-id="c9a22-121">Более того, он по-своему отправляет события **EC \_ Complete** для каждого перехода от паузы до запуска, пока фильтр не будет остановлен или сброшен.</span><span class="sxs-lookup"><span data-stu-id="c9a22-121">Furthermore, it continues to send **EC\_COMPLETE** events for each transition from pause to run, until the filter is either stopped or flushed.</span></span>

<span data-ttu-id="c9a22-122">Фильтры присвойте параметру *lParam2* указатель [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .</span><span class="sxs-lookup"><span data-stu-id="c9a22-122">Filters set the *lParam2* parameter to an [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) pointer.</span></span> <span data-ttu-id="c9a22-123">Если включено действие по умолчанию, диспетчер графа фильтра устанавливает этот параметр в ноль.</span><span class="sxs-lookup"><span data-stu-id="c9a22-123">If the default action is enabled, the filter graph manager sets this parameter to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9a22-124">Требования</span><span class="sxs-lookup"><span data-stu-id="c9a22-124">Requirements</span></span>



| <span data-ttu-id="c9a22-125">Требование</span><span class="sxs-lookup"><span data-stu-id="c9a22-125">Requirement</span></span> | <span data-ttu-id="c9a22-126">Значение</span><span class="sxs-lookup"><span data-stu-id="c9a22-126">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c9a22-127">Header</span><span class="sxs-lookup"><span data-stu-id="c9a22-127">Header</span></span><br/> | <dl> <span data-ttu-id="c9a22-128"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9a22-128"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9a22-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9a22-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9a22-130">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="c9a22-130">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="c9a22-131">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="c9a22-131">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="c9a22-132">Альтернативные модули подготовки видео</span><span class="sxs-lookup"><span data-stu-id="c9a22-132">Alternative Video Renderers</span></span>](alternative-video-renderers.md)
</dt> </dl>

 

 




