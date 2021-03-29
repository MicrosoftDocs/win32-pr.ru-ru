---
description: Вызывается сеансом мультимедиа при запуске новой презентации. Это событие указывает, когда начнется презентация, и смещение между временем презентации и исходным временем.
ms.assetid: 67c7d5f3-ffaf-4359-a59c-bb26b992b6cd
title: Событие Месессионнотифипресентатионтиме (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7b0cd8811d98094ab58ddcf844ec73e1470d120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647243"
---
# <a name="mesessionnotifypresentationtime-event"></a><span data-ttu-id="d8912-104">Событие Месессионнотифипресентатионтиме</span><span class="sxs-lookup"><span data-stu-id="d8912-104">MESessionNotifyPresentationTime event</span></span>

<span data-ttu-id="d8912-105">Вызывается сеансом мультимедиа при запуске новой презентации.</span><span class="sxs-lookup"><span data-stu-id="d8912-105">Raised by the Media Session when a new presentation starts.</span></span> <span data-ttu-id="d8912-106">Это событие указывает, когда начнется презентация, и смещение между временем презентации и исходным временем.</span><span class="sxs-lookup"><span data-stu-id="d8912-106">This event indicates when the presentation will start and the offset between the presentation time and the source time.</span></span>

## <a name="event-values"></a><span data-ttu-id="d8912-107">Значения событий</span><span class="sxs-lookup"><span data-stu-id="d8912-107">Event values</span></span>

<span data-ttu-id="d8912-108">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="d8912-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="d8912-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="d8912-109">VARTYPE</span></span>              | <span data-ttu-id="d8912-110">Описание</span><span class="sxs-lookup"><span data-stu-id="d8912-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="d8912-111">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="d8912-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="d8912-112">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="d8912-112">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="d8912-113">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d8912-113">Attributes</span></span>

<span data-ttu-id="d8912-114">Для этого события определены следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="d8912-114">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="d8912-115">attribute</span><span class="sxs-lookup"><span data-stu-id="d8912-115">Attribute</span></span>                                                                                                                   | <span data-ttu-id="d8912-116">Описание</span><span class="sxs-lookup"><span data-stu-id="d8912-116">Description</span></span>                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d8912-117">**\_ \_ \_ время начала презентации \_ для события MF**</span><span class="sxs-lookup"><span data-stu-id="d8912-117">**MF\_EVENT\_START\_PRESENTATION\_TIME**</span></span>](mf-event-start-presentation-time-attribute.md)<br/>                       | <span data-ttu-id="d8912-118">Время начала презентации.</span><span class="sxs-lookup"><span data-stu-id="d8912-118">Starting time for the presentation.</span></span><br/> <br/>                                                      |
| [<span data-ttu-id="d8912-119">**\_ \_ \_ смещение времени презентации событий \_ MF**</span><span class="sxs-lookup"><span data-stu-id="d8912-119">**MF\_EVENT\_PRESENTATION\_TIME\_OFFSET**</span></span>](mf-event-presentation-time-offset-attribute.md)<br/>                     | <span data-ttu-id="d8912-120">Смещение между временем презентации и штампами времени источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d8912-120">Offset between the presentation time and the media source's time stamps.</span></span><br/> <br/>                 |
| [<span data-ttu-id="d8912-121">**\_событие MF \_ Запуск \_ \_ во время презентации \_ на \_ выходе**</span><span class="sxs-lookup"><span data-stu-id="d8912-121">**MF\_EVENT\_START\_PRESENTATION\_TIME\_AT\_OUTPUT**</span></span>](mf-event-start-presentation-time-at-output-attribute.md)<br/> | <span data-ttu-id="d8912-122">Время презентации, когда приемники мультимедиа отображают первый образец новой топологии.</span><span class="sxs-lookup"><span data-stu-id="d8912-122">Presentation time when the media sinks will render the first sample of the new topology.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="d8912-123">Требования</span><span class="sxs-lookup"><span data-stu-id="d8912-123">Requirements</span></span>



| <span data-ttu-id="d8912-124">Требование</span><span class="sxs-lookup"><span data-stu-id="d8912-124">Requirement</span></span> | <span data-ttu-id="d8912-125">Значение</span><span class="sxs-lookup"><span data-stu-id="d8912-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8912-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d8912-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d8912-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d8912-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d8912-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d8912-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d8912-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d8912-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d8912-130">Header</span><span class="sxs-lookup"><span data-stu-id="d8912-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8912-131"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d8912-131"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8912-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d8912-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8912-133">**имфмедиасессион**</span><span class="sxs-lookup"><span data-stu-id="d8912-133">**IMFMediaSession**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
</dt> <dt>

[<span data-ttu-id="d8912-134">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d8912-134">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




