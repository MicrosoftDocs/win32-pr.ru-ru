---
title: Сетевой объект
description: Объект Network предоставляет свойства и методы, используемые для доступа к статистике, связанной с качеством сетевого подключения, а также для указания и получения параметров прокси-сервера сети.
ms.assetid: 5ae6137e-22f5-4a65-8793-b6f66adb4cba
keywords:
- Проигрыватель Windows Media, сетевой объект
topic_type:
- apiref
api_name:
- Network Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d439679636bce773c43f5610060c4744ef4d5d7c
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "104412013"
---
# <a name="network-object"></a><span data-ttu-id="84eb0-104">Сетевой объект</span><span class="sxs-lookup"><span data-stu-id="84eb0-104">Network Object</span></span>

<span data-ttu-id="84eb0-105">Объект **Network** предоставляет свойства и методы, используемые для доступа к статистике, связанной с качеством сетевого подключения, а также для указания и получения параметров прокси-сервера сети.</span><span class="sxs-lookup"><span data-stu-id="84eb0-105">The **Network** object provides properties and methods used to access statistics relating to the quality of a network connection, and to specify and retrieve the network proxy settings.</span></span>

<span data-ttu-id="84eb0-106">Объект **Network** поддерживает следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="84eb0-106">The **Network** object supports the following properties.</span></span>



