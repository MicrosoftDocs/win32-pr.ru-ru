---
description: Сигнализирует, что поток мультимедиа не имеет данных, доступных в указанное время.
ms.assetid: 1a00fff1-c3ab-4965-a663-3c15bb48ea98
title: Событие Местреамтикк (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27123569e991043a534883964ba94e4955d60a40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711213"
---
# <a name="mestreamtick-event"></a><span data-ttu-id="d0bb6-103">Событие Местреамтикк</span><span class="sxs-lookup"><span data-stu-id="d0bb6-103">MEStreamTick event</span></span>

<span data-ttu-id="d0bb6-104">Сигнализирует, что поток мультимедиа не имеет данных, доступных в указанное время.</span><span class="sxs-lookup"><span data-stu-id="d0bb6-104">Signals that a media stream does not have data available at a specified time.</span></span>

## <a name="event-values"></a><span data-ttu-id="d0bb6-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="d0bb6-105">Event values</span></span>

<span data-ttu-id="d0bb6-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="d0bb6-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="d0bb6-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="d0bb6-107">VARTYPE</span></span>           | <span data-ttu-id="d0bb6-108">Описание</span><span class="sxs-lookup"><span data-stu-id="d0bb6-108">Description</span></span>                                                                   |
|-------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="d0bb6-109">VT \_ i8</span><span class="sxs-lookup"><span data-stu-id="d0bb6-109">VT\_I8</span></span><br/> | <span data-ttu-id="d0bb6-110">Время, когда происходит разрыв, в 100-наносекундных единицах.</span><span class="sxs-lookup"><span data-stu-id="d0bb6-110">Time at which the gap occurs, in 100-nanosecond units.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="d0bb6-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d0bb6-111">Remarks</span></span>

<span data-ttu-id="d0bb6-112">Это событие сигнализирует о пропуске в данных.</span><span class="sxs-lookup"><span data-stu-id="d0bb6-112">This event signals a gap in the data.</span></span> <span data-ttu-id="d0bb6-113">Событие уведомляет подчиненные компоненты, чтобы не ждать каких бы то ни было данных в указанное время.</span><span class="sxs-lookup"><span data-stu-id="d0bb6-113">The event notifies downstream components not to expect any data at the specified time.</span></span>

<span data-ttu-id="d0bb6-114">Событие должно быть отправлено любым объектом, создающим отметки времени для образцов мультимедиа в потоке.</span><span class="sxs-lookup"><span data-stu-id="d0bb6-114">The event should be sent by whichever object generates the time stamps for the media samples in the stream.</span></span> <span data-ttu-id="d0bb6-115">В зависимости от формата данных это может быть:</span><span class="sxs-lookup"><span data-stu-id="d0bb6-115">Depending on the format of the data, this is either:</span></span>

-   <span data-ttu-id="d0bb6-116">Поток мультимедиа в источнике мультимедиа (интерфейс [**имфмедиастреам**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) ) или</span><span class="sxs-lookup"><span data-stu-id="d0bb6-116">The media stream on the media source ([**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) interface), or</span></span>
-   <span data-ttu-id="d0bb6-117">Преобразование декодера (интерфейс [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) ).</span><span class="sxs-lookup"><span data-stu-id="d0bb6-117">The decoder transform ([**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface).</span></span>

<span data-ttu-id="d0bb6-118">Во время пропуска объект должен отправить событие примерно так часто, как это обычно создает образцы.</span><span class="sxs-lookup"><span data-stu-id="d0bb6-118">During the gap, the object should send the event about as often as it would normally produce samples.</span></span> <span data-ttu-id="d0bb6-119">Для видео отправьте одно событие для каждого отсутствующего кадра.</span><span class="sxs-lookup"><span data-stu-id="d0bb6-119">For video, send one event for each missing frame.</span></span> <span data-ttu-id="d0bb6-120">Для звука Отправьте событие по крайней мере один раз в секунду во время разрыва.</span><span class="sxs-lookup"><span data-stu-id="d0bb6-120">For audio, send the event at least once per second during the gap.</span></span> <span data-ttu-id="d0bb6-121">Значение события — это метка времени отсутствующего примера.</span><span class="sxs-lookup"><span data-stu-id="d0bb6-121">The value of the event is the time stamp of the missing sample.</span></span> <span data-ttu-id="d0bb6-122">Отправьте столько событий Местреамтикк, сколько требуется для заполнения зазоров в данных.</span><span class="sxs-lookup"><span data-stu-id="d0bb6-122">Send as many MEStreamTick events as needed to fill the gap in the data.</span></span>

<span data-ttu-id="d0bb6-123">Если источник мультимедиа имеет несколько потоков и имеется разрыв в нескольких потоках, каждый поток должен отправить события Местреамтикк.</span><span class="sxs-lookup"><span data-stu-id="d0bb6-123">If a media source has several streams and there is a gap in more than one stream, each stream should send MEStreamTick events.</span></span> <span data-ttu-id="d0bb6-124">Например, если имеется разрыв в данных аудио и видео, то оба потока отправляют событие.</span><span class="sxs-lookup"><span data-stu-id="d0bb6-124">For example, if there is a gap in both audio and video data, then both streams send the event.</span></span>

<span data-ttu-id="d0bb6-125">Событие Местреамтикк не завершает запрос [**имфмедиастреам:: рекуестсампле**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .</span><span class="sxs-lookup"><span data-stu-id="d0bb6-125">The MEStreamTick event does not complete an [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) request.</span></span> <span data-ttu-id="d0bb6-126">Источник мультимедиа по-прежнему должен отправить событие [мемедиасампле](memediasample.md) для каждого вызова **рекуестсампле**.</span><span class="sxs-lookup"><span data-stu-id="d0bb6-126">The media source must still send an [MEMediaSample](memediasample.md) event for each call to **RequestSample**.</span></span>

<span data-ttu-id="d0bb6-127">Приемники мультимедиа не могут напрямую использовать это событие.</span><span class="sxs-lookup"><span data-stu-id="d0bb6-127">Media sinks cannot consume this event directly.</span></span> <span data-ttu-id="d0bb6-128">Чтобы сообщить о пропуске потока в приемник мультимедиа, вызовите [**имфстреамсинк::P лацемаркер**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) с маркером **\_ \_ деления маркера мфстреамсинк** .</span><span class="sxs-lookup"><span data-stu-id="d0bb6-128">To signal a gap in the stream to a media sink, call [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) with an **MFSTREAMSINK\_MARKER\_TICK** marker.</span></span> <span data-ttu-id="d0bb6-129">Конвейер Media Foundation преобразует события Местреамтикк в маркеры **\_ \_ деления мфстреамсинк** , когда это необходимо.</span><span class="sxs-lookup"><span data-stu-id="d0bb6-129">The Media Foundation pipeline converts MEStreamTick events to **MFSTREAMSINK\_MARKER\_TICK** markers when needed.</span></span>

<span data-ttu-id="d0bb6-130">Не устанавливайте атрибут [**\_ прекращения мфсампликстенсион**](mfsampleextension-discontinuity-attribute.md) для следующего примера носителя после события местреамтикк.</span><span class="sxs-lookup"><span data-stu-id="d0bb6-130">Do not set the [**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute on the next media sample after an MEStreamTick event.</span></span> <span data-ttu-id="d0bb6-131">Атрибут **\_ прекращения мфсампликстенсион** подразумевает, что отметка времени не является непрерывной с предыдущими штампами времени, тогда как местреамтикк предполагает, что отметки времени являются непрерывными, но некоторые данные отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="d0bb6-131">The **MFSampleExtension\_Discontinuity** attribute implies that the time stamp is discontinuous with previous time stamps, whereas MEStreamTick implies that time stamps are continuous but some data is missing.</span></span>

> [!Note]  
> <span data-ttu-id="d0bb6-132">Более ранняя версия документации неправильно объявила, что пример после события Местреамтикк должен иметь атрибут [**мфсампликстенсион \_**](mfsampleextension-discontinuity-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="d0bb6-132">An earlier version of the documentation incorrectly stated that the sample after an MEStreamTick event should have the [**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d0bb6-133">Требования</span><span class="sxs-lookup"><span data-stu-id="d0bb6-133">Requirements</span></span>



| <span data-ttu-id="d0bb6-134">Требование</span><span class="sxs-lookup"><span data-stu-id="d0bb6-134">Requirement</span></span> | <span data-ttu-id="d0bb6-135">Значение</span><span class="sxs-lookup"><span data-stu-id="d0bb6-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0bb6-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d0bb6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d0bb6-137">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d0bb6-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d0bb6-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d0bb6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d0bb6-139">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d0bb6-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d0bb6-140">Header</span><span class="sxs-lookup"><span data-stu-id="d0bb6-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0bb6-141"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0bb6-141"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0bb6-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d0bb6-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0bb6-143">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d0bb6-143">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




