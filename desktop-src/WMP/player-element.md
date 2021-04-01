---
title: Элемент PLAYER
description: Элемент PLAYER
ms.assetid: 009090b3-0055-4700-9078-0749da239674
keywords:
- Обложки проигрывателя Windows Media, элемент PLAYER
- обложки, элемент PLAYER
- Элемент PLAYER
- Справочник по обложкам, элементу игрока
- элементы, проигрыватель
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a50eb4383eab279c28b75467a9ed803501e7720b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104132990"
---
# <a name="player-element"></a><span data-ttu-id="d8146-108">Элемент PLAYER</span><span class="sxs-lookup"><span data-stu-id="d8146-108">PLAYER Element</span></span>

<span data-ttu-id="d8146-109">Элемент **Player** позволяет определять обработчики событий и указывать свойство **URL** объекта **Player** во время разработки в файле определения обложки.</span><span class="sxs-lookup"><span data-stu-id="d8146-109">The **PLAYER** element lets you define event handlers and specify the **URL** property of the **Player** object at design time within a skin definition file.</span></span> <span data-ttu-id="d8146-110">В коде скрипта доступ к объекту **Player** осуществляется через глобальный атрибут **Player** , а не через имя, заданное атрибутом **ID** , который не поддерживается элементом **Player** .</span><span class="sxs-lookup"><span data-stu-id="d8146-110">Within script code, the **Player** object is accessed through the **player** global attribute rather than through a name specified by an **id** attribute, which is not supported by the **PLAYER** element.</span></span>

<span data-ttu-id="d8146-111">Элемент **Player** поддерживает следующий атрибут.</span><span class="sxs-lookup"><span data-stu-id="d8146-111">The **PLAYER** element supports the following attribute.</span></span>



| <span data-ttu-id="d8146-112">attribute</span><span class="sxs-lookup"><span data-stu-id="d8146-112">Attribute</span></span>             | <span data-ttu-id="d8146-113">Описание</span><span class="sxs-lookup"><span data-stu-id="d8146-113">Description</span></span>                                          |
|-----------------------|------------------------------------------------------|
| [<span data-ttu-id="d8146-114">URL-адрес</span><span class="sxs-lookup"><span data-stu-id="d8146-114">URL</span></span>](player-url.md) | <span data-ttu-id="d8146-115">Указывает или получает имя файла для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d8146-115">Specifies or retrieves the name of the file to play.</span></span> |



 

<span data-ttu-id="d8146-116">Элемент **Player** может реализовывать обработчики событий для следующих событий, запускаемых из объекта **Player** .</span><span class="sxs-lookup"><span data-stu-id="d8146-116">The **PLAYER** element can implement event handlers for the following events fired from the **Player** object.</span></span>