| <span data-ttu-id="84eb0-107">Свойство</span><span class="sxs-lookup"><span data-stu-id="84eb0-107">Property</span></span>                                           | <span data-ttu-id="84eb0-108">Описание</span><span class="sxs-lookup"><span data-stu-id="84eb0-108">Description</span></span>                                                                                 |
|----------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84eb0-109">Связи</span><span class="sxs-lookup"><span data-stu-id="84eb0-109">bandWidth</span></span>](network-bandwidth.md)                 | <span data-ttu-id="84eb0-110">Извлекает текущую пропускную способность элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="84eb0-110">Retrieves the current bandwidth of the media item.</span></span>                                          |
| [<span data-ttu-id="84eb0-111">Скорость</span><span class="sxs-lookup"><span data-stu-id="84eb0-111">bitRate</span></span>](network-bitrate.md)                     | <span data-ttu-id="84eb0-112">Извлекает текущую полученную скорость.</span><span class="sxs-lookup"><span data-stu-id="84eb0-112">Retrieves the current bit rate being received.</span></span>                                              |
| [<span data-ttu-id="84eb0-113">буфферингкаунт</span><span class="sxs-lookup"><span data-stu-id="84eb0-113">bufferingCount</span></span>](network-bufferingcount.md)       | <span data-ttu-id="84eb0-114">Извлекает количество попыток буферизации во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="84eb0-114">Retrieves the number of times buffering occurred during playback.</span></span>                           |
| [<span data-ttu-id="84eb0-115">буфферингпрогресс</span><span class="sxs-lookup"><span data-stu-id="84eb0-115">bufferingProgress</span></span>](network-bufferingprogress.md) | <span data-ttu-id="84eb0-116">Возвращает процент завершенной буферизации.</span><span class="sxs-lookup"><span data-stu-id="84eb0-116">Retrieves the percentage of buffering completed.</span></span>                                            |
| [<span data-ttu-id="84eb0-117">буфферингтиме</span><span class="sxs-lookup"><span data-stu-id="84eb0-117">bufferingTime</span></span>](network-bufferingtime.md)         | <span data-ttu-id="84eb0-118">Указывает или получает количество времени буферизации в миллисекундах перед началом воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="84eb0-118">Specifies or retrieves the amount of buffering time in milliseconds before playback begins.</span></span> |
| [<span data-ttu-id="84eb0-119">довнлоадпрогресс</span><span class="sxs-lookup"><span data-stu-id="84eb0-119">downloadProgress</span></span>](network-downloadprogress.md)   | <span data-ttu-id="84eb0-120">Возвращает процент завершенной загрузки.</span><span class="sxs-lookup"><span data-stu-id="84eb0-120">Retrieves the percentage of download completed.</span></span>                                             |
| [<span data-ttu-id="84eb0-121">енкодедфрамерате</span><span class="sxs-lookup"><span data-stu-id="84eb0-121">encodedFrameRate</span></span>](network-encodedframerate.md)   | <span data-ttu-id="84eb0-122">Извлекает частоту кадров видео, указанную автором содержимого.</span><span class="sxs-lookup"><span data-stu-id="84eb0-122">Retrieves the video frame rate specified by the content author.</span></span>                             |
| [<span data-ttu-id="84eb0-123">Частота</span><span class="sxs-lookup"><span data-stu-id="84eb0-123">frameRate</span></span>](network-framerate.md)                 | <span data-ttu-id="84eb0-124">Извлекает текущую частоту кадров видео.</span><span class="sxs-lookup"><span data-stu-id="84eb0-124">Retrieves the current video frame rate.</span></span>                                                     |
| [<span data-ttu-id="84eb0-125">фрамесскиппед</span><span class="sxs-lookup"><span data-stu-id="84eb0-125">framesSkipped</span></span>](network-framesskipped.md)         | <span data-ttu-id="84eb0-126">Возвращает общее число кадров, пропущенных во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="84eb0-126">Retrieves the total number of frames skipped during playback.</span></span>                               |
| [<span data-ttu-id="84eb0-127">лостпаккетс</span><span class="sxs-lookup"><span data-stu-id="84eb0-127">lostPackets</span></span>](network-lostpackets.md)             | <span data-ttu-id="84eb0-128">Возвращает число потерянных пакетов.</span><span class="sxs-lookup"><span data-stu-id="84eb0-128">Retrieves the number of packets lost.</span></span>                                                       |
| [<span data-ttu-id="84eb0-129">maxBandwidth</span><span class="sxs-lookup"><span data-stu-id="84eb0-129">maxBandwidth</span></span>](network-maxbandwidth.md)           | <span data-ttu-id="84eb0-130">Указывает или получает максимально допустимую пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="84eb0-130">Specifies or retrieves the maximum allowed bandwidth.</span></span>                                       |
| [<span data-ttu-id="84eb0-131">максбитрате</span><span class="sxs-lookup"><span data-stu-id="84eb0-131">maxBitRate</span></span>](network-maxbitrate.md)               | <span data-ttu-id="84eb0-132">Возвращает максимальную возможную скорость видео.</span><span class="sxs-lookup"><span data-stu-id="84eb0-132">Retrieves the maximum possible video bit rate.</span></span>                                              |
| [<span data-ttu-id="84eb0-133">рецеиведпаккетс</span><span class="sxs-lookup"><span data-stu-id="84eb0-133">receivedPackets</span></span>](network-receivedpackets.md)     | <span data-ttu-id="84eb0-134">Возвращает число полученных пакетов.</span><span class="sxs-lookup"><span data-stu-id="84eb0-134">Retrieves the number of packets received.</span></span>                                                   |
| [<span data-ttu-id="84eb0-135">рецептионкуалити</span><span class="sxs-lookup"><span data-stu-id="84eb0-135">receptionQuality</span></span>](network-receptionquality.md)   | <span data-ttu-id="84eb0-136">Возвращает процент полученных пакетов за последние 30 секунд.</span><span class="sxs-lookup"><span data-stu-id="84eb0-136">Retrieves the percentage of packets received in the last 30 seconds.</span></span>                        |
| [<span data-ttu-id="84eb0-137">рековередпаккетс</span><span class="sxs-lookup"><span data-stu-id="84eb0-137">recoveredPackets</span></span>](network-recoveredpackets.md)   | <span data-ttu-id="84eb0-138">Возвращает количество восстановленных пакетов.</span><span class="sxs-lookup"><span data-stu-id="84eb0-138">Retrieves the number of recovered packets.</span></span>                                                  |
| [<span data-ttu-id="84eb0-139">саурцепротокол</span><span class="sxs-lookup"><span data-stu-id="84eb0-139">sourceProtocol</span></span>](network-sourceprotocol.md)       | <span data-ttu-id="84eb0-140">Возвращает исходный протокол, используемый для получения данных.</span><span class="sxs-lookup"><span data-stu-id="84eb0-140">Retrieves the source protocol used to receive data.</span></span>                                         |



 

<span data-ttu-id="84eb0-141">Объект **Network** поддерживает следующие методы.</span><span class="sxs-lookup"><span data-stu-id="84eb0-141">The **Network** object supports the following methods.</span></span>



