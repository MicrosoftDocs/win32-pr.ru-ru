---
description: Возникает, когда источник мультимедиа запускается без поиска.
ms.assetid: a52d8ee1-cb46-487d-a744-fca6db7c2353
title: Событие Месаурцестартед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c17ba7898a8bf33df4a3508afee9b7c0c9bc81c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544375"
---
# <a name="mesourcestarted-event"></a><span data-ttu-id="df8d9-103">Событие Месаурцестартед</span><span class="sxs-lookup"><span data-stu-id="df8d9-103">MESourceStarted event</span></span>

<span data-ttu-id="df8d9-104">Возникает, когда источник мультимедиа запускается без поиска.</span><span class="sxs-lookup"><span data-stu-id="df8d9-104">Raised when a media source starts without seeking.</span></span>

## <a name="event-values"></a><span data-ttu-id="df8d9-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="df8d9-105">Event values</span></span>

<span data-ttu-id="df8d9-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="df8d9-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="df8d9-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="df8d9-107">VARTYPE</span></span>              | <span data-ttu-id="df8d9-108">Описание</span><span class="sxs-lookup"><span data-stu-id="df8d9-108">Description</span></span>                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df8d9-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="df8d9-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="df8d9-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="df8d9-110">No event data.</span></span> <span data-ttu-id="df8d9-111">Время начала было от текущей должности.</span><span class="sxs-lookup"><span data-stu-id="df8d9-111">The start time was from the current position.</span></span><br/> <br/>                            |
| <span data-ttu-id="df8d9-112">VT \_ i8</span><span class="sxs-lookup"><span data-stu-id="df8d9-112">VT\_I8</span></span><br/>    | <span data-ttu-id="df8d9-113">Время начала (в 100-наносекундных единицах) относительно меток времени в примерах.</span><span class="sxs-lookup"><span data-stu-id="df8d9-113">The starting time, in 100-nanosecond units, relative to the time stamps on the samples.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="df8d9-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="df8d9-114">Attributes</span></span>

<span data-ttu-id="df8d9-115">Для этого события определены следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="df8d9-115">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="df8d9-116">attribute</span><span class="sxs-lookup"><span data-stu-id="df8d9-116">Attribute</span></span>                                                                                     | <span data-ttu-id="df8d9-117">Описание</span><span class="sxs-lookup"><span data-stu-id="df8d9-117">Description</span></span>                                                                                                                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="df8d9-118">**\_ \_ \_ Фактическое начало источника события MF \_**</span><span class="sxs-lookup"><span data-stu-id="df8d9-118">**MF\_EVENT\_SOURCE\_ACTUAL\_START**</span></span>](mf-event-source-actual-start-attribute.md)<br/> | <span data-ttu-id="df8d9-119">Время начала.</span><span class="sxs-lookup"><span data-stu-id="df8d9-119">Start time.</span></span> <span data-ttu-id="df8d9-120">Источник мультимедиа задает этот атрибут, если он перезапускается с текущей позицией.</span><span class="sxs-lookup"><span data-stu-id="df8d9-120">The media source sets this attribute if it restarts from its current position.</span></span><br/> <br/>                     |
| [<span data-ttu-id="df8d9-121">**\_ \_ \_ поддельный \_ Запуск источника события MF**</span><span class="sxs-lookup"><span data-stu-id="df8d9-121">**MF\_EVENT\_SOURCE\_FAKE\_START**</span></span>](mf-event-source-fake-start-attribute.md)<br/>     | <span data-ttu-id="df8d9-122">Указывает, пуста ли текущая топология сегмента.</span><span class="sxs-lookup"><span data-stu-id="df8d9-122">Specifies whether the current segment topology is empty.</span></span> <span data-ttu-id="df8d9-123">Источник Sequencer задает этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="df8d9-123">The sequencer source sets this attribute.</span></span><br/> <br/>             |
| [<span data-ttu-id="df8d9-124">**\_ \_ прожектстарт источник события \_ MF**</span><span class="sxs-lookup"><span data-stu-id="df8d9-124">**MF\_EVENT\_SOURCE\_PROJECTSTART**</span></span>](mf-event-source-projectstart-attribute.md)<br/>  | <span data-ttu-id="df8d9-125">Время начала для сегмента относительно начала презентации.</span><span class="sxs-lookup"><span data-stu-id="df8d9-125">Start time for a segment, relative to the start of the presentation.</span></span> <span data-ttu-id="df8d9-126">Источник Sequencer задает этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="df8d9-126">The sequencer source sets this attribute.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="df8d9-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="df8d9-127">Remarks</span></span>

