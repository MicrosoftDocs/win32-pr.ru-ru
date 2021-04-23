---
title: Сравнение подробной модели объектов
description: Сравнение подробной модели объектов
ms.assetid: 8f08e2a6-1944-4814-b3b7-680a3722e1a0
keywords:
- Проигрыватель Windows Media, объектная модель
- Объектная модель проигрывателя Windows Media, отличия версий
- Объектная модель, различия версий
- Элемент управления ActiveX проигрывателя Windows Media, различия версий
- Элемент управления ActiveX, различия версий
- Элемент управления ActiveX мобильных устройств проигрывателя Windows Media, различия версий
- Проигрыватель Windows Media Mobile, объектная модель
- рекомендации по миграции, отличия версий
- версии проигрывателя Windows Media, объектная модель
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086607a9d367f42479e155e3273c30d88425a457
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2020
ms.locfileid: "104069513"
---
# <a name="detailed-object-model-comparison"></a><span data-ttu-id="bc60d-112">Сравнение подробной модели объектов</span><span class="sxs-lookup"><span data-stu-id="bc60d-112">Detailed Object Model Comparison</span></span>

<span data-ttu-id="bc60d-113">В следующей таблице сравниваются свойства объектной модели проигрывателя Windows Media 6,4 с объектной моделью проигрывателя Windows Media 7 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="bc60d-113">The following table compares the Windows Media Player 6.4 object model properties with the Windows Media Player 7 or later object model.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bc60d-114">Свойство проигрывателя Windows Media 6,4</span><span class="sxs-lookup"><span data-stu-id="bc60d-114">Windows Media Player 6.4 property</span></span></th>
<th><span data-ttu-id="bc60d-115">Проигрыватель Windows Media 7 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="bc60d-115">Windows Media Player 7 or later equivalent</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bc60d-116"><em>Player6</em>. <strong>Алловчанжедисплайсизе</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-116"><em>Player6</em>.<strong>AllowChangeDisplaySize</strong></span></span></td>
<td><span data-ttu-id="bc60d-117">При отображении проигрывателя Windows Media 7 или более поздней версии автоматически изменяется размер по размеру носителя.</span><span class="sxs-lookup"><span data-stu-id="bc60d-117">The display of Windows Media Player 7 or later automatically resizes to fit the media.</span></span> <span data-ttu-id="bc60d-118">Свойства высоты и ширины можно задать в <OBJECT> теге или в скрипте.</span><span class="sxs-lookup"><span data-stu-id="bc60d-118">You can set the height and width properties in the <OBJECT> tag or in script.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-119"><em>Player6</em>. <strong>Алловскан</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-119"><em>Player6</em>.<strong>AllowScan</strong></span></span></td>
<td><span data-ttu-id="bc60d-120"><em>Элементы управления</em>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-120"><em>Controls</em>.</span></span> <span data-ttu-id="bc60d-121"><strong>фастфорвард</strong> и <em>элементы управления</em>. <strong>фастреверсе</strong> автоматически включаются для типов файлов, поддерживающих эти методы.</span><span class="sxs-lookup"><span data-stu-id="bc60d-121"><strong>fastForward</strong> and <em>Controls</em>.<strong>fastReverse</strong> are automatically enabled for file types that support these methods.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-122"><em>Player6</em>. <strong>Англесаваилабле</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-122"><em>Player6</em>.<strong>AnglesAvailable</strong></span></span></td>
<td><span data-ttu-id="bc60d-123">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-123">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-124"><em>Player6</em>. <strong>Аниматионатстарт</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-124"><em>Player6</em>.<strong>AnimationAtStart</strong></span></span></td>
<td><span data-ttu-id="bc60d-125">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-125">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-126"><em>Player6</em>. <strong>Аудиостреам</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-126"><em>Player6</em>.<strong>AudioStream</strong></span></span></td>
<td><span data-ttu-id="bc60d-127">Используйте <em>элементы управления</em>. <strong>куррентаудиолангуажеиндекс</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-127">Use <em>Controls</em>.<strong>currentAudioLanguageIndex</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-128"><em>Player6</em>. <strong>Аудиостреамсаваилабле</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-128"><em>Player6</em>.<strong>AudioStreamsAvailable</strong></span></span></td>
<td><span data-ttu-id="bc60d-129">Используйте <em>элементы управления</em>. <strong>аудиолангуажекаунт</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-129">Use <em>Controls</em>.<strong>audioLanguageCount</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-130"><em>Player6</em>. <strong>Ауторевинд</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-130"><em>Player6</em>.<strong>AutoRewind</strong></span></span></td>
<td><span data-ttu-id="bc60d-131">Используйте <em>элементы управления</em>. <strong>CurrentPosition</strong> в скрипте для указания или получения текущей позицией.</span><span class="sxs-lookup"><span data-stu-id="bc60d-131">Use <em>Controls</em>.<strong>currentPosition</strong> in script to specify or retrieve the current position.</span></span> <span data-ttu-id="bc60d-132">Кроме того, можно использовать маркеры и <em>проигрыватель</em>. событие <strong>маркерхит</strong> .</span><span class="sxs-lookup"><span data-stu-id="bc60d-132">Alternatively, use markers and the <em>Player</em>.<strong>markerHit</strong> event.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-133"><em>Player6</em>. <strong>Автоподбор размеров</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-133"><em>Player6</em>.<strong>AutoSize</strong></span></span></td>
<td><span data-ttu-id="bc60d-134">Поведение по умолчанию — автоматическое изменение размера.</span><span class="sxs-lookup"><span data-stu-id="bc60d-134">Automatic sizing is the default behavior.</span></span> <span data-ttu-id="bc60d-135">Чтобы переопределить автоматическое изменение размера, задайте свойства Height и Width в <OBJECT> теге или в скрипте.</span><span class="sxs-lookup"><span data-stu-id="bc60d-135">To override automatic sizing, set the height and width properties in the <OBJECT> tag or in script.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-136"><em>Player6</em>. <strong>Автозапуск</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-136"><em>Player6</em>.<strong>AutoStart</strong></span></span></td>
<td><span data-ttu-id="bc60d-137">Используйте <em>Параметры</em>. <strong>Автозапуск</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-137">Use <em>Settings</em>.<strong>autoStart</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-138"><em>Player6</em>. <strong>Сбалансировать</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-138"><em>Player6</em>.<strong>Balance</strong></span></span></td>
<td><span data-ttu-id="bc60d-139">Используйте <em>Параметры</em>. <strong>баланс</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-139">Use <em>Settings</em>.<strong>balance</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-140"><em>Player6</em>. <strong>Пропускная способность</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-140"><em>Player6</em>.<strong>Bandwidth</strong></span></span></td>
<td><span data-ttu-id="bc60d-141">Использовать <em>сеть</em>. <strong>пропускная способность</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-141">Use <em>Network</em>.<strong>bandWidth</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-142"><em>Player6</em>. <strong>BaseURL</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-142"><em>Player6</em>.<strong>BaseURL</strong></span></span></td>
<td><span data-ttu-id="bc60d-143">Используйте <em>Параметры</em>. <strong>baseURL</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-143">Use <em>Settings</em>.<strong>baseURL</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-144"><em>Player6</em>. <strong>Буфферингкаунт</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-144"><em>Player6</em>.<strong>BufferingCount</strong></span></span></td>
<td><span data-ttu-id="bc60d-145">Использовать <em>сеть.</em> <strong>буфферингкаунт</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-145">Use <em>Network.</em><strong>bufferingCount</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-146"><em>Player6</em>. <strong>Буфферингпрогресс</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-146"><em>Player6</em>.<strong>BufferingProgress</strong></span></span></td>
<td><span data-ttu-id="bc60d-147">Использовать <em>сеть</em>. <strong>буфферингпрогресс</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-147">Use <em>Network</em>.<strong>bufferingProgress</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-148"><em>Player6</em>. <strong>Буфферингтиме</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-148"><em>Player6</em>.<strong>BufferingTime</strong></span></span></td>
<td><span data-ttu-id="bc60d-149">Использовать <em>сеть</em>. <strong>буфферингтиме</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-149">Use <em>Network</em>.<strong>bufferingTime</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-150"><em>Player6</em>. <strong>Буттонсаваилабле</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-150"><em>Player6</em>.<strong>ButtonsAvailable</strong></span></span></td>
<td><span data-ttu-id="bc60d-151">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-151">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-152"><em>Player6</em>. <strong>Канпревиев</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-152"><em>Player6</em>.<strong>CanPreview</strong></span></span></td>
<td><span data-ttu-id="bc60d-153">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-153">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-154"><em>Player6</em>. <strong>Канскан</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-154"><em>Player6</em>.<strong>CanScan</strong></span></span></td>
<td><span data-ttu-id="bc60d-155">Используйте <em>элементы управления</em>. <strong>Available</strong>( &quot; Фастфорвард &quot; ) и <em>Controls</em>.<strong> Доступно</strong>( &quot; фастреверсе &quot; ).</span><span class="sxs-lookup"><span data-stu-id="bc60d-155">Use <em>Controls</em>.<strong>isAvailable</strong>(&quot;FastForward&quot;) and <em>Controls</em>.<strong>isAvailable</strong>(&quot;FastReverse&quot;).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-156"><em>Player6</em>. <strong>CanSeek</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-156"><em>Player6</em>.<strong>CanSeek</strong></span></span></td>
<td><span data-ttu-id="bc60d-157">Используйте <em>элементы управления</em>. <strong>доступно</strong> для проверки возможности выполнения конкретного метода Seek.</span><span class="sxs-lookup"><span data-stu-id="bc60d-157">Use <em>Controls</em>.<strong>isAvailable</strong> to test whether a particular seek method can be performed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-158"><em>Player6</em>. <strong>Кансиктомаркерс</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-158"><em>Player6</em>.<strong>CanSeekToMarkers</strong></span></span></td>
<td><span data-ttu-id="bc60d-159">Используйте <em>элементы управления</em>. <strong>доступно</strong>( &quot; куррентмаркер &quot; ).</span><span class="sxs-lookup"><span data-stu-id="bc60d-159">Use <em>Controls</em>.<strong>isAvailable</strong>(&quot;CurrentMarker&quot;).</span></span> <span data-ttu-id="bc60d-160">Используйте <em>носитель</em>. <strong>маркеркаунт</strong> для получения числа маркеров в определенном элементе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="bc60d-160">Use <em>Media</em>.<strong>markerCount</strong> to retrieve the count of markers in a particular media item.</span></span> <span data-ttu-id="bc60d-161">Используйте <em>элементы управления</em>. <strong>куррентмаркер</strong> , чтобы указать или получить номер текущего маркера.</span><span class="sxs-lookup"><span data-stu-id="bc60d-161">Use <em>Controls</em>.<strong>currentMarker</strong> to specify or retrieve the current marker number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-162"><em>Player6</em>. <strong>Каптионингид</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-162"><em>Player6</em>.<strong>CaptioningID</strong></span></span></td>
<td><span data-ttu-id="bc60d-163">Используйте <em>клоседкаптион</em>. <strong>каптионингид</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-163">Use <em>ClosedCaption</em>.<strong>captioningID</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-164"><em>Player6</em>. <strong>Ккактиве</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-164"><em>Player6</em>.<strong>CCActive</strong></span></span></td>
<td><span data-ttu-id="bc60d-165">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-165">Not available.</span></span> <span data-ttu-id="bc60d-166">Дополнительные сведения об изменении субтитров в проигрывателе Windows Media см. в разделе <a href="closed-captioning.md">Скрытые титры</a> .</span><span class="sxs-lookup"><span data-stu-id="bc60d-166">See <a href="closed-captioning.md">Closed Captioning</a> for information about how closed captioning has changed in Windows Media Player.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-167"><em>Player6</em>. <strong>ChannelDescription</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-167"><em>Player6</em>.<strong>ChannelDescription</strong></span></span></td>
<td><span data-ttu-id="bc60d-168">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-168">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-169"><em>Player6</em>. <strong>ChannelName</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-169"><em>Player6</em>.<strong>ChannelName</strong></span></span></td>
<td><span data-ttu-id="bc60d-170">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-170">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-171"><em>Player6</em>. <strong>Чаннелурл</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-171"><em>Player6</em>.<strong>ChannelURL</strong></span></span></td>
<td><span data-ttu-id="bc60d-172">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-172">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-173"><em>Player6</em>. <strong>Кликктоплай</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-173"><em>Player6</em>.<strong>ClickToPlay</strong></span></span></td>
<td><span data-ttu-id="bc60d-174">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-174">Not available.</span></span> <span data-ttu-id="bc60d-175">Для запуска воспроизведения необходимо предоставить элементы управления в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="bc60d-175">You should provide controls in your user interface to start playback.</span></span> <span data-ttu-id="bc60d-176">Кроме того, пользователь может щелкнуть изображение видео правой кнопкой мыши, чтобы открыть всплывающее меню, содержащее выбор <strong>воспроизведения и паузы</strong> при открытии <em>проигрывателя</em>. <strong>енаблеконтекстмену</strong> имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="bc60d-176">Alternatively, the user can right-click the video image to open a pop-up menu that contains a <strong>Play/Pause</strong> selection if <em>Player</em>.<strong>enableContextMenu</strong> equals true.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-177"><em>Player6</em>. <strong>ClientID</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-177"><em>Player6</em>.<strong>ClientID</strong></span></span></td>
<td><span data-ttu-id="bc60d-178">Недоступно. Проигрыватель Windows Media 9 Series или более поздней версии позволяет пользователю выбрать, следует ли передавать уникальный идентификатор проигрывателя поставщикам содержимого.</span><span class="sxs-lookup"><span data-stu-id="bc60d-178">Not available.Windows Media Player 9 Series or later allows the user to select whether a unique Player ID is transmitted to content providers.</span></span><br/> <span data-ttu-id="bc60d-179">Если пользователь выбирает этот параметр, проигрыватель отправляет уникальный идентификатор на сервер Windows Media.</span><span class="sxs-lookup"><span data-stu-id="bc60d-179">If the user selects this option, the Player sends a unique ID to the Windows Media server.</span></span> <span data-ttu-id="bc60d-180">Идентификатор заносится в файл журнала сервера, расположенный в папке. папка <em>system32\logfiles</em> по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bc60d-180">The ID is logged in the server's log file, located in the ..<em>system32\logfiles</em> folder by default.</span></span> <span data-ttu-id="bc60d-181">Имя поля журнала — &quot; c-плайерид &quot; .</span><span class="sxs-lookup"><span data-stu-id="bc60d-181">The log field name is &quot;c-playerid&quot;.</span></span> <span data-ttu-id="bc60d-182">Ведение журнала сервера не включено по умолчанию в службах Windows Media.</span><span class="sxs-lookup"><span data-stu-id="bc60d-182">Server logging is not enabled by default in Windows Media Services.</span></span><br/> <span data-ttu-id="bc60d-183">Если пользователь не выбирает этот параметр, сервер создает случайный идентификатор сеанса, уникальный для каждого клиента в данном сеансе.</span><span class="sxs-lookup"><span data-stu-id="bc60d-183">If the user does not select this option, the server generates a random session ID, which is unique for each client for a given session.</span></span><br/> <span data-ttu-id="bc60d-184">Дополнительные сведения см. в документации по сериям Windows Media Services 9.</span><span class="sxs-lookup"><span data-stu-id="bc60d-184">For more information, see the Windows Media Services 9 Series documentation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-185"><em>Player6</em>. <strong>Кодеккаунт</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-185"><em>Player6</em>.<strong>CodecCount</strong></span></span></td>
<td><span data-ttu-id="bc60d-186">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-186">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-187"><em>Player6</em>. <strong>ColorKey</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-187"><em>Player6</em>.<strong>ColorKey</strong></span></span></td>
<td><span data-ttu-id="bc60d-188">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-188">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-189"><em>Player6</em>. <strong>Коннектионспид</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-189"><em>Player6</em>.<strong>ConnectionSpeed</strong></span></span></td>
<td><span data-ttu-id="bc60d-190">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-190">Not available.</span></span> <span data-ttu-id="bc60d-191">Использовать <em>сеть</em>. <strong>скорость</strong> для определения текущей скорости.</span><span class="sxs-lookup"><span data-stu-id="bc60d-191">Use <em>Network</em>.<strong>bitRate</strong> to determine the current bit rate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-192"><em>Player6</em>. <strong>Контактаддресс</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-192"><em>Player6</em>.<strong>ContactAddress</strong></span></span></td>
<td><span data-ttu-id="bc60d-193">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-193">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-194"><em>Player6</em>. <strong>Контактемаил</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-194"><em>Player6</em>.<strong>ContactEmail</strong></span></span></td>
<td><span data-ttu-id="bc60d-195">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-195">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-196"><em>Player6</em>. <strong>Контактфоне</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-196"><em>Player6</em>.<strong>ContactPhone</strong></span></span></td>
<td><span data-ttu-id="bc60d-197">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-197">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-198"><em>Player6</em>. <strong>CreationDate</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-198"><em>Player6</em>.<strong>CreationDate</strong></span></span></td>
<td><span data-ttu-id="bc60d-199">Используйте <em>медиаколлектион</em>. <strong>жетмедиаатом</strong>( &quot; CreationDate &quot; ) для получения индекса Atom даты создания.</span><span class="sxs-lookup"><span data-stu-id="bc60d-199">Use <em>MediaCollection</em>.<strong>getMediaAtom</strong>(&quot;CreationDate&quot;) to retrieve the index of the creation date atom.</span></span> <span data-ttu-id="bc60d-200">Используйте <em>носитель</em>. <strong>жетитеминфобятом</strong> получить метаданные.</span><span class="sxs-lookup"><span data-stu-id="bc60d-200">Use <em>Media</em>.<strong>getItemInfoByAtom</strong> to retrieve the metadata.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-201"><em>Player6</em>. <strong>Куррентангле</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-201"><em>Player6</em>.<strong>CurrentAngle</strong></span></span></td>
<td><span data-ttu-id="bc60d-202">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-202">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-203"><em>Player6</em>. <strong>Куррентаудиостреам</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-203"><em>Player6</em>.<strong>CurrentAudioStream</strong></span></span></td>
<td><span data-ttu-id="bc60d-204">Используйте <em>элементы управления</em>. <strong>куррентаудиолангуажеиндекс</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-204">Use <em>Controls</em>.<strong>currentAudioLanguageIndex</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-205"><em>Player6</em>. <strong>Куррентбуттон</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-205"><em>Player6</em>.<strong>CurrentButton</strong></span></span></td>
<td><span data-ttu-id="bc60d-206">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-206">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-207"><em>Player6</em>. <strong>Курренткксервице</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-207"><em>Player6</em>.<strong>CurrentCCService</strong></span></span></td>
<td><span data-ttu-id="bc60d-208">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-208">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-209"><em>Player6</em>. <strong>Куррентчаптер</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-209"><em>Player6</em>.<strong>CurrentChapter</strong></span></span></td>
<td><span data-ttu-id="bc60d-210">Получение текущего списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="bc60d-210">Retrieve the current playlist.</span></span> <span data-ttu-id="bc60d-211">Если текущий список воспроизведения не совпадает с списком воспроизведения, возвращенным <em>CDROM</em>. <strong>списка воспроизведения</strong>нет текущей главы.</span><span class="sxs-lookup"><span data-stu-id="bc60d-211">If the current playlist is not the same one as the playlist returned by <em>Cdrom</em>.<strong>playlist</strong>, then there is no current chapter.</span></span> <span data-ttu-id="bc60d-212">В противном случае текущий номер главы — это индекс текущего носителя в текущем списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="bc60d-212">Otherwise, the current chapter number is the index of the current media in the current playlist.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-213"><em>Player6</em>. <strong>Куррентдисксиде</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-213"><em>Player6</em>.<strong>CurrentDiscSide</strong></span></span></td>
<td><span data-ttu-id="bc60d-214">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-214">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-215"><em>Player6</em>. <strong>CurrentDomain</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-215"><em>Player6</em>.<strong>CurrentDomain</strong></span></span></td>
<td><span data-ttu-id="bc60d-216">Используйте <em>DVD-диск</em>. <strong>домен</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-216">Use <em>DVD</em>.<strong>domain</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-217"><em>Player6</em>. <strong>Куррентмаркер</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-217"><em>Player6</em>.<strong>CurrentMarker</strong></span></span></td>
<td><span data-ttu-id="bc60d-218">Используйте <em>элементы управления</em>. <strong>куррентмаркер</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-218">Use <em>Controls</em>.<strong>currentMarker</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-219"><em>Player6</em>. <strong>CurrentPosition</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-219"><em>Player6</em>.<strong>CurrentPosition</strong></span></span></td>
<td><span data-ttu-id="bc60d-220">Используйте <em>элементы управления</em>. <strong>CurrentPosition</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-220">Use <em>Controls</em>.<strong>currentPosition</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-221"><em>Player6</em>. <strong>Куррентсубпиктурестреам</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-221"><em>Player6</em>.<strong>CurrentSubpictureStream</strong></span></span></td>
<td><span data-ttu-id="bc60d-222">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-222">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-223"><em>Player6</em>. <strong>CurrentTime</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-223"><em>Player6</em>.<strong>CurrentTime</strong></span></span></td>
<td><span data-ttu-id="bc60d-224">Используйте <em>элементы управления</em>. <strong>куррентпоситионтимекоде</strong>, <em>элементы управления</em>. <strong>куррентпоситионстринг</strong>или <em>элементы управления</em>. <strong>CurrentPosition.</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-224">Use <em>Controls</em>.<strong>currentPositionTimeCode</strong>, <em>Controls</em>.<strong>currentPositionString</strong>, or <em>Controls</em>.<strong>currentPosition.</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-225"><em>Player6</em>. <strong>Курренттитле</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-225"><em>Player6</em>.<strong>CurrentTitle</strong></span></span></td>
<td><span data-ttu-id="bc60d-226">Получение текущего списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="bc60d-226">Retrieve the current playlist.</span></span> <span data-ttu-id="bc60d-227">Если текущий список воспроизведения совпадает с списком воспроизведения, возвращенным <em>CDROM</em>. <strong>список воспроизведения</strong>, а номер заголовка — это индекс текущего носителя в текущем списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="bc60d-227">If the current playlist is the same one as the playlist returned by <em>Cdrom</em>.<strong>playlist</strong>, then the title number is the index of the current media in the current playlist.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-228"><em>Player6</em>. <strong>Куррентволуме</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-228"><em>Player6</em>.<strong>CurrentVolume</strong></span></span></td>
<td><span data-ttu-id="bc60d-229">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-229">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-230"><em>Player6</em>. <strong>Примеры CursorType</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-230"><em>Player6</em>.<strong>CursorType</strong></span></span></td>
<td><span data-ttu-id="bc60d-231">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-231">Not available.</span></span> <span data-ttu-id="bc60d-232">Вместо этого используйте стили Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="bc60d-232">Use Internet Explorer styles instead.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-233"><em>Player6</em>. <strong>Дефаултфраме</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-233"><em>Player6</em>.<strong>DefaultFrame</strong></span></span></td>
<td><span data-ttu-id="bc60d-234">Используйте <em>Параметры</em>. <strong>дефаултфраме</strong>или используйте</span><span class="sxs-lookup"><span data-stu-id="bc60d-234">Use <em>Settings</em>.<strong>defaultFrame</strong>, or use a</span></span> <PARAM> <span data-ttu-id="bc60d-235">атрибут в <OBJECT> элементе: <pre data-space="preserve"><code><PARAM NAME=&quot;defaultFrame&quot; VALUE=&quot;right&quot;></code></pre></span><span class="sxs-lookup"><span data-stu-id="bc60d-235">attribute in the <OBJECT> element: <pre data-space="preserve"><code><PARAM NAME=&quot;defaultFrame&quot; VALUE=&quot;right&quot;></code></pre></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-236"><em>Player6</em>. <strong>Дисплайбаккколор</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-236"><em>Player6</em>.<strong>DisplayBackColor</strong></span></span></td>
<td><span data-ttu-id="bc60d-237">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-237">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-238"><em>Player6</em>. <strong>Дисплайфореколор</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-238"><em>Player6</em>.<strong>DisplayForeColor</strong></span></span></td>
<td><span data-ttu-id="bc60d-239">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-239">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-240"><em>Player6</em>. <strong>DisplayMode</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-240"><em>Player6</em>.<strong>DisplayMode</strong></span></span></td>
<td><span data-ttu-id="bc60d-241">Текущую точку можно получить в секундах с начала в виде <strong>числа</strong> с помощью <em>элементов управления</em>. <strong>CurrentPosition</strong>в виде <strong>строки</strong> в формате чч: мм: СС (часы, минуты, секунды) с помощью <em>элементов управления</em>. <strong>куррентпоситионстринг</strong>или в формате кода времени с помощью <em>элементов управления</em>. <strong>куррентпоситионтимекоде</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-241">The current position can be retrieved in seconds from the beginning as a <strong>Number</strong> using <em>Controls</em>.<strong>currentPosition</strong>, as a <strong>String</strong> formatted as HH:MM:SS (hours, minutes, seconds) using <em>Controls</em>.<strong>currentPositionString</strong>, or in time code format using <em>Controls</em>.<strong>currentPositionTimeCode</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-242"><em>Player6</em>. <strong>Дисплайсизе</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-242"><em>Player6</em>.<strong>DisplaySize</strong></span></span></td>
<td><span data-ttu-id="bc60d-243">Изображение по умолчанию автоматически изменяется в соответствии с размером носителя.</span><span class="sxs-lookup"><span data-stu-id="bc60d-243">The default display automatically resizes to fit the media.</span></span> <span data-ttu-id="bc60d-244">Можно задать свойства Height и Width в <OBJECT> теге или в скрипте.</span><span class="sxs-lookup"><span data-stu-id="bc60d-244">You can set the height and width properties in the <OBJECT> tag, or in script.</span></span> <span data-ttu-id="bc60d-245">Используйте <em>проигрыватель</em>. <strong>полноэкранный</strong> режим, переключаясь в весь экран.</span><span class="sxs-lookup"><span data-stu-id="bc60d-245">Use <em>Player</em>.<strong>fullScreen</strong> to switch to full-screen mode.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-246"><em>Player6</em>. <strong>Длительность</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-246"><em>Player6</em>.<strong>Duration</strong></span></span></td>
<td><span data-ttu-id="bc60d-247">Используйте <em>носитель</em>. <strong>Длительность</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-247">Use <em>Media</em>.<strong>duration</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-248"><em>Player6</em>. <strong>DVD-диск</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-248"><em>Player6</em>.<strong>DVD</strong></span></span></td>
<td><span data-ttu-id="bc60d-249">Используйте <em>проигрыватель</em>. <strong>DVD-диск</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-249">Use <em>Player</em>.<strong>DVD</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-250"><em>Player6</em>. <strong>Енаблеконтекстмену</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-250"><em>Player6</em>.<strong>EnableContextMenu</strong></span></span></td>
<td><span data-ttu-id="bc60d-251">Используйте <em>проигрыватель</em>. <strong>енаблеконтекстмену</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-251">Use <em>Player</em>.<strong>enableContextMenu</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-252"><em>Player6</em>. <strong>Включено</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-252"><em>Player6</em>.<strong>Enabled</strong></span></span></td>
<td><span data-ttu-id="bc60d-253">Используйте <em>проигрыватель</em>. <strong>включено</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-253">Use <em>Player</em>.<strong>enabled</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-254"><em>Player6</em>. <strong>Енаблефуллскринконтролс</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-254"><em>Player6</em>.<strong>EnableFullScreenControls</strong></span></span></td>
<td><span data-ttu-id="bc60d-255">При использовании проигрывателя Windows Media 9 Series или более поздних версий элементы управления для полноэкранного режима включаются автоматически, если <em>проигрыватель</em>не используется. <strong></strong>  =  uiMode &quot; нет &quot; .</span><span class="sxs-lookup"><span data-stu-id="bc60d-255">When using Windows Media Player 9 Series or later, full-screen controls are enabled automatically unless <em>Player</em>.<strong>uiMode</strong> = &quot;none&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-256"><em>Player6</em>. <strong>Енаблепоситионконтролс</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-256"><em>Player6</em>.<strong>EnablePositionControls</strong></span></span></td>
<td><span data-ttu-id="bc60d-257">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-257">Not available.</span></span> <span data-ttu-id="bc60d-258">Вы можете предоставить настраиваемые элементы управления или использовать <em>проигрыватель</em>. <strong>UIMODE</strong> , чтобы выбрать конфигурацию по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bc60d-258">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-259"><em>Player6</em>. <strong>Енаблетраккер</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-259"><em>Player6</em>.<strong>EnableTracker</strong></span></span></td>
<td><span data-ttu-id="bc60d-260">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-260">Not available.</span></span> <span data-ttu-id="bc60d-261">Вы можете предоставить пользовательский элемент управления или использовать <em>проигрыватель</em>. <strong>UIMODE</strong> , чтобы выбрать конфигурацию по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bc60d-261">You can provide a custom control or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-262"><em>Player6</em>. <strong>Ентрикаунт</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-262"><em>Player6</em>.<strong>EntryCount</strong></span></span></td>
<td><span data-ttu-id="bc60d-263">Использовать <em>список воспроизведения</em>. <strong>количество</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-263">Use <em>Playlist</em>.<strong>count</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-264"><em>Player6</em>. <strong>Код ошибки</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-264"><em>Player6</em>.<strong>ErrorCode</strong></span></span></td>
<td><span data-ttu-id="bc60d-265">Используйте <em>ерроритем</em>. <strong>код ошибки</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-265">Use <em>ErrorItem</em>.<strong>errorCode</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-266"><em>Player6</em>. <strong>Ерроркорректион</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-266"><em>Player6</em>.<strong>ErrorCorrection</strong></span></span></td>
<td><span data-ttu-id="bc60d-267">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-267">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-268"><em>Player6</em>. <strong>ErrorDescription</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-268"><em>Player6</em>.<strong>ErrorDescription</strong></span></span></td>
<td><span data-ttu-id="bc60d-269">Используйте <em>ерроритем</em>. <strong>errorDescription</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-269">Use <em>ErrorItem</em>.<strong>errorDescription</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-270"><em>Player6</em>. <strong>Имя файла</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-270"><em>Player6</em>.<strong>FileName</strong></span></span></td>
<td><span data-ttu-id="bc60d-271">Используйте <em>проигрыватель</em>. <strong>URL-адрес</strong> или <em>проигрыватель</em>. <strong>куррентмедиа</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-271">Use <em>Player</em>.<strong>URL</strong> or <em>Player</em>.<strong>currentMedia</strong>.</span></span> <span data-ttu-id="bc60d-272">Используйте <em>элементы управления</em>. <strong>currentItem</strong> при работе в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="bc60d-272">Use <em>Controls</em>.<strong>currentItem</strong> when working within a playlist.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-273"><em>Player6</em>. <strong>Фрамесперсеконд</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-273"><em>Player6</em>.<strong>FramesPerSecond</strong></span></span></td>
<td><span data-ttu-id="bc60d-274">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-274">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-275"><em>Player6</em>. <strong>HasError</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-275"><em>Player6</em>.<strong>HasError</strong></span></span></td>
<td><span data-ttu-id="bc60d-276">Использовать <em>ошибку</em>. <strong>ерроркаунт</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-276">Use <em>Error</em>.<strong>errorCount</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-277"><em>Player6</em>. <strong>Хасмултиплеитемс</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-277"><em>Player6</em>.<strong>HasMultipleItems</strong></span></span></td>
<td><span data-ttu-id="bc60d-278">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-278">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-279"><em>Player6</em>. <strong>Имажесаурцехеигхт</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-279"><em>Player6</em>.<strong>ImageSourceHeight</strong></span></span></td>
<td><span data-ttu-id="bc60d-280">Используйте <em>носитель</em>. <strong>имажесаурцехеигхт</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-280">Use <em>Media</em>.<strong>imageSourceHeight</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-281"><em>Player6</em>. <strong>Имажесаурцевидс</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-281"><em>Player6</em>.<strong>ImageSourceWidth</strong></span></span></td>
<td><span data-ttu-id="bc60d-282">Используйте <em>носитель</em>. <strong>имажесаурцевидс</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-282">Use <em>Media</em>.<strong>imageSourceWidth</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-283"><em>Player6</em>. <strong>Инвокеурлс</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-283"><em>Player6</em>.<strong>InvokeURLs</strong></span></span></td>
<td><span data-ttu-id="bc60d-284">Используйте <em>Параметры</em>. <strong>инвокеурлс</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-284">Use <em>Settings</em>.<strong>invokeURLs</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-285"><em>Player6</em>. <strong>Трансляция</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-285"><em>Player6</em>.<strong>IsBroadcast</strong></span></span></td>
<td><span data-ttu-id="bc60d-286">Использовать <em>сеть</em>. <strong>саурцепротокол</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-286">Use <em>Network</em>.<strong>sourceProtocol</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-287"><em>Player6</em>. <strong>Исдуратионвалид</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-287"><em>Player6</em>.<strong>IsDurationValid</strong></span></span></td>
<td><span data-ttu-id="bc60d-288">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-288">Not available.</span></span> <span data-ttu-id="bc60d-289"><em>Носитель</em>. параметр <strong>Duration</strong> содержит допустимое значение при использовании с текущим объектом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="bc60d-289"><em>Media</em>.<strong>duration</strong> contains a valid value when used with the current media object.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-290"><em>Player6</em>. <strong>Языковая</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-290"><em>Player6</em>.<strong>Language</strong></span></span></td>
<td><span data-ttu-id="bc60d-291">Используйте <em>элементы управления</em>. <strong>куррентаудиолангуаже</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-291">Use <em>Controls</em>.<strong>currentAudioLanguage</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-292"><em>Player6</em>. <strong>Лостпаккетс</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-292"><em>Player6</em>.<strong>LostPackets</strong></span></span></td>
<td><span data-ttu-id="bc60d-293">Использовать <em>сеть</em>. <strong>лостпаккетс</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-293">Use <em>Network</em>.<strong>lostPackets</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-294"><em>Player6</em>. <strong>Маркеркаунт</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-294"><em>Player6</em>.<strong>MarkerCount</strong></span></span></td>
<td><span data-ttu-id="bc60d-295">Используйте <em>носитель</em>. <strong>маркеркаунт</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-295">Use <em>Media</em>.<strong>markerCount</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-296"><em>Player6</em>. <strong>Отключить звук</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-296"><em>Player6</em>.<strong>Mute</strong></span></span></td>
<td><span data-ttu-id="bc60d-297">Используйте <em>Параметры</em>. <strong>Отключить звук</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-297">Use <em>Settings</em>.<strong>mute</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-298"><em>Player6</em>. <strong>Опенстате</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-298"><em>Player6</em>.<strong>OpenState</strong></span></span></td>
<td><span data-ttu-id="bc60d-299">Используйте <em>проигрыватель</em>. <strong>опенстате</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-299">Use <em>Player</em>.<strong>openState</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-300"><em>Player6</em>. <strong>Плайкаунт</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-300"><em>Player6</em>.<strong>PlayCount</strong></span></span></td>
<td><span data-ttu-id="bc60d-301">Используйте <em>Параметры</em>. <strong>плайкаунт</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-301">Use <em>Settings</em>.<strong>playCount</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-302"><em>Player6</em>. <strong>Плайстате</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-302"><em>Player6</em>.<strong>PlayState</strong></span></span></td>
<td><span data-ttu-id="bc60d-303">Используйте <em>проигрыватель</em>. <strong>плайстате</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-303">Use <em>Player</em>.<strong>playState</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-304"><em>Player6</em>. <strong>PreviewMode</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-304"><em>Player6</em>.<strong>PreviewMode</strong></span></span></td>
<td><span data-ttu-id="bc60d-305">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-305">Not available.</span></span> <span data-ttu-id="bc60d-306">Используйте структуру цикла скриптов с таймером HTML для дублирования этой функции.</span><span class="sxs-lookup"><span data-stu-id="bc60d-306">Use a script loop structure with an HTML timer to duplicate this functionality.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-307"><em>Player6</em>. <strong>Скорость передачи</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-307"><em>Player6</em>.<strong>Rate</strong></span></span></td>
<td><span data-ttu-id="bc60d-308">Используйте <em>Параметры</em>. <strong>ставка</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-308">Use <em>Settings</em>.<strong>rate</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-309"><em>Player6</em>. <strong>ReadyState</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-309"><em>Player6</em>.<strong>ReadyState</strong></span></span></td>
<td><span data-ttu-id="bc60d-310">Используйте <em>проигрыватель</em>. <strong>опенстате</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-310">Use <em>Player</em>.<strong>openState</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-311"><em>Player6</em>. <strong>Рецеиведпаккетс</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-311"><em>Player6</em>.<strong>ReceivedPackets</strong></span></span></td>
<td><span data-ttu-id="bc60d-312">Использовать <em>сеть</em>. <strong>рецеиведпаккетс</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-312">Use <em>Network</em>.<strong>receivedPackets</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-313"><em>Player6</em>. <strong>Рецептионкуалити</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-313"><em>Player6</em>.<strong>ReceptionQuality</strong></span></span></td>
<td><span data-ttu-id="bc60d-314">Использовать <em>сеть</em>. <strong>рецептионкуалити</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-314">Use <em>Network</em>.<strong>receptionQuality</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-315"><em>Player6</em>. <strong>Рековередпаккетс</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-315"><em>Player6</em>.<strong>RecoveredPackets</strong></span></span></td>
<td><span data-ttu-id="bc60d-316">Использовать <em>сеть</em>. <strong>рековередпаккетс</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-316">Use <em>Network</em>.<strong>recoveredPackets</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-317"><em>Player6</em>. <strong>Корневая папка</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-317"><em>Player6</em>.<strong>Root</strong></span></span></td>
<td><span data-ttu-id="bc60d-318">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-318">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-319"><em>Player6</em>. <strong>Самифиленаме</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-319"><em>Player6</em>.<strong>SAMIFileName</strong></span></span></td>
<td><span data-ttu-id="bc60d-320">Используйте <em>клоседкаптион</em>. <strong>Самифиленаме</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-320">Use <em>ClosedCaption</em>.<strong>SAMIFileName</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-321"><em>Player6</em>. <strong>Самиланг</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-321"><em>Player6</em>.<strong>SAMILang</strong></span></span></td>
<td><span data-ttu-id="bc60d-322">Используйте <em>клоседкаптион</em>. <strong>Самиланг</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-322">Use <em>ClosedCaption</em>.<strong>SAMILang</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-323"><em>Player6</em>. <strong>Самистиле</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-323"><em>Player6</em>.<strong>SAMIStyle</strong></span></span></td>
<td><span data-ttu-id="bc60d-324">Используйте <em>клоседкаптион</em>. <strong>Самистиле</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-324">Use <em>ClosedCaption</em>.<strong>SAMIStyle</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-325"><em>Player6</em>. <strong>Селектионенд</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-325"><em>Player6</em>.<strong>SelectionEnd</strong></span></span></td>
<td><span data-ttu-id="bc60d-326">Используйте <em>носитель</em>. <strong>Длительность</strong> для определения длины объекта <strong>мультимедиа</strong> .</span><span class="sxs-lookup"><span data-stu-id="bc60d-326">Use <em>Media</em>.<strong>duration</strong> to determine the length of a <strong>Media</strong> object.</span></span> <span data-ttu-id="bc60d-327">Используйте маркер с <em>элементами управления</em>. <strong>куррентмаркер</strong> , чтобы указать пользовательскую конечную точку.</span><span class="sxs-lookup"><span data-stu-id="bc60d-327">Use a marker with <em>Controls</em>.<strong>currentMarker</strong> to specify a custom end position.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-328"><em>Player6</em>. <strong>Селектионстарт</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-328"><em>Player6</em>.<strong>SelectionStart</strong></span></span></td>
<td><span data-ttu-id="bc60d-329">Используйте <em>элементы управления</em>. <strong>CurrentPosition</strong> , чтобы начать воспроизведение из определенной должности или использовать маркер с <em>элементами управления</em>. <strong>куррентмаркер</strong> , чтобы указать пользовательскую начальную точку.</span><span class="sxs-lookup"><span data-stu-id="bc60d-329">Use <em>Controls</em>.<strong>currentPosition</strong> to start playback from a particular position or use a marker with <em>Controls</em>.<strong>currentMarker</strong> to specify a custom start position.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-330"><em>Player6</em>. <strong>Сендерроревентс</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-330"><em>Player6</em>.<strong>SendErrorEvents</strong></span></span></td>
<td><span data-ttu-id="bc60d-331">Ошибки помещаются в очередь.</span><span class="sxs-lookup"><span data-stu-id="bc60d-331">Errors are queued.</span></span> <span data-ttu-id="bc60d-332">Для получения сведений об ошибке используйте объект <strong>Error</strong> и объект <strong>ерроритем</strong> .</span><span class="sxs-lookup"><span data-stu-id="bc60d-332">Use the <strong>Error</strong> object and the <strong>ErrorItem</strong> object to retrieve error information.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-333"><em>Player6</em>. <strong>Сендкэйбоардевентс</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-333"><em>Player6</em>.<strong>SendKeyboardEvents</strong></span></span></td>
<td><span data-ttu-id="bc60d-334">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-334">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-335"><em>Player6</em>. <strong>Сендмаусекликкевентс</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-335"><em>Player6</em>.<strong>SendMouseClickEvents</strong></span></span></td>
<td><span data-ttu-id="bc60d-336">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-336">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-337"><em>Player6</em>. <strong>Сендмаусемовивентс</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-337"><em>Player6</em>.<strong>SendMouseMoveEvents</strong></span></span></td>
<td><span data-ttu-id="bc60d-338">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-338">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-339"><em>Player6</em>. <strong>Сендопенстатечанжеевентс</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-339"><em>Player6</em>.<strong>SendOpenStateChangeEvents</strong></span></span></td>
<td><span data-ttu-id="bc60d-340">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-340">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-341"><em>Player6</em>. <strong>Сендплайстатечанжеевентс</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-341"><em>Player6</em>.<strong>SendPlayStateChangeEvents</strong></span></span></td>
<td><span data-ttu-id="bc60d-342">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-342">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-343"><em>Player6</em>. <strong>Сендварнинжевентс</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-343"><em>Player6</em>.<strong>SendWarningEvents</strong></span></span></td>
<td><span data-ttu-id="bc60d-344">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-344">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-345"><em>Player6</em>. <strong>Шоваудиоконтролс</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-345"><em>Player6</em>.<strong>ShowAudioControls</strong></span></span></td>
<td><span data-ttu-id="bc60d-346">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-346">Not available.</span></span> <span data-ttu-id="bc60d-347">Вы можете предоставить настраиваемые элементы управления или использовать <em>проигрыватель</em>. <strong>UIMODE</strong> , чтобы выбрать конфигурацию по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bc60d-347">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-348"><em>Player6</em>. <strong>Шовкаптионинг</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-348"><em>Player6</em>.<strong>ShowCaptioning</strong></span></span></td>
<td><span data-ttu-id="bc60d-349">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-349">Not available.</span></span> <span data-ttu-id="bc60d-350">Можно задать пользовательский вывод закрытого заголовка.</span><span class="sxs-lookup"><span data-stu-id="bc60d-350">You can provide a custom closed caption display.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-351"><em>Player6</em>. <strong>Шовконтролс</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-351"><em>Player6</em>.<strong>ShowControls</strong></span></span></td>
<td><span data-ttu-id="bc60d-352">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-352">Not available.</span></span> <span data-ttu-id="bc60d-353">Вы можете предоставить настраиваемые элементы управления или использовать <em>проигрыватель</em>. <strong>UIMODE</strong> , чтобы выбрать конфигурацию по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bc60d-353">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-354"><em>Player6</em>. <strong>Шовдисплай</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-354"><em>Player6</em>.<strong>ShowDisplay</strong></span></span></td>
<td><span data-ttu-id="bc60d-355">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-355">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-356"><em>Player6</em>. <strong>Шовготобар</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-356"><em>Player6</em>.<strong>ShowGotoBar</strong></span></span></td>
<td><span data-ttu-id="bc60d-357">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-357">Not available.</span></span> <span data-ttu-id="bc60d-358">С помощью объекта мультимедиа можно предоставить пользовательские функции.</span><span class="sxs-lookup"><span data-stu-id="bc60d-358">You can provide custom functionality using the Media object</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-359"><em>Player6</em>. <strong>Шовпоситионконтролс</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-359"><em>Player6</em>.<strong>ShowPositionControls</strong></span></span></td>
<td><span data-ttu-id="bc60d-360">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-360">Not available.</span></span> <span data-ttu-id="bc60d-361">Вы можете предоставить настраиваемые элементы управления или использовать <em>проигрыватель</em>. <strong>UIMODE</strong> , чтобы выбрать конфигурацию по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bc60d-361">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-362"><em>Player6</em>. <strong>Шовстатусбар</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-362"><em>Player6</em>.<strong>ShowStatusBar</strong></span></span></td>
<td><span data-ttu-id="bc60d-363">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-363">Not available.</span></span> <span data-ttu-id="bc60d-364">Вы можете предоставить настраиваемые элементы управления или использовать <em>проигрыватель</em>. <strong>UIMODE</strong> , чтобы выбрать конфигурацию по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bc60d-364">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-365"><em>Player6</em>. <strong>Шовтраккер</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-365"><em>Player6</em>.<strong>ShowTracker</strong></span></span></td>
<td><span data-ttu-id="bc60d-366">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-366">Not available.</span></span> <span data-ttu-id="bc60d-367">Вы можете предоставить настраиваемые элементы управления или использовать <em>проигрыватель</em>. <strong>UIMODE</strong> , чтобы выбрать конфигурацию по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bc60d-367">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-368"><em>Player6</em>. <strong>SourceLink</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-368"><em>Player6</em>.<strong>SourceLink</strong></span></span></td>
<td><span data-ttu-id="bc60d-369">Используйте <em>носитель</em>. <strong>саурцеурл</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-369">Use <em>Media</em>.<strong>sourceURL</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-370"><em>Player6</em>. <strong>Саурцепротокол</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-370"><em>Player6</em>.<strong>SourceProtocol</strong></span></span></td>
<td><span data-ttu-id="bc60d-371">Использовать <em>сеть</em>. <strong>саурцепротокол</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-371">Use <em>Network</em>.<strong>sourceProtocol</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-372"><em>Player6</em>. <strong>Стреамкаунт</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-372"><em>Player6</em>.<strong>StreamCount</strong></span></span></td>
<td><span data-ttu-id="bc60d-373">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-373">Not available.</span></span> <span data-ttu-id="bc60d-374">Используйте <em>элементы управления</em>. <strong>аудиолангуажекаунт</strong> для получения числа потоков звукового языка.</span><span class="sxs-lookup"><span data-stu-id="bc60d-374">Use <em>Controls</em>.<strong>audioLanguageCount</strong> to retrieve the number of audio language streams.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-375"><em>Player6</em>. <strong>Субпиктуреон</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-375"><em>Player6</em>.<strong>SubpictureOn</strong></span></span></td>
<td><span data-ttu-id="bc60d-376">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-376">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-377"><em>Player6</em>. <strong>Субпиктурестреамсаваилабле</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-377"><em>Player6</em>.<strong>SubpictureStreamsAvailable</strong></span></span></td>
<td><span data-ttu-id="bc60d-378">Недоступно</span><span class="sxs-lookup"><span data-stu-id="bc60d-378">Not available</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-379"><em>Player6</em>. <strong>Титлесаваилабле</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-379"><em>Player6</em>.<strong>TitlesAvailable</strong></span></span></td>
<td><span data-ttu-id="bc60d-380">Используйте следующую команду:<code>Player.Cdrom.playlist.count - 1</code></span><span class="sxs-lookup"><span data-stu-id="bc60d-380">Use the following:<code>Player.Cdrom.playlist.count - 1</code></span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-381"><em>Player6</em>. <strong>Тоталтитлетиме</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-381"><em>Player6</em>.<strong>TotalTitleTime</strong></span></span></td>
<td><span data-ttu-id="bc60d-382">Используйте <em>куррентмедиа</em>. <strong>Duration</strong> или <em>куррентмедиа</em>. <strong>дуратионстринг</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-382">Use <em>currentMedia</em>.<strong>duration</strong> or <em>currentMedia</em>.<strong>durationString</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-383"><em>Player6</em>. <strong>Транспарентатстарт</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-383"><em>Player6</em>.<strong>TransparentAtStart</strong></span></span></td>
<td><span data-ttu-id="bc60d-384">Используйте скрипт, чтобы задать значения высоты и ширины, чтобы сделать проигрыватель видимым или невидимым.</span><span class="sxs-lookup"><span data-stu-id="bc60d-384">Use script to specify the height and width values to make the player visible or invisible.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-385"><em>Player6</em>. <strong>UniqueID</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-385"><em>Player6</em>.<strong>UniqueID</strong></span></span></td>
<td><span data-ttu-id="bc60d-386">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-386">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-387"><em>Player6</em>. <strong>VideoBorder3D</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-387"><em>Player6</em>.<strong>VideoBorder3D</strong></span></span></td>
<td><span data-ttu-id="bc60d-388">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-388">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-389"><em>Player6</em>. <strong>Видеобордерколор</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-389"><em>Player6</em>.<strong>VideoBorderColor</strong></span></span></td>
<td><span data-ttu-id="bc60d-390">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-390">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-391"><em>Player6</em>. <strong>Видеобордервидс</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-391"><em>Player6</em>.<strong>VideoBorderWidth</strong></span></span></td>
<td><span data-ttu-id="bc60d-392">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-392">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-393"><em>Player6</em>. <strong>Том</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-393"><em>Player6</em>.<strong>Volume</strong></span></span></td>
<td><span data-ttu-id="bc60d-394">Используйте <em>Параметры</em>. <strong>Том</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-394">Use <em>Settings</em>.<strong>Volume</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-395"><em>Player6</em>. <strong>Волумесаваилабле</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-395"><em>Player6</em>.<strong>VolumesAvailable</strong></span></span></td>
<td><span data-ttu-id="bc60d-396">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-396">Not available.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="bc60d-397">В следующей таблице сравниваются методы объектной модели проигрывателя Windows Media версии 6,4 с объектной моделью проигрывателя Windows Media 7 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="bc60d-397">The following table compares the Windows Media Player version 6.4 object model methods with the Windows Media Player 7 or later object model.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bc60d-398">Метод проигрывателя Windows Media 6,4</span><span class="sxs-lookup"><span data-stu-id="bc60d-398">Windows Media Player 6.4 method</span></span></th>
<th><span data-ttu-id="bc60d-399">Проигрыватель Windows Media 7 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="bc60d-399">Windows Media Player 7 or later equivalent</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bc60d-400"><em>Player6</em>. <strong>AboutBox</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-400"><em>Player6</em>.<strong>AboutBox</strong></span></span></td>
<td><span data-ttu-id="bc60d-401">Используйте <em>проигрыватель</em>. <strong>versionInfo</strong> для получения версии проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="bc60d-401">Use <em>Player</em>.<strong>versionInfo</strong> to retrieve the version of Windows Media Player.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-402"><em>Player6</em>. <strong>Бакквардскан</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-402"><em>Player6</em>.<strong>BackwardScan</strong></span></span></td>
<td><span data-ttu-id="bc60d-403">Используйте <em>Параметры</em>. <strong>ставка</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-403">Use <em>Settings</em>.<strong>rate</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-404"><em>Player6</em>. <strong>Буттонактивате</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-404"><em>Player6</em>.<strong>ButtonActivate</strong></span></span></td>
<td><span data-ttu-id="bc60d-405">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-405">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-406"><em>Player6</em>. <strong>Буттонселектандактивате</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-406"><em>Player6</em>.<strong>ButtonSelectAndActivate</strong></span></span></td>
<td><span data-ttu-id="bc60d-407">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-407">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-408"><em>Player6</em>. <strong>Отмена</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-408"><em>Player6</em>.<strong>Cancel</strong></span></span></td>
<td><span data-ttu-id="bc60d-409">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-409">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-410"><em>Player6</em>. <strong>Чаптерплай</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-410"><em>Player6</em>.<strong>ChapterPlay</strong></span></span></td>
<td><span data-ttu-id="bc60d-411">Если вы уже воспроизводили указанный список воспроизведения заголовков, извлеките нужную главу в виде объекта мультимедиа, используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="bc60d-411">If already playing the specified title playlist, retrieve the desired chapter as a media object using the following syntax:</span></span>
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
<span data-ttu-id="bc60d-412">Затем укажите <em>Player</em>. <strong>куррентмедиа</strong> с использованием возвращенного объекта мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="bc60d-412">Then, specify <em>Player</em>.<strong>currentMedia</strong> using the media object returned.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-413"><em>Player6</em>. <strong>Чаптерплайаутостоп</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-413"><em>Player6</em>.<strong>ChapterPlayAutoStop</strong></span></span></td>
<td><span data-ttu-id="bc60d-414">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-414">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-415"><em>Player6</em>. <strong>Чаптерсеарч</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-415"><em>Player6</em>.<strong>ChapterSearch</strong></span></span></td>
<td><span data-ttu-id="bc60d-416">Если вы уже воспроизводили указанный список воспроизведения заголовков, извлеките нужную главу в виде объекта мультимедиа, используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="bc60d-416">If already playing the specified title playlist, retrieve the desired chapter as a media object using the following syntax:</span></span>
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
<span data-ttu-id="bc60d-417">Затем укажите <em>Player</em>. <strong>куррентмедиа</strong> с использованием возвращенного объекта мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="bc60d-417">Then, specify <em>Player</em>.<strong>currentMedia</strong> using the media object returned.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-418"><em>Player6</em>. <strong>Фастфорвард</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-418"><em>Player6</em>.<strong>FastForward</strong></span></span></td>
<td><span data-ttu-id="bc60d-419">Используйте <em>элементы управления</em>. <strong>фастфорвард</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-419">Use <em>Controls</em>.<strong>fastForward</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-420"><em>Player6</em>. <strong>Фастреверсе</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-420"><em>Player6</em>.<strong>FastReverse</strong></span></span></td>
<td><span data-ttu-id="bc60d-421">Используйте <em>элементы управления</em>. <strong>фастреверсе</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-421">Use <em>Controls</em>.<strong>fastReverse</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-422"><em>Player6</em>. <strong>Форвардскан</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-422"><em>Player6</em>.<strong>ForwardScan</strong></span></span></td>
<td><span data-ttu-id="bc60d-423">Используйте <em>Параметры</em>. <strong>ставка</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-423">Use <em>Settings</em>.<strong>rate</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-424"><em>Player6</em>. <strong>Жеталлгпрмс</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-424"><em>Player6</em>.<strong>GetAllGPRMs</strong></span></span></td>
<td><span data-ttu-id="bc60d-425">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-425">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-426"><em>Player6</em>. <strong>Жеталлспрмс</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-426"><em>Player6</em>.<strong>GetAllSPRMs</strong></span></span></td>
<td><span data-ttu-id="bc60d-427">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-427">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-428"><em>Player6</em>. <strong>Жетаудиолангуаже</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-428"><em>Player6</em>.<strong>GetAudioLanguage</strong></span></span></td>
<td><span data-ttu-id="bc60d-429">Используйте <em>элементы управления</em>. <strong>куррентаудиолангуаже</strong> получить код языка текущего аудио языка.</span><span class="sxs-lookup"><span data-stu-id="bc60d-429">Use <em>Controls</em>.<strong>currentAudioLanguage</strong> to retrieve the LCID of the current audio language.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-430"><em>Player6</em>. <strong>Жеткодекдескриптион</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-430"><em>Player6</em>.<strong>GetCodecDescription</strong></span></span></td>
<td><span data-ttu-id="bc60d-431">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-431">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-432"><em>Player6</em>. <strong>ЖеткодеЦинсталлед</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-432"><em>Player6</em>.<strong>GetCodecInstalled</strong></span></span></td>
<td><span data-ttu-id="bc60d-433">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-433">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-434"><em>Player6</em>. <strong>Жеткодекурл</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-434"><em>Player6</em>.<strong>GetCodecURL</strong></span></span></td>
<td><span data-ttu-id="bc60d-435">Используйте <em>ерроритем</em>. <strong>кустомурл</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-435">Use <em>ErrorItem</em>.<strong>customUrl</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-436"><em>Player6</em>. <strong>Жеткуррентентри</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-436"><em>Player6</em>.<strong>GetCurrentEntry</strong></span></span></td>
<td><span data-ttu-id="bc60d-437">Используйте скрипт для прохода по текущему списку воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="bc60d-437">Use script to loop through the current playlist.</span></span> <span data-ttu-id="bc60d-438">Используйте <em>носитель</em>. « <strong>идентично</strong> » для сравнения каждой записи в списке воспроизведения с <em>проигрывателем</em>. Объект <strong>куррентмедиа</strong> .</span><span class="sxs-lookup"><span data-stu-id="bc60d-438">Use <em>Media</em>.<strong>isIdentical</strong> to compare each entry in the playlist to the <em>Player</em>.<strong>currentMedia</strong> object.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-439"><em>Player6</em>. <strong>Жетмаркернаме</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-439"><em>Player6</em>.<strong>GetMarkerName</strong></span></span></td>
<td><span data-ttu-id="bc60d-440">Используйте <em>носитель</em>. <strong>жетмаркернаме</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-440">Use <em>Media</em>.<strong>getMarkerName</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-441"><em>Player6</em>. <strong>Жетмаркертиме</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-441"><em>Player6</em>.<strong>GetMarkerTime</strong></span></span></td>
<td><span data-ttu-id="bc60d-442">Используйте <em>носитель</em>. <strong>жетмаркертиме</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-442">Use <em>Media</em>.<strong>getMarkerTime</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-443"><em>Player6</em>. <strong>Жетмедиаинфостринг</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-443"><em>Player6</em>.<strong>GetMediaInfoString</strong></span></span></td>
<td><span data-ttu-id="bc60d-444">Используйте <em>носитель</em>. <strong>getItemInfo</strong>, <em>Media</em>. <strong>жетитеминфобятом</strong>и связанные с ними методы для получения метаданных.</span><span class="sxs-lookup"><span data-stu-id="bc60d-444">Use <em>Media</em>.<strong>getItemInfo</strong>, <em>Media</em>.<strong>getItemInfoByAtom</strong>, and their associated methods to retrieve metadata.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-445"><em>Player6</em>. <strong>Жетмедиапараметер</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-445"><em>Player6</em>.<strong>GetMediaParameter</strong></span></span></td>
<td><span data-ttu-id="bc60d-446">Использовать <em>список воспроизведения</em>. <strong>элемент</strong> , который извлекает элемент мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="bc60d-446">Use <em>Playlist</em>.<strong>item</strong> to retrieve a media item.</span></span> <span data-ttu-id="bc60d-447">Затем используйте <em>носитель</em>. <strong>getItemInfo</strong> для получения строки параметра.</span><span class="sxs-lookup"><span data-stu-id="bc60d-447">Then use <em>Media</em>.<strong>getItemInfo</strong> to retrieve the parameter string.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-448"><em>Player6</em>. <strong>Жетмедиапараметернаме</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-448"><em>Player6</em>.<strong>GetMediaParameterName</strong></span></span></td>
<td><span data-ttu-id="bc60d-449">Использовать <em>список воспроизведения</em>. <strong>элемент</strong> , который извлекает элемент мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="bc60d-449">Use <em>Playlist</em>.<strong>item</strong> to retrieve a media item.</span></span> <span data-ttu-id="bc60d-450">Затем используйте <em>носитель</em>. <strong>жетаттрибутенаме</strong> для получения строки параметра.</span><span class="sxs-lookup"><span data-stu-id="bc60d-450">Then use <em>Media</em>.<strong>getAttributeName</strong> to retrieve the parameter string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-451"><em>Player6</em>. <strong>Жетмореинфаурл</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-451"><em>Player6</em>.<strong>GetMoreInfoURL</strong></span></span></td>
<td><span data-ttu-id="bc60d-452">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-452">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-453"><em>Player6</em>. <strong>Жетнумберофчаптерс</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-453"><em>Player6</em>.<strong>GetNumberOfChapters</strong></span></span></td>
<td><span data-ttu-id="bc60d-454">Если в данный момент заголовок воспроизводится, используйте <em>куррентплайлист</em>. <strong>количество</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-454">If a title is currently playing, use <em>currentPlaylist</em>.<strong>count</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-455"><em>Player6</em>. <strong>Жетстреамграуп</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-455"><em>Player6</em>.<strong>GetStreamGroup</strong></span></span></td>
<td><span data-ttu-id="bc60d-456">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-456">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-457"><em>Player6</em>. <strong>Жетстреамнаме</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-457"><em>Player6</em>.<strong>GetStreamName</strong></span></span></td>
<td><span data-ttu-id="bc60d-458">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-458">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-459"><em>Player6</em>. <strong>Жетстреамселектед</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-459"><em>Player6</em>.<strong>GetStreamSelected</strong></span></span></td>
<td><span data-ttu-id="bc60d-460">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-460">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-461"><em>Player6</em>. <strong>Жетсубпиктурелангуаже</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-461"><em>Player6</em>.<strong>GetSubpictureLanguage</strong></span></span></td>
<td><span data-ttu-id="bc60d-462">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-462">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-463"><em>Player6</em>. <strong>Группы</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-463"><em>Player6</em>.<strong>GoUp</strong></span></span></td>
<td><span data-ttu-id="bc60d-464">Используйте <em>DVD-диск</em>. <strong>назад</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-464">Use <em>DVD</em>.<strong>back</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-465"><em>Player6</em>. <strong>Иссаундкарденаблед</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-465"><em>Player6</em>.<strong>IsSoundCardEnabled</strong></span></span></td>
<td><span data-ttu-id="bc60d-466">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-466">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-467"><em>Player6</em>. <strong>Лефтбуттонселект</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-467"><em>Player6</em>.<strong>LeftButtonSelect</strong></span></span></td>
<td><span data-ttu-id="bc60d-468">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-468">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-469"><em>Player6</em>. <strong>Ловербуттонселект</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-469"><em>Player6</em>.<strong>LowerButtonSelect</strong></span></span></td>
<td><span data-ttu-id="bc60d-470">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-470">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-471"><em>Player6</em>. <strong>Менукалл</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-471"><em>Player6</em>.<strong>MenuCall</strong></span></span></td>
<td><span data-ttu-id="bc60d-472">Используйте <em>DVD-диск</em>. <strong>титлемену</strong> или <em>DVD</em>. <strong>топмену</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-472">Use <em>DVD</em>.<strong>titleMenu</strong> or <em>DVD</em>.<strong>topMenu</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-473"><em>Player6</em>. <strong>Далее</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-473"><em>Player6</em>.<strong>Next</strong></span></span></td>
<td><span data-ttu-id="bc60d-474">Используйте <em>элементы управления</em>. <strong>Далее</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-474">Use <em>Controls</em>.<strong>next</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-475"><em>Player6</em>. <strong>Некстпгсеарч</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-475"><em>Player6</em>.<strong>NextPGSearch</strong></span></span></td>
<td><span data-ttu-id="bc60d-476">Используйте <em>элементы управления</em>. <strong>Далее</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-476">Use <em>Controls</em>.<strong>next</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-477"><em>Player6</em>. <strong>Открыть</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-477"><em>Player6</em>.<strong>Open</strong></span></span></td>
<td><span data-ttu-id="bc60d-478">Используйте <em>проигрыватель</em>. <strong>URL-адрес</strong> или <em>проигрыватель</em>. <strong>куррентмедиа</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-478">Use <em>Player</em>.<strong>URL</strong> or <em>Player</em>.<strong>currentMedia</strong>.</span></span> <span data-ttu-id="bc60d-479">Файлы всегда открываются асинхронно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-479">Files always open asynchronously.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-480"><em>Player6</em>. <strong>Приостановить</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-480"><em>Player6</em>.<strong>Pause</strong></span></span></td>
<td><span data-ttu-id="bc60d-481">Используйте <em>элементы управления</em>. <strong>приостановить</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-481">Use <em>Controls</em>.<strong>pause</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-482"><em>Player6</em>. <strong>Воспроизвести</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-482"><em>Player6</em>.<strong>Play</strong></span></span></td>
<td><span data-ttu-id="bc60d-483">Используйте <em>элементы управления</em>. <strong>воспроизвести</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-483">Use <em>Controls</em>.<strong>play</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-484"><em>Player6</em>. <strong>Предыдущий</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-484"><em>Player6</em>.<strong>Previous</strong></span></span></td>
<td><span data-ttu-id="bc60d-485">Используйте <em>элементы управления</em>. <strong>назад</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-485">Use <em>Controls</em>.<strong>previous</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-486"><em>Player6</em>. <strong>Превпгсеарч</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-486"><em>Player6</em>.<strong>PrevPGSearch</strong></span></span></td>
<td><span data-ttu-id="bc60d-487">Используйте <em>элементы управления</em>. <strong>назад</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-487">Use <em>Controls</em>.<strong>previous</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-488"><em>Player6</em>. <strong>Ресумефроммену</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-488"><em>Player6</em>.<strong>ResumeFromMenu</strong></span></span></td>
<td><span data-ttu-id="bc60d-489">Используйте <em>DVD-диск</em>. <strong>возобновить</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-489">Use <em>DVD</em>.<strong>resume</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-490"><em>Player6</em>. <strong>Ригхтбуттонселект</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-490"><em>Player6</em>.<strong>RightButtonSelect</strong></span></span></td>
<td><span data-ttu-id="bc60d-491">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-491">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-492"><em>Player6</em>. <strong>Сеткуррентентри</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-492"><em>Player6</em>.<strong>SetCurrentEntry</strong></span></span></td>
<td><span data-ttu-id="bc60d-493">Получите объект мультимедиа с помощью <em>куррентплайлист</em>. <strong>Item</strong>(<em>ентринумбер</em>).</span><span class="sxs-lookup"><span data-stu-id="bc60d-493">Retrieve a media object using <em>currentPlaylist</em>.<strong>item</strong>(<em>entryNumber</em>).</span></span> <span data-ttu-id="bc60d-494">Затем укажите полученный объект мультимедиа с помощью <em>элементов управления</em>. <strong>currentItem</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-494">Then, specify the retrieved media object using <em>Controls</em>.<strong>currentItem</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-495"><em>Player6</em>. <strong>ShowDialog</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-495"><em>Player6</em>.<strong>ShowDialog</strong></span></span></td>
<td><span data-ttu-id="bc60d-496">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-496">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-497"><em>Player6</em>. <strong>Стиллофф</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-497"><em>Player6</em>.<strong>StillOff</strong></span></span></td>
<td><span data-ttu-id="bc60d-498">Используйте <em>элементы управления</em>. <strong>воспроизвести</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-498">Use <em>Controls</em>.<strong>play</strong>.</span></span> <span data-ttu-id="bc60d-499">Кроме того, можно использовать <em>элементы управления</em>. <strong>Далее</strong> , если сейчас находится в режиме.</span><span class="sxs-lookup"><span data-stu-id="bc60d-499">Alternatively, use <em>Controls</em>.<strong>Next</strong> if currently in still mode.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-500"><em>Player6</em>. <strong>Завершение</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-500"><em>Player6</em>.<strong>Stop</strong></span></span></td>
<td><span data-ttu-id="bc60d-501">Используйте <em>элементы управления</em>. <strong>останавливается</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-501">Use <em>Controls</em>.<strong>stop</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-502"><em>Player6</em>. <strong>Стреамселект</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-502"><em>Player6</em>.<strong>StreamSelect</strong></span></span></td>
<td><span data-ttu-id="bc60d-503">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-503">Not available.</span></span> <span data-ttu-id="bc60d-504">Используйте <em>элементы управления</em>. <strong>куррентаудиолангуаже</strong> , чтобы указать поток на звуковом языке.</span><span class="sxs-lookup"><span data-stu-id="bc60d-504">Use <em>Controls</em>.<strong>currentAudioLanguage</strong> to specify an audio language stream.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-505"><em>Player6</em>. <strong>Тимеплай</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-505"><em>Player6</em>.<strong>TimePlay</strong></span></span></td>
<td><span data-ttu-id="bc60d-506">В корневом списке воспроизведения используйте <em>куррентплайлист</em>. <strong>элемент</strong>(<em>индекс</em>) для получения объекта мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="bc60d-506">From the root playlist, use <em>currentPlaylist</em>.<strong>item</strong>(<em>index</em>) to retrieve a media object.</span></span> <span data-ttu-id="bc60d-507">Затем установите объект мультимедиа в качестве текущего объекта с помощью <em>элементов управления</em>. <strong>currentItem</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-507">Then, set the media object as the current one using <em>Controls</em>.<strong>currentItem</strong>.</span></span> <span data-ttu-id="bc60d-508">Затем укажите <em>элементы управления</em>. <strong>CurrentPosition</strong> , используя значение времени в секундах.</span><span class="sxs-lookup"><span data-stu-id="bc60d-508">Then, specify <em>Controls</em>.<strong>currentPosition</strong> using a time value in seconds.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-509"><em>Player6</em>. <strong>Тимесеарч</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-509"><em>Player6</em>.<strong>TimeSearch</strong></span></span></td>
<td><span data-ttu-id="bc60d-510">Используйте <em>элементы управления</em>. <strong>CurrentPosition</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-510">Use <em>Controls</em>.<strong>currentPosition</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-511"><em>Player6</em>. <strong>Титлеплай</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-511"><em>Player6</em>.<strong>TitlePlay</strong></span></span></td>
<td><span data-ttu-id="bc60d-512">Если вы уже воспроизводили указанный список воспроизведения заголовков, извлеките нужную главу в виде объекта мультимедиа, используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="bc60d-512">If already playing the specified title playlist, retrieve the desired chapter as a media object using the following syntax:</span></span>
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
<span data-ttu-id="bc60d-513">Затем укажите <em>Player</em>. <strong>куррентмедиа</strong> с использованием возвращенного объекта мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="bc60d-513">Then, specify <em>Player</em>.<strong>currentMedia</strong> using the media object returned.</span></span><br/> <span data-ttu-id="bc60d-514">Кроме того, можно использовать <em>куррентплайлист</em>. <strong>элемент</strong> для получения объекта мультимедиа, а затем используйте возвращаемый объект мультимедиа для указания <em>элементов управления</em>. <strong>currentItem</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc60d-514">Alternatively, use <em>currentPlaylist</em>.<strong>item</strong> to retrieve a media object, and then use the media object returned to specify <em>Controls</em>.<strong>currentItem</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-515"><em>Player6</em>. <strong>Топпгсеарч</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-515"><em>Player6</em>.<strong>TopPGSearch</strong></span></span></td>
<td><span data-ttu-id="bc60d-516">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-516">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc60d-517"><em>Player6</em>. <strong>Уопвалид</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-517"><em>Player6</em>.<strong>UOPValid</strong></span></span></td>
<td><span data-ttu-id="bc60d-518">Недоступно</span><span class="sxs-lookup"><span data-stu-id="bc60d-518">Not available</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc60d-519"><em>Player6</em>. <strong>Уппербуттонселект</strong></span><span class="sxs-lookup"><span data-stu-id="bc60d-519"><em>Player6</em>.<strong>UpperButtonSelect</strong></span></span></td>
<td><span data-ttu-id="bc60d-520">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-520">Not available.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="bc60d-521">В следующей таблице сравниваются события объектной модели проигрывателя Windows Media версии 6,4 с объектной моделью проигрывателя Windows Media 7 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="bc60d-521">The following table compares the Windows Media Player version 6.4 object model events with the Windows Media Player 7 or later object model.</span></span>



