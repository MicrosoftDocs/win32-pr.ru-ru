---
title: Мультимедийная потоковая передача мультимедиа
description: Мультимедийная потоковая передача мультимедиа
ms.assetid: 3a48ee9a-5bf8-4cd0-9eed-07ec6da0f578
keywords:
- Проигрыватель Windows Media, веб-презентации
- Объектная модель проигрывателя Windows Media, веб-презентации
- Объектная модель, веб-презентации
- Проигрыватель Windows Media Mobile, веб-презентации
- Элемент управления ActiveX проигрывателя Windows Media, веб-презентации
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, веб-презентации
- Элементы управления ActiveX, веб-презентации
- Проигрыватель Windows Media, мультимедийная потоковая передача мультимедиа
- Объектная модель проигрывателя Windows Media, мультимедийная потоковая передача мультимедиа
- Объектная модель, многофункциональная потоковая передача мультимедиа
- Проигрыватель Windows Media Mobile, многофункциональная потоковая передача мультимедиа
- Элемент управления ActiveX проигрывателя Windows Media, мультимедийная потоковая передача мультимедиа
- Мобильный элемент управления ActiveX проигрывателя Windows Media, мультимедийная потоковая передача мультимедиа
- Элемент управления ActiveX, мультимедийная потоковая передача
- Веб-презентации, многофункциональная потоковая передача мультимедиа
- Создание веб-презентаций, многофункциональная потоковая передача мультимедиа
- Мультимедийная потоковая передача мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b454ef62f5f5aaaf424598d55d85c03684538c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778251"
---
# <a name="rich-media-streaming"></a><span data-ttu-id="b22ce-120">Мультимедийная потоковая передача мультимедиа</span><span class="sxs-lookup"><span data-stu-id="b22ce-120">Rich Media Streaming</span></span>

<span data-ttu-id="b22ce-121">Сложные веб-страницы содержат множество различных компонентов, которые обычно передаются отдельно.</span><span class="sxs-lookup"><span data-stu-id="b22ce-121">Complex webpages contain many different components that are normally transferred separately.</span></span> <span data-ttu-id="b22ce-122">При низком подключении такие страницы отображаются по одному элементу за раз и может занять несколько минут для полного вывода.</span><span class="sxs-lookup"><span data-stu-id="b22ce-122">On a slow connection, such pages display one piece at a time and may take several minutes to display completely.</span></span> <span data-ttu-id="b22ce-123">Это может помешать эффективно синхронизировать веб-страницы с цифровым носителем.</span><span class="sxs-lookup"><span data-stu-id="b22ce-123">This may prevent you from effectively synchronizing webpages with your digital media.</span></span> <span data-ttu-id="b22ce-124">Решением этой проблемы является мультимедийная потоковая передача мультимедиа, что означает добавление веб-страниц в поток цифрового мультимедиа, чтобы они доставлялись одновременно с аудио-или видеоданными.</span><span class="sxs-lookup"><span data-stu-id="b22ce-124">The solution to this problem is rich media streaming, which means adding your webpages to your digital media stream so that they are delivered at the same time as the audio or video data.</span></span>

<span data-ttu-id="b22ce-125">Насыщенная потоковая передача мультимедиа использует простой макет набора фреймов и работает точно так же, как обычное переключение URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="b22ce-125">Rich media streaming uses a simple frameset layout and behaves exactly like normal URL flipping.</span></span> <span data-ttu-id="b22ce-126">Как и при отражении URL-адресов, команды сценария URL-адреса, внедренные в цифровые мультимедийные потоки, используются для отображения содержимого в целевом кадре.</span><span class="sxs-lookup"><span data-stu-id="b22ce-126">Just as in URL flipping, URL script commands embedded in digital media streams are used to display the content in the target frame.</span></span> <span data-ttu-id="b22ce-127">Однако вместо того, чтобы указывать на страницы в Интернете, команды сценария URL-адреса используются в проигрывателе Windows Media 9 Series или более поздней версии для доступа к файлам в кэше Internet Explorer, где помещается потоковая передача содержимого HTML по мере их получения.</span><span class="sxs-lookup"><span data-stu-id="b22ce-127">Instead of pointing to pages on the Web, however, the URL script commands are used by Windows Media Player 9 Series or later to access files in the Internet Explorer cache where the streamed HTML content is placed as it is received.</span></span> <span data-ttu-id="b22ce-128">Как и при обычной перезаписи URL-адресов, можно написать обработчики событий, отвечающие на эти команды сценария URL-адреса, или позволить проигрывателю Windows Media обрабатывать все автоматически.</span><span class="sxs-lookup"><span data-stu-id="b22ce-128">Just as with normal URL flipping, you can write event handlers that respond to these URL script commands, or you can let the Windows Media Player control handle everything automatically.</span></span>

> [!Note]  
> <span data-ttu-id="b22ce-129">Любое содержимое HTML, доставленное через мультимедийную потоковую передачу мультимедиа, воспроизводится в зоне Интернет-безопасности и подлежит настройке безопасности браузера пользователя.</span><span class="sxs-lookup"><span data-stu-id="b22ce-129">Any HTML content delivered through rich media streaming is played back in the Internet security zone, and is subject to the user's browser security settings.</span></span>

 

<span data-ttu-id="b22ce-130">Дополнительные сведения о создании мультимедийных презентаций см. в статье Windows Media Format 9 серии или более поздней версии пакета SDK для Windows Media Encoder 9.</span><span class="sxs-lookup"><span data-stu-id="b22ce-130">For more information on creating rich media presentations, see the Windows Media Format 9 Series or later SDK and the Windows Media Encoder 9 Series SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b22ce-131">См. также</span><span class="sxs-lookup"><span data-stu-id="b22ce-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b22ce-132">**Создание Web-Based презентаций**</span><span class="sxs-lookup"><span data-stu-id="b22ce-132">**Creating Web-Based Presentations**</span></span>](creating-web-based-presentations.md)
</dt> <dt>

[<span data-ttu-id="b22ce-133">**Использование сценария для управления перелистыванием URL-адресов**</span><span class="sxs-lookup"><span data-stu-id="b22ce-133">**Using Script to Control URL Flipping**</span></span>](using-script-to-control-url-flipping.md)
</dt> </dl>

 

 