| <span data-ttu-id="84eb0-142">Метод</span><span class="sxs-lookup"><span data-stu-id="84eb0-142">Method</span></span>                                                       | <span data-ttu-id="84eb0-143">Описание</span><span class="sxs-lookup"><span data-stu-id="84eb0-143">Description</span></span>                                                                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84eb0-144">жетпроксибипассфорлокал</span><span class="sxs-lookup"><span data-stu-id="84eb0-144">getProxyBypassForLocal</span></span>](network-getproxybypassforlocal.md) | <span data-ttu-id="84eb0-145">Извлекает значение, указывающее, должен ли прокси-сервер пропускать, если сервер-источник находится в локальной сети.</span><span class="sxs-lookup"><span data-stu-id="84eb0-145">Retrieves a value indicating whether the proxy server should by bypassed if the origin server is on a local network.</span></span> |
| [<span data-ttu-id="84eb0-146">жетпроксексцептионлист</span><span class="sxs-lookup"><span data-stu-id="84eb0-146">getProxyExceptionList</span></span>](network-getproxyexceptionlist.md)   | <span data-ttu-id="84eb0-147">Извлекает список исключений прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="84eb0-147">Retrieves the proxy exception list.</span></span>                                                                                  |
| [<span data-ttu-id="84eb0-148">жетпроксинаме</span><span class="sxs-lookup"><span data-stu-id="84eb0-148">getProxyName</span></span>](network-getproxyname.md)                     | <span data-ttu-id="84eb0-149">Возвращает имя используемого прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="84eb0-149">Retrieves the name of a proxy server to use.</span></span>                                                                         |
| [<span data-ttu-id="84eb0-150">жетпроксипорт</span><span class="sxs-lookup"><span data-stu-id="84eb0-150">getProxyPort</span></span>](network-getproxyport.md)                     | <span data-ttu-id="84eb0-151">Извлекает порт прокси-сервера для использования.</span><span class="sxs-lookup"><span data-stu-id="84eb0-151">Retrieves the proxy port to use.</span></span>                                                                                     |
| [<span data-ttu-id="84eb0-152">жетпроксисеттингс</span><span class="sxs-lookup"><span data-stu-id="84eb0-152">getProxySettings</span></span>](network-getproxysettings.md)             | <span data-ttu-id="84eb0-153">Получает параметр прокси-сервера для данного протокола.</span><span class="sxs-lookup"><span data-stu-id="84eb0-153">Retrieves the proxy setting for a given protocol.</span></span>                                                                    |
| [<span data-ttu-id="84eb0-154">сетпроксибипассфорлокал</span><span class="sxs-lookup"><span data-stu-id="84eb0-154">setProxyBypassForLocal</span></span>](network-setproxybypassforlocal.md) | <span data-ttu-id="84eb0-155">Указывает значение, указывающее, должен ли прокси-сервер обходиться, если исходный сервер находится в локальной сети.</span><span class="sxs-lookup"><span data-stu-id="84eb0-155">Specifies a value indicating whether the proxy server should by bypassed if the origin server is on a local network.</span></span> |
| [<span data-ttu-id="84eb0-156">сетпроксексцептионлист</span><span class="sxs-lookup"><span data-stu-id="84eb0-156">setProxyExceptionList</span></span>](network-setproxyexceptionlist.md)   | <span data-ttu-id="84eb0-157">Указывает список исключений прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="84eb0-157">Specifies the proxy exception list.</span></span>                                                                                  |
| [<span data-ttu-id="84eb0-158">сетпроксинаме</span><span class="sxs-lookup"><span data-stu-id="84eb0-158">setProxyName</span></span>](network-setproxyname.md)                     | <span data-ttu-id="84eb0-159">Указывает имя прокси-сервера для использования.</span><span class="sxs-lookup"><span data-stu-id="84eb0-159">Specifies the name of a proxy server to use.</span></span>                                                                         |
| [<span data-ttu-id="84eb0-160">сетпроксипорт</span><span class="sxs-lookup"><span data-stu-id="84eb0-160">setProxyPort</span></span>](network-setproxyport.md)                     | <span data-ttu-id="84eb0-161">Указывает используемый порт прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="84eb0-161">Specifies the proxy port to use.</span></span>                                                                                     |
| [<span data-ttu-id="84eb0-162">setProxySettings</span><span class="sxs-lookup"><span data-stu-id="84eb0-162">setProxySettings</span></span>](network-setproxysettings.md)             | <span data-ttu-id="84eb0-163">Указывает параметр прокси-сервера для данного протокола.</span><span class="sxs-lookup"><span data-stu-id="84eb0-163">Specifies the proxy setting for a given protocol.</span></span>                                                                    |



 

<span data-ttu-id="84eb0-164">Доступ к объекту **сети** осуществляется через следующее свойство.</span><span class="sxs-lookup"><span data-stu-id="84eb0-164">The **Network** object is accessed through the following property.</span></span>



| <span data-ttu-id="84eb0-165">Объект</span><span class="sxs-lookup"><span data-stu-id="84eb0-165">Object</span></span>                      | <span data-ttu-id="84eb0-166">Свойство</span><span class="sxs-lookup"><span data-stu-id="84eb0-166">Property</span></span>                      |
|-----------------------------|-------------------------------|
| [<span data-ttu-id="84eb0-167">Игрок</span><span class="sxs-lookup"><span data-stu-id="84eb0-167">Player</span></span>](player-object.md) | [<span data-ttu-id="84eb0-168">сети</span><span class="sxs-lookup"><span data-stu-id="84eb0-168">network</span></span>](player-network.md) |



 

## <a name="see-also"></a><span data-ttu-id="84eb0-169">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="84eb0-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84eb0-170">**Справочник по объектной модели для создания сценариев**</span><span class="sxs-lookup"><span data-stu-id="84eb0-170">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