<span data-ttu-id="df8d9-128">Источник мультимедиа вызывает это событие при запуске из остановленного состояния или начинает с приостановленного состояния в той же позиции в источнике.</span><span class="sxs-lookup"><span data-stu-id="df8d9-128">A media source raises this event when it starts from a stopped state, or starts from a paused state at the same position in the source.</span></span> <span data-ttu-id="df8d9-129">Событие возникает, если метод [**имфмедиасаурце:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="df8d9-129">The event is raised if the [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method returns S\_OK.</span></span>

<span data-ttu-id="df8d9-130">Если источник мультимедиа начинается с текущей позицией, а предыдущее состояние источника было запущено или приостановлено, данные события могут быть пустыми (VT \_ Empty).</span><span class="sxs-lookup"><span data-stu-id="df8d9-130">If the media source starts from the current position and the source's previous state was running or paused, the event data can empty (VT\_EMPTY).</span></span> <span data-ttu-id="df8d9-131">Если данные события имеют значение VT \_ Empty, источник мультимедиа может установить атрибут « [**\_ Источник события MF» \_ \_ фактического \_**](mf-event-source-actual-start-attribute.md) времени начала.</span><span class="sxs-lookup"><span data-stu-id="df8d9-131">If the event data is VT\_EMPTY, the media source might set the [**MF\_EVENT\_SOURCE\_ACTUAL\_START**](mf-event-source-actual-start-attribute.md) attribute with the actual starting time.</span></span>

<span data-ttu-id="df8d9-132">Если источник мультимедиа начинается с новой положения или остановлено предыдущее состояние источника, то данные события должны быть временем начала (VT \_ I8).</span><span class="sxs-lookup"><span data-stu-id="df8d9-132">If the media source starts from a new position, or the source's previous state was stopped, the event data must be the starting time (VT\_I8).</span></span>

<span data-ttu-id="df8d9-133">Если метод [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) вызывает Поиск, источник мультимедиа отправляет событие [месаурцесикед](mesourceseeked.md) вместо месаурцестартед.</span><span class="sxs-lookup"><span data-stu-id="df8d9-133">If the [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method causes a seek, the media source sends the [MESourceSeeked](mesourceseeked.md) event instead of MESourceStarted.</span></span>

## <a name="requirements"></a><span data-ttu-id="df8d9-134">Требования</span><span class="sxs-lookup"><span data-stu-id="df8d9-134">Requirements</span></span>



| <span data-ttu-id="df8d9-135">Требование</span><span class="sxs-lookup"><span data-stu-id="df8d9-135">Requirement</span></span> | <span data-ttu-id="df8d9-136">Значение</span><span class="sxs-lookup"><span data-stu-id="df8d9-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df8d9-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="df8d9-137">Minimum supported client</span></span><br/> | <span data-ttu-id="df8d9-138">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="df8d9-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="df8d9-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="df8d9-139">Minimum supported server</span></span><br/> | <span data-ttu-id="df8d9-140">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="df8d9-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="df8d9-141">Header</span><span class="sxs-lookup"><span data-stu-id="df8d9-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="df8d9-142"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="df8d9-142"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df8d9-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="df8d9-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df8d9-144">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="df8d9-144">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