| <span data-ttu-id="d8146-117">Событие</span><span class="sxs-lookup"><span data-stu-id="d8146-117">Event</span></span>                                                                                            | <span data-ttu-id="d8146-118">Описание</span><span class="sxs-lookup"><span data-stu-id="d8146-118">Description</span></span>                                                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="d8146-119">аудиолангуажечанже</span><span class="sxs-lookup"><span data-stu-id="d8146-119">AudioLanguageChange</span></span>](player-player-audiolanguagechange.md)                                     | <span data-ttu-id="d8146-120">Происходит при изменении текущего звукового языка.</span><span class="sxs-lookup"><span data-stu-id="d8146-120">Occurs when the current audio language changes.</span></span>                                  |
| [<span data-ttu-id="d8146-121">ответов</span><span class="sxs-lookup"><span data-stu-id="d8146-121">Buffering</span></span>](player-player-buffering.md)                                                         | <span data-ttu-id="d8146-122">Происходит при начале или окончании буферизации проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d8146-122">Occurs when Windows Media Player begins or ends buffering.</span></span>                       |
| [<span data-ttu-id="d8146-123">кдроммедиачанже</span><span class="sxs-lookup"><span data-stu-id="d8146-123">CdromMediaChange</span></span>](player-player-cdrommediachange.md)                                           | <span data-ttu-id="d8146-124">Происходит при изменении носителя компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="d8146-124">Occurs when the CD media changes.</span></span>                                                |
| [<span data-ttu-id="d8146-125">куррентитемчанже</span><span class="sxs-lookup"><span data-stu-id="d8146-125">CurrentItemChange</span></span>](player-player-currentitemchange.md)                                         | <span data-ttu-id="d8146-126">Происходит при изменении текущего элемента.</span><span class="sxs-lookup"><span data-stu-id="d8146-126">Occurs when the current item changes.</span></span>                                            |
| [<span data-ttu-id="d8146-127">куррентмедиаитемаваилабле</span><span class="sxs-lookup"><span data-stu-id="d8146-127">CurrentMediaItemAvailable</span></span>](player-player-currentmediaitemavailable.md)                         | <span data-ttu-id="d8146-128">Происходит, когда текущий элемент мультимедиа станет доступным.</span><span class="sxs-lookup"><span data-stu-id="d8146-128">Occurs when the current media item becomes available.</span></span>                            |
| [<span data-ttu-id="d8146-129">куррентплайлистчанже</span><span class="sxs-lookup"><span data-stu-id="d8146-129">CurrentPlaylistChange</span></span>](player-player-currentplaylistchange.md)                                 | <span data-ttu-id="d8146-130">Происходит при изменении текущего списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d8146-130">Occurs when the current playlist changes.</span></span>                                        |
| [<span data-ttu-id="d8146-131">куррентплайлиститемаваилабле</span><span class="sxs-lookup"><span data-stu-id="d8146-131">CurrentPlaylistItemAvailable</span></span>](player-player-currentplaylistitemavailable.md)                   | <span data-ttu-id="d8146-132">Происходит, когда текущий элемент списка воспроизведения станет доступным.</span><span class="sxs-lookup"><span data-stu-id="d8146-132">Occurs when the current playlist item becomes available.</span></span>                         |
| [<span data-ttu-id="d8146-133">домаинчанже</span><span class="sxs-lookup"><span data-stu-id="d8146-133">DomainChange</span></span>](player-player-domainchange.md)                                                   | <span data-ttu-id="d8146-134">Происходит при изменении домена DVD.</span><span class="sxs-lookup"><span data-stu-id="d8146-134">Occurs when the DVD domain changes.</span></span>                                              |
| [<span data-ttu-id="d8146-135">Ошибка</span><span class="sxs-lookup"><span data-stu-id="d8146-135">Error</span></span>](player-player-error.md)                                                                 | <span data-ttu-id="d8146-136">Происходит, когда элемент управления проигрывателя Windows Media имеет условие ошибки.</span><span class="sxs-lookup"><span data-stu-id="d8146-136">Occurs when the Windows Media Player control has an error condition.</span></span>             |
| [<span data-ttu-id="d8146-137">маркерхит</span><span class="sxs-lookup"><span data-stu-id="d8146-137">MarkerHit</span></span>](player-player-markerhit.md)                                                         | <span data-ttu-id="d8146-138">Происходит при обнаружении проигрывателем Windows Media маркера в клипе.</span><span class="sxs-lookup"><span data-stu-id="d8146-138">Occurs when Windows Media Player encounters a marker in the clip.</span></span>                |
| [<span data-ttu-id="d8146-139">медиачанже</span><span class="sxs-lookup"><span data-stu-id="d8146-139">MediaChange</span></span>](player-player-mediachange.md)                                                     | <span data-ttu-id="d8146-140">Происходит при изменении элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d8146-140">Occurs when a media item changes.</span></span>                                                |
| [<span data-ttu-id="d8146-141">медиаколлектионаттрибутестрингаддед</span><span class="sxs-lookup"><span data-stu-id="d8146-141">MediaCollectionAttributeStringAdded</span></span>](player-player-mediacollectionattributestringadded.md)     | <span data-ttu-id="d8146-142">Происходит при добавлении значения атрибута в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="d8146-142">Occurs when an attribute value is added to the library.</span></span>                          |
| [<span data-ttu-id="d8146-143">медиаколлектионаттрибутестрингчанжед</span><span class="sxs-lookup"><span data-stu-id="d8146-143">MediaCollectionAttributeStringChanged</span></span>](player-player-mediacollectionattributestringchanged.md) | <span data-ttu-id="d8146-144">Происходит при изменении значения атрибута в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="d8146-144">Occurs when an attribute value in the library is changed.</span></span>                        |
| [<span data-ttu-id="d8146-145">медиаколлектионаттрибутестрингремовед</span><span class="sxs-lookup"><span data-stu-id="d8146-145">MediaCollectionAttributeStringRemoved</span></span>](player-player-mediacollectionattributestringremoved.md) | <span data-ttu-id="d8146-146">Происходит при удалении значения атрибута из библиотеки.</span><span class="sxs-lookup"><span data-stu-id="d8146-146">Occurs when an attribute value is removed from the library.</span></span>                      |
| [<span data-ttu-id="d8146-147">медиаколлектиончанже</span><span class="sxs-lookup"><span data-stu-id="d8146-147">MediaCollectionChange</span></span>](player-player-mediacollectionchange.md)                                 | <span data-ttu-id="d8146-148">Происходит при изменении объекта **медиаколлектион** .</span><span class="sxs-lookup"><span data-stu-id="d8146-148">Occurs when the **MediaCollection** object changes.</span></span>                              |
| [<span data-ttu-id="d8146-149">медиаеррор</span><span class="sxs-lookup"><span data-stu-id="d8146-149">MediaError</span></span>](player-player-mediaerror.md)                                                       | <span data-ttu-id="d8146-150">Происходит, когда объект **мультимедиа** имеет условие ошибки.</span><span class="sxs-lookup"><span data-stu-id="d8146-150">Occurs when the **Media** object has an error condition.</span></span>                         |
| [<span data-ttu-id="d8146-151">модечанже</span><span class="sxs-lookup"><span data-stu-id="d8146-151">ModeChange</span></span>](player-player-modechange.md)                                                       | <span data-ttu-id="d8146-152">Происходит при переключении между режимом "случайный" и нормальный.</span><span class="sxs-lookup"><span data-stu-id="d8146-152">Occurs when switching between shuffle and normal mode.</span></span>                           |
| [<span data-ttu-id="d8146-153">опенплайлистсвитч</span><span class="sxs-lookup"><span data-stu-id="d8146-153">OpenPlaylistSwitch</span></span>](player-player-openplaylistswitch.md)                                       | <span data-ttu-id="d8146-154">Происходит, когда начинается воспроизведение заголовка DVD-диска.</span><span class="sxs-lookup"><span data-stu-id="d8146-154">Occurs when a title on a DVD begins playing.</span></span>                                     |
| [<span data-ttu-id="d8146-155">опенстатечанже</span><span class="sxs-lookup"><span data-stu-id="d8146-155">OpenStateChange</span></span>](player-player-openstatechange.md)                                             | <span data-ttu-id="d8146-156">Происходит при *проигрывателе*. **опенстате** изменения.</span><span class="sxs-lookup"><span data-stu-id="d8146-156">Occurs when *player*.**openState** changes.</span></span>                                      |
| [<span data-ttu-id="d8146-157">плайлистчанже</span><span class="sxs-lookup"><span data-stu-id="d8146-157">PlaylistChange</span></span>](player-player-playlistchange.md)                                               | <span data-ttu-id="d8146-158">Происходит при изменении списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d8146-158">Occurs when a playlist changes.</span></span>                                                  |
| [<span data-ttu-id="d8146-159">плайлистколлектиончанже</span><span class="sxs-lookup"><span data-stu-id="d8146-159">PlaylistCollectionChange</span></span>](player-player-playlistcollectionchange.md)                           | <span data-ttu-id="d8146-160">Происходит при внесении каких-либо изменений в коллекцию списков воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d8146-160">Occurs when something changes in the playlist collection.</span></span>                        |
| [<span data-ttu-id="d8146-161">плайлистколлектионплайлистаддед</span><span class="sxs-lookup"><span data-stu-id="d8146-161">PlaylistCollectionPlaylistAdded</span></span>](player-player-playlistcollectionplaylistadded.md)             | <span data-ttu-id="d8146-162">Происходит при добавлении списка воспроизведения в коллекцию списков воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d8146-162">Occurs when a playlist is added to the playlist collection.</span></span>                      |
| [<span data-ttu-id="d8146-163">плайлистколлектионплайлистремовед</span><span class="sxs-lookup"><span data-stu-id="d8146-163">PlaylistCollectionPlaylistRemoved</span></span>](player-player-playlistcollectionplaylistremoved.md)         | <span data-ttu-id="d8146-164">Происходит при удалении списка воспроизведения из коллекции списков воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d8146-164">Occurs when a playlist is removed from the playlist collection.</span></span>                  |
| [<span data-ttu-id="d8146-165">плайстатечанже</span><span class="sxs-lookup"><span data-stu-id="d8146-165">PlayStateChange</span></span>](player-player-playstatechange.md)                                             | <span data-ttu-id="d8146-166">Происходит при *проигрывателе*. **плайстате** изменения.</span><span class="sxs-lookup"><span data-stu-id="d8146-166">Occurs when *player*.**playState** changes.</span></span>                                      |
| [<span data-ttu-id="d8146-167">поситиончанже</span><span class="sxs-lookup"><span data-stu-id="d8146-167">PositionChange</span></span>](player-player-positionchange.md)                                               | <span data-ttu-id="d8146-168">Происходит при *проигрывателе*. *элементы управления*. **CurrentPosition** изменения.</span><span class="sxs-lookup"><span data-stu-id="d8146-168">Occurs when *player*.*controls*.**currentPosition** changes.</span></span>                     |
| [<span data-ttu-id="d8146-169">ScriptCommand</span><span class="sxs-lookup"><span data-stu-id="d8146-169">ScriptCommand</span></span>](player-player-scriptcommand.md)                                                 | <span data-ttu-id="d8146-170">Происходит при обнаружении проигрывателем Windows Media команды сценария, внедренной в файл.</span><span class="sxs-lookup"><span data-stu-id="d8146-170">Occurs when Windows Media Player encounters a script command embedded in a file.</span></span> |
| [<span data-ttu-id="d8146-171">StatusChange</span><span class="sxs-lookup"><span data-stu-id="d8146-171">StatusChange</span></span>](player-player-statuschange.md)                                                   | <span data-ttu-id="d8146-172">Происходит при изменении значения свойства **Status** .</span><span class="sxs-lookup"><span data-stu-id="d8146-172">Occurs when the **status** property changes value.</span></span>                               |



 

## <a name="related-topics"></a><span data-ttu-id="d8146-173">См. также</span><span class="sxs-lookup"><span data-stu-id="d8146-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8146-174">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="d8146-174">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="d8146-175">**Справочник по программированию для обложки**</span><span class="sxs-lookup"><span data-stu-id="d8146-175">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