| <span data-ttu-id="bc60d-522">Событие проигрывателя Windows Media 6,4</span><span class="sxs-lookup"><span data-stu-id="bc60d-522">Windows Media Player 6.4 event</span></span>  | <span data-ttu-id="bc60d-523">Проигрыватель Windows Media 7 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="bc60d-523">Windows Media Player 7 or later equivalent</span></span>                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc60d-524">*Player6*. **Буферизация**</span><span class="sxs-lookup"><span data-stu-id="bc60d-524">*Player6*.**Buffering**</span></span>         | <span data-ttu-id="bc60d-525">Используйте *проигрыватель*. **Буферизация**.</span><span class="sxs-lookup"><span data-stu-id="bc60d-525">Use *Player*.**Buffering**.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="bc60d-526">*Player6*. **Нажмите кнопку**</span><span class="sxs-lookup"><span data-stu-id="bc60d-526">*Player6*.**Click**</span></span>             | <span data-ttu-id="bc60d-527">Используйте *проигрыватель*. **Нажмите кнопку**</span><span class="sxs-lookup"><span data-stu-id="bc60d-527">Use *Player*.**Click**</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="bc60d-528">*Player6*. **Двойное** нажатие</span><span class="sxs-lookup"><span data-stu-id="bc60d-528">*Player6*.**DblClick**</span></span>          | <span data-ttu-id="bc60d-529">Используйте *проигрыватель*. **DoubleClick**</span><span class="sxs-lookup"><span data-stu-id="bc60d-529">Use *Player*.**DoubleClick**</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="bc60d-530">*Player6*. **Отключиться**</span><span class="sxs-lookup"><span data-stu-id="bc60d-530">*Player6*.**Disconnect**</span></span>        | <span data-ttu-id="bc60d-531">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-531">Not available.</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="bc60d-532">*Player6*. **Дисплаймодечанже**</span><span class="sxs-lookup"><span data-stu-id="bc60d-532">*Player6*.**DisplayModeChange**</span></span> | <span data-ttu-id="bc60d-533">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-533">Not available.</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="bc60d-534">*Player6*. **Двднотифи**</span><span class="sxs-lookup"><span data-stu-id="bc60d-534">*Player6*.**DVDNotify**</span></span>         | <span data-ttu-id="bc60d-535">*Проигрыватель*. **Домаинчанже** и *Player*. **Опенплайлистсвитч** — это события, связанные с DVD-дисками.</span><span class="sxs-lookup"><span data-stu-id="bc60d-535">*Player*.**DomainChange** and *Player*.**OpenPlaylistSwitch** are DVD-specific events.</span></span> <span data-ttu-id="bc60d-536">Кроме того, в зависимости от приложения могут применяться и другие события, связанные с списками воспроизведения, носителями и носителями компакт-дисков.</span><span class="sxs-lookup"><span data-stu-id="bc60d-536">Other events related to playlists, media, and CD-ROM media may apply as well depending on the application.</span></span>                        |
| <span data-ttu-id="bc60d-537">*Player6*. **EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="bc60d-537">*Player6*.**EndOfStream**</span></span>       | <span data-ttu-id="bc60d-538">Используйте *проигрыватель*. **Плайстате**.</span><span class="sxs-lookup"><span data-stu-id="bc60d-538">Use *Player*.**PlayState**.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="bc60d-539">*Player6*. **Ошибка при**</span><span class="sxs-lookup"><span data-stu-id="bc60d-539">*Player6*.**Error**</span></span>             | <span data-ttu-id="bc60d-540">Событие не изменено.</span><span class="sxs-lookup"><span data-stu-id="bc60d-540">The event is unchanged.</span></span> <span data-ttu-id="bc60d-541">Однако ошибки помещаются в очередь.</span><span class="sxs-lookup"><span data-stu-id="bc60d-541">Errors, however, are queued.</span></span> <span data-ttu-id="bc60d-542">Используйте объект **Error** с объектом **ерроритем** для получения сведений об ошибке из очереди.</span><span class="sxs-lookup"><span data-stu-id="bc60d-542">Use the **Error** object with the **ErrorItem** object to retrieve error information from the queue.</span></span> <span data-ttu-id="bc60d-543">См. пример кода в предыдущем разделе Обработка ошибок.</span><span class="sxs-lookup"><span data-stu-id="bc60d-543">See the example code in the preceding section, Error handling.</span></span> |
| <span data-ttu-id="bc60d-544">*Player6*. **Клавиша вниз**</span><span class="sxs-lookup"><span data-stu-id="bc60d-544">*Player6*.**KeyDown**</span></span>           | <span data-ttu-id="bc60d-545">Используйте *проигрыватель*. **Клавиша вниз**</span><span class="sxs-lookup"><span data-stu-id="bc60d-545">Use *Player*.**Keydown**</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="bc60d-546">*Player6*. **Нажатие клавиши**</span><span class="sxs-lookup"><span data-stu-id="bc60d-546">*Player6*.**KeyPress**</span></span>          | <span data-ttu-id="bc60d-547">Используйте *проигрыватель*. **Нажатие клавиши**</span><span class="sxs-lookup"><span data-stu-id="bc60d-547">Use *Player*.**KeyPress**</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="bc60d-548">*Player6*. **Клавиша вверх**</span><span class="sxs-lookup"><span data-stu-id="bc60d-548">*Player6*.**KeyUp**</span></span>             | <span data-ttu-id="bc60d-549">Используйте *проигрыватель*. **Клавиша вверх**</span><span class="sxs-lookup"><span data-stu-id="bc60d-549">Use *Player*.**KeyUp**</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="bc60d-550">*Player6*. **Маркерхит**</span><span class="sxs-lookup"><span data-stu-id="bc60d-550">*Player6*.**MarkerHit**</span></span>         | <span data-ttu-id="bc60d-551">Используйте *проигрыватель*. **Маркерхит**.</span><span class="sxs-lookup"><span data-stu-id="bc60d-551">Use *Player*.**MarkerHit**.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="bc60d-552">*Player6*. **MouseDown**</span><span class="sxs-lookup"><span data-stu-id="bc60d-552">*Player6*.**MouseDown**</span></span>         | <span data-ttu-id="bc60d-553">Используйте *проигрыватель*. **MouseDown**</span><span class="sxs-lookup"><span data-stu-id="bc60d-553">Use *Player*.**MouseDown**</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="bc60d-554">*Player6*. **Перемещение указателя**</span><span class="sxs-lookup"><span data-stu-id="bc60d-554">*Player6*.**MouseMove**</span></span>         | <span data-ttu-id="bc60d-555">Используйте *проигрыватель*. **Перемещение указателя**</span><span class="sxs-lookup"><span data-stu-id="bc60d-555">Use *Player*.**MouseMove**</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="bc60d-556">*Player6*. **MouseUp**</span><span class="sxs-lookup"><span data-stu-id="bc60d-556">*Player6*.**MouseUp**</span></span>           | <span data-ttu-id="bc60d-557">Используйте *проигрыватель*. **MouseUp**</span><span class="sxs-lookup"><span data-stu-id="bc60d-557">Use *Player*.**MouseUp**</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="bc60d-558">*Player6*. **Невстреам**</span><span class="sxs-lookup"><span data-stu-id="bc60d-558">*Player6*.**NewStream**</span></span>         | <span data-ttu-id="bc60d-559">Используйте *проигрыватель*. **Опенстатечанже**</span><span class="sxs-lookup"><span data-stu-id="bc60d-559">Use *Player*.**OpenStateChange**</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="bc60d-560">*Player6*. **Опенстатечанже**</span><span class="sxs-lookup"><span data-stu-id="bc60d-560">*Player6*.**OpenStateChange**</span></span>   | <span data-ttu-id="bc60d-561">Используйте *проигрыватель*. **Опенстатечанже**.</span><span class="sxs-lookup"><span data-stu-id="bc60d-561">Use *Player*.**OpenStateChange**.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="bc60d-562">*Player6*. **Плайстатечанже**</span><span class="sxs-lookup"><span data-stu-id="bc60d-562">*Player6*.**PlayStateChange**</span></span>   | <span data-ttu-id="bc60d-563">Используйте *проигрыватель*. **Плайстатечанже**.</span><span class="sxs-lookup"><span data-stu-id="bc60d-563">Use *Player*.**PlayStateChange**.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="bc60d-564">*Player6*. **Поситиончанже**</span><span class="sxs-lookup"><span data-stu-id="bc60d-564">*Player6*.**PositionChange**</span></span>    | <span data-ttu-id="bc60d-565">Используйте *проигрыватель*. **Поситиончанже**.</span><span class="sxs-lookup"><span data-stu-id="bc60d-565">Use *Player*.**PositionChange**.</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="bc60d-566">*Player6*. **Реадистатечанже**</span><span class="sxs-lookup"><span data-stu-id="bc60d-566">*Player6*.**ReadyStateChange**</span></span>  | <span data-ttu-id="bc60d-567">Используйте *проигрыватель*. **Плайстатечанже**.</span><span class="sxs-lookup"><span data-stu-id="bc60d-567">Use *Player*.**PlayStateChange**.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="bc60d-568">*Player6*. **Команду скрипта**</span><span class="sxs-lookup"><span data-stu-id="bc60d-568">*Player6*.**ScriptCommand**</span></span>     | <span data-ttu-id="bc60d-569">Используйте *проигрыватель*. **Команду скрипта**.</span><span class="sxs-lookup"><span data-stu-id="bc60d-569">Use *Player*.**ScriptCommand**.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="bc60d-570">*Player6*. **Предупреждение об ошибке**</span><span class="sxs-lookup"><span data-stu-id="bc60d-570">*Player6*.**Warning**</span></span>           | <span data-ttu-id="bc60d-571">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="bc60d-571">Not available.</span></span>                                                                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="bc60d-572">См. также</span><span class="sxs-lookup"><span data-stu-id="bc60d-572">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc60d-573">**Руководством по миграции объектной модели**</span><span class="sxs-lookup"><span data-stu-id="bc60d-573">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> <dt>

[<span data-ttu-id="bc60d-574">**Справочник по объектной модели для создания сценариев**</span><span class="sxs-lookup"><span data-stu-id="bc60d-574">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 





