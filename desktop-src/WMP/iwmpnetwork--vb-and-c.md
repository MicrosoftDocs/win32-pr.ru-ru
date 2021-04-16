---
title: Интерфейс Ивмпнетворк (VB и C) (WMP. h)
description: Предоставляет свойства и методы для доступа к статистике, связанной с качеством сетевого подключения, а также для указания и получения параметров прокси-сервера сети. Интерфейс Ивмпнетворк предоставляет следующие свойства.
ms.assetid: d385510f-11cf-4a2a-96be-b416cddc3d80
keywords:
- Ивмпнетворк (VB и C) интерфейс проигрывателя Windows Media
- Ивмпнетворк (VB и C) интерфейс проигрывателя Windows Media, описание
topic_type:
- apiref
api_name:
- IWMPNetwork (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 301fe5c89d2eb5df3dd4c22927e75a5607e7abd0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688789"
---
# <a name="iwmpnetwork-vb-and-c-interface"></a><span data-ttu-id="cf3ee-105">Интерфейс Ивмпнетворк (VB и C#)</span><span class="sxs-lookup"><span data-stu-id="cf3ee-105">IWMPNetwork (VB and C#) interface</span></span>

<span data-ttu-id="cf3ee-106">Предоставляет свойства и методы для доступа к статистике, связанной с качеством сетевого подключения, а также для указания и получения параметров прокси-сервера сети.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-106">Provides properties and methods to access statistics relating to the quality of a network connection, and to specify and retrieve the network proxy settings.</span></span>

<span data-ttu-id="cf3ee-107">Интерфейс **ивмпнетворк** предоставляет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-107">The **IWMPNetwork** interface exposes the following properties.</span></span>

## <a name="members"></a><span data-ttu-id="cf3ee-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="cf3ee-108">Members</span></span>

<span data-ttu-id="cf3ee-109">Интерфейс **ивмпнетворк (VB и C#)** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="cf3ee-109">The **IWMPNetwork (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="cf3ee-110">Методы</span><span class="sxs-lookup"><span data-stu-id="cf3ee-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="cf3ee-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="cf3ee-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cf3ee-112">Методы</span><span class="sxs-lookup"><span data-stu-id="cf3ee-112">Methods</span></span>

<span data-ttu-id="cf3ee-113">Интерфейс **ивмпнетворк (VB и C#)** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-113">The **IWMPNetwork (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="cf3ee-114">Метод</span><span class="sxs-lookup"><span data-stu-id="cf3ee-114">Method</span></span>                                                                                           | <span data-ttu-id="cf3ee-115">Описание</span><span class="sxs-lookup"><span data-stu-id="cf3ee-115">Description</span></span>                                                                                                            |
|:-------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cf3ee-116">**жетпроксибипассфорлокал**</span><span class="sxs-lookup"><span data-stu-id="cf3ee-116">**getProxyBypassForLocal**</span></span>](iwmpnetwork-getproxybypassforlocal--vb-and-c.md)                   | <span data-ttu-id="cf3ee-117">Возвращает значение, указывающее, пропускается ли прокси-сервер, если исходный сервер находится в локальной сети.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-117">Returns a value indicating whether the proxy server is bypassed if the origin server is on a local network.</span></span><br/> |
| [<span data-ttu-id="cf3ee-118">**жетпроксексцептионлист**</span><span class="sxs-lookup"><span data-stu-id="cf3ee-118">**getProxyExceptionList**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyexceptionlist--vb-and-c.md)   | <span data-ttu-id="cf3ee-119">Возвращает список исключений прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-119">Returns the proxy exception list.</span></span><br/>                                                                           |
| [<span data-ttu-id="cf3ee-120">**жетпроксинаме**</span><span class="sxs-lookup"><span data-stu-id="cf3ee-120">**getProxyName**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyname--vb-and-c.md)                     | <span data-ttu-id="cf3ee-121">Возвращает имя используемого прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-121">Returns the name of the proxy server being used.</span></span><br/>                                                            |
| [<span data-ttu-id="cf3ee-122">**жетпроксипорт**</span><span class="sxs-lookup"><span data-stu-id="cf3ee-122">**getProxyPort**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyport--vb-and-c.md)                     | <span data-ttu-id="cf3ee-123">Возвращает используемый порт прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-123">Returns the proxy port being used.</span></span><br/>                                                                          |
| [<span data-ttu-id="cf3ee-124">**жетпроксисеттингс**</span><span class="sxs-lookup"><span data-stu-id="cf3ee-124">**getProxySettings**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)             | <span data-ttu-id="cf3ee-125">Возвращает сведения о параметрах прокси-сервера для протокола.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-125">Returns information about the proxy settings for a protocol.</span></span><br/>                                                |
| [<span data-ttu-id="cf3ee-126">**сетпроксибипассфорлокал**</span><span class="sxs-lookup"><span data-stu-id="cf3ee-126">**setProxyBypassForLocal**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxybypassforlocal--vb-and-c.md) | <span data-ttu-id="cf3ee-127">Указывает, пропускается ли прокси-сервер, если исходный сервер находится в локальной сети.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-127">Specifies whether the proxy server is bypassed if the origin server is on a local network.</span></span><br/>                  |
| [<span data-ttu-id="cf3ee-128">**сетпроксексцептионлист**</span><span class="sxs-lookup"><span data-stu-id="cf3ee-128">**setProxyExceptionList**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyexceptionlist--vb-and-c.md)   | <span data-ttu-id="cf3ee-129">Указывает список исключений прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-129">Specifies the proxy exception list.</span></span><br/>                                                                         |
| [<span data-ttu-id="cf3ee-130">**сетпроксинаме**</span><span class="sxs-lookup"><span data-stu-id="cf3ee-130">**setProxyName**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyname--vb-and-c.md)                     | <span data-ttu-id="cf3ee-131">Указывает имя используемого прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-131">Specifies the name of the proxy server to use.</span></span><br/>                                                              |
| [<span data-ttu-id="cf3ee-132">**сетпроксипорт**</span><span class="sxs-lookup"><span data-stu-id="cf3ee-132">**setProxyPort**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyport--vb-and-c.md)                     | <span data-ttu-id="cf3ee-133">Указывает используемый порт прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-133">Specifies the proxy port to use.</span></span><br/>                                                                            |
| [<span data-ttu-id="cf3ee-134">**setProxySettings**</span><span class="sxs-lookup"><span data-stu-id="cf3ee-134">**setProxySettings**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxysettings--vb-and-c.md)             | <span data-ttu-id="cf3ee-135">Задает параметры прокси-сервера для протокола.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-135">Specifies the proxy settings for a protocol.</span></span><br/>                                                                |



 

### <a name="properties"></a><span data-ttu-id="cf3ee-136">Свойства</span><span class="sxs-lookup"><span data-stu-id="cf3ee-136">Properties</span></span>

<span data-ttu-id="cf3ee-137">Интерфейс **ивмпнетворк (VB и C#)** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-137">The **IWMPNetwork (VB and C#)** interface has these properties.</span></span>



| <span data-ttu-id="cf3ee-138">Свойство</span><span class="sxs-lookup"><span data-stu-id="cf3ee-138">Property</span></span>                                                                                          | <span data-ttu-id="cf3ee-139">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="cf3ee-139">Access type</span></span>           | <span data-ttu-id="cf3ee-140">Описание</span><span class="sxs-lookup"><span data-stu-id="cf3ee-140">Description</span></span>                                                                                  |
|:--------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cf3ee-141">**Связи**</span><span class="sxs-lookup"><span data-stu-id="cf3ee-141">**bandWidth**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bandwidth--vb-and-c.md)<br/>                 | <span data-ttu-id="cf3ee-142">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf3ee-142">Read-only</span></span><br/>  | <span data-ttu-id="cf3ee-143">Возвращает текущую пропускную способность элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-143">Gets the current bandwidth of the media item.</span></span><br/>                                     |
| [<span data-ttu-id="cf3ee-144">**Скорость**</span><span class="sxs-lookup"><span data-stu-id="cf3ee-144">**bitRate**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bitrate--vb-and-c.md)<br/>                     | <span data-ttu-id="cf3ee-145">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf3ee-145">Read-only</span></span><br/>  | <span data-ttu-id="cf3ee-146">Возвращает скорость получения текущей скорости.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-146">Gets the current bit rate being received.</span></span><br/>                                         |
| [<span data-ttu-id="cf3ee-147">**буфферингкаунт**</span><span class="sxs-lookup"><span data-stu-id="cf3ee-147">**bufferingCount**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bufferingcount--vb-and-c.md)<br/>       | <span data-ttu-id="cf3ee-148">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf3ee-148">Read-only</span></span><br/>  | <span data-ttu-id="cf3ee-149">Возвращает количество попыток буферизации во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-149">Gets the number of times buffering occurred during playback.</span></span><br/>                      |
| [<span data-ttu-id="cf3ee-150">**буфферингпрогресс**</span><span class="sxs-lookup"><span data-stu-id="cf3ee-150">**bufferingProgress**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bufferingprogress--vb-and-c.md)<br/> | <span data-ttu-id="cf3ee-151">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf3ee-151">Read-only</span></span><br/>  | <span data-ttu-id="cf3ee-152">Возвращает процент завершенной буферизации.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-152">Gets the percentage of buffering completed.</span></span><br/>                                       |
| [<span data-ttu-id="cf3ee-153">**буфферингтиме**</span><span class="sxs-lookup"><span data-stu-id="cf3ee-153">**bufferingTime**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bufferingtime--vb-and-c.md)<br/>         | <span data-ttu-id="cf3ee-154">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="cf3ee-154">Read/write</span></span><br/> | <span data-ttu-id="cf3ee-155">Возвращает или задает количество времени буферизации в миллисекундах перед началом воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-155">Gets or sets the amount of buffering time in milliseconds before playback begins.</span></span><br/> |
| [<span data-ttu-id="cf3ee-156">**довнлоадпрогресс**</span><span class="sxs-lookup"><span data-stu-id="cf3ee-156">**downloadProgress**</span></span>](wmplibiwmpnetwork-iwmpnetwork-downloadprogress--vb-and-c.md)<br/>   | <span data-ttu-id="cf3ee-157">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf3ee-157">Read-only</span></span><br/>  | <span data-ttu-id="cf3ee-158">Возвращает процент завершенной загрузки.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-158">Gets the percentage of downloading completed.</span></span><br/>                                     |
| [<span data-ttu-id="cf3ee-159">**енкодедфрамерате**</span><span class="sxs-lookup"><span data-stu-id="cf3ee-159">**encodedFrameRate**</span></span>](wmplibiwmpnetwork-iwmpnetwork-encodedframerate--vb-and-c.md)<br/>   | <span data-ttu-id="cf3ee-160">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf3ee-160">Read-only</span></span><br/>  | <span data-ttu-id="cf3ee-161">Возвращает частоту кадров видео, указанную автором содержимого.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-161">Gets the video frame rate specified by the content author.</span></span><br/>                        |
| [<span data-ttu-id="cf3ee-162">**Частота**</span><span class="sxs-lookup"><span data-stu-id="cf3ee-162">**frameRate**</span></span>](wmplibiwmpnetwork-iwmpnetwork-framerate--vb-and-c.md)<br/>                 | <span data-ttu-id="cf3ee-163">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf3ee-163">Read-only</span></span><br/>  | <span data-ttu-id="cf3ee-164">Возвращает текущую частоту кадров видео.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-164">Gets the current video frame rate.</span></span><br/>                                                |
| [<span data-ttu-id="cf3ee-165">**фрамесскиппед**</span><span class="sxs-lookup"><span data-stu-id="cf3ee-165">**framesSkipped**</span></span>](wmplibiwmpnetwork-iwmpnetwork-framesskipped--vb-and-c.md)<br/>         | <span data-ttu-id="cf3ee-166">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf3ee-166">Read-only</span></span><br/>  | <span data-ttu-id="cf3ee-167">Возвращает общее число кадров, пропущенных во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-167">Gets the total number of frames skipped during playback.</span></span><br/>                          |
| [<span data-ttu-id="cf3ee-168">**лостпаккетс**</span><span class="sxs-lookup"><span data-stu-id="cf3ee-168">**lostPackets**</span></span>](wmplibiwmpnetwork-iwmpnetwork-lostpackets--vb-and-c.md)<br/>             | <span data-ttu-id="cf3ee-169">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf3ee-169">Read-only</span></span><br/>  | <span data-ttu-id="cf3ee-170">Возвращает число потерянных пакетов.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-170">Gets the number of packets lost.</span></span><br/>                                                  |
| [<span data-ttu-id="cf3ee-171">**maxBandwidth**</span><span class="sxs-lookup"><span data-stu-id="cf3ee-171">**maxBandwidth**</span></span>](wmplibiwmpnetwork-iwmpnetwork-maxbandwidth--vb-and-c.md)<br/>           | <span data-ttu-id="cf3ee-172">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="cf3ee-172">Read/write</span></span><br/> | <span data-ttu-id="cf3ee-173">Возвращает или задает максимально допустимую пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-173">Gets or sets the maximum allowed bandwidth.</span></span><br/>                                       |
| [<span data-ttu-id="cf3ee-174">**максбитрате**</span><span class="sxs-lookup"><span data-stu-id="cf3ee-174">**maxBitRate**</span></span>](wmplibiwmpnetwork-iwmpnetwork-maxbitrate--vb-and-c.md)<br/>               | <span data-ttu-id="cf3ee-175">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf3ee-175">Read-only</span></span><br/>  | <span data-ttu-id="cf3ee-176">Возвращает максимальную возможную скорость видео.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-176">Gets the maximum possible video bit rate.</span></span><br/>                                         |
| [<span data-ttu-id="cf3ee-177">**рецеиведпаккетс**</span><span class="sxs-lookup"><span data-stu-id="cf3ee-177">**receivedPackets**</span></span>](wmplibiwmpnetwork-iwmpnetwork-receivedpackets--vb-and-c.md)<br/>     | <span data-ttu-id="cf3ee-178">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf3ee-178">Read-only</span></span><br/>  | <span data-ttu-id="cf3ee-179">Возвращает число полученных пакетов.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-179">Gets the number of packets received.</span></span><br/>                                              |
| [<span data-ttu-id="cf3ee-180">**рецептионкуалити**</span><span class="sxs-lookup"><span data-stu-id="cf3ee-180">**receptionQuality**</span></span>](wmplibiwmpnetwork-iwmpnetwork-receptionquality--vb-and-c.md)<br/>   | <span data-ttu-id="cf3ee-181">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf3ee-181">Read-only</span></span><br/>  | <span data-ttu-id="cf3ee-182">Возвращает процент пакетов, которые не были потеряны за последние 30 секунд.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-182">Gets the percentage of packets not lost in the last 30 seconds.</span></span><br/>                   |
| [<span data-ttu-id="cf3ee-183">**рековередпаккетс**</span><span class="sxs-lookup"><span data-stu-id="cf3ee-183">**recoveredPackets**</span></span>](wmplibiwmpnetwork-iwmpnetwork-recoveredpackets--vb-and-c.md)<br/>   | <span data-ttu-id="cf3ee-184">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf3ee-184">Read-only</span></span><br/>  | <span data-ttu-id="cf3ee-185">Возвращает число восстановленных пакетов.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-185">Gets the number of recovered packets.</span></span><br/>                                             |
| [<span data-ttu-id="cf3ee-186">**саурцепротокол**</span><span class="sxs-lookup"><span data-stu-id="cf3ee-186">**sourceProtocol**</span></span>](wmplibiwmpnetwork-iwmpnetwork-sourceprotocol--vb-and-c.md)<br/>       | <span data-ttu-id="cf3ee-187">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf3ee-187">Read-only</span></span><br/>  | <span data-ttu-id="cf3ee-188">Возвращает исходный протокол, используемый для получения данных.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-188">Gets the source protocol used to receive data.</span></span><br/>                                    |



 

<span data-ttu-id="cf3ee-189">Получите интерфейс **ивмпнетворк** с помощью следующего свойства.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-189">Get an **IWMPNetwork** interface by using the following property.</span></span>



| <span data-ttu-id="cf3ee-190">Объект</span><span class="sxs-lookup"><span data-stu-id="cf3ee-190">Object</span></span>                                                                   | <span data-ttu-id="cf3ee-191">Свойство</span><span class="sxs-lookup"><span data-stu-id="cf3ee-191">Property</span></span>                                                           |
|--------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="cf3ee-192">Объект Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="cf3ee-192">AxWindowsMediaPlayer Object</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="cf3ee-193">**сети**</span><span class="sxs-lookup"><span data-stu-id="cf3ee-193">**network**</span></span>](axwmplib-axwindowsmediaplayer-network--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="cf3ee-194">Требования</span><span class="sxs-lookup"><span data-stu-id="cf3ee-194">Requirements</span></span>



| <span data-ttu-id="cf3ee-195">Требование</span><span class="sxs-lookup"><span data-stu-id="cf3ee-195">Requirement</span></span> | <span data-ttu-id="cf3ee-196">Значение</span><span class="sxs-lookup"><span data-stu-id="cf3ee-196">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cf3ee-197">Header</span><span class="sxs-lookup"><span data-stu-id="cf3ee-197">Header</span></span><br/> | <dl> <span data-ttu-id="cf3ee-198"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf3ee-198"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf3ee-199">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf3ee-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf3ee-200">**Интерфейсы для Visual Basic .NET и C #**</span><span class="sxs-lookup"><span data-stu-id="cf3ee-200">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





