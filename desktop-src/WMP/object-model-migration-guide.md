---
title: Руководством по миграции объектной модели
description: Руководством по миграции объектной модели
ms.assetid: 2fd4f7ec-36b0-49da-9a11-546dd41c7a98
keywords:
- Проигрыватель Windows Media, объектная модель
- Проигрыватель Windows Media, руководством по миграции
- Объектная модель проигрывателя Windows Media, руководством по миграции
- Объектная модель, руководством по миграции
- Элемент управления ActiveX проигрывателя Windows Media, руководством по миграции
- Элемент управления ActiveX, руководством по миграции
- Элемент управления ActiveX проигрывателя Windows Media Mobile, руководством по миграции
- Проигрыватель Windows Media Mobile, объектная модель
- Проигрыватель Windows Media Mobile, руководством по миграции
- рекомендации по миграции, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29c9be40e3cc252ed9461bcb18ea5bfed49bb58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068402"
---
# <a name="object-model-migration-guide"></a><span data-ttu-id="96714-113">Руководством по миграции объектной модели</span><span class="sxs-lookup"><span data-stu-id="96714-113">Object Model Migration Guide</span></span>

<span data-ttu-id="96714-114">В проигрывателе Windows Media 7 появилась новая объектная модель, которая предлагает обширный новый набор функциональных возможностей, которые можно использовать для улучшения веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="96714-114">Windows Media Player 7 introduced a new object model that offers a rich new set of functionality that you can use to enhance your webpages.</span></span> <span data-ttu-id="96714-115">В последующих версиях объектная модель версии 7 расширена с помощью дополнительных свойств, методов и событий.</span><span class="sxs-lookup"><span data-stu-id="96714-115">Subsequent versions have extended the version 7 object model with additional properties, methods, and events.</span></span> <span data-ttu-id="96714-116">Однако новая объектная модель существенно отличается от объектной модели проигрывателя Windows Media 6,4, поэтому необходимо понять, как обновить существующий код, если вы хотите поддерживать проигрыватель Windows Media 7 и более поздние версии в своих проектах.</span><span class="sxs-lookup"><span data-stu-id="96714-116">However, the new object model differs substantially from the Windows Media Player 6.4 object model, so you need to understand how to update your existing code if you want to support Windows Media Player 7 and later in your projects.</span></span>

<span data-ttu-id="96714-117">Пример, демонстрирующий, как определить версию проигрывателя Windows Media для пользователя и текущий браузер, см. в примере с именем "Обнаружение", который устанавливается вместе с этим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="96714-117">For a sample that demonstrates how to detect the user's Windows Media Player version and current browser, see the sample named "detection" that is installed with this SDK.</span></span> <span data-ttu-id="96714-118">Дополнительные сведения о примерах см. в разделе [Samples](samples.md).</span><span class="sxs-lookup"><span data-stu-id="96714-118">For more information about samples, see [Samples](samples.md).</span></span>

<span data-ttu-id="96714-119">Это руководством относится к новой объектной модели в качестве объектной модели проигрывателя Windows Media 7 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="96714-119">This guide refers to the new object model as the Windows Media Player 7 or later object model.</span></span> <span data-ttu-id="96714-120">Дополнительные сведения о функциях, доступных в каждой версии проигрывателя Windows Media, см. в разделе [Справочник по объектной модели для создания сценариев](object-model-reference-for-scripting.md).</span><span class="sxs-lookup"><span data-stu-id="96714-120">For details about which functionality is available in each version of Windows Media Player, see [Object Model Reference for Scripting](object-model-reference-for-scripting.md).</span></span>

<span data-ttu-id="96714-121">Эти проблемы с объектной моделью описаны в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="96714-121">These object model issues are covered by the following topics:</span></span>

-   [<span data-ttu-id="96714-122">Различия между объектными моделями</span><span class="sxs-lookup"><span data-stu-id="96714-122">Differences Between the Object Models</span></span>](differences-between-the-object-models.md)
-   [<span data-ttu-id="96714-123">Использование объектной модели проигрывателя Windows Media 7 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="96714-123">Using the Windows Media Player 7 or Later Object Model</span></span>](using-the-windows-media-player-7-or-later-object-model.md)
-   [<span data-ttu-id="96714-124">Обработка ошибок</span><span class="sxs-lookup"><span data-stu-id="96714-124">Error Handling</span></span>](error-handling.md)
-   [<span data-ttu-id="96714-125">Списки воспроизведения</span><span class="sxs-lookup"><span data-stu-id="96714-125">Playlists</span></span>](playlists.md)
-   [<span data-ttu-id="96714-126">Субтитры</span><span class="sxs-lookup"><span data-stu-id="96714-126">Closed Captioning</span></span>](closed-captioning.md)
-   [<span data-ttu-id="96714-127">ОПТИЧЕСКИ</span><span class="sxs-lookup"><span data-stu-id="96714-127">DVD</span></span>](dvd.md)
-   [<span data-ttu-id="96714-128">Сравнение подробной модели объектов</span><span class="sxs-lookup"><span data-stu-id="96714-128">Detailed Object Model Comparison</span></span>](detailed-object-model-comparison.md)

## <a name="related-topics"></a><span data-ttu-id="96714-129">См. также</span><span class="sxs-lookup"><span data-stu-id="96714-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96714-130">**Управление проигрывателем**</span><span class="sxs-lookup"><span data-stu-id="96714-130">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




