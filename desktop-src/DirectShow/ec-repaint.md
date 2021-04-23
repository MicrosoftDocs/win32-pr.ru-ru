---
description: Для модуля подготовки видео требуется перерисовка.
ms.assetid: 2e756dea-366c-4024-8fc8-6feabaef1954
title: EC_REPAINT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba86b54d6d465330ec1635ed7301ce774ef7cb27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685071"
---
# <a name="ec_repaint"></a><span data-ttu-id="cec02-103">\_ПЕРЕрисовка EC</span><span class="sxs-lookup"><span data-stu-id="cec02-103">EC\_REPAINT</span></span>

<span data-ttu-id="cec02-104">Для модуля подготовки видео требуется перерисовка.</span><span class="sxs-lookup"><span data-stu-id="cec02-104">A video renderer requires a repaint.</span></span>

## <a name="parameters"></a><span data-ttu-id="cec02-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="cec02-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cec02-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="cec02-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="cec02-107">(**IUnknown** \* ) Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) входного ПИН-кода модуля подготовки видео или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="cec02-107">(**IUnknown**\*) Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the video renderer's input pin, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cec02-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="cec02-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="cec02-109">Ноль.</span><span class="sxs-lookup"><span data-stu-id="cec02-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="cec02-110">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="cec02-110">Default Action</span></span>

<span data-ttu-id="cec02-111">Параметр *lParam1* может указывать входной ПИН-код модуля подготовки видео.</span><span class="sxs-lookup"><span data-stu-id="cec02-111">The *lParam1* parameter might specify the video renderer's input pin.</span></span> <span data-ttu-id="cec02-112">Если да, диспетчер графов фильтров находит ПИН-код вывода, подключенный к этому ПИН-коду, и запрашивает его для интерфейса [**имедиаевентсинк**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) .</span><span class="sxs-lookup"><span data-stu-id="cec02-112">If so, the filter graph manager finds the output pin connected to that pin and queries it for the [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface.</span></span> <span data-ttu-id="cec02-113">Если выходной ПИН-код поддерживает **имедиаевентсинк**, диспетчер графа фильтров вызывает [**Имедиаевентсинк:: notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) с \_ кодом события repain EC.</span><span class="sxs-lookup"><span data-stu-id="cec02-113">If the output pin supports **IMediaEventSink**, the filter graph manager calls [**IMediaEventSink::Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) with the EC\_REPAINT event code.</span></span> <span data-ttu-id="cec02-114">Это дает вышестоящему фильтру возможность повторной отправки последней выборки.</span><span class="sxs-lookup"><span data-stu-id="cec02-114">This gives the upstream filter the opportunity to re-send the last sample.</span></span>

<span data-ttu-id="cec02-115">Если *lParam1* имеет **значение NULL** или если ПИН-код не поддерживает [**имедиаевентсинк**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)или если метод [**Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) завершается неудачей, диспетчер графа фильтра обрабатывает \_ событие перерисовки EC по отдельности.</span><span class="sxs-lookup"><span data-stu-id="cec02-115">If *lParam1* is **NULL**, or if the pin does not support [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink), or if the [**Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) method fails, the filter graph manager handles the EC\_REPAINT event by itself.</span></span> <span data-ttu-id="cec02-116">Его поведение зависит от состояния графа:</span><span class="sxs-lookup"><span data-stu-id="cec02-116">Its behavior depends on the state of the graph:</span></span>

-   <span data-ttu-id="cec02-117">Работает: пропускает событие.</span><span class="sxs-lookup"><span data-stu-id="cec02-117">Running: Ignores the event.</span></span> <span data-ttu-id="cec02-118">(Модуль подготовки отчетов получит следующий пример в потоке.)</span><span class="sxs-lookup"><span data-stu-id="cec02-118">(The renderer will receive the next sample in the stream.)</span></span>
-   <span data-ttu-id="cec02-119">Приостановлено: выполняет поиск диаграммы в ее текущем расположении, тем самым заменяя фильтр и повторно поставит в очередь данные.</span><span class="sxs-lookup"><span data-stu-id="cec02-119">Paused: Seeks the graph to its current location, thereby flushing the filter and re-queuing the data.</span></span>
-   <span data-ttu-id="cec02-120">Остановлено: Приостановка и остановка графа, таким образом, повторная постановка данных в очередь.</span><span class="sxs-lookup"><span data-stu-id="cec02-120">Stopped: Pauses and stops the graph, thereby re-queuing the data.</span></span>

<span data-ttu-id="cec02-121">По умолчанию диспетчер графов фильтров не передает это событие в приложение.</span><span class="sxs-lookup"><span data-stu-id="cec02-121">By default, the filter graph manager does not pass this event to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="cec02-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cec02-122">Remarks</span></span>

<span data-ttu-id="cec02-123">Модули подготовки видео отправляют это сообщение, когда получают сообщение [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) и не имеют данных для отображения.</span><span class="sxs-lookup"><span data-stu-id="cec02-123">Video renderers send this message when they receive a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message and have no data to display.</span></span>

## <a name="requirements"></a><span data-ttu-id="cec02-124">Требования</span><span class="sxs-lookup"><span data-stu-id="cec02-124">Requirements</span></span>



| <span data-ttu-id="cec02-125">Требование</span><span class="sxs-lookup"><span data-stu-id="cec02-125">Requirement</span></span> | <span data-ttu-id="cec02-126">Значение</span><span class="sxs-lookup"><span data-stu-id="cec02-126">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cec02-127">Header</span><span class="sxs-lookup"><span data-stu-id="cec02-127">Header</span></span><br/> | <dl> <span data-ttu-id="cec02-128"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="cec02-128"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cec02-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cec02-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cec02-130">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="cec02-130">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="cec02-131">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="cec02-131">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

