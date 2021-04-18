---
description: События источника мультимедиа
ms.assetid: c7b6ea86-e919-45b8-a1f9-bd18c3aed163
title: События источника мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72c40755a32f610b33ef3a5c66d3acb448223813
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105713299"
---
# <a name="media-source-events"></a><span data-ttu-id="b0224-103">События источника мультимедиа</span><span class="sxs-lookup"><span data-stu-id="b0224-103">Media Source Events</span></span>

<span data-ttu-id="b0224-104">В этом разделе перечислены события, отправляемые источниками мультимедиа и потоками мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b0224-104">This topic lists the events that are sent by media sources and media streams.</span></span> <span data-ttu-id="b0224-105">Источники мультимедиа также могут отсылать пользовательские события, не указанные здесь.</span><span class="sxs-lookup"><span data-stu-id="b0224-105">Media sources can also send custom events not listed here.</span></span>

## <a name="media-source-events"></a><span data-ttu-id="b0224-106">События источника мультимедиа</span><span class="sxs-lookup"><span data-stu-id="b0224-106">Media Source Events</span></span>



| <span data-ttu-id="b0224-107">Событие</span><span class="sxs-lookup"><span data-stu-id="b0224-107">Event</span></span>                                                                      | <span data-ttu-id="b0224-108">Описание</span><span class="sxs-lookup"><span data-stu-id="b0224-108">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b0224-109">Событие Миндофпресентатион</span><span class="sxs-lookup"><span data-stu-id="b0224-109">MEEndOfPresentation Event</span></span>](meendofpresentation.md)                       | <span data-ttu-id="b0224-110">Презентация завершена.</span><span class="sxs-lookup"><span data-stu-id="b0224-110">The presentation ended.</span></span> <span data-ttu-id="b0224-111">Все потоки в презентации достигли конца потока.</span><span class="sxs-lookup"><span data-stu-id="b0224-111">All streams in the presentation have reached the end of the stream.</span></span>      |
| [<span data-ttu-id="b0224-112">Событие Меневстреам</span><span class="sxs-lookup"><span data-stu-id="b0224-112">MENewStream Event</span></span>](menewstream.md)                                       | <span data-ttu-id="b0224-113">Создан новый поток.</span><span class="sxs-lookup"><span data-stu-id="b0224-113">A new stream was created.</span></span> <span data-ttu-id="b0224-114">Событие содержит указатель на поток.</span><span class="sxs-lookup"><span data-stu-id="b0224-114">The event contains a pointer to the stream.</span></span>                            |
| [<span data-ttu-id="b0224-115">Событие Месаурцечарактеристиксчанжед</span><span class="sxs-lookup"><span data-stu-id="b0224-115">MESourceCharacteristicsChanged Event</span></span>](mesourcecharacteristicschanged.md) | <span data-ttu-id="b0224-116">Изменились характеристики источника.</span><span class="sxs-lookup"><span data-stu-id="b0224-116">The characteristics of the source have changed.</span></span> <span data-ttu-id="b0224-117">(Необязательно.)</span><span class="sxs-lookup"><span data-stu-id="b0224-117">(Optional.)</span></span>                                      |
| [<span data-ttu-id="b0224-118">Событие Месаурцеметадатачанжед</span><span class="sxs-lookup"><span data-stu-id="b0224-118">MESourceMetadataChanged Event</span></span>](mesourcemetadatachanged.md)               | <span data-ttu-id="b0224-119">Метаданные источника изменились.</span><span class="sxs-lookup"><span data-stu-id="b0224-119">The source's metadata has changed.</span></span> <span data-ttu-id="b0224-120">(Необязательно.)</span><span class="sxs-lookup"><span data-stu-id="b0224-120">(Optional.)</span></span>                                                   |
| [<span data-ttu-id="b0224-121">Событие Месаурцепаусед</span><span class="sxs-lookup"><span data-stu-id="b0224-121">MESourcePaused Event</span></span>](mesourcepaused.md)                                 | <span data-ttu-id="b0224-122">Источник приостановлен.</span><span class="sxs-lookup"><span data-stu-id="b0224-122">The source was paused.</span></span> <span data-ttu-id="b0224-123">Не все источники поддерживают приостановку.</span><span class="sxs-lookup"><span data-stu-id="b0224-123">Not all sources support pausing.</span></span>                                          |
| [<span data-ttu-id="b0224-124">Событие Месаурцератечанжед</span><span class="sxs-lookup"><span data-stu-id="b0224-124">MESourceRateChanged Event</span></span>](mesourceratechanged.md)                       | <span data-ttu-id="b0224-125">Частота воспроизведения источника изменилась.</span><span class="sxs-lookup"><span data-stu-id="b0224-125">The source's playback rate has changed.</span></span> <span data-ttu-id="b0224-126">(Необязательно; применяется, если источник поддерживает управление скоростью.)</span><span class="sxs-lookup"><span data-stu-id="b0224-126">(Optional; applies if the source supports rate control.)</span></span> |
| [<span data-ttu-id="b0224-127">Событие Месаурцератечанжерекуестед</span><span class="sxs-lookup"><span data-stu-id="b0224-127">MESourceRateChangeRequested Event</span></span>](mesourceratechangerequested.md)       | <span data-ttu-id="b0224-128">Источник запрашивает новый темп воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="b0224-128">The source is requesting a new playback rate.</span></span> <span data-ttu-id="b0224-129">(Необязательно.)</span><span class="sxs-lookup"><span data-stu-id="b0224-129">(Optional.)</span></span>                                        |
| [<span data-ttu-id="b0224-130">Событие Месаурцесикед</span><span class="sxs-lookup"><span data-stu-id="b0224-130">MESourceSeeked Event</span></span>](mesourceseeked.md)                                 | <span data-ttu-id="b0224-131">Был выполнен поиск в источнике.</span><span class="sxs-lookup"><span data-stu-id="b0224-131">The source was seeked.</span></span> <span data-ttu-id="b0224-132">Не все источники поддерживают поиск.</span><span class="sxs-lookup"><span data-stu-id="b0224-132">Not all sources support seeking.</span></span>                                          |
| [<span data-ttu-id="b0224-133">Событие Месаурцестартед</span><span class="sxs-lookup"><span data-stu-id="b0224-133">MESourceStarted Event</span></span>](mesourcestarted.md)                               | <span data-ttu-id="b0224-134">Источник запущен.</span><span class="sxs-lookup"><span data-stu-id="b0224-134">The source was started.</span></span>                                                                          |
| [<span data-ttu-id="b0224-135">Событие Месаурцестоппед</span><span class="sxs-lookup"><span data-stu-id="b0224-135">MESourceStopped Event</span></span>](mesourcestopped.md)                               | <span data-ttu-id="b0224-136">Источник остановлен.</span><span class="sxs-lookup"><span data-stu-id="b0224-136">The source was stopped.</span></span>                                                                          |
| [<span data-ttu-id="b0224-137">Событие Меупдатедстреам</span><span class="sxs-lookup"><span data-stu-id="b0224-137">MEUpdatedStream Event</span></span>](meupdatedstream.md)                               | <span data-ttu-id="b0224-138">Был выполнен поиск или повторный запуск существующего потока.</span><span class="sxs-lookup"><span data-stu-id="b0224-138">An existing stream was seeked or re-started.</span></span> <span data-ttu-id="b0224-139">Событие содержит указатель на поток.</span><span class="sxs-lookup"><span data-stu-id="b0224-139">The event contains a pointer to the stream.</span></span>         |



 

