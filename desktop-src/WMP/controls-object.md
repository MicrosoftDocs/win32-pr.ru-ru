---
title: Объект Controls
description: Объект Controls предоставляет способ управления воспроизведением мультимедиа с помощью следующих свойств и методов.
ms.assetid: bcc1e768-4fa6-4c82-a12f-52c9bfb4c10c
keywords:
- Управляет проигрывателем объектов Windows Media Player
topic_type:
- apiref
api_name:
- Controls Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7bac91c522c95c1b45565ca013a000022c73bcc4
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "103784485"
---
# <a name="controls-object"></a><span data-ttu-id="e3b91-104">Объект Controls</span><span class="sxs-lookup"><span data-stu-id="e3b91-104">Controls Object</span></span>

<span data-ttu-id="e3b91-105">Объект **Controls** предоставляет способ управления воспроизведением мультимедиа с помощью следующих свойств и методов.</span><span class="sxs-lookup"><span data-stu-id="e3b91-105">The **Controls** object provides a way to manipulate the playback of media using the following properties and methods.</span></span>

<span data-ttu-id="e3b91-106">Объект **Controls** поддерживает следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e3b91-106">The **Controls** object supports the following properties.</span></span>



| <span data-ttu-id="e3b91-107">Свойство</span><span class="sxs-lookup"><span data-stu-id="e3b91-107">Property</span></span>                                                            | <span data-ttu-id="e3b91-108">Описание</span><span class="sxs-lookup"><span data-stu-id="e3b91-108">Description</span></span>                                                                                                                                       |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e3b91-109">аудиолангуажекаунт</span><span class="sxs-lookup"><span data-stu-id="e3b91-109">audioLanguageCount</span></span>](controls-audiolanguagecount.md)               | <span data-ttu-id="e3b91-110">Извлекает количество поддерживаемых аудио языков.</span><span class="sxs-lookup"><span data-stu-id="e3b91-110">Retrieves the number of supported audio languages.</span></span>                                                                                                |
| [<span data-ttu-id="e3b91-111">куррентаудиолангуаже</span><span class="sxs-lookup"><span data-stu-id="e3b91-111">currentAudioLanguage</span></span>](controls-currentaudiolanguage.md)           | <span data-ttu-id="e3b91-112">Указывает или получает код локали (LCID) звукового языка для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="e3b91-112">Specifies or retrieves the locale identifier (LCID) of the audio language for playback</span></span>                                                            |
| [<span data-ttu-id="e3b91-113">куррентаудиолангуажеиндекс</span><span class="sxs-lookup"><span data-stu-id="e3b91-113">currentAudioLanguageIndex</span></span>](controls-currentaudiolanguageindex.md) | <span data-ttu-id="e3b91-114">Указывает или получает Отсчитываемый от единицы индекс, соответствующий звуковому языку для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="e3b91-114">Specifies or retrieves the one-based index that corresponds to the audio language for playback.</span></span>                                                   |
| [<span data-ttu-id="e3b91-115">currentItem</span><span class="sxs-lookup"><span data-stu-id="e3b91-115">currentItem</span></span>](controls-currentitem.md)                             | <span data-ttu-id="e3b91-116">Указывает или получает текущий элемент мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="e3b91-116">Specifies or retrieves the current media item.</span></span>                                                                                                    |
| [<span data-ttu-id="e3b91-117">куррентмаркер</span><span class="sxs-lookup"><span data-stu-id="e3b91-117">currentMarker</span></span>](controls-currentmarker.md)                         | <span data-ttu-id="e3b91-118">Указывает или получает номер текущего маркера.</span><span class="sxs-lookup"><span data-stu-id="e3b91-118">Specifies or retrieves the current marker number.</span></span>                                                                                                 |
| [<span data-ttu-id="e3b91-119">currentPosition</span><span class="sxs-lookup"><span data-stu-id="e3b91-119">currentPosition</span></span>](controls-currentposition.md)                     | <span data-ttu-id="e3b91-120">Указывает или получает текущую позицию в элементе мультимедиа за считаные секунды с начала.</span><span class="sxs-lookup"><span data-stu-id="e3b91-120">Specifies or retrieves the current position in the media item in seconds from the beginning.</span></span>                                                      |
| [<span data-ttu-id="e3b91-121">куррентпоситионстринг</span><span class="sxs-lookup"><span data-stu-id="e3b91-121">currentPositionString</span></span>](controls-currentpositionstring.md)         | <span data-ttu-id="e3b91-122">Извлекает текущую позицию в элементе мультимедиа в виде **строки**.</span><span class="sxs-lookup"><span data-stu-id="e3b91-122">Retrieves the current position in the media item as a **String**.</span></span>                                                                                 |
| [<span data-ttu-id="e3b91-123">куррентпоситионтимекоде</span><span class="sxs-lookup"><span data-stu-id="e3b91-123">currentPositionTimecode</span></span>](controls-currentpositiontimecode.md)     | <span data-ttu-id="e3b91-124">Указывает или получает текущую позицию в текущем элементе мультимедиа, используя формат кода времени.</span><span class="sxs-lookup"><span data-stu-id="e3b91-124">Specifies or retrieves the current position in the current media item using a time code format.</span></span> <span data-ttu-id="e3b91-125">Сейчас это свойство поддерживает код времени SMPTE.</span><span class="sxs-lookup"><span data-stu-id="e3b91-125">This property currently supports SMPTE time code.</span></span> |
| [<span data-ttu-id="e3b91-126">isAvailable</span><span class="sxs-lookup"><span data-stu-id="e3b91-126">isAvailable</span></span>](controls-isavailable.md)                             | <span data-ttu-id="e3b91-127">Получает сведения о доступности указанного типа сведений или о том, что может быть выполнено данное действие.</span><span class="sxs-lookup"><span data-stu-id="e3b91-127">Retrieves whether a specified type of information is available or a given action can be performed.</span></span>                                                |



 

