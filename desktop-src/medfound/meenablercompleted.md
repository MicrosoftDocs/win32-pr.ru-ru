---
description: Вызывается объектом включения содержимого при завершении действия "объекты".
ms.assetid: 5162800c-9c55-40de-be66-a98765324f76
title: Событие Минаблеркомплетед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f05459a648f6b357fd483baa9fc56809540e64a1
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119449"
---
# <a name="meenablercompleted-event"></a><span data-ttu-id="e8e88-103">Событие Минаблеркомплетед</span><span class="sxs-lookup"><span data-stu-id="e8e88-103">MEEnablerCompleted event</span></span>

<span data-ttu-id="e8e88-104">Вызывается объектом включения содержимого при завершении действия по включению объекта.</span><span class="sxs-lookup"><span data-stu-id="e8e88-104">Raised by a content enabler object when the object's enabling action is completed.</span></span> <span data-ttu-id="e8e88-105">Это событие может вызываться объектами, которые предоставляют интерфейс [**имфконтентенаблер**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) .</span><span class="sxs-lookup"><span data-stu-id="e8e88-105">Objects that expose the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface can raise this event.</span></span> <span data-ttu-id="e8e88-106">Событие возникает, если происходит одно из следующих событий:</span><span class="sxs-lookup"><span data-stu-id="e8e88-106">The event is raised if either of the following occurs:</span></span>

-   <span data-ttu-id="e8e88-107">Метод [**имфконтентенаблер:: аутоматиценабле**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) завершается асинхронно.</span><span class="sxs-lookup"><span data-stu-id="e8e88-107">The [**IMFContentEnabler::AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) method completes asynchronously.</span></span>
-   <span data-ttu-id="e8e88-108">Приложение вызывает [**имфконтентенаблер:: мониторенабле**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable), а затем приложение ЗАВЕРШАЕТ запрос HTTP POST, как описано в методе **мониторенабле** .</span><span class="sxs-lookup"><span data-stu-id="e8e88-108">The application calls [**IMFContentEnabler::MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable), and then the application completes the HTTP POST request, as described in the **MonitorEnable** method.</span></span>

## <a name="event-values"></a><span data-ttu-id="e8e88-109">Значения событий</span><span class="sxs-lookup"><span data-stu-id="e8e88-109">Event values</span></span>

<span data-ttu-id="e8e88-110">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="e8e88-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="e8e88-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e8e88-111">VARTYPE</span></span>              | <span data-ttu-id="e8e88-112">Описание</span><span class="sxs-lookup"><span data-stu-id="e8e88-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="e8e88-113">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="e8e88-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="e8e88-114">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="e8e88-114">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="e8e88-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="e8e88-115">Remarks</span></span>

<span data-ttu-id="e8e88-116">Код состояния события может содержать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e8e88-116">The status code from the event may contain one of the following values.</span></span>



| <span data-ttu-id="e8e88-117">Значение</span><span class="sxs-lookup"><span data-stu-id="e8e88-117">Value</span></span>                                     | <span data-ttu-id="e8e88-118">Описание</span><span class="sxs-lookup"><span data-stu-id="e8e88-118">Description</span></span>                                                                                                                                                                                |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8e88-119">**\_ОК**</span><span class="sxs-lookup"><span data-stu-id="e8e88-119">**S\_OK**</span></span>                            | <span data-ttu-id="e8e88-120">Операция успешно выполнена.</span><span class="sxs-lookup"><span data-stu-id="e8e88-120">The operation succeeded.</span></span>                                                                                                                                                        |
| <span data-ttu-id="e8e88-121">**нотаккуиред лицензия на NS \_ E \_ DRM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e8e88-121">**NS\_E\_DRM\_LICENSE\_NOTACQUIRED**</span></span> | <span data-ttu-id="e8e88-122">Лицензия DRM не была получена.</span><span class="sxs-lookup"><span data-stu-id="e8e88-122">The DRM license was not acquired.</span></span> <span data-ttu-id="e8e88-123">Если предыдущая попытка использовала [**аутоматиценабле**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable), приложение должно попытаться не выполнять автоматическое получение.</span><span class="sxs-lookup"><span data-stu-id="e8e88-123">If the previous attempt used [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable), the application should try non-silent acquisition.</span></span> |
| <span data-ttu-id="e8e88-124">**\_ \_ монитор DRM NS \_ S \_ отменен**</span><span class="sxs-lookup"><span data-stu-id="e8e88-124">**NS\_S\_DRM\_MONITOR\_CANCELLED**</span></span>   | <span data-ttu-id="e8e88-125">Операция [**мониторенабле**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable) была отменена.</span><span class="sxs-lookup"><span data-stu-id="e8e88-125">The [**MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable) operation was canceled.</span></span>                                                                                            |



 

<span data-ttu-id="e8e88-126">Чтобы получить это событие, запросите интерфейс [**имфконтентенаблер**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) для интерфейса [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="e8e88-126">To receive this event, query the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface for the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="e8e88-127">Затем вызовите [**имфмедиаевентженератор:: бегинжетевент**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), как описано в разделе [генераторы событий мультимедиа](media-event-generators.md).</span><span class="sxs-lookup"><span data-stu-id="e8e88-127">Then call [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), as described in the topic [Media Event Generators](media-event-generators.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e8e88-128">Требования</span><span class="sxs-lookup"><span data-stu-id="e8e88-128">Requirements</span></span>



| <span data-ttu-id="e8e88-129">Требование</span><span class="sxs-lookup"><span data-stu-id="e8e88-129">Requirement</span></span> | <span data-ttu-id="e8e88-130">Значение</span><span class="sxs-lookup"><span data-stu-id="e8e88-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8e88-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e8e88-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e8e88-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e8e88-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e8e88-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e8e88-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e8e88-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e8e88-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e8e88-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e8e88-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8e88-136"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e8e88-136"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8e88-137">См. также</span><span class="sxs-lookup"><span data-stu-id="e8e88-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8e88-138">**имфконтентенаблер**</span><span class="sxs-lookup"><span data-stu-id="e8e88-138">**IMFContentEnabler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[<span data-ttu-id="e8e88-139">Генераторы событий мультимедиа</span><span class="sxs-lookup"><span data-stu-id="e8e88-139">Media Event Generators</span></span>](media-event-generators.md)
</dt> <dt>

[<span data-ttu-id="e8e88-140">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e8e88-140">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