## <a name="media-stream-events"></a><span data-ttu-id="b0224-140">События потока мультимедиа</span><span class="sxs-lookup"><span data-stu-id="b0224-140">Media Stream Events</span></span>



| <span data-ttu-id="b0224-141">Событие</span><span class="sxs-lookup"><span data-stu-id="b0224-141">Event</span></span>                                                    | <span data-ttu-id="b0224-142">Описание</span><span class="sxs-lookup"><span data-stu-id="b0224-142">Description</span></span>                                                                                                                    |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b0224-143">Событие Миндофстреам</span><span class="sxs-lookup"><span data-stu-id="b0224-143">MEEndOfStream Event</span></span>](meendofstream.md)                 | <span data-ttu-id="b0224-144">Поток завершен.</span><span class="sxs-lookup"><span data-stu-id="b0224-144">The stream ended.</span></span>                                                                                                              |
| [<span data-ttu-id="b0224-145">Событие Миррор</span><span class="sxs-lookup"><span data-stu-id="b0224-145">MEError Event</span></span>](meerror.md)                             | <span data-ttu-id="b0224-146">Во время потоковой передачи произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="b0224-146">An error has occurred during streaming.</span></span> <span data-ttu-id="b0224-147">Используйте это событие для ошибок, не связанных с другими событиями, перечисленными здесь.</span><span class="sxs-lookup"><span data-stu-id="b0224-147">Use this event for errors that are not related to any of the other events listed here.</span></span> |
| [<span data-ttu-id="b0224-148">Событие Мемедиасампле</span><span class="sxs-lookup"><span data-stu-id="b0224-148">MEMediaSample Event</span></span>](memediasample.md)                 | <span data-ttu-id="b0224-149">Поток создал новый пример.</span><span class="sxs-lookup"><span data-stu-id="b0224-149">The stream has generated a new sample.</span></span>                                                                                         |
| [<span data-ttu-id="b0224-150">Событие Местреамформатчанжед</span><span class="sxs-lookup"><span data-stu-id="b0224-150">MEStreamFormatChanged Event</span></span>](mestreamformatchanged.md) | <span data-ttu-id="b0224-151">Тип носителя изменился.</span><span class="sxs-lookup"><span data-stu-id="b0224-151">The media type has changed.</span></span> <span data-ttu-id="b0224-152">(Необязательно.)</span><span class="sxs-lookup"><span data-stu-id="b0224-152">(Optional.)</span></span>                                                                                        |
| [<span data-ttu-id="b0224-153">Событие Местреампаусед</span><span class="sxs-lookup"><span data-stu-id="b0224-153">MEStreamPaused Event</span></span>](mestreampaused.md)               | <span data-ttu-id="b0224-154">Поток был приостановлен.</span><span class="sxs-lookup"><span data-stu-id="b0224-154">The stream was paused.</span></span>                                                                                                         |
| [<span data-ttu-id="b0224-155">Событие Местреамсикед</span><span class="sxs-lookup"><span data-stu-id="b0224-155">MEStreamSeeked Event</span></span>](mestreamseeked.md)               | <span data-ttu-id="b0224-156">Поиск в потоке выполнен.</span><span class="sxs-lookup"><span data-stu-id="b0224-156">The stream was seeked.</span></span>                                                                                                         |
| [<span data-ttu-id="b0224-157">Событие Местреамстартед</span><span class="sxs-lookup"><span data-stu-id="b0224-157">MEStreamStarted Event</span></span>](mestreamstarted.md)             | <span data-ttu-id="b0224-158">Поток запущен.</span><span class="sxs-lookup"><span data-stu-id="b0224-158">The stream was started.</span></span>                                                                                                        |
| [<span data-ttu-id="b0224-159">Событие Местреамстоппед</span><span class="sxs-lookup"><span data-stu-id="b0224-159">MEStreamStopped Event</span></span>](mestreamstopped.md)             | <span data-ttu-id="b0224-160">Поток остановлен.</span><span class="sxs-lookup"><span data-stu-id="b0224-160">The stream was stopped.</span></span>                                                                                                        |
| [<span data-ttu-id="b0224-161">Событие Местреамсинмоде</span><span class="sxs-lookup"><span data-stu-id="b0224-161">MEStreamThinMode Event</span></span>](mestreamthinmode.md)           | <span data-ttu-id="b0224-162">Режим тонкого режима запущен или остановлен.</span><span class="sxs-lookup"><span data-stu-id="b0224-162">Thinning mode has started or stopped.</span></span> <span data-ttu-id="b0224-163">(Необязательно.)</span><span class="sxs-lookup"><span data-stu-id="b0224-163">(Optional.)</span></span>                                                                              |
| [<span data-ttu-id="b0224-164">Событие Местреамтикк</span><span class="sxs-lookup"><span data-stu-id="b0224-164">MEStreamTick Event</span></span>](mestreamtick.md)                   | <span data-ttu-id="b0224-165">В потоке присутствует разрыв.</span><span class="sxs-lookup"><span data-stu-id="b0224-165">There is a gap in the stream.</span></span> <span data-ttu-id="b0224-166">(Необязательно.)</span><span class="sxs-lookup"><span data-stu-id="b0224-166">(Optional.)</span></span>                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="b0224-167">См. также</span><span class="sxs-lookup"><span data-stu-id="b0224-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0224-168">Источники мультимедиа</span><span class="sxs-lookup"><span data-stu-id="b0224-168">Media Sources</span></span>](media-sources.md)
</dt> </dl>

 

 



