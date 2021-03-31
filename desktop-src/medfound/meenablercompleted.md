---
description: Вызывается объектом включения содержимого при завершении действия "объекты".
ms.assetid: 5162800c-9c55-40de-be66-a98765324f76
title: Событие Минаблеркомплетед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a74f7379ccc2983abd2327e1250bcf1ca14e688
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155591"
---
# <a name="meenablercompleted-event"></a><span data-ttu-id="b60c4-103">Событие Минаблеркомплетед</span><span class="sxs-lookup"><span data-stu-id="b60c4-103">MEEnablerCompleted event</span></span>

<span data-ttu-id="b60c4-104">Вызывается объектом включения содержимого при завершении действия по включению объекта.</span><span class="sxs-lookup"><span data-stu-id="b60c4-104">Raised by a content enabler object when the object's enabling action is completed.</span></span> <span data-ttu-id="b60c4-105">Это событие может вызываться объектами, которые предоставляют интерфейс [**имфконтентенаблер**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) .</span><span class="sxs-lookup"><span data-stu-id="b60c4-105">Objects that expose the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface can raise this event.</span></span> <span data-ttu-id="b60c4-106">Событие возникает, если происходит одно из следующих событий:</span><span class="sxs-lookup"><span data-stu-id="b60c4-106">The event is raised if either of the following occurs:</span></span>

-   <span data-ttu-id="b60c4-107">Метод [**имфконтентенаблер:: аутоматиценабле**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) завершается асинхронно.</span><span class="sxs-lookup"><span data-stu-id="b60c4-107">The [**IMFContentEnabler::AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) method completes asynchronously.</span></span>
-   <span data-ttu-id="b60c4-108">Приложение вызывает [**имфконтентенаблер:: мониторенабле**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable), а затем приложение ЗАВЕРШАЕТ запрос HTTP POST, как описано в методе **мониторенабле** .</span><span class="sxs-lookup"><span data-stu-id="b60c4-108">The application calls [**IMFContentEnabler::MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable), and then the application completes the HTTP POST request, as described in the **MonitorEnable** method.</span></span>

## <a name="event-values"></a><span data-ttu-id="b60c4-109">Значения событий</span><span class="sxs-lookup"><span data-stu-id="b60c4-109">Event values</span></span>

<span data-ttu-id="b60c4-110">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="b60c4-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="b60c4-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="b60c4-111">VARTYPE</span></span>              | <span data-ttu-id="b60c4-112">Описание</span><span class="sxs-lookup"><span data-stu-id="b60c4-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="b60c4-113">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="b60c4-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="b60c4-114">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="b60c4-114">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="b60c4-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b60c4-115">Remarks</span></span>

<span data-ttu-id="b60c4-116">Код состояния события может содержать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="b60c4-116">The status code from the event may contain one of the following values.</span></span>



|                                      |                                                                                                                                                                                 |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b60c4-117">**\_ОК**</span><span class="sxs-lookup"><span data-stu-id="b60c4-117">**S\_OK**</span></span>                            | <span data-ttu-id="b60c4-118">Операция успешно выполнена.</span><span class="sxs-lookup"><span data-stu-id="b60c4-118">The operation succeeded.</span></span>                                                                                                                                                        |
| <span data-ttu-id="b60c4-119">**нотаккуиред лицензия на NS \_ E \_ DRM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b60c4-119">**NS\_E\_DRM\_LICENSE\_NOTACQUIRED**</span></span> | <span data-ttu-id="b60c4-120">Лицензия DRM не была получена.</span><span class="sxs-lookup"><span data-stu-id="b60c4-120">The DRM license was not acquired.</span></span> <span data-ttu-id="b60c4-121">Если предыдущая попытка использовала [**аутоматиценабле**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable), приложение должно попытаться не выполнять автоматическое получение.</span><span class="sxs-lookup"><span data-stu-id="b60c4-121">If the previous attempt used [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable), the application should try non-silent acquisition.</span></span> |
| <span data-ttu-id="b60c4-122">**\_ \_ монитор DRM NS \_ S \_ отменен**</span><span class="sxs-lookup"><span data-stu-id="b60c4-122">**NS\_S\_DRM\_MONITOR\_CANCELLED**</span></span>   | <span data-ttu-id="b60c4-123">Операция [**мониторенабле**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable) была отменена.</span><span class="sxs-lookup"><span data-stu-id="b60c4-123">The [**MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable) operation was canceled.</span></span>                                                                                            |



 

<span data-ttu-id="b60c4-124">Чтобы получить это событие, запросите интерфейс [**имфконтентенаблер**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) для интерфейса [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="b60c4-124">To receive this event, query the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface for the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="b60c4-125">Затем вызовите [**имфмедиаевентженератор:: бегинжетевент**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), как описано в разделе [генераторы событий мультимедиа](media-event-generators.md).</span><span class="sxs-lookup"><span data-stu-id="b60c4-125">Then call [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), as described in the topic [Media Event Generators](media-event-generators.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b60c4-126">Требования</span><span class="sxs-lookup"><span data-stu-id="b60c4-126">Requirements</span></span>



| <span data-ttu-id="b60c4-127">Требование</span><span class="sxs-lookup"><span data-stu-id="b60c4-127">Requirement</span></span> | <span data-ttu-id="b60c4-128">Значение</span><span class="sxs-lookup"><span data-stu-id="b60c4-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b60c4-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b60c4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b60c4-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b60c4-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b60c4-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b60c4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b60c4-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b60c4-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b60c4-133">Header</span><span class="sxs-lookup"><span data-stu-id="b60c4-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b60c4-134"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b60c4-134"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b60c4-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b60c4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b60c4-136">**имфконтентенаблер**</span><span class="sxs-lookup"><span data-stu-id="b60c4-136">**IMFContentEnabler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[<span data-ttu-id="b60c4-137">Генераторы событий мультимедиа</span><span class="sxs-lookup"><span data-stu-id="b60c4-137">Media Event Generators</span></span>](media-event-generators.md)
</dt> <dt>

[<span data-ttu-id="b60c4-138">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b60c4-138">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