<span data-ttu-id="e3b91-128">Объект **Controls** поддерживает следующие методы.</span><span class="sxs-lookup"><span data-stu-id="e3b91-128">The **Controls** object supports the following methods.</span></span>



| <span data-ttu-id="e3b91-129">Метод</span><span class="sxs-lookup"><span data-stu-id="e3b91-129">Method</span></span>                                                                  | <span data-ttu-id="e3b91-130">Описание</span><span class="sxs-lookup"><span data-stu-id="e3b91-130">Description</span></span>                                                                                      |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e3b91-131">фастфорвард</span><span class="sxs-lookup"><span data-stu-id="e3b91-131">fastForward</span></span>](controls-fastforward.md)                                 | <span data-ttu-id="e3b91-132">Запускает быстрое воспроизведение элемента мультимедиа в прямом направлении.</span><span class="sxs-lookup"><span data-stu-id="e3b91-132">Starts fast play of the media item in the forward direction.</span></span>                                     |
| [<span data-ttu-id="e3b91-133">фастреверсе</span><span class="sxs-lookup"><span data-stu-id="e3b91-133">fastReverse</span></span>](controls-fastreverse.md)                                 | <span data-ttu-id="e3b91-134">Запускает быстрое воспроизведение элемента мультимедиа в обратном направлении.</span><span class="sxs-lookup"><span data-stu-id="e3b91-134">Starts fast play of the media item in the reverse direction.</span></span>                                     |
| [<span data-ttu-id="e3b91-135">жетаудиолангуажедескриптион</span><span class="sxs-lookup"><span data-stu-id="e3b91-135">getAudioLanguageDescription</span></span>](controls-getaudiolanguagedescription.md) | <span data-ttu-id="e3b91-136">Извлекает описание для языка звука, соответствующего указанному индексу, основанному на единице.</span><span class="sxs-lookup"><span data-stu-id="e3b91-136">Retrieves the description for the audio language corresponding to the specified one-based index.</span></span> |
| [<span data-ttu-id="e3b91-137">жетаудиолангуажеид</span><span class="sxs-lookup"><span data-stu-id="e3b91-137">getAudioLanguageID</span></span>](controls-getaudiolanguageid.md)                   | <span data-ttu-id="e3b91-138">Возвращает код языка для указанного индекса языкового звука.</span><span class="sxs-lookup"><span data-stu-id="e3b91-138">Retrieves the LCID for a specified audio language index.</span></span>                                         |
| [<span data-ttu-id="e3b91-139">жетлангуаженаме</span><span class="sxs-lookup"><span data-stu-id="e3b91-139">getLanguageName</span></span>](controls-getlanguagename.md)                         | <span data-ttu-id="e3b91-140">Извлекает имя аудио языка с указанным LCID.</span><span class="sxs-lookup"><span data-stu-id="e3b91-140">Retrieves the name of the audio language with the specified LCID.</span></span>                                |
| [<span data-ttu-id="e3b91-141">далее</span><span class="sxs-lookup"><span data-stu-id="e3b91-141">next</span></span>](controls-next.md)                                               | <span data-ttu-id="e3b91-142">Устанавливает текущий элемент на следующий элемент в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="e3b91-142">Sets the current item to the next item in the playlist.</span></span>                                          |
| [<span data-ttu-id="e3b91-143">pause</span><span class="sxs-lookup"><span data-stu-id="e3b91-143">pause</span></span>](controls-pause.md)                                             | <span data-ttu-id="e3b91-144">Приостанавливает воспроизведение элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="e3b91-144">Pauses the playing of the media item.</span></span>                                                            |
| [<span data-ttu-id="e3b91-145">воспроизводит</span><span class="sxs-lookup"><span data-stu-id="e3b91-145">play</span></span>](controls-play.md)                                               | <span data-ttu-id="e3b91-146">Запускает воспроизведение элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="e3b91-146">Causes the media item to start playing.</span></span>                                                          |
| [<span data-ttu-id="e3b91-147">плайитем</span><span class="sxs-lookup"><span data-stu-id="e3b91-147">playItem</span></span>](controls-playitem.md)                                       | <span data-ttu-id="e3b91-148">Заставляет текущий элемент мультимедиа начать воспроизведение или возобновить воспроизведение приостановленного элемента.</span><span class="sxs-lookup"><span data-stu-id="e3b91-148">Causes the current media item to start playing, or resumes play of a paused item.</span></span>                |
| [<span data-ttu-id="e3b91-149">previous</span><span class="sxs-lookup"><span data-stu-id="e3b91-149">previous</span></span>](controls-previous.md)                                       | <span data-ttu-id="e3b91-150">Устанавливает текущий элемент на предыдущий элемент в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="e3b91-150">Sets the current item to the previous item in the playlist.</span></span>                                      |
| [<span data-ttu-id="e3b91-151">первом</span><span class="sxs-lookup"><span data-stu-id="e3b91-151">step</span></span>](controls-step.md)                                               | <span data-ttu-id="e3b91-152">Приводит к тому, что текущий элемент мультимедиа видеозаписи зависает при воспроизведении на следующем кадре.</span><span class="sxs-lookup"><span data-stu-id="e3b91-152">Causes the current video media item to freeze playback on the next frame.</span></span>                        |
| [<span data-ttu-id="e3b91-153">stop</span><span class="sxs-lookup"><span data-stu-id="e3b91-153">stop</span></span>](controls-stop.md)                                               | <span data-ttu-id="e3b91-154">Останавливает воспроизведение элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="e3b91-154">Stops the playing of the media item.</span></span>                                                             |



 

<span data-ttu-id="e3b91-155">Доступ к объекту **Controls** осуществляется через следующее свойство.</span><span class="sxs-lookup"><span data-stu-id="e3b91-155">The **Controls** object is accessed through the following property.</span></span>



| <span data-ttu-id="e3b91-156">Объект</span><span class="sxs-lookup"><span data-stu-id="e3b91-156">Object</span></span>                      | <span data-ttu-id="e3b91-157">Свойство</span><span class="sxs-lookup"><span data-stu-id="e3b91-157">Property</span></span>                        |
|-----------------------------|---------------------------------|
| [<span data-ttu-id="e3b91-158">Игрок</span><span class="sxs-lookup"><span data-stu-id="e3b91-158">Player</span></span>](player-object.md) | [<span data-ttu-id="e3b91-159">элементы управления</span><span class="sxs-lookup"><span data-stu-id="e3b91-159">controls</span></span>](player-controls.md) |



 

## <a name="see-also"></a><span data-ttu-id="e3b91-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3b91-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3b91-161">**Справочник по объектной модели для создания сценариев**</span><span class="sxs-lookup"><span data-stu-id="e3b91-161">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




