---
title: Создание Web-Based презентаций
description: Создание Web-Based презентаций
ms.assetid: 60d8be10-ebed-4a4f-b17f-700475b51b34
keywords:
- Проигрыватель Windows Media, веб-презентации
- Объектная модель проигрывателя Windows Media, веб-презентации
- Объектная модель, веб-презентации
- Проигрыватель Windows Media Mobile, веб-презентации
- Элемент управления ActiveX проигрывателя Windows Media, веб-презентации
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, веб-презентации
- Элементы управления ActiveX, веб-презентации
- Веб-презентации, создание
- Создание веб-презентаций, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 117ee00164b50d319699f6e1d1806c4d8bf374af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332512"
---
# <a name="creating-web-based-presentations"></a><span data-ttu-id="a1833-112">Создание Web-Based презентаций</span><span class="sxs-lookup"><span data-stu-id="a1833-112">Creating Web-Based Presentations</span></span>

<span data-ttu-id="a1833-113">Элемент управления проигрывателя Windows Media позволяет легко создавать презентации на основе веб-презентаций, сочетая аудио и видео с HTML.</span><span class="sxs-lookup"><span data-stu-id="a1833-113">The Windows Media Player control lets you easily create Web-based slide-show presentations that combine audio and video with HTML.</span></span> <span data-ttu-id="a1833-114">Добавляя команды сценария типа "URL-адрес" в файлы мультимедиа, можно вызвать отображение определенных веб-страниц в указанном фрагменте браузера в определенное время при воспроизведении цифрового мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="a1833-114">By adding URL-type script commands to your media files, you can cause specified webpages to display in a specified Web browser frame at specific times during digital media playback.</span></span>

<span data-ttu-id="a1833-115">Проигрыватель Windows Media также имеет широкие возможности потоковой передачи мультимедиа, чтобы обеспечить эффективную доставку данных HTML по сети внутри одного потока или файла Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a1833-115">Windows Media Player also features rich media streaming to enable efficient delivery of HTML data over a network inside a single Windows Media stream or file.</span></span> <span data-ttu-id="a1833-116">Проигрыватель и сервер обрабатывали гладкую своевременную доставку аудио, видео и HTML в браузер.</span><span class="sxs-lookup"><span data-stu-id="a1833-116">The Player and server handle the smooth, timely delivery of audio, video, and HTML to the browser.</span></span> <span data-ttu-id="a1833-117">Как и в веб-презентациях, в которых не используется мультимедийная потоковая передача мультимедиа, внедренные команды сценариев отображают презентацию в указанном интервале.</span><span class="sxs-lookup"><span data-stu-id="a1833-117">Just as in Web presentations that do not use rich media streaming, embedded script commands render the presentation in a specified browser frame at specified times.</span></span>

<span data-ttu-id="a1833-118">Типичный макет для веб-презентаций использует два кадра.</span><span class="sxs-lookup"><span data-stu-id="a1833-118">A typical layout for Web-based presentations uses two frames.</span></span> <span data-ttu-id="a1833-119">Один кадр содержит веб-страницу, содержащую элемент управления проигрывателя Windows Media и отображающий его часть презентации.</span><span class="sxs-lookup"><span data-stu-id="a1833-119">One frame contains a webpage that embeds the Windows Media Player control and displays the video part of a presentation.</span></span> <span data-ttu-id="a1833-120">В другом фрейме отображаются веб-страницы, которые меняются в различные моменты времени при воспроизведении видео.</span><span class="sxs-lookup"><span data-stu-id="a1833-120">The other frame displays webpages that change at various times as the video plays.</span></span>

<span data-ttu-id="a1833-121">Если цифровые носители, сопровождающие веб-страницы, содержат только аудио, можно скрыть рамку, содержащую элемент управления проигрывателя Windows Media, установив для ширины значение 0.</span><span class="sxs-lookup"><span data-stu-id="a1833-121">If the digital media accompanying your webpages contains audio only, you can hide the frame that contains the Windows Media Player control by setting its width to zero.</span></span> <span data-ttu-id="a1833-122">Таким образом, звук может воспроизводиться в фоновом режиме, в то время как веб-страницы отображаются в полном окне браузера.</span><span class="sxs-lookup"><span data-stu-id="a1833-122">This way, the audio can play uninterrupted in the background while your webpages display in the full browser window.</span></span>

<span data-ttu-id="a1833-123">В следующих разделах описаны распространенные методы включения веб-презентаций.</span><span class="sxs-lookup"><span data-stu-id="a1833-123">The following sections describe common techniques for enabling Web-based presentations:</span></span>

-   [<span data-ttu-id="a1833-124">Перелистывание URL-адресов</span><span class="sxs-lookup"><span data-stu-id="a1833-124">URL Flipping</span></span>](url-flipping.md)
-   [<span data-ttu-id="a1833-125">Мультимедийная потоковая передача мультимедиа</span><span class="sxs-lookup"><span data-stu-id="a1833-125">Rich Media Streaming</span></span>](rich-media-streaming.md)

## <a name="related-topics"></a><span data-ttu-id="a1833-126">См. также</span><span class="sxs-lookup"><span data-stu-id="a1833-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1833-127">**Управление проигрывателем**</span><span class="sxs-lookup"><span data-stu-id="a1833-127">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




