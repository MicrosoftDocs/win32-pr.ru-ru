---
title: Отображение веб-страниц в проигрывателе Windows Media
description: Отображение веб-страниц в проигрывателе Windows Media
ms.assetid: 73f6ea02-5855-4eb0-b064-cfb1abac37c3
keywords:
- Списки воспроизведения метафайлов Windows Media, отображение веб-страниц в проигрывателе Windows Media
- списки воспроизведения, отображение веб-страниц
- списки воспроизведения метафайлов, отображение веб-страниц
- Списки воспроизведения метафайлов Windows Media, веб-страницы
- списки воспроизведения, веб-страницы
- списки воспроизведения метафайлов, веб-страницы
- Отображение веб-страниц
- Проигрыватель Windows Media, отображение веб-страниц
- Проигрыватель Windows Media, веб-страницы
- Проигрыватель Windows Media, Хтмлвиев для показа веб-страниц
- Хтмлвиев, отображение веб-страниц
- Хтмлвиев, веб-страницы
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c6015b8d162b4734aa4e57fa7aaebe86e56c748
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332688"
---
# <a name="displaying-web-pages-in-windows-media-player"></a><span data-ttu-id="0f73b-115">Отображение веб-страниц в проигрывателе Windows Media</span><span class="sxs-lookup"><span data-stu-id="0f73b-115">Displaying Web Pages in Windows Media Player</span></span>

<span data-ttu-id="0f73b-116">Функция Хтмлвиев проигрывателя Windows Media позволяет поставщикам содержимого Интернета (ICP) использовать функцию **воспроизводимого** проигрывателя в полноэкранном режиме для показа веб-содержимого во время воспроизведения цифрового мультимедийного содержимого.</span><span class="sxs-lookup"><span data-stu-id="0f73b-116">The Windows Media Player HTMLView feature enables Internet content providers (ICPs) to use the **Now Playing** feature of the full mode Player to display Web-based content while digital media content is playing.</span></span> <span data-ttu-id="0f73b-117">(Хтмлвиев не поддерживается элементом управления проигрывателя Windows Media.) В прошлом в ICP отображались объявления в отдельных окнах веб-браузера («всплывающие рекламные сообщения») или пришлось добавлять на веб-страницы пользовательские проигрыватели Digital Media.</span><span class="sxs-lookup"><span data-stu-id="0f73b-117">(HTMLView is not supported by the Windows Media Player control.) In the past, ICPs had to display advertisements in separate Web browser windows (called "pop-up advertising") or had to add customized digital media players to their webpages.</span></span> <span data-ttu-id="0f73b-118">С помощью Хтмлвиев ICP может предоставить персонализированный и интегрированный интерфейс, созданный специально для проигрывателя Windows Media 9 и проигрывателя Windows Media 10, а также обеспечить воспроизведение мультимедийного содержимого в более ранних версиях проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0f73b-118">With HTMLView, ICPs can provide a personalized and integrated experience created specifically for Windows Media Player 9 Series and Windows Media Player 10, while ensuring that digital media content still plays back in earlier versions of Windows Media Player.</span></span>

<span data-ttu-id="0f73b-119">В этом разделе содержатся сведения об использовании Хтмлвиев, создании содержимого Хтмлвиев и устранении потенциальных проблем, которые могут возникнуть при использовании функции Хтмлвиев в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="0f73b-119">This section provides information about using HTMLView, creating HTMLView content, and resolving potential issues you may encounter when using the HTMLView feature in the following topics:</span></span>

-   [<span data-ttu-id="0f73b-120">Преимущества использования Хтмлвиев</span><span class="sxs-lookup"><span data-stu-id="0f73b-120">Advantages of Using HTMLView</span></span>](advantages-of-using-htmlview.md)
-   [<span data-ttu-id="0f73b-121">Создание презентации Хтмлвиев</span><span class="sxs-lookup"><span data-stu-id="0f73b-121">Creating an HTMLView Presentation</span></span>](creating-an-htmlview-presentation.md)
-   [<span data-ttu-id="0f73b-122">Добавление встроенного элемента управления проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="0f73b-122">Adding an Embedded Windows Media Player Control</span></span>](adding-an-embedded-windows-media-player-control.md)
-   [<span data-ttu-id="0f73b-123">Обеспечение открытия проигрывателем Windows Media содержимого Хтмлвиев</span><span class="sxs-lookup"><span data-stu-id="0f73b-123">Ensuring that Windows Media Player Opens the HTMLView Content</span></span>](ensuring-that-windows-media-player-opens-the-htmlview-content.md)
-   [<span data-ttu-id="0f73b-124">Проблемы с веб-страницей</span><span class="sxs-lookup"><span data-stu-id="0f73b-124">Web Page Issues</span></span>](web-page-issues.md)
-   [<span data-ttu-id="0f73b-125">Управление процессом воспроизведения</span><span class="sxs-lookup"><span data-stu-id="0f73b-125">Controlling the Playback Experience</span></span>](controlling-the-playback-experience.md)
-   [<span data-ttu-id="0f73b-126">Проблемы совместимости</span><span class="sxs-lookup"><span data-stu-id="0f73b-126">Compatibility Issues</span></span>](compatibility-issues.md)

## <a name="related-topics"></a><span data-ttu-id="0f73b-127">См. также</span><span class="sxs-lookup"><span data-stu-id="0f73b-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f73b-128">**Списки воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="0f73b-128">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> </dl>

 

 




