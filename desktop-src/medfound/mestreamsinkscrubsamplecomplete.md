---
description: Вызывается приемником потока при завершении запроса на очистку.
ms.assetid: 451c7e09-868e-4c05-b970-d222b97223f2
title: Событие Местреамсинкскрубсамплекомплете (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81f29d478635d5a9ba7e7c5356c49ebd8da216f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674283"
---
# <a name="mestreamsinkscrubsamplecomplete-event"></a><span data-ttu-id="09229-103">Событие Местреамсинкскрубсамплекомплете</span><span class="sxs-lookup"><span data-stu-id="09229-103">MEStreamSinkScrubSampleComplete event</span></span>

<span data-ttu-id="09229-104">Вызывается приемником потока при завершении запроса на очистку.</span><span class="sxs-lookup"><span data-stu-id="09229-104">Raised by a stream sink when it completes a scrubbing request.</span></span>

<span data-ttu-id="09229-105">Очистка происходит, когда скорость воспроизведения равна нулю и часы презентации запускаются с указанным сруббинг временем.</span><span class="sxs-lookup"><span data-stu-id="09229-105">Scrubbing occurs when the playback rate is zero and the presentation clock is started with a specified srubbing time.</span></span> <span data-ttu-id="09229-106">Если приемник мультимедиа поддерживает очистку, каждый поток в приемнике вызывает это событие при вызове метода [**имфклоккстатесинк:: онклоккстарт**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) , когда скорость воспроизведения равна нулю.</span><span class="sxs-lookup"><span data-stu-id="09229-106">If a media sink supports scrubbing, every stream on the sink raises this event whenever the [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) method is called while the playback rate is zero.</span></span>

<span data-ttu-id="09229-107">Если поток визуализирует данные при очистке, он отправляет событие сразу после подготовки данных.</span><span class="sxs-lookup"><span data-stu-id="09229-107">If the stream renders data while scrubbing, it sends the event as soon as the data is rendered.</span></span> <span data-ttu-id="09229-108">Если поток не отображает данные, он отправляет событие сразу после вызова [**онклоккстарт**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) .</span><span class="sxs-lookup"><span data-stu-id="09229-108">If the stream does not render data, it sends the event immediately after [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) is called.</span></span>

## <a name="event-values"></a><span data-ttu-id="09229-109">Значения событий</span><span class="sxs-lookup"><span data-stu-id="09229-109">Event values</span></span>

<span data-ttu-id="09229-110">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="09229-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="09229-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="09229-111">VARTYPE</span></span>              | <span data-ttu-id="09229-112">Описание</span><span class="sxs-lookup"><span data-stu-id="09229-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="09229-113">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="09229-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="09229-114">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="09229-114">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="09229-115">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="09229-115">Attributes</span></span>

<span data-ttu-id="09229-116">Для этого события определены следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="09229-116">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="09229-117">attribute</span><span class="sxs-lookup"><span data-stu-id="09229-117">Attribute</span></span>                                                                              | <span data-ttu-id="09229-118">Описание</span><span class="sxs-lookup"><span data-stu-id="09229-118">Description</span></span>                                                                                                                                                   |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="09229-119">**\_ \_ время СКРУБСАМПЛЕ события \_ MF**</span><span class="sxs-lookup"><span data-stu-id="09229-119">**MF\_EVENT\_SCRUBSAMPLE\_TIME**</span></span>](mf-event-scrubsample-time-attribute.md)<br/> | <span data-ttu-id="09229-120">Время презентации, для которой были подготовлены данные.</span><span class="sxs-lookup"><span data-stu-id="09229-120">Presentation time for which data was rendered.</span></span> <span data-ttu-id="09229-121">Если приемник мультимедиа не отображает данные при очистке, он не устанавливает этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="09229-121">If the media sink does not render data while scrubbing, it does not set this attribute.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="09229-122">Требования</span><span class="sxs-lookup"><span data-stu-id="09229-122">Requirements</span></span>



| <span data-ttu-id="09229-123">Требование</span><span class="sxs-lookup"><span data-stu-id="09229-123">Requirement</span></span> | <span data-ttu-id="09229-124">Значение</span><span class="sxs-lookup"><span data-stu-id="09229-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09229-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="09229-125">Minimum supported client</span></span><br/> | <span data-ttu-id="09229-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="09229-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="09229-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="09229-127">Minimum supported server</span></span><br/> | <span data-ttu-id="09229-128">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="09229-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="09229-129">Header</span><span class="sxs-lookup"><span data-stu-id="09229-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="09229-130"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="09229-130"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09229-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="09229-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09229-132">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="09229-132">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="09229-133">Приемники носителей</span><span class="sxs-lookup"><span data-stu-id="09229-133">Media Sinks</span></span>](media-sinks.md)
</dt> <dt>

[<span data-ttu-id="09229-134">месессионскрубсамплекомплете</span><span class="sxs-lookup"><span data-stu-id="09229-134">MESessionScrubSampleComplete</span></span>](mesessionscrubsamplecomplete.md)
</dt> </dl>

 

 




